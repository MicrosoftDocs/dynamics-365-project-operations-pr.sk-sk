---
title: Predvolené hodnoty finančnej dimenzie
description: Tento článok poskytuje informácie o tom, ako nastaviť predvolené hodnoty finančnej dimenzie.
author: sigitac
ms.date: 12/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9e0d739ac1b7681e2e77ec651daf3da8316ff
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931073"
---
# <a name="financial-dimension-defaults"></a>Predvolené hodnoty finančnej dimenzie

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_



Dynamics 365 Project Operations používa rámec [Finančné dimenzie](/dynamics365/finance/general-ledger/financial-dimensions) v Dynamics 365 Finance na poskytnutie ďalších prehľadov o transakciách v hlavnej a vedľajšej účtovnej knihe projektu.

Predvolené finančné dimenzie je možné nastaviť na zákazníka, zdroj financovania projektu, medzník, riadok projektovej zmluvy alebo projekt.

## <a name="define-default-financial-dimensions-for-a-customer"></a>Definovanie predvolených finančných dimenzií pre zákazníka

Predvolené hodnoty dimenzií zákazníka sú špecifikované v časti Financie. Na nastavenie predvolených dimenzií vykonajte nasledujúce kroky.

1. Prejdite do **Pohľadávky** > **Zákazníci** > **Všetci zákazníci**.
2. Na stránke **Zákazníci** na karte **Finančné dimenzie** nastavte hodnoty finančnej dimenzie pre konkrétneho zákazníka.

## <a name="define-default-financial-dimensions-for-project-contracts"></a>Definovanie predvolených finančných dimenzií pre projektové zmluvy

Projektové zmluvy sa vytvárajú a udržiavajú v Common Data Service (CDS). Účtovné atribúty pre projektové zmluvy sú stanovené v module **Projektový manažment a účtovníctvo** vo Financie.

### <a name="set-financial-dimensions-for-a-project-funding-source"></a>Stanovenie finančných dimenzií pre zdroj financovania projektu

1. Prejdite do časti **Projektový manažment a účtovníctvo** > **Projekty** > **Projektové zmluvy**.
2. Vyberte záznam, ktorý chcete aktualizovať, a na karte **Projektová zmluva** vyberte **Zobraziť predvolené účtovníctvo**.
3. Rozbaľte **Súvisiace informácie** a vyberte kartu **Zdroje financovania**.
4. Nastavte predvolené hodnoty finančnej dimenzie. Všimnite si, že finančné dimenzie sa predvolene získavajú z obchodného vzťahu zákazníka.

### <a name="set-financial-dimensions-for-a-project-contract-line"></a>Stanovenie finančných dimenzií pre riadok projektovej zmluvy

1. Prejdite do časti **Projektový manažment a účtovníctvo** > **Projekty** > **Projektové zmluvy**.
2. Vyberte záznam, ktorý chcete aktualizovať, a na karte **Projektová zmluva** vyberte **Zobraziť predvolené účtovníctvo**.
3. Rozbaľte **Súvisiace informácie** a vyberte kartu **Riadky zmluvy**.
4. Nastavte predvolené hodnoty finančnej dimenzie. Predvolené hodnoty finančnej dimenzie sú platné a je možné ich použiť iba pri riadkoch zmluvy s pevnou cenou (medzníkom).

Tieto predvolené hodnoty sa používajú v súvisiacich transakciách projektu na účte a na riadkoch faktúr.

## <a name="define-default-financial-dimensions-for-projects"></a>Definovanie predvolených finančných dimenzií pre projekty

Projekty sa vytvárajú a udržiavajú v CDS. Účtovné atribúty pre projekty sú stanovené v module **Projektový manažment a účtovníctvo** vo Financie.

1. Prejdite do časti **Riadenie projektu a účtovníctvo** > **Projekty** > **Všetky projekty**.
2. Vyberte záznam, ktorý chcete aktualizovať, a na karte **Projekt** vyberte **Zobraziť predvolené účtovníctvo**.
3. Rozbaľte **Súvisiace informácie** a vyberte kartu **Nastavenie**.
4. Nastavte predvolené hodnoty finančnej dimenzie. Všimnite si, že finančné dimenzie sa predvolene získavajú z obchodného vzťahu zákazníka. Ak je projekt spojený s riadkom zmluvy s viacerými zmluvnými zákazníkmi projektu, primárny zákazník sa použije na predvolené finančné dimenzie.

Predvolené finančné dimenzie projektu sa používajú na nastavenie predvolených hodnôt záznamov v účtovnom denníku pre časové, nákladové a poplatkové transakcie v **Denníku integrácie Project Operations** a na súvisiacich riadkoch projektových faktúr.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
