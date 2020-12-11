---
title: Zmeny správy zdrojov (Project Service Automation 3. x)
description: Táto téma poskytuje informácie o zmenách v oblasti správy zdrojov.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 5176d2c6b7b00d47d4aeb12f54bdb84d4b87304c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084555"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="a8db7-103">Zmeny správy zdrojov (Project Service Automation 3. x)</span><span class="sxs-lookup"><span data-stu-id="a8db7-103">Resource management changes (Project Service Automation 3.x)</span></span>

<span data-ttu-id="a8db7-104">Časti tejto témy poskytujú informácie o zmenách, ktoré boli vykonané v oblasti správy zdrojov Dynamics 365 Project Service Automation verzie 3. x.</span><span class="sxs-lookup"><span data-stu-id="a8db7-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="a8db7-105">Odhady projektu</span><span class="sxs-lookup"><span data-stu-id="a8db7-105">Project estimates</span></span>

<span data-ttu-id="a8db7-106">Namiesto toho, aby bol založený na entite **msdyn\_projecttask** ( **Projektová úloha** ), odhady projektu sú založené na entite **msdyn\_resourceassignment** ( **Priradenie zdroja** ).</span><span class="sxs-lookup"><span data-stu-id="a8db7-106">Instead of being based on the **msdyn\_projecttask** entity ( **Project Task** ), project estimates are based on the **msdyn\_resourceassignment** entity ( **Resource Assignment** ).</span></span> <span data-ttu-id="a8db7-107">Priradenia prostriedkov sa stali "zdrojom pravdy" pre plánovanie úloh a určovanie cien.</span><span class="sxs-lookup"><span data-stu-id="a8db7-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="a8db7-108">Riadkové úlohy</span><span class="sxs-lookup"><span data-stu-id="a8db7-108">Line tasks</span></span>

<span data-ttu-id="a8db7-109">V PSA 3.x sú úlohy v riadku zastarané (zastarané).</span><span class="sxs-lookup"><span data-stu-id="a8db7-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="a8db7-110">Úlohy teraz poukazujú na celú úlohu namiesto úloh riadkov.</span><span class="sxs-lookup"><span data-stu-id="a8db7-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="a8db7-111">Nasledujúci príklad ukazuje, ako úlohu, ktorá sa nazýva "Skúšobná úloha" je priradená členom tímu A a B v starších verziách PSA a PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="a8db7-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="a8db7-112">**Pred PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="a8db7-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="a8db7-113">Skúšobná úloha</span><span class="sxs-lookup"><span data-stu-id="a8db7-113">Test task</span></span>

        - <span data-ttu-id="a8db7-114">Skúšobná úloha – úloha riadka 1</span><span class="sxs-lookup"><span data-stu-id="a8db7-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="a8db7-115">Priradenie k A</span><span class="sxs-lookup"><span data-stu-id="a8db7-115">Assignment to A</span></span>

        - <span data-ttu-id="a8db7-116">Skúšobná úloha – úloha riadka 2</span><span class="sxs-lookup"><span data-stu-id="a8db7-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="a8db7-117">Priradenie k B</span><span class="sxs-lookup"><span data-stu-id="a8db7-117">Assignment to B</span></span>

- <span data-ttu-id="a8db7-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="a8db7-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="a8db7-119">Skúšobná úloha</span><span class="sxs-lookup"><span data-stu-id="a8db7-119">Test task</span></span>

        - <span data-ttu-id="a8db7-120">Priradenie k A</span><span class="sxs-lookup"><span data-stu-id="a8db7-120">Assignment to A</span></span>
        - <span data-ttu-id="a8db7-121">Priradenie k B</span><span class="sxs-lookup"><span data-stu-id="a8db7-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="a8db7-122">Nepriradené priradenie</span><span class="sxs-lookup"><span data-stu-id="a8db7-122">Unassigned assignment</span></span>

<span data-ttu-id="a8db7-123">V PSA 3.x, nepriradené nasadenie je priradenie, ktoré je priradené členov tímu **NULL** a zdroju **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a8db7-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="a8db7-124">Nepriradené nasadenia sa môžu vyskytnúť v niekoľkých prípadoch:</span><span class="sxs-lookup"><span data-stu-id="a8db7-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="a8db7-125">Ak bola úloha vytvorená, ale ešte nebola priradená žiadnemu členovi tímu, nepriradené nasadenie sa vždy vytvorí.</span><span class="sxs-lookup"><span data-stu-id="a8db7-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="a8db7-126">Ak sa odstránia všetci postupníci úlohy, nepriradené nasadenie je pre túto úlohu znova vytvorené.</span><span class="sxs-lookup"><span data-stu-id="a8db7-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="a8db7-127">Plánovanie polí v entite Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="a8db7-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="a8db7-128">Polia v entite **msdyn\_projecttask** boli zastarané alebo presunuté do entity **msdyn\_resourceassignment** , alebo sa na ne dnes odkazuje z entity **msdyn\_projectteam** ( **Člen projektového tímu** ).</span><span class="sxs-lookup"><span data-stu-id="a8db7-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity ( **Project Team Member** ).</span></span>

