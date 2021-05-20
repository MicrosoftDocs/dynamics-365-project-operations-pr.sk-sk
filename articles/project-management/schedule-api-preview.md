---
title: Používanie rozhraní API na plánovanie na vykonávanie operácií s entitami plánovania
description: Táto téma poskytuje informácie a ukážky používania rozhraní API na plánovanie.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950823"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="01da0-103">Používanie rozhraní API na plánovanie na vykonávanie operácií s entitami plánovania</span><span class="sxs-lookup"><span data-stu-id="01da0-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="01da0-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="01da0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="01da0-105">Niektoré alebo všetky z funkcií uvádzaných v tejto téme sú k dispozícii ako súčasť vydania verzie Preview.</span><span class="sxs-lookup"><span data-stu-id="01da0-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="01da0-106">Obsah a funkcie sa môžu zmeniť.</span><span class="sxs-lookup"><span data-stu-id="01da0-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="01da0-107">Entity na plánovanie</span><span class="sxs-lookup"><span data-stu-id="01da0-107">Scheduling entities</span></span>

<span data-ttu-id="01da0-108">Rozhrania API na plánovanie poskytujú možnosť vykonávať operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania**.</span><span class="sxs-lookup"><span data-stu-id="01da0-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="01da0-109">Tieto entity sú spravované prostredníctvom modulu Plánovanie v Projekte pre web.</span><span class="sxs-lookup"><span data-stu-id="01da0-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="01da0-110">Operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania** boli obmedzené v skorších vydaniach Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="01da0-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="01da0-111">Nasledujúca tabuľka poskytuje úplný zoznam **Entít na plánovanie**.</span><span class="sxs-lookup"><span data-stu-id="01da0-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="01da0-112">Názov entity</span><span class="sxs-lookup"><span data-stu-id="01da0-112">Entity name</span></span>  | <span data-ttu-id="01da0-113">Logický názov entity</span><span class="sxs-lookup"><span data-stu-id="01da0-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="01da0-114">Project</span><span class="sxs-lookup"><span data-stu-id="01da0-114">Project</span></span> | <span data-ttu-id="01da0-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="01da0-115">msdyn_project</span></span> |
| <span data-ttu-id="01da0-116">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="01da0-116">Project Task</span></span>  | <span data-ttu-id="01da0-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="01da0-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="01da0-118">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="01da0-118">Project Task Dependency</span></span>  | <span data-ttu-id="01da0-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="01da0-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="01da0-120">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="01da0-120">Resource Assignment</span></span> | <span data-ttu-id="01da0-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="01da0-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="01da0-122">Projektový kontajner</span><span class="sxs-lookup"><span data-stu-id="01da0-122">Project Bucket</span></span>  | <span data-ttu-id="01da0-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="01da0-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="01da0-124">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="01da0-124">Project Team Member</span></span> | <span data-ttu-id="01da0-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="01da0-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="01da0-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="01da0-126">OperationSet</span></span>

<span data-ttu-id="01da0-127">OperationSet je vzor jednotky práce, ktorý je možné použiť, keď sa v rámci transakcie musí spracovať niekoľko požiadaviek ovplyvňujúcich plán.</span><span class="sxs-lookup"><span data-stu-id="01da0-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="01da0-128">Rozhrania API pre plánovanie</span><span class="sxs-lookup"><span data-stu-id="01da0-128">Schedule APIs</span></span>

<span data-ttu-id="01da0-129">Nasleduje zoznam aktuálnych rozhraní API pre plánovanie.</span><span class="sxs-lookup"><span data-stu-id="01da0-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="01da0-130">**msdyn_CreateProjectV1**: Toto rozhranie API možno použiť na vytvorenie projektu.</span><span class="sxs-lookup"><span data-stu-id="01da0-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="01da0-131">Projekt a predvolený kontajner projektu sa vytvorí okamžite.</span><span class="sxs-lookup"><span data-stu-id="01da0-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="01da0-132">**msdyn_CreateTeamMemberV1**: Toto rozhranie API možno použiť na vytvorenie člena projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="01da0-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="01da0-133">Záznam o členovi tímu sa vytvorí okamžite.</span><span class="sxs-lookup"><span data-stu-id="01da0-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="01da0-134">**msdyn_CreateOperationSetV1**: Toto API možno použiť na naplánovanie niekoľkých požiadaviek, ktoré sa musia vykonať v rámci transakcie.</span><span class="sxs-lookup"><span data-stu-id="01da0-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="01da0-135">**msdyn_PSSCreateV1**: Toto API možno použiť na vytvorenie entity.</span><span class="sxs-lookup"><span data-stu-id="01da0-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="01da0-136">Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu vytvorenia.</span><span class="sxs-lookup"><span data-stu-id="01da0-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="01da0-137">**msdyn_PSSUpdateV1**: Toto API možno použiť na aktualizáciu entity.</span><span class="sxs-lookup"><span data-stu-id="01da0-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="01da0-138">Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="01da0-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="01da0-139">**msdyn_PSSDeleteV1**: Toto API možno použiť na odstránenie entity.</span><span class="sxs-lookup"><span data-stu-id="01da0-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="01da0-140">Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu odstránenia.</span><span class="sxs-lookup"><span data-stu-id="01da0-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="01da0-141">**msdyn_ExecuteOperationSetV1**: Toto API sa používa na vykonávanie všetkých operácií v rámci danej množiny operácií.</span><span class="sxs-lookup"><span data-stu-id="01da0-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="01da0-142">Používanie rozhraní API plánovania s množinou OperationSet</span><span class="sxs-lookup"><span data-stu-id="01da0-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="01da0-143">Pretože záznamy s **CreateProjectV1** a **CreateTeamMemberV1** sú vytvorené okamžite, tieto API nemôžu byť použité v **OperationSet** priamo.</span><span class="sxs-lookup"><span data-stu-id="01da0-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="01da0-144">Môžete však použiť API na vytvorenie potrebných záznamov, vytvorenie **OperationSet** a potom použiť tieto vopred vytvorené záznamy v **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="01da0-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="01da0-145">Podporované operácie</span><span class="sxs-lookup"><span data-stu-id="01da0-145">Supported operations</span></span>

