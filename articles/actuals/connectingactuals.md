---
title: Kontaktné osoby pre transakcie – prepojenie skutočných hodnôt rôznych typov transakcií
description: Tento článok vysvetľuje, ako sa transakčné pripojenie používa na prepojenie skutočných údajov rôznych typov, čo pomáha sledovať ziskovosť, nevybavené fakturácie a výpočty účtovaných a nevyfakturovaných príjmov.
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

Záznamy o transakčnom spojení sa vytvárajú na prepojenie skutočných údajov rôznych typov, keď sa čas, náklady alebo spotreba materiálu počas svojho životného cyklu presúva z ponuky alebo fázy predpredaja do fázy zmluvy, schvaľovania a/alebo odvolaní, fakturácie a potenciálne kreditnej alebo opravnej fakturácie. .

Nasledujúci príklad znázorňuje typické spracovanie časových záznamov v životnom cykle projektu Project Operations.

> ![Spracovanie časových záznamov v Projektových operáciách.](media/basic-guide-17.png)

Spracovanie časových záznamov v životnom cykle projektu Project Operations prebieha podľa týchto krokov: 

1. Odoslanie časového záznamu spôsobí, že sa vytvoria dva riadky denníka: jeden pre náklady a jeden pre nevyfakturovaný predaj. 
2. Prípadné schválenie časového záznamu spôsobí, že sa vytvoria dva skutočné údaje: jeden pre náklady a jeden pre nevyfakturovaný predaj. Tieto 2 skutočnosti sú prepojené pomocou transakčných spojení.
3. Keď používateľ vytvorí fakturačný projekt, vytvorí sa fakturačný riadok transakcie zo skutočného nefakturovaného predaja.
4. Po potvrdení faktúry sa vytvoria dve nové skutočnosti: stornovanie nevyfakturovaného predaja a skutočné vyúčtované tržby. Storno nevyfakturovaných tržieb a pôvodný skutočný nevyfakturovaný predaj sú prepojené pomocou reverzných transakčných spojení. Fakturované tržby a pôvodné skutočné nevyfakturované tržby sú tiež prepojené, aby sa zobrazili prepojenia medzi tým, čo bolo kedysi nevybavené alebo nedokončená výroba (WIP), s tým, čo je teraz fakturovaným príjmom.   

Každá udalosť v pracovnom toku spracovania spúšťa vytváranie záznamov v **Transakčné spojenie** tabuľky. Pomáha to vytvoriť stopu vzťahov medzi záznamami, ktoré sú vytvorené cez časový záznam, riadok denníka, skutočné údaje a podrobnosti o riadku faktúry.

Nasledujúca tabuľka zobrazuje záznamy v **Transakčné spojenie** entity pre predchádzajúci pracovný tok.

|Udalosť                   |Transakcia 1                 |Rola transakcie 1 |Typ transakcie 1       |Transakcia 2          |Rola transakcie 2 |Typ transakcie 2 |
|------------------------|------------------------------|---------------|-----------------------------|-----------------------------|-------------------|-------------------|
|Podanie časového záznamu   |Záznam v účtovnom denníku GUID (Predaje)     |Nefakturovaný predaj |msdyn_journalline            |Záznam v účtovnom denníku GUID (náklady)     |Náklady            |msdyn_journalline  |
|Schválený čas           |Skutočné náklady (základné)  |Nefakturovaný predaj |msdyn_actual                 |Skutočné náklady (náklady) GUID       |Náklady            |msdyn_actual       |
|Vytváranie faktúr        |Podrobnosti o riadku faktúry GUID      |Fakturovaný predaj   |msdyn_invoicelinetransaction |Nové nefakturované skutočné údaje predaja GUID   |Nefakturovaný predaj  |msdyn_actual       |
|Potvrdenie faktúry    |Storno skutočných údajov GUID         |Storno      |msdyn_actual                 |Pôvodné nefakturované predaje GUID |Pôvodné        |msdyn_actual       |
|                        |Fakturovaný predaj GUID             |Fakturovaný predaj   |msdyn_actual                 |Nové nefakturované skutočné údaje predaja GUID   |Nefakturovaný predaj  |msdyn_actual       |
|Koncept opravy faktúry |Riadok faktúry Transaction GUID|Nahradenie      |msdyn_invoicelinetransaction |Fakturovaný predaj GUID            |Pôvodné        |msdyn_actual       |
|Potvrdená oprava faktúry|Storno fakturovaného predaja GUID  |Storno      |msdyn_actual                 |Fakturovaný predaj GUID            |Pôvodné        |msdyn_actual       |
|                        |Nový GUID nevyúčtovaných predajov |Nahradenie            |msdyn_actual                 |Fakturovaný predaj GUID            |Pôvodné        |msdyn_actual       |


Nasledujúca ilustrácia zobrazuje prepojenia, ktoré sa vytvárajú medzi rôznymi typmi skutočných hodnôt pri rôznych udalostiach, na príklade časových záznamov v Project Operations.

> ![Ako sú fakty rôznych typov navzájom prepojené v projektových operáciách.](media/TransactionConnections.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
