---
title: Výkon rozhrania API plánovania projektov
description: Tento článok poskytuje informácie o výkonnostných testoch API plánovania projektu a identifikuje najlepšie postupy na optimálne použitie.
author: ruhercul
ms.date: 11/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ee1bd8e4412ee1d10f445628c5dc87cc9fa91d3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911201"
---
# <a name="project-schedule-api-performance"></a>Výkon rozhrania API plánovania projektov

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/nenaskladnené, nasadenie Lite – dohoda o proforma fakturácii, Project for the Web_

Tento článok poskytuje informácie o výkonnostných benchmarkoch rozhraní API (Project schedule application programming interfaces) a identifikuje najlepšie postupy na optimalizáciu používania.

## <a name="project-scheduling-service"></a>Služba Project Scheduling
Služba Project Scheduling je služba pre viacerých nájomníkov, ktorá beží v Microsoft Azure. Je navrhnutý tak, aby zlepšil interakciu poskytovaním rýchleho a plynulého zážitku, keď používatelia pracujú na projektoch. Toto zlepšenie sa dosiahne prijatím požiadaviek na zmenu, ich spracovaním a následným okamžitým vrátením výsledku. Služba asynchrónne pretrváva na Dataverse a neblokuje používateľov vo vykonávaní iných operácií.

Rozhrania API plánovania projektu sa pri spúšťaní požiadaviek, ktoré sú podrobnejšie opísané v neskorších častiach tohto článku, spoliehajú na službu plánovania projektu.

Rozhrania API harmonogramu projektu sú navrhnuté tak, aby spolupracovali s nasledujúcimi entitami štruktúry rozdelenia práce (WBS):

  - Project
  - Projektová úloha
  - Závislosť projektovej úlohy
  - Člen projektového tímu
  - Priradenie zdroja
  
Podporované sú predvolené polia aj vlastné polia. Ak nie je uvedené inak, sú podporované všetky bežné operácie, ako je vytváranie, aktualizácia a odstraňovanie. Ďalšie informácie nájdete v časti [Použite rozhrania API plánovania projektu na vykonávanie operácií s entitami plánovania](schedule-api-preview.md).

Ako súčasť API Project schedule bol pridaný vzor jednotiek práce. Tento vzor je známy ako OperationSet a možno ho použiť, keď sa musí v jednej transakcii spracovať niekoľko požiadaviek.

Nasledujúci obrázok ukazuje postup, ktorý partner zažije pri použití tejto funkcie.

![Postup Dataverse služby plánovania projektov.](./media/dataverse-project-scheduling-service-flow.png)

**Krok 1**: Klient vyvolá API ku koncovému bodu Open Data Protocol (OData) v Dataverse na vytvorenie OperationSet.

**Krok 2**: Po vytvorení nového OperationSet sa vráti hodnota **OperationSetId**.

**Krok 3**: Klient používa hodnotu **OperationSetId**, aby ste mohli zadať ďalšiu požiadavku rozhrania API Project schedule. Výsledkom je požiadavka na vytvorenie, aktualizáciu alebo odstránenie v entite plánovania. Po zadaní tejto požiadavky sa vykoná overenie metadát. Ak overenie zlyhá, požiadavka sa ukončí a vráti sa chyba.

**Kroky 4a–4c**: Tieto kroky predstavujú fázu ACCEPT. Klient vyvolá **ExecuteOperationSetV1**, ktoré odosiela všetky zmeny do služby plánovania projektu v jednej dávke. Služba plánovania projektu spúšťa svoje vlastné overenia žiadostí v dávke. Akékoľvek zlyhanie overenia zruší dávku a vráti výnimku volajúcemu. Ak je dávka úspešne prijatá službou plánovania projektu, stav množiny operácií sa aktualizuje tak, aby odrážal skutočnosť, že množinu operácií spracúva služba plánovania projektu.

