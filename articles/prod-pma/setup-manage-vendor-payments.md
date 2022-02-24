---
title: Nastavenie a použitie platieb typu „zaplatiť po zaplatení“ pre dodávateľov
description: Táto téma vysvetľuje, ako vytvoriť podmienky PWP (pay-when-paid), aby ste mohli uvoľniť čiastočné platby dodávateľa na základe platieb zákazníka.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
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
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084343"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Nastavenie a použitie platieb typu „zaplatiť po zaplatení“ pre dodávateľov

[!include [banner](../includes/banner.md)]

Keď schválite dodávateľa, aby pracoval ako subdodávateľ, možno budete chcieť zadržať platbu dodávateľovi, kým vám zákazník za projekt nezaplatí. Na podporu tohto scenára môžete nastaviť podmienky platby za platbu (PWP) pri nastavovaní objednávky (PO) u dodávateľa.

Napríklad keď zákazník zaplatí sumu na faktúre za projekt, môžete uvoľniť časť alebo celú sumu faktúry dodávateľa. Stačí nastaviť podmienky PWP, ktoré určujú, že predajcovi bude vyplatené, keď dostanete od zákazníka percento súvisiacej platby. Ak dostanete čiastočnú platbu od zákazníka, môžete manuálne uvoľniť niektoré súvisiace faktúry dodávateľa na platbu.

Nasledujúci príklad načrtáva postup, keď sa používajú termíny PWP.

## <a name="example"></a>Príklad

Vaša organizácia sa zaväzuje poskytnúť zákazníkovi 100 počítačov, ktoré majú nainštalovaný softvér, za cenu 150 USD (USD) za počítač. Potom si najmete predajcu, ktorý vám poskytne počítače s nainštalovaným softvérom. Podľa dohody musí zákazník schváliť kvalitu počítačov skôr, ako zaplatí vašej organizácii. Politikou vašej organizácie je zadržiavanie platieb dodávateľom, kým vám zákazník nezaplatí. Preto ste nastavili projekt tak, aby mal 100-percentné PWP.

Predajca vám pošle 100 počítačov, ktoré majú nainštalovaný softvér, spolu s faktúrou za 10 000.00 USD. Pretože sú pre váš projekt nastavené podmienky PWP, neplatíte predajcovi po prijatí počítačov. Namiesto toho odošlete zákazníkovi počítače spolu s faktúrou za 15 000,00. Zákazník skontroluje počítače a schváli celú sumu projektovej faktúry.

Po prijatí celej platby od zákazníka zaplatíte dodávateľovi 10 000.00 celú sumu faktúry dodávateľa.

## <a name="set-up-pwp-terms-for-a-project"></a>Nastaviť podmienky PWP pre projekt

Keď nastavujete podmienky PWP pre projekt, musíte percentuálne určiť minimálnu sumu, ktorú vám musí zákazník zaplatiť za projekt, skôr ako zaplatíte predajcovi. Prahová hodnota sa automaticky počíta na zákazníckych faktúrach za projekt. Podľa týchto pokynov môžete nastaviť prahové percento pre výrazy PWP.

1. Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Všetky projekty**.
2. Nájdite a otvorte projekt, pre ktorý chcete nastaviť podmienky PWP.
3. Na karte FastTab **Zmluvy s predajcom** stlačte možnosť **Pridať riadok**.
3. V poli **Kód účtu** vyberte jednu z nasledujúcich možností:

    - **Tabuľka** – Podmienky PVP sa vzťahujú na jedného dodávateľa.
    - **Skupina** – Podmienky PWP sa vzťahujú na všetkých dodávateľov v skupine dodávateľov.
    - **Všetky** – Podmienky PWP sa vzťahujú na všetkých dodávateľov.

