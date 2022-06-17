---
title: Kopírovanie projektu
description: Tento článok poskytuje informácie o kopírovaní projektov v Dynamics 365 Project Operations.
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: b358f9e45278d886f3e6e8e8cd747fc0ea30212b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925783"
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
- Kontrolné zoznamy projektov
- Projektové vedrá

## <a name="project-properties"></a>Vlastnosti projektu

Pri kopírovaní projektu sa skopírujú hodnoty v nasledujúcich poliach.

| Pole | Projektové operácie Neskladové materiály | Project Operations Lite | Projekt pre web |
|-------|------------------------------------------|-------------------------|---------------------|
| Name | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Description | :heavy_check_mark: | :heavy_check_mark: | |
| zákazník | :heavy_check_mark: | :heavy_check_mark: | |
| Šablóna kalendára | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Mena | :heavy_check_mark: | :heavy_check_mark: | |
| Zmluvná jednotka | :heavy_check_mark: | :heavy_check_mark: | |
| Vlastniaca spoločnosť | :heavy_check_mark: | | |
| Projektový manažér | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Status | :heavy_check_mark: | :heavy_check_mark: | |
| Celkový stav projektu | :heavy_check_mark: | :heavy_check_mark: | |
| Vytvoril | :heavy_check_mark: | :heavy_check_mark: | |
| Odhady | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Odhadovaný dátum začatia</p><p><strong>Poznámka:</strong> Toto pole určuje dátum vytvorenia projektu z kópie. | :heavy_check_mark: | :heavy_check_mark: | |
| <p>Odhadovaný dátum dokončenia</p><p><strong>Poznámka:</strong> Dátum v tomto poli je upravený na základe dátumu začiatku nového projektu, ktorý bol vytvorený z kópie.</p> | :heavy_check_mark: | :heavy_check_mark: | |
| Úsilie (hodiny) | :heavy_check_mark: | :heavy_check_mark: | |
| Odhadované mzdové náklady | :heavy_check_mark: | :heavy_check_mark: | |
| Odhadované výdavkové náklady | :heavy_check_mark: | :heavy_check_mark: | |
| Odhadované materiálové náklady | | :heavy_check_mark: | |

> [!NOTE]
> Kopírovanie projektu je dlhodobá operácia. Skopírujú sa tiež záznamy projektu, ich príslušné atribúty a veľa súvisiacich entít. Z dôvodu dlhodobého charakteru operácie sa po spustení kopírovania uzamkne cieľová stránka projektu na účely vykonávania úprav, kým nebude kopírovanie dokončené.

## <a name="work-breakdown-structure"></a>Štruktúra rozdelenia práce

Pri kopírovaní projektu sa skopíruje celá štruktúra rozdelenia práce načítaná zdrojom. Pomenované zdroje sa nahradia všeobecnými zdrojmi. Ak pomenované zdroje nemajú rovnaký pracovný čas ako všeobecný zdroj, plán sa prepočíta a trvanie úloh sa môže zmeniť.

## <a name="project-team-members"></a>Členovia projektového tímu

Keď sa projektový tím skopíruje zo zdrojového projektu, skopírujú sa všeobecné zdroje. Priradenie všeobecných zdrojov sa zachová rovnaké ako bolo pri zdrojovom projekte. Pomenované zdroje sa prevedú na všeobecných členov tímu.

> [!NOTE]
> Členovia tímu a úlohy sa v Projecte pre web neskopírujú.

## <a name="estimates"></a>Odhady

Pri skopírovaní projektu sa zo zdrojového projektu skopírujú riadky s odhadmi zdrojov, výdavkov a materiálov. 

Informácie o tom, ako programovo získať prístup k možnosti kopírovania projektu nájdete v časti [Vytvorenie šablóny projektu pomocou kopírovania projektu](dev-copy-project.md).

## <a name="quotes-and-contracts"></a>Cenové ponuky a zmluvy

Cenové ponuky a zmluvy nie sú prepojené s cieľovým projektom.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
