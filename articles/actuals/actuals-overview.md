---
title: Skutočné hodnoty
description: Táto téma poskytuje informácie o spôsobe práce so skutočnými hodnotami v Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084354"
---
# <a name="actuals"></a>Skutočné hodnoty 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte. Vytvárajú sa ako výsledok časových a výdavkových záznamov a účtovných záznamov a faktúr.

## <a name="journal-lines-and-time-submission"></a>Záznamy v účtovnom denníku a časový záznam

Viac informácií o časovom zázname nájdete na [Prehľad časového záznamu](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Čas a materiály

Keď je zadaný časový záznam prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.

### <a name="fixed-price"></a>Pevná cena

Keď je predložená časová položka prepojená s projektom ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.

### <a name="default-pricing"></a>Predvolená cena

Logika pre vytváranie predvolených cien býva ako záznam v účtovnom denníku. Hodnoty polí z časového záznamu sa skopírujú do záznamu v účtovnom denníku. Tieto hodnoty zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.

Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka** , sa používajú na určenie primeranej ceny v zázname v účtovnom denníku. K časovému záznamu môžete pridať vlastné pole. Ak chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočné hodnoty a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných hodnôt.

## <a name="journal-lines-and-basic-expense-submission"></a>Záznamy v účtovnom denníku a predloženie základných výdavkov

Viac informácií o zázname o výdavku nájdete na [Prehľad výdavkov](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Čas a materiály

Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.

### <a name="fixed-price"></a>Pevná cena

Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.

### <a name="default-pricing"></a>Predvolená cena

Logika zadávania predvolených cien pre výdavky je založená na kategórii výdavkov. Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka. Predvolene je však pre samotnú cenu čiastka zadaná používateľom nastavená priamo na súvisiace výdavkové záznamy v účtovnom denníku pre náklady a predaje.

Kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.

## <a name="use-entry-journals-to-record-costs"></a>Používanie účtovných záznamov na zaznamenávanie nákladov

Účtovné záznamy môžete použiť na zaznamenávanie nákladov alebo výnosov materiálov, poplatkov, času, výdavkov alebo daňových transakcií. Denníky možno použiť na nasledujúce účely:

- Zaznamenávanie skutočných nákladov na materiál a predaja projektu.
- Presun skutočných údajov transakcie z iného systému do Microsoft Dynamics 365 Project Operations.
- Záznam nákladov, ktoré sa vyskytli v inom systéme. Tieto náklady môžu zahŕňať náklady na obstaranie alebo subdodávky.

> [!IMPORTANT]
> Aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku. Preto iba používateľ, ktorý si je plne vedomý účtovných dopadov, ktoré môžu mať skutočné hodnoty na projekt, by mal na vytváranie skutočných hodnôt používať účtovné záznamy. Z dôvodu vplyvu tohto typu denníka by ste si mali starostlivo zvoliť, kto má prístup k vytváraniu účtovných záznamov.
## <a name="record-actuals-based-on-project-events"></a>Zaznamenanie skutočných údajov na základe projektových podujatí

Project Operations zaznamenáva finančné transakcie, ktoré nastanú počas projektu. Tieto transakcie sa zaznamenávajú ako skutočné údaje. Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a>Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu

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

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a>Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu

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