**Krok 5**: Tento krok predstavuje fázu PERSIST. Služba plánovania projektu asynchrónne zapíše dávku Dataverse v transakcii. Ak je operácia zápisu úspešná, OperationSet sa označí ako **Dokončené**. Akékoľvek chyby vrátia späť transakciu a dávku a OperationSet sa označí ako **Zlyhalo**.

## <a name="performance-methodology"></a>Metodika výkonu
Čas vykonania je definovaný ako čas od volania do API **ExecuteOperationSetV1**, kým služba plánovania projektu nedokončí zápis do Dataverse. Všetky operácie sa spustia spolu 2 200-krát a zaznamenávajú sa merania času vykonania P99. Merajú sa operácie s jedným záznamom a hromadné operácie.

Pre operáciu s jedným záznamom obsahuje OperationSet jednu požiadavku. Pre hromadné operácie obsahuje 20, 50 alebo 100 požiadaviek. Každá hromadná veľkosť sa uvádza samostatne.

Tieto operácie bežia na nasadení UR 15 Project Operations Lite v Severnej Amerike.

## <a name="results"></a>Výsledky
### <a name="create-operations"></a>Vytvorenie operácií
#### <a name="single-record-create-operations"></a>Operácie vytvorenia jedného záznamu
Nasledujúca tabuľka zobrazuje časy vykonania pre vytvorenie jedného záznamu. Časy sú uvedené v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="2">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinné polia</th>
    <th class="tg-0lax">Všetky podporované polia</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">2.5</td>
    <td class="tg-0lax">3.78</td>
  </tr>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priradenie</td>
    <td class="tg-0lax">9.19</td>
    <td class="tg-0lax">9.19</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen tímu</td>
    <td class="tg-0lax">0.84</td>
    <td class="tg-0lax">4.2</td>
  </tr>
  <tr>
    <td class="tg-0lax">Závislosť</td>
    <td class="tg-0lax">8.84</td>
    <td class="tg-0lax">8.84</td>
  </tr>
</tbody>
</table>

#### <a name="bulk-create-operations"></a>Operácie hromadného vytvorenia
Nasledujúca tabuľka zobrazuje časy vykonania pre vytvorenie mnohých záznamov. Microsoft konkrétne meral časy vykonávania pre vytvorenie 20, 50 a 100 záznamov v rámci jednej OperationSet. Časy sú uvedené v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="6">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 záznamov</th>
    <th class="tg-0lax" colspan="2">50 záznamov</th>
    <th class="tg-0lax" colspan="2">100 záznamov</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinné polia</th>
    <th class="tg-0lax">Všetky podporované polia</th>
    <th class="tg-0lax">Povinné polia</th>
    <th class="tg-0lax">Všetky podporované polia</th>
    <th class="tg-0lax">Povinné polia</th>
    <th class="tg-0lax">Všetky podporované polia</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">19.92</td>
    <td class="tg-0lax">38.35</td>
    <td class="tg-0lax">36.67</td>
    <td class="tg-0lax">99.13</td>
    <td class="tg-0lax">116.77</td>
    <td class="tg-0lax">174.06</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priradenie</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">13.94</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">43.95</td>
    <td class="tg-0lax">69.38</td>
    <td class="tg-0lax">69.38</td>
  </tr>
  <tr>
    <td class="tg-0lax">Závislosť</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">30.04</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">77.82</td>
    <td class="tg-0lax">176.89</td>
    <td class="tg-0lax">176.89</td>
  </tr>
</tbody>
</table>

> [!NOTE] 
> Hromadné vytváranie operácií v entitách **Projekt** a **Člen tímu** nie sú zahrnuté v tejto tabuľke, pretože runtime pre tieto operácie sa podobá runtime, keď sa API na vytvorenie jedného záznamu volá viackrát. Tieto rozhrania API sa spúšťajú v Dataverse okamžite.

Nasledujúca ilustrácia zobrazuje graf časov realizácie pre entity **Úloha**, **Priradenie** a **Závislosť** entity, keď sa vytvorí 20, 50 a 100 záznamov a použijú sa všetky podporované polia.

