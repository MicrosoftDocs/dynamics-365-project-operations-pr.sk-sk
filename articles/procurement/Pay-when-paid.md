---
title: Platba po zaplatení platieb dodávateľom
description: Táto téma vysvetľuje, ako použiť scenár platby po zaplatení (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525393"
---
# <a name="pay-when-paid-vendor-payments"></a>Platba po zaplatení platieb dodávateľom

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma vysvetľuje, ako použiť scenár platby po zaplatení (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Vytvorte nákupnú objednávku, ktorá má podmienky PWP

Keď účtujete faktúru od dodávateľa a ak sa na dodávateľa vzťahujú podmienky PWP, tieto podmienky sa zobrazia na riadkoch nákupnej objednávky (PO). Ak chcete vytvoriť objednávku, ktorá má podmienky PWP, postupujte podľa týchto krokov.

1. V Microsoft Dynamics 365 Finance postupujte podľa jedného z týchto krokov:

    - Prejdite do **Obstarávanie a získavanie zdrojov**\>**Nákupné objednávky**\>**Všetky nákupné objednávky**. Na table Akcia vyberte možnosť **Nový**. V dialógovom okne **Vytvoriť nákupnú objednávku** vyberte dodávateľa, pre ktorého sú v projekte nastavené podmienky PWP, zadajte ďalšie požadované informácie a potom vyberte **OK**.
    - Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Všetky projekty**. Na table akcií na karte **Spravovať** vyberte **Úloha položky**. Vyberte nákupnú objednávku. Vyberte dodávateľa, pre ktorého sú v projekte nastavené podmienky PWP, a potom vyberte **OK**.

2. Na stránke **Nákupná objednávka**, na rýchlej karte **Riadky nákupných objednávok** vyberte **Pridať riadok** na vytvorenie riadku nákupnej objednávky.
3. Vyberte číslo položky alebo kategóriu obstarávania a zadajte ďalšie požadované podrobnosti. Skontrolujte podrobnosti o riadku PO pre dodávateľa.

    Možnosť **Zaplatiť po zaplatení** sa automaticky vyberie a hodnota v poli **Percentuálna hodnota PWP** sa automaticky skopíruje z poľa **Percentuálna hodnota PWP** na stránke **Projekty**.

4. Ak nechcete uplatniť podmienky PWP na dodávateľa pre linku objednávky, zrušte začiarknutie možnosti **Zaplatiť po zaplatení**. V takom prípade pole **Percentuálny prah PWP** pre riadok PO sa nastaví na **0** (nula).
5. Na stránke **Nákupná objednávka** na paneli akcií na karte **Nákup** vyberte **Potvrdiť** na potvrdenie nákupnej objednávky.
6. Na paneli akcií na karte **Faktúra** vyberte **Faktúra** na vygenerovanie faktúry za nákupnú objednávku.

## <a name="create-a-project-invoice-proposal"></a>Vytvorenie návrhu projektovej faktúry

Návrhy projektových faktúr sa používajú na vytváranie projektových faktúr pre zákazníka. V scenári PWP sú platby dodávateľa závislé od platieb zákazníkov podľa nastavení PWP. Existujú však možnosti, ktoré vám umožnia uvoľniť platby bez platieb zákazníkom, ako požadujete. Ak chcete vytvoriť projektovú faktúru pre zákazníka, postupujte podľa týchto krokov.

1. V aplikáciách na interakciu so zákazníkmi prejdite do časti **Projekt** \> **Projekty** a vyberte projekt.
2. Na karte **Skutočné hodnoty** vyberte riadok skutočnej hodnoty, ktorý generuje PO, ktorý má typ transakcie **Nefakturovaný predaj**. Potom vyberte **Pripravené pre faktúru**.
3. Prejdite do **Predaj** \> **Predaj** \> **Projektová zmluva** a vyberte projektovú zmluvu.
4. Na table akcií vyberte položku **Faktúra** , ak chcete vygenerovať faktúru pre zákazníka.
5. Vo Finance prejdite na **Projektový manažment a účtovníctvo** \> **Periodické** \> **Import z pracovnej tabuľky** a vyberte **OK**, aby ste vytvorili denník integrácie Project Operations.
6. Prejdite do **Projektový manažment a účtovníctvo** \> **Projektové faktúry** \> **Návrh projektovej faktúry** a vyberte **Zaúčtovať** na zaúčtovanie návrhu faktúry, ktorý bol vygenerovaný pre projekt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizujte platbu zákazníkom a zaplaťte dodávateľovi

Keď dodávateľ dokončí svoju prácu na projekte a pošle vám faktúru, musíte skontrolovať stav projektu a faktúry zákazníka, aby ste zistili, či boli pre projekt splnené podmienky PWP. Ak boli podmienky PWP pre dodávateľa splnené, môžete na základe platieb zákazníka za projekt určiť, ktoré riadky na faktúre dodávateľa sa majú zaplatiť. Ak sa rozhodnete zaplatiť predajcovi, aj keď neboli splnené podmienky PWP, môžete tieto podmienky PWP prepísať na stránke **Faktúra dodávateľa s platbou, keď je zaplatená**.

1. Vo časti Finance prejdite na **Projektový manažment a účtovníctvo** \> **Projekty** \> **Všetky projekty** a vyberte projekt.
2. Na table akcií vyberte **Kontrola** a potom vyberte **Faktúry dodávateľa** na zobrazenie všetkých faktúr dodávateľa, ktoré boli vygenerované pre projekt.
3. Na stránke **Faktúra dodávateľa s platbou, keď je zaplatená** do vyhľadávacieho poľa zadajte hodnoty, aby ste našli faktúru dodávateľa, ktorú chcete skontrolovať, a potom stlačte **Vyhľadať**.
4. Vyberte možnosť **Zaplatiť po zaplatení** na zobrazenie iba faktúr PWP.
5. Na rýchlej karte **Riadky faktúr dodávateľa** vyberte riadky, ktoré chcete uvoľniť na platbu.
6. Vyberte **Uvoľniť platbu dodávateľa**. Možnosť **Zaplatiť po zaplatení** sa zruší a hodnota poľa **Pripravené na platbu** sa zmení na **Áno**.
