---
title: Priraďte zdroj k úlohe
description: Táto téma poskytuje informácie o tom, ako priradiť zdroje k úlohám.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 3f96344b917f088f1d5782c5cee1d84f1aff47bc1bad7c8f6b33307d1df340fa
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987680"
---
# <a name="assign-a-resource-to-a-task"></a>Priradenie zdroja k úlohe

[!include [banner](../includes/psa-now-project-operations.md)]

Existujú tri spôsoby, ako priradiť zdroj k úlohe v Microsoft Dynamics 365 Project Service Automation.

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a>Rezervujte si zdroj ako člen tímu a potom ho priradiť k úlohe.

Môžete zdroj priradiť k tímovému projektu a následne ho priradiť k úlohám v pláne projektu.

1. V karte **člen tímu** pridajte nového člena tímu stlačením možnosti **nový**. 

2. Otvorí sa panel **rýchleho vytvorenia člena tímu**, kde si môžete zvoliť názov rezervovateľného zdroja a nastaviť mu rolu. 

    Vyberte jednu z nasledujúcich metód prideľovania pre rezerváciu zdroja:

    - **Plná kapacita** Táto metóda zarezervuje úplnú kapacitu zdroje pre stanovené dátumy od a do.
    - **Kapacita v percentách** zarezervuje zdroj pre percento kapacity zdroja pre stanovené dátumy od a do.
    - **Podľa rovnomerne rozmiestnených hodín** zarezervuje zdroj pre stanovený počet hodín, ktoré rovnomerne rozdelí na dni v rámci stanovených dátumov od a do.
    - **Podľa hodín počiatočného vyťaženia** zarezervuje prostriedok pre stanovený počet hodín, v rámci počiatočného vyťaženia denných hodín v rámci stanovených dátumov od a do.
    - Možnosť **Žiadne** zdroj pridá k tímu, no nevytvorí žiadne rezervácie, ktoré by využili kapacity zdroja.

3. Na mriežke **plánov** pre úlohu, stlačte ikonu **Zdroj** v bunke zdroja a potom pod **členovia tímu** zvoľte člena tímu, ktorého ste práve pridali. 

> [!NOTE]
> Na karte **člen tímu** aj na karte **odsúhlasenie** sa zdroj zobrazí spolu so zarezervovanými a pridelenými hodinami. Hodiny by mali byť rovnaké, no nie je to požadované, pretože rezervácie a pridelenia nie sú úzko spojené. Na karte **odsúhlasenia** nájdete podrobnosti v prípade, že sa budú líšiť. Ide napríklad o prípady, keď priradíte zdroju viac hodín, než ste zarezervovali. Ak je to treba, môžete opraviť informácie rozšírením rezervácie zdroja alebo zmenou priradenia.

## <a name="create-a-generic-team-member-through-task-assignment"></a>Vytvorte všeobecného člena tímu prostredníctvom priradenia úlohy

Keď vytvoríte všeobecného člena tímu prostredníctvom priradenia úlohy, vytvoríte zástupný alebo všeobecný zdroj, ktorý popisuje vlastnosti pomenovaného zdroja, ktorý chcete aby nakoniec pracoval na úlohách. Následne vygenerujte požiadavku (alebo odošlite žiadosť pomocou požiadavky), ktorá sa použije na vyhľadávanie a rezerváciu pomenovaného zdroja.

1. Na mriežke **plánu** stlačte ikonu **zdroja** v bunke zdroja.

2. Zadajte názov, ktorý bude slúžiť ako zástupný znak názvu zdroja. Napríklad, programový manažér

3. Vybert **vytvoriť** a v poli **rýchle vytvorenie porjektového člena tímu**, nastavte rolu pre všeobecný zdroj.

4. Môžete pokračovať na priradenie úloh k tomuto zástupnému zdroju výberom zdroja v časti **výber zdroja** pre úlohy. Sú uvedené pod **členmi tímu**.

5. Keď skončíte s priraďovaním všeobecného zdroja, zvoľte si na karte **Tím** všeobecný zdroj a stlačte možnosť **Generovať požiadavku** na vytvorenie požiadavky zdroja pre všeobecný zdroj.

6. Pri všeobecnom zdroji stlačte možnosť **Rezervovať**. Následne môžete použiť tabuľku plánu na vyhľadanie a rezerváciu skutočného zdroja. Požiadavku môžete tiež odoslať na vyplnenie manažérovi zdroja.

7. Pri plnení všeobecného zdroja pomenovaným zdrojom sa všeobecný zdroj odstráni z tímu a priradenia úlohy pre všeobecný zdroj sa priradia k pomenovanému zdroju, ktorý vyplnil požiadavku na zdroj všeobecného zdroja.

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a>Priradenie pomenovaného zdroja zo zoznamu všetkých rezervovateľných zdrojov

Pole vyhľadávania možno vo **výbere zdroja** použiť na vyhľadanie všetkých rezervovateľných zdrojov a ich priradenie k úlohe.

Prostriedky pridelené týmto spôsobom sa pridajú do tímu bez akýchkoľvek rezervácií. To je podobné ako pridanie člena tímu a výber nič ako spôsob prideľovania. Zdroje sa zobrazia na karte **tím** a na karte **odsúhlasenie** ako zdroje s tým, že im bude chýbať priradenie a rezervácia. Ak chcete využiť ich dostupnosť, zarezervujte ich.

1. Na mriežke **plánu** stlačte ikonu **zdroja** v bunke zdroja.

2. Začnite písať názov. Výsledky vyhľadávania pre názov sú zobrazené vo **výbere zdroja** v časti **iné zdroje**.

3. V zozname vyberte zdroj, ktorý chcete priradiť k úlohe.



[!INCLUDE[footer-include](../includes/footer-banner.md)]