| <span data-ttu-id="01da0-146">Entita na plánovanie</span><span class="sxs-lookup"><span data-stu-id="01da0-146">Scheduling entity</span></span> | <span data-ttu-id="01da0-147">Vytvoriť</span><span class="sxs-lookup"><span data-stu-id="01da0-147">Create</span></span> | <span data-ttu-id="01da0-148">Aktualizácia</span><span class="sxs-lookup"><span data-stu-id="01da0-148">Update</span></span> | <span data-ttu-id="01da0-149">Delete</span><span class="sxs-lookup"><span data-stu-id="01da0-149">Delete</span></span> | <span data-ttu-id="01da0-150">Dôležité aspekty</span><span class="sxs-lookup"><span data-stu-id="01da0-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="01da0-151">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="01da0-151">Project task</span></span> | <span data-ttu-id="01da0-152">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-152">Yes</span></span> | <span data-ttu-id="01da0-153">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-153">Yes</span></span> | <span data-ttu-id="01da0-154">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-154">Yes</span></span> | <span data-ttu-id="01da0-155">Nie je</span><span class="sxs-lookup"><span data-stu-id="01da0-155">None</span></span> |
| <span data-ttu-id="01da0-156">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="01da0-156">Project task dependency</span></span> | <span data-ttu-id="01da0-157">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-157">Yes</span></span> | <span data-ttu-id="01da0-158">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-158">Yes</span></span> | | <span data-ttu-id="01da0-159">Záznamy o závislosti od projektových úloh sa neaktualizujú.</span><span class="sxs-lookup"><span data-stu-id="01da0-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="01da0-160">Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam.</span><span class="sxs-lookup"><span data-stu-id="01da0-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="01da0-161">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="01da0-161">Resource assignment</span></span> | <span data-ttu-id="01da0-162">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-162">Yes</span></span> | <span data-ttu-id="01da0-163">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-163">Yes</span></span> | | <span data-ttu-id="01da0-164">Operácie s nasledujúcimi poľami nie sú podporované: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="01da0-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="01da0-165">Záznamy o priradení zdrojov sa neaktualizujú.</span><span class="sxs-lookup"><span data-stu-id="01da0-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="01da0-166">Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam.</span><span class="sxs-lookup"><span data-stu-id="01da0-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="01da0-167">Projektový kontajner</span><span class="sxs-lookup"><span data-stu-id="01da0-167">Project bucket</span></span> | <span data-ttu-id="01da0-168">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="01da0-168">N/A</span></span> | <span data-ttu-id="01da0-169">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="01da0-169">N/A</span></span> | <span data-ttu-id="01da0-170">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="01da0-170">N/A</span></span> | <span data-ttu-id="01da0-171">Predvolený kontajner sa vytvára pomocou API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="01da0-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="01da0-172">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="01da0-172">Project team member</span></span> | <span data-ttu-id="01da0-173">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-173">Yes</span></span> | <span data-ttu-id="01da0-174">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-174">Yes</span></span> | <span data-ttu-id="01da0-175">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-175">Yes</span></span> | <span data-ttu-id="01da0-176">Na operáciu vytvorenia použite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="01da0-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="01da0-177">Project</span><span class="sxs-lookup"><span data-stu-id="01da0-177">Project</span></span> | <span data-ttu-id="01da0-178">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-178">Yes</span></span> | <span data-ttu-id="01da0-179">Áno</span><span class="sxs-lookup"><span data-stu-id="01da0-179">Yes</span></span> | <span data-ttu-id="01da0-180">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="01da0-180">N/A</span></span> | <span data-ttu-id="01da0-181">Operácie s nasledujúcimi poľami nie sú podporované: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.</span><span class="sxs-lookup"><span data-stu-id="01da0-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="01da0-182">Tieto rozhrania API je možné volať s objektmi entít, ktoré obsahujú vlastné polia.</span><span class="sxs-lookup"><span data-stu-id="01da0-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="01da0-183">Toto ID vlastnosti je voliteľné.</span><span class="sxs-lookup"><span data-stu-id="01da0-183">The ID property is optional.</span></span> <span data-ttu-id="01da0-184">Ak je uvedené, systém sa ho pokúsi použiť a v prípade, že ho nemožno použiť, vyvolá výnimku.</span><span class="sxs-lookup"><span data-stu-id="01da0-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="01da0-185">Ak nie je uvedené, systém ho vygeneruje.</span><span class="sxs-lookup"><span data-stu-id="01da0-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="01da0-186">Obmedzené polia</span><span class="sxs-lookup"><span data-stu-id="01da0-186">Restricted fields</span></span>

<span data-ttu-id="01da0-187">Nasledujúce tabuľky definujú polia, ktoré sú obmedzené v rámci možností **Vytvoriť** a **Upraviť**.</span><span class="sxs-lookup"><span data-stu-id="01da0-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="01da0-188">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="01da0-188">Project task</span></span>