4. Ak ste stlačili možnosť **Tabuľka** alebo **Skupina** v predchádzajúcom kroku, v poli **Dodávateľ/skupina dodávateľov** vyberte dodávateľa alebo skupinu dodávateľov, na ktorých sa vzťahujú podmienky PWP. Ak ste v predošlom kroku zvolil možnosť **Všetky**, pole **Dodávateľ/skupina dodávateľov** nemožno upravovať.
5. Ak sú pre dodávateľa v projekte stanovené podmienky uchovania dodávateľa, v poli **Podmienky uchovania dodávateľa** vyberte ID pravidla pre podmienky uchovania.
6. V poli **Percentuálna hodnota PWP** zadajte percentuálne prahové hodnoty pre projekt. Percento, ktoré zadáte pre projekt, určuje minimálnu sumu, ktorú vám musí zákazník zaplatiť, skôr ako zaplatíte dodávateľovi.

## <a name="create-a-po-that-has-pwp-terms"></a>Vytvorte PO, ktorá má podmienky PWP

Keď účtujete faktúru od dodávateľa a ak sa na dodávateľa vzťahujú podmienky PWP, tieto podmienky sa zobrazia na riadkoch objednávky. Ak chcete vytvoriť objednávku, ktorá má podmienky PWP, postupujte podľa týchto krokov.

1. Prejdite do **Obstarávanie a získavanie zdrojov**\>**Nákupné objednávky**\>**Všetky nákupné objednávky**.
2. Na table Akcia vyberte možnosť **Nový**. Potom v dialógovom okne **Vytvoriť nákupnú objednávku** zadajte požadované informácie a stlačte možnosť **OK**.

    Prípadne otvorte existujúcu objednávku na stránke zoznamu **Všetky nákupné objednávky**.

4. Na stránke **Nákupná objednávka** na karte **Riadky nákupných objednávok**, skontrolujte podrobnosti o riadku objednávky pre dodávateľa. Možnosť **Zaplatiť po zaplatení** sa automaticky vyberie a hodnota v poli **Percentuálna hodnota PWP** sa automaticky skopíruje z poľa **Percentuálna hodnota PWP** na stránke **Projekty**.
6. Ak nechcete uplatniť podmienky PWP na dodávateľa pre linku objednávky, zrušte začiarknutie možnosti **Zaplatiť po zaplatení**. V takom prípade pole **Percentuálna hodnota PWP** pre riadok PO sa nastaví na 0 (nula).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Aktualizujte platbu zákazníkom a zaplaťte dodávateľovi

Keď dodávateľ dokončí svoju prácu na projekte a pošle vám faktúru, musíte skontrolovať stav projektu a faktúry zákazníka, aby ste zistili, či boli pre projekt splnené podmienky PWP. Ak boli podmienky PWP pre dodávateľa splnené, môžete na základe platieb zákazníka za projekt určiť, ktoré riadky na faktúre dodávateľa sa majú zaplatiť. Ak sa rozhodnete zaplatiť predajcovi, aj keď neboli splnené podmienky PWP, môžete tieto podmienky PWP prepísať na stránke **Faktúra dodávateľa s platbou, keď je zaplatená**.

1. Prejdite do **Projektové riadenie a účtovníctvo** \> **Dotazy a zostavy** \> **Retenčné otázky** \> **Faktúra dodávateľa s platbou, keď je zaplatená**.
2. Na stránke **Faktúra dodávateľa s platbou, keď je zaplatená** do vyhľadávacieho poľa zadajte hodnoty, aby ste našli faktúru dodávateľa, ktorú chcete skontrolovať, a potom stlačte **Vyhľadať**.
3. Na karte FastTab **Riadky faktúr dodávateľa** vyberte riadky, ktoré chcete zmeniť.
4. Ak sú splnené podmienky **Zaplatiť po zaplatení** pre riadok faktúry, stlačte možnosť **Uvoľnite platbu dodávateľa**. Možnosť **Zaplatiť po zaplatení** sa zruší a hodnota poľa **Pripravené na platbu** sa zmení na **Áno**.
