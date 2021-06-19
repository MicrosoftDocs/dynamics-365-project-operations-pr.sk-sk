---
title: Používanie rozhraní API na plánovanie na vykonávanie operácií s entitami plánovania
description: Táto téma poskytuje informácie a ukážky používania rozhraní API na plánovanie.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116816"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="2c025-103">Používanie rozhraní API na plánovanie na vykonávanie operácií s entitami plánovania</span><span class="sxs-lookup"><span data-stu-id="2c025-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="2c025-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="2c025-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="2c025-105">Niektoré alebo všetky z funkcií uvádzaných v tejto téme sú k dispozícii ako súčasť vydania verzie Preview.</span><span class="sxs-lookup"><span data-stu-id="2c025-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="2c025-106">Obsah a funkcie sa môžu zmeniť.</span><span class="sxs-lookup"><span data-stu-id="2c025-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="2c025-107">Entity na plánovanie</span><span class="sxs-lookup"><span data-stu-id="2c025-107">Scheduling entities</span></span>

<span data-ttu-id="2c025-108">Rozhrania API na plánovanie poskytujú možnosť vykonávať operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania**.</span><span class="sxs-lookup"><span data-stu-id="2c025-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="2c025-109">Tieto entity sú spravované prostredníctvom modulu Plánovanie v Projekte pre web.</span><span class="sxs-lookup"><span data-stu-id="2c025-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="2c025-110">Operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania** boli obmedzené v skorších vydaniach Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2c025-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="2c025-111">Nasledujúca tabuľka poskytuje úplný zoznam **Entít na plánovanie**.</span><span class="sxs-lookup"><span data-stu-id="2c025-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="2c025-112">Názov entity</span><span class="sxs-lookup"><span data-stu-id="2c025-112">Entity name</span></span>  | <span data-ttu-id="2c025-113">Logický názov entity</span><span class="sxs-lookup"><span data-stu-id="2c025-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="2c025-114">Project</span><span class="sxs-lookup"><span data-stu-id="2c025-114">Project</span></span> | <span data-ttu-id="2c025-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="2c025-115">msdyn_project</span></span> |
| <span data-ttu-id="2c025-116">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="2c025-116">Project Task</span></span>  | <span data-ttu-id="2c025-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="2c025-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="2c025-118">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="2c025-118">Project Task Dependency</span></span>  | <span data-ttu-id="2c025-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="2c025-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="2c025-120">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="2c025-120">Resource Assignment</span></span> | <span data-ttu-id="2c025-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="2c025-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="2c025-122">Projektový kontajner</span><span class="sxs-lookup"><span data-stu-id="2c025-122">Project Bucket</span></span>  | <span data-ttu-id="2c025-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="2c025-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="2c025-124">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="2c025-124">Project Team Member</span></span> | <span data-ttu-id="2c025-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="2c025-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="2c025-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="2c025-126">OperationSet</span></span>

<span data-ttu-id="2c025-127">OperationSet je vzor jednotky práce, ktorý je možné použiť, keď sa v rámci transakcie musí spracovať niekoľko požiadaviek ovplyvňujúcich plán.</span><span class="sxs-lookup"><span data-stu-id="2c025-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="2c025-128">Rozhrania API pre plánovanie</span><span class="sxs-lookup"><span data-stu-id="2c025-128">Schedule APIs</span></span>

<span data-ttu-id="2c025-129">Nasleduje zoznam aktuálnych rozhraní API pre plánovanie.</span><span class="sxs-lookup"><span data-stu-id="2c025-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="2c025-130">**msdyn_CreateProjectV1**: Toto rozhranie API možno použiť na vytvorenie projektu.</span><span class="sxs-lookup"><span data-stu-id="2c025-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="2c025-131">Projekt a predvolený kontajner projektu sa vytvorí okamžite.</span><span class="sxs-lookup"><span data-stu-id="2c025-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="2c025-132">**msdyn_CreateTeamMemberV1**: Toto rozhranie API možno použiť na vytvorenie člena projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="2c025-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="2c025-133">Záznam o členovi tímu sa vytvorí okamžite.</span><span class="sxs-lookup"><span data-stu-id="2c025-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="2c025-134">**msdyn_CreateOperationSetV1**: Toto API možno použiť na naplánovanie niekoľkých požiadaviek, ktoré sa musia vykonať v rámci transakcie.</span><span class="sxs-lookup"><span data-stu-id="2c025-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="2c025-135">**msdyn_PSSCreateV1**: Toto API možno použiť na vytvorenie entity.</span><span class="sxs-lookup"><span data-stu-id="2c025-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="2c025-136">Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu vytvorenia.</span><span class="sxs-lookup"><span data-stu-id="2c025-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="2c025-137">**msdyn_PSSUpdateV1**: Toto API možno použiť na aktualizáciu entity.</span><span class="sxs-lookup"><span data-stu-id="2c025-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="2c025-138">Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="2c025-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="2c025-139">**msdyn_PSSDeleteV1**: Toto API možno použiť na odstránenie entity.</span><span class="sxs-lookup"><span data-stu-id="2c025-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="2c025-140">Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu odstránenia.</span><span class="sxs-lookup"><span data-stu-id="2c025-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="2c025-141">**msdyn_ExecuteOperationSetV1**: Toto API sa používa na vykonávanie všetkých operácií v rámci danej množiny operácií.</span><span class="sxs-lookup"><span data-stu-id="2c025-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="2c025-142">Používanie rozhraní API plánovania s množinou OperationSet</span><span class="sxs-lookup"><span data-stu-id="2c025-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="2c025-143">Pretože záznamy s **CreateProjectV1** a **CreateTeamMemberV1** sú vytvorené okamžite, tieto API nemôžu byť použité v **OperationSet** priamo.</span><span class="sxs-lookup"><span data-stu-id="2c025-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="2c025-144">Môžete však použiť API na vytvorenie potrebných záznamov, vytvorenie **OperationSet** a potom použiť tieto vopred vytvorené záznamy v **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="2c025-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="2c025-145">Podporované operácie</span><span class="sxs-lookup"><span data-stu-id="2c025-145">Supported operations</span></span>

