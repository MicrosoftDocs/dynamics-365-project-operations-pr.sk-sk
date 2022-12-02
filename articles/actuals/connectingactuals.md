---
title: Kontaktné osoby pre transakcie – prepojenie skutočných hodnôt rôznych typov transakcií
description: Tento článok vysvetľuje, ako sa kontaktná osoba pre transakciu používa na prepojenie skutočných hodnôt rôznych typov, čo pomáha sledovať ziskovosť, backlog pre fakturáciu a výpočty účtovaných a nevyfakturovaných príjmov.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 19a78336099f54c5d6b36a963a90b9fd77e3d0af
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8926105"
---
# <a name="transaction-connections---link-actuals-of-different-transaction-types"></a>Kontaktné osoby pre transakcie – prepojenie skutočných hodnôt rôznych typov transakcií

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Záznamy o transakčnom pripojení sa vytvárajú na prepojenie skutočných hodnôt rôznych typov, ako sa čas, výdavky alebo spotreba materiálu, keď sa počas svojho životného cyklu presúvajú z cenovej ponuky alebo etapy pred predajom do etapy zmluvy, schvaľovania a/alebo odvolania, fakturácie a potenciálne kreditnej alebo opravnej fakturácie.

Nasledujúci príklad znázorňuje typické spracovanie časových záznamov v životnom cykle projektu Project Operations.

> ![Spracovanie časových záznamov v Project Operations.](media/basic-guide-17.png)

Spracovanie časových zadaní v životnom cykle projektu Project Operations prebieha v týchto krokoch: 

1. Odoslanie zadania času spôsobí vytvorenie dvoch záznamov v účtovnom denníku: jeden pre náklad a jeden pre nevyfakturované predaje. 
2. Prípadné schválenie zadania času spôsobuje vytvorenie dvoch skutočných hodnôt: jedna pre náklad a jedna pre nevyfakturované predaje. Tieto 2 skutočné hodnoty sú prepojené pomocou transakčných pripojení.
3. Keď používateľ vytvorí fakturačný projekt, vytvorí sa fakturačný riadok transakcie zo skutočného nefakturovaného predaja.
4. Po potvrdení faktúry toto vytvorí dve nové skutočné hodnoty: nefakturovaný obrat predaja a skutočný fakturovaný predaj. Storno nevyfakturovaných tržieb a pôvodnú skutočnú sumu nefakturovaného predaja sú prepojené pomocou reverzných transakčných pripojení. Fakturované tržby a pôvodné skutočné nevyfakturované tržby sú tiež prepojené, aby sa zobrazili prepojenia medzi tým, čo bolo kedysi nevybavené alebo nedokončené tržby (WIP), s tým, čo je teraz fakturovaným príjmom.   

Každá udalosť v pracovnom postupe spracovania spúšťa vytváranie záznamov v tabuľke **Transakčné pripojenie**. Pomáha to budovať sledovanie vzťahov medzi záznamami, ktoré sa vytvárajú v zadaniach času, zázname v účtovnom denníku, skutočnej hodnote a detailoch riadkov faktúry.

Nasledujúca tabuľka zobrazuje záznamy v entite **Transakčné pripojenie** pre predchádzajúci pracovný postup.

|Udalosť                   |Transakcia 1                 |Rola transakcie 1 |Typ transakcie 1       |Transakcia 2          |Rola transakcie 2 |Typ transakcie 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Podanie časového záznamu   |Záznam v účtovnom denníku GUID (Predaje)     |Nefakturovaný predaj |msdyn_journalline            |Záznam v účtovnom denníku GUID (náklady)     |Náklady            |msdyn_journalline  |
|Schválený čas           |Skutočné náklady (základné)  |Nefakturovaný predaj |msdyn_actual                 |Skutočné náklady (náklady) GUID       |Náklady            |msdyn_actual       |
|Vytváranie faktúr        |Podrobnosti o riadku faktúry GUID      |Fakturovaný predaj   |msdyn_invoicelinetransaction |Nové nefakturované skutočné údaje predaja GUID   |Nefakturovaný predaj  |msdyn_actual       |
|Potvrdenie faktúry    |Storno skutočných údajov GUID         |Storno      |msdyn_actual                 |Pôvodné nefakturované predaje GUID |Pôvodné        |msdyn_actual       |
|                        |Fakturovaný predaj GUID             |Fakturovaný predaj   |msdyn_actual                 |Nové nefakturované skutočné údaje predaja GUID   |Nefakturovaný predaj  |msdyn_actual       |
|Koncept opravy faktúry |Riadok faktúry Transaction GUID|Nahradenie      |msdyn_invoicelinetransaction |Fakturovaný predaj GUID            |Pôvodné        |msdyn_actual       |
|Potvrdená oprava faktúry|Storno fakturovaného predaja GUID  |Storno      |msdyn_actual                 |Fakturovaný predaj GUID            |Pôvodné        |msdyn_actual       |
|                        |Nové GUID nefakturovaného predaja |Nahradenie            |msdyn_actual                 |Fakturovaný predaj GUID            |Pôvodné        |msdyn_actual       |


Nasledujúca ilustrácia zobrazuje prepojenia, ktoré sa vytvárajú medzi rôznymi typmi skutočných hodnôt pri rôznych udalostiach, na príklade zadaní času v Project Operations.

> ![Ako sú skutočné hodnoty rôznych typov navzájom prepojené v Project Operations.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
