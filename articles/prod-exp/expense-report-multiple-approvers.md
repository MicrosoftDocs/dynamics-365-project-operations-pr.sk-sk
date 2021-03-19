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
ms.openlocfilehash: 0fbe1c93c5359a6be493e3c4e1b27b06dbb48002
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271732"
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]