| <span data-ttu-id="01da0-189">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="01da0-189">**Logical name**</span></span>                       | <span data-ttu-id="01da0-190">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="01da0-190">**Can create**</span></span> | <span data-ttu-id="01da0-191">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="01da0-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="01da0-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="01da0-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="01da0-193">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-193">no</span></span>             | <span data-ttu-id="01da0-194">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-194">no</span></span>               |
| <span data-ttu-id="01da0-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="01da0-196">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-196">no</span></span>             | <span data-ttu-id="01da0-197">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-197">no</span></span>               |
| <span data-ttu-id="01da0-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="01da0-198">msdyn_actualend</span></span>                        | <span data-ttu-id="01da0-199">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-199">no</span></span>             | <span data-ttu-id="01da0-200">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-200">no</span></span>               |
| <span data-ttu-id="01da0-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="01da0-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="01da0-202">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-202">no</span></span>             | <span data-ttu-id="01da0-203">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-203">no</span></span>               |
| <span data-ttu-id="01da0-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="01da0-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="01da0-205">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-205">no</span></span>             | <span data-ttu-id="01da0-206">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-206">no</span></span>               |
| <span data-ttu-id="01da0-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="01da0-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="01da0-208">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-208">no</span></span>             | <span data-ttu-id="01da0-209">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-209">no</span></span>               |
| <span data-ttu-id="01da0-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="01da0-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="01da0-211">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-211">no</span></span>             | <span data-ttu-id="01da0-212">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-212">no</span></span>               |
| <span data-ttu-id="01da0-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="01da0-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="01da0-214">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-214">no</span></span>             | <span data-ttu-id="01da0-215">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-215">no</span></span>               |
| <span data-ttu-id="01da0-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="01da0-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="01da0-217">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-217">no</span></span>             | <span data-ttu-id="01da0-218">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-218">no</span></span>               |
| <span data-ttu-id="01da0-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="01da0-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="01da0-220">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-220">no</span></span>             | <span data-ttu-id="01da0-221">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-221">no</span></span>               |
| <span data-ttu-id="01da0-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="01da0-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="01da0-223">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-223">no</span></span>             | <span data-ttu-id="01da0-224">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-224">no</span></span>               |
| <span data-ttu-id="01da0-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="01da0-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="01da0-226">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-226">no</span></span>             | <span data-ttu-id="01da0-227">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-227">no</span></span>               |
| <span data-ttu-id="01da0-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="01da0-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="01da0-229">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-229">no</span></span>             | <span data-ttu-id="01da0-230">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-230">no</span></span>               |
| <span data-ttu-id="01da0-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="01da0-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="01da0-232">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-232">no</span></span>             | <span data-ttu-id="01da0-233">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-233">no</span></span>               |
| <span data-ttu-id="01da0-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="01da0-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="01da0-235">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-235">no</span></span>             | <span data-ttu-id="01da0-236">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-236">no</span></span>               |
| <span data-ttu-id="01da0-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="01da0-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="01da0-238">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-238">no</span></span>             | <span data-ttu-id="01da0-239">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-239">no</span></span>               |
| <span data-ttu-id="01da0-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="01da0-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="01da0-241">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-241">no</span></span>             | <span data-ttu-id="01da0-242">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-242">no</span></span>               |
| <span data-ttu-id="01da0-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="01da0-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="01da0-244">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-244">no</span></span>             | <span data-ttu-id="01da0-245">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-245">no</span></span>               |
| <span data-ttu-id="01da0-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="01da0-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="01da0-247">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-247">no</span></span>             | <span data-ttu-id="01da0-248">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-248">no</span></span>               |
| <span data-ttu-id="01da0-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="01da0-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="01da0-250">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-250">no</span></span>             | <span data-ttu-id="01da0-251">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-251">no</span></span>               |
| <span data-ttu-id="01da0-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="01da0-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="01da0-253">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-253">no</span></span>             | <span data-ttu-id="01da0-254">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-254">no</span></span>               |
| <span data-ttu-id="01da0-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="01da0-256">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-256">no</span></span>             | <span data-ttu-id="01da0-257">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-257">no</span></span>               |
| <span data-ttu-id="01da0-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="01da0-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="01da0-259">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-259">no</span></span>             | <span data-ttu-id="01da0-260">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-260">no</span></span>               |
| <span data-ttu-id="01da0-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="01da0-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="01da0-262">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-262">no</span></span>             | <span data-ttu-id="01da0-263">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-263">no</span></span>               |
| <span data-ttu-id="01da0-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="01da0-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="01da0-265">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-265">no</span></span>             | <span data-ttu-id="01da0-266">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-266">no</span></span>               |
| <span data-ttu-id="01da0-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="01da0-267">msdyn_progress</span></span>                         | <span data-ttu-id="01da0-268">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-268">no</span></span>             | <span data-ttu-id="01da0-269">nie (áno pre P4W)</span><span class="sxs-lookup"><span data-stu-id="01da0-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="01da0-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="01da0-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="01da0-271">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-271">no</span></span>             | <span data-ttu-id="01da0-272">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-272">no</span></span>               |
| <span data-ttu-id="01da0-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="01da0-274">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-274">no</span></span>             | <span data-ttu-id="01da0-275">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-275">no</span></span>               |
| <span data-ttu-id="01da0-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="01da0-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="01da0-277">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-277">no</span></span>             | <span data-ttu-id="01da0-278">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-278">no</span></span>               |
| <span data-ttu-id="01da0-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="01da0-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="01da0-280">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-280">no</span></span>             | <span data-ttu-id="01da0-281">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-281">no</span></span>               |
| <span data-ttu-id="01da0-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="01da0-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="01da0-283">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-283">no</span></span>             | <span data-ttu-id="01da0-284">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-284">no</span></span>               |
| <span data-ttu-id="01da0-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="01da0-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="01da0-286">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-286">no</span></span>             | <span data-ttu-id="01da0-287">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-287">no</span></span>               |
| <span data-ttu-id="01da0-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="01da0-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="01da0-289">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-289">no</span></span>             | <span data-ttu-id="01da0-290">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-290">no</span></span>               |
| <span data-ttu-id="01da0-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="01da0-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="01da0-292">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-292">no</span></span>             | <span data-ttu-id="01da0-293">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-293">no</span></span>               |
| <span data-ttu-id="01da0-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="01da0-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="01da0-295">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-295">no</span></span>             | <span data-ttu-id="01da0-296">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-296">no</span></span>               |
| <span data-ttu-id="01da0-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="01da0-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="01da0-298">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-298">no</span></span>             | <span data-ttu-id="01da0-299">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-299">no</span></span>               |
| <span data-ttu-id="01da0-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="01da0-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="01da0-301">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-301">no</span></span>             | <span data-ttu-id="01da0-302">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-302">no</span></span>               |
| <span data-ttu-id="01da0-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="01da0-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="01da0-304">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-304">no</span></span>             | <span data-ttu-id="01da0-305">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-305">no</span></span>               |
| <span data-ttu-id="01da0-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="01da0-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="01da0-307">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-307">no</span></span>             | <span data-ttu-id="01da0-308">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-308">no</span></span>               |
| <span data-ttu-id="01da0-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="01da0-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="01da0-310">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-310">no</span></span>             | <span data-ttu-id="01da0-311">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-311">no</span></span>               |
| <span data-ttu-id="01da0-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="01da0-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="01da0-313">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-313">no</span></span>             | <span data-ttu-id="01da0-314">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-314">no</span></span>               |
| <span data-ttu-id="01da0-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="01da0-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="01da0-316">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-316">no</span></span>             | <span data-ttu-id="01da0-317">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-317">no</span></span>               |
| <span data-ttu-id="01da0-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="01da0-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="01da0-319">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-319">no</span></span>             | <span data-ttu-id="01da0-320">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-320">no</span></span>               |
| <span data-ttu-id="01da0-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="01da0-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="01da0-322">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-322">no</span></span>             | <span data-ttu-id="01da0-323">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-323">no</span></span>               |
| <span data-ttu-id="01da0-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="01da0-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="01da0-325">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-325">no</span></span>             | <span data-ttu-id="01da0-326">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-326">no</span></span>               |
| <span data-ttu-id="01da0-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="01da0-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="01da0-328">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-328">no</span></span>             | <span data-ttu-id="01da0-329">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-329">no</span></span>               |
| <span data-ttu-id="01da0-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="01da0-330">msdyn_summary</span></span>                          | <span data-ttu-id="01da0-331">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-331">no</span></span>             | <span data-ttu-id="01da0-332">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-332">no</span></span>               |
| <span data-ttu-id="01da0-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="01da0-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="01da0-334">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-334">no</span></span>             | <span data-ttu-id="01da0-335">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-335">no</span></span>               |
| <span data-ttu-id="01da0-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="01da0-337">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-337">no</span></span>             | <span data-ttu-id="01da0-338">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="01da0-339">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="01da0-339">Project task dependency</span></span>

