---
title: Režimy plánovania
description: Táto téma poskytuje informácie o režimoch plánovania.
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981454"
---
# <a name="scheduling-modes"></a><span data-ttu-id="0d652-103">Režimy plánovania</span><span class="sxs-lookup"><span data-stu-id="0d652-103">Scheduling modes</span></span>

<span data-ttu-id="0d652-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="0d652-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="0d652-105">Dynamics 365 Project Operations poskytuje organizáciám možnosť definovať, ako riadia zmeny kľúčových premenných v úlohách v rámci štruktúry rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="0d652-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="0d652-106">Na základe konkrétnych potrieb organizácie môžu projektoví manažéri po vytvorení projektu vykonať zmeny v režime plánovania.</span><span class="sxs-lookup"><span data-stu-id="0d652-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="0d652-107">V Project Operations sú k dispozícii tri režimy plánovania:</span><span class="sxs-lookup"><span data-stu-id="0d652-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="0d652-108">Pevné trvanie (toto je predvolený režim)</span><span class="sxs-lookup"><span data-stu-id="0d652-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="0d652-109">Pevná práca</span><span class="sxs-lookup"><span data-stu-id="0d652-109">Fixed work</span></span>
  - <span data-ttu-id="0d652-110">Pevné jednotky</span><span class="sxs-lookup"><span data-stu-id="0d652-110">Fixed units</span></span>

<span data-ttu-id="0d652-111">Hodnoty ovplyvnené definíciou konkrétneho režimu plánovania sú určené nasledujúcim vzorcom:</span><span class="sxs-lookup"><span data-stu-id="0d652-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="0d652-112">Úsilie (*Práca*) = Trvanie x Jednotky</span><span class="sxs-lookup"><span data-stu-id="0d652-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="0d652-113">Keď definujete režim plánovania projektu, nastavujete jednu z týchto hodnôt, ktorú potom nemožno zmeniť.</span><span class="sxs-lookup"><span data-stu-id="0d652-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="0d652-114">Udržiavanie tejto hodnoty ako konštanty dáva tejto hodnote prioritu, ktorá upozorní systém, aby ju nezmenil, keď sa zmenia ďalšie dve hodnoty.</span><span class="sxs-lookup"><span data-stu-id="0d652-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="0d652-115">Nasledujúca tabuľka poskytuje informácie o vplyvoch výberu konkrétneho režimu.</span><span class="sxs-lookup"><span data-stu-id="0d652-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="0d652-116">**V tejto úlohe**</span><span class="sxs-lookup"><span data-stu-id="0d652-116">**In this task**</span></span>             | <span data-ttu-id="0d652-117">**Ak revidujete jednotky**</span><span class="sxs-lookup"><span data-stu-id="0d652-117">**If you revise units**</span></span>   | <span data-ttu-id="0d652-118">**Ak revidujete trvanie**</span><span class="sxs-lookup"><span data-stu-id="0d652-118">**If you revise duration**</span></span> | <span data-ttu-id="0d652-119">**Ak revidujete úsilie**</span><span class="sxs-lookup"><span data-stu-id="0d652-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="0d652-120">Úloha Pevné jednotky</span><span class="sxs-lookup"><span data-stu-id="0d652-120">Fixed units task</span></span>     | <span data-ttu-id="0d652-121">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="0d652-121">Duration is recalculated.</span></span> | <span data-ttu-id="0d652-122">Prepočíta sa úsilie.</span><span class="sxs-lookup"><span data-stu-id="0d652-122">Effort is recalculated.</span></span>    | <span data-ttu-id="0d652-123">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="0d652-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="0d652-124">Úloha Pevné úsilie</span><span class="sxs-lookup"><span data-stu-id="0d652-124">Fixed effort task</span></span>    | <span data-ttu-id="0d652-125">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="0d652-125">Duration is recalculated.</span></span> | <span data-ttu-id="0d652-126">Prepočítajú sa jednotky.</span><span class="sxs-lookup"><span data-stu-id="0d652-126">Units are recalculated.</span></span>    | <span data-ttu-id="0d652-127">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="0d652-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="0d652-128">Úloha Pevné trvanie</span><span class="sxs-lookup"><span data-stu-id="0d652-128">Fixed duration task</span></span>  | <span data-ttu-id="0d652-129">Prepočíta sa úsilie.</span><span class="sxs-lookup"><span data-stu-id="0d652-129">Effort is recalculated.</span></span>   | <span data-ttu-id="0d652-130">Prepočíta sa úsilie.</span><span class="sxs-lookup"><span data-stu-id="0d652-130">Effort is recalculated.</span></span>    | <span data-ttu-id="0d652-131">Prepočítajú sa jednotky.</span><span class="sxs-lookup"><span data-stu-id="0d652-131">Units are recalculated.</span></span>   |

<span data-ttu-id="0d652-132">Ďalšie informácie o vplyvoch daného režimu nájdete v časti [Zmena typu úlohy a spresnenie plánovania](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="0d652-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="0d652-133">V téme sa termín **Práca** používa namiesto termínu **Úsilie**.</span><span class="sxs-lookup"><span data-stu-id="0d652-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="0d652-134">Zmeňte režim plánovania organizácie</span><span class="sxs-lookup"><span data-stu-id="0d652-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="0d652-135">Vykonaním nasledujúcich krokov definujete režim plánovania organizácie.</span><span class="sxs-lookup"><span data-stu-id="0d652-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="0d652-136">Prejdite na **Nastavenia** \> **Všeobecné** \> **Parametre** a potom vyberte parameter projektu.</span><span class="sxs-lookup"><span data-stu-id="0d652-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="0d652-137">Na stránke **Parametre projektu** vyberte predvolený režim plánovania pre organizáciu a potom definujte schopnosť projektového manažéra prepísať nastavenie pri vytváraní nového projektu.</span><span class="sxs-lookup"><span data-stu-id="0d652-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="0d652-138">Zmeňte nastavenie režimu plánovania na projekte</span><span class="sxs-lookup"><span data-stu-id="0d652-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="0d652-139">Ak organizácia umožňuje projektovému manažérovi prepísať predvolený režim plánovania, môže projektový manažér vykonať túto zmenu pri vytváraní nového projektu.</span><span class="sxs-lookup"><span data-stu-id="0d652-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="0d652-140">Po uložení projektu sa však režim plánovania nedá zmeniť.</span><span class="sxs-lookup"><span data-stu-id="0d652-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="0d652-141">Skopírované projekty</span><span class="sxs-lookup"><span data-stu-id="0d652-141">Copied projects</span></span>

<span data-ttu-id="0d652-142">Pretože sa projekt vytvorí, keď sa vykoná akcia kopírovania projektu, správca projektu nemôže nastaviť režim plánovania.</span><span class="sxs-lookup"><span data-stu-id="0d652-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="0d652-143">Cieľový projekt bude vždy predvolený do režimu definovaného na úrovni organizácie.</span><span class="sxs-lookup"><span data-stu-id="0d652-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="0d652-144">Skopírované úlohy</span><span class="sxs-lookup"><span data-stu-id="0d652-144">Copied tasks</span></span>

<span data-ttu-id="0d652-145">Keď sa úloha skopíruje z jedného projektu do druhého, dedí úlohu v režime plánovania cieľového projektu.</span><span class="sxs-lookup"><span data-stu-id="0d652-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
