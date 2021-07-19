---
title: Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu
description: Táto téma poskytuje informácie a ukážky použitia rozhraní API plánovania projektu.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4915261c08a3271a919e04084e92a14b297c1b35
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293246"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="d2b8d-103">Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d2b8d-103">Use Project schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="d2b8d-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="d2b8d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="d2b8d-105">Niektoré alebo všetky z funkcií uvádzaných v tejto téme sú k dispozícii ako súčasť vydania verzie Preview.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="d2b8d-106">Obsah a funkcie sa môžu zmeniť.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="d2b8d-107">Entity na plánovanie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-107">Scheduling entities</span></span>

<span data-ttu-id="d2b8d-108">Rozhrania API pre plánovanie projektu umožňujú vykonávať operácie vytvárania, aktualizácie a mazania pomocou **Entít plánovania**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-108">Project schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="d2b8d-109">Tieto entity sú spravované prostredníctvom modulu Plánovanie v Projekte pre web.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="d2b8d-110">Operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania** boli obmedzené v skorších vydaniach Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="d2b8d-111">Nasledujúca tabuľka poskytuje úplný zoznam entít plánovania projektu.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-111">The following table provides a full list of the Project schedule entities.</span></span>

| <span data-ttu-id="d2b8d-112">Názov entity</span><span class="sxs-lookup"><span data-stu-id="d2b8d-112">Entity name</span></span>  | <span data-ttu-id="d2b8d-113">Logický názov entity</span><span class="sxs-lookup"><span data-stu-id="d2b8d-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="d2b8d-114">Project</span><span class="sxs-lookup"><span data-stu-id="d2b8d-114">Project</span></span> | <span data-ttu-id="d2b8d-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="d2b8d-115">msdyn_project</span></span> |
| <span data-ttu-id="d2b8d-116">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="d2b8d-116">Project Task</span></span>  | <span data-ttu-id="d2b8d-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="d2b8d-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="d2b8d-118">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="d2b8d-118">Project Task Dependency</span></span>  | <span data-ttu-id="d2b8d-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="d2b8d-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="d2b8d-120">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="d2b8d-120">Resource Assignment</span></span> | <span data-ttu-id="d2b8d-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="d2b8d-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="d2b8d-122">Projektový kontajner</span><span class="sxs-lookup"><span data-stu-id="d2b8d-122">Project Bucket</span></span>  | <span data-ttu-id="d2b8d-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="d2b8d-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="d2b8d-124">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="d2b8d-124">Project Team Member</span></span> | <span data-ttu-id="d2b8d-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="d2b8d-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="d2b8d-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="d2b8d-126">OperationSet</span></span>

<span data-ttu-id="d2b8d-127">OperationSet je vzor jednotky práce, ktorý je možné použiť, keď sa v rámci transakcie musí spracovať niekoľko požiadaviek ovplyvňujúcich plán.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="project-schedule-apis"></a><span data-ttu-id="d2b8d-128">API plánovania projektu</span><span class="sxs-lookup"><span data-stu-id="d2b8d-128">Project schedule APIs</span></span>

<span data-ttu-id="d2b8d-129">Nasleduje zoznam aktuálnych rozhraní API plánovania projektu.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-129">The following is a list of current Project schedule APIs.</span></span>

- <span data-ttu-id="d2b8d-130">**msdyn_CreateProjectV1**: Toto rozhranie API možno použiť na vytvorenie projektu.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="d2b8d-131">Projekt a predvolený kontajner projektu sa vytvorí okamžite.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="d2b8d-132">**msdyn_CreateTeamMemberV1**: Toto rozhranie API možno použiť na vytvorenie člena projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="d2b8d-133">Záznam o členovi tímu sa vytvorí okamžite.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="d2b8d-134">**msdyn_CreateOperationSetV1**: Toto API možno použiť na naplánovanie niekoľkých požiadaviek, ktoré sa musia vykonať v rámci transakcie.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="d2b8d-135">**msdyn_PSSCreateV1**: Toto API možno použiť na vytvorenie entity.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="d2b8d-136">Entitou môže byť ktorákoľvek z entít plánovania projektu, ktoré podporujú operáciu vytvorenia.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-136">The entity can be any of the Project scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="d2b8d-137">**msdyn_PSSUpdateV1**: Toto API možno použiť na aktualizáciu entity.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="d2b8d-138">Entitou môže byť ktorákoľvek z entít plánovania projektu, ktoré podporujú operáciu aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-138">The entity can be any of the Project scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="d2b8d-139">**msdyn_PSSDeleteV1**: Toto API možno použiť na odstránenie entity.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="d2b8d-140">Entitou môže byť ktorákoľvek z entít plánovania projektu, ktoré podporujú operáciu vymazania.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-140">The entity can be any of the Project scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="d2b8d-141">**msdyn_ExecuteOperationSetV1**: Toto API sa používa na vykonávanie všetkých operácií v rámci danej množiny operácií.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-project-schedule-apis-with-operationset"></a><span data-ttu-id="d2b8d-142">Používanie rozhraní API pre plánovanie projektu s OperationSet</span><span class="sxs-lookup"><span data-stu-id="d2b8d-142">Using Project schedule APIs with OperationSet</span></span>

<span data-ttu-id="d2b8d-143">Pretože záznamy s **CreateProjectV1** a **CreateTeamMemberV1** sú vytvorené okamžite, tieto API nemôžu byť použité v **OperationSet** priamo.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="d2b8d-144">Môžete však použiť API na vytvorenie potrebných záznamov, vytvorenie **OperationSet** a potom použiť tieto vopred vytvorené záznamy v **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="d2b8d-145">Podporované operácie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-145">Supported operations</span></span>