| <span data-ttu-id="01da0-340">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="01da0-340">**Logical name**</span></span>              | <span data-ttu-id="01da0-341">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="01da0-341">**Can create**</span></span> | <span data-ttu-id="01da0-342">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="01da0-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="01da0-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="01da0-343">msdyn_linktype</span></span>                | <span data-ttu-id="01da0-344">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-344">no</span></span>             | <span data-ttu-id="01da0-345">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-345">no</span></span>           |
| <span data-ttu-id="01da0-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="01da0-346">msdyn_linktypename</span></span>            | <span data-ttu-id="01da0-347">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-347">no</span></span>             | <span data-ttu-id="01da0-348">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-348">no</span></span>           |
| <span data-ttu-id="01da0-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="01da0-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="01da0-350">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-350">yes</span></span>            | <span data-ttu-id="01da0-351">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-351">no</span></span>           |
| <span data-ttu-id="01da0-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="01da0-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="01da0-353">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-353">yes</span></span>            | <span data-ttu-id="01da0-354">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-354">no</span></span>           |
| <span data-ttu-id="01da0-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="01da0-355">msdyn_project</span></span>                 | <span data-ttu-id="01da0-356">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-356">yes</span></span>            | <span data-ttu-id="01da0-357">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-357">no</span></span>           |
| <span data-ttu-id="01da0-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="01da0-358">msdyn_projectname</span></span>             | <span data-ttu-id="01da0-359">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-359">yes</span></span>            | <span data-ttu-id="01da0-360">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-360">no</span></span>           |
| <span data-ttu-id="01da0-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="01da0-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="01da0-362">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-362">yes</span></span>            | <span data-ttu-id="01da0-363">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-363">no</span></span>           |
| <span data-ttu-id="01da0-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="01da0-364">msdyn_successortask</span></span>           | <span data-ttu-id="01da0-365">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-365">yes</span></span>            | <span data-ttu-id="01da0-366">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-366">no</span></span>           |
| <span data-ttu-id="01da0-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="01da0-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="01da0-368">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-368">yes</span></span>            | <span data-ttu-id="01da0-369">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="01da0-370">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="01da0-370">Resource assignment</span></span>