![Vytvorte graf času vykonania záznamu.](./media/create-record-execution-time.png)

### <a name="update-operations"></a>Aktualizácia operácií
#### <a name="single-record-update-operations"></a>Operácie aktualizácie jedného záznamu
Nasledujúca tabuľka zobrazuje časy vykonania pre aktualizácie jedného záznamu. Časy sú uvedené v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="2">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinné polia </th>
    <th class="tg-0lax">Všetky podporované polia</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Project</td>
    <td class="tg-0lax">9.53</td>
    <td class="tg-0lax">13.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">8.82</td>
    <td class="tg-0lax">9.91</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen tímu</td>
    <td class="tg-0lax">9</td>
    <td class="tg-0lax">8.96</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Aktualizácia operácií na entity **Priradenia zdrojov** a **Závislosť projektovej úlohy** nie sú podporované.

#### <a name="bulk-update-operations"></a>Operácie hromadnej aktualizácie
Nasledujúca tabuľka zobrazuje časy vykonania pre aktualizácie mnohých záznamov. Microsoft konkrétne meral časy vykonávania pre aktualizácie 20, 50 a 100 záznamov v rámci jednej OperationSet. Časy sú uvedené v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="3">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="6">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax" colspan="2">20 záznamov</th>
    <th class="tg-0lax" colspan="2">50 záznamov</th>
    <th class="tg-0lax" colspan="2">100 záznamov</th>
  </tr>
  <tr>
    <th class="tg-0lax">Povinné polia</th>
    <th class="tg-0lax">Všetky podporované polia</th>
    <th class="tg-0lax">Povinné polia</th>
    <th class="tg-0lax">Všetky podporované polia</th>
    <th class="tg-0lax">Povinné polia</th>
    <th class="tg-0lax">Všetky podporované polia</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">8.91</td>
    <td class="tg-0lax">38.71</td>
    <td class="tg-0lax">20.92</td>
    <td class="tg-0lax">87.13</td>
    <td class="tg-0lax">36.68</td>
    <td class="tg-0lax">190.34</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen tímu</td>
    <td class="tg-0lax">20.52</td>
    <td class="tg-0lax">26.06</td>
    <td class="tg-0lax">41.93</td>
    <td class="tg-0lax">44.51</td>
    <td class="tg-0lax">38.63</td>
    <td class="tg-0lax">66.53</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Aktualizácia operácií na entity **Priradenia zdrojov** a **Závislosť projektovej úlohy** nie sú podporované.

Nasledujúca ilustrácia zobrazuje graf časov realizácie pre entity Úloha a Člen tímu, keď sa aktualizuje 20, 50 a 100 záznamov a použijú sa všetky podporované polia.

![Aktualizujte graf času vykonania záznamu.](./media/update-record-execution-time.png)

### <a name="delete-operations"></a>Operácie odstránenia
#### <a name="single-record-delete-operations"></a>Operácie vymazania jedného záznamu
Nasledujúca tabuľka zobrazuje časy vykonania pre vymazanie jedného záznamu. Časy sú uvedené v sekundách.

| Typ záznamu | Čas  |
|-------------|-------|
| Úloha        | 20.12 |
| Priradenie  | 10.86 |
| Člen tímu | 12.52 |
| Závislosť  | 20.89 |

> [!NOTE]
> Odstránenie operácií v entite **Projekt** nie sú podporované.

#### <a name="bulk-delete-operations"></a>Operácie hromadného odstránenia
Nasledujúca tabuľka zobrazuje časy vykonania pre vymazanie mnohých záznamov. Microsoft konkrétne meral časy vykonávania pre vymazanie 20, 50 a 100 záznamov v rámci jednej OperationSet. Časy sú uvedené v sekundách.