| <span data-ttu-id="d2b8d-146">Entita na plánovanie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-146">Scheduling entity</span></span> | <span data-ttu-id="d2b8d-147">Vytvoriť</span><span class="sxs-lookup"><span data-stu-id="d2b8d-147">Create</span></span> | <span data-ttu-id="d2b8d-148">Aktualizácia</span><span class="sxs-lookup"><span data-stu-id="d2b8d-148">Update</span></span> | <span data-ttu-id="d2b8d-149">Delete</span><span class="sxs-lookup"><span data-stu-id="d2b8d-149">Delete</span></span> | <span data-ttu-id="d2b8d-150">Dôležité aspekty</span><span class="sxs-lookup"><span data-stu-id="d2b8d-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="d2b8d-151">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="d2b8d-151">Project task</span></span> | <span data-ttu-id="d2b8d-152">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-152">Yes</span></span> | <span data-ttu-id="d2b8d-153">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-153">Yes</span></span> | <span data-ttu-id="d2b8d-154">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-154">Yes</span></span> | <span data-ttu-id="d2b8d-155">Nie je</span><span class="sxs-lookup"><span data-stu-id="d2b8d-155">None</span></span> |
| <span data-ttu-id="d2b8d-156">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="d2b8d-156">Project task dependency</span></span> | <span data-ttu-id="d2b8d-157">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-157">Yes</span></span> | <span data-ttu-id="d2b8d-158">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-158">Yes</span></span> | | <span data-ttu-id="d2b8d-159">Záznamy o závislosti od projektových úloh sa neaktualizujú.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="d2b8d-160">Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d2b8d-161">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="d2b8d-161">Resource assignment</span></span> | <span data-ttu-id="d2b8d-162">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-162">Yes</span></span> | <span data-ttu-id="d2b8d-163">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-163">Yes</span></span> | | <span data-ttu-id="d2b8d-164">Operácie s nasledujúcimi poľami nie sú podporované: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="d2b8d-165">Záznamy o priradení zdrojov sa neaktualizujú.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="d2b8d-166">Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="d2b8d-167">Projektový kontajner</span><span class="sxs-lookup"><span data-stu-id="d2b8d-167">Project bucket</span></span> | <span data-ttu-id="d2b8d-168">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="d2b8d-168">N/A</span></span> | <span data-ttu-id="d2b8d-169">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="d2b8d-169">N/A</span></span> | <span data-ttu-id="d2b8d-170">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="d2b8d-170">N/A</span></span> | <span data-ttu-id="d2b8d-171">Predvolený kontajner sa vytvára pomocou API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="d2b8d-172">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="d2b8d-172">Project team member</span></span> | <span data-ttu-id="d2b8d-173">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-173">Yes</span></span> | <span data-ttu-id="d2b8d-174">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-174">Yes</span></span> | <span data-ttu-id="d2b8d-175">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-175">Yes</span></span> | <span data-ttu-id="d2b8d-176">Na operáciu vytvorenia použite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="d2b8d-177">Project</span><span class="sxs-lookup"><span data-stu-id="d2b8d-177">Project</span></span> | <span data-ttu-id="d2b8d-178">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-178">Yes</span></span> | <span data-ttu-id="d2b8d-179">Áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-179">Yes</span></span> | <span data-ttu-id="d2b8d-180">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="d2b8d-180">N/A</span></span> | <span data-ttu-id="d2b8d-181">Operácie s nasledujúcimi poľami nie sú podporované: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="d2b8d-182">Tieto rozhrania API je možné volať s objektmi entít, ktoré obsahujú vlastné polia.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="d2b8d-183">Toto ID vlastnosti je voliteľné.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-183">The ID property is optional.</span></span> <span data-ttu-id="d2b8d-184">Ak je uvedené, systém sa ho pokúsi použiť a v prípade, že ho nemožno použiť, vyvolá výnimku.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="d2b8d-185">Ak nie je uvedené, systém ho vygeneruje.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="d2b8d-186">Obmedzené polia</span><span class="sxs-lookup"><span data-stu-id="d2b8d-186">Restricted fields</span></span>

<span data-ttu-id="d2b8d-187">Nasledujúce tabuľky definujú polia, ktoré sú obmedzené v rámci možností **Vytvoriť** a **Upraviť**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="d2b8d-188">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="d2b8d-188">Project task</span></span>

