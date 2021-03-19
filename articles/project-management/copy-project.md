---
title: Kopírovanie projektu
description: Táto téma poskytuje informácie o kopírovaní projektov v aplikácii Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 02/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: af1942e81691d9e13fdcbbf68599c1a8a4004582
ms.sourcegitcommit: 24528bb9c0ef8898077cb3bc672daa211c0e73aa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5479538"
---
# <a name="copy-a-project"></a><span data-ttu-id="2bf2b-103">Kopírovanie projektu</span><span class="sxs-lookup"><span data-stu-id="2bf2b-103">Copy a project</span></span>

<span data-ttu-id="2bf2b-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="2bf2b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2bf2b-105">S aplikáciou Dynamics 365 Project Operations môžete rýchlo vytvárať nové projekty pomocou výberu možnosti **Kopírovať projekt** na formulári **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="2bf2b-106">Ak chcete skopírovať projekt, otvorte projekt, ktorý chcete skopírovať, a potom vyberte **Kopírovať projekt**.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="2bf2b-107">Vykonaním akcie sa skopíruje:</span><span class="sxs-lookup"><span data-stu-id="2bf2b-107">The action will copy:</span></span>

- <span data-ttu-id="2bf2b-108">Vlastnosti projektu (odhadovaný dátum začatia sa skopíruje zo zdrojového projektu)</span><span class="sxs-lookup"><span data-stu-id="2bf2b-108">Project properties (The estimated start date is copied from the source project)</span></span>
- <span data-ttu-id="2bf2b-109">Štruktúra rozdelenia práce</span><span class="sxs-lookup"><span data-stu-id="2bf2b-109">The Work breakdown structure</span></span>
- <span data-ttu-id="2bf2b-110">Členovia projektového tímu</span><span class="sxs-lookup"><span data-stu-id="2bf2b-110">Project team members</span></span>
- <span data-ttu-id="2bf2b-111">Odhady projektu</span><span class="sxs-lookup"><span data-stu-id="2bf2b-111">Project estimates</span></span>
- <span data-ttu-id="2bf2b-112">Odhady projektových výdavkov</span><span class="sxs-lookup"><span data-stu-id="2bf2b-112">Project expense estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="2bf2b-113">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="2bf2b-113">Project properties</span></span>

<span data-ttu-id="2bf2b-114">Pri kopírovaní projektu sa skopírujú hodnoty v nasledujúcich poliach:</span><span class="sxs-lookup"><span data-stu-id="2bf2b-114">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="2bf2b-115">Meno</span><span class="sxs-lookup"><span data-stu-id="2bf2b-115">Name</span></span>
- <span data-ttu-id="2bf2b-116">Popis</span><span class="sxs-lookup"><span data-stu-id="2bf2b-116">Description</span></span>
- <span data-ttu-id="2bf2b-117">Zákazník</span><span class="sxs-lookup"><span data-stu-id="2bf2b-117">Customer</span></span>
- <span data-ttu-id="2bf2b-118">Šablóna kalendára</span><span class="sxs-lookup"><span data-stu-id="2bf2b-118">Calendar Template</span></span>
- <span data-ttu-id="2bf2b-119">Mena</span><span class="sxs-lookup"><span data-stu-id="2bf2b-119">Currency</span></span>
- <span data-ttu-id="2bf2b-120">Zmluvná jednotka</span><span class="sxs-lookup"><span data-stu-id="2bf2b-120">Contracting Unit</span></span>
- <span data-ttu-id="2bf2b-121">Projektový manažér</span><span class="sxs-lookup"><span data-stu-id="2bf2b-121">Project Manager</span></span>
- <span data-ttu-id="2bf2b-122">Status</span><span class="sxs-lookup"><span data-stu-id="2bf2b-122">Status</span></span>
- <span data-ttu-id="2bf2b-123">Celkový stav projektu</span><span class="sxs-lookup"><span data-stu-id="2bf2b-123">Overall Project Status</span></span>
- <span data-ttu-id="2bf2b-124">Vytvoril</span><span class="sxs-lookup"><span data-stu-id="2bf2b-124">Comments</span></span>
- <span data-ttu-id="2bf2b-125">Odhady</span><span class="sxs-lookup"><span data-stu-id="2bf2b-125">Estimates</span></span>
- <span data-ttu-id="2bf2b-126">Odhadovaný dátum začatia</span><span class="sxs-lookup"><span data-stu-id="2bf2b-126">Estimated Start Date</span></span>
- <span data-ttu-id="2bf2b-127">Dátum dokončenia</span><span class="sxs-lookup"><span data-stu-id="2bf2b-127">Finish Date</span></span>
- <span data-ttu-id="2bf2b-128">Úsilie (hodiny)</span><span class="sxs-lookup"><span data-stu-id="2bf2b-128">Effort (Hours)</span></span>
- <span data-ttu-id="2bf2b-129">Odhadované mzdové náklady</span><span class="sxs-lookup"><span data-stu-id="2bf2b-129">Estimated Labor Cost</span></span>
- <span data-ttu-id="2bf2b-130">Odhadované výdavkové náklady</span><span class="sxs-lookup"><span data-stu-id="2bf2b-130">Estimated Expense Cost</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="2bf2b-131">Štruktúra rozdelenia práce</span><span class="sxs-lookup"><span data-stu-id="2bf2b-131">Work breakdown structure</span></span>

<span data-ttu-id="2bf2b-132">Pri kopírovaní projektu sa skopíruje celá štruktúra rozdelenia práce načítaná zdrojom.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-132">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="2bf2b-133">Pomenované zdroje sa nahradia všeobecnými zdrojmi.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-133">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="2bf2b-134">Ak pomenované zdroje nemajú rovnaký pracovný čas ako všeobecný zdroj, plán sa prepočíta a trvanie úlohy sa môže zmeniť.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-134">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="2bf2b-135">Členovia projektového tímu</span><span class="sxs-lookup"><span data-stu-id="2bf2b-135">Project team members</span></span>

<span data-ttu-id="2bf2b-136">Keď sa projektový tím skopíruje zo zdrojového projektu, skopírujú sa všeobecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-136">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="2bf2b-137">Priradenie všeobecných zdrojov sa zachová rovnaké ako bolo pri zdrojovom projekte.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-137">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="2bf2b-138">Pomenované zdroje sa prevedú na všeobecných členov tímu.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-138">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="2bf2b-139">Odhady</span><span class="sxs-lookup"><span data-stu-id="2bf2b-139">Estimates</span></span>

<span data-ttu-id="2bf2b-140">Pri kopírovaní projektu sa zo zdrojového projektu skopírujú riadky odhadu zdrojov a výdavkov.</span><span class="sxs-lookup"><span data-stu-id="2bf2b-140">When the project is copied, both resource and expense estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="2bf2b-141">Informácie o tom, ako programovo získať prístup k možnosti kopírovania projektu nájdete v časti [Vytvorenie šablóny projektu pomocou kopírovania projektu](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="2bf2b-141">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
