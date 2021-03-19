---
title: Plány projektov
description: Táto téma poskytuje informácie o tom, ako vytvoriť plán.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
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
ms.openlocfilehash: 8f1a0b0ed610ade094546782a1fa517682a390e4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284016"
---
# <a name="project-schedules"></a><span data-ttu-id="def02-103">Plány projektov</span><span class="sxs-lookup"><span data-stu-id="def02-103">Project schedules</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="def02-104">Plán projektu komunikuje, aká práca sa musí dokončiť, ktoré zdroje budú vykonávať prácu, a časový rámec v ktorom práca musí byť dokončená.</span><span class="sxs-lookup"><span data-stu-id="def02-104">A project schedule communicates what work must be completed, which resources will do the work, and the timeframe that the work must be finished in.</span></span> <span data-ttu-id="def02-105">To odráža všetku prácu spojenú s dodaním projektu na čas.</span><span class="sxs-lookup"><span data-stu-id="def02-105">It reflects all the work that is associated with delivering the project on time.</span></span> <span data-ttu-id="def02-106">V Dynamics 365 Project Service Automation, môžete vytvoriť plán projektu tým, že rodelíte prácu na zvládnuteľné úlohy, odhad času, ktorý je potrebný na vykonanie každej úlohy, nastavenie závislostí úloh, nastavenie trvania úlohy, a odhad všeobecných zdrojov, ktoré budú robiť úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-106">In Dynamics 365 Project Service Automation, you create a project schedule by breaking the work down into manageable tasks, estimating the time that is required to do each task, setting task dependencies, setting task durations, and estimating the generic resources that will do the tasks.</span></span> <span data-ttu-id="def02-107">Plán projektu sa vytvorí na karte **plán** na stránke projektu.</span><span class="sxs-lookup"><span data-stu-id="def02-107">The project schedule is created on the **Schedule** tab of the project page.</span></span>
 
## <a name="tasks"></a><span data-ttu-id="def02-108">Úlohy</span><span class="sxs-lookup"><span data-stu-id="def02-108">Tasks</span></span>

<span data-ttu-id="def02-109">Prvým krokom pri vytváraní plánu projektu je rozdelenie na zvládnuteľné porcie.</span><span class="sxs-lookup"><span data-stu-id="def02-109">The first step in creating a project schedule is to break the work down into manageable portions.</span></span> <span data-ttu-id="def02-110">Plán v PSA podporuje nasledujúce funkcie:</span><span class="sxs-lookup"><span data-stu-id="def02-110">The schedule in PSA supports the following features:</span></span>

- <span data-ttu-id="def02-111">Koreňový uzol projektu</span><span class="sxs-lookup"><span data-stu-id="def02-111">Project root node</span></span>
- <span data-ttu-id="def02-112">Súhrn alebo zásobník úloh</span><span class="sxs-lookup"><span data-stu-id="def02-112">Summary or container tasks</span></span>
- <span data-ttu-id="def02-113">Úlohy listového uzla</span><span class="sxs-lookup"><span data-stu-id="def02-113">Leaf node tasks</span></span>

### <a name="project-root-node"></a><span data-ttu-id="def02-114">Koreňový uzol projektu</span><span class="sxs-lookup"><span data-stu-id="def02-114">Project root node</span></span>

