---
title: Výkazy výdavkov a viacerí schvaľovatelia
description: Táto téma poskytuje informácie o výkazoch výdavkov, ktoré si vyžadujú schválenie viac ako jednou osobou.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897110"
---
# <a name="expense-reports-and-multiple-approvers"></a>Výkazy výdavkov a viacerí schvaľovatelia

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V závislosti od politík schvaľovania výdavkov vašej organizácie môže byť potrebné, aby odovzdaný výkaz výdavkov schválila viac ako jedna osoba. Keď nastavujete proces pracovného postupu na schválenie výkazu výdavkov, môžete pridať prvky pracovného postupu, ktoré zahŕňajú úlohy alebo kroky pre jedného alebo viacerých schvaľovateľov výkazov výdavkov. Môžete napríklad požadovať, aby všetky výkazy výdavkov schvaľovali dve samostatné osoby, manažér zamestnanca, ktorý správu predložil, a koordinátor záväzkov.

Ak sa rozhodnete vyžadovať viacerých schvaľovateľov výkazov výdavkov, môžete prvky pracovného postupu pridať niektorým z nasledujúcich spôsobov:

- Pridajte jeden schvaľovací prvok, ktorý má jeden krok. Krok môže napríklad vyžadovať, aby bol výkaz výdavkov priradený k skupine používateľov a aby bol schválený 50 percentami členov skupiny používateľov.
- Pridajte jeden schvaľovací prvok, ktorý má viac krokov. Schvaľovací prvok môže mať napríklad nasledujúce kroky:

    1. Vedúci zamestnanca, ktorý predložil výkaz výdavkov, ho schvaľuje.
    2. Referent pre záväzky overuje účtenky a položky výkazu výdavkov.
    3. Vlastník rozpočtu schvaľuje výkaz výdavkov.

- Pridajte viac schvaľovacích prvkov, z ktorých každý má jeden krok. Môžete napríklad pridať samostatný schvaľovací prvok pre každý z nasledujúcich krokov:

    1. Vedúci zamestnanca schvaľuje výkaz výdavkov.
    2. Vlastník rozpočtu schvaľuje výkaz výdavkov.
