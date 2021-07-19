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
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="ea1cd-103">Výkon návrhov projektových faktúr</span><span class="sxs-lookup"><span data-stu-id="ea1cd-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea1cd-104">Keď vytvárate nový návrh faktúry, môžu sa pri zvyšovaní počtu projektov a podprojektov vyskytnúť problémy s výkonom.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="ea1cd-105">Na zlepšenie výkonu je k dispozícii funkcia, ktorá skracuje čas potrebný na vytvorenie nového návrhu faktúry za zaúčtované projektové transakcie.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="ea1cd-106">Povolenie zvýšenia výkonu návrhu projektovej faktúry</span><span class="sxs-lookup"><span data-stu-id="ea1cd-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="ea1cd-107">Ak chcete povoliť funkciu vylepšenia výkonu návrhu projektovej faktúry, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="ea1cd-108">Prejdite do ponuky **Správa funkcií** > **Všetky**.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="ea1cd-109">V zozname funkcií vyhľadajte **Zlepšenie výkonu návrhu projektových faktúr**.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="ea1cd-110">Vyberte položku **Povoliť teraz**.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="ea1cd-111">Obnovte prehliadač a potom vytvorte nový návrh faktúry.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="ea1cd-112">Vypnutie zvýšenia výkonu návrhu projektovej faktúry</span><span class="sxs-lookup"><span data-stu-id="ea1cd-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="ea1cd-113">Ak chcete vypnúť funkciu vylepšenia výkonu návrhu projektovej faktúry, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="ea1cd-114">Prejdite do ponuky **Správa funkcií** > **Všetky**.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="ea1cd-115">V zozname funkcií vyhľadajte **Zlepšenie výkonu návrhu projektových faktúr**.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="ea1cd-116">Vyberte položku **Zakázať**.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="ea1cd-117">Obnovte prehliadač.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="ea1cd-118">Výkonnosť návrhu faktúry nie je možné použiť, keď sú povolené fakturačné pravidlá.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="ea1cd-119">Počas dávkového procesu na vytvorenie návrhov faktúr počet čiastkových úloh rozdelí úlohy na maximálny počet na základe počtu zmlúv s fakturovateľnými transakciami bez ohľadu na to, čo ste zadali.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="ea1cd-120">Napríklad, ak zadáte **3** pre počet podúloh na hromadné vytvorenie návrhu faktúry a existujú iba dve zmluvy s fakturovateľnými transakciami, sú vytvorené iba dve podúlohy.</span><span class="sxs-lookup"><span data-stu-id="ea1cd-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
