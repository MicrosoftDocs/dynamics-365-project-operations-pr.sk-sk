---
title: Režimy plánovania
description: Táto téma poskytuje informácie o režimoch plánovania.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116726"
---
# <a name="scheduling-modes"></a><span data-ttu-id="c8402-103">Režimy plánovania</span><span class="sxs-lookup"><span data-stu-id="c8402-103">Scheduling modes</span></span>

<span data-ttu-id="c8402-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="c8402-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c8402-105">Dynamics 365 Project Operations poskytuje organizáciám možnosť definovať, ako riadia zmeny kľúčových premenných v úlohách v rámci štruktúry rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="c8402-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="c8402-106">Na základe konkrétnych potrieb organizácie môžu projektoví manažéri po vytvorení projektu vykonať zmeny v režime plánovania.</span><span class="sxs-lookup"><span data-stu-id="c8402-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="c8402-107">V Project Operations sú k dispozícii tri režimy plánovania:</span><span class="sxs-lookup"><span data-stu-id="c8402-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="c8402-108">Pevné trvanie (toto je predvolený režim)</span><span class="sxs-lookup"><span data-stu-id="c8402-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="c8402-109">Fixné úsilie (*Práca*)</span><span class="sxs-lookup"><span data-stu-id="c8402-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="c8402-110">Pevné jednotky</span><span class="sxs-lookup"><span data-stu-id="c8402-110">Fixed units</span></span>

<span data-ttu-id="c8402-111">Hodnoty ovplyvnené definíciou konkrétneho režimu plánovania sú určené nasledujúcim vzorcom:</span><span class="sxs-lookup"><span data-stu-id="c8402-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="c8402-112">Úsilie = Trvanie x Jednotky</span><span class="sxs-lookup"><span data-stu-id="c8402-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="c8402-113">Keď definujete režim plánovania projektu, nastavujete jednu z týchto hodnôt, ktorú potom nemožno zmeniť.</span><span class="sxs-lookup"><span data-stu-id="c8402-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="c8402-114">Udržiavanie tejto hodnoty ako konštanty dáva tejto hodnote prioritu, ktorá upozorní systém, aby ju nezmenil, keď sa zmenia ďalšie dve hodnoty.</span><span class="sxs-lookup"><span data-stu-id="c8402-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="c8402-115">Nasledujúca tabuľka poskytuje informácie o vplyvoch výberu konkrétneho režimu.</span><span class="sxs-lookup"><span data-stu-id="c8402-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="c8402-116">**V tejto úlohe**</span><span class="sxs-lookup"><span data-stu-id="c8402-116">**In this task**</span></span>             | <span data-ttu-id="c8402-117">**Ak revidujete jednotky**</span><span class="sxs-lookup"><span data-stu-id="c8402-117">**If you revise units**</span></span>   | <span data-ttu-id="c8402-118">**Ak revidujete trvanie**</span><span class="sxs-lookup"><span data-stu-id="c8402-118">**If you revise duration**</span></span> | <span data-ttu-id="c8402-119">**Ak revidujete úsilie**</span><span class="sxs-lookup"><span data-stu-id="c8402-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="c8402-120">Úloha Pevné jednotky</span><span class="sxs-lookup"><span data-stu-id="c8402-120">Fixed units task</span></span>     | <span data-ttu-id="c8402-121">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="c8402-121">Duration is recalculated.</span></span> | <span data-ttu-id="c8402-122">Prepočíta sa úsilie.</span><span class="sxs-lookup"><span data-stu-id="c8402-122">Effort is recalculated.</span></span>    | <span data-ttu-id="c8402-123">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="c8402-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="c8402-124">Úloha Pevné úsilie</span><span class="sxs-lookup"><span data-stu-id="c8402-124">Fixed effort task</span></span>    | <span data-ttu-id="c8402-125">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="c8402-125">Duration is recalculated.</span></span> | <span data-ttu-id="c8402-126">Prepočítajú sa jednotky.</span><span class="sxs-lookup"><span data-stu-id="c8402-126">Units are recalculated.</span></span>    | <span data-ttu-id="c8402-127">Prepočíta sa trvanie.</span><span class="sxs-lookup"><span data-stu-id="c8402-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="c8402-128">Úloha Pevné trvanie</span><span class="sxs-lookup"><span data-stu-id="c8402-128">Fixed duration task</span></span>  | <span data-ttu-id="c8402-129">Prepočíta sa úsilie.</span><span class="sxs-lookup"><span data-stu-id="c8402-129">Effort is recalculated.</span></span>   | <span data-ttu-id="c8402-130">Prepočíta sa úsilie.</span><span class="sxs-lookup"><span data-stu-id="c8402-130">Effort is recalculated.</span></span>    | <span data-ttu-id="c8402-131">Prepočítajú sa jednotky.</span><span class="sxs-lookup"><span data-stu-id="c8402-131">Units are recalculated.</span></span>   |

<span data-ttu-id="c8402-132">Ďalšie informácie o vplyvoch daného režimu nájdete v časti [Zmena typu úlohy a spresnenie plánovania](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="c8402-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="c8402-133">V téme sa termín **Práca** používa namiesto termínu **Úsilie**.</span><span class="sxs-lookup"><span data-stu-id="c8402-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="c8402-134">Zmeňte režim plánovania organizácie</span><span class="sxs-lookup"><span data-stu-id="c8402-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="c8402-135">Vykonaním nasledujúcich krokov definujete režim plánovania organizácie.</span><span class="sxs-lookup"><span data-stu-id="c8402-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="c8402-136">Prejdite na **Nastavenia** \> **Všeobecné** \> **Parametre** a potom vyberte parameter projektu.</span><span class="sxs-lookup"><span data-stu-id="c8402-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="c8402-137">Na stránke **Parametre projektu** vyberte predvolený režim plánovania pre organizáciu a potom definujte schopnosť projektového manažéra prepísať nastavenie pri vytváraní nového projektu.</span><span class="sxs-lookup"><span data-stu-id="c8402-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="c8402-138">Zmeňte nastavenie režimu plánovania na projekte</span><span class="sxs-lookup"><span data-stu-id="c8402-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="c8402-139">Ak organizácia umožňuje projektovému manažérovi prepísať predvolený režim plánovania, môže projektový manažér vykonať túto zmenu pri vytváraní nového projektu.</span><span class="sxs-lookup"><span data-stu-id="c8402-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="c8402-140">Po uložení projektu sa však režim plánovania nedá zmeniť.</span><span class="sxs-lookup"><span data-stu-id="c8402-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="c8402-141">Skopírované projekty</span><span class="sxs-lookup"><span data-stu-id="c8402-141">Copied projects</span></span>

<span data-ttu-id="c8402-142">Pretože sa projekt vytvorí, keď sa vykoná akcia kopírovania projektu, správca projektu nemôže nastaviť režim plánovania.</span><span class="sxs-lookup"><span data-stu-id="c8402-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="c8402-143">Cieľový projekt bude vždy predvolený do režimu definovaného na úrovni organizácie.</span><span class="sxs-lookup"><span data-stu-id="c8402-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="c8402-144">Skopírované úlohy</span><span class="sxs-lookup"><span data-stu-id="c8402-144">Copied tasks</span></span>

<span data-ttu-id="c8402-145">Keď sa úloha skopíruje z jedného projektu do druhého, dedí úlohu v režime plánovania cieľového projektu.</span><span class="sxs-lookup"><span data-stu-id="c8402-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
