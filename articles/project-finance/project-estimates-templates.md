---
title: Synchronizácia projektových odhadov priamo z Project Service Automation do Finance and Operations
description: Táto téma popisuje šablóny a základné úlohy, ktoré sa používajú na synchronizáciu projektových odhadov hodín a projektových odhadov nákladov priamo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
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
ms.assetid: d688ce9a-41e3-4ebe-952e-700f8351fbe9
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: a24a967d82c2e005e61234d34da8a583b61ff7b1
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755574"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="cc5d9-103">Synchronizácia projektových odhadov priamo z Project Service Automation do Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cc5d9-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cc5d9-104">Táto téma popisuje šablóny a základné úlohy, ktoré sa používajú na synchronizáciu projektových odhadov hodín a projektových odhadov nákladov priamo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="cc5d9-105">Integrácia projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií sú k dispozícii vo verzii 8.0.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="cc5d9-106">Integrácia skutočných hodnôt je k dispozícii vo verzii 8.0.1 alebo novšej.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="cc5d9-107">Tok údajov pre Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="cc5d9-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="cc5d9-108">Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="cc5d9-109">Šablóna integrácie, ktorá je k dispozícii s funkciou integrácie údajov, umožňuje tok údajov o kategóriách transakcie projektových odhadov hodín a projektových odhadov výdavkov z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cc5d9-110">Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="cc5d9-111">[![Tok údajov pre integráciu Project Service Automation s Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="cc5d9-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="cc5d9-112">Odhady hodín projektu</span><span class="sxs-lookup"><span data-stu-id="cc5d9-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cc5d9-113">Šablóna a úlohy</span><span class="sxs-lookup"><span data-stu-id="cc5d9-113">Template and tasks</span></span>

<span data-ttu-id="cc5d9-114">Dostupné šablóny nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt**, kde si vyberiete verejné šablóny.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cc5d9-115">Nasledujúca šablóna a základné úlohy sa používajú na synchronizáciu odhadov hodín z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="cc5d9-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="cc5d9-116">**Názov šablóny v časti Integrácia údajov:** Odhady hodín projektu (PSA do Fin a Ops)</span><span class="sxs-lookup"><span data-stu-id="cc5d9-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cc5d9-117">**Názov úloh v projekte:**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cc5d9-118">Vzťahy transakcie</span><span class="sxs-lookup"><span data-stu-id="cc5d9-118">Transaction relationships</span></span>
    - <span data-ttu-id="cc5d9-119">Odhady nákladov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="cc5d9-120">Nastavenie entity</span><span class="sxs-lookup"><span data-stu-id="cc5d9-120">Entity set</span></span>

| <span data-ttu-id="cc5d9-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc5d9-121">Project Service Automation</span></span> | <span data-ttu-id="cc5d9-122">Financie</span><span class="sxs-lookup"><span data-stu-id="cc5d9-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="cc5d9-123">Projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="cc5d9-123">Project tasks</span></span>              | <span data-ttu-id="cc5d9-124">Entita integrácie pre odhady hodín projektu</span><span class="sxs-lookup"><span data-stu-id="cc5d9-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="cc5d9-125">Tok entity</span><span class="sxs-lookup"><span data-stu-id="cc5d9-125">Entity flow</span></span>

<span data-ttu-id="cc5d9-126">Projektové odhady hodín sa spravujú v Project Service Automation a synchronizujú s Finance ako prognózy hodín.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cc5d9-127">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="cc5d9-127">Prerequisites</span></span>

<span data-ttu-id="cc5d9-128">Predtým, ako môže dôjsť k synchronizácii odhadov hodín projektu, musíte synchronizovať projekty, projektové úlohy a kategórie transakcií výdavkov na projekt.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cc5d9-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="cc5d9-129">Power Query</span></span>

<span data-ttu-id="cc5d9-130">V šablóne odhadov hodín projektu musíte na dokončenie týchto úloh použiť Microsoft Power Query for Excel:</span><span class="sxs-lookup"><span data-stu-id="cc5d9-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="cc5d9-131">Nastavte predvolené ID modelu predpovede, ktoré sa použije, keď integrácia vytvorí nové predpovede hodín.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="cc5d9-132">Odfiltrujte všetky záznamy týkajúce sa konkrétnych zdrojov v úlohe, ktoré zlyhajú pri integrácii, do hodinových predpovedí.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="cc5d9-133">Odfiltrujte všetky prázdne riadky kategórií transakcií.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="cc5d9-134">Nedokončenie tejto úlohy môže mať za následok nesprávnu predpoveď hodín.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="cc5d9-135">Nastavte predvolené ID modelu prognózy</span><span class="sxs-lookup"><span data-stu-id="cc5d9-135">Set the default forecast model ID</span></span>

<span data-ttu-id="cc5d9-136">Ak chcete aktualizovať predvolené ID modelu prognózy v šablóne, kliknite na šípku **Mapovať** na otvorenie mapovania.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cc5d9-137">Potom stlačte odkaz **Pokročilý dotaz a filtrovanie**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="cc5d9-138">Ak používate predvolenú šablónu Odhady hodín projektu (PSA po Fin a Ops) stlačte ikonu **Vložený stav** v zozname **Uplatnené kroky**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="cc5d9-139">V zázname **Funkcia** nahraďte **O\_forecast** za názov ID modelu predpovede, ktoré sa musí použiť pri integrácii.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="cc5d9-140">Predvolená šablóna obsahuje ID modelu prognózy z ukážkových údajov.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="cc5d9-141">Ak vytvárate novú šablónu, musíte pridať tento stĺpec.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="cc5d9-142">V Power Query vyberte **Pridajte podmienený stĺpec** a zadajte názov nového stĺpca, napríklad **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="cc5d9-143">Zadajte podmienku pre stĺpec, kde, ak projektová úloha nemá hodnotu null, potom \<zadajte ID predpovedného modelu\>; inak null.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="cc5d9-144">Odfiltrujte záznamy týkajúce sa konkrétnych zdrojov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-144">Filter out resource-specific records</span></span>

<span data-ttu-id="cc5d9-145">Šablóna Odhady hodín projektu (PSA pre Fin a Ops) má predvolený filter, ktorý odstráni všetky záznamy špecifické pre daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="cc5d9-146">Ak vytvárate vlastnú šablónu, musíte pridať tento filter.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="cc5d9-147">Vyberte prepojenie **Pokročilý dotaz a filtrovanie** na filtrovanie v stĺpci **msdyn\_islinetask** tak, že sa zahrnú iba záznamy s príznakom **False**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="cc5d9-148">Odfiltrujte všetky prázdne riadky kategórií transakcií</span><span class="sxs-lookup"><span data-stu-id="cc5d9-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="cc5d9-149">Ak chcete odstrániť všetky riadky, ktoré majú prázdne kategórie transakcií, musíte pridať filter.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="cc5d9-150">Táto úloha je povinná bez ohľadu na to, či používate predvolenú šablónu alebo si vytvoríte vlastnú šablónu.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="cc5d9-151">Tento filter odstráni všetky súhrnné riadky z Project Service Automation, ktoré by mohli spôsobiť, že hodinové predpovede v aplikácii Finance budú nesprávne.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="cc5d9-152">Stlačte možnosť **Pokročilý dotaz a filtrovanie** na odfiltrovanie záznamov s príznakom null v stĺpci **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cc5d9-153">Mapovanie šablón v integrácii údajov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-153">Template mapping in Data integration</span></span>

<span data-ttu-id="cc5d9-154">Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="cc5d9-155">Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cc5d9-156">[![Mapovanie šablón](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cc5d9-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="cc5d9-157">Odhady projektových výdavkov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="cc5d9-158">Šablóna a úlohy</span><span class="sxs-lookup"><span data-stu-id="cc5d9-158">Template and tasks</span></span>

<span data-ttu-id="cc5d9-159">Nasledujúca šablóna a základné úlohy sa používajú na synchronizáciu odhadov výdavkov z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="cc5d9-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="cc5d9-160">**Názov šablóny v časti Integrácia údajov:** Projektové odhady výdavkov (PSA do Fin a Ops)</span><span class="sxs-lookup"><span data-stu-id="cc5d9-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="cc5d9-161">**Názov úloh v projekte:**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="cc5d9-162">Vzťahy transakcie</span><span class="sxs-lookup"><span data-stu-id="cc5d9-162">Transaction relationships</span></span> 
    - <span data-ttu-id="cc5d9-163">Odhady nákladov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="cc5d9-164">Nastavenie entity</span><span class="sxs-lookup"><span data-stu-id="cc5d9-164">Entity set</span></span>

| <span data-ttu-id="cc5d9-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cc5d9-165">Project Service Automation</span></span> | <span data-ttu-id="cc5d9-166">Financie</span><span class="sxs-lookup"><span data-stu-id="cc5d9-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="cc5d9-167">Kontaktné osoby pre transakcie</span><span class="sxs-lookup"><span data-stu-id="cc5d9-167">Transaction Connections</span></span>    | <span data-ttu-id="cc5d9-168">Integračná entita pre transakčné vzťahy projektu</span><span class="sxs-lookup"><span data-stu-id="cc5d9-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="cc5d9-169">Riadky odhadov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-169">Estimate Lines</span></span>             | <span data-ttu-id="cc5d9-170">Entita integrácie pre odhady projektových výdavkov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="cc5d9-171">Tok entity</span><span class="sxs-lookup"><span data-stu-id="cc5d9-171">Entity flow</span></span>

<span data-ttu-id="cc5d9-172">Projektové odhady výdavkov sa spravujú v Project Service Automation a synchronizujú s Finance ako prognózy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cc5d9-173">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="cc5d9-173">Prerequisites</span></span>

<span data-ttu-id="cc5d9-174">Predtým, ako môže dôjsť k synchronizácii odhadov výdavkov projektu, musíte synchronizovať projekty, projektové úlohy a kategórie transakcií výdavkov na projekt.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="cc5d9-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="cc5d9-175">Power Query</span></span>

<span data-ttu-id="cc5d9-176">V šablóne odhadov výdavkov projektu musíte na dokončenie týchto úloh použiť Power Query:</span><span class="sxs-lookup"><span data-stu-id="cc5d9-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="cc5d9-177">Filtrujte tak, aby boli zahrnuté iba riadkové záznamy odhadu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="cc5d9-178">Nastavte predvolené ID modelu predpovede, ktoré sa použije, keď integrácia vytvorí nové predpovede hodín.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="cc5d9-179">Transformujte typy fakturácie.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-179">Transform the billing types.</span></span>
- <span data-ttu-id="cc5d9-180">Transformujte typy transakcií.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="cc5d9-181">Filtrujte tak, aby boli zahrnuté iba riadky odhadov výdavkov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="cc5d9-182">Šablóna Odhady výdavkov projektu (PSA na Fin a Ops) má predvolený filter, ktorý v integrácii obsahuje iba riadky výdavkov.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="cc5d9-183">Ak vytvárate vlastnú šablónu, musíte pridať tento filter.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="cc5d9-184">Zvoľte úlohu **Transakčné vzťahy** a potom kliknite na šípku **Mapovať** na otvorenie mapovania.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cc5d9-185">Stlačte odkaz **Pokročilý dotaz a filtrovanie**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="cc5d9-186">Filtrujte stĺpec **msdyn\_transactiontype1** tak, aby obsahoval iba **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="cc5d9-187">Nastavte predvolené ID modelu prognózy</span><span class="sxs-lookup"><span data-stu-id="cc5d9-187">Set the default forecast model ID</span></span>

<span data-ttu-id="cc5d9-188">Ak chcete aktualizovať predvolené ID modelu prognózy v šablóne, kliknite na úlohu **Odhady výdavkov** a potom kliknutím na šípku **Mapovať** otvorte mapovanie.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="cc5d9-189">Stlačte odkaz **Pokročilý dotaz a filtrovanie**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="cc5d9-190">Ak používate predvolenú šablónu odhadov výdavkov projektu (PSA po Fin a Ops) v Power Query stlačte najprv **Vložený stav** v časti **Uplatnené kroky**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="cc5d9-191">V zázname **Funkcia** nahraďte **O\_forecast** za názov ID modelu predpovede, ktoré sa musí použiť pri integrácii.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="cc5d9-192">Predvolená šablóna obsahuje ID modelu prognózy z ukážkových údajov.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="cc5d9-193">Ak vytvárate novú šablónu, musíte pridať tento stĺpec.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="cc5d9-194">V Power Query vyberte **Pridajte podmienený stĺpec** a zadajte názov nového stĺpca, napríklad **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="cc5d9-195">Zadajte podmienku pre stĺpec, kde, ak ID riadka odhadu nemá hodnotu null, potom \<zadajte ID predpovedného modelu\>; inak null.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="cc5d9-196">Transformujte typy fakturácie</span><span class="sxs-lookup"><span data-stu-id="cc5d9-196">Transform the billing types</span></span>

<span data-ttu-id="cc5d9-197">Šablóna Odhady výdavkov na projekt (PSA do Fin a Ops) obsahuje podmienený stĺpec, ktorý sa používa na transformáciu typov fakturácie, ktoré sa prijímajú z Project Service Automation počas integrácie.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="cc5d9-198">Ak vytvárate vlastnú šablónu, musíte pridať tento podmienený stĺpec.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="cc5d9-199">Stlačte prepojenie **Pokročilý dopyt a filtrovanie** a potom vyberte **Pridať podmienený stĺpec**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="cc5d9-200">Zadajte názov nového stĺpca, napríklad **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="cc5d9-201">Potom zadajte nasledujúcu podmienku:</span><span class="sxs-lookup"><span data-stu-id="cc5d9-201">Then enter the following condition:</span></span>

<span data-ttu-id="cc5d9-202">Ak **msdyn\_billingtype** = 192350000, potom **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="cc5d9-203">alebo ak **msdyn\_billingtype** = 192350001, potom **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="cc5d9-204">alebo ak **msdyn\_billingtype** = 192350002, potom **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="cc5d9-205">Inak **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="cc5d9-206">Transformujte typy transakcií</span><span class="sxs-lookup"><span data-stu-id="cc5d9-206">Transform the transaction types</span></span>

<span data-ttu-id="cc5d9-207">Šablóna Odhady výdavkov na projekt (PSA do Fin a Ops) obsahuje podmienený stĺpec, ktorý sa používa na transformáciu typov transakcie, ktoré sa prijímajú z Project Service Automation počas integrácie.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="cc5d9-208">Ak vytvárate vlastnú šablónu, musíte pridať tento podmienený stĺpec.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="cc5d9-209">Stlačte prepojenie **Pokročilý dopyt a filtrovanie** a potom vyberte **Pridať podmienený stĺpec**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="cc5d9-210">Zadajte názov nového stĺpca, napríklad **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="cc5d9-211">Potom zadajte nasledujúcu podmienku:</span><span class="sxs-lookup"><span data-stu-id="cc5d9-211">Then enter the following condition:</span></span>

<span data-ttu-id="cc5d9-212">Ak **msdyn\_transactiontypecode** = 192350000, potom **Cost**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="cc5d9-213">alebo ak **msdyn\_transactiontypecode** = 192350005, potom **Sales**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="cc5d9-214">Inak **null**</span><span class="sxs-lookup"><span data-stu-id="cc5d9-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cc5d9-215">Mapovanie šablón v integrácii údajov</span><span class="sxs-lookup"><span data-stu-id="cc5d9-215">Template mapping in Data integration</span></span>

<span data-ttu-id="cc5d9-216">Nasledujúca ilustrácia ukazuje príklady mapovania úlohy šablóny v Integrácii údajov.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="cc5d9-217">Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="cc5d9-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="cc5d9-218">[![Mapovanie šablón](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cc5d9-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="cc5d9-219">[![Mapovanie šablón](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cc5d9-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
