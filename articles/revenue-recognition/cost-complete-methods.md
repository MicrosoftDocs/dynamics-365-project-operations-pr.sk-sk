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
ms.openlocfilehash: 790b5c98182acdc0a37e3741a40baf7152f0bf66
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531550"
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