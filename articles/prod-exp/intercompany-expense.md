---
title: Medzipodnikové výdavky
description: Pracovník, ktorý je zamestnaný v jednej právnickej entite v organizácii, môže vykonávať prácu pre inú právnickú entitu v tej istej organizácii. V tejto situácii môžete pomocou funkcie medzipodnikových výdavkov priradiť výdavky pracovníka právnickej entite, pre ktorú bola práca vykonaná.
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084515"
---
# <a name="intercompany-expenses"></a>Medzipodnikové výdavky

[!include [banner](../includes/banner.md)]

Pracovník, ktorý je zamestnaný v jednej právnickej entite v organizácii, môže vykonávať prácu pre inú právnickú entitu v tej istej organizácii. V tejto situácii môžete pomocou funkcie medzipodnikových výdavkov priradiť výdavky pracovníka právnickej entite, pre ktorú bola práca vykonaná. Právnická entita, ktorá zamestnáva pracovníka, sa nazýva požičiavajúca právnická entita. Právnická entita, za ktorú pracovník znáša výdavky, sa nazýva požičiavajúca si právnická entita. 

Predtým, ako pracovník môže vytvoriť a odoslať výdavky na prácu, ktorá sa vykonáva pre inú právnickú entitu, v požičiavajúcej právnickej osobe, na stránke **Parametre správy výdavkov** vyberte možnosť **Povoliť medzipodnikové riadky výdavkov**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Zaúčtovanie dane pre medzipodnikové náklady

[!include [banner](../includes/banner.md)]

Ak chcete vo výkaze výdavkov použiť daňové skupiny, ktoré sú spojené s požičiavajúcou (zdrojovou) právnickou entitou, namiesto požičiavajúcej si (cieľovej) právnickej entity, budete to musieť nakonfigurovať v nastavení dane z predaja v hlavnej knihe. Keď je parameter hlavnej knihy **Právnická entita pre účtovanie daní medzi spoločnosťami** nastavená na **Zdroj** a **Použiť pravidlá zdaňovania dane z predaja** je nastavená na **Nie** , použije sa daňová kombinácia pre požičiavajúcu právnickú entitu. Keď je rovnaký parameter nastavený na **Cieľ** , použije sa daňová kombinácia pre požičiavajúcu si právnickú entitu. Pre právnické entity v Spojených štátoch, keď je parameter nastavený na **Zdroj** , musí byť pole **Pohľadávka z obratu** nakonfigurované aj na novej stránke **Skupiny účtovania v hlavnej knihe**. Účtovný nástroj použije informácie z tohto poľa pre účtovný záznam súvisiaci s daňou.   
Správanie je konzistentné pre riadky výdavkov zaúčtované s projektom alebo bez neho.  