| <span data-ttu-id="d2b8d-189">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-189">**Logical name**</span></span>                       | <span data-ttu-id="d2b8d-190">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-190">**Can create**</span></span> | <span data-ttu-id="d2b8d-191">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="d2b8d-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="d2b8d-193">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-193">no</span></span>             | <span data-ttu-id="d2b8d-194">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-194">no</span></span>               |
| <span data-ttu-id="d2b8d-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="d2b8d-196">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-196">no</span></span>             | <span data-ttu-id="d2b8d-197">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-197">no</span></span>               |
| <span data-ttu-id="d2b8d-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="d2b8d-198">msdyn_actualend</span></span>                        | <span data-ttu-id="d2b8d-199">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-199">no</span></span>             | <span data-ttu-id="d2b8d-200">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-200">no</span></span>               |
| <span data-ttu-id="d2b8d-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="d2b8d-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="d2b8d-202">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-202">no</span></span>             | <span data-ttu-id="d2b8d-203">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-203">no</span></span>               |
| <span data-ttu-id="d2b8d-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="d2b8d-205">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-205">no</span></span>             | <span data-ttu-id="d2b8d-206">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-206">no</span></span>               |
| <span data-ttu-id="d2b8d-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="d2b8d-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="d2b8d-208">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-208">no</span></span>             | <span data-ttu-id="d2b8d-209">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-209">no</span></span>               |
| <span data-ttu-id="d2b8d-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="d2b8d-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="d2b8d-211">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-211">no</span></span>             | <span data-ttu-id="d2b8d-212">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-212">no</span></span>               |
| <span data-ttu-id="d2b8d-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="d2b8d-214">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-214">no</span></span>             | <span data-ttu-id="d2b8d-215">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-215">no</span></span>               |
| <span data-ttu-id="d2b8d-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="d2b8d-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="d2b8d-217">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-217">no</span></span>             | <span data-ttu-id="d2b8d-218">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-218">no</span></span>               |
| <span data-ttu-id="d2b8d-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d2b8d-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="d2b8d-220">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-220">no</span></span>             | <span data-ttu-id="d2b8d-221">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-221">no</span></span>               |
| <span data-ttu-id="d2b8d-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d2b8d-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="d2b8d-223">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-223">no</span></span>             | <span data-ttu-id="d2b8d-224">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-224">no</span></span>               |
| <span data-ttu-id="d2b8d-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="d2b8d-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="d2b8d-226">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-226">no</span></span>             | <span data-ttu-id="d2b8d-227">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-227">no</span></span>               |
| <span data-ttu-id="d2b8d-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="d2b8d-229">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-229">no</span></span>             | <span data-ttu-id="d2b8d-230">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-230">no</span></span>               |
| <span data-ttu-id="d2b8d-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="d2b8d-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="d2b8d-232">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-232">no</span></span>             | <span data-ttu-id="d2b8d-233">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-233">no</span></span>               |
| <span data-ttu-id="d2b8d-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="d2b8d-235">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-235">no</span></span>             | <span data-ttu-id="d2b8d-236">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-236">no</span></span>               |
| <span data-ttu-id="d2b8d-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="d2b8d-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="d2b8d-238">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-238">no</span></span>             | <span data-ttu-id="d2b8d-239">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-239">no</span></span>               |
| <span data-ttu-id="d2b8d-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="d2b8d-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="d2b8d-241">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-241">no</span></span>             | <span data-ttu-id="d2b8d-242">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-242">no</span></span>               |
| <span data-ttu-id="d2b8d-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="d2b8d-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="d2b8d-244">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-244">no</span></span>             | <span data-ttu-id="d2b8d-245">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-245">no</span></span>               |
| <span data-ttu-id="d2b8d-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="d2b8d-247">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-247">no</span></span>             | <span data-ttu-id="d2b8d-248">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-248">no</span></span>               |
| <span data-ttu-id="d2b8d-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="d2b8d-250">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-250">no</span></span>             | <span data-ttu-id="d2b8d-251">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-251">no</span></span>               |
| <span data-ttu-id="d2b8d-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="d2b8d-253">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-253">no</span></span>             | <span data-ttu-id="d2b8d-254">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-254">no</span></span>               |
| <span data-ttu-id="d2b8d-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="d2b8d-256">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-256">no</span></span>             | <span data-ttu-id="d2b8d-257">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-257">no</span></span>               |
| <span data-ttu-id="d2b8d-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d2b8d-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="d2b8d-259">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-259">no</span></span>             | <span data-ttu-id="d2b8d-260">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-260">no</span></span>               |
| <span data-ttu-id="d2b8d-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="d2b8d-262">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-262">no</span></span>             | <span data-ttu-id="d2b8d-263">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-263">no</span></span>               |
| <span data-ttu-id="d2b8d-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="d2b8d-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="d2b8d-265">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-265">no</span></span>             | <span data-ttu-id="d2b8d-266">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-266">no</span></span>               |
| <span data-ttu-id="d2b8d-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="d2b8d-267">msdyn_progress</span></span>                         | <span data-ttu-id="d2b8d-268">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-268">no</span></span>             | <span data-ttu-id="d2b8d-269">nie (áno pre P4W)</span><span class="sxs-lookup"><span data-stu-id="d2b8d-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="d2b8d-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="d2b8d-271">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-271">no</span></span>             | <span data-ttu-id="d2b8d-272">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-272">no</span></span>               |
| <span data-ttu-id="d2b8d-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="d2b8d-274">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-274">no</span></span>             | <span data-ttu-id="d2b8d-275">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-275">no</span></span>               |
| <span data-ttu-id="d2b8d-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d2b8d-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="d2b8d-277">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-277">no</span></span>             | <span data-ttu-id="d2b8d-278">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-278">no</span></span>               |
| <span data-ttu-id="d2b8d-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="d2b8d-280">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-280">no</span></span>             | <span data-ttu-id="d2b8d-281">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-281">no</span></span>               |
| <span data-ttu-id="d2b8d-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="d2b8d-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="d2b8d-283">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-283">no</span></span>             | <span data-ttu-id="d2b8d-284">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-284">no</span></span>               |
| <span data-ttu-id="d2b8d-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="d2b8d-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="d2b8d-286">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-286">no</span></span>             | <span data-ttu-id="d2b8d-287">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-287">no</span></span>               |
| <span data-ttu-id="d2b8d-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="d2b8d-289">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-289">no</span></span>             | <span data-ttu-id="d2b8d-290">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-290">no</span></span>               |
| <span data-ttu-id="d2b8d-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="d2b8d-292">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-292">no</span></span>             | <span data-ttu-id="d2b8d-293">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-293">no</span></span>               |
| <span data-ttu-id="d2b8d-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="d2b8d-295">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-295">no</span></span>             | <span data-ttu-id="d2b8d-296">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-296">no</span></span>               |
| <span data-ttu-id="d2b8d-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="d2b8d-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="d2b8d-298">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-298">no</span></span>             | <span data-ttu-id="d2b8d-299">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-299">no</span></span>               |
| <span data-ttu-id="d2b8d-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d2b8d-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="d2b8d-301">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-301">no</span></span>             | <span data-ttu-id="d2b8d-302">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-302">no</span></span>               |
| <span data-ttu-id="d2b8d-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="d2b8d-304">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-304">no</span></span>             | <span data-ttu-id="d2b8d-305">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-305">no</span></span>               |
| <span data-ttu-id="d2b8d-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="d2b8d-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="d2b8d-307">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-307">no</span></span>             | <span data-ttu-id="d2b8d-308">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-308">no</span></span>               |
| <span data-ttu-id="d2b8d-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="d2b8d-310">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-310">no</span></span>             | <span data-ttu-id="d2b8d-311">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-311">no</span></span>               |
| <span data-ttu-id="d2b8d-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="d2b8d-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="d2b8d-313">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-313">no</span></span>             | <span data-ttu-id="d2b8d-314">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-314">no</span></span>               |
| <span data-ttu-id="d2b8d-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="d2b8d-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="d2b8d-316">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-316">no</span></span>             | <span data-ttu-id="d2b8d-317">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-317">no</span></span>               |
| <span data-ttu-id="d2b8d-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="d2b8d-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="d2b8d-319">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-319">no</span></span>             | <span data-ttu-id="d2b8d-320">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-320">no</span></span>               |
| <span data-ttu-id="d2b8d-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="d2b8d-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="d2b8d-322">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-322">no</span></span>             | <span data-ttu-id="d2b8d-323">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-323">no</span></span>               |
| <span data-ttu-id="d2b8d-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="d2b8d-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="d2b8d-325">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-325">no</span></span>             | <span data-ttu-id="d2b8d-326">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-326">no</span></span>               |
| <span data-ttu-id="d2b8d-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="d2b8d-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="d2b8d-328">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-328">no</span></span>             | <span data-ttu-id="d2b8d-329">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-329">no</span></span>               |
| <span data-ttu-id="d2b8d-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="d2b8d-330">msdyn_summary</span></span>                          | <span data-ttu-id="d2b8d-331">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-331">no</span></span>             | <span data-ttu-id="d2b8d-332">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-332">no</span></span>               |
| <span data-ttu-id="d2b8d-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="d2b8d-334">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-334">no</span></span>             | <span data-ttu-id="d2b8d-335">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-335">no</span></span>               |
| <span data-ttu-id="d2b8d-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="d2b8d-337">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-337">no</span></span>             | <span data-ttu-id="d2b8d-338">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="d2b8d-339">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="d2b8d-339">Project task dependency</span></span>