<table class="tg">
<thead>
  <tr>
    <th class="tg-0lax" rowspan="2">Typ&nbsp;&nbsp;&nbsp;záznamu</th>
    <th class="tg-0lax" colspan="3">Čas</th>
  </tr>
  <tr>
    <th class="tg-0lax">20 záznamov</th>
    <th class="tg-0lax">50 záznamov</th>
    <th class="tg-0lax">100 záznamov</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td class="tg-0lax">Úloha</td>
    <td class="tg-0lax">20.91</td>
    <td class="tg-0lax">67.43</td>
    <td class="tg-0lax">71.96</td>
  </tr>
  <tr>
    <td class="tg-0lax">Priradenie</td>
    <td class="tg-0lax">11.75</td>
    <td class="tg-0lax">25.79</td>
    <td class="tg-0lax">47.66</td>
  </tr>
  <tr>
    <td class="tg-0lax">Člen tímu</td>
    <td class="tg-0lax">9.78</td>
    <td class="tg-0lax">39.73</td>
    <td class="tg-0lax">24.33</td>
  </tr>
  <tr>
    <td class="tg-0lax">Závislosť</td>
    <td class="tg-0lax">24.61</td>
    <td class="tg-0lax">54.9</td>
    <td class="tg-0lax">109.16</td>
  </tr>
</tbody>
</table>

> [!NOTE]
> Odstránenie operácií v entite **Projekt** nie sú podporované.

Nasledujúca ilustrácia zobrazuje graf časov realizácie pre entity **Úloha**, **Priradenie** a **Člen tímu** a **Závislosti**, keď sa vymaže 20, 50 a 100 záznamov.

![Vymazať graf času vykonania záznamu.](./media/delete-record-execution-time.png)

## <a name="observations"></a>Pozorovania
Pre každú záznamovú operáciu bude rozhraniu API **ExecuteOperationSet** trvať odoslanie požiadavky do služby plánovania projektu približne 800 milisekúnd. Službe plánovania projektu potom trvá približne päť sekúnd spracovanie zaťaženia a volanie Dataverse. Zvyšný čas realizácie sa strávi spustením obchodnej logiky a zápisom údajov do databázy v Dataverse.

Keď sa vytvorí, aktualizuje alebo odstráni 100 záznamov, API **ExecuteOperationSet** trvá odoslanie požiadavky do služby plánovania projektu približne tri sekundy. Službe plánovania projektu potom trvá približne päť sekúnd spracovanie požiadaviek a volanie Dataverse. Hromadné operácie sú spoplatnené jednorazovým **poplatkom za služby plánovania projektu**, a to pre všetky záznamy v OperationSet. Hromadné operácie majú preto výrazne kratší priemerný čas vykonávania ako operácie s jedným záznamom.

## <a name="scenarios"></a>Scenáre
Nasledujúca tabuľka zobrazuje časy realizácie, keď sa rozhrania API plánovania projektu používajú na splnenie konkrétnych scenárov. Časy sú uvedené v sekundách.

| Scenár                                                                   | Čas  |
|----------------------------------------------------------------------------|-------|
| Vytvorte projekt, ktorý má 40 úloh.                                      | 36.01 |
| Vytvorte projekt, ktorý má 40 úloh a 20 závislostí.                  | 38.11 |
| Vytvorte projekt, ktorý má 40 úloh a 30 priradení.                   | 60.17 |
| Vytvorte projekt, ktorý má 40 úloh a 20 závislostí a 30 priradení. | 60.27 |

## <a name="best-practices"></a>Osvedčené postupy
Na základe výsledkov predchádzajúceho scenára fungujú rozhrania API lepšie v nasledujúcich podmienkach:

  - Zoskupte čo najviac operácií. Priemerná doba spustenia pre hromadné operácie je lepšia ako priemerná doba spustenia pre operácie s jedným záznamom. Čím menší je počet používaných operačných sád, tým rýchlejší bude priemerný čas vykonania.
  - Nastavte len minimálne atribúty, ktoré sú potrebné na splnenie vášho scenára. Buďte selektívni, pokiaľ ide o typy nepovinných polí zahrnutých do požiadavky OperationSet. Polia, ktoré obsahujú cudzie kľúče alebo súhrnné polia, negatívne ovplyvnia výkon.
