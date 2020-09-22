---
title: Synchronizácia projektových úloh priamo z Project Service Automation do Finance and Operations
description: Táto téma popisuje šablónu a základnú úlohu, ktoré sa používajú na synchronizáciu projektových úloh priamo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755650"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="91fca-103">Synchronizácia projektových úloh priamo z Project Service Automation do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="91fca-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="91fca-104">Táto téma popisuje šablónu a základnú úlohu, ktoré sa používajú na synchronizáciu projektových úloh priamo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="91fca-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="91fca-105">Integrácia projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií sú k dispozícii vo verzii 8.0.</span><span class="sxs-lookup"><span data-stu-id="91fca-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="91fca-106">Ak používate Enterprise Edition 7.3.0, po inštalácii KB 4132657 a KB 4132660 budete môcť tieto šablóny použiť na integráciu projektových úloh, kategórií transakcií výdavkov, odhadov hodín, odhadov výdavkov a skutočných údajov a na nakonfigurovať blokovanie funkcií.</span><span class="sxs-lookup"><span data-stu-id="91fca-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="91fca-107">Ak musíte resetovať účtovné prerozdelenie, odporúčame vám nainštalovať si aj KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="91fca-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="91fca-108">Integrácia skutočných hodnôt je k dispozícii vo verzii 8.0.1 alebo novšej.</span><span class="sxs-lookup"><span data-stu-id="91fca-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="91fca-109">Tok údajov pre Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="91fca-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="91fca-110">Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="91fca-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="91fca-111">Šablóna integrácie, ktorá je k dispozícii s funkciou integrácie údajov, umožňuje tok údajov o projektových úlohách z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="91fca-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="91fca-112">Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="91fca-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="91fca-113">[![Tok údajov pre integráciu Project Service Automation s Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="91fca-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="91fca-114">Šablóna a úloha</span><span class="sxs-lookup"><span data-stu-id="91fca-114">Template and task</span></span>

<span data-ttu-id="91fca-115">Šablónu nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt**, kde si vyberiete verejné šablóny.</span><span class="sxs-lookup"><span data-stu-id="91fca-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="91fca-116">Nasledujúca šablóna a základná úlohu sa používajú na synchronizáciu projektových úloh Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="91fca-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="91fca-117">**Názov šablóny v časti Integrácia údajov:** Projektové úlohy (PSA do Fin a Ops)</span><span class="sxs-lookup"><span data-stu-id="91fca-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="91fca-118">**Názov úlohy v projekte:** Projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="91fca-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="91fca-119">Predtým, ako môže dôjsť k synchronizácii projektových úloh, musíte synchronizovať projektové zmluvy a projekty.</span><span class="sxs-lookup"><span data-stu-id="91fca-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="91fca-120">Nastavenie entity</span><span class="sxs-lookup"><span data-stu-id="91fca-120">Entity set</span></span>

| <span data-ttu-id="91fca-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="91fca-121">Project Service Automation</span></span> | <span data-ttu-id="91fca-122">Finance</span><span class="sxs-lookup"><span data-stu-id="91fca-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="91fca-123">Projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="91fca-123">Project Tasks</span></span>              | <span data-ttu-id="91fca-124">Integračná entita pre projektovú úlohu</span><span class="sxs-lookup"><span data-stu-id="91fca-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="91fca-125">Tok entity</span><span class="sxs-lookup"><span data-stu-id="91fca-125">Entity flow</span></span>

<span data-ttu-id="91fca-126">Projektové úlohy sa spravujú v Project Service Automation a synchronizujú s Finance ako projektové aktivity.</span><span class="sxs-lookup"><span data-stu-id="91fca-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="91fca-127">Nevyhnutné predpoklady a nastavenie mapovania</span><span class="sxs-lookup"><span data-stu-id="91fca-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="91fca-128">Predtým, ako môže dôjsť k synchronizácii projektových úloh, musíte synchronizovať projektové zmluvy a projekty.</span><span class="sxs-lookup"><span data-stu-id="91fca-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="91fca-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="91fca-129">Power Query</span></span>

<span data-ttu-id="91fca-130">Ak je táto podmienka splnená, na filtrovanie údajov musíte použiť Microsoft Power Query for Excel:</span><span class="sxs-lookup"><span data-stu-id="91fca-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="91fca-131">V projektovej úlohe máte záznamy týkajúce sa konkrétnych zdrojov.</span><span class="sxs-lookup"><span data-stu-id="91fca-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="91fca-132">Ak musíte použiť Power Query, postupujte podľa tohto pokynu:</span><span class="sxs-lookup"><span data-stu-id="91fca-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="91fca-133">Šablóna Projektové úlohy (PSA do Fin a Ops) má predvolený filter, ktorý vylučuje záznamy špecifické pre daný zdroj z projektovej úlohy nastavením filtra na **IsLineTask** na **False**.</span><span class="sxs-lookup"><span data-stu-id="91fca-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="91fca-134">Ak vytvárate vlastnú šablónu, musíte pridať tento filter.</span><span class="sxs-lookup"><span data-stu-id="91fca-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="91fca-135">Mapovanie šablón v integrácii údajov</span><span class="sxs-lookup"><span data-stu-id="91fca-135">Template mapping in Data integration</span></span>

<span data-ttu-id="91fca-136">Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov.</span><span class="sxs-lookup"><span data-stu-id="91fca-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="91fca-137">Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="91fca-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="91fca-138">[![Mapovanie šablón](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="91fca-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
