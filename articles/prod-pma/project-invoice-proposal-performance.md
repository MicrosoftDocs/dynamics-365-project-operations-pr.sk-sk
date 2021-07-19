---
title: Výkon návrhov projektových faktúr
description: Táto téma poskytuje informácie o vylepšeniach výkonnosti návrhov projektových faktúr.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269809"
---
# <a name="project-invoice-proposal-performance"></a>Výkon návrhov projektových faktúr

[!include [banner](../includes/banner.md)]

Keď vytvárate nový návrh faktúry, môžu sa pri zvyšovaní počtu projektov a podprojektov vyskytnúť problémy s výkonom. Na zlepšenie výkonu je k dispozícii funkcia, ktorá skracuje čas potrebný na vytvorenie nového návrhu faktúry za zaúčtované projektové transakcie.

## <a name="enable-project-invoice-proposal-performance-enhancement"></a>Povolenie zvýšenia výkonu návrhu projektovej faktúry
Ak chcete povoliť funkciu vylepšenia výkonu návrhu projektovej faktúry, vykonajte nasledujúce kroky.

1.  Prejdite do ponuky **Správa funkcií** > **Všetky**. V zozname funkcií vyhľadajte **Zlepšenie výkonu návrhu projektových faktúr**.
2.  Vyberte položku **Povoliť teraz**.
3.  Obnovte prehliadač a potom vytvorte nový návrh faktúry.

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a>Vypnutie zvýšenia výkonu návrhu projektovej faktúry
Ak chcete vypnúť funkciu vylepšenia výkonu návrhu projektovej faktúry, vykonajte nasledujúce kroky.

1.  Prejdite do ponuky **Správa funkcií** > **Všetky**. V zozname funkcií vyhľadajte **Zlepšenie výkonu návrhu projektových faktúr**.
2.  Vyberte položku **Zakázať**.
3.  Obnovte prehliadač.

> [!NOTE]
> Výkonnosť návrhu faktúry nie je možné použiť, keď sú povolené fakturačné pravidlá.
> 
> Počas dávkového procesu na vytvorenie návrhov faktúr počet čiastkových úloh rozdelí úlohy na maximálny počet na základe počtu zmlúv s fakturovateľnými transakciami bez ohľadu na to, čo ste zadali. Napríklad, ak zadáte **3** pre počet podúloh na hromadné vytvorenie návrhu faktúry a existujú iba dve zmluvy s fakturovateľnými transakciami, sú vytvorené iba dve podúlohy.