<span data-ttu-id="def02-115">Koreňový uzol projektu je súhrnná úloha najvyššej úrovne projektu.</span><span class="sxs-lookup"><span data-stu-id="def02-115">The project root node is the top-level summary task for the project.</span></span> <span data-ttu-id="def02-116">Všetky ostatné úlohy projektu sú vytvorené pod ním.</span><span class="sxs-lookup"><span data-stu-id="def02-116">All other project tasks are created under it.</span></span> <span data-ttu-id="def02-117">Názov koreňového uzla je vždy nastavený na názov projektu.</span><span class="sxs-lookup"><span data-stu-id="def02-117">The name of the root node is always set to the project name.</span></span> <span data-ttu-id="def02-118">Úsilie, dátumy a trvanie koreňového uzla sú zosumarizované na základe hodnôt v hierarchii pod ním.</span><span class="sxs-lookup"><span data-stu-id="def02-118">The effort, dates, and duration of the root node are summarized based on the values in the hierarchy below it.</span></span> <span data-ttu-id="def02-119">Vlastnosti koreňového uzla nemôžete upraviť.</span><span class="sxs-lookup"><span data-stu-id="def02-119">You can't edit the properties of the root node.</span></span> <span data-ttu-id="def02-120">Koreňový uzol tiež nemôžete odstrániť.</span><span class="sxs-lookup"><span data-stu-id="def02-120">You also can't delete the root node.</span></span>

### <a name="summary-or-container-tasks"></a><span data-ttu-id="def02-121">Súhrn alebo zásobník úloh</span><span class="sxs-lookup"><span data-stu-id="def02-121">Summary or container tasks</span></span> 

<span data-ttu-id="def02-122">Súhrnné úlohy majú čiastkové úlohy alebo kontajnerové úlohy v rámci nich.</span><span class="sxs-lookup"><span data-stu-id="def02-122">Summary tasks have sub-tasks or container tasks under them.</span></span> <span data-ttu-id="def02-123">Nemajú na seba žiadne pracovné úsilie alebo náklady.</span><span class="sxs-lookup"><span data-stu-id="def02-123">They have no work effort or cost of their own.</span></span> <span data-ttu-id="def02-124">Namiesto toho ich pracovné úsilie a náklady sú súhrnom úsilia a nákladov na ich kontajnerové úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-124">Instead, their work effort and cost are a rollup of the work effort and cost of their container tasks.</span></span> <span data-ttu-id="def02-125">Počiatočný dátum súhrnnej úlohy je dátum začatia kontajnerovej úlohy a koncový dátum je dátum ukončenia kontajnerovej úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-125">The start date of the summary task is the start date of the container tasks, and the end date is the end date of the container tasks.</span></span> <span data-ttu-id="def02-126">Názov súhrnnej úlohy je možné upraviť, ale nie je možné upraviť vlastnosti plánovania (úsilie, dátumy a trvanie).</span><span class="sxs-lookup"><span data-stu-id="def02-126">The name of a summary task can be edited, but scheduling properties (effort, dates, and duration) can't be edited.</span></span> <span data-ttu-id="def02-127">Ak odstránite súhrnnú úlohu, odstránite aj všetky jej kontajnerové úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-127">If you delete a summary task, you also delete all its container tasks.</span></span>

### <a name="leaf-node-tasks"></a><span data-ttu-id="def02-128">Úlohy listového uzla</span><span class="sxs-lookup"><span data-stu-id="def02-128">Leaf node tasks</span></span>

<span data-ttu-id="def02-129">Úloha listového uzla predstavuje najpodrobnejšiu prácu na projekte.</span><span class="sxs-lookup"><span data-stu-id="def02-129">Leaf node tasks represent the most granular work on the project.</span></span> <span data-ttu-id="def02-130">Majú odhadnuté úsilie, zdroje, plánovaný dátum začatia a ukončenia a celkové trvanie.</span><span class="sxs-lookup"><span data-stu-id="def02-130">They have an estimated effort, resources, planned start and end dates, and a duration.</span></span>
 
## <a name="creating-a-task-hierarchy"></a><span data-ttu-id="def02-131">Vytvorenie hierarchie úloh</span><span class="sxs-lookup"><span data-stu-id="def02-131">Creating a task hierarchy</span></span>

<span data-ttu-id="def02-132">Môžte vytvoriť heirarchiu úloh pomocou nasledujúcich možností:</span><span class="sxs-lookup"><span data-stu-id="def02-132">You can create a task hierarchy by using the following options:</span></span>

