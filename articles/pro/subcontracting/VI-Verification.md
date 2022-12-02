---
title: Overenie faktúr dodávateľov so schválenými skutočnými hodnotami
description: Tento článok vysvetľuje, ako Microsoft Dynamics 365 Project Operations umožňuje projektovým manažérom overiť faktúry dodávateľov so skutočnými hodnotami, ktoré boli schválené, keď dodávatelia vykonali prácu a zaznamenali čas, a výdavky a materiály, ktoré použili členovia projektového tímu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 67e0a0143fa354ca9a87bfac5fbbd6306a97811c
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522961"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Overenie faktúr dodávateľov so schválenými skutočnými hodnotami

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Microsoft Dynamics 365 Project Operations umožňuje projektovým manažérom overiť riadky faktúry dodávateľa nasledujúcimi spôsobmi:

- Pomocou poľa **Stav overenia** v riadkoch faktúry dodávateľa.
- Ak riadky faktúry dodávateľa odkazujú na riadok subdodávateľskej zmluvy, prepojte skutočné hodnoty z činnosti aktivity subdodávateľa s týmito riadkami faktúry dodávateľa. Prepojenie sa vytvorí spárovaním skutočných hodnôt nákladov s riadkami faktúry dodávateľa.

    > [!NOTE]
    > Hoci stav overenia možno sledovať pre riadky faktúry dodávateľa, ktoré neodkazujú na subdodávateľskú zmluvu, skutočné náklady nemožno prepojiť s týmito riadkami faktúry dodávateľa.

## <a name="verification-status"></a>Stav overenia

Pole **Stav overenia** na riadku faktúry dodávateľa označuje tento stav overenia. Podporované sú nasledujúce stavy:

1. Nespustené
2. Prebieha
3. Dokončené

Riadky faktúry dodávateľa, ktoré majú stav overenia **Nezačaté**, je možné upravovať.

Riadky faktúry dodávateľa, ktoré majú stav overenia **Prebieha**, nie je možné upravovať. Pre riadok faktúry dodávateľa, ktorý odkazuje na subdodávateľskú zmluvu, je stav overenia automaticky nastavený na **Prebieha**, hneď ako sa prvá skutočná hodnota priradí k riadku faktúry dodávateľa.

Riadky faktúry dodávateľa, ktoré majú stav overenia **Dokončené**, nie je možné upravovať. Keď všetky riadky na faktúre dodávateľa majú tento stav overenia, faktúra dodávateľa môže byť potvrdená.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Spárovanie skutočných nákladov s riadkami faktúr dodávateľov

Párovanie skutočných nákladov pomáha pri procese overovania na riadku faktúry dodávateľa. Ak chcete spárovať skutočné náklady s riadkom faktúry dodávateľa, postupujte podľa týchto krokov.

1. Otvorte riadok faktúry dodávateľa a vyberte kartu **Nespárované skutočné hodnoty nákladov**. Mriežka zobrazuje zoznam skutočných nákladov, ktoré odkazujú na rovnaký riadok subdodávateľskej zmluvy ako riadok faktúry dodávateľa.
2. Vyberte jeden alebo viacero skutočných nákladov a potom vyberte **Spárovať** na paneli nástrojov nad mriežkou. Systém overí, či je možné spárovať vybrané skutočné náklady. Po overení sa skutočné náklady prepoja s riadkom faktúry dodávateľa.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Overovacie kritériá, ktoré sa používajú na prepojenie skutočných nákladov s riadkami faktúry dodávateľa

Počas procesu párovania je možné vytvoriť prepojenie medzi skutočnými nákladmi a riadkom faktúry dodávateľa, iba ak sú splnené obe nasledujúce podmienky:

- Pole **Stav úpravy** pre každý vybratý skutočný náklad musí byť prázdne. Inými slovami, skutočné náklady nesmú byť nahradené inými skutočnými nákladmi počas procesu storna, zrušenia schválenia alebo korekcii denníka.
- Hodnoty nasledujúcich polí sú spárované medzi riadkom faktúry dodávateľa a vybratými skutočnými nákladmi. Ak v riadku faktúry dodávateľa nie je nastavené žiadne pole, nebude sa brať do úvahy pri párovaní.

    - Projektová zmluva
    - Riadok projektovej zmluvy
    - Trieda transakcie
    - Project
    - Úloha
    - Kategória zdroja
    - Kategória transakcie
    - Produkt
    - Riadok subdodávateľskej zmluvy
    - Rezervovateľný zdroj

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Zrušenie spárovania skutočných nákladov z riadku faktúry dodávateľa

Zrušenie spárovania skutočných nákladov môže tiež pomôcť s procesom overovania na faktúre dodávateľa tým, že umožňuje odstrániť predtým vytvorené prepojenia. Skutočné náklady možno odpárovať len z riadkov faktúr dodávateľa, ktoré majú stav overenia **Prebieha**. Ak chcete zrušiť spárovanie skutočných nákladov s riadkom faktúry dodávateľa, postupujte podľa týchto krokov.

1. Otvorte riadok faktúry dodávateľa a vyberte kartu **Spárované skutočné hodnoty nákladov**. Mriežka zobrazuje zoznam skutočných nákladov, ktoré odkazujú na riadok faktúry dodávateľa.
2. Vyberte jeden alebo viac skutočných nákladov a potom vyberte **Zrušiť spárovanie** na paneli nástrojov nad mriežkou.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