| <span data-ttu-id="d2b8d-340">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-340">**Logical name**</span></span>              | <span data-ttu-id="d2b8d-341">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-341">**Can create**</span></span> | <span data-ttu-id="d2b8d-342">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="d2b8d-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="d2b8d-343">msdyn_linktype</span></span>                | <span data-ttu-id="d2b8d-344">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-344">no</span></span>             | <span data-ttu-id="d2b8d-345">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-345">no</span></span>           |
| <span data-ttu-id="d2b8d-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="d2b8d-346">msdyn_linktypename</span></span>            | <span data-ttu-id="d2b8d-347">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-347">no</span></span>             | <span data-ttu-id="d2b8d-348">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-348">no</span></span>           |
| <span data-ttu-id="d2b8d-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="d2b8d-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="d2b8d-350">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-350">yes</span></span>            | <span data-ttu-id="d2b8d-351">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-351">no</span></span>           |
| <span data-ttu-id="d2b8d-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="d2b8d-353">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-353">yes</span></span>            | <span data-ttu-id="d2b8d-354">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-354">no</span></span>           |
| <span data-ttu-id="d2b8d-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="d2b8d-355">msdyn_project</span></span>                 | <span data-ttu-id="d2b8d-356">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-356">yes</span></span>            | <span data-ttu-id="d2b8d-357">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-357">no</span></span>           |
| <span data-ttu-id="d2b8d-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-358">msdyn_projectname</span></span>             | <span data-ttu-id="d2b8d-359">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-359">yes</span></span>            | <span data-ttu-id="d2b8d-360">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-360">no</span></span>           |
| <span data-ttu-id="d2b8d-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="d2b8d-362">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-362">yes</span></span>            | <span data-ttu-id="d2b8d-363">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-363">no</span></span>           |
| <span data-ttu-id="d2b8d-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="d2b8d-364">msdyn_successortask</span></span>           | <span data-ttu-id="d2b8d-365">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-365">yes</span></span>            | <span data-ttu-id="d2b8d-366">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-366">no</span></span>           |
| <span data-ttu-id="d2b8d-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="d2b8d-368">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-368">yes</span></span>            | <span data-ttu-id="d2b8d-369">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="d2b8d-370">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="d2b8d-370">Resource assignment</span></span>