- <span data-ttu-id="def02-133">Tlačidlo **pridať úlohu**</span><span class="sxs-lookup"><span data-stu-id="def02-133">**Add task** button</span></span>
- <span data-ttu-id="def02-134">Tlačidlo **znížiť úroveň úlohy**</span><span class="sxs-lookup"><span data-stu-id="def02-134">**Indent task** button</span></span>
- <span data-ttu-id="def02-135">Tlačidlo **zvýšiť úroveň úlohy**</span><span class="sxs-lookup"><span data-stu-id="def02-135">**Outdent task** button</span></span>
- <span data-ttu-id="def02-136">Tlačidlá **posunúť nahor** a **posunúť nadol**</span><span class="sxs-lookup"><span data-stu-id="def02-136">**Move up** and **Move down** buttons</span></span>
- <span data-ttu-id="def02-137">Klávesové skratky a zjednodušenie ovládania</span><span class="sxs-lookup"><span data-stu-id="def02-137">Accessibility and keyboard shortcuts</span></span>

### <a name="add-task"></a><span data-ttu-id="def02-138">Pridať úlohu</span><span class="sxs-lookup"><span data-stu-id="def02-138">Add task</span></span>

<span data-ttu-id="def02-139">Tlačidlo **pridať úlohu** umožňuje vytvoriť novú úlohu v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="def02-139">The **Add task** button lets you create a new task in the hierarchy.</span></span> <span data-ttu-id="def02-140">Ak nevyberiete pozíciu, úloha je vložená na koniec.</span><span class="sxs-lookup"><span data-stu-id="def02-140">If you don't select a position, the task is inserted at the end.</span></span> 

<span data-ttu-id="def02-141">Pre každú úlohu je priradené ID plánu.</span><span class="sxs-lookup"><span data-stu-id="def02-141">A schedule ID is assigned to every task.</span></span> <span data-ttu-id="def02-142">ID plánu predstavuje hĺbku a pozíciu úlohy v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="def02-142">The schedule ID represents the task's depth and position in the hierarchy.</span></span> <span data-ttu-id="def02-143">Používa prehľad číslovania.</span><span class="sxs-lookup"><span data-stu-id="def02-143">It uses outline numbering.</span></span> <span data-ttu-id="def02-144">Pre úlohy v prvej úrovni v rámci projektu koreňového uzla, sa požíva schéma číslovania 1, 2, 3, a tak ďalej.</span><span class="sxs-lookup"><span data-stu-id="def02-144">For tasks in the first level under the project root node, a numbering scheme of 1, 2, 3, and so on, is used.</span></span> <span data-ttu-id="def02-145">Pre úlohy pod prvou úrovňou v rámci projektu koreňového uzla, sa požíva schéma číslovania 1.1, 1.2, 1.3, a tak ďalej.</span><span class="sxs-lookup"><span data-stu-id="def02-145">For tasks under the first level, a numbering scheme of 1.1, 1.2, 1.3, and so on, is used.</span></span>

### <a name="indent-task"></a><span data-ttu-id="def02-146">Znížiť úroveň úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-146">Indent task</span></span>

<span data-ttu-id="def02-147">Keď je úroveň úlohy znížená, stane sa podradenou úlohou úlohe, ktorá je priamo nad ňou.</span><span class="sxs-lookup"><span data-stu-id="def02-147">When a task is indented, it becomes a child of the task that is directly above it.</span></span> <span data-ttu-id="def02-148">ID plánu úlohy sa potom prepočíta tak, že je založené na ID plánu svojho nového nadradeného a sleduje prehľad schémy číslovania.</span><span class="sxs-lookup"><span data-stu-id="def02-148">The schedule ID of the task is then recalculated so that it's based on the schedule ID of its new parent and follows the outline numbering scheme.</span></span> <span data-ttu-id="def02-149">Nadradená úloha je teraz súhrnná úloha alebo kontajnerová úlohu.</span><span class="sxs-lookup"><span data-stu-id="def02-149">The parent task is now a summary task or a container task.</span></span> <span data-ttu-id="def02-150">Preto sa stáva súhrnom jej podradených úloh.</span><span class="sxs-lookup"><span data-stu-id="def02-150">Therefore, it becomes a rollup of its child tasks.</span></span>