| <span data-ttu-id="2c025-146">Entita na plánovanie</span><span class="sxs-lookup"><span data-stu-id="2c025-146">Scheduling entity</span></span> | <span data-ttu-id="2c025-147">Vytvoriť</span><span class="sxs-lookup"><span data-stu-id="2c025-147">Create</span></span> | <span data-ttu-id="2c025-148">Aktualizácia</span><span class="sxs-lookup"><span data-stu-id="2c025-148">Update</span></span> | <span data-ttu-id="2c025-149">Delete</span><span class="sxs-lookup"><span data-stu-id="2c025-149">Delete</span></span> | <span data-ttu-id="2c025-150">Dôležité aspekty</span><span class="sxs-lookup"><span data-stu-id="2c025-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="2c025-151">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="2c025-151">Project task</span></span> | <span data-ttu-id="2c025-152">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-152">Yes</span></span> | <span data-ttu-id="2c025-153">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-153">Yes</span></span> | <span data-ttu-id="2c025-154">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-154">Yes</span></span> | <span data-ttu-id="2c025-155">Nie je</span><span class="sxs-lookup"><span data-stu-id="2c025-155">None</span></span> |
| <span data-ttu-id="2c025-156">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="2c025-156">Project task dependency</span></span> | <span data-ttu-id="2c025-157">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-157">Yes</span></span> | <span data-ttu-id="2c025-158">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-158">Yes</span></span> | | <span data-ttu-id="2c025-159">Záznamy o závislosti od projektových úloh sa neaktualizujú.</span><span class="sxs-lookup"><span data-stu-id="2c025-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="2c025-160">Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam.</span><span class="sxs-lookup"><span data-stu-id="2c025-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="2c025-161">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="2c025-161">Resource assignment</span></span> | <span data-ttu-id="2c025-162">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-162">Yes</span></span> | <span data-ttu-id="2c025-163">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-163">Yes</span></span> | | <span data-ttu-id="2c025-164">Operácie s nasledujúcimi poľami nie sú podporované: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="2c025-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="2c025-165">Záznamy o priradení zdrojov sa neaktualizujú.</span><span class="sxs-lookup"><span data-stu-id="2c025-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="2c025-166">Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam.</span><span class="sxs-lookup"><span data-stu-id="2c025-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="2c025-167">Projektový kontajner</span><span class="sxs-lookup"><span data-stu-id="2c025-167">Project bucket</span></span> | <span data-ttu-id="2c025-168">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="2c025-168">N/A</span></span> | <span data-ttu-id="2c025-169">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="2c025-169">N/A</span></span> | <span data-ttu-id="2c025-170">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="2c025-170">N/A</span></span> | <span data-ttu-id="2c025-171">Predvolený kontajner sa vytvára pomocou API **CreateProjectV1**.</span><span class="sxs-lookup"><span data-stu-id="2c025-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="2c025-172">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="2c025-172">Project team member</span></span> | <span data-ttu-id="2c025-173">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-173">Yes</span></span> | <span data-ttu-id="2c025-174">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-174">Yes</span></span> | <span data-ttu-id="2c025-175">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-175">Yes</span></span> | <span data-ttu-id="2c025-176">Na operáciu vytvorenia použite API **CreateTeamMemberV1**.</span><span class="sxs-lookup"><span data-stu-id="2c025-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="2c025-177">Project</span><span class="sxs-lookup"><span data-stu-id="2c025-177">Project</span></span> | <span data-ttu-id="2c025-178">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-178">Yes</span></span> | <span data-ttu-id="2c025-179">Áno</span><span class="sxs-lookup"><span data-stu-id="2c025-179">Yes</span></span> | <span data-ttu-id="2c025-180">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="2c025-180">N/A</span></span> | <span data-ttu-id="2c025-181">Operácie s nasledujúcimi poľami nie sú podporované: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.</span><span class="sxs-lookup"><span data-stu-id="2c025-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="2c025-182">Tieto rozhrania API je možné volať s objektmi entít, ktoré obsahujú vlastné polia.</span><span class="sxs-lookup"><span data-stu-id="2c025-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="2c025-183">Toto ID vlastnosti je voliteľné.</span><span class="sxs-lookup"><span data-stu-id="2c025-183">The ID property is optional.</span></span> <span data-ttu-id="2c025-184">Ak je uvedené, systém sa ho pokúsi použiť a v prípade, že ho nemožno použiť, vyvolá výnimku.</span><span class="sxs-lookup"><span data-stu-id="2c025-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="2c025-185">Ak nie je uvedené, systém ho vygeneruje.</span><span class="sxs-lookup"><span data-stu-id="2c025-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="2c025-186">Obmedzené polia</span><span class="sxs-lookup"><span data-stu-id="2c025-186">Restricted fields</span></span>

<span data-ttu-id="2c025-187">Nasledujúce tabuľky definujú polia, ktoré sú obmedzené v rámci možností **Vytvoriť** a **Upraviť**.</span><span class="sxs-lookup"><span data-stu-id="2c025-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="2c025-188">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="2c025-188">Project task</span></span>

