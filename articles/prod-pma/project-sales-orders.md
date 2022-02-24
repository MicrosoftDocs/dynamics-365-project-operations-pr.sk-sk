---
title: Projektové predajné objednávky pre projekty typu „čas a materiál“
description: Táto téma vysvetľuje, ako vytvoriť projektové predajné objednávky pre projekty typu „čas a materiál“.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084349"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a>Projektové predajné objednávky pre projekty typu „čas a materiál“

[!include[banner](../includes/banner.md)]

Táto téma popisuje, ako vytvoriť predajnú objednávku pre projekt. Predajné objednávky je možné vytvoriť iba pre projekty typu **čas a materiál**.

Ak má projekt typu „čas a materiál“ na projektovej zmluve viac zdrojov financovania, musíte povoliť parameter **Povoliť predajné objednávky pre projekty s viacerými zdrojmi financovania** na stránke **Parametre projektového riadenia a účtovníctva**. 

> [!NOTE]
> - Podpora pre projektové predajné objednávky s viacerými zdrojmi financovania je k dispozícii počnúc vydaním aplikácie 10.0.2 a vyšším.
> - Parameter umožňujúci podporu projektových predajných objednávok s viacerými zdrojmi financovania bude odstránený vo vlne vydania v apríli 2020, po ktorej bude táto funkcia vždy povolená.

Projektové predajné objednávky môžete vytvoriť dvoma spôsobmi:

- Prejdite do samotného projektu. Na table Akcia vyberte možnosť **Spravovať > Úlohy položiek > Predajná objednávka**. Informácie o projekte budú predvolene nastavené na predajnú objednávku z projektu. Ak má projektová zmluva viac ako jeden zdroj financovania, budete musieť zvoliť zdroj financovania, aby ste zákazníka nastavili na predajnú objednávku. Ak je pre projekt k dispozícii iba jeden zdroj financovania, zákazník sa nastaví automaticky.
- Prejdite na stránku so zoznamom **Všetky predajné objednávky** a vytvorte novú predajnú objednávku. Budete musieť vybrať projekt pre predajnú objednávku. Po výbere projektu sa zákazník nastaví zo zdroja financovania alebo budete musieť zvoliť zdroj financovania, ak má projektová zmluva viac zdrojov financovania.