### <a name="outdent-task"></a><span data-ttu-id="def02-151">Znížiť úroveň úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-151">Outdent task</span></span> 

<span data-ttu-id="def02-152">Keď je úroveň úlohy znížená, táto už nie je podradená úloha úlohe, ktorá bola jej nadradenou úlohou.</span><span class="sxs-lookup"><span data-stu-id="def02-152">When a task is outdented, it's no longer a child of the task that was its parent.</span></span> <span data-ttu-id="def02-153">Potom sa prepočítajú ID plánu tak, aby odrážal aktualizovanú hĺbku a pozíciu úlohy v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="def02-153">The schedule ID is then recalculated so that it reflects the task's updated depth and position in the hierarchy.</span></span> <span data-ttu-id="def02-154">Úsilie, náklady a dátumy predchádzajúcej nadradenej úlohy sa prepočítajú tak, aby nezahŕňali túto úlohu.</span><span class="sxs-lookup"><span data-stu-id="def02-154">The effort, cost, and dates of the previous parent task are recalculated so that they don't include this task.</span></span>

### <a name="move-up-and-move-down"></a><span data-ttu-id="def02-155">Posun nahor a posun nadol.</span><span class="sxs-lookup"><span data-stu-id="def02-155">Move up and Move down</span></span> 

<span data-ttu-id="def02-156">Tlačidlá **posunúť nahor** a **posunúť nadol** zmenia pozíciu úlohy v nadradenej hierarchii.</span><span class="sxs-lookup"><span data-stu-id="def02-156">The **Move up** and **Move down** buttons change the position of a task within its parent hierarchy.</span></span> <span data-ttu-id="def02-157">Zmeny tohto typu neovplyvnia úsilie, náklady, dátumy alebo trvanie úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-157">Changes of this type don't affect the task's effort, cost, dates, or duration.</span></span> <span data-ttu-id="def02-158">Len ID plánu úlohy je ovplyvnené.</span><span class="sxs-lookup"><span data-stu-id="def02-158">Only the task's schedule ID is affected.</span></span> <span data-ttu-id="def02-159">Potom sa prepočíta ID plánu tak, aby odrážal novú pozíciu úlohy v zozname nadradených a podradených úloh.</span><span class="sxs-lookup"><span data-stu-id="def02-159">The schedule ID is recalculated so that it reflects the task's new position in the parent's list of child tasks.</span></span>

### <a name="accessibility-and-keyboard-shortcuts"></a><span data-ttu-id="def02-160">Klávesové skratky a zjednodušenie ovládania</span><span class="sxs-lookup"><span data-stu-id="def02-160">Accessibility and keyboard shortcuts</span></span>