| <span data-ttu-id="2c025-189">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="2c025-189">**Logical name**</span></span>                       | <span data-ttu-id="2c025-190">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="2c025-190">**Can create**</span></span> | <span data-ttu-id="2c025-191">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="2c025-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="2c025-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="2c025-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="2c025-193">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-193">no</span></span>             | <span data-ttu-id="2c025-194">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-194">no</span></span>               |
| <span data-ttu-id="2c025-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="2c025-196">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-196">no</span></span>             | <span data-ttu-id="2c025-197">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-197">no</span></span>               |
| <span data-ttu-id="2c025-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="2c025-198">msdyn_actualend</span></span>                        | <span data-ttu-id="2c025-199">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-199">no</span></span>             | <span data-ttu-id="2c025-200">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-200">no</span></span>               |
| <span data-ttu-id="2c025-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="2c025-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="2c025-202">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-202">no</span></span>             | <span data-ttu-id="2c025-203">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-203">no</span></span>               |
| <span data-ttu-id="2c025-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="2c025-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="2c025-205">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-205">no</span></span>             | <span data-ttu-id="2c025-206">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-206">no</span></span>               |
| <span data-ttu-id="2c025-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="2c025-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="2c025-208">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-208">no</span></span>             | <span data-ttu-id="2c025-209">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-209">no</span></span>               |
| <span data-ttu-id="2c025-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="2c025-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="2c025-211">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-211">no</span></span>             | <span data-ttu-id="2c025-212">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-212">no</span></span>               |
| <span data-ttu-id="2c025-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="2c025-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="2c025-214">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-214">no</span></span>             | <span data-ttu-id="2c025-215">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-215">no</span></span>               |
| <span data-ttu-id="2c025-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="2c025-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="2c025-217">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-217">no</span></span>             | <span data-ttu-id="2c025-218">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-218">no</span></span>               |
| <span data-ttu-id="2c025-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2c025-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="2c025-220">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-220">no</span></span>             | <span data-ttu-id="2c025-221">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-221">no</span></span>               |
| <span data-ttu-id="2c025-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="2c025-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="2c025-223">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-223">no</span></span>             | <span data-ttu-id="2c025-224">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-224">no</span></span>               |
| <span data-ttu-id="2c025-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="2c025-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="2c025-226">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-226">no</span></span>             | <span data-ttu-id="2c025-227">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-227">no</span></span>               |
| <span data-ttu-id="2c025-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="2c025-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="2c025-229">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-229">no</span></span>             | <span data-ttu-id="2c025-230">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-230">no</span></span>               |
| <span data-ttu-id="2c025-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="2c025-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="2c025-232">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-232">no</span></span>             | <span data-ttu-id="2c025-233">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-233">no</span></span>               |
| <span data-ttu-id="2c025-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="2c025-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="2c025-235">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-235">no</span></span>             | <span data-ttu-id="2c025-236">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-236">no</span></span>               |
| <span data-ttu-id="2c025-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="2c025-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="2c025-238">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-238">no</span></span>             | <span data-ttu-id="2c025-239">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-239">no</span></span>               |
| <span data-ttu-id="2c025-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="2c025-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="2c025-241">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-241">no</span></span>             | <span data-ttu-id="2c025-242">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-242">no</span></span>               |
| <span data-ttu-id="2c025-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="2c025-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="2c025-244">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-244">no</span></span>             | <span data-ttu-id="2c025-245">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-245">no</span></span>               |
| <span data-ttu-id="2c025-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="2c025-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="2c025-247">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-247">no</span></span>             | <span data-ttu-id="2c025-248">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-248">no</span></span>               |
| <span data-ttu-id="2c025-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="2c025-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="2c025-250">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-250">no</span></span>             | <span data-ttu-id="2c025-251">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-251">no</span></span>               |
| <span data-ttu-id="2c025-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="2c025-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="2c025-253">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-253">no</span></span>             | <span data-ttu-id="2c025-254">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-254">no</span></span>               |
| <span data-ttu-id="2c025-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="2c025-256">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-256">no</span></span>             | <span data-ttu-id="2c025-257">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-257">no</span></span>               |
| <span data-ttu-id="2c025-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2c025-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="2c025-259">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-259">no</span></span>             | <span data-ttu-id="2c025-260">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-260">no</span></span>               |
| <span data-ttu-id="2c025-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="2c025-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="2c025-262">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-262">no</span></span>             | <span data-ttu-id="2c025-263">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-263">no</span></span>               |
| <span data-ttu-id="2c025-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="2c025-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="2c025-265">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-265">no</span></span>             | <span data-ttu-id="2c025-266">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-266">no</span></span>               |
| <span data-ttu-id="2c025-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="2c025-267">msdyn_progress</span></span>                         | <span data-ttu-id="2c025-268">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-268">no</span></span>             | <span data-ttu-id="2c025-269">nie (áno pre P4W)</span><span class="sxs-lookup"><span data-stu-id="2c025-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="2c025-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="2c025-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="2c025-271">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-271">no</span></span>             | <span data-ttu-id="2c025-272">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-272">no</span></span>               |
| <span data-ttu-id="2c025-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="2c025-274">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-274">no</span></span>             | <span data-ttu-id="2c025-275">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-275">no</span></span>               |
| <span data-ttu-id="2c025-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="2c025-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="2c025-277">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-277">no</span></span>             | <span data-ttu-id="2c025-278">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-278">no</span></span>               |
| <span data-ttu-id="2c025-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="2c025-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="2c025-280">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-280">no</span></span>             | <span data-ttu-id="2c025-281">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-281">no</span></span>               |
| <span data-ttu-id="2c025-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="2c025-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="2c025-283">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-283">no</span></span>             | <span data-ttu-id="2c025-284">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-284">no</span></span>               |
| <span data-ttu-id="2c025-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="2c025-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="2c025-286">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-286">no</span></span>             | <span data-ttu-id="2c025-287">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-287">no</span></span>               |
| <span data-ttu-id="2c025-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="2c025-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="2c025-289">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-289">no</span></span>             | <span data-ttu-id="2c025-290">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-290">no</span></span>               |
| <span data-ttu-id="2c025-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="2c025-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="2c025-292">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-292">no</span></span>             | <span data-ttu-id="2c025-293">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-293">no</span></span>               |
| <span data-ttu-id="2c025-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="2c025-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="2c025-295">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-295">no</span></span>             | <span data-ttu-id="2c025-296">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-296">no</span></span>               |
| <span data-ttu-id="2c025-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="2c025-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="2c025-298">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-298">no</span></span>             | <span data-ttu-id="2c025-299">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-299">no</span></span>               |
| <span data-ttu-id="2c025-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="2c025-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="2c025-301">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-301">no</span></span>             | <span data-ttu-id="2c025-302">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-302">no</span></span>               |
| <span data-ttu-id="2c025-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="2c025-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="2c025-304">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-304">no</span></span>             | <span data-ttu-id="2c025-305">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-305">no</span></span>               |
| <span data-ttu-id="2c025-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="2c025-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="2c025-307">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-307">no</span></span>             | <span data-ttu-id="2c025-308">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-308">no</span></span>               |
| <span data-ttu-id="2c025-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="2c025-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="2c025-310">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-310">no</span></span>             | <span data-ttu-id="2c025-311">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-311">no</span></span>               |
| <span data-ttu-id="2c025-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="2c025-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="2c025-313">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-313">no</span></span>             | <span data-ttu-id="2c025-314">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-314">no</span></span>               |
| <span data-ttu-id="2c025-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="2c025-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="2c025-316">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-316">no</span></span>             | <span data-ttu-id="2c025-317">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-317">no</span></span>               |
| <span data-ttu-id="2c025-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="2c025-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="2c025-319">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-319">no</span></span>             | <span data-ttu-id="2c025-320">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-320">no</span></span>               |
| <span data-ttu-id="2c025-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="2c025-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="2c025-322">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-322">no</span></span>             | <span data-ttu-id="2c025-323">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-323">no</span></span>               |
| <span data-ttu-id="2c025-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="2c025-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="2c025-325">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-325">no</span></span>             | <span data-ttu-id="2c025-326">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-326">no</span></span>               |
| <span data-ttu-id="2c025-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="2c025-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="2c025-328">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-328">no</span></span>             | <span data-ttu-id="2c025-329">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-329">no</span></span>               |
| <span data-ttu-id="2c025-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="2c025-330">msdyn_summary</span></span>                          | <span data-ttu-id="2c025-331">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-331">no</span></span>             | <span data-ttu-id="2c025-332">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-332">no</span></span>               |
| <span data-ttu-id="2c025-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="2c025-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="2c025-334">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-334">no</span></span>             | <span data-ttu-id="2c025-335">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-335">no</span></span>               |
| <span data-ttu-id="2c025-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="2c025-337">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-337">no</span></span>             | <span data-ttu-id="2c025-338">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="2c025-339">Závislosť projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="2c025-339">Project task dependency</span></span>

