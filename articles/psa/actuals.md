---
title: Prehľad skutočných hodnôt
description: Táto téma poskytuje informácie o skutočných údajoch projektu.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
ms.date: 08/03/2020
ms.topic: overview
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 7ab2638d82eb5ba928d95ca6a524a1566f21e1ba
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587605"
---
# <a name="actuals-overview"></a>Prehľad skutočných hodnôt

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte. Skutočné údaje projektu možno vystopovať späť do svojich zdrojových dokladov. Tieto zdrojové doklady zahŕňajú čas, výdavky a účtovné záznamy, ako aj faktúry.

![Ako vystopovať skutočné údaje projektov na zdrojové dokumenty.](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a>Odoslanie časovej položky

V PSA, keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy. Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj. Keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady. 

Logika pre zadávanie predvolených cien býva ako záznam v účtovnom denníku. Všetky hodnoty polí z časového záznamu sa skopírujú do účtovného denníka. Tieto polia zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku. 

Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka**, spôsobujú, že v zázname účtovného denníka sa predvolene zadá primeraná cena. Ak do časového záznamu pridáte vlastné pole a chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočná entita a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných údajov.

## <a name="submitting-an-expense-entry"></a>Odoslanie výdavkového záznamu

V PSA, keď je predložený výdavkový záznam položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy. Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj. Keď je predložený výdavkový záznam pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.

Logika pre zadávanie predvolených cien výdavkov je založená na kategórii výdavkov, ktorá je vybratá na stránke **Výdavkový záznam**. Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka. Pre samotnú cenu však čiastka zadaná používateľom je nastavená priamo na súvisiace výdavkové záznamy účtovného denníka pre náklady a predaje predvolene.

V aktuálnej verzii PSA, kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.

## <a name="using-entry-journals-to-record-costs"></a>Používanie účtovných záznamov na zaznamenávanie nákladov

V PSA vám účtovné záznamy umožňujú zaznamenávať náklady alebo výnosy materiálov, poplatkov, času, výdavkov alebo daňových transakcií. Denník má hlavičku, riadky a **Potvrdiť** akciu. Tu je niekoľko scenárov, v ktorých možno použiť denník:

- Musíte zaznamenať skutočné materiálne náklady a predaj na projekte.
- Musíte presunúť transakcie skutočných údajov z iného systému na PSA.
- Musíte zaznamenať náklady, ktoré sa vyskytli v inom systéme, ako napríklad obstarávacie alebo subdodávateľské náklady.

> [!IMPORTANT]
> Účtovné záznamy by mal na vytváranie skutočných hodnôt používať iba používateľ, ktorý si je plne vedomý účtovného dopadu skutočných hodnôt na projekt. Dôvodom je, že aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku. Z dôvodu dopadu tohto typu záznamu v účtovnom denníku buďte pri vytváraní účtovných záznamov primerane opatrní.     


## <a name="recording-actuals-based-on-project-events"></a>Zaznamenávanie skutočných údajov na základe projektových podujatí

PSA zaznamenáva finančné transakcie, ktoré nastanú počas projektu. Tieto transakcie sa zaznamenávajú ako **skutočné údaje**. Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.

**Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu**

<table>
<thead>
<tr>
<th rowspan="3">Udalosť</th>
<th colspan="4">Fakturovateľný alebo predaný projekt</th>
<th rowspan="3">Projekt v štádiu predpredaja</th>
<th rowspan="3">Interný projekt</th>
</tr>
<tr>
<th colspan="2">Čas a materiály</th>
<th colspan="2">Pevná cena</th>
</tr>
<tr>
<th>Skutočné hodnoty</th>
<th>Mena transakcie</th>
<th>Pevná cena</th>
<th>Mena transakcie</th>
</tr>
</thead>
<tbody>
<tr>
<td>Časový záznam je vytvorený.</td>
<td colspan="6">Žiadna aktivita v entite skutočných údajov</td>
</tr>
<tr>
<td>Časový záznam je predložený.</td>
<td colspan="6">Žiadna aktivita v entite skutočných údajov</td>
</tr>
<tr>
<td rowspan="2">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</td>
<td>Skutočné údaje nákladov</td>
<td>Meny zmluvnej jednotky</td>
<td rowspan="2">Skutočné údaje nákladov</td>
<td rowspan="2">Meny zmluvnej jednotky
<td rowspan="2">Skutočné údaje nákladov</td>
<td rowspan="2">Skutočné údaje nákladov</td>
</tr>
<tr>
<td>Nefakturované skutočné údaje predaja - Zahrnuté v cene</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="3">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</td>
<td>Skutočné údaje nákladov</td>
<td>Meny zmluvnej jednotky</td>
<td rowspan="3">Skutočné údaje nákladov</td>
<td rowspan="3">Meny zmluvnej jednotky</td>
<td rowspan="3">Skutočné údaje nákladov</td>
<td rowspan="3">Skutočné údaje nákladov</td>
</tr>
<tr>
<td>Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="2">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</td>
<td>Storno nefakturovaného predaj</td>
<td>Meny projektovej zmluvy</td>
<td rowspan="2">Fakturovaný predaj pre míľnik</td>
<td rowspan="2">Meny projektovej zmluvy</td>
<td rowspan="2">Nevzťahuje sa</td>
<td rowspan="2">Nevzťahuje sa</td>
</tr>
<tr>
<td>Fakturovaný predaj</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="3">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</td>
<td>Storno nefakturovaného predaj</td>
<td>Meny projektovej zmluvy</td>
<td rowspan="3">Nevzťahuje sa</td>
<td rowspan="3">Nevzťahuje sa</td>
<td rowspan="3">Nevzťahuje sa</td>
<td rowspan="3">Nevzťahuje sa</td>
</tr>
<tr>
<td>Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="2">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</td>
<td>Storno fakturovaného predaja</td>
<td>Meny projektovej zmluvy</td>
<td rowspan="5">
<ul>
<li>Storno fakturovaného predaja pre míľnik</li>
<li>Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></li>
</ul>
</td>
<td rowspan="5">Meny projektovej zmluvy</td>
<td rowspan="5">Nevzťahuje sa</td>
<td rowspan="5">Nevzťahuje sa</td>
</tr>
<tr>
<td>Fakturovaný predaj</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="3">Faktúra je opravená na zníženie množstva zahrnutého v cene.</td>
<td>Storno fakturovaného predaja</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Fakturovaný predaj pre nové množstvo</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</td>
<td>Meny projektovej zmluvy</td>
</tr>
</tbody>
</table>

**Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu**

<table>
<thead>
<tr>
<th rowspan="3">Udalosť</th>
<th colspan="4">Fakturovateľný alebo predaný projekt</th>
<th rowspan="3">Projekt v štádiu predpredaja</th>
<th rowspan="3">Interný projekt</th>
</tr>
<tr>
<th colspan="2">Čas a materiály</th>
<th colspan="2">Pevná cena</th>
</tr>
<tr>
<th>Skutočné hodnoty</th>
<th>Mena transakcie</th>
<th>Pevná cena</th>
<th>Mena transakcie</th>
</tr>
</thead>
<tbody>
<tr>
<td>Časový záznam je vytvorený.</td>
<td colspan="6">Žiadna aktivita v entite skutočných údajov</td>
</tr>
<tr>
<td>Časový záznam je predložený.</td>
<td colspan="6">Žiadna aktivita v entite skutočných údajov</td>
</tr>
<tr>
<td rowspan="4">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</td>
<td>Skutočné údaje nákladov</td>
<td>Meny zmluvnej jednotky</td>
<td rowspan="4">Skutočné údaje nákladov</td>
<td rowspan="4">Meny zmluvnej jednotky</td>
<td rowspan="4">Skutočné údaje nákladov</td>
<td rowspan="4">Skutočné údaje nákladov</td>
</tr>
<tr>
<td>Nefakturované skutočné údaje predaja - Zahrnuté v cene</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Náklady zdrojovej jednotky</td>
<td>Zdrojová mena jednotky</td>
</tr>
<tr>
<td>Predaj medzi organizáciami</td>
<td>Meny zmluvnej jednotky</td>
</tr>
<tr>
<td rowspan="5">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</td>
<td>Skutočné údaje nákladov</td>
<td>Meny zmluvnej jednotky</td>
<td rowspan="5">Skutočné údaje nákladov</td>
<td rowspan="5">Meny zmluvnej jednotky</td>
<td rowspan="5">Skutočné údaje nákladov</td>
<td rowspan="5">Skutočné údaje nákladov</td>
</tr>
<tr>
<td>Náklady zdrojovej jednotky</td>
<td>Zdrojová mena jednotky</td>
</tr>
<tr>
<td>Predaj medzi organizáciami</td>
<td>Meny zmluvnej jednotky</td>
</tr>
<tr>
<td>Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="2">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</td>
<td>Storno nefakturovaného predaj</td>
<td>Meny projektovej zmluvy</td>
<td rowspan="2">Fakturovaný predaj pre míľnik</td>
<td rowspan="2">Meny projektovej zmluvy</td>
<td rowspan="2">Nevzťahuje sa</td>
<td rowspan="2">Nevzťahuje sa</td>
</tr>
<tr>
<td>Fakturovaný predaj</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="3">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</td>
<td>Storno nefakturovaného predaj</td>
<td>Meny projektovej zmluvy</td>
<td rowspan="3">Nevzťahuje sa</td>
<td rowspan="3">Nevzťahuje sa</td>
<td rowspan="3">Nevzťahuje sa</td>
<td rowspan="3">Nevzťahuje sa</td>
</tr>
<tr>
<td>Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="2">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</td>
<td>Storno fakturovaného predaja</td>
<td>Meny projektovej zmluvy</td>
<td rowspan="5">
<ul>
<li>Storno fakturovaného predaja pre míľnik</li>
<li>Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></li>
</ul>
</td>
<td rowspan="5">Meny projektovej zmluvy</td>
<td rowspan="5">Nevzťahuje sa</td>
<td rowspan="5">Nevzťahuje sa</td>
</tr>
<tr>
<td>Fakturovaný predaj</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td rowspan="3">Faktúra je opravená na zníženie množstva zahrnutého v cene.</td>
<td>Storno fakturovaného predaja</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Fakturovaný predaj pre nové množstvo</td>
<td>Meny projektovej zmluvy</td>
</tr>
<tr>
<td>Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</td>
<td>Meny projektovej zmluvy</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