<span data-ttu-id="def02-161">Mriežka **plánu** je plne prístupná a môže sa používať s čítačkami obrazovky, ako sú napríklad Narrator, JAWS alebo NVDA.</span><span class="sxs-lookup"><span data-stu-id="def02-161">The **Schedule** grid is fully accessible and can be used with screen readers such as Narrator, JAWS, or NVDA.</span></span> <span data-ttu-id="def02-162">Môžete prechádzať oblasti mriežky pomocou šípok (ako v Microsoft Excel), môžete použiť klávesu Tab na postúp cez interaktívne prvky UI, a môžete použiť šípku nadol, klávesu ENTER, alebo medzerník pre výber a vyvolanie rozbaľovacích ponúk.</span><span class="sxs-lookup"><span data-stu-id="def02-162">You can move through the grid area by using arrow keys (as in Microsoft Excel), you can use the Tab key to advance through the interactive UI elements, and you can use the Down arrow key, the Enter key, or the Spacebar to select and invoke the drop-down menus.</span></span> <span data-ttu-id="def02-163">Hlavičky stĺpcov sú tiež interaktívne.</span><span class="sxs-lookup"><span data-stu-id="def02-163">The column headers are also interactive.</span></span> <span data-ttu-id="def02-164">Môžete skryť a zobraziť stĺpce, pomocou klávesy Tab a kláves so šípkami prechádzať hlavičkami stĺpcov a použiť tlačidlá akcie na paneli s nástrojmi.</span><span class="sxs-lookup"><span data-stu-id="def02-164">You can hide and show columns, use the Tab key and arrow keys to move through the column headers, and use the action buttons on the toolbar.</span></span> <span data-ttu-id="def02-165">Okrem toho môžete použiť nasledujúce klávesové skratky:</span><span class="sxs-lookup"><span data-stu-id="def02-165">In addition, you can use the following keyboard shortcuts:</span></span>

- <span data-ttu-id="def02-166">**Obnoviť**: ALT+SHIFT+F5</span><span class="sxs-lookup"><span data-stu-id="def02-166">**Refresh**: ALT+SHIFT+F5</span></span>
- <span data-ttu-id="def02-167">**Pridať**: ALT+SHIFT+Insert</span><span class="sxs-lookup"><span data-stu-id="def02-167">**Add**: ALT+SHIFT+Insert</span></span>
- <span data-ttu-id="def02-168">**Odstrániť**: ALT+SHIFT+DELETE</span><span class="sxs-lookup"><span data-stu-id="def02-168">**Delete**: ALT+SHIFT+Delete</span></span>
- <span data-ttu-id="def02-169">**Posunúť nahor/nadol**: ALT+SHIFT+šípky nahor/nadol</span><span class="sxs-lookup"><span data-stu-id="def02-169">**Move up/down**: ALT+SHIFT+Up/Down arrows</span></span>
- <span data-ttu-id="def02-170">**Znížiť/Zvýšiť úroveň**: ALT_SHIFT+šípky vľavo/vpravo</span><span class="sxs-lookup"><span data-stu-id="def02-170">**Indent/Outdent**: ALT_SHIFT+Left/Right arrows</span></span>
- <span data-ttu-id="def02-171">**Rozbaliť/Zbaliť hierarchie**: ALT+SHIFT+plus/mínus tlačidlá</span><span class="sxs-lookup"><span data-stu-id="def02-171">**Expand/Collapse Hierarchies**: ALT+SHIFT+Plus/Minus keys</span></span>

## <a name="task-attributes"></a><span data-ttu-id="def02-172">Atribúty úlohy</span><span class="sxs-lookup"><span data-stu-id="def02-172">Task attributes</span></span>

<span data-ttu-id="def02-173">Názov úlohy popisuje prácu, ktorá sa musí dokončiť.</span><span class="sxs-lookup"><span data-stu-id="def02-173">A task's name describes the work that must be completed.</span></span> <span data-ttu-id="def02-174">V PSA, atribúty, ktoré sú priradené k úlohe opísať plán úlohy a jeho personálne požiadavky.</span><span class="sxs-lookup"><span data-stu-id="def02-174">In PSA, the attributes that are associated with a task describe the schedule of the task and its staffing requirements.</span></span>

> ![Atribúty úlohy](media/project-2.png)
 
### <a name="schedule-attributes"></a><span data-ttu-id="def02-176">Naplánovať atribúty</span><span class="sxs-lookup"><span data-stu-id="def02-176">Schedule attributes</span></span>

<span data-ttu-id="def02-177">Atribúty **Úsilie**, **dátum začiatku**, **dátum konca** a **trvanie** určujú plán úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-177">The **Effort**, **Start date**, **End date**, and **Duration** attributes define the schedule for the task.</span></span>

