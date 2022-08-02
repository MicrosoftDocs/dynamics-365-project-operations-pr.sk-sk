---
title: Overenie faktúr dodávateľov so schválenými skutočnými hodnotami
description: Tento článok vysvetľuje, ako spoločnosť Microsoft Dynamics 365 Project Operations Poďme projektových manažérov overiť faktúry dodávateľov so skutočnosťami, ktoré boli schválené, keď dodávatelia vykonali prácu a zaznamenali čas, a výdavky a materiály, ktoré použili členovia projektového tímu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7bf48dd17063daece5df3ce44c0375eec3dc3cae
ms.sourcegitcommit: 49c2a668b8d7bf0acb9e9b0bb44687e6d3dcaa8c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/28/2022
ms.locfileid: "9204194"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Overenie faktúr dodávateľov so schválenými skutočnými hodnotami

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Microsoft Dynamics 365 Project Operations Poďme projektových manažérov overiť riadky faktúry dodávateľa nasledujúcimi spôsobmi:

- Použi **Stav overenia** v riadkoch faktúry dodávateľa.
- Ak riadky faktúry dodávateľa odkazujú na riadok subdodávky, prepojte skutočné náklady z činnosti subdodávateľa s týmito riadkami faktúry dodávateľa. Prepojenie sa vytvorí spárovaním skutočných nákladov s riadkami faktúry dodávateľa.

    > [!NOTE]
    > Hoci stav overenia možno sledovať pre riadky faktúry dodávateľa, ktoré neodkazujú na subdodávku, skutočné náklady nemožno prepojiť s týmito riadkami faktúry dodávateľa.

## <a name="verification-status"></a>Stav overenia

The **Stav overenia** pole na riadku faktúry dodávateľa označuje tento stav overenia. Podporované sú nasledujúce stavy:

1. Nespustené
2. Prebieha
3. Dokončené

Riadky faktúry dodávateľa, ktoré majú stav overenia **Nezačal** je možné upraviť.

Riadky faktúry dodávateľa, ktoré majú stav overenia **Prebieha** už nie je možné upravovať. Pre riadok faktúry dodávateľa, ktorý odkazuje na subdodávku, je stav overenia automaticky nastavený na **Prebieha** hneď ako sa prvá skutočná cena priradí k riadku faktúry dodávateľa.

Riadky faktúry dodávateľa, ktoré majú stav overenia **Dokončiť** už nie je možné upravovať. Keď všetky riadky na faktúre dodávateľa majú tento stav overenia, faktúra dodávateľa môže byť potvrdená.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Priraďte skutočné náklady k riadkom faktúry dodávateľa

Párovanie skutočných nákladov pomáha pri procese overovania na riadku faktúry dodávateľa. Ak chcete priradiť skutočné náklady k riadku faktúry dodávateľa, postupujte podľa týchto krokov.

1. Otvorte riadok faktúry dodávateľa a vyberte **Neporovnateľné skutočné náklady** tab. Mriežka zobrazuje zoznam skutočných nákladov, ktoré odkazujú na rovnaký riadok subdodávky ako riadok faktúry dodávateľa.
2. Vyberte jednu alebo viacero skutočných nákladov a potom vyberte **Zápas** na paneli nástrojov nad mriežkou. Systém overí, či je možné spárovať vybrané skutočné náklady. Po overení sa skutočné náklady prepoja s riadkom faktúry dodávateľa.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Overovacie kritériá, ktoré sa používajú na prepojenie skutočných nákladov s riadkami faktúry dodávateľa

Počas procesu párovania je možné vytvoriť prepojenie medzi skutočnými nákladmi a riadkom faktúry dodávateľa, iba ak sú splnené obe nasledujúce podmienky:

- The **Stav úpravy** pole pre každú vybratú skutočnú cenu musí byť prázdne. Inými slovami, skutočné náklady nesmú byť nahradené inými skutočnými nákladmi počas procesu stiahnutia, zrušenia schválenia alebo denníka opráv.
- Hodnoty nasledujúcich polí sú spárované medzi riadkom faktúry dodávateľa a vybratými skutočnými nákladmi. Ak v riadku faktúry dodávateľa nie je nastavené žiadne pole, nebude sa brať do úvahy pri párovaní.

    - Projektová zmluva
    - Riadok projektovej zmluvy
    - Trieda transakcie
    - Project
    - Úloha
    - Kategória zdrojov
    - Kategória transakcie
    - Produkt
    - Subdodávateľská linka
    - Rezervovateľný zdroj

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Zrušte spárovanie skutočných nákladov z riadku faktúry dodávateľa

Nezodpovedanie skutočných nákladov môže tiež pomôcť s procesom overovania na faktúre dodávateľa tým, že umožňuje odstrániť predtým vytvorené prepojenia. Skutočné náklady možno zrušiť len z riadkov faktúry dodávateľa, ktoré majú stav overenia **Prebieha**. Ak chcete zrušiť zhodu skutočných nákladov z riadku faktúry dodávateľa, postupujte podľa týchto krokov.

1. Otvorte riadok faktúry dodávateľa a vyberte **Prirovnané skutočné náklady** tab. Mriežka zobrazuje zoznam skutočných nákladov, ktoré odkazujú na riadok faktúry dodávateľa.
2. Vyberte jednu alebo viacero skutočných nákladov a potom vyberte **Neporovnateľné** na paneli nástrojov nad mriežkou.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
