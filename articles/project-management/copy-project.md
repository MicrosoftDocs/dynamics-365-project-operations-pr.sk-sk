---
title: Kopírovanie projektu
description: Táto téma poskytuje informácie o kopírovaní projektov v aplikácii Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe76f59b315fd0f46b25e1d116acde1f6b2864d1753e01d6311ea93ae7d116fc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007210"
---
# <a name="copy-a-project"></a>Kopírovanie projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

S aplikáciou Dynamics 365 Project Operations môžete rýchlo vytvárať nové projekty pomocou výberu možnosti **Kopírovať projekt** na formulári **Projekty**. Ak chcete skopírovať projekt, otvorte projekt, ktorý chcete skopírovať, a potom vyberte **Kopírovať projekt**. Touto akciou sa skopíruje nasledovné:

- Vlastnosti projektu 
- Štruktúra rozdelenia práce
- Členovia projektového tímu
- Odhady projektu
- Odhady projektových výdavkov
- Odhady materiálov projektu

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
- Odhadovaný dátum začiatku: Toto je dátum vytvorenia projektu z kópie.
- Odhadovaný dátum konca: Tento dátum je prispôsobený na základe dátumu začiatku nového projektu, ktorý bol vytvorený z kópie.
- Úsilie (hodiny)
- Odhadované mzdové náklady
- Odhadované výdavkové náklady
- Odhadované materiálové náklady

> [!NOTE]
> Kopírovanie projektu je dlhodobá operácia. Skopírujú sa tiež záznamy projektu, ich príslušné atribúty a veľa súvisiacich entít. Z dôvodu dlhodobého charakteru operácie sa po spustení kopírovania uzamkne cieľová stránka projektu na účely vykonávania úprav, kým nebude kopírovanie dokončené.

## <a name="work-breakdown-structure"></a>Štruktúra rozdelenia práce

Pri kopírovaní projektu sa skopíruje celá štruktúra rozdelenia práce načítaná zdrojom. Pomenované zdroje sa nahradia všeobecnými zdrojmi. Ak pomenované zdroje nemajú rovnaký pracovný čas ako všeobecný zdroj, plán sa prepočíta a trvanie úlohy sa môže zmeniť.

## <a name="project-team-members"></a>Členovia projektového tímu

Keď sa projektový tím skopíruje zo zdrojového projektu, skopírujú sa všeobecné zdroje. Priradenie všeobecných zdrojov sa zachová rovnaké ako bolo pri zdrojovom projekte. Pomenované zdroje sa prevedú na všeobecných členov tímu.

## <a name="estimates"></a>Odhady

Pri skopírovaní projektu sa zo zdrojového projektu skopírujú riadky s odhadmi zdrojov, výdavkov a materiálov. 

Informácie o tom, ako programovo získať prístup k možnosti kopírovania projektu nájdete v časti [Vytvorenie šablóny projektu pomocou kopírovania projektu](dev-copy-project.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
