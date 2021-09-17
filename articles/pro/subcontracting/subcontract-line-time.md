---
title: Riadky subdodávateľskej zmluvy pre čas
description: Táto téma vysvetľuje, ako zaznamenávať riadky subdodávateľskej zmluvy pre čas a zaznamenávať nákup času od dodávateľov.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323885"
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

| **Pole** | **Opis** |
| --- | --- |
| Meno | Názov riadku subdodávateľskej zmluvy. |
| Popis | Stručný popis služieb, ktoré sa nakupujú na riadku subdodávateľskej zmluvy. | 
| Typ riadka | Toto pole je predvolená hodnota.  |
| Spôsob fakturácie | Vyberte typu fakturácie. Na základe metódy fakturácie v uvedenom riadku subdodávateľskej zmluvy je pre metódu fakturácie s pevnou cenou k dispozícii plán fakturácie založený na medzníku. |
| Trieda transakcie | Toto pole je predvolená hodnota, ktorá označuje, či sa na zaznamenanie nákupu času subdodávateľa používa riadok subdodávateľskej zmluvy. |
| Rola | Rola zdrojov subdodávateľskej zmluvy, ktorých čas sa nakupuje. Rola priradená zdrojom subdodávateľskej zmluvy určuje náklady na nákup. |
| Požadovaný štart | Dátum, kedy sú zdroje subdodávateľa povinné začať pracovať. Požadovaný štart sa používa aj na výber cenníka projektu z cenníkov projektov pripojených k subdodávateľskej zmluve. Náklady na rolu na riadku subdodávateľskej zmluvy sa potom predvolene odvíjajú od tohto cenníka. |
| Požadovaný koniec | Dátum, kedy sa skončí priradenie zdrojov subdodávateľa. Tento dátum sa používa na zobrazenie upozornení, keď projektový manažér čerpá z tejto kapacity pre požiadavky na zdroje, ktoré sa vyskytnú po tomto dátume. |
| Objednané množstvo | Počet hodín rolí zakúpených u dodávateľa. Táto hodnota sa používa na zobrazenie upozornení, keď projektový manažér nadmerne čerpá z tejto kapacity pre požiadavky na zdroje. |
| Skupina jednotiek | Táto hodnota poľa je predvolene nastavená na jednotkovú skupinu Čas a nemožno ju zmeniť.  |
| Jednotka | Toto pole je predvolene nastavené na základnú jednotku hodín z jednotkovej skupiny Čas. Túto hodnotu môžete zmeniť, aby ste si mohli kúpiť akúkoľvek jednotku jednotkovej skupiny Čas, napríklad deň alebo týždeň. Kombinácia Roly a Jednotky sa používa na výpočet jednotkovej ceny na riadku subdodávateľskej zmluvy. |
| Jednotková cena | Jednotková cena sa predvolene používa z kombinácie Roly a Jednotky z cenníka projektu, ktorý je použiteľný pre požadovaný dátum začiatku riadku subdodávateľskej zmluvy. Keď má príslušný cenník projektu cenu nastavenú v inej jednotke, ako je jednotka v riadku subdodávateľskej zmluvy, systém použije na výpočet jednotkovej ceny prevod jednotiek. |
| Medzisúčet | Toto je pole iba na čítanie, ktoré sa automaticky počíta ako **Množstvo × Jednotková cena**, ak sú zadané hodnoty množstva aj jednotkovej ceny. Ak buď je niektoré z polí Množstvo alebo Jednotková cena prázdne, môžete do poľa zadať hodnotu. |
| Daň z predaja |  Zadajte sumu dane z predaja. |
| Celková čiastka | Celková suma riadka subdodávateľskej zmluvy po zahrnutí daní. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
