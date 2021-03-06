---
title: Vytvorenie priradení zdrojov
description: Táto téma poskytuje informácie o vytváraní všeobecných a pomenovaných priradení zdrojov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 20eb3880b17fb1f765ad79bd720520b0c8004c0a
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906325"
---
# <a name="create-resource-assignments"></a>Vytvorenie priradení zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Priradenie zdroja je priame priradenie člena projektového tímu k úlohe listového uzla. Táto téma poskytuje informácie o rôznych spôsoboch priradenia zdrojov.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vytvorte všeobecného člena tímu prostredníctvom priradenia úlohy


Keď vytvoríte všeobecného člena tímu prostredníctvom priradenia úlohy, vytvoríte zástupný symbol alebo všeobecný zdroj. Tento všeobecný zdroj popisuje charakteristiky pomenovaného zdroja, ktorý chcete, aby pracoval na úlohách. Následne vygenerujte požiadavku, alebo odošlite žiadosť pomocou požiadavky, ktorá sa použije na vyhľadávanie a rezerváciu pomenovaného zdroja.

1. Na mriežke plánu stlačte ikonu zdroja v bunke **Zdroj**.
2. Zadajte názov, ktorý bude slúžiť ako zástupný znak názvu zdroja. Napríklad, programový manažér
3. Vybert **vytvoriť** a v poli **rýchle vytvorenie porjektového člena tímu**, nastavte rolu pre všeobecný zdroj.
4. Priraďte potrebné úlohu k tomuto zástupnému zdroju výberom zdroja v časti **Výber zdroja** pre úlohy. Zdroje uvedené pod položkou **Členovia tímu**.
5. Keď skončíte s priraďovaním všeobecného zdroja, na karte **Tím** vyberte všeobecný zdroj a stlačte možnosť **Generovať požiadavku** na vytvorenie požiadavky zdroja pre všeobecný zdroj.
6. Stlačte možnosť **Rezervovať** pre všeobecný zdroj a potom použite tabuľu plánovania na vyhľadanie a rezerváciu skutočného zdroja. Požiadavku môžete tiež odoslať na vyplnenie manažérovi zdroja.
7. Keď je všeobecný zdroj úplne splnený (splnenie čiastočnej požiadavky na zdroj nebude mať za následok priradenie zdroja) s pomenovaným zdrojom, všeobecný zdroj sa z tímu odstráni. Priradenia úloh pre všeobecný zdroj sú priradené k pomenovanému zdroji, ktorý splnil požiadavku na zdroj všeobecného zdroja.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Priradenie pomenovaného zdroja zo zoznamu všetkých rezervovateľných zdrojov

Pole vyhľadávania možno v časti **Výber zdroja** použiť na vyhľadanie všetkých aktívnych rezervovateľných zdrojov a ich priradenie k úlohe listového uzla. Prostriedky pridelené týmto spôsobom sa pridajú do tímu bez akýchkoľvek rezervácií. To je podobné ako pridanie člena tímu a výber možnosti **Nič** ako spôsob prideľovania. Zdroje sa zobrazia na kartách **Tím**, **Priradenie zdroja** a **Odsúhlasenie** ako zdroje s tým, že im bude chýbať priradenie a rezervácia. Ak chcete využiť ich dostupnosť, zarezervujte ich.

1. Z mriežky úloh, tabule alebo časovej osi prejdite na bunku **Priradené používateľovi**.
2. Do vyhľadávacieho poľa začnite písať meno. Výsledky vyhľadávania pre názov sú zobrazené vo **výbere zdroja** v časti **iné zdroje**.
3. Vyberte zdroj, ktorý chcete priradiť k úlohe, alebo vyberte názov zdroja v časti **Ďalšie tímové zdroje**.
