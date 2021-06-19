---
title: Kopírovanie projektu
description: Táto téma poskytuje informácie o kopírovaní projektov v aplikácii Dynamics 365 Project Operations.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091273"
---
# <a name="copy-a-project"></a><span data-ttu-id="e5daf-103">Kopírovanie projektu</span><span class="sxs-lookup"><span data-stu-id="e5daf-103">Copy a project</span></span>

<span data-ttu-id="e5daf-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="e5daf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5daf-105">S aplikáciou Dynamics 365 Project Operations môžete rýchlo vytvárať nové projekty pomocou výberu možnosti **Kopírovať projekt** na formulári **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="e5daf-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="e5daf-106">Ak chcete skopírovať projekt, otvorte projekt, ktorý chcete skopírovať, a potom vyberte **Kopírovať projekt**.</span><span class="sxs-lookup"><span data-stu-id="e5daf-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="e5daf-107">Touto akciou sa skopíruje nasledovné:</span><span class="sxs-lookup"><span data-stu-id="e5daf-107">The action will copy the following:</span></span>

- <span data-ttu-id="e5daf-108">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="e5daf-108">Project properties</span></span> 
- <span data-ttu-id="e5daf-109">Štruktúra rozdelenia práce</span><span class="sxs-lookup"><span data-stu-id="e5daf-109">Work breakdown structure</span></span>
- <span data-ttu-id="e5daf-110">Členovia projektového tímu</span><span class="sxs-lookup"><span data-stu-id="e5daf-110">Project team members</span></span>
- <span data-ttu-id="e5daf-111">Odhady projektu</span><span class="sxs-lookup"><span data-stu-id="e5daf-111">Project estimates</span></span>
- <span data-ttu-id="e5daf-112">Odhady projektových výdavkov</span><span class="sxs-lookup"><span data-stu-id="e5daf-112">Project expense estimates</span></span>
- <span data-ttu-id="e5daf-113">Odhady materiálov projektu</span><span class="sxs-lookup"><span data-stu-id="e5daf-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="e5daf-114">Vlastnosti projektu</span><span class="sxs-lookup"><span data-stu-id="e5daf-114">Project properties</span></span>

