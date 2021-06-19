---
title: Potvrdenie projektovej zmluvy
description: Táto téma poskytuje informácie o spôsobe potvrdenia zmluvy v aplikácii Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003695"
---
# <a name="confirm-a-project-contract"></a>Potvrdenie projektovej zmluvy

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Zmluva o projekte v aplikácii Dynamics 365 Project Operations môže byť aktívna z dôvodu **Potvrdené**, alebo môže byť uzavretá z dôvodu **Stratené**. Po potvrdení projektovej zmluvy sa stav aktualizuje z **Koncept** na **Aktívna** a dôvod stavu je **Potvrdená**. Aktívnu alebo uzavretú zmluvu nie je možné upraviť ani znova otvoriť. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finančný dopad potvrdenia projektovej zmluvy

Po potvrdení projektovej zmluvy aplikácia prepočíta náklady obrátením starších skutočných nákladov a vytvorením nových skutočných nákladov. Nové skutočné náklady sa potom spracujú na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu. Ak sa skutočné náklady odvolávajú na riadok zmluvy Čas a materiál, aplikácia automaticky znova vytvorí príslušné nevyfakturované skutočné hodnoty predaja. Ak sa skutočné náklady odvolávajú na riadok zmluvy Pevná cena, aplikácia zastaví spracovanie skutočných nákladov.

V rámci procesu potvrdzovania sa vyhodnocujú a aktualizujú limity, ktoré sa nesmú prekročiť, nastavenie účtovateľnosti a ceny a náklady pri skutočných hodnotách.

## <a name="close-a-project-contract-as-lost"></a>Uzavretie projektovej zmluvy ako nevyužitej

Keď uzavriete projektovú zmluvu ako nevyužitú, stav zmluvy sa aktualizuje na **Uzavretá** a dôvod stavu je **Nevyužitá**. Projektová zmluva bude iba na čítanie. Pred dokončením zmien sa zobrazí dialógové okno s potvrdením, pretože nemôžete znovu otvoriť uzavretú projektovú zmluvu.

Ak projektová zmluva, ktorá je uzavretá ako nevyužitá, odkazuje na projekt v jeho riadkoch, tento projekt sa tiež označí ako uzavretý. Všetky rezervácie zdrojov od daného dňa budú zrušené. Akékoľvek nevyfakturované predajné skutočné údaje o projektovej zmluve, ktoré ešte nie sú na faktúre, budú vrátené späť.

> [!NOTE]
> V aplikácii Dynamics 365 Project Operations uzavretie projektovej zmluvy ako stratenej nebude mať vplyv na tento stav súvisiacej príležitosti. Príležitosť zostane otvorená a musí byť uzavretá manuálne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]