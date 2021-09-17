---
title: Riadky subdodávateľskej zmluvy pre kategórie výdavkov
description: Táto téma vysvetľuje, ako zaznamenávať riadky subdodávateľskej zmluvy pre výdavky a používať polia na nákup času od dodávateľov.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323840"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Riadky subdodávateľskej zmluvy pre kategórie výdavkov

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Subdodávateľská zmluva v Dynamics 365 Project Operations môže mať riadok pre kategórie výdavkov. Riadky subdodávateľských zmlúv pre kategórie výdavkov umožňujú projektovému manažérovi nakupovať kategórie služieb alebo produktov od dodávateľov, ktoré môžu účtovať projektu.

Ak chcete vytvoriť riadok subdodávateľskej zmluvy pre kategórie výdavkov v Project Operations, postupujte podľa nasledujúcich pokynov.

1. Na navigačnej table vyberte položku **Subdodávateľské zmluvy** a otvorte subdodávateľskú zmluvu, s ktorou chcete pracovať.
2. Na karte **Riadky subdodávateľskej zmluvy** vyberte **Nový** a vytvorte nový riadok.
3. Na stránke **Rýchle vytvorenie** v poli **Trieda transakcie** vyberte **Výdavok** a zadajte alebo vyberte akékoľvek iné požadované informácie o poli.

Nasledujúca tabuľka poskytuje informácie o poliach na stránke s podrobnosťami **Riadok subdodávateľskej zmluvy** a stránke **Rýchle vytvorenie**.

| **Pole** |  **Opis** |
| ----------| ---------------- |
| Meno | Názov riadku subdodávateľskej zmluvy. |
| Popis | Stručný popis kategórií služieb alebo produktov, ktoré sa nakupujú v riadku subdodávateľskej zmluvy. |
| Typ riadka | Toto pole má predvolenú hodnotu **Založené na množstve**.  |
| Spôsob fakturácie | Spôsob fakturácie riadka subdodávateľskej zmluvy. Na základe metódy fakturácie v riadku je pre metódu fakturácie s pevnou cenou k dispozícii plán fakturácie založený na medzníkoch.  |
| Trieda transakcie | Toto pole má predvolenú hodnotu **Čas**. Ak chcete vytvoriť riadky subdodávateľských zmlúv na nákup produktov, nastavte pole **Trieda transakcie** na **Výdavok**. Hodnota tohto poľa naznačuje, že riadok subdodávateľskej zmluvy sa používa na zaznamenanie nákupu kategórie produktov alebo služieb, ktoré sa majú použiť v projektoch. |
| Kategória transakcie | Vyberte kategóriu transakcie. |
| Požadovaný štart | Dátum, kedy musia byť kategórie nákupov k dispozícii u predajcu. Požadovaný štart sa používa aj na výber cenníka projektu z cenníkov projektov pripojených k subdodávateľskej zmluve. Náklady na kategóriu na riadku subdodávateľskej zmluvy sa potom predvolene odvíjajú od tohto cenníka. |
| Požadovaný koniec | Dátum, kedy už kategórie nákupov nie sú potrebné. Tento dátum vyvolá varovanie, keď projektový manažér spojí tento riadok subdodávateľskej zmluvy s konkrétnymi odhadmi výdavkov na projekty, ktoré sú datované po tomto dátume. |
| Objednané množstvo | Množstvo kategórií, ktoré ste kúpili u predajcu. Ak vedúci projektu prečerpá nakúpené množstvo, zobrazí sa upozornenie.  |
| Skupina jednotiek | Táto hodnota poľa je predvolene založená na predvolenej jednotkovej skupine, ktorá je nastavená pre vybratú kategóriu. |
| Jednotka | Táto hodnota poľa je predvolene založená na predvolenej jednotke, ktorá je nastavená pre vybratú kategóriu. Kombinácia kategórie a jednotky sa používa ako predvolená jednotková cena na riadku subdodávateľskej zmluvy. |
| Jednotková cena | Hodnota poľa jednotkovej ceny sa predvolene používa z kombinácie kategórie a jednotky z cien kategórií súvisiacich s cenníkom projektu, ktorý je použiteľný pre požadovaný začiatok riadku subdodávateľskej zmluvy.  |
| Medzisúčet | Toto je pole iba na čítanie, ktoré sa automaticky počíta ako množstvo × jednotková cena, ak sú zadané hodnoty množstva aj jednotkovej ceny. Ak je niektoré z polí prázdne, môžete hodnotu tohto poľa zadať ručne.  |
| Daň z predaja | Zadajte sumu dane z predaja.  |
| Celková čiastka | Celková suma riadka subdodávateľskej zmluvy vrátane daní. Toto pole sa počíta ako medzisúčet + daň z predaja.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