<span data-ttu-id="def02-178">Ďalšie atribúty plánu zahŕňajú:</span><span class="sxs-lookup"><span data-stu-id="def02-178">Additional schedule attributes include:</span></span>

- <span data-ttu-id="def02-179">**Hodiny úsilia**: zadajte odhad hodín, ktoré sú potrebné na dokončenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-179">**Effort hours**: Enter an estimate of the hours that are required to complete the task.</span></span> 
- <span data-ttu-id="def02-180">**Trvanie**: zadajte počet pracovných dní, ktoré sú potrebné na dokončenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-180">**Duration**: Specify the number of workdays that are required to complete the task.</span></span>
- <span data-ttu-id="def02-181">**ID plánu**: toto automaticky generované ID sa používa na objednávku úloh v hierarchii.</span><span class="sxs-lookup"><span data-stu-id="def02-181">**Schedule ID**: This automatically generated ID is used to order tasks in the hierarchy.</span></span> <span data-ttu-id="def02-182">Závislosti medzi úlohami riadia skutočné poradie, v ktorom sú úlohy spracované.</span><span class="sxs-lookup"><span data-stu-id="def02-182">Dependencies between the tasks manage the actual order in which the tasks are worked on.</span></span>
 
### <a name="staffing-attributes"></a><span data-ttu-id="def02-183">Personálne atribúty</span><span class="sxs-lookup"><span data-stu-id="def02-183">Staffing attributes</span></span>

<span data-ttu-id="def02-184">Personálne atribúty sú prístupné prostredníctvom poľa **zdroje** v pláne.</span><span class="sxs-lookup"><span data-stu-id="def02-184">Staffing attributes are accessed through the **Resources** field in the schedule.</span></span> <span data-ttu-id="def02-185">Môžete vyhľadať existujúci zdroj alebo kliknúť na **vytvoriť** a na paneli **rýchle vytvorenie** pridať člena projektového tímu ako nový zdroj.</span><span class="sxs-lookup"><span data-stu-id="def02-185">You can either search for an existing resource, or click **Create** and in the **Quick Create** pane, add a project team member as a new resource.</span></span>

<span data-ttu-id="def02-186">Polia **rola**, **zdrojová jednotka** a **názov pozície** sa používajú na popis personálnych požiadaviek na úlohu.</span><span class="sxs-lookup"><span data-stu-id="def02-186">The **Role**, **Resourcing Unit**, and **Position Name** fields are used to describe the staffing requirements for the task.</span></span> <span data-ttu-id="def02-187">Tieto personálne atribúty spolu s plánom úloh sa používajú na vyhľadanie dostupných zdrojov na vykonanie tejto úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-187">These staffing attributes together with the task schedule are used to find available resources to do this task.</span></span>

<span data-ttu-id="def02-188">**Rola** - zadajte typ zdroja, ktorý je potrebný na vykonanie úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-188">**Role** - Specify the type of resource that is required to do the task.</span></span>

<span data-ttu-id="def02-189">**Zdrojová jednotka** - zadajte jednotku, z ktorej by mali byť pridelené zdroje pre úlohu.</span><span class="sxs-lookup"><span data-stu-id="def02-189">**Resourcing unit** - Specify the unit that resources for the task should be assigned from.</span></span> <span data-ttu-id="def02-190">Tento atribút ovplyvňuje odhady nákladov a predaja na úlohy, ak sú náklady a fakturačná sadzba zdroja nastavené na zdrojové jednotky.</span><span class="sxs-lookup"><span data-stu-id="def02-190">This attribute affects the cost and sales estimate for the task if the cost and bill rate for the resource are set based on resourcing units.</span></span>

