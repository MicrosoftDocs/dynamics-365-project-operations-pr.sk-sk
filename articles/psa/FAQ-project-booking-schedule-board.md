---
title: Vytvorte rezerváciu projektu z tabule plánovania
description: Táto téma poskytuje informácie o tom, ako vytvoriť projektovú rezerváciu z tabule plánovania.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 513f7fe75cfb7b1658b4be71ed0a17da7b64a1023992e1dada9adca8f0dbf21e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987635"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Vytvorte rezerváciu projektu z tabule plánovania

[!include [banner](../includes/psa-now-project-operations.md)]

Môžete si rezervovať zdroj na projekte buď priamo na karte **tím**, alebo vytvorením požiadavky zdroja pri všeobecnom priradení člena tímu a následnom vyplnení vygenerovaných požiadaviek použitím člena tímu projektu.

Môžete si rezervovať prostriedok do projektu priamo z plánovacej tabule. Existujú tri spôsoby, ako sa s tým vysporiadať:

- **Rezervujte požiadavku z vygenerovaného zdroja:** po vytvorení všeobecného prostriedku môžete vygenerovať požiadavku na zdroj a priradiť úlohy v rámci projektu.

- **Rezervácia z primárnej požiadavky:** primárne požiadavky sa zobrazia na tabuli plánovania na karte **projekt**. 

- **Rezervácia z požiadavky nového zdroja:** môžete vytvoriť požiadavku na zdroj od nuly a priradiť ho k projektu. Na tabule plánovania sa tieto požiadavky zdrojov zobrazia v karte **Otvorené požiadavky**.

## <a name="book-from-a-generated-resource-requirement"></a>Zarezervujte prostredníctvom vygenerovanej požiadavky zdroja.

Môžete vytvoriť všeobecný zdroj a priradiť mu úlohu alebo viacero úloh v rámci projektu. Potom vygenerujete požiadavku zdroja zo všeobecného člena tímu. 

1.  Na tabuli plánovania sa tento zdroj objaví na karte **otvorené požiadavky**. Možno bude potrebné použiť filtre stĺpcov na mriežke v prípade, že máte priveľa otvorených požiadaviek. 

    ![Otvorenie karty Požiadavky na tabuli plánovania.](media/FAQ-Project-Booking-Schedule-Board-1.png "Snímka obrazovky rezervácií a tabuľka priradenia")

2. Vyberte si požiadavku. Karta **Hľadať dostupnosť** sa zobrazí v hornej časti vybraného riadka.
 
3. Výberom karty dôjde k spusteniu režimu asistenta plánovania tabule plánovania a k odfiltrovaniu dostupných zdrojov, ktoré spĺňajú požiadavky zdroja. Po tomto si môžete rezervovať zdroj.

4. Vybratý riadok môžete tiež presunúť zo spodnej časti tabule plánovania k bunke zdroja v mriežke. Po rozbalení sa vpravo otvorí panel **Vytvoriť rezerváciu zdroja**.

    Stlačením možnosti **Rezervovať** sa zdroj zarezervuje do tímu projektu.

![Vytvorte panel rezervácie zdroja.](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervácia zo základnej požiadavky

Vytvorením projektu v Project Service sa automaticky vytvorí požiadavky na zdroj s názvom Hlavná požiadavka. Ide o prázdnu požiadavku, ktorá sa používa na rýchlu rezerváciu zdroja pomocou tabule plánovania bez toho, aby sa vygenerovala požiadavka alebo sa vytvárala od nuly. Pretože je požiadavka prázdna, budete musieť zadať dátumy spolu so spôsobom pridelenia a hodín, ak sú uplatniteľné. 

1. Na rezerváciu zdroja prostredníctvom hlavnej požiadavky stlačte na tabuli plánovania kartu **Projekt**. Možno bude potrebné použiť filter stĺpcov na stĺpci **Projekt** v prípade, že máte priveľa projektov.

   ![Filtrovanie stĺpcov na tabuli plánovania.](media/FAQ-Project-Booking-Schedule-Board-2.png "Snímka obrazovky rezervácií a tabuľka priradenia")

2. Vyberte požiadavku, ktorá má názov projektu ako názov a trvanie má nul (0).

3. Zvoľte kartu **Hľadať dostupnosť**, ktorá sa objaví na riadku. Týmto sa tabuľa plánovania spustí do režimu asistenta plánovania a zobrazia sa dostupné zdroje, ktoré možno zarezervovať do projektu.

4. Pretože **hlavná požiadavka** predstavuje prázdnu požiadavku s trvaním nula (0), budete musieť nastaviť trvanie na paneli **Vytvoriť rezerváciu zdroja** pri výbere a rezervácii zdroja.

5. Môžete si tiež vybrať **primárnu požiadavku projektu** v spodnej časti tabule plánovania a presunúť ju na zdroj, čím sa zarezervuje.
 
    Pretože **hlavná požiadavka** predstavuje prázdnu požiadavku s trvaním nula (0), budete musieť nastaviť trvanie na paneli **Vytvoriť rezerváciu zdroja** pri výbere a rezervácii zdroja.
 
    Keď si zarezervujete zdroj cez **hlavnú požiadavku** na paneli plánovania, pridáte ju k tímu projektu bez akéhokoľvek priradenia.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervácia z novej požiadavky zdroja
Ak chcete rezervovať z novej požiadavky zdroja, postupujte podľa nasledujúcich krokov. 

1. Prejdite na **Požiadavky na zdroje** a zvoľte možnosť **Nová**, čím vytvoríte novú požiadavku na zdroje.

2. Na karte **projekt**, vyberte projekt na priradenie požiadavky k projektu.
 
    Táto novovytvorená požiadavka sa zobrazí ako **otvorená požiadavka** na tabuli plánovania, kde ju možno vyplniť.

3. Rezervujte zdroj na jeho pridanie k projektovému tímu.

4. Teraz keď je zdroj zarezervovaný, musíte manuálne priradiť úlohy.



[!INCLUDE[footer-include](../includes/footer-banner.md)]