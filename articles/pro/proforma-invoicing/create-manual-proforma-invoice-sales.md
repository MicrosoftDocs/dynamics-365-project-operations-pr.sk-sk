---
title: Vytvorenie manuálnej faktúry pro forma – čiastočné
description: Táto téma poskytuje informácie o manuálnom vytváraní zálohovej faktúry v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764522"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>Vytvorenie manuálnej faktúry pro forma – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations je možné podľa potreby vytvárať proforma faktúry ručne. Zálohovú faktúru môžete vytvoriť manuálne na stránke so zoznamom **Projektové zmluvy** alebo na stránke s podrobnosťami **Projektová zmluva**.

##  <a name="project-contracts-list-page"></a>Stránka so zoznamom projektovej zmluvy

Na stránke so zoznamom **Projektové zmluvy** vyberte jednu alebo viac projektových zmlúv a vytvorte faktúry pre všetky vybrané záznamy.

Systém kontroluje, ktoré z vybraných projektových zmlúv majú nevybavené termíny **Pripravené na faktúru** datované pred dnešným dátumom. Z týchto zmlúv systém vytvára koncepty zálohových faktúr. Ak má projektová zmluva viac zákazníkov, môže byť pre každého zákazníka vytvorená jedna faktúra a pre každú projektovú zmluvu viac faktúr.

Všetky vytvorené faktúry pre projekt sú k dispozícii na stránke **Faktúra** v časti **Fakturácia** v oblasti **Predaj**.

## <a name="project-contract-details-page"></a>Stránka s podrobnosťami o projektovej zmluve

Proforma faktúra môže byť vytvorená aj na stránke s podrobnosťami **Zmluva o projekte**. Systém overuje, ktoré z projektových zmlúv majú nevybavené termíny **Pripravené na faktúru** datované pred dnešným dátumom. Z týchto zmlúv systém vytvára koncepty zálohových faktúr na základe počtu zákazníkov v každom riadku zmluvy.

Po vytvorení samostatnej zálohovej faktúry sa otvorí stránka **Faktúra**. Ak sa pre túto projektovú zmluvu vytvorí viac faktúr, otvorí sa stránka so zoznamom **Faktúry**, kde sa zobrazia všetky vytvorené faktúry.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]