<span data-ttu-id="e5daf-115">Pri kopírovaní projektu sa skopírujú hodnoty v nasledujúcich poliach:</span><span class="sxs-lookup"><span data-stu-id="e5daf-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="e5daf-116">Meno</span><span class="sxs-lookup"><span data-stu-id="e5daf-116">Name</span></span>
- <span data-ttu-id="e5daf-117">Popis</span><span class="sxs-lookup"><span data-stu-id="e5daf-117">Description</span></span>
- <span data-ttu-id="e5daf-118">Zákazník</span><span class="sxs-lookup"><span data-stu-id="e5daf-118">Customer</span></span>
- <span data-ttu-id="e5daf-119">Šablóna kalendára</span><span class="sxs-lookup"><span data-stu-id="e5daf-119">Calendar Template</span></span>
- <span data-ttu-id="e5daf-120">Mena</span><span class="sxs-lookup"><span data-stu-id="e5daf-120">Currency</span></span>
- <span data-ttu-id="e5daf-121">Zmluvná jednotka</span><span class="sxs-lookup"><span data-stu-id="e5daf-121">Contracting Unit</span></span>
- <span data-ttu-id="e5daf-122">Projektový manažér</span><span class="sxs-lookup"><span data-stu-id="e5daf-122">Project Manager</span></span>
- <span data-ttu-id="e5daf-123">Status</span><span class="sxs-lookup"><span data-stu-id="e5daf-123">Status</span></span>
- <span data-ttu-id="e5daf-124">Celkový stav projektu</span><span class="sxs-lookup"><span data-stu-id="e5daf-124">Overall Project Status</span></span>
- <span data-ttu-id="e5daf-125">Vytvoril</span><span class="sxs-lookup"><span data-stu-id="e5daf-125">Comments</span></span>
- <span data-ttu-id="e5daf-126">Odhady</span><span class="sxs-lookup"><span data-stu-id="e5daf-126">Estimates</span></span>
- <span data-ttu-id="e5daf-127">Odhadovaný dátum začiatku: Toto je dátum vytvorenia projektu z kópie.</span><span class="sxs-lookup"><span data-stu-id="e5daf-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="e5daf-128">Odhadovaný dátum konca: Tento dátum je prispôsobený na základe dátumu začiatku nového projektu, ktorý bol vytvorený z kópie.</span><span class="sxs-lookup"><span data-stu-id="e5daf-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="e5daf-129">Úsilie (hodiny)</span><span class="sxs-lookup"><span data-stu-id="e5daf-129">Effort (Hours)</span></span>
- <span data-ttu-id="e5daf-130">Odhadované mzdové náklady</span><span class="sxs-lookup"><span data-stu-id="e5daf-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="e5daf-131">Odhadované výdavkové náklady</span><span class="sxs-lookup"><span data-stu-id="e5daf-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="e5daf-132">Odhadované materiálové náklady</span><span class="sxs-lookup"><span data-stu-id="e5daf-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="e5daf-133">Kopírovanie projektu je dlhodobá operácia.</span><span class="sxs-lookup"><span data-stu-id="e5daf-133">Copy project is a long running operation.</span></span> <span data-ttu-id="e5daf-134">Skopírujú sa tiež záznamy projektu, ich príslušné atribúty a veľa súvisiacich entít.</span><span class="sxs-lookup"><span data-stu-id="e5daf-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="e5daf-135">Z dôvodu dlhodobého charakteru operácie sa po spustení kopírovania uzamkne cieľová stránka projektu na účely vykonávania úprav, kým nebude kopírovanie dokončené.</span><span class="sxs-lookup"><span data-stu-id="e5daf-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="e5daf-136">Štruktúra rozdelenia práce</span><span class="sxs-lookup"><span data-stu-id="e5daf-136">Work breakdown structure</span></span>

<span data-ttu-id="e5daf-137">Pri kopírovaní projektu sa skopíruje celá štruktúra rozdelenia práce načítaná zdrojom.</span><span class="sxs-lookup"><span data-stu-id="e5daf-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="e5daf-138">Pomenované zdroje sa nahradia všeobecnými zdrojmi.</span><span class="sxs-lookup"><span data-stu-id="e5daf-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="e5daf-139">Ak pomenované zdroje nemajú rovnaký pracovný čas ako všeobecný zdroj, plán sa prepočíta a trvanie úlohy sa môže zmeniť.</span><span class="sxs-lookup"><span data-stu-id="e5daf-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="e5daf-140">Členovia projektového tímu</span><span class="sxs-lookup"><span data-stu-id="e5daf-140">Project team members</span></span>

<span data-ttu-id="e5daf-141">Keď sa projektový tím skopíruje zo zdrojového projektu, skopírujú sa všeobecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="e5daf-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="e5daf-142">Priradenie všeobecných zdrojov sa zachová rovnaké ako bolo pri zdrojovom projekte.</span><span class="sxs-lookup"><span data-stu-id="e5daf-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="e5daf-143">Pomenované zdroje sa prevedú na všeobecných členov tímu.</span><span class="sxs-lookup"><span data-stu-id="e5daf-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="e5daf-144">Odhady</span><span class="sxs-lookup"><span data-stu-id="e5daf-144">Estimates</span></span>

<span data-ttu-id="e5daf-145">Pri skopírovaní projektu sa zo zdrojového projektu skopírujú riadky s odhadmi zdrojov, výdavkov a materiálov.</span><span class="sxs-lookup"><span data-stu-id="e5daf-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="e5daf-146">Informácie o tom, ako programovo získať prístup k možnosti kopírovania projektu nájdete v časti [Vytvorenie šablóny projektu pomocou kopírovania projektu](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="e5daf-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
