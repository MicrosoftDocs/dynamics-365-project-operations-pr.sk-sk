---
title: Naplánovať projekt so štruktúrou rozdelenia práce
description: Ako naplánovať projekt so štruktúrou rozdelenia práce v Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ca9b899c-7791-4990-b02e-cdff7f652621
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 003a1c543163b7ef1df1221d0b633a078e6619cf
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755634"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="33fc4-103">Naplánovať projekt so štruktúrou rozdelenia práce (Project Service)</span><span class="sxs-lookup"><span data-stu-id="33fc4-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="33fc4-104">Plán projektu komunikuje, akú prácu treba vykonať, ktoré zdroje budú vykonávať prácu, a časový rámec v ktorom práca musí byť dokončená.</span><span class="sxs-lookup"><span data-stu-id="33fc4-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="33fc4-105">Plán projektu odráža všetky práce spojené s realizáciu projektu na čas.</span><span class="sxs-lookup"><span data-stu-id="33fc4-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="33fc4-106">Jedným z prvých krokov vo fáze začatia projektu je prísť s plánom projektu.</span><span class="sxs-lookup"><span data-stu-id="33fc4-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="33fc4-107">Ak chcete vytvoriť plán projektu, musíte vytvoriť štruktúru pracovných rozpisov.</span><span class="sxs-lookup"><span data-stu-id="33fc4-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="33fc4-108">Vytvorte štruktúru projektu so štruktúrou rozdelenia prác, ktorá vám pomôže:</span><span class="sxs-lookup"><span data-stu-id="33fc4-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="33fc4-109">Rozobrať práce do konkrétnych úloh</span><span class="sxs-lookup"><span data-stu-id="33fc4-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="33fc4-110">Odhad času potrebného na dokončenie úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="33fc4-111">Určenie závislostí medzi úlohami a trvanie úloh</span><span class="sxs-lookup"><span data-stu-id="33fc4-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="33fc4-112">Určenie úloh na dokončenie každej úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="33fc4-113">Plán projektu v štruktúre rozdelenia práce má známy vzhľad a jeho súčasťou je interaktívny Ganttov graf.</span><span class="sxs-lookup"><span data-stu-id="33fc4-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="33fc4-114">Vytvárať štruktúru rozdelenia práce pre projekt</span><span class="sxs-lookup"><span data-stu-id="33fc4-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="33fc4-115">Vytvárať štruktúru rozdelenia práce na zastúpenie postupnosti úloh v projekte.</span><span class="sxs-lookup"><span data-stu-id="33fc4-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="33fc4-116">Štruktúra rozdelenia práce zahŕňa úlohy, požiadavky každej úlohy a informácie o výnosoch a nákladoch.</span><span class="sxs-lookup"><span data-stu-id="33fc4-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="33fc4-117">V štruktúre rozdelenie práce môžete pridať:</span><span class="sxs-lookup"><span data-stu-id="33fc4-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="33fc4-118">Poradie úloh v hierarchii</span><span class="sxs-lookup"><span data-stu-id="33fc4-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="33fc4-119">Ostatné úlohy, ktoré musia byť dokončené pred spustením úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="33fc4-120">Počiatočný dátum, koncový dátum a trvanie úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="33fc4-121">Počet hodín, ktoré sú potrebné pre úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="33fc4-122">Požadované zručnosti a vzdelanie každého pracovníka</span><span class="sxs-lookup"><span data-stu-id="33fc4-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="33fc4-123">Pracovníci, ktorí sú priradení k úlohe</span><span class="sxs-lookup"><span data-stu-id="33fc4-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="33fc4-124">Odhadované výnosy a náklady</span><span class="sxs-lookup"><span data-stu-id="33fc4-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="33fc4-125">Typ úloh</span><span class="sxs-lookup"><span data-stu-id="33fc4-125">Task types</span></span>  
<span data-ttu-id="33fc4-126">Pri vytváraní vašej štruktúry rozdelenia práce budete používať tieto druhy úloh:</span><span class="sxs-lookup"><span data-stu-id="33fc4-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="33fc4-127">**Koreňový uzol projektu**</span><span class="sxs-lookup"><span data-stu-id="33fc4-127">**Project root node**</span></span> | <span data-ttu-id="33fc4-128">Súhrn úloh najvyššej úrovne pre projekt.</span><span class="sxs-lookup"><span data-stu-id="33fc4-128">The top-level summary task for the project.</span></span> <span data-ttu-id="33fc4-129">Všetky ostatné úlohy projektu sú vytvorené pod ním.</span><span class="sxs-lookup"><span data-stu-id="33fc4-129">All other project tasks are created under it.</span></span> <span data-ttu-id="33fc4-130">Názov koreňovej úlohy je názov projektu.</span><span class="sxs-lookup"><span data-stu-id="33fc4-130">The name of the root task is the project name.</span></span> <span data-ttu-id="33fc4-131">Úsilie, dátumy a trvanie koreňového uzla vychádzajú z hodnôt v hierarchii pod ním.</span><span class="sxs-lookup"><span data-stu-id="33fc4-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="33fc4-132">Nemôžete upraviť vlastnosti koreňového uzla, ani koreňový uzol odstrániť.</span><span class="sxs-lookup"><span data-stu-id="33fc4-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="33fc4-133">**Súhrn alebo zásobník úloh**</span><span class="sxs-lookup"><span data-stu-id="33fc4-133">**Summary or container tasks**</span></span> | <span data-ttu-id="33fc4-134">Súhrnná úloha je úloha, ktorá má priradené čiastkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="33fc4-135">Súhrnná úloha nemá žiadne pracovné úsilie, ani vlastné náklady.</span><span class="sxs-lookup"><span data-stu-id="33fc4-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="33fc4-136">Jeho pracovného úsilia a náklady sú súhrnom jeho čiastkových úloh.</span><span class="sxs-lookup"><span data-stu-id="33fc4-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="33fc4-137">Môžete zmeniť názov súhrnnej úlohy, ale nie je možné zmeniť úsilie, dátumy alebo čas, pretože tie sa vypočítajú automaticky.</span><span class="sxs-lookup"><span data-stu-id="33fc4-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="33fc4-138">Odstránenie súhrnnej úlohy odstráni úlohu a všetkých jej čiastkové úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="33fc4-139">**Úlohy listového uzla**</span><span class="sxs-lookup"><span data-stu-id="33fc4-139">**Leaf node tasks**</span></span> | <span data-ttu-id="33fc4-140">Úloha listového uzla predstavuje najpodrobnejšie práce na projekte.</span><span class="sxs-lookup"><span data-stu-id="33fc4-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="33fc4-141">Má odhadnuté úsilie, plánovaný počet zdrojov, plánovaný dátum začatia a ukončenia a celkové trvanie.</span><span class="sxs-lookup"><span data-stu-id="33fc4-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="33fc4-142">Hierarchia úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-142">Task hierarchy</span></span>  
 <span data-ttu-id="33fc4-143">Pri vytváraní hierarchia úloh máte nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="33fc4-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="33fc4-144">**Pridať úlohu**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-144">**Add task**.</span></span>   <span data-ttu-id="33fc4-145">Úlohy môžete pridať na pozícii, ktorú si v hierarchii úlohy vyberiete.</span><span class="sxs-lookup"><span data-stu-id="33fc4-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="33fc4-146">Ak nevyberiete pozíciu, objaví sa na konci vašej novej úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="33fc4-147">**Zväčšiť odsadenie úlohy**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-147">**Indent task**.</span></span>   <span data-ttu-id="33fc4-148">Odsaďte úlohu, aby sa stala podriadenou úlohe, ktorá je priamo nad ňou.</span><span class="sxs-lookup"><span data-stu-id="33fc4-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="33fc4-149">**Zmenšiť odsadenie úlohy**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-149">**Outdent task**.</span></span>   <span data-ttu-id="33fc4-150">Zmenšiť odsadenie úlohy, aby už nebolo podriadenou úlohou svojej pôvodne nadradenej úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="33fc4-151">**Posunúť nahor a posunúť nadol**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-151">**Move up and Move down**.</span></span>   <span data-ttu-id="33fc4-152">Posúvajte úlohy nahor a nadol v hierarchii nadradenej úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="33fc4-153">Presúvanie úloh nahor alebo nadol, nemá vplyv na jeho úsilie, náklady, termíny, alebo trvanie.</span><span class="sxs-lookup"><span data-stu-id="33fc4-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="33fc4-154">Atribúty úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-154">Task attributes</span></span>  
 <span data-ttu-id="33fc4-155">Názov úlohy popisuje prácu, ktorú treba dokončiť.</span><span class="sxs-lookup"><span data-stu-id="33fc4-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="33fc4-156">Použite rôzne atribúty úloh na popísanie plánu a personálnych požiadaviek na úlohu.</span><span class="sxs-lookup"><span data-stu-id="33fc4-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="33fc4-157">Naplánovať atribúty</span><span class="sxs-lookup"><span data-stu-id="33fc4-157">Schedule attributes</span></span>

 - <span data-ttu-id="33fc4-158">Priraďte hodnoty do **hodín úsilie**, **počet zdrojov**, **dátum začatia**, **dátum skončenia** a **trvanie** na stanovenie plánu úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-158">Assign values to **Effort hours**, **Number of resources**, **Start date**, **End date**, and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="33fc4-159">**Úsilie** je odhad hodín, ktoré sú potrebné na dokončenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="33fc4-160">**Počet zdrojov** je odhad, ktorý projektový manažér použije v úlohe na čo najlepší plán.</span><span class="sxs-lookup"><span data-stu-id="33fc4-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="33fc4-161">**Trvanie** (v dňoch) udáva počet pracovných dní, koľko bude trvať dokončenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="33fc4-162">Personálne atribúty</span><span class="sxs-lookup"><span data-stu-id="33fc4-162">Staffing attributes</span></span>

 - <span data-ttu-id="33fc4-163">**Úloha**, **Organizačná jednotka zdroja**, **Počet zdrojov** a **Zdroje** popisujú personálne požiadavky úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-163">**Role**, **Resource organizational unit**, **Number of resources**, and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="33fc4-164">**Úloha** popisuje typ zdroja, ktorý je potrebný na vykonanie úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="33fc4-165">**Organizačná jednotka zdroj** označuje organizačnú jednotku, z ktorej by mal byť personálom obsadený zdroj úlohy. Ovplyvňuje to tiež odhad nákladov a predajov úlohy, pretože sa na to odkazuje pri odhadovaní jednotkovej predajnej ceny zdroja.</span><span class="sxs-lookup"><span data-stu-id="33fc4-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="33fc4-166">**Zdroje** má všeobecný prostriedok alebo prostriedok s názvom keď sa nájde.</span><span class="sxs-lookup"><span data-stu-id="33fc4-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="33fc4-167">Závislosti úloh</span><span class="sxs-lookup"><span data-stu-id="33fc4-167">Task dependencies</span></span>  
 <span data-ttu-id="33fc4-168">Môžete vytvoriť predchodcu vzťah jednej alebo viacerých úloh štruktúry rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="33fc4-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="33fc4-169">Môžete nastaviť jednu alebo viacero hodnôt v poli predchodcu úlohy na označenie úloh, ktoré sú závislé.</span><span class="sxs-lookup"><span data-stu-id="33fc4-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="33fc4-170">Keď priradíte hodnotu predchodcu úlohy, úloha môže začať iba ak sa dokončili všetky predchádzajúce úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="33fc4-171">Nastavenie tejto závislosti na úlohe bude mať za následok prepočet plánovaného dátum začatia úlohy ako najneskoršieho konca všetkých svojich predchodcov.</span><span class="sxs-lookup"><span data-stu-id="33fc4-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="33fc4-172">Predchodcov vplyv na plán nie sú obmedzované stanoveným režimom úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="33fc4-173">Režim úlohy</span><span class="sxs-lookup"><span data-stu-id="33fc4-173">Task mode</span></span>  
 <span data-ttu-id="33fc4-174">Režim úlohy je jedným z dôležitých faktorov, ktoré určujú plánovanie úloh listového uzla.</span><span class="sxs-lookup"><span data-stu-id="33fc4-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="33fc4-175">Existujú dva režimy pre každú úlohu: režim automatického plánovania a režim manuálneho plánovania.</span><span class="sxs-lookup"><span data-stu-id="33fc4-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="33fc4-176">**Automatické plánovanie**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-176">**Auto scheduling**.</span></span>   <span data-ttu-id="33fc4-177">Keď nastavíte režim úlohy na automatické plánovanie, systém plánovania úloh použije pravidlá plánovania na nasledovné atribúty úloh, čím sa určí plán úlohy:</span><span class="sxs-lookup"><span data-stu-id="33fc4-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="33fc4-178">Predchodcovia</span><span class="sxs-lookup"><span data-stu-id="33fc4-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="33fc4-179">Úsilie</span><span class="sxs-lookup"><span data-stu-id="33fc4-179">Effort</span></span>  
  
    -   <span data-ttu-id="33fc4-180">Počet zdrojov</span><span class="sxs-lookup"><span data-stu-id="33fc4-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="33fc4-181">počiatočný a koncový dátum,</span><span class="sxs-lookup"><span data-stu-id="33fc4-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="33fc4-182">**Moje pravidlá plánovania**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-182">**Scheduling rules**.</span></span>   <span data-ttu-id="33fc4-183">Dátum začiatku listového uzla úlohy nemá prednastavených predchodcov plánovaného počiatočného dátumu plánovania projektu.</span><span class="sxs-lookup"><span data-stu-id="33fc4-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="33fc4-184">Trvanie úlohy listového uzla sa vždy vypočítava ako počet pracovných dní medzi dátumom začatia a skončenia.</span><span class="sxs-lookup"><span data-stu-id="33fc4-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="33fc4-185">Po automatickom naplánovaní úlohy bude systém plánovania sledovať nižšie uvedené pravidlá:</span><span class="sxs-lookup"><span data-stu-id="33fc4-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="33fc4-186">Počiatočný a koncový dátum úlohy musí vždy byť pracovný deň v súlade s plánovacím kalendárom projektu</span><span class="sxs-lookup"><span data-stu-id="33fc4-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="33fc4-187">Dátum začatia úlohy, ktorá má predvolených predchodcov poslednému dátumu ukončenia svojich predchodcov</span><span class="sxs-lookup"><span data-stu-id="33fc4-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="33fc4-188">Úsilie = počet ľudí \* trvanie \* hodín v štandardný pracovný deň kalendára projektu</span><span class="sxs-lookup"><span data-stu-id="33fc4-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="33fc4-189">**Ručné plánovanie**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-189">**Manual scheduling**.</span></span>   <span data-ttu-id="33fc4-190">V niektorých prípadoch sa budete chcieť od týchto pravidiel odchýliť.</span><span class="sxs-lookup"><span data-stu-id="33fc4-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="33fc4-191">V týchto prípadoch môžete nastaviť režim úloh na manuálne naplánované úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="33fc4-192">Tým plánovací systém prestane vypočítavať hodnoty pre ostatné atribúty plánovania.</span><span class="sxs-lookup"><span data-stu-id="33fc4-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="33fc4-193">Nastavenie predchodcov úloh vždy ovplyvní dátum začatia závislej úlohy.</span><span class="sxs-lookup"><span data-stu-id="33fc4-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="33fc4-194">Vytvorenie štruktúry rozdelenia práce</span><span class="sxs-lookup"><span data-stu-id="33fc4-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="33fc4-195">Prejdite na **Project Service > Projekty**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="33fc4-196">Kliknite na projekt, na ktorom chcete pracovať.</span><span class="sxs-lookup"><span data-stu-id="33fc4-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="33fc4-197">Na paneli v hornej časti obrazovky zvoľte šípku ukazujúcu nadol vedľa názvu projektu a potom kliknite na Štruktúra rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="33fc4-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="33fc4-198">Ak chcete pridať úlohu, kliknite na **Pridať úlohu**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="33fc4-199">Vyplňte polia pre úlohu a potom kliknite na položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="33fc4-200">Pokračujte v pridávaní úloh, kým nebude štruktúra rozdelenia práce úplná.</span><span class="sxs-lookup"><span data-stu-id="33fc4-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="33fc4-201">Pri vytváraní vašej štruktúry rozdelenia práce, môžete vykonať nasledovné činnosti pri organizácii svojich úloh:</span><span class="sxs-lookup"><span data-stu-id="33fc4-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="33fc4-202">Vyberte úlohu a kliknite na tlačidlo **Zarážka** ju presuniete pod inú úlohu, alebo kliknite na zmenšenie odsadenia ju presuniete mimo úrovne.</span><span class="sxs-lookup"><span data-stu-id="33fc4-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="33fc4-203">Vyberte úlohu a kliknite na tlačidlo **Posunúť nahor** alebo **Posunúť nadol**, čím ju presuniete v zozname nadol alebo nahor.</span><span class="sxs-lookup"><span data-stu-id="33fc4-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="33fc4-204">Kliknite na tlačidlo **Skryť ganttov graf** skryjete ganttov graf. Kliknutím na **Zobraziť ganttov graf** ho znova zobrazíte.</span><span class="sxs-lookup"><span data-stu-id="33fc4-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="33fc4-205">Zvoľte rôzne obdobie času pre ganttov graf v časti **Časový rozsah**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="33fc4-206">Na pridanie rol, ktoré ste zadali do vašej štruktúry rozdelenia práce pre členov tímu projektu, kliknite na tlačidlo **Generovať projektový tím**.</span><span class="sxs-lookup"><span data-stu-id="33fc4-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="33fc4-207">Po skončení so zmenami kliknite na možnosť **Uložiť** v pravom spodnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="33fc4-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="33fc4-208">Pozrite si tiež</span><span class="sxs-lookup"><span data-stu-id="33fc4-208">See Also</span></span>  
 [<span data-ttu-id="33fc4-209">Príručka projektového manažéra</span><span class="sxs-lookup"><span data-stu-id="33fc4-209">Project manager guide</span></span>](../project-service/project-manager-guide.md)
