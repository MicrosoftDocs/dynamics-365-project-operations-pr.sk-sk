---
title: Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh
description: Táto téma poskytuje informácie o spôsobe rezervovania pomenovaných zdrojov pre projektové tímy a ich priradenia k úlohám.
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 11/28/2018
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
ms.openlocfilehash: defc92e701ae6baf9d54f41dca123a09ef834c35
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084483"
---
# <a name="book-named-bookable-resources-to-a-project-team-and-assign-tasks"></a><span data-ttu-id="78202-103">Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh</span><span class="sxs-lookup"><span data-stu-id="78202-103">Book named bookable resources to a project team and assign tasks</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="78202-104">Môžete pridať pomenovaný zdroj do projektového tímu jeho rezerváciou priamo do tímu.</span><span class="sxs-lookup"><span data-stu-id="78202-104">You can  add a named resource to your project team by booking them directly onto the team.</span></span> <span data-ttu-id="78202-105">Ak to chcete urobiť, postupujte podľa nasledujúcich krokov.</span><span class="sxs-lookup"><span data-stu-id="78202-105">To do this, complete the following steps.</span></span>

1. <span data-ttu-id="78202-106">V Project Service Automation, prejdite na **Projects** , a vyberte otvoriť projekt, pre ktorý robíte rezerváciu.</span><span class="sxs-lookup"><span data-stu-id="78202-106">In  Project Service Automation, go to **Projects** , and select the open the project that you are booking for.</span></span>
2. <span data-ttu-id="78202-107">Na stránke **Project** na karte **Team** kliknite na **New**.</span><span class="sxs-lookup"><span data-stu-id="78202-107">On the **Project** page, on the **Team** tab, click **New**.</span></span> 

![Pridanie člena tímu z karty tímu](media/RM-how-to-1.png)

3. <span data-ttu-id="78202-109">V dialógovom okne **Quick Create Project Team Member** vyberte rezervovateľný zdroj.</span><span class="sxs-lookup"><span data-stu-id="78202-109">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="78202-110">Pole **Rola** sa vyplní predvolenou úlohou prostriedku, ak má jeden priradený.</span><span class="sxs-lookup"><span data-stu-id="78202-110">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="78202-111">Môžete zmeniť rolu podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="78202-111">You can change the role if needed.</span></span> 
4. <span data-ttu-id="78202-112">Vyberte z a do dátumov, že zdroj bude potrebný a vyberte spôsob pridelenia kapacity zdroja.</span><span class="sxs-lookup"><span data-stu-id="78202-112">Select the from and to dates that the resource will be needed and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="78202-113">Ak chcete, aby bol člen tímu schvaľovateľ projektu, vyberte **Yes** v poli **Project Approver**.</span><span class="sxs-lookup"><span data-stu-id="78202-113">If you want the team member to be a project approver, select **Yes** in the **Project Approver** field.</span></span> <span data-ttu-id="78202-114">To bude znamenať, že člen tímu môže schváliť odoslané časové a výdavkové záznamy pre tento projekt.</span><span class="sxs-lookup"><span data-stu-id="78202-114">This will mean that the team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="78202-115">Kliknite na tlačidlo **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="78202-115">Click **Save**.</span></span>

![Pridanie člena tímu do formulára rýchleho vytvorenia](media/RM-how-to-2.png)


<span data-ttu-id="78202-117">Teraz môžete priradiť rezervovaný zdroj k úlohám v projekte.</span><span class="sxs-lookup"><span data-stu-id="78202-117">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="78202-118">Na stránke **Project** kliknite na kartu **Schedule** na priradenie úloh k novému zdroju.</span><span class="sxs-lookup"><span data-stu-id="78202-118">On the **Project** page, click the **Schedule** tab to assign tasks to the new resource.</span></span> <span data-ttu-id="78202-119">Výber zdroja, ktorý sa spúšťa z poľa **Resources** v mriežke úloh, zobrazí členov tímu, ktorých môžete vybrať.</span><span class="sxs-lookup"><span data-stu-id="78202-119">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>

![Priradenie člena tímu k úlohe na karte plánu](media/RM-how-to-3.png)

<span data-ttu-id="78202-121">Vo verzii 3 pre Project Service Automation (PSA), rezervované zdroje a priradenia úloh nie sú tesne spojené.</span><span class="sxs-lookup"><span data-stu-id="78202-121">In version 3 for Project Service Automation (PSA), resource bookings and task assignments are not tightly coupled.</span></span> <span data-ttu-id="78202-122">To znamená, že keď použijete výber zdrojov v pláne, môžete priradiť úlohy členom tímu na viac hodín ako pokrývajú ich rezervácie projektu.</span><span class="sxs-lookup"><span data-stu-id="78202-122">This means that when you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>
<span data-ttu-id="78202-123">Rozdiely medzi rezerváciami členov tímu a priradeniami môžete vidieť na karte **Team** alebo na karte **Resource Reconciliation**. Môžete tiež zosúladiť rozdiely medzi rezerváciami a priradeniami pre zdroje na podrobnejšej úrovni.</span><span class="sxs-lookup"><span data-stu-id="78202-123">You can see the differences between team member bookings and assignments on the **Team** tab or on the **Resource Reconciliation** tab. You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

![Tabuľka odsúhlasenia zdrojov](media/RM-how-to-4.png)

<span data-ttu-id="78202-125">Môžete tiež použiť výber zdrojov, na karte **Plán** k vyhľadaniu vybraných rezervovateľných zdrojov, ktoré nie súčasťou projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="78202-125">You can also use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="78202-126">Tieto sú uvedené vo výbere zdrojov ako **Other Resources**.</span><span class="sxs-lookup"><span data-stu-id="78202-126">These are shown in the resource picker as **Other Resources**.</span></span>

![Priradenie zdroja ktorý nie je členom tímu k úlohe](media/RM-how-to-5.png)

<span data-ttu-id="78202-128">Keď to urobíte, zdroj je pridaný do projektového tímu a priradený k úlohe, ale nie sú generované žiadne rezervácie.</span><span class="sxs-lookup"><span data-stu-id="78202-128">When you do this, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

![Člen tímu s úlohami a bez rezervácií](media/RM-how-to-6.png)

<span data-ttu-id="78202-130">Môžete použiť **Reconciliation** na zväčšenie tabuľkovej rezervačnej schopnosti alebo **Schedule Board** na rezerváciu zdrojovej kapacity pre projekt.</span><span class="sxs-lookup"><span data-stu-id="78202-130">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

![Rozšírenie rezervácií pre člena tímu na karte odsúhlasenie zdroja](media/RM-how-to-7.png)

<span data-ttu-id="78202-132">Po tom, ako sa člen tímu rezervuje na váš projekt, môžete použiť spravovanie rezervácií alebo nástenku plánovania priamo na spravovanie ich rezervácií.</span><span class="sxs-lookup"><span data-stu-id="78202-132">After a team member is booked on your project, you can use maintain bookings or use the Schedule Board directly to manage their bookings.</span></span>