| <span data-ttu-id="a8db7-129">Zastarané pole v msdyn\_projecttask (Projektová úloha)</span><span class="sxs-lookup"><span data-stu-id="a8db7-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a8db7-130">Nové pole na msdyn\_resourceassignment (priradenie prostriedkov)</span><span class="sxs-lookup"><span data-stu-id="a8db7-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="a8db7-131">Komentár</span><span class="sxs-lookup"><span data-stu-id="a8db7-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="a8db7-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="a8db7-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="a8db7-133">Žiadne</span><span class="sxs-lookup"><span data-stu-id="a8db7-133">None</span></span> | |
| <span data-ttu-id="a8db7-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="a8db7-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="a8db7-135">Žiadne</span><span class="sxs-lookup"><span data-stu-id="a8db7-135">None</span></span> | |
| <span data-ttu-id="a8db7-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="a8db7-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="a8db7-137">Žiadne</span><span class="sxs-lookup"><span data-stu-id="a8db7-137">None</span></span> | |
| <span data-ttu-id="a8db7-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="a8db7-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="a8db7-139">Žiadne</span><span class="sxs-lookup"><span data-stu-id="a8db7-139">None</span></span> | |
| <span data-ttu-id="a8db7-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="a8db7-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="a8db7-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="a8db7-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="a8db7-142">Formát dátovej štruktúry zápisu objektov JavaScript (JSON), ktorý je uložený v poli, sa zmenil.</span><span class="sxs-lookup"><span data-stu-id="a8db7-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="a8db7-143">Naplánovať obrys</span><span class="sxs-lookup"><span data-stu-id="a8db7-143">Schedule contour</span></span>

<span data-ttu-id="a8db7-144">Obrys plánu sa ukladá do poľa **Plánovaná práca** ( **msdyn\_plannedwork** ) každej entity **Priradenie zdroja** ( **msdyn\_resourceassignment** ).</span><span class="sxs-lookup"><span data-stu-id="a8db7-144">The schedule contour is stored in the **Planned Work** field ( **msdyn\_plannedwork** ) of each **Resource Assignment** entity ( **msdyn\_resourceassignment** ).</span></span>

### <a name="structure"></a><span data-ttu-id="a8db7-145">Štruktúra</span><span class="sxs-lookup"><span data-stu-id="a8db7-145">Structure</span></span>

<span data-ttu-id="a8db7-146">Nová štruktúra obrysu plánu pozostáva z flexibilných časových plátkov, ktoré sú definované pre každý deň plánu.</span><span class="sxs-lookup"><span data-stu-id="a8db7-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="a8db7-147">Každý časový plátok má nasledujúce vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="a8db7-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="a8db7-148">**Začiatok** – Ide o začiatok pracovného času na deň podľa kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="a8db7-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="a8db7-149">**Koniec** – Ide o koniec pracovného času na deň podľa kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="a8db7-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="a8db7-150">**Hodiny** – Počet hodín, ktoré sú priradené v deň.</span><span class="sxs-lookup"><span data-stu-id="a8db7-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="a8db7-151">**Príklad**</span><span class="sxs-lookup"><span data-stu-id="a8db7-151">**Example**</span></span>

<span data-ttu-id="a8db7-152">Tento príklad používa kalendár projektu, kde pracovný deň je od 9 hodín do 5 hodín v časovom pásme UTC-8.</span><span class="sxs-lookup"><span data-stu-id="a8db7-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="a8db7-153">Automatické plánovanie a manuálne plánovanie</span><span class="sxs-lookup"><span data-stu-id="a8db7-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="a8db7-154">Ak je úloha automaticky naplánovaná, hodiny sú načítané dopredu a trvanie úlohy môže byť znížené.</span><span class="sxs-lookup"><span data-stu-id="a8db7-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="a8db7-155">**Príklad**</span><span class="sxs-lookup"><span data-stu-id="a8db7-155">**Example**</span></span>

<span data-ttu-id="a8db7-156">Nasledujúca úloha je automaticky naplánovaná na 18 hodín počas troch dní (december 3, 2018 až december 5, 2018).</span><span class="sxs-lookup"><span data-stu-id="a8db7-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="a8db7-157">Ak je úloha manuálne naplánovaná, hodiny sú rovnomerne rozdelené do všetkých dátumov.</span><span class="sxs-lookup"><span data-stu-id="a8db7-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="a8db7-158">**Príklad**</span><span class="sxs-lookup"><span data-stu-id="a8db7-158">**Example**</span></span>

