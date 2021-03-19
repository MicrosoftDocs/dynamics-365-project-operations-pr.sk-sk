---
title: Kopírovanie projektu
description: Táto téma poskytuje informácie o kopírovaní projektov v aplikácii Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479538"
---
# <a name="copy-a-project"></a>Kopírovanie projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

S aplikáciou Dynamics 365 Project Operations môžete rýchlo vytvárať nové projekty pomocou výberu možnosti **Kopírovať projekt** na formulári **Projekty**. Ak chcete skopírovať projekt, otvorte projekt, ktorý chcete skopírovať, a potom vyberte **Kopírovať projekt**. Vykonaním akcie sa skopíruje:

- Vlastnosti projektu (odhadovaný dátum začatia sa skopíruje zo zdrojového projektu)
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

Informácie o tom, ako programovo získať prístup k možnosti kopírovania projektu nájdete v časti [Vytvorenie šablóny projektu pomocou kopírovania projektu](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
