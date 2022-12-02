---
title: Výkon návrhov projektových faktúr
description: Tento článok poskytuje informácie o vylepšeniach výkonnosti návrhov projektových faktúr.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: johnmichalak
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 70069778b7d4326cb23d6bb36e2c78a33da12573
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927209"
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
