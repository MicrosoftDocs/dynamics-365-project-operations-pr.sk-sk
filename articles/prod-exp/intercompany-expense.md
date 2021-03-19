---
title: Medzipodnikové výdavky
description: Táto téma poskytuje informácie o spôsobe použitia medzipodnikových výdavkov na priradenie výdavkov pracovníka k právnickej osobe, pre ktorú bola práca vykonaná.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271552"
---
# <a name="intercompany-expenses"></a>Medzipodnikové výdavky

Pracovník, ktorý je zamestnaný v jednej právnickej entite v organizácii, môže vykonávať prácu pre inú právnickú entitu v tej istej organizácii. Môžete použiť medzipodnikové výdavky na priradenie výdavkov pracovníka k právnickej osobe, pre ktorú bola práca vykonaná. Právnická entita, ktorá zamestnáva pracovníka, sa nazýva požičiavajúca právnická entita. Právnická entita, za ktorú pracovník znáša výdavky, sa nazýva požičiavajúca si právnická entita. 

Predtým, ako pracovník bude môcť vytvárať a odosielať medzipodnikové výdavky, musíte povoliť riadky medzipodnikových výdavkov. V prenajímajúcej právnickej osobe na stránke **Parametre riadenia výdavkov** vyberte možnosť **Povoliť riadky medzipodnikových výdavkov**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Zaúčtovanie dane pre medzipodnikové náklady

[!include [banner](../includes/banner.md)]

Predtým, ako budete môcť vo svojom výkaze výdavkov použiť daňové skupiny spojené s požičiavajúcou (zdrojovou) právnickou osobou namiesto požičiavajúcej (cieľovej) právnickej osoby, musíte povoliť funkciu v nastavení dane z obratu hlavnej knihy. Keď je parameter **Právnická osoba pre účtovanie medzipodnikových daní** nastavený na **Zdroj** a možnosť **Použiť pravidlá zdaňovania dane z obratu** je nastavená na **Nie**, použije sa daňová kombinácia pre požičiavajúcu právnickú osobu. Keď je rovnaký parameter nastavený na **Cieľ**, použije sa daňová kombinácia pre požičiavajúcu si právnickú entitu. Pre právnické entity v Spojených štátoch, keď je parameter nastavený na **Zdroj**, musí byť pole **Pohľadávka z obratu** nakonfigurované aj na novej stránke **Skupiny účtovania v hlavnej knihe**. Účtovný nástroj použije informácie z tohto poľa pre účtovný záznam súvisiaci s daňou.   
Správanie je konzistentné pre riadky výdavkov zaúčtované s projektom alebo bez neho.  


[!INCLUDE[footer-include](../includes/footer-banner.md)]