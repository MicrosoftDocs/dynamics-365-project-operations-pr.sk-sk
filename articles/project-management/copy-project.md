---
title: Kopírovanie projektu
description: Táto téma poskytuje informácie o kopírovaní projektu v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e35dc725e7938e9f59f7151dd1b37500fabf77a4
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908583"
---
# <a name="copy-a-project"></a>Kopírovanie projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Vďaka Dynamics 365 Project Operations môžete rýchlo vytvárať nové projekty pomocou akcie **Kopírovať projekt** vo formulári **Projekty**. Ak chcete skopírovať projekt, vyberte projekt a potom vyberte **Kopírovať**. Vykonaním akcie sa skopíruje:

- Vlastnosti projektu
- Štruktúra rozdelenia práce
- Členovia projektového tímu
- Odhady projektu
- Odhady projektových výdavkov

## <a name="project-properties"></a>Vlastnosti projektu

Pri kopírovaní projektu sa skopírujú hodnoty v nasledujúcich poliach:

- Meno
- Popis
- Zákazník
- Šablóna kalendára
- Mena
- Zmluvná jednotka
- Projektový manažér
- Status
- Celkový stav projektu
- Vytvoril
- Odhady
- Odhadovaný dátum začatia
- Dátum dokončenia
- Úsilie (hodiny)
- Odhadované mzdové náklady
- Odhadované výdavkové náklady

## <a name="work-breakdown-structure"></a>Štruktúra rozdelenia práce

Pri kopírovaní projektu sa skopíruje celá štruktúra rozdelenia práce načítaná zdrojom. Pomenované zdroje sa nahradia všeobecnými zdrojmi. Ak pomenované zdroje nemajú rovnaký pracovný čas ako všeobecný zdroj, plán sa prepočíta a trvanie úlohy sa môže zmeniť.

## <a name="project-team-members"></a>Členovia projektového tímu

Keď sa projektový tím skopíruje zo zdrojového projektu, skopírujú sa všeobecné zdroje. Priradenie všeobecných zdrojov sa zachová rovnaké ako bolo pri zdrojovom projekte. Pomenované zdroje sa prevedú na všeobecných členov tímu.

## <a name="estimates"></a>Odhady

Pri kopírovaní projektu sa zo zdrojového projektu skopírujú riadky odhadu zdrojov a výdavkov.