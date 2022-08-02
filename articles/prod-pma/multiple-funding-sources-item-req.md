---
title: Požiadavky na položky pre projektové zmluvy s viacerými zdrojmi financovania
description: Tento článok poskytuje informácie o tom, ako nakonfigurovať a používať požiadavky na položky s viacerými zdrojmi financovania.
author: sigitac
ms.date: 05/04/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 079856e7cf2ffa9b80ab31ebad1c1b5dbe36a4ad
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028507"
---
# <a name="item-requirements-for-project-contracts-with-multiple-funding-sources"></a>Požiadavky na položky pre projektové zmluvy s viacerými zdrojmi financovania

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/výrobe_

Niektoré zmluvné dohody pre výstupy založené na projekte si môžu vyžadovať viacero zdrojov financovania. Tento článok vysvetľuje, ako vybrať a nakonfigurovať požadované zdroje financovania, keď je pre projekt alebo projektovú zmluvu potrebných viacero zdrojov.

## <a name="terminology"></a>Terminológia

- **Zdroj financovania** – Subjekt, ktorý financuje prácu na projektovej zmluve. Touto entitou môže byť interná organizácia alebo externý fakturačný účet (zákazník alebo grant).
- **Zákazník projektu** – Subjekt, ktorému sa projektová práca doručuje.
- **Fakturačný účet** – Externý subjekt, ktorý platí za projektové práce.

## <a name="example"></a>Príklad

Contoso vyhral zmluvu o obnove vybavenia s dvoma svojimi zákazníkmi: Adatum US a Adatum Corporate. Zmluva zahŕňa hardvérové a inštalačné služby, ktoré budú dodané spoločnosti Adatum US (zákazník projektu). Hardvér bude financovať Adatum Corporate (fakturačný účet 1) a inštalačné práce bude financovať Adatum US (fakturačný účet 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Nastavte predvolené pravidlá fakturačného účtu pre požiadavky na položky

### <a name="prerequisites"></a>Požiadavky

- Microsoft Dynamics 365 Financie **verzia 10.0.27 alebo novšia** je potrebné použiť požiadavky na položky, ktoré majú viacero fakturačných účtov.
- Váš správca systému musí povoliť **Povoľte požiadavky na položky s viacerými zdrojmi financovania pre scenáre na sklade/produkcii projektových operácií** funkcia v **Správa funkcií** pracovnom priestore.

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Nastavte predvolené pravidlá fakturačného účtu

Ak chcete nastaviť predvolené pravidlá pre fakturačný účet, postupujte podľa týchto krokov.

1. Prejdite na **Projektové riadenie a účtovníctvo** \> **Nastaviť** \> **Parametre projektového riadenia a účtovníctva**.
1. Na **generál** kartu, v **Predajné objednávky a požiadavky na položky** sekciu, nastavte **Povoliť projekty s viacerými zdrojmi financovania** možnosť **Áno**.
1. V **Predvolený zákazník** zadajte, odkiaľ štandardne pochádza zákazník na dodávku projektu v požiadavke na položku:

    - **Zo zdroja financovania** – Predvolený zákazník na dodávku projektu pochádza zo zdroja financovania. Ak je s projektovou zmluvou spojených viacero zdrojov financovania, použije sa prvý zdroj financovania v zozname.
    - **Z projektu** – Predvolený zákazník dodávky projektu pochádza od zákazníka, ktorý je vybratý v **Evidenčný účet projektu** lúka.

1. Voliteľné: Nastavte alebo zmeňte predvolený fakturačný účet v záznamoch projektu:

    1. Ísť do **Projektový manažment a účtovníctvo** \> **projekty** \> **Všetky projekty** a otvorte podrobnosti záznamu projektu.
    2. Na **generál** kartu, nastavte alebo aktualizujte **Predvolený fakturačný účet** lúka. Účet, ktorý určíte, sa použije ako predvolený účet faktúry pre nové požiadavky na položky, ktoré sa vytvoria pre projekt. Ak necháte pole prázdne, štandardne sa použije fakturačný účet prvého zdroja financovania projektovej zmluvy. Používatelia však budú môcť pri ukladaní záznamu zmeniť účet.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Vyberte fakturačný účet, ktorý sa má použiť pri vytváraní požiadavky na položku

Ak chcete vybrať účet faktúry, ktorý sa má použiť pri vytváraní požiadavky na položku, postupujte podľa týchto krokov.

1. Ísť do **Projektový manažment a účtovníctvo** \> **projekty** \> **Všetky projekty** a vyberte záznam projektu.
1. Na **Plán** kartu, vyberte **Požiadavky na položky**.
1. Vytvorte nový záznam požiadavky na materiál.

    - V predvolenom nastavení je **Fakturačný účet** pole v zázname je nastavené na účet faktúry, ktorý je nastavený pre projekt. Môžete zmeniť hodnotu **Fakturačný účet** pole a potom záznam uložte. Po uložení záznamu ho už nemôžete aktualizovať **Fakturačný účet** hodnotu. Ak musíte aktualizovať **Fakturačný účet** hodnotu pre požiadavku na položku, odstráňte existujúcu požiadavku na položku a potom vytvorte novú, ktorá má požadovanú hodnotu.
    - V predvolenom nastavení je **Zákazník** pole pre požiadavku na položku je nastavené na základe **Predvolený zákazník** hodnota, ktorá je nastavená na **Projektový manažment a účtovné parametre** stránku.

    Keď je záznam požiadavky na materiál uložený, systém ho priradí k **Požiadavka na položku predajná objednávka** hlavičkový záznam. Ak žiadna hlavička otvorenej zákazky odberateľa nemá vybratý účet faktúry, systém ho vytvorí a priradí k nemu riadok požiadavky na materiál.

> [!NOTE]
> Požiadavky na položky sú vždy plne fakturované na fakturačný účet, ktorý je nastavený v zázname. Systém momentálne nepodporuje pravidlá prideľovania financií, ktoré majú požiadavky na položky, a nerozdelí zaúčtovanie na základe nastavenia pravidiel prideľovania financií.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Vytvorte požiadavku na materiál zo záznamu prognózy materiálu

Ak chcete vytvoriť požiadavku na položku zo záznamu prognózy položky, postupujte podľa týchto krokov.

1. Ísť do **Projektový manažment a účtovníctvo** \> **projekty** \> **Všetky projekty** a vyberte záznam projektu.
1. Na **Plán** kartu, vyberte **Prognózy položiek**.
1. Vytvorte nový záznam prognózy položky.
1. Voliteľné: Na **Projekt** kartu, v **Zdroj financovania** vyberte požadovaný fakturačný účet.
1. Vyberte **Vytvorte požiadavku na položku** a potvrďte prijatú správu.

    > [!NOTE]
    > Systém skopíruje **Zdroj financovania** hodnotu zo záznamu prognózy materiálu do novovytvoreného záznamu požiadavky na materiál.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Predvolený účet faktúry, keď systém automaticky vytvorí požiadavku na materiál z riadku nákupnej objednávky

Ak **Vytvorte požiadavku na položku** možnosť je nastavená na **Áno** na **Projektový manažment a účtovné parametre** systém automaticky vytvorí požiadavku na materiál, keď sa uloží nový riadok projektovej objednávky. V predvolenom nastavení je **Fakturačný účet** a **Požiadavka na položku** polia sú nastavené na hodnotu **Predvolený fakturačný účet** pole v zázname projektu. Systém momentálne nepodporuje aktualizáciu alebo zmenu fakturačného účtu pre záznamy tohto typu.