| <span data-ttu-id="2c025-340">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="2c025-340">**Logical name**</span></span>              | <span data-ttu-id="2c025-341">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="2c025-341">**Can create**</span></span> | <span data-ttu-id="2c025-342">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="2c025-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="2c025-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="2c025-343">msdyn_linktype</span></span>                | <span data-ttu-id="2c025-344">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-344">no</span></span>             | <span data-ttu-id="2c025-345">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-345">no</span></span>           |
| <span data-ttu-id="2c025-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="2c025-346">msdyn_linktypename</span></span>            | <span data-ttu-id="2c025-347">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-347">no</span></span>             | <span data-ttu-id="2c025-348">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-348">no</span></span>           |
| <span data-ttu-id="2c025-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="2c025-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="2c025-350">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-350">yes</span></span>            | <span data-ttu-id="2c025-351">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-351">no</span></span>           |
| <span data-ttu-id="2c025-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="2c025-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="2c025-353">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-353">yes</span></span>            | <span data-ttu-id="2c025-354">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-354">no</span></span>           |
| <span data-ttu-id="2c025-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="2c025-355">msdyn_project</span></span>                 | <span data-ttu-id="2c025-356">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-356">yes</span></span>            | <span data-ttu-id="2c025-357">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-357">no</span></span>           |
| <span data-ttu-id="2c025-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="2c025-358">msdyn_projectname</span></span>             | <span data-ttu-id="2c025-359">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-359">yes</span></span>            | <span data-ttu-id="2c025-360">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-360">no</span></span>           |
| <span data-ttu-id="2c025-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="2c025-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="2c025-362">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-362">yes</span></span>            | <span data-ttu-id="2c025-363">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-363">no</span></span>           |
| <span data-ttu-id="2c025-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="2c025-364">msdyn_successortask</span></span>           | <span data-ttu-id="2c025-365">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-365">yes</span></span>            | <span data-ttu-id="2c025-366">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-366">no</span></span>           |
| <span data-ttu-id="2c025-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="2c025-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="2c025-368">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-368">yes</span></span>            | <span data-ttu-id="2c025-369">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="2c025-370">Priradenie zdroja</span><span class="sxs-lookup"><span data-stu-id="2c025-370">Resource assignment</span></span>

