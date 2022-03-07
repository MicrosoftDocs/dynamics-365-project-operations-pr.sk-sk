---
title: Medzipodnikové výdavky
description: Táto téma poskytuje informácie o spôsobe použitia medzipodnikových výdavkov na priradenie výdavkov pracovníka k právnickej osobe, pre ktorú bola práca vykonaná.
author: Surya Vaidyanathan
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 80ef42bf5274ff9a5c50e6dcb93995cfbbda40a66d7471f29ebf056086320640
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001225"
---
# <a name="intercompany-expenses"></a>Medzipodnikové výdavky

Pracovník, ktorý je zamestnaný v jednej právnickej entite v organizácii, môže vykonávať prácu pre inú právnickú entitu v tej istej organizácii. Môžete použiť medzipodnikové výdavky na priradenie výdavkov pracovníka k právnickej osobe, pre ktorú bola práca vykonaná. Právnická entita, ktorá zamestnáva pracovníka, sa nazýva požičiavajúca právnická entita. Právnická entita, za ktorú pracovník znáša výdavky, sa nazýva požičiavajúca si právnická entita. 

Predtým, ako pracovník bude môcť vytvárať a odosielať medzipodnikové výdavky, musíte povoliť riadky medzipodnikových výdavkov. V prenajímajúcej právnickej osobe na stránke **Parametre riadenia výdavkov** vyberte možnosť **Povoliť riadky medzipodnikových výdavkov**. 

## <a name="tax-posting-for-intercompany-expenses"></a>Zaúčtovanie dane pre medzipodnikové náklady

[!include [banner](../includes/banner.md)]

Predtým, ako budete môcť vo svojom výkaze výdavkov použiť daňové skupiny spojené s požičiavajúcou (zdrojovou) právnickou osobou namiesto požičiavajúcej (cieľovej) právnickej osoby, musíte povoliť funkciu v nastavení dane z obratu hlavnej knihy. Keď je parameter **Právnická osoba pre účtovanie medzipodnikových daní** nastavený na **Zdroj** a možnosť **Použiť pravidlá zdaňovania dane z obratu** je nastavená na **Nie**, použije sa daňová kombinácia pre požičiavajúcu právnickú osobu. Keď je rovnaký parameter nastavený na **Cieľ**, použije sa daňová kombinácia pre požičiavajúcu si právnickú entitu. Pre právnické entity v Spojených štátoch, keď je parameter nastavený na **Zdroj**, musí byť pole **Pohľadávka z obratu** nakonfigurované aj na novej stránke **Skupiny účtovania v hlavnej knihe**. Účtovný nástroj použije informácie z tohto poľa pre účtovný záznam súvisiaci s daňou.   
Správanie je konzistentné pre riadky výdavkov zaúčtované s projektom alebo bez neho.  

## <a name="new-expense-expression-builder"></a>Nový nástroj na tvorbu výrazov pre výdavky

Nový nástroj na tvorbu výrazov pre výdavky rieši problémy so vnútropodnikovými scenármi výdavkov, ktoré používajú projekty. Táto funkcia zaisťuje, že keď vytvoríte medzipodnikové výdavky, politika výdavkov sa správne overí voči projektu, ktorý je vybratý na riadku výdavkov, a že správu o výdavkoch je možné úspešne odoslať.

Aby funkcia tvorcu výrazov pre výdavky fungovala, musí byť zapnutá. Okrem toho by mala byť nastavená politika výdavkov, ktorá má ID projektu.

Ak ste už nakonfigurovali politiky, ktoré overujú ID projektu na riadku výdavkov, tieto politiky musia byť zrušené. Potom môžete funkciu zapnúť a prekonfigurovať politiky.

Ak chcete funkciu zapnúť, postupujte podľa týchto pokynov.

1. Prejdite do časti **Pracovné priestory** \> **Správa funkcií**.
2. V zozname vyberte **Nový nástroj na tvorbu výrazov na riešenie problémov so scenármi vnútropodnikových výdavkov, ktoré používajú projekty**. Potom vyberte **Povoliť**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
