---
title: 'Nastavenie plánu preddavkov '
description: Tento článok poskytuje informácie o tom, ako nastaviť plán preddavkov v Project Operations.
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 077961d2f649754149315438252970609c246555
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927761"
---
# <a name="set-up-a-retainer-schedule"></a>Nastavenie plánu preddavkov 

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Plány preddavkov sú nastavené na stránke **Projektové zmluva** v Dynamics 365 Project Operations.

1. Na stránke **Projektová zmluva** na karte **Zálohy a preddavky** vyberte **Nastavenie plánu preddavkov**.
2. Na dialógovej stránke, ktorá sa otvorí, sa zobrazia polia uvedené v nasledujúcej tabuľke. Tabuľka poskytuje predstavu o tom, ako majú vložené hodnoty vplyv na plán preddavkov, ktorý sa vytvorí.

| Pole | Popis | Nadväzujúci vplyv |
| --- | --- | --- |
| Zákazník projektovej zmluvy | Zákazník v zmluve, ktorému bude fakturovaná táto záloha alebo preddavok. | Ak máte v zmluve viac zákazníkov a potrebujete každému z nich fakturovať konkrétnu zálohu alebo preddavok, vytvorte ručne jednu faktúru pre každého zákazníka. |
| Počiatočný dátum plánu preddavkov | Zadajte dátum začatia plánu preddavkov. | Tento dátum nemusí byť dátumom vytvorenia prvého preddavku alebo zálohy. Dátum vytvorenia prvého preddavku alebo zálohy je tiež ovplyvnený frekvenciou fakturácie. |
| Konečný dátum plánu preddavkov | Zadajte dátum skončenia plánu preddavkov. | Tento dátum nemusí byť dátumom vytvorenia posledného preddavku alebo zálohy. Dátum vytvorenia posledného preddavku alebo zálohy je tiež ovplyvnený frekvenciou fakturácie. |
| Počet preddavkov, ktoré sa majú vytvoriť | Keď zadáte počet vytváraných preddavkov, systém použije na vytvorenie počtu v tomto poli počiatočný dátum a frekvenciu. | Keď je toto pole manuálne aktualizované, systém ignoruje hodnotu v poli **Konečný dátum plánu preddavkov** a namiesto toho vytvorí konkrétny počet preddavkov alebo záloh. |
| Frekvencia faktúr | Ako často aplikácia vytvorí preddavky a zálohy. | Táto hodnota priamo ovplyvňuje počet preddavkov a záloh a vytvorené dátumy. |
| Celková čiastka | Celková suma je suma, ktorá sa rozdelí na jednotlivé preddavky alebo zálohy, ktoré sa vytvoria. | Toto pole nemá žiadny následný dopad. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]