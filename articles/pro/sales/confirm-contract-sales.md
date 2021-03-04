---
title: Potvrdenie projektovej zmluvy
description: Táto téma poskytuje informácie o spôsobe potvrdenia zmluvy v aplikácii Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 24da0887c0266d51bddcbbf8efd6f2644b6d0f4f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128303"
---
# <a name="confirm-a-project-contract"></a>Potvrdenie projektovej zmluvy

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Projektová zmluva v systéme Dynamics 365 Project Operations môže byť aktívna s dôvodom **Potvrdená**, alebo uzavretá s dôvodom **Nevyužitá**. Po potvrdení projektovej zmluvy sa stav aktualizuje z **Koncept** na **Aktívna** a dôvod stavu je **Potvrdená**. Aktívnu alebo uzavretú zmluvu nie je možné upraviť ani znova otvoriť. 

### <a name="financial-impact-of-confirming-a-project-contract"></a>Finančný dopad potvrdenia projektovej zmluvy

Po potvrdení projektovej zmluvy aplikácia prepočíta náklady obrátením starších skutočných nákladov a vytvorením nových skutočných nákladov. Nové skutočné náklady sa potom spracujú na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu. Ak sa skutočné náklady odvolávajú na riadok zmluvy Čas a materiál, aplikácia automaticky znova vytvorí príslušné nevyfakturované skutočné hodnoty predaja. Ak sa skutočné náklady odvolávajú na riadok zmluvy Pevná cena, aplikácia zastaví spracovanie skutočných nákladov.

V rámci procesu potvrdzovania sa vyhodnocujú a aktualizujú limity, ktoré sa nesmú prekročiť, nastavenie účtovateľnosti a ceny a náklady pri skutočných hodnotách.

## <a name="close-a-project-contract-as-lost"></a>Uzavretie projektovej zmluvy ako nevyužitej

Keď uzavriete projektovú zmluvu ako nevyužitú, stav zmluvy sa aktualizuje na **Uzavretá** a dôvod stavu je **Nevyužitá**. Projektová zmluva bude iba na čítanie. Pred dokončením zmien sa zobrazí dialógové okno s potvrdením, pretože nemôžete znovu otvoriť uzavretú projektovú zmluvu.

Ak projektová zmluva, ktorá je uzavretá ako nevyužitá, odkazuje na projekt v jeho riadkoch, tento projekt sa tiež označí ako uzavretý. Všetky rezervácie zdrojov od daného dňa budú zrušené. Akékoľvek nevyfakturované predajné skutočné údaje o projektovej zmluve, ktoré ešte nie sú na faktúre, budú vrátené späť.

> [!NOTE]
> V systéme Dynamics 365 Project Operations nebude mať uzavretie projektovej zmluvy ako nevyužitej žiadny vplyv na tento stav súvisiacej príležitosti. Príležitosť zostane otvorená a musí byť uzavretá manuálne.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]