<span data-ttu-id="def02-191">**Názov pozície** – zadajte popisný názov pre všeobecný zdroj, ktorý slúži ako zástupný symbol pre zdroj, ktorý bude v konečnom dôsledku vykonávať prácu.</span><span class="sxs-lookup"><span data-stu-id="def02-191">**Position name** – Enter a friendly name for the generic resource that serves as a placeholder for the resource that will ultimately do the work.</span></span>

<span data-ttu-id="def02-192">Pole **zdroje** obsahuje názov pozície všeobecného zdroja alebo pomenovaného zdroja, keď sa našiel.</span><span class="sxs-lookup"><span data-stu-id="def02-192">The **Resources** field holds the position name of the generic resource or named resource when one is found.</span></span>

<span data-ttu-id="def02-193">Pole **Kategória** obsahuje hodnoty, ktoré označujú širší typ práce, do ktorej môže byť úloha zoskupená.</span><span class="sxs-lookup"><span data-stu-id="def02-193">The **Category** field holds the values that indicate a broader type of work that the task can be grouped into.</span></span> <span data-ttu-id="def02-194">Toto pole neovplyvňuje plánovanie ani personálne obsadenie.</span><span class="sxs-lookup"><span data-stu-id="def02-194">This field doesn't affect scheduling or staffing.</span></span> <span data-ttu-id="def02-195">Používa sa len na vykazovanie.</span><span class="sxs-lookup"><span data-stu-id="def02-195">It's used only for reporting.</span></span>

### <a name="task-dependencies"></a><span data-ttu-id="def02-196">Závislosti úloh</span><span class="sxs-lookup"><span data-stu-id="def02-196">Task dependencies</span></span> 

<span data-ttu-id="def02-197">Môžete použiť plán v PSA na vytvorenie predchodcu vzťahov medzi úlohami.</span><span class="sxs-lookup"><span data-stu-id="def02-197">You can use the schedule in PSA to create predecessor relationships between tasks.</span></span> <span data-ttu-id="def02-198">Pole **predchodcu** v časti **úlohy** preberá jednu alebo viacero hodnôt na označenie úloh, na ktorých je úloha závislá.</span><span class="sxs-lookup"><span data-stu-id="def02-198">The **Predecessor** field under **Tasks** takes one or more values to indicate the tasks that a task depends on.</span></span> <span data-ttu-id="def02-199">Keď sú hodnoty predchodcu priradené k úlohe, úloha môže začať iba ak sa dokončili všetky predchádzajúce úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-199">When predecessor values are assigned to a task, the task can start only after all the predecessor tasks have been completed.</span></span> <span data-ttu-id="def02-200">Z dôvodu závislosti, plánovaný počiatočný dátum úlohy sa obnoví na dátum po dokončení predchádzajúcich úloh.</span><span class="sxs-lookup"><span data-stu-id="def02-200">Because of the dependency, the planned start date of the task is reset to the date when the predecessor tasks are completed.</span></span>

<span data-ttu-id="def02-201">Režim úlohy nemá žiadny vplyv na aktualizácie, ktoré sú vykonané na počiatočných a koncových dátumoch predchádzajúcich/závislých úloh.</span><span class="sxs-lookup"><span data-stu-id="def02-201">The task mode has no effect on updates that are made to the start and end dates of predecessor/dependent tasks.</span></span>

## <a name="task-mode"></a><span data-ttu-id="def02-202">Režim úlohy</span><span class="sxs-lookup"><span data-stu-id="def02-202">Task mode</span></span> 

<span data-ttu-id="def02-203">Režim úlohy určuje plánovanie úloh listového uzla.</span><span class="sxs-lookup"><span data-stu-id="def02-203">The task mode determines the scheduling of leaf node tasks.</span></span> <span data-ttu-id="def02-204">PSA podporuje dva režimy pre každú úlohu: režim automatického plánovania a režim manuálneho plánovania.</span><span class="sxs-lookup"><span data-stu-id="def02-204">PSA supports two task modes for every task: automatic scheduling and manual scheduling.</span></span>