| <span data-ttu-id="d2b8d-371">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-371">**Logical name**</span></span>             | <span data-ttu-id="d2b8d-372">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-372">**Can create**</span></span> | <span data-ttu-id="d2b8d-373">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="d2b8d-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="d2b8d-375">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-375">yes</span></span>            | <span data-ttu-id="d2b8d-376">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-376">no</span></span>           |
| <span data-ttu-id="d2b8d-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="d2b8d-378">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-378">yes</span></span>            | <span data-ttu-id="d2b8d-379">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-379">no</span></span>           |
| <span data-ttu-id="d2b8d-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="d2b8d-381">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-381">no</span></span>             | <span data-ttu-id="d2b8d-382">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-382">no</span></span>           |
| <span data-ttu-id="d2b8d-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="d2b8d-384">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-384">no</span></span>             | <span data-ttu-id="d2b8d-385">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-385">no</span></span>           |
| <span data-ttu-id="d2b8d-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="d2b8d-386">msdyn_committype</span></span>             | <span data-ttu-id="d2b8d-387">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-387">no</span></span>             | <span data-ttu-id="d2b8d-388">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-388">no</span></span>           |
| <span data-ttu-id="d2b8d-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="d2b8d-389">msdyn_committypename</span></span>         | <span data-ttu-id="d2b8d-390">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-390">no</span></span>             | <span data-ttu-id="d2b8d-391">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-391">no</span></span>           |
| <span data-ttu-id="d2b8d-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d2b8d-392">msdyn_effort</span></span>                 | <span data-ttu-id="d2b8d-393">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-393">no</span></span>             | <span data-ttu-id="d2b8d-394">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-394">no</span></span>           |
| <span data-ttu-id="d2b8d-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d2b8d-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="d2b8d-396">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-396">no</span></span>             | <span data-ttu-id="d2b8d-397">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-397">no</span></span>           |
| <span data-ttu-id="d2b8d-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d2b8d-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="d2b8d-399">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-399">no</span></span>             | <span data-ttu-id="d2b8d-400">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-400">no</span></span>           |
| <span data-ttu-id="d2b8d-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d2b8d-401">msdyn_finish</span></span>                 | <span data-ttu-id="d2b8d-402">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-402">no</span></span>             | <span data-ttu-id="d2b8d-403">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-403">no</span></span>           |
| <span data-ttu-id="d2b8d-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="d2b8d-405">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-405">no</span></span>             | <span data-ttu-id="d2b8d-406">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-406">no</span></span>           |
| <span data-ttu-id="d2b8d-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="d2b8d-408">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-408">no</span></span>             | <span data-ttu-id="d2b8d-409">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-409">no</span></span>           |
| <span data-ttu-id="d2b8d-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="d2b8d-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="d2b8d-411">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-411">no</span></span>             | <span data-ttu-id="d2b8d-412">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-412">no</span></span>           |
| <span data-ttu-id="d2b8d-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d2b8d-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="d2b8d-414">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-414">no</span></span>             | <span data-ttu-id="d2b8d-415">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-415">no</span></span>           |
| <span data-ttu-id="d2b8d-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="d2b8d-417">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-417">no</span></span>             | <span data-ttu-id="d2b8d-418">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-418">no</span></span>           |
| <span data-ttu-id="d2b8d-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="d2b8d-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="d2b8d-420">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-420">no</span></span>             | <span data-ttu-id="d2b8d-421">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-421">no</span></span>           |
| <span data-ttu-id="d2b8d-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="d2b8d-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="d2b8d-423">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-423">no</span></span>             | <span data-ttu-id="d2b8d-424">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-424">no</span></span>           |
| <span data-ttu-id="d2b8d-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-425">msdyn_projectid</span></span>              | <span data-ttu-id="d2b8d-426">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-426">yes</span></span>            | <span data-ttu-id="d2b8d-427">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-427">no</span></span>           |
| <span data-ttu-id="d2b8d-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-428">msdyn_projectidname</span></span>          | <span data-ttu-id="d2b8d-429">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-429">no</span></span>             | <span data-ttu-id="d2b8d-430">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-430">no</span></span>           |
| <span data-ttu-id="d2b8d-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="d2b8d-432">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-432">no</span></span>             | <span data-ttu-id="d2b8d-433">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-433">no</span></span>           |
| <span data-ttu-id="d2b8d-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="d2b8d-435">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-435">no</span></span>             | <span data-ttu-id="d2b8d-436">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-436">no</span></span>           |
| <span data-ttu-id="d2b8d-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="d2b8d-437">msdyn_start</span></span>                  | <span data-ttu-id="d2b8d-438">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-438">no</span></span>             | <span data-ttu-id="d2b8d-439">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-439">no</span></span>           |
| <span data-ttu-id="d2b8d-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-440">msdyn_taskid</span></span>                 | <span data-ttu-id="d2b8d-441">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-441">no</span></span>             | <span data-ttu-id="d2b8d-442">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-442">no</span></span>           |
| <span data-ttu-id="d2b8d-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-443">msdyn_taskidname</span></span>             | <span data-ttu-id="d2b8d-444">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-444">no</span></span>             | <span data-ttu-id="d2b8d-445">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-445">no</span></span>           |
| <span data-ttu-id="d2b8d-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="d2b8d-447">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-447">no</span></span>             | <span data-ttu-id="d2b8d-448">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="d2b8d-449">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="d2b8d-449">Project team member</span></span>