| <span data-ttu-id="01da0-371">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="01da0-371">**Logical name**</span></span>             | <span data-ttu-id="01da0-372">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="01da0-372">**Can create**</span></span> | <span data-ttu-id="01da0-373">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="01da0-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="01da0-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="01da0-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="01da0-375">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-375">yes</span></span>            | <span data-ttu-id="01da0-376">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-376">no</span></span>           |
| <span data-ttu-id="01da0-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="01da0-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="01da0-378">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-378">yes</span></span>            | <span data-ttu-id="01da0-379">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-379">no</span></span>           |
| <span data-ttu-id="01da0-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="01da0-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="01da0-381">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-381">no</span></span>             | <span data-ttu-id="01da0-382">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-382">no</span></span>           |
| <span data-ttu-id="01da0-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="01da0-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="01da0-384">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-384">no</span></span>             | <span data-ttu-id="01da0-385">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-385">no</span></span>           |
| <span data-ttu-id="01da0-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="01da0-386">msdyn_committype</span></span>             | <span data-ttu-id="01da0-387">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-387">no</span></span>             | <span data-ttu-id="01da0-388">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-388">no</span></span>           |
| <span data-ttu-id="01da0-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="01da0-389">msdyn_committypename</span></span>         | <span data-ttu-id="01da0-390">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-390">no</span></span>             | <span data-ttu-id="01da0-391">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-391">no</span></span>           |
| <span data-ttu-id="01da0-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="01da0-392">msdyn_effort</span></span>                 | <span data-ttu-id="01da0-393">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-393">no</span></span>             | <span data-ttu-id="01da0-394">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-394">no</span></span>           |
| <span data-ttu-id="01da0-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="01da0-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="01da0-396">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-396">no</span></span>             | <span data-ttu-id="01da0-397">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-397">no</span></span>           |
| <span data-ttu-id="01da0-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="01da0-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="01da0-399">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-399">no</span></span>             | <span data-ttu-id="01da0-400">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-400">no</span></span>           |
| <span data-ttu-id="01da0-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="01da0-401">msdyn_finish</span></span>                 | <span data-ttu-id="01da0-402">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-402">no</span></span>             | <span data-ttu-id="01da0-403">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-403">no</span></span>           |
| <span data-ttu-id="01da0-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="01da0-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="01da0-405">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-405">no</span></span>             | <span data-ttu-id="01da0-406">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-406">no</span></span>           |
| <span data-ttu-id="01da0-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="01da0-408">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-408">no</span></span>             | <span data-ttu-id="01da0-409">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-409">no</span></span>           |
| <span data-ttu-id="01da0-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="01da0-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="01da0-411">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-411">no</span></span>             | <span data-ttu-id="01da0-412">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-412">no</span></span>           |
| <span data-ttu-id="01da0-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="01da0-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="01da0-414">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-414">no</span></span>             | <span data-ttu-id="01da0-415">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-415">no</span></span>           |
| <span data-ttu-id="01da0-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="01da0-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="01da0-417">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-417">no</span></span>             | <span data-ttu-id="01da0-418">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-418">no</span></span>           |
| <span data-ttu-id="01da0-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="01da0-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="01da0-420">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-420">no</span></span>             | <span data-ttu-id="01da0-421">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-421">no</span></span>           |
| <span data-ttu-id="01da0-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="01da0-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="01da0-423">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-423">no</span></span>             | <span data-ttu-id="01da0-424">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-424">no</span></span>           |
| <span data-ttu-id="01da0-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="01da0-425">msdyn_projectid</span></span>              | <span data-ttu-id="01da0-426">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-426">yes</span></span>            | <span data-ttu-id="01da0-427">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-427">no</span></span>           |
| <span data-ttu-id="01da0-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="01da0-428">msdyn_projectidname</span></span>          | <span data-ttu-id="01da0-429">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-429">no</span></span>             | <span data-ttu-id="01da0-430">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-430">no</span></span>           |
| <span data-ttu-id="01da0-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="01da0-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="01da0-432">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-432">no</span></span>             | <span data-ttu-id="01da0-433">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-433">no</span></span>           |
| <span data-ttu-id="01da0-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="01da0-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="01da0-435">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-435">no</span></span>             | <span data-ttu-id="01da0-436">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-436">no</span></span>           |
| <span data-ttu-id="01da0-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="01da0-437">msdyn_start</span></span>                  | <span data-ttu-id="01da0-438">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-438">no</span></span>             | <span data-ttu-id="01da0-439">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-439">no</span></span>           |
| <span data-ttu-id="01da0-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="01da0-440">msdyn_taskid</span></span>                 | <span data-ttu-id="01da0-441">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-441">no</span></span>             | <span data-ttu-id="01da0-442">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-442">no</span></span>           |
| <span data-ttu-id="01da0-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="01da0-443">msdyn_taskidname</span></span>             | <span data-ttu-id="01da0-444">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-444">no</span></span>             | <span data-ttu-id="01da0-445">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-445">no</span></span>           |
| <span data-ttu-id="01da0-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="01da0-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="01da0-447">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-447">no</span></span>             | <span data-ttu-id="01da0-448">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="01da0-449">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="01da0-449">Project team member</span></span>

