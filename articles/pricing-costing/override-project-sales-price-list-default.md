---
title: Prepísanie projektových predajných cenníkov
description: Táto téma poskytuje informácie o vytváraní prispôsobených predajných cenníkov.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275557"
---
# <a name="override-project-sales-price-lists"></a>Prepísanie projektových predajných cenníkov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

## <a name="customer-specific-project-price-lists"></a>Projektové cenníky pre konkrétneho zákazníka

Cenové dohody s konkrétnym zákazníkom je možné nastaviť ako projektové cenníky v zázname obchodného vzťahu v aplikácii Dynamics 365 Project Operations.

Ak chcete nastaviť projektový cenník pre konkrétneho zákazníka, prejdite do oblasti **Predaj** a následne k záznamu obchodného vzťahu.

1. Otvorte stránku so zoznamom **Obchodné vzťahy**.
2. Vyhľadajte a dvakrát kliknite na záznam zákazníka, čím otvoríte stránku s podrobnosťami **Obchodného vzťahu**.
3. Na karte **Projektové cenníky** vyberte **+ Nový projektový cenník**.
4. Na stránke **Nový projektový cenník** vyberte z rozbaľovacej ponuky cenník. Zahrnuté budú iba cenníky, ktoré majú nastavený kontext na **Predaj** a ktorých mena sa zhoduje s menou obchodného vzťahu.
5. Pomenujte priradenie a potom vyberte položku **Uložiť**. Vytvorí sa projektový cenník pre konkrétneho zákazníka. Tento cenník sa použije na predvolené projektové ceny v projektových cenových ponukách alebo zmluvách vytvorených pre tohto zákazníka, pričom dátum vytvorenia cenovej ponuky alebo projektovej zmluvy spadá do dátumu účinnosti cenníka.

## <a name="custom-pricing-on-project-quotes"></a>Vlastné ceny na základe projektových ponúk

V projektových cenových ponukách môžete mať stanovenú cenu projektu, ktorá sa začína predvoleným štandardným cenníkom, ktorý je predvolený od zákazníka alebo od parametrov projektu.

Ak potrebujete vlastnú cenu pre prácu súvisiacu s projektom v určitej cenovej ponuke, získate ju z entity priradenej k projektovým cenníkom.

Vykonaním nasledujúcich krokov nastavíte projektové cenu špecifickú pre cenovú ponuku.

1. Otvorte projektovú cenovú ponuku vyberte kartu **Projektové cenníky**.
2. Vo vedľajšej mriežke vyberte **Vytvorenie vlastných cien**.

Všetky cenníky projektu, ktoré sú priložené k cenovej ponuke, sa skopírujú do nových cenníkov. Názvy nových cenníkov odrážajú názov cenovej ponuky s časovou pečiatkou, kedy boli tieto cenníky vytvorené.

Môžete použiť každý z týchto cenníkov a aktualizovať ceny práce (cena roly) a výdavkov (cena kategórie). Tieto zmenené budú platiť iba na túto projektovú cenovú ponuku.

## <a name="price-lists-on-a-project-contract"></a>Projektové cenníky v projektovej zmluve

V projektovej zmluve je projektová cena vždy predvolená ako vlastný cenník s názvom zmluvy a časovou pečiatkou vytvorenia pripojenou k názvu. To platí bez ohľadu na to, či bola zmluva vytvorená pri získaní cenovej ponuky, alebo či bola zmluva vytvorená úplne od začiatku. V prípade potreby môžete toto priradenie k vlastnému cenníku odstrániť a namiesto toho priradiť štandardný cenník k projektovej zmluve.

Ak priraďujete štandardný cenník k projektovým cenníkom v cenovej ponuke alebo zmluve, akékoľvek zmeny cien v cenníku ovplyvnia všetky cenové ponuky a zmluvy, ktoré používajú cenník.


[!INCLUDE[footer-include](../includes/footer-banner.md)]