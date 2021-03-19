---
title: Informácie o inovácii o štruktúre rozdelenia práce
description: Táto téma poskytuje informácie o inovácii štruktúry rozdelenia práce z programu Project Service Automation 2.x na 3.x.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a067521410f0fe0d8f5d4c510a35f2a3b018dce3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281767"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="754a3-103">Informácie o inovácii o štruktúre rozdelenia práce</span><span class="sxs-lookup"><span data-stu-id="754a3-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="754a3-104">Táto téma poskytuje informácie o inovácii štruktúry rozdelenia práce z programu Project Service Automation 2.x na 3.x.</span><span class="sxs-lookup"><span data-stu-id="754a3-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="754a3-105">Táto téma definuje dobrý stav projektu v Project Service Automation (PSA), ktorý je potrebný pre úspešnú inováciu.</span><span class="sxs-lookup"><span data-stu-id="754a3-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="754a3-106">Je tam tiež informácia o bežných podmienkach blokovania, ktoré budú po inovácii neúspešné.</span><span class="sxs-lookup"><span data-stu-id="754a3-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="754a3-107">Ďalšie informácie o definovaní projektových úloh a ich funkcií v rámci plánu projektu nájdete v časti [Projektové plány](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="754a3-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="754a3-108">Kľúčové entity</span><span class="sxs-lookup"><span data-stu-id="754a3-108">Key entities</span></span>
<span data-ttu-id="754a3-109">Pre presnú štruktúru rozdelenia práce, ktorá je už načítaná so zdrojmi, sa požadujú nasledujúce entity:</span><span class="sxs-lookup"><span data-stu-id="754a3-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="754a3-110">Projekt</span><span class="sxs-lookup"><span data-stu-id="754a3-110">Project</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="754a3-111">Projektový tím</span><span class="sxs-lookup"><span data-stu-id="754a3-111">Project Team</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="754a3-112">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="754a3-112">Project Task</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="754a3-113">Priradenia zdrojov</span><span class="sxs-lookup"><span data-stu-id="754a3-113">Resource Assignments</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="754a3-114">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="754a3-114">Project Task Dependency</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="754a3-115">Rezervovateľné zdroje</span><span class="sxs-lookup"><span data-stu-id="754a3-115">Bookable Resources</span></span>](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="754a3-116">Ak chcete definovať prostriedok načítaný štruktúrou rozdelenia práce, musíte vykonať nasledujúce kroky:</span><span class="sxs-lookup"><span data-stu-id="754a3-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="754a3-117">Vytvorte nový projekt.</span><span class="sxs-lookup"><span data-stu-id="754a3-117">Create a new project.</span></span> <span data-ttu-id="754a3-118">Ďalšie informácie o vytváraní nového projektu nájdete v časti [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="754a3-118">For more information about how to create a new project, see [msdyn_project](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="754a3-119">Vytvorte jednu alebo viac úloh.</span><span class="sxs-lookup"><span data-stu-id="754a3-119">Create one or more tasks.</span></span> <span data-ttu-id="754a3-120">Ďalšie informácie o vytváraní úlohy si prečítajte v časti [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="754a3-120">For more information about how to create a task, see [msdyn_projecttask](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="754a3-121">Definovanie závislostí úloh.</span><span class="sxs-lookup"><span data-stu-id="754a3-121">Define the task dependencies.</span></span> <span data-ttu-id="754a3-122">Viac informácií nájdete v časti [Závislosť projektovej úlohy](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="754a3-122">For more information, see [Project Task Dependency](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="754a3-123">Priraďte členom projektového tímu projekt.</span><span class="sxs-lookup"><span data-stu-id="754a3-123">Assign project team members to the project.</span></span> <span data-ttu-id="754a3-124">Ďalšie informácie nájdete v dokumente [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="754a3-124">For more information, see [msdyn_projectteam](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="754a3-125">Priraďte členov projektového tímu k úlohám.</span><span class="sxs-lookup"><span data-stu-id="754a3-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="754a3-126">Ďalšie informácie nájdete v dokumente [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="754a3-126">For more information, see [msdyn_resourceassignment](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="754a3-127">Vzťahy projektového tímu</span><span class="sxs-lookup"><span data-stu-id="754a3-127">Project team relationships</span></span>

<span data-ttu-id="754a3-128">Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:</span><span class="sxs-lookup"><span data-stu-id="754a3-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="754a3-129">Všetci členovia projektového tímu musia byť spájaní s rezervovateľnými zdrojmi.</span><span class="sxs-lookup"><span data-stu-id="754a3-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="754a3-130">Všetci členovia projektového tímu musia byť spájaní s rovnakým projektom.</span><span class="sxs-lookup"><span data-stu-id="754a3-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="754a3-131">Vzťahy projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="754a3-131">Project task relationships</span></span>
<span data-ttu-id="754a3-132">Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:</span><span class="sxs-lookup"><span data-stu-id="754a3-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="754a3-133">Všetky súvisiace úlohy musia byť priradené k rovnakému projektu.</span><span class="sxs-lookup"><span data-stu-id="754a3-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="754a3-134">Každá riadna úloha musí mať nadradenú úlohu.</span><span class="sxs-lookup"><span data-stu-id="754a3-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="754a3-135">Každá riadna úloha musí mať nadradený projekt.</span><span class="sxs-lookup"><span data-stu-id="754a3-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="754a3-136">Platné podmienky</span><span class="sxs-lookup"><span data-stu-id="754a3-136">Valid conditions</span></span>

- <span data-ttu-id="754a3-137">Všetky trvania úloh musí byť väčšie alebo rovné (>=) jednej hodiny a menej ako 1 800 000 minút (1 250 dní).\*</span><span class="sxs-lookup"><span data-stu-id="754a3-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="754a3-138">Všetky úlohy musia mať počiatočný dátum nie skôr ako 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="754a3-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="754a3-139">Všetky úlohy musia mať počiatočný dátum najneskôr 17 rokov od dnešného dňa.\*</span><span class="sxs-lookup"><span data-stu-id="754a3-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="754a3-140">Všetky úlohy musia mať počiatočný dátum skorší alebo rovný dátumu dokončenia.</span><span class="sxs-lookup"><span data-stu-id="754a3-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="754a3-141">Všetky typy klasifikácie (náklady, materiál, daň a čas) musia mať hodnoty pre **predvolenú jednotku** a **jednotkovú skupinu**.</span><span class="sxs-lookup"><span data-stu-id="754a3-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="754a3-142">Malo by sa vyhýbať formátom dátumov s písmenami.</span><span class="sxs-lookup"><span data-stu-id="754a3-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="754a3-143">Potenciálny postup zmiernenia</span><span class="sxs-lookup"><span data-stu-id="754a3-143">Potential mitigation steps</span></span>
- <span data-ttu-id="754a3-144">Pomocou rozšíreného vyhľadávania môžete identifikovať úlohy projektu, ktoré neobsahujú ID projektu.</span><span class="sxs-lookup"><span data-stu-id="754a3-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="754a3-145">Pomocou rozšíreného vyhľadávania môžete identifikovať úlohy projektu, pri ktorých je plánované trvanie väčšie ako 1 800 000.</span><span class="sxs-lookup"><span data-stu-id="754a3-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="754a3-146">Pred vykonaním akýchkoľvek zmien údajov by ste mali preskúmať všetky prispôsobenia spojené s entitou, ktoré mohli viesť k uvedeniu údajov do nesprávneho stavu.</span><span class="sxs-lookup"><span data-stu-id="754a3-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="754a3-147">Tieto prispôsobenia by sa mali vyriešiť pred pokračovaním akýchkoľvek aktualizácií týkajúcich sa údajov.</span><span class="sxs-lookup"><span data-stu-id="754a3-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="754a3-148">V prípade identifikovaných úloh, ktoré boli osamotené, zvážte odstránenie týchto úloh, ak nie sú potrebné alebo ak by sa mali spojiť so správnym nadradeným projektom.</span><span class="sxs-lookup"><span data-stu-id="754a3-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="754a3-149">V prípade akýchkoľvek úloh, ktorých trvanie je dlhšie ako 1 250 dní, zvážte pridanie viacerých úloh, ktoré predstavujú celkové trvanie, ak je to možné.</span><span class="sxs-lookup"><span data-stu-id="754a3-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="754a3-150">Položky označené hviezdičkou (\*) majú limity, ktoré sú spôsobené tým, že riadenie vzťahov so zákazníkmi (CRM) podporuje iba 7 320 rozšírení opakovania.</span><span class="sxs-lookup"><span data-stu-id="754a3-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="754a3-151">Musíte zostať pod týmto limitom.</span><span class="sxs-lookup"><span data-stu-id="754a3-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="754a3-152">Vzťahy priradenia zdrojov</span><span class="sxs-lookup"><span data-stu-id="754a3-152">Resource Assignment relationships</span></span>
<span data-ttu-id="754a3-153">Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:</span><span class="sxs-lookup"><span data-stu-id="754a3-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="754a3-154">Všetky priradenia zdrojov v štruktúre rozdelenia práce musia súvisieť s tým istým projektom.</span><span class="sxs-lookup"><span data-stu-id="754a3-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="754a3-155">Všetky priradenia zdrojov v štruktúre rozdelenia práce musia byť priradené k členom projektového tímu v rovnakom projekte.</span><span class="sxs-lookup"><span data-stu-id="754a3-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="754a3-156">Potenciálny postup zmiernenia</span><span class="sxs-lookup"><span data-stu-id="754a3-156">Potential mitigation steps</span></span>
- <span data-ttu-id="754a3-157">Identifikujte všetky úlohy, ktoré nespĺňajú vyššie uvedené podmienky.</span><span class="sxs-lookup"><span data-stu-id="754a3-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="754a3-158">Všetky priradenia zdrojov, ktoré už nie sú platné, by sa mali odstrániť.</span><span class="sxs-lookup"><span data-stu-id="754a3-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="754a3-159">Vzťahy závislosti projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="754a3-159">Project task dependency relationships</span></span>
<span data-ttu-id="754a3-160">Ak chcete zabezpečiť úspešnú inováciu, musia byť správne udržiavané nasledujúce vzťahy:</span><span class="sxs-lookup"><span data-stu-id="754a3-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="754a3-161">Všetky závislosti projektových úloh musia súvisieť s rovnakým projektom.</span><span class="sxs-lookup"><span data-stu-id="754a3-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="754a3-162">Úloha nemôže mať rovnakú závislosť odkazovanú viackrát.</span><span class="sxs-lookup"><span data-stu-id="754a3-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]