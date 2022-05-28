---
title: Rezervovanie projektu
description: Táto téma poskytuje informácie o rezervácii zdrojov pre projekt.
author: ruhercul
ms.date: 01/24/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b47ae8cb38be6d29804aec8b069e6a8aec0ffb70
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8591408"
---
# <a name="book-to-a-project"></a>Rezervovanie projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Sú chvíle, kedy bude projektový manažér alebo manažér zdrojov musieť prideliť zdroj k projektu, bez toho, aby boli definované konkrétne požiadavky od všeobecného člena tímu. Môže sa dosiahnuť jedným z troch spôsobov.

- Rezervácia na mriežke člena tímu
- Rezervácia z tabule plánovania
- Rezervácia pomocou formulára **Projekt**

## <a name="book-from-the-team-member-grid"></a>Rezervácia na mriežke člena tímu

Ak vaša organizácia pracuje v hybridnom režime prideľovania zdrojov, projektový manažér môže rezervovať zdroj priamo do projektu vykonaním nasledujúcich krokov.

1. V projekte prejdite do mriežky členov tímu a vyberte **Nový**.
2. Definujte názov pozície a úlohu zdroja.
3. Vyberte rezervovateľný zdroj z dostupného vyhľadávania.
4. Po výbere zdroja definujte nasledujúce informácie o poli, pomocou ktorých si môžete rezervovať zdroj:

    - Počiatočný dátum
    - Dátum dokončenia
    - Metóda pridelenia
    - Hodiny, ak je to relevantné
    - Schvaľovateľ projektu

6. Vyberte položku **Uložiť a zavrieť**

## <a name="book-from-the-schedule-board"></a>Rezervácia z tabule plánovania

Ak manažér zdrojov potrebuje rezervovať zdroj priamo v projekte, môže použiť tabuľu plánovania a požiadavky na projekt. Požiadavka na projekt je požiadavka na zdroje, ktorú je možné kedykoľvek rezervovať. Ak chcete rezervovať priamo projekt z tabule plánovania, postupujte podľa nasledujúcich krokov.

1. Prejdite na tabuľu plánovania a na ľavej strane odfiltrujte zdroje, ktoré zvažujete pre požiadavku.
2. Na spodnom paneli vyberte kartu **Projekt** na zobrazenie zoznamu požiadaviek pre projekt.
3. Presuňte požiadavku na zdroj a definujte nasledujúce informácie:

    - Počiatočný dátum
    - Dátum dokončenia
    - Stav rezervácie
    - Spôsob rezervácie
    - Duration
   
   > [!NOTE]
   > V súčasnosti Dynamics 365 Project Operations nepodporuje tabuľu plánovania.   

## <a name="book-from-the-project-form"></a>Rezervácia pomocou formulára Projekt

Ako projektový manažér možno budete musieť rezervovať zdroj v projekte, ak poznáte iba kritériá a nie názov zdroja. Ak chcete pomocou asistenta plánovania vyhľadať zdroj na základe akýchkoľvek dostupných atribútov zdroja, vykonajte nasledujúce kroky. 

1. Prejdite na projekt a vyberte **Rezervovať** na otvorenie Asistenta plánovania.
2. Pomocou filtrov na ľavej strane asistenta plánovania zúžte kritériá a vyberte **Hľadať.**
3. Na základe zdrojov vrátených vo výsledkoch si môžete rezervovať zdroj.

> [!NOTE]
> Táto metóda nevytvára pre zdroj žiadne rezervácie. Namiesto toho pridá zdroj do tímu. Po pridaní člena tímu do projektu môže projektový manažér pomocou údržby rezervácií alebo rozšírenia rezervácií pridať požadované rezervácie do zdroja.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