| <span data-ttu-id="d2b8d-450">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-450">**Logical name**</span></span>                                 | <span data-ttu-id="d2b8d-451">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-451">**Can create**</span></span> | <span data-ttu-id="d2b8d-452">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="d2b8d-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="d2b8d-454">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-454">no</span></span>             | <span data-ttu-id="d2b8d-455">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-455">no</span></span>           |
| <span data-ttu-id="d2b8d-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="d2b8d-457">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-457">no</span></span>             | <span data-ttu-id="d2b8d-458">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-458">no</span></span>           |
| <span data-ttu-id="d2b8d-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="d2b8d-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="d2b8d-460">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-460">no</span></span>             | <span data-ttu-id="d2b8d-461">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-461">no</span></span>           |
| <span data-ttu-id="d2b8d-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="d2b8d-463">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-463">no</span></span>             | <span data-ttu-id="d2b8d-464">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-464">no</span></span>           |
| <span data-ttu-id="d2b8d-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d2b8d-465">msdyn_effort</span></span>                                     | <span data-ttu-id="d2b8d-466">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-466">no</span></span>             | <span data-ttu-id="d2b8d-467">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-467">no</span></span>           |
| <span data-ttu-id="d2b8d-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d2b8d-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="d2b8d-469">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-469">no</span></span>             | <span data-ttu-id="d2b8d-470">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-470">no</span></span>           |
| <span data-ttu-id="d2b8d-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d2b8d-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="d2b8d-472">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-472">no</span></span>             | <span data-ttu-id="d2b8d-473">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-473">no</span></span>           |
| <span data-ttu-id="d2b8d-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d2b8d-474">msdyn_finish</span></span>                                     | <span data-ttu-id="d2b8d-475">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-475">no</span></span>             | <span data-ttu-id="d2b8d-476">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-476">no</span></span>           |
| <span data-ttu-id="d2b8d-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="d2b8d-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="d2b8d-478">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-478">no</span></span>             | <span data-ttu-id="d2b8d-479">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-479">no</span></span>           |
| <span data-ttu-id="d2b8d-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="d2b8d-480">msdyn_hours</span></span>                                      | <span data-ttu-id="d2b8d-481">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-481">no</span></span>             | <span data-ttu-id="d2b8d-482">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-482">no</span></span>           |
| <span data-ttu-id="d2b8d-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="d2b8d-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="d2b8d-484">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-484">no</span></span>             | <span data-ttu-id="d2b8d-485">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-485">no</span></span>           |
| <span data-ttu-id="d2b8d-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="d2b8d-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="d2b8d-487">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-487">no</span></span>             | <span data-ttu-id="d2b8d-488">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-488">no</span></span>           |
| <span data-ttu-id="d2b8d-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="d2b8d-490">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-490">no</span></span>             | <span data-ttu-id="d2b8d-491">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-491">no</span></span>           |
| <span data-ttu-id="d2b8d-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="d2b8d-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="d2b8d-493">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-493">no</span></span>             | <span data-ttu-id="d2b8d-494">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-494">no</span></span>           |
| <span data-ttu-id="d2b8d-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="d2b8d-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="d2b8d-496">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-496">no</span></span>             | <span data-ttu-id="d2b8d-497">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-497">no</span></span>           |
| <span data-ttu-id="d2b8d-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="d2b8d-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="d2b8d-499">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-499">no</span></span>             | <span data-ttu-id="d2b8d-500">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-500">no</span></span>           |
| <span data-ttu-id="d2b8d-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="d2b8d-501">msdyn_start</span></span>                                      | <span data-ttu-id="d2b8d-502">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-502">no</span></span>             | <span data-ttu-id="d2b8d-503">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="d2b8d-504">Project</span><span class="sxs-lookup"><span data-stu-id="d2b8d-504">Project</span></span>