| <span data-ttu-id="01da0-450">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="01da0-450">**Logical name**</span></span>                                 | <span data-ttu-id="01da0-451">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="01da0-451">**Can create**</span></span> | <span data-ttu-id="01da0-452">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="01da0-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="01da0-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="01da0-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="01da0-454">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-454">no</span></span>             | <span data-ttu-id="01da0-455">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-455">no</span></span>           |
| <span data-ttu-id="01da0-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="01da0-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="01da0-457">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-457">no</span></span>             | <span data-ttu-id="01da0-458">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-458">no</span></span>           |
| <span data-ttu-id="01da0-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="01da0-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="01da0-460">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-460">no</span></span>             | <span data-ttu-id="01da0-461">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-461">no</span></span>           |
| <span data-ttu-id="01da0-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="01da0-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="01da0-463">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-463">no</span></span>             | <span data-ttu-id="01da0-464">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-464">no</span></span>           |
| <span data-ttu-id="01da0-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="01da0-465">msdyn_effort</span></span>                                     | <span data-ttu-id="01da0-466">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-466">no</span></span>             | <span data-ttu-id="01da0-467">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-467">no</span></span>           |
| <span data-ttu-id="01da0-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="01da0-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="01da0-469">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-469">no</span></span>             | <span data-ttu-id="01da0-470">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-470">no</span></span>           |
| <span data-ttu-id="01da0-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="01da0-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="01da0-472">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-472">no</span></span>             | <span data-ttu-id="01da0-473">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-473">no</span></span>           |
| <span data-ttu-id="01da0-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="01da0-474">msdyn_finish</span></span>                                     | <span data-ttu-id="01da0-475">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-475">no</span></span>             | <span data-ttu-id="01da0-476">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-476">no</span></span>           |
| <span data-ttu-id="01da0-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="01da0-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="01da0-478">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-478">no</span></span>             | <span data-ttu-id="01da0-479">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-479">no</span></span>           |
| <span data-ttu-id="01da0-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="01da0-480">msdyn_hours</span></span>                                      | <span data-ttu-id="01da0-481">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-481">no</span></span>             | <span data-ttu-id="01da0-482">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-482">no</span></span>           |
| <span data-ttu-id="01da0-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="01da0-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="01da0-484">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-484">no</span></span>             | <span data-ttu-id="01da0-485">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-485">no</span></span>           |
| <span data-ttu-id="01da0-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="01da0-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="01da0-487">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-487">no</span></span>             | <span data-ttu-id="01da0-488">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-488">no</span></span>           |
| <span data-ttu-id="01da0-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="01da0-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="01da0-490">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-490">no</span></span>             | <span data-ttu-id="01da0-491">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-491">no</span></span>           |
| <span data-ttu-id="01da0-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="01da0-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="01da0-493">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-493">no</span></span>             | <span data-ttu-id="01da0-494">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-494">no</span></span>           |
| <span data-ttu-id="01da0-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="01da0-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="01da0-496">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-496">no</span></span>             | <span data-ttu-id="01da0-497">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-497">no</span></span>           |
| <span data-ttu-id="01da0-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="01da0-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="01da0-499">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-499">no</span></span>             | <span data-ttu-id="01da0-500">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-500">no</span></span>           |
| <span data-ttu-id="01da0-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="01da0-501">msdyn_start</span></span>                                      | <span data-ttu-id="01da0-502">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-502">no</span></span>             | <span data-ttu-id="01da0-503">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="01da0-504">Project</span><span class="sxs-lookup"><span data-stu-id="01da0-504">Project</span></span>

