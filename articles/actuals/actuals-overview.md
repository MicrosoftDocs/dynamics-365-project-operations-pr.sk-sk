---
title: Skutočné hodnoty
description: Táto téma poskytuje informácie o tom, ako pracovať so skutočnými údajmi v aplikácii Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996630"
---
# <a name="actuals"></a>Skutočné hodnoty 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Skutočné hodnoty predstavujú skontrolované a schválené finančné údaje a naplánovaný postup projektu. Vytvárajú sa na základe schválenia časových položiek, výdavkových položiek, položiek použitia materiálu, účtovných záznamov a faktúr.

## <a name="journal-lines-and-time-submission"></a>Záznamy v účtovnom denníku a časový záznam

Viac informácií o časovom zázname nájdete na [Prehľad časového záznamu](../time/time-entry-overview.md).

### <a name="time-and-materials"></a>Čas a materiály

Keď je zadaný časový záznam prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.

### <a name="fixed-price"></a>Pevná cena

Keď je predložená časová položka prepojená s projektom ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.

### <a name="default-pricing"></a>Predvolená cena

Logika pre vytváranie predvolených cien býva ako záznam v účtovnom denníku. Hodnoty polí z časového záznamu sa skopírujú do záznamu v účtovnom denníku. Tieto hodnoty zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.

Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Zdrojová jednotka** sa používajú na určenie primeranej ceny v zázname v účtovom denníku. K časovému záznamu môžete pridať vlastné pole. Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**. Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií. Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-basic-expense-submission"></a>Záznamy v účtovnom denníku a predloženie základných výdavkov

Viac informácií o zázname o výdavku nájdete na [Prehľad výdavkov](../expense/expense-overview.md).

### <a name="time-and-materials"></a>Čas a materiály

Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.

### <a name="fixed-price"></a>Pevná cena

Keď je predložený základný výdavkový záznam prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.

### <a name="default-pricing"></a>Predvolená cena

Logika zadávania predvolených cien pre výdavky je založená na kategórii výdavkov. Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený a mena sú všetky použité na určenie príslušného cenníka. Polia, ktoré ovplyvňujú predvolené ceny, ako je **Kategória transakcie** a **Jednotka**, sa používajú na určenie primeranej ceny v zázname v účtovom denníku. Funguje to však iba vtedy, keď je v cenníku cenová metóda **Cena za jednotku**. Ak je cenová metóda **V rámci nákladov** alebo **Prirážka nad rámec nákladov**, pre náklady sa použije cena zadaná pri vytvorení položky výdaja a cena predaja v zázname v účtovnom denníku sa vypočíta na základe metódy oceňovania. 

Do záznamu výdavkov môžete pridať vlastné pole. Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**. Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií. Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="journal-lines-and-material-usage-log-submission"></a>Záznamy v účtovnom denníku a odoslanie denníka použitia materiálu

Viac informácií o zadávaní výdavkov nájdete v článku [Denník použitia materiálu](../material/material-usage-log.md).

### <a name="time-and-materials"></a>Čas a materiály

Keď je zadaná položka denníka použitia materiálu spojená s projektom, ktorý je namapovaný na riadok zmluvy s časom a materiálom, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a druhý pre nevyfakturovaný predaj.

### <a name="fixed-price"></a>Pevná cena

Keď je odoslaný záznam denníka použitia materiálu prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.

### <a name="default-pricing"></a>Predvolená cena

Logika zadávania predvolených cien materiálu je založená na kombinácii produktu a jednotky. Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený a mena sú všetky použité na určenie príslušného cenníka. Polia, ktoré ovplyvňujú predvolené ceny, ako je **ID produktu** a **Zdrojová jednotka** sa používajú na určenie primeranej ceny v zázname v účtovom denníku. Toto však funguje iba pre katalógové produkty. Pre pridávané produkty sa cena zadaná pri vytvorení záznamu v denníku použitia materiálu použije pre náklady a predajnú cenu v záznamoch v účtovnom denníku. 

Do záznamu **Denník použitia materiálu** môžete pridať vlastné pole. Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**. Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií. Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).

## <a name="use-entry-journals-to-record-costs"></a>Používanie účtovných záznamov na zaznamenávanie nákladov

Účtovné záznamy môžete použiť na zaznamenávanie nákladov alebo výnosov materiálov, poplatkov, času, výdavkov alebo daňových transakcií. Denníky možno použiť na nasledujúce účely:

- Presuňte transakcie skutočných údajov z iného systému do aplikácie Microsoft Dynamics 365 Project Operations.
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