### <a name="auto-scheduling"></a><span data-ttu-id="def02-205">Automatické plánovanie</span><span class="sxs-lookup"><span data-stu-id="def02-205">Auto-scheduling</span></span> 
 
<span data-ttu-id="def02-206">Keď nastavíte režim úlohy na **automatické plánovanie**, systém plánovania úloh použije pravidlá plánovania na nasledovné atribúty úloh, čím sa určí plán úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-206">When task mode is set to **Automatically Scheduled** for a task, the task scheduling engine uses the scheduling rules on task attributes to determine the schedule for the task.</span></span>

#### <a name="scheduling-rules"></a><span data-ttu-id="def02-207">Pravidlá plánovania</span><span class="sxs-lookup"><span data-stu-id="def02-207">Scheduling rules</span></span>

<span data-ttu-id="def02-208">Ak nemá úloha listového uzla predchodcov, jej dátum začiatku je prednastavený na dátum plánovaného začiatku projektu.</span><span class="sxs-lookup"><span data-stu-id="def02-208">By default, if a leaf node task doesn't have predecessors, its start date is set to the project's scheduled start date.</span></span> <span data-ttu-id="def02-209">Trvanie úlohy listového uzla sa vždy vypočítava ako počet pracovných dní medzi dátumom začatia a skončenia.</span><span class="sxs-lookup"><span data-stu-id="def02-209">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="def02-210">Po automatickom naplánovaní úlohy bude systém plánovania sledovať tieto pravidlá:</span><span class="sxs-lookup"><span data-stu-id="def02-210">When a task is automatically scheduled, the scheduling engine follows these rules:</span></span>

- <span data-ttu-id="def02-211">Počiatočný a koncový dátum úlohy musí byť vždy pracovný deň v súlade s plánovacím kalendárom projektu</span><span class="sxs-lookup"><span data-stu-id="def02-211">The start and end dates of the task must be working days, according to the project's scheduling calendar.</span></span> 
- <span data-ttu-id="def02-212">Pre každú úlohu, ktorá má predchádzajúce úlohy, sa dátum začatia úlohy automaticky nastaví na dátum posledného ukončenia svojich predchodcov.</span><span class="sxs-lookup"><span data-stu-id="def02-212">For any task that has predecessor tasks, the start date is automatically set to the latest end date of its predecessors.</span></span>
- <span data-ttu-id="def02-213">Úsilie sa vypočíta pomocou tohto vzorca: počet ľudí × trvanie × hodiny v štandardnom pracovnom dni v kalendári projektu.</span><span class="sxs-lookup"><span data-stu-id="def02-213">Effort is calculated by using this formula: Number of people × Duration × Hours in a standard workday in the project calendar.</span></span>

### <a name="manual-scheduling"></a><span data-ttu-id="def02-214">Ručné plánovanie</span><span class="sxs-lookup"><span data-stu-id="def02-214">Manual scheduling</span></span>

<span data-ttu-id="def02-215">Ak pravidlá automatického plánovania nespĺňajú vaše požiadavky, môžete nastaviť režim úloh pre úlohu na **manuálne naplánované.**</span><span class="sxs-lookup"><span data-stu-id="def02-215">If the rules of automatic scheduling don't meet your requirements, you can set the task mode for the task to **Manually Scheduled**.</span></span> <span data-ttu-id="def02-216">Tým plánovací systém prestane vypočítavať hodnoty ostatných atribútov plánovania.</span><span class="sxs-lookup"><span data-stu-id="def02-216">This setting stops the scheduling engine from calculating the values of other scheduling attributes.</span></span> <span data-ttu-id="def02-217">Bez ohľadu na režim úloh, ak nastavíte predchodcov úloh, vždy ovplyvníte dátum začatia závislej úlohy.</span><span class="sxs-lookup"><span data-stu-id="def02-217">Regardless of the task mode, if you set predecessors on tasks, you always affect the dependent task's start date.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]