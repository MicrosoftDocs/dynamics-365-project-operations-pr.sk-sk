---
title: Viacero schvaľovateľov vo výkaze výdavkov
description: Táto téma poskytuje informácie o výkazoch výdavkov, ktoré si vyžadujú schválenie viacerými osobami.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b6d07f00fd6c1ba2d860787665d95f95f7b1a89
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960626"
---
# <a name="multiple-approvers-on-an-expense-report"></a>Viacero schvaľovateľov vo výkaze výdavkov

V závislosti od politík schvaľovania výdavkov vašej organizácie môže byť potrebné, aby výkaz výdavkov odovzdaný zamestnancom schválila viac ako jedna osoba. Keď nastavujete proces pracovného postupu na schválenie výkazu výdavkov, môžete pridať prvky pracovného postupu, ktoré zahŕňajú úlohy alebo kroky pre jedného alebo viacerých schvaľovateľov výkazov výdavkov. Môžete napríklad požadovať, aby všetky výkazy výdavkov schvaľoval najskôr manažér zamestnanca, ktorý správu predložil a potom koordinátor záväzkov.

Ak sa rozhodnete vyžadovať viacerých schvaľovateľov výkazov výdavkov, môžete prvky pracovného postupu pridať niektorým z nasledujúcich spôsobov:

- Pridajte jeden schvaľovací prvok, ktorý má jeden krok. Krok môže napríklad vyžadovať, aby bol výkaz výdavkov priradený k skupine používateľov a aby bol schválený 50 percentami členov skupiny používateľov.
- Pridajte jeden schvaľovací prvok, ktorý má viac krokov. Schvaľovací prvok môže mať napríklad nasledujúce kroky:

    1. Vedúci zamestnanca, ktorý predložil výkaz výdavkov, ho schvaľuje.
    2. Referent pre záväzky overuje účtenky a položky výkazu výdavkov.
    3. Vlastník rozpočtu schvaľuje výkaz výdavkov.

- Pridajte viac schvaľovacích prvkov, z ktorých každý má jeden krok. Môžete napríklad pridať samostatný schvaľovací prvok pre každý z nasledujúcich krokov:

    1. Vedúci zamestnanca schvaľuje výkaz výdavkov.
    2. Vlastník rozpočtu schvaľuje výkaz výdavkov.