| <span data-ttu-id="d2b8d-505">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-505">**Logical name**</span></span>                       | <span data-ttu-id="d2b8d-506">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-506">**Can create**</span></span> | <span data-ttu-id="d2b8d-507">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="d2b8d-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="d2b8d-509">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-509">no</span></span>             | <span data-ttu-id="d2b8d-510">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-510">no</span></span>           |
| <span data-ttu-id="d2b8d-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="d2b8d-512">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-512">no</span></span>             | <span data-ttu-id="d2b8d-513">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-513">no</span></span>           |
| <span data-ttu-id="d2b8d-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="d2b8d-515">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-515">no</span></span>             | <span data-ttu-id="d2b8d-516">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-516">no</span></span>           |
| <span data-ttu-id="d2b8d-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="d2b8d-518">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-518">no</span></span>             | <span data-ttu-id="d2b8d-519">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-519">no</span></span>           |
| <span data-ttu-id="d2b8d-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="d2b8d-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="d2b8d-521">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-521">no</span></span>             | <span data-ttu-id="d2b8d-522">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-522">no</span></span>           |
| <span data-ttu-id="d2b8d-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="d2b8d-524">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-524">no</span></span>             | <span data-ttu-id="d2b8d-525">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-525">no</span></span>           |
| <span data-ttu-id="d2b8d-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="d2b8d-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="d2b8d-527">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-527">yes</span></span>            | <span data-ttu-id="d2b8d-528">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-528">no</span></span>           |
| <span data-ttu-id="d2b8d-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="d2b8d-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="d2b8d-530">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-530">yes</span></span>            | <span data-ttu-id="d2b8d-531">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-531">no</span></span>           |
| <span data-ttu-id="d2b8d-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="d2b8d-533">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-533">yes</span></span>            | <span data-ttu-id="d2b8d-534">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-534">no</span></span>           |
| <span data-ttu-id="d2b8d-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="d2b8d-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="d2b8d-536">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-536">no</span></span>             | <span data-ttu-id="d2b8d-537">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-537">no</span></span>           |
| <span data-ttu-id="d2b8d-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="d2b8d-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="d2b8d-539">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-539">no</span></span>             | <span data-ttu-id="d2b8d-540">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-540">no</span></span>           |
| <span data-ttu-id="d2b8d-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="d2b8d-542">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-542">no</span></span>             | <span data-ttu-id="d2b8d-543">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-543">no</span></span>           |
| <span data-ttu-id="d2b8d-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="d2b8d-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="d2b8d-545">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-545">no</span></span>             | <span data-ttu-id="d2b8d-546">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-546">no</span></span>           |
| <span data-ttu-id="d2b8d-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="d2b8d-548">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-548">no</span></span>             | <span data-ttu-id="d2b8d-549">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-549">no</span></span>           |
| <span data-ttu-id="d2b8d-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="d2b8d-550">msdyn_duration</span></span>                         | <span data-ttu-id="d2b8d-551">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-551">no</span></span>             | <span data-ttu-id="d2b8d-552">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-552">no</span></span>           |
| <span data-ttu-id="d2b8d-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="d2b8d-553">msdyn_effort</span></span>                           | <span data-ttu-id="d2b8d-554">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-554">no</span></span>             | <span data-ttu-id="d2b8d-555">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-555">no</span></span>           |
| <span data-ttu-id="d2b8d-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="d2b8d-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="d2b8d-557">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-557">no</span></span>             | <span data-ttu-id="d2b8d-558">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-558">no</span></span>           |
| <span data-ttu-id="d2b8d-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="d2b8d-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="d2b8d-560">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-560">no</span></span>             | <span data-ttu-id="d2b8d-561">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-561">no</span></span>           |
| <span data-ttu-id="d2b8d-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="d2b8d-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="d2b8d-563">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-563">no</span></span>             | <span data-ttu-id="d2b8d-564">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-564">no</span></span>           |
| <span data-ttu-id="d2b8d-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="d2b8d-565">msdyn_finish</span></span>                           | <span data-ttu-id="d2b8d-566">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-566">yes</span></span>            | <span data-ttu-id="d2b8d-567">áno</span><span class="sxs-lookup"><span data-stu-id="d2b8d-567">yes</span></span>          |
| <span data-ttu-id="d2b8d-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="d2b8d-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="d2b8d-569">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-569">no</span></span>             | <span data-ttu-id="d2b8d-570">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-570">no</span></span>           |
| <span data-ttu-id="d2b8d-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="d2b8d-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="d2b8d-572">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-572">no</span></span>             | <span data-ttu-id="d2b8d-573">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-573">no</span></span>           |
| <span data-ttu-id="d2b8d-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="d2b8d-575">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-575">no</span></span>             | <span data-ttu-id="d2b8d-576">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-576">no</span></span>           |
| <span data-ttu-id="d2b8d-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="d2b8d-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="d2b8d-578">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-578">no</span></span>             | <span data-ttu-id="d2b8d-579">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-579">no</span></span>           |
| <span data-ttu-id="d2b8d-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="d2b8d-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="d2b8d-581">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-581">no</span></span>             | <span data-ttu-id="d2b8d-582">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-582">no</span></span>           |
| <span data-ttu-id="d2b8d-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="d2b8d-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="d2b8d-584">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-584">no</span></span>             | <span data-ttu-id="d2b8d-585">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-585">no</span></span>           |
| <span data-ttu-id="d2b8d-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="d2b8d-587">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-587">no</span></span>             | <span data-ttu-id="d2b8d-588">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-588">no</span></span>           |
| <span data-ttu-id="d2b8d-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="d2b8d-590">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-590">no</span></span>             | <span data-ttu-id="d2b8d-591">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-591">no</span></span>           |
| <span data-ttu-id="d2b8d-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="d2b8d-593">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-593">no</span></span>             | <span data-ttu-id="d2b8d-594">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-594">no</span></span>           |
| <span data-ttu-id="d2b8d-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="d2b8d-596">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-596">no</span></span>             | <span data-ttu-id="d2b8d-597">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-597">no</span></span>           |
| <span data-ttu-id="d2b8d-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="d2b8d-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="d2b8d-599">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-599">no</span></span>             | <span data-ttu-id="d2b8d-600">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-600">no</span></span>           |
| <span data-ttu-id="d2b8d-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="d2b8d-602">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-602">no</span></span>             | <span data-ttu-id="d2b8d-603">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-603">no</span></span>           |
| <span data-ttu-id="d2b8d-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="d2b8d-604">msdyn_progress</span></span>                         | <span data-ttu-id="d2b8d-605">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-605">no</span></span>             | <span data-ttu-id="d2b8d-606">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-606">no</span></span>           |
| <span data-ttu-id="d2b8d-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="d2b8d-608">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-608">no</span></span>             | <span data-ttu-id="d2b8d-609">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-609">no</span></span>           |
| <span data-ttu-id="d2b8d-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="d2b8d-611">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-611">no</span></span>             | <span data-ttu-id="d2b8d-612">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-612">no</span></span>           |
| <span data-ttu-id="d2b8d-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="d2b8d-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="d2b8d-614">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-614">no</span></span>             | <span data-ttu-id="d2b8d-615">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-615">no</span></span>           |
| <span data-ttu-id="d2b8d-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="d2b8d-617">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-617">no</span></span>             | <span data-ttu-id="d2b8d-618">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-618">no</span></span>           |
| <span data-ttu-id="d2b8d-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="d2b8d-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="d2b8d-620">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-620">no</span></span>             | <span data-ttu-id="d2b8d-621">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-621">no</span></span>           |
| <span data-ttu-id="d2b8d-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="d2b8d-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="d2b8d-623">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-623">no</span></span>             | <span data-ttu-id="d2b8d-624">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-624">no</span></span>           |
| <span data-ttu-id="d2b8d-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="d2b8d-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="d2b8d-626">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-626">no</span></span>             | <span data-ttu-id="d2b8d-627">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-627">no</span></span>           |
| <span data-ttu-id="d2b8d-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="d2b8d-629">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-629">no</span></span>             | <span data-ttu-id="d2b8d-630">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-630">no</span></span>           |
| <span data-ttu-id="d2b8d-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="d2b8d-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="d2b8d-632">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-632">no</span></span>             | <span data-ttu-id="d2b8d-633">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-633">no</span></span>           |
| <span data-ttu-id="d2b8d-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="d2b8d-635">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-635">no</span></span>             | <span data-ttu-id="d2b8d-636">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-636">no</span></span>           |
| <span data-ttu-id="d2b8d-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="d2b8d-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="d2b8d-638">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-638">no</span></span>             | <span data-ttu-id="d2b8d-639">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-639">no</span></span>           |
| <span data-ttu-id="d2b8d-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="d2b8d-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="d2b8d-641">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-641">no</span></span>             | <span data-ttu-id="d2b8d-642">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-642">no</span></span>           |
| <span data-ttu-id="d2b8d-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="d2b8d-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="d2b8d-644">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-644">no</span></span>             | <span data-ttu-id="d2b8d-645">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-645">no</span></span>           |
| <span data-ttu-id="d2b8d-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="d2b8d-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="d2b8d-647">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-647">no</span></span>             | <span data-ttu-id="d2b8d-648">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-648">no</span></span>           |
| <span data-ttu-id="d2b8d-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="d2b8d-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="d2b8d-650">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-650">no</span></span>             | <span data-ttu-id="d2b8d-651">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-651">no</span></span>           |
| <span data-ttu-id="d2b8d-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="d2b8d-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="d2b8d-653">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-653">no</span></span>             | <span data-ttu-id="d2b8d-654">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-654">no</span></span>           |
| <span data-ttu-id="d2b8d-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="d2b8d-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="d2b8d-656">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-656">no</span></span>             | <span data-ttu-id="d2b8d-657">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-657">no</span></span>           |
| <span data-ttu-id="d2b8d-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="d2b8d-659">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-659">no</span></span>             | <span data-ttu-id="d2b8d-660">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-660">no</span></span>           |
| <span data-ttu-id="d2b8d-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="d2b8d-662">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-662">no</span></span>             | <span data-ttu-id="d2b8d-663">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-663">no</span></span>           |
| <span data-ttu-id="d2b8d-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="d2b8d-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="d2b8d-665">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-665">no</span></span>             | <span data-ttu-id="d2b8d-666">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-666">no</span></span>           |
| <span data-ttu-id="d2b8d-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="d2b8d-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="d2b8d-668">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-668">no</span></span>             | <span data-ttu-id="d2b8d-669">nie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="d2b8d-670">Obmedzenia a známe problémy</span><span class="sxs-lookup"><span data-stu-id="d2b8d-670">Limitations and known issues</span></span>
<span data-ttu-id="d2b8d-671">Nasleduje zoznam obmedzení a známych problémov:</span><span class="sxs-lookup"><span data-stu-id="d2b8d-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="d2b8d-672">Rozhrania API plánovania projektu môžu používať iba **Používatelia s licenciou Microsoft Project.**</span><span class="sxs-lookup"><span data-stu-id="d2b8d-672">Project Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="d2b8d-673">Nemôžu ich používať:</span><span class="sxs-lookup"><span data-stu-id="d2b8d-673">They can't be used by:</span></span>
    - <span data-ttu-id="d2b8d-674">Používatelia aplikácie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-674">Application users</span></span>
    - <span data-ttu-id="d2b8d-675">Systémoví používatelia</span><span class="sxs-lookup"><span data-stu-id="d2b8d-675">System users</span></span>
    - <span data-ttu-id="d2b8d-676">Používatelia integrácie</span><span class="sxs-lookup"><span data-stu-id="d2b8d-676">Integration users</span></span>
    - <span data-ttu-id="d2b8d-677">Ostatní používatelia, ktorí nemajú požadovanú licenciu</span><span class="sxs-lookup"><span data-stu-id="d2b8d-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="d2b8d-678">Každá množina **OperationSet** môže mať maximálne 100 operácií.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="d2b8d-679">Každý používateľ môže mať maximálne 10 otvorených množín **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="d2b8d-680">Project Operations v súčasnosti podporuje v projekte celkovo maximálne 500 úloh.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="d2b8d-681">Stav zlyhania množiny **OperationSet** a protokoly zlyhaní nie sú momentálne k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="d2b8d-682">Hranice projektov a úloh</span><span class="sxs-lookup"><span data-stu-id="d2b8d-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="d2b8d-683">Spracovanie chýb</span><span class="sxs-lookup"><span data-stu-id="d2b8d-683">Error handling</span></span>

   - <span data-ttu-id="d2b8d-684">Ak chcete skontrolovať chyby generované z množín operácií, prejdite na **Nastavenie**\> **Integrácia plánu** \> **Množiny operácií**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="d2b8d-685">Ak chcete skontrolovať chyby generované službou plánovania projektu, prejdite na **Nastavenia** \> **Integrácia plánu** \> **Denník chýb PSS**.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-685">To review errors generated from the Project schedule Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="d2b8d-686">Vzorový scenár</span><span class="sxs-lookup"><span data-stu-id="d2b8d-686">Sample scenario</span></span>

<span data-ttu-id="d2b8d-687">V tomto scenári vytvoríte projekt, člena tímu, štyri úlohy a dve priradenia zdrojov.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="d2b8d-688">Ďalej aktualizujete jednu úlohu, projekt, odstránite jednu úlohu, odstránite jedno priradenie zdroja a vytvoríte závislosť úlohy.</span><span class="sxs-lookup"><span data-stu-id="d2b8d-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="d2b8d-689">Ďalšie ukážky</span><span class="sxs-lookup"><span data-stu-id="d2b8d-689">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
