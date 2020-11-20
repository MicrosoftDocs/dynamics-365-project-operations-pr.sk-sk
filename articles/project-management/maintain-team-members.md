---
title: Udržiavanie členov tímu
description: Táto téma poskytuje informácie o rezervovaní pomenovaných zdrojov pre projektové tímy a ich priradení k úlohám.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: abab21ff98481166517be0c74a2c14c36d5e9d1d
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131542"
---
# <a name="maintain-team-members"></a><span data-ttu-id="3db29-103">Udržiavanie členov tímu</span><span class="sxs-lookup"><span data-stu-id="3db29-103">Maintain team members</span></span>

<span data-ttu-id="3db29-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="3db29-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3db29-105">Môžete pridať pomenovaný zdroj do projektového tímu jeho rezerváciou priamo v tíme.</span><span class="sxs-lookup"><span data-stu-id="3db29-105">You can add a named resource to your project team by booking them directly to the team.</span></span>

1. <span data-ttu-id="3db29-106">V Dynamics 365 Project Operations prejdite na **Projekty** a vyberte otvorenie projektu, pre ktorý robíte rezerváciu.</span><span class="sxs-lookup"><span data-stu-id="3db29-106">In Dynamics 365 Project Operations, go to **Projects**, and select the open the project that you're booking for.</span></span>
2. <span data-ttu-id="3db29-107">Na stránke **Projekt** na karte **Tím** vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="3db29-107">On the **Project** page, on the **Team** tab, select **New**.</span></span> 
3. <span data-ttu-id="3db29-108">V dialógovom okne **Quick Create Project Team Member** vyberte rezervovateľný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3db29-108">In the **Quick Create Project Team Member** dialog box, select the bookable resource.</span></span> <span data-ttu-id="3db29-109">Pole **Rola** sa vyplní predvolenou úlohou prostriedku, ak má jeden priradený.</span><span class="sxs-lookup"><span data-stu-id="3db29-109">The **Role** field will populate with the resource's default role if they have one assigned.</span></span> <span data-ttu-id="3db29-110">Rolu môžete zmeniť.</span><span class="sxs-lookup"><span data-stu-id="3db29-110">You can change the role.</span></span> 
4. <span data-ttu-id="3db29-111">Vyberte dátumy od a do, kedy bude zdroj potrebný a vyberte spôsob pridelenia kapacity zdroja.</span><span class="sxs-lookup"><span data-stu-id="3db29-111">Select the from and to dates that the resource will be needed, and select the allocation method of the resource's capacity.</span></span> 
5. <span data-ttu-id="3db29-112">Ak chcete, aby bol člen tímu schvaľovateľ projektu, vyberte pole **Schvaľovateľ projektu** a vyberte **Áno**.</span><span class="sxs-lookup"><span data-stu-id="3db29-112">In the **Project Approver** field, select **Yes** if you want the team member to be a project approver.</span></span> <span data-ttu-id="3db29-113">Člen tímu môže schváliť odoslané časové a výdavkové záznamy pre tento projekt.</span><span class="sxs-lookup"><span data-stu-id="3db29-113">The team member can approve submitted time and expense entries for this project.</span></span> 
6. <span data-ttu-id="3db29-114">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3db29-114">Select **Save**.</span></span>

<span data-ttu-id="3db29-115">Teraz môžete priradiť rezervovaný zdroj k úlohám v projekte.</span><span class="sxs-lookup"><span data-stu-id="3db29-115">You can now assign the booked resource to tasks on the project.</span></span> <span data-ttu-id="3db29-116">Na stránke **Projekt**, na karte **Plán** priraďte úlohy k novému zdroju.</span><span class="sxs-lookup"><span data-stu-id="3db29-116">On the **Project** page, on the **Schedule** tab, assign tasks to the new resource.</span></span> <span data-ttu-id="3db29-117">Výber zdroja, ktorý sa spúšťa z poľa **Resources** v mriežke úloh, zobrazí členov tímu, ktorých môžete vybrať.</span><span class="sxs-lookup"><span data-stu-id="3db29-117">The resource picker that is launched from the **Resources** field in the task grid will show the team members that you can select.</span></span>


<span data-ttu-id="3db29-118">V Project Operations nie sú rezervácie zdrojov a priradenia úloh úzko spojené.</span><span class="sxs-lookup"><span data-stu-id="3db29-118">In Project Operations, resource bookings and task assignments aren't tightly coupled.</span></span> <span data-ttu-id="3db29-119">Keď použijete výber zdrojov v pláne, môžete priradiť úlohy členom tímu na viac hodín ako pokrývajú ich rezervácie projektu.</span><span class="sxs-lookup"><span data-stu-id="3db29-119">When you use the resource picker in the schedule, you can assign tasks to team members for more hours than their bookings cover on the project.</span></span>

<span data-ttu-id="3db29-120">Rozdiely medzi rezerváciami a úlohami členov tímu sú zobrazené na kartách **Tím** a **Vyrovnanie zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="3db29-120">The differences between team member bookings and assignments are shown on the **Team** and **Resource Reconciliation** tabs.</span></span> <span data-ttu-id="3db29-121">Môžete tiež vyrovnať rozdiely medzi rezerváciami a priradeniami zdrojov na podrobnejšej úrovni.</span><span class="sxs-lookup"><span data-stu-id="3db29-121">You can also reconcile the differences between bookings and assignments for resources at a more detailed level.</span></span>

<span data-ttu-id="3db29-122">Použite výber zdrojov na karte **Plán** k vyhľadaniu vybraných rezervovateľných zdrojov, ktoré nie súčasťou projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="3db29-122">Use the resource picker on the **Schedule** tab to search for and select bookable resources that are not already part of the project team.</span></span> <span data-ttu-id="3db29-123">Tieto zdroje sú uvedené vo výbere zdrojov ako **Ďalšie zdroje**.</span><span class="sxs-lookup"><span data-stu-id="3db29-123">These resources are shown in the resource picker as **Other Resources**.</span></span>

<span data-ttu-id="3db29-124">Keď urobíte výber, zdroj sa pridá do projektového tímu a priradí k úlohe, ale nie sú generované žiadne rezervácie.</span><span class="sxs-lookup"><span data-stu-id="3db29-124">When you make a selection, the resource is added to the project team and assigned to the task, but no bookings are generated.</span></span>

<span data-ttu-id="3db29-125">Môžete použiť **Reconciliation** na zväčšenie tabuľkovej rezervačnej schopnosti alebo **Schedule Board** na rezerváciu zdrojovej kapacity pre projekt.</span><span class="sxs-lookup"><span data-stu-id="3db29-125">You can use the **Reconciliation** tab’s extend booking capability or the **Schedule Board** to book the resource’s capacity to the project.</span></span>

<span data-ttu-id="3db29-126">Po tom, ako sa člen tímu rezervuje na váš projekt, môžete použiť **Spravovanie rezervácií** alebo **Tabuľu plánovania** priamo na spravovanie ich rezervácií.</span><span class="sxs-lookup"><span data-stu-id="3db29-126">After a team member is booked on your project, you can use **Maintain bookings** or the **Schedule Board** directly to manage their bookings.</span></span>
