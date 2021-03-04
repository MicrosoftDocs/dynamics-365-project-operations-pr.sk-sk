---
title: Granty v aplikácii Project
description: Táto téma vysvetľuje, ako vytvoriť alebo upraviť grant.
author: RadhikaRS
manager: AnnBe
ms.date: 04/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 89801696d6a2924d78c85f6e9b4281409222dbb0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084545"
---
# <a name="project-grants"></a>Granty v aplikácii Project

[!include [banner](../includes/banner.md)]

Grant je dar v podobe peňazí na konkrétny účel alebo projekt. Spravidla existujú obmedzenia týkajúce sa spôsobu použitia grantu. V časti Riadenie projektu a účtovníctvo môžete zadávať a sledovať granty a definovať ich vzťahy k projektom a projektovým zmluvám. Napríklad môžete vykonať nasledovné úlohy:

- Priraďte granty k projektom a zdrojom financovania prostredníctvom odkazov na stránky **Projekt** a **Podrobnosti projektovej zmluvy**.
- Zadajte a sledujte zmeny grantu pri jeho prechode z jedného stavu do druhého.
- Zadajte a sledujte náklady, požadované sumy a pridelené sumy.
- Vytvorte hlavné granty a priraďte k nim vedľajšie granty.

Grant môžete vytvoriť zadaním všetkých podrobností do nového záznamu alebo môžete podrobnosti skopírovať z existujúceho grantu a potom ich aktualizovať.

## <a name="create-a-new-grant"></a>Vytvorenie nového grantu

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Granty** \> **Granty**.
2. Stlačte **Nový** \> **Grant**.
3. Na stránke podrobností o grante na karte **Všeobecné** v poli **ID grantu** zadajte alfanumerický identifikátor grantu.
4. Do poľa **Názov grantu** zadajte jedinečný názov grantu.
5. V poli **Popis** pridajte ďalšie podrobnosti o novom grante.

    Väčšina ostatných polí na stránke je voliteľných a môžete zadať toľko informácií, koľko chcete.

    Nasledujúci zoznam popisuje informácie, ktoré sú uvedené na každej karte FastTab na stránke podrobností o grante:

    - **Všeobecné** – Zadajte názov grantu, stav, popis, účel a sumu.
    - **Kontaktné informácie** – Zadajte podrobnosti o zamestnancoch, oddelení, ktoré spravuje grant, a zdroj grantu pre zákazníka alebo organizáciu. Môžete tiež určiť, či je vaša organizácia prechodným subjektom, ktorý dostane grant, a potom ho odovzdá ďalšiemu príjemcovi. Vyberte možnosť **Pridať** na pridanie kontaktných informácií, ako sú telefónne čísla a e-mailové adresy organizácie, ktorá poskytuje grant.
    - **Dátumy a termíny** – Zadajte dátumy, ktoré sa týkajú grantu a žiadosti o grant. Príklady zahŕňajú dátum termínu žiadosti, dátum predloženia a dátum schválenia alebo zamietnutia grantu.
    - **Pridružené projekty a projektové zmluvy** – Na tejto karte FastTab môžete zadávať informácie, iba ak je pole **Stav grantu** na karte **Všeobecné** nastavené na **Aktívny** alebo **Udelený**. Vyberte jednu z nasledujúcich možností na dokončenie súvisiacej úlohy:

        - **Pridajte zdroj financovania** – Pridajte nový zdroj financovania grantu. Teraz môžete zadať všetky podrobnosti alebo môžete použiť predvolené informácie a potom ich neskôr aktualizovať.
        - **Pridať projektovú zmluvu** – Pridajte alebo aktualizujte informácie o zmluve o projekte.
        - **Pridať projekt** – Pridajte alebo aktualizujte podrobnosti projektu.

    - **Nastaviť** – Ak sú tieto informácie potrebné, zadajte podrobnosti o zodpovedajúcich fondoch. Mnoho organizácií, ktoré udeľujú granty, vyžaduje, aby príjemcovia utratili konkrétnu sumu svojich vlastných peňazí alebo zdrojov, aby zodpovedali sume pridelenej v grante. V poli **Lokálny projekt alebo ID sledovania** do poľa môžete zadať identifikátor, ktorý sa líši od identifikátora projektu.

        > [!NOTE]
        > Ak bude časť grantu pridelená inej organizácii, nastavte možnosť **Vedľajší donor** na **Áno**. V prípade grantov, ktoré sa udeľujú v Spojených štátoch, môžete určiť, či sa grant bude udeľovať na základe štátneho alebo federálneho mandátu.

    - **Podrobnosti o čerpaní** – Pridajte alebo aktualizujte informácie o tom, ako často je možné grantové prostriedky vyberať, účtovať alebo minúť.

## <a name="create-a-new-grant-from-a-copy"></a>Vytvorte nový grant z kópie

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Granty** \> **Granty**.
2. Stlačte možnosť **Nový**\>**Kópia z grantu**.
3. Zadajte alfanumerický identifikátor a názov nového grantu a potom stlačte **OK**.
4. Na stránke s podrobnosťami o grante skontrolujte podrobnosti skopírovaného grantu a vykonajte požadované zmeny. Väčšina polí na stránke je voliteľných.

## <a name="view-or-modify-grant-details"></a>Zobraziť alebo upraviť podrobnosti grantu

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Granty** \> **Granty**.
2. Vyberte grant, ktorý chcete upraviť.
3. Na table Akcia na karte **Grant** v skupine **Údržba** stlačte možnosť **Upraviť**.
4. Skontrolujte podrobnosti o grante a vykonajte požadované zmeny.


[!INCLUDE[footer-include](../includes/footer-banner.md)]