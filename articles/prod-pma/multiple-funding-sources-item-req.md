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

- **Zdroj financovania** – Subjekt, ktorý financuje prácu podľa projektovej zmluvy. Týmto subjektom môže byť interná organizácia alebo externý fakturačný účet (zákazník alebo grant).
- **Zákazník projektu** – Subjekt, ktorému sa projektová práca doručuje.
- **Fakturačný účet** – Externý subjekt, ktorý platí za projektové práce.

## <a name="example"></a>Príklad

Spoločnosť Contoso získala zmluvu na obnovu vybavenia s dvoma svojimi zákazníkmi: Adatum US a Adatum Corporate. Zmluva zahŕňa hardvérové a inštalačné služby, ktoré budú dodané spoločnosti Adatum US (zákazník projektu). Hardvér bude financovať Adatum Corporate (fakturačný účet 1) a inštalačné práce bude financovať Adatum US (fakturačný účet 2).

## <a name="set-up-invoice-account-defaulting-rules-for-item-requirements"></a>Nastavte predvolené pravidlá fakturačného účtu pre požiadavky na položky

### <a name="prerequisites"></a>Požiadavky

- Microsoft Dynamics 365 Finance **verzia 10.0.27 alebo novšia** je potrebná, aby bolo možné použiť požiadavky na položky, ktoré majú viacero fakturačných účtov.
- Váš správca systému musí povoliť funkciu **Povoliť požiadavky na položky s viacerými zdrojmi financovania pre scenáre založené na zdrojoch/výrobe v Project Operations** v pracovnom priestore **Správa funkcií** .

### <a name="set-up-the-invoice-account-defaulting-rules"></a>Nastavte predvolené pravidlá fakturačného účtu

Ak chcete nastaviť predvolené pravidlá pre fakturačný účet, postupujte podľa týchto krokov.

1. Prejdite na **Projektové riadenie a účtovníctvo** \> **Nastaviť** \> **Parametre projektového riadenia a účtovníctva**.
1. Na karte **Všeobecné** v časti **Predajné objednávky a požiadavky na položky** nastavte možnosť **Povoliť projekty s viacerými zdrojmi financovania** na **Áno**.
1. V poli **Predvolený zákazník** zadajte, odkiaľ štandardne pochádza zákazník na dodávku projektu v požiadavke na položku:

    - **Zo zdroja financovania** – Predvolený zákazník na dodávku projektu pochádza zo zdroja financovania. Ak je s projektovou zmluvou spojených viacero zdrojov financovania, použije sa prvý zdroj financovania v zozname.
    - **Z projektu** – Predvolený zákazník dodávky projektu pochádza od zákazníka, ktorý je vybratý v poli **Účet záznamu projektu**.

1. Voliteľné: Nastavte alebo zmeňte predvolený fakturačný účet v záznamoch projektu:

    1. Prejdite na položku **Projektové riadenie a účtovníctvo** \> **Projekty** \> **Všetky projekty** a otvorte podrobnosti záznamu projektu.
    2. Na karte **Všeobecné** nastavte alebo aktualizujte pole **Predvolený fakturačný účet**. Účet, ktorý určíte, sa použije ako predvolený fakturačný účet pre nové požiadavky na položky, ktoré sa vytvoria pre projekt. Ak necháte pole prázdne, štandardne sa použije fakturačný účet prvého zdroja financovania projektovej zmluvy. Používatelia však budú môcť pri ukladaní záznamu zmeniť účet.

### <a name="select-the-invoice-account-to-use-when-you-create-an-item-requirement"></a>Vyberte fakturačný účet, ktorý sa má použiť pri vytváraní požiadavky na položku

Ak chcete vybrať fakturačný účet, ktorý sa má použiť pri vytváraní požiadavky na položku, postupujte podľa týchto krokov.

1. Prejdite na **Projektový manažment a účtovníctvo** \> **Projekty** \> **Všetky projekty** a vyberte záznam projektu.
1. Na karte **Plán** vyberte **Požiadavky na položky**.
1. Vytvorte nový záznam požiadavky na položky.

    - V predvolenom nastavení je pole **Fakturačný účet** v zázname nastavené na fakturačný účet, ktorý je nastavený pre projekt. Môžete zmeniť hodnotu poľa **Fakturačný účet** a potom záznam uložiť. Po uložení záznamu už nemôžete aktualizovať hodnotu **Fakturačný účet**. Ak musíte aktualizovať hodnotu **Fakturačný účet** pre požiadavku na položku, odstráňte existujúcu požiadavku na položku a potom vytvorte novú, ktorá má požadovanú hodnotu.
    - V predvolenom nastavení je pole **Zákazník** pre požiadavku na položku nastavené na základe hodnoty **Predvolený zákazník**, ktorá je nastavená na stránke **Parametre projektového riadenia a účtovníctva**.

    Keď sa záznam požiadavky na položku uloží, systém ho priradí k záznamu hlavičky **Predajná objednávka požiadavky na položku**. Ak žiadna hlavička otvorenej predajnej objednávky nemá vybratý fakturačný účet, systém ho vytvorí a priradí k nemu riadok požiadavky na položku.

> [!NOTE]
> Požiadavky na položky sú vždy plne fakturované na fakturačný účet, ktorý je nastavený v zázname. Systém momentálne nepodporuje pravidlá prideľovania financií, ktoré majú požiadavky na položky, a nerozdelí zaúčtovanie na základe nastavenia pravidiel prideľovania financií.

### <a name="create-an-item-requirement-from-an-item-forecast-record"></a>Vytvorenie požiadavky na položku zo záznamu prognózy položky

Ak chcete vytvoriť požiadavky na položku zo záznamu prognózy položky, postupujte podľa týchto krokov.

1. Prejdite na **Projektový manažment a účtovníctvo** \> **Projekty** \> **Všetky projekty** a vyberte záznam projektu.
1. Na karte **Plán** vyberte **Prognózy položiek**.
1. Vytvorte nový záznam prognózy položky.
1. Voliteľné: Na karte **Projekt** v poli **Zdroj financovania** vyberte požadovaný fakturačný účet.
1. Vyberte **Vytvoriť požiadavku na položku** a potvrďte prijatú správu.

    > [!NOTE]
    > Systém skopíruje hodnotu **Zdroj financovania** zo záznamu prognózy položky do novovytvoreného záznamu požiadavky na položku.

### <a name="default-invoice-account-when-the-system-automatically-creates-an-item-requirement-from-a-purchase-order-line"></a>Predvolený fakturačný účet, keď systém automaticky vytvorí požiadavku na položku z riadku nákupnej objednávky

Ak je možnosť **Vytvoriť požiadavku na položku** nastavená na **Áno** na stránke **Parametre projektového riadenia a účtovníctva**, systém automaticky vytvorí požiadavku na položku, keď sa uloží nový riadok projektovej objednávky. V predvolenom nastavení sú polia **Fakturačný účet** a **Požiadavka na položku** sú nastavené na hodnotu poľa **Predvolený fakturačný účet** v zázname projektu. Systém momentálne nepodporuje aktualizáciu ani zmenu fakturačného účtu pre záznamy tohto typu.