| <span data-ttu-id="2c025-371">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="2c025-371">**Logical name**</span></span>             | <span data-ttu-id="2c025-372">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="2c025-372">**Can create**</span></span> | <span data-ttu-id="2c025-373">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="2c025-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="2c025-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="2c025-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="2c025-375">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-375">yes</span></span>            | <span data-ttu-id="2c025-376">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-376">no</span></span>           |
| <span data-ttu-id="2c025-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="2c025-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="2c025-378">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-378">yes</span></span>            | <span data-ttu-id="2c025-379">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-379">no</span></span>           |
| <span data-ttu-id="2c025-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="2c025-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="2c025-381">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-381">no</span></span>             | <span data-ttu-id="2c025-382">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-382">no</span></span>           |
| <span data-ttu-id="2c025-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="2c025-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="2c025-384">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-384">no</span></span>             | <span data-ttu-id="2c025-385">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-385">no</span></span>           |
| <span data-ttu-id="2c025-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="2c025-386">msdyn_committype</span></span>             | <span data-ttu-id="2c025-387">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-387">no</span></span>             | <span data-ttu-id="2c025-388">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-388">no</span></span>           |
| <span data-ttu-id="2c025-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="2c025-389">msdyn_committypename</span></span>         | <span data-ttu-id="2c025-390">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-390">no</span></span>             | <span data-ttu-id="2c025-391">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-391">no</span></span>           |
| <span data-ttu-id="2c025-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="2c025-392">msdyn_effort</span></span>                 | <span data-ttu-id="2c025-393">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-393">no</span></span>             | <span data-ttu-id="2c025-394">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-394">no</span></span>           |
| <span data-ttu-id="2c025-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2c025-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="2c025-396">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-396">no</span></span>             | <span data-ttu-id="2c025-397">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-397">no</span></span>           |
| <span data-ttu-id="2c025-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="2c025-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="2c025-399">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-399">no</span></span>             | <span data-ttu-id="2c025-400">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-400">no</span></span>           |
| <span data-ttu-id="2c025-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="2c025-401">msdyn_finish</span></span>                 | <span data-ttu-id="2c025-402">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-402">no</span></span>             | <span data-ttu-id="2c025-403">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-403">no</span></span>           |
| <span data-ttu-id="2c025-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="2c025-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="2c025-405">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-405">no</span></span>             | <span data-ttu-id="2c025-406">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-406">no</span></span>           |
| <span data-ttu-id="2c025-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="2c025-408">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-408">no</span></span>             | <span data-ttu-id="2c025-409">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-409">no</span></span>           |
| <span data-ttu-id="2c025-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="2c025-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="2c025-411">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-411">no</span></span>             | <span data-ttu-id="2c025-412">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-412">no</span></span>           |
| <span data-ttu-id="2c025-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2c025-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="2c025-414">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-414">no</span></span>             | <span data-ttu-id="2c025-415">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-415">no</span></span>           |
| <span data-ttu-id="2c025-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="2c025-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="2c025-417">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-417">no</span></span>             | <span data-ttu-id="2c025-418">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-418">no</span></span>           |
| <span data-ttu-id="2c025-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="2c025-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="2c025-420">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-420">no</span></span>             | <span data-ttu-id="2c025-421">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-421">no</span></span>           |
| <span data-ttu-id="2c025-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="2c025-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="2c025-423">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-423">no</span></span>             | <span data-ttu-id="2c025-424">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-424">no</span></span>           |
| <span data-ttu-id="2c025-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="2c025-425">msdyn_projectid</span></span>              | <span data-ttu-id="2c025-426">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-426">yes</span></span>            | <span data-ttu-id="2c025-427">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-427">no</span></span>           |
| <span data-ttu-id="2c025-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="2c025-428">msdyn_projectidname</span></span>          | <span data-ttu-id="2c025-429">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-429">no</span></span>             | <span data-ttu-id="2c025-430">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-430">no</span></span>           |
| <span data-ttu-id="2c025-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="2c025-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="2c025-432">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-432">no</span></span>             | <span data-ttu-id="2c025-433">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-433">no</span></span>           |
| <span data-ttu-id="2c025-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="2c025-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="2c025-435">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-435">no</span></span>             | <span data-ttu-id="2c025-436">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-436">no</span></span>           |
| <span data-ttu-id="2c025-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="2c025-437">msdyn_start</span></span>                  | <span data-ttu-id="2c025-438">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-438">no</span></span>             | <span data-ttu-id="2c025-439">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-439">no</span></span>           |
| <span data-ttu-id="2c025-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="2c025-440">msdyn_taskid</span></span>                 | <span data-ttu-id="2c025-441">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-441">no</span></span>             | <span data-ttu-id="2c025-442">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-442">no</span></span>           |
| <span data-ttu-id="2c025-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="2c025-443">msdyn_taskidname</span></span>             | <span data-ttu-id="2c025-444">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-444">no</span></span>             | <span data-ttu-id="2c025-445">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-445">no</span></span>           |
| <span data-ttu-id="2c025-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="2c025-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="2c025-447">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-447">no</span></span>             | <span data-ttu-id="2c025-448">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="2c025-449">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="2c025-449">Project team member</span></span>

