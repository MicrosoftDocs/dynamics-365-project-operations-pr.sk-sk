---
title: Metódy nákladov na dokončenie
description: Táto téma poskytuje informácie o metódach použitých na výpočet nákladov na dokončenie projektu.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 837cb3abe33e6e74087b8aae8b072bf4a21dc933
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279067"
---
# <a name="cost-to-complete-methods"></a>Metódy nákladov na dokončenie

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie o metódach použitých na výpočet nákladov na dokončenie projektu. Existuje niekoľko metód, ktoré môžete použiť na výpočet nákladov na dokončenie projektu. 

Keď vytvárate odhad projektu, na stránke **Vytvoriť odhad** v poli **Metóda nákladov na dokončenie** môžete vybrať jednu z nasledujúcich metód nákladov na dokončenie.

| Metóda nákladov na dokončenie    | Popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Celkové náklady – skutočné            | Zadajte ručne odhad nákladov do polí **Celkové náklady** alebo **Celkové množstvo** pomocou tlačidla **Odhad nákladov** na stránke **Odhad**. Systém odčíta skutočné náklady od súčtov, ktoré ste zadali. Súčet predstavuje náklady na dokončenie projektu. Táto metóda nepoužíva odhady výdavkov a priradenia zdrojov zadané v rámci aplikácie Project Operations zabudovanej v rámci Microsoft Dataverse. Celkové náklady alebo celkové množstvo je možné podľa potreby aktualizovať ručne.  |
| Celková predpoveď – skutočné        | Priradenie zdrojov a odhady výdavkov sa používajú na určenie celkovej výšky prognózy projektu. Skutočné náklady sa porovnajú s touto predpoveďou, aby sa vypočítali náklady na dokončenie.                                                                                                                                                                                                                                                                          |
| Ako predchádzajúci odhad         | Používajú sa tu rovnaké metódy odhadu, aké boli použité v predchádzajúcom období. Táto metóda vyžaduje predpovedný model, ak predchádzajúce obdobie vyžadovalo predpovedný model.                                                                                                                                                                                                                                                                                                                           |
| Nastaviť náklady na dokončenie na nulu | Táto metóda, ktorá sa zvyčajne používa pred odstránením projektu odhadu, porovnáva celkové odhady so zaúčtovanými skutočnými transakciami a vymaže stĺpec **Náklady na dokončenie**. Po dokončení je výsledok vždy 100 percent. Pre každý nákladový riadok, ktorý vytvoríte, začiarkavacie políčko **Prognózy** nie je zaškrtnuté a celkový odhad je skopírovaný z predchádzajúceho odhadu nákladov. Skutočná spotreba za odhadované obdobie sa odpočíta od nákladov na dokončenie projektu.              |
| Zo šablóny nákladov           | Metóda nákladov na dokončenie, ktorá je nastavená v šablóne nákladov, ktorá je spojená s vybraným projektom odhadu.                                                                                                                                                                                                                                                                                                                                                                          |


[!INCLUDE[footer-include](../includes/footer-banner.md)]