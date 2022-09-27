---
title: Zaplatiť pri platbe dodávateľa
description: Táto téma vysvetľuje, ako použiť scenár platby pri zaplatení (PWP).
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
# <a name="pay-when-paid-vendor-payments"></a>Zaplatiť pri platbe dodávateľa

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma vysvetľuje, ako použiť scenár platby pri zaplatení (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Vytvorte nákupnú objednávku, ktorá má podmienky PWP

Keď zaúčtujete faktúru od dodávateľa, ak dodávateľ podlieha podmienkam PWP, tieto podmienky sa zobrazia v riadkoch nákupnej objednávky (PO). Ak chcete vytvoriť objednávku, ktorá má podmienky PWP, postupujte podľa týchto krokov.

1. In Microsoft Dynamics 365 Finance, postupujte podľa jedného z týchto krokov:

    - Prejdite do **Obstarávanie a získavanie zdrojov**\>**Nákupné objednávky**\>**Všetky nákupné objednávky**. Na table Akcia vyberte možnosť **Nový**. V **Vytvorte nákupnú objednávku** v dialógovom okne vyberte dodávateľa, pre ktorého sú v projekte nastavené podmienky PWP, zadajte ďalšie požadované informácie a potom vyberte **OK**.
    - Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Všetky projekty**. Na paneli akcií na **Spravovať** kartu, vyberte **Úloha položky**. Vyberte nákupnú objednávku. Vyberte dodávateľa, pre ktorého sú v projekte nastavené podmienky PWP, a potom vyberte **OK**.

2. Na **Objednávka** stránke, na **Riadky nákupných objednávok** Rýchla karta, vyberte **Pridať riadok** na vytvorenie riadku nákupnej objednávky.
3. Vyberte číslo položky alebo kategóriu obstarávania a zadajte ďalšie požadované podrobnosti. Skontrolujte podrobnosti o riadku objednávky pre dodávateľa.

    Možnosť **Zaplatiť po zaplatení** sa automaticky vyberie a hodnota v poli **Percentuálna hodnota PWP** sa automaticky skopíruje z poľa **Percentuálna hodnota PWP** na stránke **Projekty**.

4. Ak nechcete uplatniť podmienky PWP na dodávateľa pre linku objednávky, zrušte začiarknutie možnosti **Zaplatiť po zaplatení**. V tomto prípade, **Percento prahovej hodnoty PWP** pole pre riadok PO bude resetované na **0** (nula).
5. Na **Objednávka** na paneli akcií na **Nákup** kartu, vyberte **Potvrďte** na potvrdenie objednávky.
6. Na paneli akcií na **Faktúra** kartu, vyberte **Faktúra** na vygenerovanie faktúry za objednávku.

## <a name="create-a-project-invoice-proposal"></a>Vytvorte návrh projektovej faktúry

Návrhy projektových faktúr sa používajú na vytváranie projektových faktúr pre zákazníka. V scenári PWP sú platby dodávateľa závislé od platieb zákazníkov podľa nastavení PWP. Existujú však možnosti, ktoré vám umožnia uvoľniť platby bez platieb zákazníkom, ako požadujete. Ak chcete vytvoriť projektovú faktúru pre zákazníka, postupujte podľa týchto krokov.

1. V aplikáciách na interakciu so zákazníkmi prejdite na **Projekt** \> **projekty** a vyberte projekt.
2. Na **Aktuálne** vyberte skutočný riadok, ktorý generuje PO, ktorý má **Nevyfakturovaný predaj** typ transakcie. Potom vyberte **Pripravené na faktúru**.
3. Ísť do **Predaj** \> **Predaj** \> **Projektová zmluva** a vyberte zmluvu o projekte.
4. Na table akcií vyberte **Faktúra** na vygenerovanie zákazníckej faktúry.
5. V časti Financie prejdite na **Projektový manažment a účtovníctvo** \> **Pravidelné** \> **Import z pracovnej tabuľky** a vyberte **OK** na vygenerovanie denníka integrácie operácií projektu.
6. Ísť do **Projektový manažment a účtovníctvo** \> **Projektové faktúry** \> **Návrh projektovej faktúry** a vyberte **Príspevok** zaúčtovať návrh faktúry, ktorý bol vygenerovaný pre projekt.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizujte platbu zákazníkom a zaplaťte dodávateľovi

Keď dodávateľ dokončí svoju prácu na projekte a pošle vám faktúru, musíte skontrolovať stav projektu a zákaznícke faktúry, aby ste zistili, či boli pre projekt splnené podmienky PWP. Ak boli podmienky PWP pre dodávateľa splnené, môžete na základe platieb zákazníka za projekt určiť, ktoré riadky na faktúre dodávateľa sa majú zaplatiť. Ak sa rozhodnete zaplatiť predajcovi, aj keď neboli splnené podmienky PWP, môžete tieto podmienky PWP prepísať na stránke **Faktúra dodávateľa s platbou, keď je zaplatená**.

1. V časti Financie prejdite na **Projektový manažment a účtovníctvo** \> **projekty** \> **Všetky projekty** a vyberte projekt.
2. Na table akcií vyberte **Kontrola** a potom vyberte **Dodávateľské faktúry** zobraziť všetky faktúry dodávateľa, ktoré boli vygenerované pre projekt.
3. Na stránke **Faktúra dodávateľa s platbou, keď je zaplatená** do vyhľadávacieho poľa zadajte hodnoty, aby ste našli faktúru dodávateľa, ktorú chcete skontrolovať, a potom stlačte **Vyhľadať**.
4. Vyberte **Zaplatiť pri zaplatení** možnosť zobrazenia iba faktúr PWP.
5. Na **Riadky faktúry dodávateľa** Rýchla karta, vyberte riadky, ktoré chcete uvoľniť na platbu.
6. Vyberte **Uvoľnite platbu dodávateľa**. Možnosť **Zaplatiť po zaplatení** sa zruší a hodnota poľa **Pripravené na platbu** sa zmení na **Áno**.
