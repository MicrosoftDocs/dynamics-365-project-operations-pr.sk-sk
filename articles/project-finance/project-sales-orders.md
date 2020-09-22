---
title: Projektové predajné objednávky pre projekty typu „čas a materiál“
description: Táto téma vysvetľuje, ako vytvoriť projektové predajné objednávky pre projekty typu „čas a materiál“.
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755540"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektové predajné objednávky pre projekty typu „čas a materiál“

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Táto téma popisuje, ako vytvoriť predajnú objednávku pre projekt. Predajné objednávky je možné vytvoriť iba pre projekty typu **čas a materiál**.

Ak má projekt typu „čas a materiál“ na projektovej zmluve viac zdrojov financovania, musíte povoliť parameter **Povoliť predajné objednávky pre projekty s viacerými zdrojmi financovania** na stránke **Parametre projektového riadenia a účtovníctva**. 

> [!NOTE]
> - Podpora pre projektové predajné objednávky s viacerými zdrojmi financovania je k dispozícii počnúc vydaním aplikácie 10.0.2 a vyšším.
> - Parameter umožňujúci podporu projektových predajných objednávok s viacerými zdrojmi financovania bude odstránený vo vlne vydania v apríli 2020, po ktorej bude táto funkcia vždy povolená.

Projektové predajné objednávky môžete vytvoriť dvoma spôsobmi:

- Prejdite do samotného projektu. Na table Akcia vyberte možnosť **Spravovať > Úlohy položiek > Predajná objednávka**. Informácie o projekte budú predvolene nastavené na predajnú objednávku z projektu. Ak má projektová zmluva viac ako jeden zdroj financovania, budete musieť zvoliť zdroj financovania, aby ste zákazníka nastavili na predajnú objednávku. Ak je pre projekt k dispozícii iba jeden zdroj financovania, zákazník sa nastaví automaticky.
- Prejdite na stránku so zoznamom **Všetky predajné objednávky** a vytvorte novú predajnú objednávku. Budete musieť vybrať projekt pre predajnú objednávku. Po výbere projektu sa zákazník nastaví zo zdroja financovania alebo budete musieť zvoliť zdroj financovania, ak má projektová zmluva viac zdrojov financovania.