| <span data-ttu-id="2c025-450">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="2c025-450">**Logical name**</span></span>                                 | <span data-ttu-id="2c025-451">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="2c025-451">**Can create**</span></span> | <span data-ttu-id="2c025-452">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="2c025-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="2c025-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="2c025-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="2c025-454">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-454">no</span></span>             | <span data-ttu-id="2c025-455">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-455">no</span></span>           |
| <span data-ttu-id="2c025-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="2c025-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="2c025-457">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-457">no</span></span>             | <span data-ttu-id="2c025-458">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-458">no</span></span>           |
| <span data-ttu-id="2c025-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="2c025-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="2c025-460">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-460">no</span></span>             | <span data-ttu-id="2c025-461">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-461">no</span></span>           |
| <span data-ttu-id="2c025-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="2c025-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="2c025-463">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-463">no</span></span>             | <span data-ttu-id="2c025-464">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-464">no</span></span>           |
| <span data-ttu-id="2c025-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="2c025-465">msdyn_effort</span></span>                                     | <span data-ttu-id="2c025-466">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-466">no</span></span>             | <span data-ttu-id="2c025-467">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-467">no</span></span>           |
| <span data-ttu-id="2c025-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2c025-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="2c025-469">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-469">no</span></span>             | <span data-ttu-id="2c025-470">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-470">no</span></span>           |
| <span data-ttu-id="2c025-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="2c025-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="2c025-472">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-472">no</span></span>             | <span data-ttu-id="2c025-473">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-473">no</span></span>           |
| <span data-ttu-id="2c025-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="2c025-474">msdyn_finish</span></span>                                     | <span data-ttu-id="2c025-475">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-475">no</span></span>             | <span data-ttu-id="2c025-476">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-476">no</span></span>           |
| <span data-ttu-id="2c025-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="2c025-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="2c025-478">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-478">no</span></span>             | <span data-ttu-id="2c025-479">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-479">no</span></span>           |
| <span data-ttu-id="2c025-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="2c025-480">msdyn_hours</span></span>                                      | <span data-ttu-id="2c025-481">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-481">no</span></span>             | <span data-ttu-id="2c025-482">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-482">no</span></span>           |
| <span data-ttu-id="2c025-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="2c025-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="2c025-484">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-484">no</span></span>             | <span data-ttu-id="2c025-485">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-485">no</span></span>           |
| <span data-ttu-id="2c025-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="2c025-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="2c025-487">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-487">no</span></span>             | <span data-ttu-id="2c025-488">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-488">no</span></span>           |
| <span data-ttu-id="2c025-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="2c025-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="2c025-490">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-490">no</span></span>             | <span data-ttu-id="2c025-491">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-491">no</span></span>           |
| <span data-ttu-id="2c025-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="2c025-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="2c025-493">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-493">no</span></span>             | <span data-ttu-id="2c025-494">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-494">no</span></span>           |
| <span data-ttu-id="2c025-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="2c025-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="2c025-496">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-496">no</span></span>             | <span data-ttu-id="2c025-497">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-497">no</span></span>           |
| <span data-ttu-id="2c025-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="2c025-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="2c025-499">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-499">no</span></span>             | <span data-ttu-id="2c025-500">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-500">no</span></span>           |
| <span data-ttu-id="2c025-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="2c025-501">msdyn_start</span></span>                                      | <span data-ttu-id="2c025-502">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-502">no</span></span>             | <span data-ttu-id="2c025-503">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="2c025-504">Project</span><span class="sxs-lookup"><span data-stu-id="2c025-504">Project</span></span>

