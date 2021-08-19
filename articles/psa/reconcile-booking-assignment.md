---
title: Zmierenie zdrojov a priradenia
description: Táto téma poskytuje informácie o skutočných údajoch.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 264271a5be63cb2e51f175595a48bef5fbff0a42a37795c85dd5b4725deec35e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995150"
---
# <a name="reconcile-bookings-and-assignments"></a>Zmierenie zdrojov a priradenia

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projektové rezervácie člena projektového tímu a úlohy projektových úloh sú voľne spojené. Preto prostriedok môže mať úlohy priradenia, ktoré nezodpovedajú rezervácie a rezervácie, ktoré nezodpovedajú priradenia úloh. V ideálnom prípade by mali byť rezervácie projektov a úlohy zarovnané tak, aby zdroje zaplnili kapacity na plnenie úloh. Skutočnosťou však je, že rezervácie sa môžu vyskytnúť na základe dostupnosti, pričom časovanie úloh sa môže zmeniť, pretože projekt pokračuje prostredníctvom jeho životného cyklu. Preto voľné spojenia umožňujú flexibilitu.

Z dôvodu voľného spojenia projektových rezervácií a priradenia úloh je na entite projektu zahrnutá karta **Vyrovnanie**. Táto karta pomáha projektovým správcom porovnať rezervácie členov tímu a ich priradenia pre ich projektový tím.

Pre každého menovaného člena tímu karta **Vyrovnanie** zobrazuje rezervácie a priradenia k samostatnému priradeniu úlohy. To zobrazuje hodiny v bunkách, ktoré môžu reprezentovať časové periódy od mesiacov ku dňom.

V poli **Časový rozsah** môžete vybrať položku **Mesiac**, **Týždeň** alebo **Deň**. Predvolene je vybratá možnosť **Týždeň**. Predvolenú hodnotu však môžete zmeniť výberom tlačidla **Nastavenia**. Keď je karta **Vyrovnanie** otvorená, zobrazuje aktuálny dátum, ale môžete použiť ovládací prvok kalendára na posun dopredu alebo dozadu v čase. Ak má projekt počiatočný dátum, ktorý je v budúcnosti, na karte sa zobrazí dátum otvorenia. Ovládací prvok kalendára má tiež možnosti, ktoré umožňujú presunúť do dátumu začatia a ukončenia projektu.

Na zobrazenie podrobností o rezerváciách tohto prostriedku môžete použiť ovládacie prvky rozbalenia na každom prostriedku. Môžete tiež rozbaliť priradenia každého prostriedku na úroveň jednotlivých úloh.

Spodná časť karty **Vyrovnanie** zobrazuje celkový čistý súčet projektu a karta obsahuje aj stĺpec celkom. Pre každý zdroj karta vypočíta rozdiel medzi rezerváciami člena tímu v projekte a súhrnom priradení úloh člena tímu. V ideálnom prípade by tento rozdiel mal byť 0 (nula). Inými slovami, nemal by existovať žiadny rozdiel medzi rezerváciou zdroja a jeho priradeniami. Všetky rozdiely sú označené farbou a tieňovaním na vyvolanie dvoch podmienok:

- **Nedostatok rezervácií** – Nedostatky rezervácie sa objavia, keď má zdroj viac priradení než rezervácie. Keďže táto kapacita nebola vyhradená, projektový manažér ho môže napraviť rozšírením rezervácií prostriedkov na krytie deficitu.
- **Rozšírené rezervácie** – Nadmerná rezervácia nastane, keď sa zdroj zarezervuje do projektu, no nebude priradený k úlohám. Táto podmienka môže byť prijateľná, napríklad ak bol zdroj rezervovaný pred priradením úlohy. V ostatných prípadoch však zdroj nemusí byť naplánovaný na priradenie k úlohe. V takýchto prípadoch by mal projektový manažér zvážiť zrušenie rezervácií prostriedku tak, aby sa kapacita mohla použiť pre iný projekt.

> [!NOTE]
> Legenda pre tieto podmienky môže byť skrytá, aby uvoľnila viac miesta mriežke. V tomto prípade môžete zobraziť legendu tak, že vyberiete tlačidlo **Nastavenia**.

V niektorých prípadoch, keď je pole **Časový rozsah** nastavený na úroveň, ktorá je vyššia ako **Deň**, rozdiely sa môžu vypočítať ako 0 (nula). Napríklad na úrovni **Mesiac** môže byť čistý rozdiel zdroja 0 (nula) na označenie, že rezervácie sa rovná priradeniu. Avšak, ak si prezriete čas na úrovni **týždňa**, môžete vidieť, že existujú úlohy nula hodín a rezervácie 40 hodín v prvom týždni mesiaca, ale úlohy 40 hodín a rezervácie nula hodín v druhom týždni mesiaca. Hoci celkové rezervácie a úlohy za mesiac sú rovnaké, líšia sa podľa týždňa.

Keď zobrazíte čas na vyšších časových úrovniach, bunky na karte **Vyrovnanie** majú indikátor bunky, ktorý vám oznámi, že existujú rozdiely na nižších časových úrovniach. Napríklad na nasledujúcom obrázku sa v bunke zobrazí indikátor bunky pre mesiac október 2018 pre prostriedok s názvom Dana Mrázová. Preto môžete vidieť, že aj keď zdroj rezervácie a priradenia sú rovnaké, keď sú agregované na úrovni **mesiaca**, nezhodujú sa na nižších úrovniach.

![Nesúlad rezervácií a úloh na mesačnej úrovni.](media/reconcile-assignments-01.JPG)

