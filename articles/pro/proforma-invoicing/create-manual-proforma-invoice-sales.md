---
title: Vytvorenie manuálnej zálohovej faktúry
description: Táto téma poskytuje informácie o manuálnom vytváraní zálohovej faktúry v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084593"
---
# <a name="creating-a-manual-proforma-invoice"></a>Vytvorenie manuálnej zálohovej faktúry

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

V Dynamics 365 Project Operations možno zálohové faktúry podľa potreby vytvárať manuálne. Zálohovú faktúru môžete vytvoriť manuálne na stránke so zoznamom **Projektové zmluvy** alebo na stránke s podrobnosťami **Projektová zmluva**.

##  <a name="project-contracts-list-page"></a>Stránka so zoznamom projektovej zmluvy

Na stránke so zoznamom **Projektové zmluvy** vyberte jednu alebo viac projektových zmlúv a vytvorte faktúry pre všetky vybrané záznamy.

Systém kontroluje, ktoré z vybraných projektových zmlúv majú nevybavené termíny **Pripravené na faktúru** datované pred dnešným dátumom. Z týchto zmlúv systém vytvára koncepty zálohových faktúr. Ak má projektová zmluva viac zákazníkov, môže byť pre každého zákazníka vytvorená jedna faktúra a pre každú projektovú zmluvu viac faktúr.

Všetky vytvorené faktúry pre projekt sú k dispozícii na stránke **Faktúra** v časti **Fakturácia** v oblasti **Predaj**.

## <a name="project-contract-details-page"></a>Stránka s podrobnosťami o projektovej zmluve

Zálohovú faktúru je možné vytvoriť aj na stránke s podrobnosťami **Projektová zmluva** , kde sa vytvorí faktúra pre konkrétnu projektovú zmluvu. Systém overí, či má projektová zmluva nevybavený termín **Pripravené na faktúru** datovaný pred dnešným dátumom. Z týchto zmlúv systém vytvára koncepty zálohových faktúr na základe počtu zákazníkov v každom riadku zmluvy.

Po vytvorení samostatnej zálohovej faktúry sa otvorí stránka **Faktúra**. Ak je pre túto projektovú zmluvu vytvorených viac faktúr, tak sa otvorí stránka so zoznamom **Faktúry** , kde sa zobrazia všetky vytvorené faktúry.