| <span data-ttu-id="2c025-505">**Logický názov**</span><span class="sxs-lookup"><span data-stu-id="2c025-505">**Logical name**</span></span>                       | <span data-ttu-id="2c025-506">**Môže vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="2c025-506">**Can create**</span></span> | <span data-ttu-id="2c025-507">**Môže upravovať**</span><span class="sxs-lookup"><span data-stu-id="2c025-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="2c025-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="2c025-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="2c025-509">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-509">no</span></span>             | <span data-ttu-id="2c025-510">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-510">no</span></span>           |
| <span data-ttu-id="2c025-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="2c025-512">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-512">no</span></span>             | <span data-ttu-id="2c025-513">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-513">no</span></span>           |
| <span data-ttu-id="2c025-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="2c025-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="2c025-515">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-515">no</span></span>             | <span data-ttu-id="2c025-516">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-516">no</span></span>           |
| <span data-ttu-id="2c025-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="2c025-518">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-518">no</span></span>             | <span data-ttu-id="2c025-519">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-519">no</span></span>           |
| <span data-ttu-id="2c025-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="2c025-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="2c025-521">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-521">no</span></span>             | <span data-ttu-id="2c025-522">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-522">no</span></span>           |
| <span data-ttu-id="2c025-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="2c025-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="2c025-524">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-524">no</span></span>             | <span data-ttu-id="2c025-525">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-525">no</span></span>           |
| <span data-ttu-id="2c025-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="2c025-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="2c025-527">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-527">yes</span></span>            | <span data-ttu-id="2c025-528">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-528">no</span></span>           |
| <span data-ttu-id="2c025-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="2c025-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="2c025-530">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-530">yes</span></span>            | <span data-ttu-id="2c025-531">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-531">no</span></span>           |
| <span data-ttu-id="2c025-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="2c025-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="2c025-533">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-533">yes</span></span>            | <span data-ttu-id="2c025-534">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-534">no</span></span>           |
| <span data-ttu-id="2c025-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="2c025-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="2c025-536">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-536">no</span></span>             | <span data-ttu-id="2c025-537">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-537">no</span></span>           |
| <span data-ttu-id="2c025-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="2c025-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="2c025-539">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-539">no</span></span>             | <span data-ttu-id="2c025-540">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-540">no</span></span>           |
| <span data-ttu-id="2c025-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="2c025-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="2c025-542">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-542">no</span></span>             | <span data-ttu-id="2c025-543">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-543">no</span></span>           |
| <span data-ttu-id="2c025-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="2c025-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="2c025-545">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-545">no</span></span>             | <span data-ttu-id="2c025-546">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-546">no</span></span>           |
| <span data-ttu-id="2c025-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="2c025-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="2c025-548">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-548">no</span></span>             | <span data-ttu-id="2c025-549">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-549">no</span></span>           |
| <span data-ttu-id="2c025-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="2c025-550">msdyn_duration</span></span>                         | <span data-ttu-id="2c025-551">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-551">no</span></span>             | <span data-ttu-id="2c025-552">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-552">no</span></span>           |
| <span data-ttu-id="2c025-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="2c025-553">msdyn_effort</span></span>                           | <span data-ttu-id="2c025-554">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-554">no</span></span>             | <span data-ttu-id="2c025-555">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-555">no</span></span>           |
| <span data-ttu-id="2c025-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="2c025-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="2c025-557">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-557">no</span></span>             | <span data-ttu-id="2c025-558">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-558">no</span></span>           |
| <span data-ttu-id="2c025-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="2c025-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="2c025-560">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-560">no</span></span>             | <span data-ttu-id="2c025-561">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-561">no</span></span>           |
| <span data-ttu-id="2c025-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="2c025-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="2c025-563">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-563">no</span></span>             | <span data-ttu-id="2c025-564">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-564">no</span></span>           |
| <span data-ttu-id="2c025-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="2c025-565">msdyn_finish</span></span>                           | <span data-ttu-id="2c025-566">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-566">yes</span></span>            | <span data-ttu-id="2c025-567">áno</span><span class="sxs-lookup"><span data-stu-id="2c025-567">yes</span></span>          |
| <span data-ttu-id="2c025-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="2c025-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="2c025-569">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-569">no</span></span>             | <span data-ttu-id="2c025-570">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-570">no</span></span>           |
| <span data-ttu-id="2c025-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="2c025-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="2c025-572">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-572">no</span></span>             | <span data-ttu-id="2c025-573">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-573">no</span></span>           |
| <span data-ttu-id="2c025-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="2c025-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="2c025-575">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-575">no</span></span>             | <span data-ttu-id="2c025-576">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-576">no</span></span>           |
| <span data-ttu-id="2c025-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="2c025-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="2c025-578">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-578">no</span></span>             | <span data-ttu-id="2c025-579">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-579">no</span></span>           |
| <span data-ttu-id="2c025-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="2c025-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="2c025-581">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-581">no</span></span>             | <span data-ttu-id="2c025-582">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-582">no</span></span>           |
| <span data-ttu-id="2c025-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="2c025-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="2c025-584">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-584">no</span></span>             | <span data-ttu-id="2c025-585">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-585">no</span></span>           |
| <span data-ttu-id="2c025-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="2c025-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="2c025-587">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-587">no</span></span>             | <span data-ttu-id="2c025-588">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-588">no</span></span>           |
| <span data-ttu-id="2c025-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="2c025-590">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-590">no</span></span>             | <span data-ttu-id="2c025-591">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-591">no</span></span>           |
| <span data-ttu-id="2c025-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="2c025-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="2c025-593">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-593">no</span></span>             | <span data-ttu-id="2c025-594">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-594">no</span></span>           |
| <span data-ttu-id="2c025-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="2c025-596">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-596">no</span></span>             | <span data-ttu-id="2c025-597">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-597">no</span></span>           |
| <span data-ttu-id="2c025-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="2c025-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="2c025-599">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-599">no</span></span>             | <span data-ttu-id="2c025-600">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-600">no</span></span>           |
| <span data-ttu-id="2c025-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="2c025-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="2c025-602">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-602">no</span></span>             | <span data-ttu-id="2c025-603">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-603">no</span></span>           |
| <span data-ttu-id="2c025-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="2c025-604">msdyn_progress</span></span>                         | <span data-ttu-id="2c025-605">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-605">no</span></span>             | <span data-ttu-id="2c025-606">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-606">no</span></span>           |
| <span data-ttu-id="2c025-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="2c025-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="2c025-608">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-608">no</span></span>             | <span data-ttu-id="2c025-609">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-609">no</span></span>           |
| <span data-ttu-id="2c025-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="2c025-611">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-611">no</span></span>             | <span data-ttu-id="2c025-612">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-612">no</span></span>           |
| <span data-ttu-id="2c025-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="2c025-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="2c025-614">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-614">no</span></span>             | <span data-ttu-id="2c025-615">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-615">no</span></span>           |
| <span data-ttu-id="2c025-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="2c025-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="2c025-617">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-617">no</span></span>             | <span data-ttu-id="2c025-618">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-618">no</span></span>           |
| <span data-ttu-id="2c025-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="2c025-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="2c025-620">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-620">no</span></span>             | <span data-ttu-id="2c025-621">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-621">no</span></span>           |
| <span data-ttu-id="2c025-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="2c025-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="2c025-623">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-623">no</span></span>             | <span data-ttu-id="2c025-624">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-624">no</span></span>           |
| <span data-ttu-id="2c025-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="2c025-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="2c025-626">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-626">no</span></span>             | <span data-ttu-id="2c025-627">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-627">no</span></span>           |
| <span data-ttu-id="2c025-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="2c025-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="2c025-629">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-629">no</span></span>             | <span data-ttu-id="2c025-630">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-630">no</span></span>           |
| <span data-ttu-id="2c025-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="2c025-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="2c025-632">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-632">no</span></span>             | <span data-ttu-id="2c025-633">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-633">no</span></span>           |
| <span data-ttu-id="2c025-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="2c025-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="2c025-635">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-635">no</span></span>             | <span data-ttu-id="2c025-636">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-636">no</span></span>           |
| <span data-ttu-id="2c025-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="2c025-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="2c025-638">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-638">no</span></span>             | <span data-ttu-id="2c025-639">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-639">no</span></span>           |
| <span data-ttu-id="2c025-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="2c025-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="2c025-641">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-641">no</span></span>             | <span data-ttu-id="2c025-642">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-642">no</span></span>           |
| <span data-ttu-id="2c025-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="2c025-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="2c025-644">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-644">no</span></span>             | <span data-ttu-id="2c025-645">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-645">no</span></span>           |
| <span data-ttu-id="2c025-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="2c025-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="2c025-647">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-647">no</span></span>             | <span data-ttu-id="2c025-648">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-648">no</span></span>           |
| <span data-ttu-id="2c025-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="2c025-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="2c025-650">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-650">no</span></span>             | <span data-ttu-id="2c025-651">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-651">no</span></span>           |
| <span data-ttu-id="2c025-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="2c025-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="2c025-653">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-653">no</span></span>             | <span data-ttu-id="2c025-654">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-654">no</span></span>           |
| <span data-ttu-id="2c025-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="2c025-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="2c025-656">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-656">no</span></span>             | <span data-ttu-id="2c025-657">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-657">no</span></span>           |
| <span data-ttu-id="2c025-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="2c025-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="2c025-659">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-659">no</span></span>             | <span data-ttu-id="2c025-660">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-660">no</span></span>           |
| <span data-ttu-id="2c025-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="2c025-662">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-662">no</span></span>             | <span data-ttu-id="2c025-663">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-663">no</span></span>           |
| <span data-ttu-id="2c025-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="2c025-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="2c025-665">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-665">no</span></span>             | <span data-ttu-id="2c025-666">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-666">no</span></span>           |
| <span data-ttu-id="2c025-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="2c025-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="2c025-668">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-668">no</span></span>             | <span data-ttu-id="2c025-669">nie</span><span class="sxs-lookup"><span data-stu-id="2c025-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="2c025-670">Obmedzenia a známe problémy</span><span class="sxs-lookup"><span data-stu-id="2c025-670">Limitations and known issues</span></span>
<span data-ttu-id="2c025-671">Nasleduje zoznam obmedzení a známych problémov:</span><span class="sxs-lookup"><span data-stu-id="2c025-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="2c025-672">API pre plánovanie môžu používať iba **Používatelia s licenciou Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="2c025-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="2c025-673">Nemôžu ich používať:</span><span class="sxs-lookup"><span data-stu-id="2c025-673">They can't be used by:</span></span>
    - <span data-ttu-id="2c025-674">Používatelia aplikácie</span><span class="sxs-lookup"><span data-stu-id="2c025-674">Application users</span></span>
    - <span data-ttu-id="2c025-675">Systémoví používatelia</span><span class="sxs-lookup"><span data-stu-id="2c025-675">System users</span></span>
    - <span data-ttu-id="2c025-676">Používatelia integrácie</span><span class="sxs-lookup"><span data-stu-id="2c025-676">Integration users</span></span>
    - <span data-ttu-id="2c025-677">Ostatní používatelia, ktorí nemajú požadovanú licenciu</span><span class="sxs-lookup"><span data-stu-id="2c025-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="2c025-678">Každá množina **OperationSet** môže mať maximálne 100 operácií.</span><span class="sxs-lookup"><span data-stu-id="2c025-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="2c025-679">Každý používateľ môže mať maximálne 10 otvorených množín **OperationSets**.</span><span class="sxs-lookup"><span data-stu-id="2c025-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="2c025-680">Project Operations v súčasnosti podporuje v projekte celkovo maximálne 500 úloh.</span><span class="sxs-lookup"><span data-stu-id="2c025-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="2c025-681">Stav zlyhania množiny **OperationSet** a protokoly zlyhaní nie sú momentálne k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="2c025-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="2c025-682">Hranice projektov a úloh</span><span class="sxs-lookup"><span data-stu-id="2c025-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="2c025-683">Spracovanie chýb</span><span class="sxs-lookup"><span data-stu-id="2c025-683">Error handling</span></span>

   - <span data-ttu-id="2c025-684">Ak chcete skontrolovať chyby generované z množín operácií, prejdite na **Nastavenie**\> **Integrácia plánu** \> **Množiny operácií**.</span><span class="sxs-lookup"><span data-stu-id="2c025-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="2c025-685">Ak chcete skontrolovať chyby generované službou plánovania projektu, choďte na **Nastavenia** \> **Integrácia plánu** \> **Denníky chýb PSS**.</span><span class="sxs-lookup"><span data-stu-id="2c025-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="2c025-686">Vzorový scenár</span><span class="sxs-lookup"><span data-stu-id="2c025-686">Sample scenario</span></span>

<span data-ttu-id="2c025-687">V tomto scenári vytvoríte projekt, člena tímu, štyri úlohy a dve priradenia zdrojov.</span><span class="sxs-lookup"><span data-stu-id="2c025-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="2c025-688">Ďalej aktualizujete jednu úlohu, projekt, odstránite jednu úlohu, odstránite jedno priradenie zdroja a vytvoríte závislosť úlohy.</span><span class="sxs-lookup"><span data-stu-id="2c025-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="2c025-689">Ďalšie ukážky</span><span class="sxs-lookup"><span data-stu-id="2c025-689">Additional samples</span></span>

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