Dvojitým kliknutím na bunku priblížite ďalšiu nižšiu úroveň a zobrazíte rozdiel. Napríklad, ak dvakrát kliknete na október 2018 rozdiel pre Dana Mrázová si zobrazíte na úroveň **Týždeň**. Potom môžete vidieť, že zdroj má rezerváciu 16 hodín, ale žiadne úlohy v prvých dvoch týždňoch v októbri, a 16 hodín úloh, ale žiadne rezervácie v treťom týždni v októbri.

![Nesúlad rezervácií a úloh na týždennej úrovni.](media/reconcile-assignments-02.JPG)

Môžete kliknúť pravým tlačidlom myši na bunku a zmenšiť tak ďalšiu vyššiu úroveň. Indikátor bunky môžete vypnúť aj tak, že vyberiete tlačidlo **Nastavenia**. 

Môžete tiež použiť tlačidlá **Predošlé** a **Nasledujúce** nad mriežkou, aby ste prešli rozdielmi v projekte. Ak chcete použiť tieto tlačidlá, musíte najprv vybrať zdroj. Ak chcete prejsť na ďalší rozdiel medzi rezerváciami a priradeniami pre daný prostriedok, vyberte možnosť **Ďalej**. Ak chcete prejsť na predchádzajúci rozdiel, vyberte položku **Predchádzajúce**.

V situáciách, kedy máte priradenia úloh pre prostriedok, no nemáte rezervácie, môžete vybrať súhrnný nedostatok rezervácií a kliknúť na položku **Rozšíriť rezerváciu**. Potom môžete vidieť rezerváciu, ktorá je potrebná na riešenie nedostatku prostriedku. Môžete si tiež prezrieť rezervácie zdrojov na aktuálnom projekte a ďalších projektoch. Výberom možnosti **OK** vytvoríte rezerváciu prostriedku bez ohľadu na aktuálnu dostupnosť. Projektový manažér alebo správca zdrojov potom môže pomocou tabule plánovania spravovať všetky situácie, v ktorých je zdroj prerezervovaný nad rámec jeho kapacity v dôsledku jeho nadmernej rezervácie.

## <a name="managing-with-time-zones"></a>Správa pomocou časových pásiem
Na zabezpečenie presných a predvídateľných výsledkov pri používaní rozšírenia rezervácie je potrebné splniť dva kľúčové predpoklady:  

- Používateľ musí nakonfigurovať časové pásmo svojho zariadenia tak, aby sa zhodovalo s časovým pásmom definovaným v nastaveniach prispôsobenia vášho systému.
 
  ![Nastavenia časového pásma v systéme Windows 10.](media/reconcile-assignments-03.png)

  ![Nastavenia časového pásma v nastaveniach prispôsobenia.](media/reconcile-assignments-04.png)
 
- Rezervovateľný zdroj musí mať najmenej jednu minútu pracovného času, ktorá sa prekrýva s obrysmi, ktoré sa používajú na definovanie požadovaného rozšírenia. Nasledujúci príklad napríklad zobrazuje zdroje na preskúmanie s pracovnými hodinami, ktoré spadajú medzi 9:00 a 19:00. 

  ![Porovnanie obrysov zdrojov.](media/reconcile-assignments-05.png)

Nasledujúca tabuľka zobrazuje:

- Šablóna kalendára projektu.
- Zdroj A: Tento zdroj má rovnaký kalendár a je v rovnakom časovom pásme ako projekt. Čas začiatku rezervácie bude 9.00.
- Zdroje B: Tento zdroj sa nachádza v inom časovom pásme, ako je projekt, a preto sa začína v 7.00 v jeho časovom pásme. Rezervácie sa však začnú o 9.00, pretože ide o najskorší čas začiatku obrysu priradenia.
- Zdroje C a D: Zdroje sa nachádzajú aj v rôznych časových pásmach, ktoré sa odlišujú od seba a od projektu, a ktorých rezervácie sa nezačínajú skôr, ako sú príslušné dostupné časy začiatku.

|Entity  |Kalendár  |
|-|-|
|Šablóna kalendára projektu   | ![kalendár projektu.](media/reconcile-assignments-06.png) |
|Zdroj A  | ![Kalendár zdroja A.](media/reconcile-assignments-06.png) |
|Zdroj B  |  ![Kalendár zdroja B.](media/reconcile-assignments-07.png) |
|Zdroj C  |  ![Kalendár zdroja C.](media/reconcile-assignments-08.png) |
|Zdroj D  | ![Kalendár zdroja D.](media/reconcile-assignments-09.png)  |
 
Keď prejdete na zobrazenie odsúhlasenia, zobrazia sa priradenia zdrojov a súvisiace rezervačné nedostatky.
 ![Zobrazenie odsúhlasenia pred predĺžením.](media/reconcile-assignments-10.png)

Po vykonaní funkcie rozšírenia rezervácie na každom zdroji sa rezervácie úspešne rozšíria pre každý zdroj. Dôvodom je, že pracovná doba každého zdroja sa prekrývala s obrysmi nedostatku.
 ![Zobrazenie odsúhlasenia po rozšírení rezervácie.](media/reconcile-assignments-11.png) 

Bližší pohľad na podrobnosti rezervácií však ukazuje rozdiely v počiatočnom čase rezervácií. Rezervácie sa nezačnú skôr, ako je čas začiatku obrysu priradenia, a nie skôr, ako je čas začiatku, ktorý je k dispozícii pre zdroj.
 ![Nové rezervácie zdrojov na tabuli plánovania.](media/reconcile-assignments-12.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]