<span data-ttu-id="a8db7-159">Nasledujúca úloha je manuálne naplánovaná na 18 hodín počas troch dní (december 3, 2018 až december 5, 2018).</span><span class="sxs-lookup"><span data-stu-id="a8db7-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="a8db7-160">Jednotka priradenia</span><span class="sxs-lookup"><span data-stu-id="a8db7-160">Assignment unit</span></span>

<span data-ttu-id="a8db7-161">Jednotka priradenia bola zastaraná v PSA 3.x.</span><span class="sxs-lookup"><span data-stu-id="a8db7-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="a8db7-162">Úloha úsilia hodín je teraz rovnomerne rozdelená, na deň, medzi všetky pridelené zdroje.</span><span class="sxs-lookup"><span data-stu-id="a8db7-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="a8db7-163">**Príklad**</span><span class="sxs-lookup"><span data-stu-id="a8db7-163">**Example**</span></span>

<span data-ttu-id="a8db7-164">V tomto príklade je úloha priradená k dvom prostriedkom a je automaticky naplánovaná na 36 hodín počas troch dní (3. decembra 2018 až 5. decembra, 2018).</span><span class="sxs-lookup"><span data-stu-id="a8db7-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="a8db7-165">Priradenie 1:</span><span class="sxs-lookup"><span data-stu-id="a8db7-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="a8db7-166">Priradenie 2:</span><span class="sxs-lookup"><span data-stu-id="a8db7-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="a8db7-167">Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="a8db7-167">Pricing dimensions</span></span>

<span data-ttu-id="a8db7-168">V PSA 3.x, dimenzie týkajúce sa zdroja (napríklad **Rola** a **Organizačná jednotka** ) boli odstránené z entity **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="a8db7-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit** ) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="a8db7-169">Tieto polia je teraz možné načítať z príslušného člena projektového tímu **(msdyn\_projectteam** ) priradenia prostriedkov ( **msdyn\_resourceassignment** ) pri vygenerovaný projektových odhadov.</span><span class="sxs-lookup"><span data-stu-id="a8db7-169">These fields can now be retrieved from the corresponding project team member ( **msdyn\_projectteam** ) of the resource assignment ( **msdyn\_resourceassignment** ) when project estimates are generated.</span></span> <span data-ttu-id="a8db7-170">Nové pole **msdyn\_organizationalunit** bolo pridané do entity **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="a8db7-170">A new field, **msdyn\_organizationalunit** , has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="a8db7-171">Zastarané pole v msdyn\_projecttask (Projektová úloha)</span><span class="sxs-lookup"><span data-stu-id="a8db7-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a8db7-172">Pole z msdyn\_projectteam (člen projektového tímu), ktoré sa používa namiesto</span><span class="sxs-lookup"><span data-stu-id="a8db7-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="a8db7-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a8db7-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="a8db7-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="a8db7-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="a8db7-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="a8db7-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="a8db7-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="a8db7-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="a8db7-177">Kontúry</span><span class="sxs-lookup"><span data-stu-id="a8db7-177">Contours</span></span>

<span data-ttu-id="a8db7-178">Ceny a odhad obrysy polia boli zastarané v entite **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="a8db7-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="a8db7-179">Boli presunuté do entity **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="a8db7-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="a8db7-180">Zastarané pole v msdyn\_projecttask (Projektová úloha)</span><span class="sxs-lookup"><span data-stu-id="a8db7-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="a8db7-181">Nové pole na msdyn\_resourceassignment (priradenie prostriedkov)</span><span class="sxs-lookup"><span data-stu-id="a8db7-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="a8db7-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="a8db7-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="a8db7-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="a8db7-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="a8db7-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="a8db7-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="a8db7-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="a8db7-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="a8db7-186">Nasledovné polia boli pridané do entity **msdyn\_resourceassignment** :</span><span class="sxs-lookup"><span data-stu-id="a8db7-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="a8db7-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a8db7-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="a8db7-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a8db7-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="a8db7-189">Tieto polia plánované, skutočné a zostávajúce náklady a predaja sa nezmenia na entitu **msdyn\_projecttask** :</span><span class="sxs-lookup"><span data-stu-id="a8db7-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="a8db7-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="a8db7-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="a8db7-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="a8db7-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="a8db7-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="a8db7-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="a8db7-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="a8db7-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="a8db7-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="a8db7-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="a8db7-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="a8db7-195">msdyn\_remainingsales</span></span>