| <span data-ttu-id="01da0-505">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="01da0-505">**Logical name**</span></span>                       | <span data-ttu-id="01da0-506">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="01da0-506">**Can create**</span></span> | <span data-ttu-id="01da0-507">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="01da0-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="01da0-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="01da0-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="01da0-509">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-509">no</span></span>             | <span data-ttu-id="01da0-510">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-510">no</span></span>           |
| <span data-ttu-id="01da0-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="01da0-512">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-512">no</span></span>             | <span data-ttu-id="01da0-513">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-513">no</span></span>           |
| <span data-ttu-id="01da0-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="01da0-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="01da0-515">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-515">no</span></span>             | <span data-ttu-id="01da0-516">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-516">no</span></span>           |
| <span data-ttu-id="01da0-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="01da0-518">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-518">no</span></span>             | <span data-ttu-id="01da0-519">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-519">no</span></span>           |
| <span data-ttu-id="01da0-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="01da0-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="01da0-521">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-521">no</span></span>             | <span data-ttu-id="01da0-522">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-522">no</span></span>           |
| <span data-ttu-id="01da0-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="01da0-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="01da0-524">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-524">no</span></span>             | <span data-ttu-id="01da0-525">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-525">no</span></span>           |
| <span data-ttu-id="01da0-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="01da0-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="01da0-527">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-527">yes</span></span>            | <span data-ttu-id="01da0-528">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-528">no</span></span>           |
| <span data-ttu-id="01da0-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="01da0-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="01da0-530">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-530">yes</span></span>            | <span data-ttu-id="01da0-531">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-531">no</span></span>           |
| <span data-ttu-id="01da0-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="01da0-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="01da0-533">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-533">yes</span></span>            | <span data-ttu-id="01da0-534">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-534">no</span></span>           |
| <span data-ttu-id="01da0-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="01da0-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="01da0-536">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-536">no</span></span>             | <span data-ttu-id="01da0-537">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-537">no</span></span>           |
| <span data-ttu-id="01da0-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="01da0-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="01da0-539">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-539">no</span></span>             | <span data-ttu-id="01da0-540">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-540">no</span></span>           |
| <span data-ttu-id="01da0-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="01da0-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="01da0-542">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-542">no</span></span>             | <span data-ttu-id="01da0-543">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-543">no</span></span>           |
| <span data-ttu-id="01da0-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="01da0-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="01da0-545">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-545">no</span></span>             | <span data-ttu-id="01da0-546">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-546">no</span></span>           |
| <span data-ttu-id="01da0-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="01da0-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="01da0-548">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-548">no</span></span>             | <span data-ttu-id="01da0-549">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-549">no</span></span>           |
| <span data-ttu-id="01da0-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="01da0-550">msdyn_duration</span></span>                         | <span data-ttu-id="01da0-551">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-551">no</span></span>             | <span data-ttu-id="01da0-552">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-552">no</span></span>           |
| <span data-ttu-id="01da0-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="01da0-553">msdyn_effort</span></span>                           | <span data-ttu-id="01da0-554">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-554">no</span></span>             | <span data-ttu-id="01da0-555">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-555">no</span></span>           |
| <span data-ttu-id="01da0-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="01da0-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="01da0-557">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-557">no</span></span>             | <span data-ttu-id="01da0-558">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-558">no</span></span>           |
| <span data-ttu-id="01da0-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="01da0-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="01da0-560">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-560">no</span></span>             | <span data-ttu-id="01da0-561">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-561">no</span></span>           |
| <span data-ttu-id="01da0-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="01da0-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="01da0-563">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-563">no</span></span>             | <span data-ttu-id="01da0-564">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-564">no</span></span>           |
| <span data-ttu-id="01da0-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="01da0-565">msdyn_finish</span></span>                           | <span data-ttu-id="01da0-566">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-566">yes</span></span>            | <span data-ttu-id="01da0-567">áno</span><span class="sxs-lookup"><span data-stu-id="01da0-567">yes</span></span>          |
| <span data-ttu-id="01da0-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="01da0-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="01da0-569">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-569">no</span></span>             | <span data-ttu-id="01da0-570">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-570">no</span></span>           |
| <span data-ttu-id="01da0-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="01da0-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="01da0-572">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-572">no</span></span>             | <span data-ttu-id="01da0-573">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-573">no</span></span>           |
| <span data-ttu-id="01da0-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="01da0-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="01da0-575">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-575">no</span></span>             | <span data-ttu-id="01da0-576">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-576">no</span></span>           |
| <span data-ttu-id="01da0-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="01da0-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="01da0-578">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-578">no</span></span>             | <span data-ttu-id="01da0-579">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-579">no</span></span>           |
| <span data-ttu-id="01da0-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="01da0-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="01da0-581">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-581">no</span></span>             | <span data-ttu-id="01da0-582">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-582">no</span></span>           |
| <span data-ttu-id="01da0-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="01da0-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="01da0-584">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-584">no</span></span>             | <span data-ttu-id="01da0-585">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-585">no</span></span>           |
| <span data-ttu-id="01da0-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="01da0-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="01da0-587">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-587">no</span></span>             | <span data-ttu-id="01da0-588">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-588">no</span></span>           |
| <span data-ttu-id="01da0-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="01da0-590">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-590">no</span></span>             | <span data-ttu-id="01da0-591">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-591">no</span></span>           |
| <span data-ttu-id="01da0-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="01da0-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="01da0-593">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-593">no</span></span>             | <span data-ttu-id="01da0-594">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-594">no</span></span>           |
| <span data-ttu-id="01da0-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="01da0-596">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-596">no</span></span>             | <span data-ttu-id="01da0-597">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-597">no</span></span>           |
| <span data-ttu-id="01da0-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="01da0-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="01da0-599">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-599">no</span></span>             | <span data-ttu-id="01da0-600">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-600">no</span></span>           |
| <span data-ttu-id="01da0-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="01da0-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="01da0-602">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-602">no</span></span>             | <span data-ttu-id="01da0-603">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-603">no</span></span>           |
| <span data-ttu-id="01da0-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="01da0-604">msdyn_progress</span></span>                         | <span data-ttu-id="01da0-605">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-605">no</span></span>             | <span data-ttu-id="01da0-606">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-606">no</span></span>           |
| <span data-ttu-id="01da0-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="01da0-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="01da0-608">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-608">no</span></span>             | <span data-ttu-id="01da0-609">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-609">no</span></span>           |
| <span data-ttu-id="01da0-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="01da0-611">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-611">no</span></span>             | <span data-ttu-id="01da0-612">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-612">no</span></span>           |
| <span data-ttu-id="01da0-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="01da0-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="01da0-614">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-614">no</span></span>             | <span data-ttu-id="01da0-615">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-615">no</span></span>           |
| <span data-ttu-id="01da0-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="01da0-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="01da0-617">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-617">no</span></span>             | <span data-ttu-id="01da0-618">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-618">no</span></span>           |
| <span data-ttu-id="01da0-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="01da0-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="01da0-620">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-620">no</span></span>             | <span data-ttu-id="01da0-621">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-621">no</span></span>           |
| <span data-ttu-id="01da0-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="01da0-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="01da0-623">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-623">no</span></span>             | <span data-ttu-id="01da0-624">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-624">no</span></span>           |
| <span data-ttu-id="01da0-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="01da0-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="01da0-626">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-626">no</span></span>             | <span data-ttu-id="01da0-627">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-627">no</span></span>           |
| <span data-ttu-id="01da0-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="01da0-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="01da0-629">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-629">no</span></span>             | <span data-ttu-id="01da0-630">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-630">no</span></span>           |
| <span data-ttu-id="01da0-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="01da0-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="01da0-632">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-632">no</span></span>             | <span data-ttu-id="01da0-633">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-633">no</span></span>           |
| <span data-ttu-id="01da0-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="01da0-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="01da0-635">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-635">no</span></span>             | <span data-ttu-id="01da0-636">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-636">no</span></span>           |
| <span data-ttu-id="01da0-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="01da0-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="01da0-638">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-638">no</span></span>             | <span data-ttu-id="01da0-639">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-639">no</span></span>           |
| <span data-ttu-id="01da0-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="01da0-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="01da0-641">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-641">no</span></span>             | <span data-ttu-id="01da0-642">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-642">no</span></span>           |
| <span data-ttu-id="01da0-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="01da0-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="01da0-644">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-644">no</span></span>             | <span data-ttu-id="01da0-645">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-645">no</span></span>           |
| <span data-ttu-id="01da0-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="01da0-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="01da0-647">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-647">no</span></span>             | <span data-ttu-id="01da0-648">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-648">no</span></span>           |
| <span data-ttu-id="01da0-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="01da0-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="01da0-650">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-650">no</span></span>             | <span data-ttu-id="01da0-651">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-651">no</span></span>           |
| <span data-ttu-id="01da0-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="01da0-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="01da0-653">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-653">no</span></span>             | <span data-ttu-id="01da0-654">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-654">no</span></span>           |
| <span data-ttu-id="01da0-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="01da0-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="01da0-656">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-656">no</span></span>             | <span data-ttu-id="01da0-657">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-657">no</span></span>           |
| <span data-ttu-id="01da0-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="01da0-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="01da0-659">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-659">no</span></span>             | <span data-ttu-id="01da0-660">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-660">no</span></span>           |
| <span data-ttu-id="01da0-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="01da0-662">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-662">no</span></span>             | <span data-ttu-id="01da0-663">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-663">no</span></span>           |
| <span data-ttu-id="01da0-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="01da0-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="01da0-665">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-665">no</span></span>             | <span data-ttu-id="01da0-666">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-666">no</span></span>           |
| <span data-ttu-id="01da0-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="01da0-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="01da0-668">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-668">no</span></span>             | <span data-ttu-id="01da0-669">nie</span><span class="sxs-lookup"><span data-stu-id="01da0-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="01da0-670">Obmedzenia a známe problémy</span><span class="sxs-lookup"><span data-stu-id="01da0-670">Limitations and known issues</span></span>
<span data-ttu-id="01da0-671">Nasleduje zoznam obmedzení a známych problémov:</span><span class="sxs-lookup"><span data-stu-id="01da0-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="01da0-672">API pre plánovanie môžu používať iba **Používatelia s licenciou Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="01da0-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="01da0-673">Nemôžu ich používať:</span><span class="sxs-lookup"><span data-stu-id="01da0-673">They can't be used by:</span></span>
    - <span data-ttu-id="01da0-674">Používatelia aplikácie</span><span class="sxs-lookup"><span data-stu-id="01da0-674">Application users</span></span>
    - <span data-ttu-id="01da0-675">Systémoví používatelia</span><span class="sxs-lookup"><span data-stu-id="01da0-675">System users</span></span>
    - <span data-ttu-id="01da0-676">Používatelia integrácie</span><span class="sxs-lookup"><span data-stu-id="01da0-676">Integration users</span></span>
    - <span data-ttu-id="01da0-677">Ostatní používatelia, ktorí nemajú požadovanú licenciu</span><span class="sxs-lookup"><span data-stu-id="01da0-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="01da0-678">Každá množina **OperationSet** môže mať maximálne 100 operácií.</span><span class="sxs-lookup"><span data-stu-id="01da0-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="01da0-679">Každý používateľ môže mať maximálne 10 otvorených množín **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="01da0-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="01da0-680">Project Operations v súčasnosti podporuje v projekte celkovo maximálne 500 úloh.</span><span class="sxs-lookup"><span data-stu-id="01da0-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="01da0-681">Stav zlyhania množiny **OperationSet** a protokoly zlyhaní nie sú momentálne k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="01da0-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="01da0-682">Rozhrania API pre plánovanie sú vo verejnej verzii Preview.</span><span class="sxs-lookup"><span data-stu-id="01da0-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="01da0-683">Spoločnosť Microsoft nepodporuje použitie týchto rozhraní API v produkčnom prostredí.</span><span class="sxs-lookup"><span data-stu-id="01da0-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="01da0-684">Hranice projektov a úloh</span><span class="sxs-lookup"><span data-stu-id="01da0-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="01da0-685">Spracovanie chýb</span><span class="sxs-lookup"><span data-stu-id="01da0-685">Error handling</span></span>

   - <span data-ttu-id="01da0-686">Ak chcete skontrolovať chyby generované z množín operácií, prejdite na **Nastavenie**\> **Integrácia plánu** \> **Množiny operácií**.</span><span class="sxs-lookup"><span data-stu-id="01da0-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="01da0-687">Ak chcete skontrolovať chyby generované službou plánovania projektu, choďte na **Nastavenia** \> **Integrácia plánu** \> **Denníky chýb PSS**.</span><span class="sxs-lookup"><span data-stu-id="01da0-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="01da0-688">Vzorový scenár</span><span class="sxs-lookup"><span data-stu-id="01da0-688">Sample scenario</span></span>

<span data-ttu-id="01da0-689">V tomto scenári vytvoríte projekt, člena tímu, štyri úlohy a dve priradenia zdrojov.</span><span class="sxs-lookup"><span data-stu-id="01da0-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="01da0-690">Ďalej aktualizujete jednu úlohu, projekt, odstránite jednu úlohu, odstránite jedno priradenie zdroja a vytvoríte závislosť úlohy.</span><span class="sxs-lookup"><span data-stu-id="01da0-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="01da0-691">Ďalšie ukážky</span><span class="sxs-lookup"><span data-stu-id="01da0-691">Additional samples</span></span>

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
