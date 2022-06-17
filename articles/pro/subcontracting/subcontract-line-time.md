---
title: Riadky subdodávateľskej zmluvy pre čas
description: Tento článok vysvetľuje, ako zaznamenávať riadky subdodávok pre čas a zaznamenávať nákup času od dodávateľov.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0295ddd1b36eef9289110c4fe7b51397d81320d6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925967"
---
# <a name="subcontract-lines-for-time"></a>Riadky subdodávateľskej zmluvy pre čas

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Subdodávateľská zmluva v Dynamics 365 Project Operations môže mať pre čas riadok subdodávateľskej zmluvy. Riadky subdodávateľských zmlúv pre čas umožňujú projektovému manažérovi kúpiť čas zdrojov od dodávateľa na plnenie úloh projektu a požiadaviek na zdroje.

Ak chcete vytvoriť riadok subdodávateľskej zmluvy pre čas v Project Operations, postupujte podľa nasledujúcich pokynov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a otvorte subdodávateľskú zmluvu.
2. Na karte **Riadky subdodávateľskej zmluvy** vyberte **Nový** a vytvorte nový riadok subdodávateľskej zmluvy.
3. Na stránke **Rýchle vytvorenie** v poli **Trieda transakcie** vyberte **Čas**.
4. Zadajte zostávajúce informácie o poli a vyberte **Uložiť**.

  Nasledujúca tabuľka poskytuje informácie o poliach na stránke **Riadok subdodávateľskej zmluvy** a stránke **Rýchle vytvorenie**.

| **Pole** | **Opis** | **Funkčný vplyv** |
| --- | --- | --- |
| Meno | Názov riadka subdodávateľskej zmluvy, ktorý má pomôcť s identifikáciou. | Toto sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach na základe riadkov subdodávateľských zmlúv. |
| Popis | Stručný popis služieb, ktoré sa nakupujú na riadku subdodávateľskej zmluvy. |Nie je |
| Typ riadka |   Toto pole má predvolenú hodnotu **Založené na množstve**.| Nie je |
| Spôsob fakturácie | Toto je množina možností, ktorý predstavuje dva hlavné zmluvné modely podporované zo strany Project Operations: **Pevná cena** a **Čas a materiál**. | Na základe zvoleného spôsobu fakturácie je pre riadky subdodávateľov s metódou fakturácie s pevnou cenou k dispozícii míľnik založený na faktúre. |
| Trieda transakcie | Predvolená hodnota je **Čas**. | To naznačuje, že riadok zmluvy subdodávateľa sa používa na zaznamenanie času nákupu subdodávateľa. |
| Rola | Vyberte úlohu zdrojov subdodávateľov, ktorých čas sa nakupuje. | Rola vykonávaná zdrojmi subdodávateľov určuje náklady na nákup. |
| Požadovaný štart | Zadajte dátum, kedy sú zdroje subdodávateľa povinné začať pracovať. | Toto sa používa na výber cenníka projektu z cenníkov projektu pripojených k subdodávke. Náklady na úlohu na riadku subdodávateľskej zmluvy pochádzajú z tohto cenníka. |
| Požadovaný koniec | Zadajte dátum, kedy sa skončí priradenie zdroja subdodávateľa. | Toto sa použije na zobrazenie upozornení, keď projektový manažér čerpá z kapacity pre požiadavky na zdroje, ktoré sa vyskytnú po tomto dátume. |
| Objednané množstvo | Zadajte počet hodín roly, ktoré sa nakupujú u dodávateľa. | Toto sa použije na zobrazenie upozornení, keď projektový manažér prečerpá z kapacity pre požiadavky na zdroje. |
| Skupina jednotiek | Predvolená hodnota je **Skupina časových jednotiek**, ktorú nie je možné zmeniť. | Nie je|
| Jednotka | Predvolená hodnota pre toto pole je základná jednotka hodín od **Skupina časových jednotiek**. Túto hodnotu môžete zmeniť, aby ste si mohli kúpiť akúkoľvek jednotku **Skupiny časových jednotiek**, napríklad deň alebo týždeň. | Kombinácia **Rola** a **Jednotka** budú použité ako predvolené alebo vypočítané pre jednotkovú cenu pre riadok subdodávateľskej zmluvy. |
| Jednotková cena | Predvolená jednotková cena používa kombináciu **Rola** a **Jednotka** z cenníka projektu platného pre **Požadovaný dátum začatia** riadka subdodávateľskej zmluvy. | Keď má príslušný cenník projektu cenu nastavenú v inej jednotke, ako je jednotka v riadku subdodávateľskej zmluvy, systém použije na výpočet jednotkovej ceny prevod jednotiek. |
| Medzisúčet |    Toto je pole iba na čítanie, ktoré sa počíta ako množstvo x jednotková cena, ak sú zadané hodnoty množstva aj jednotkovej ceny. Ak buď je niektoré z polí Množstvo alebo Jednotková cena prázdne, môžete do poľa zadať hodnotu. | Nie je|
| Daň z predaja |   Zadajte sumu dane z predaja. |Nie je |
| Celková čiastka | Celková suma riadka subdodávateľskej zmluvy vrátane daní. Toto pole sa počíta ako medzisúčet + daň z predaja.|Nie je |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
