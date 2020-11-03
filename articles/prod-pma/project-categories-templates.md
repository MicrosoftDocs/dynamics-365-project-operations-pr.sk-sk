---
title: Synchronizujte kategórie výdavkov projektu medzi Finance and Operations a Project Service Automation
description: Táto téma popisuje šablóny a základné úlohu, ktoré sa používajú na synchronizáciu projektových kategórií výdavkov medzi Microsoft Dynamics 365 Finance a Dynamics 365 Project Service Automation.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084503"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="2b142-103">Synchronizujte kategórie výdavkov projektu medzi Finance and Operations a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2b142-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2b142-104">Táto téma popisuje šablóny a základné úlohu, ktoré sa používajú na synchronizáciu projektových kategórií výdavkov medzi Dynamics 365 Finance a Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2b142-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="2b142-105">Integrácia projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií sú k dispozícii vo verzii 8.0.</span><span class="sxs-lookup"><span data-stu-id="2b142-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="2b142-106">Integrácia skutočných hodnôt je k dispozícii vo verzii 8.0.1 alebo novšej.</span><span class="sxs-lookup"><span data-stu-id="2b142-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="2b142-107">Ak používate Enterprise Edition 7.3.0, po inštalácii KB 4132657 a KB 4132660 budete môcť tieto šablóny použiť na integráciu projektových úloh, kategórií transakcií výdavkov, odhadov hodín, odhadov výdavkov a skutočných údajov a na nakonfigurovať blokovanie funkcií.</span><span class="sxs-lookup"><span data-stu-id="2b142-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="2b142-108">Ak musíte resetovať účtovné prerozdelenie, odporúčame vám nainštalovať si aj KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="2b142-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="2b142-109">Tok údajov pre Project Service Automation a Finance</span><span class="sxs-lookup"><span data-stu-id="2b142-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="2b142-110">Integračné riešenie Project Service Automation a služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="2b142-111">Šablóna integrácie, ktorá je k dispozícii s funkciou integrácie údajov, umožňuje tok údajov o kategóriách transakcie projektových výdavkov medzi Finance a Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2b142-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="2b142-112">Ak sú kategórie výdavkov projektu zvládnuté v aplikácii Finance, integračný tok ide najskôr od Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2b142-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="2b142-113">ID integrácie kategórií výdavkov projektu sa potom aktualizujú synchronizáciou z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="2b142-114">Ak sú kategórie výdavkov projektu zvládnuté v Project Service Automation, integračný tok ide najskôr od Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="2b142-115">Pred synchronizáciou z Project Service Automation musia byť kategórie projektov už nakonfigurované v aplikácii Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="2b142-116">Následne sa synchronizujú z Finance späť do Project Service Automation a potom znova z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="2b142-117">Týmto spôsobom pomôžete zaručiť, že kategórie budú prepojené a že sa nevytvárajú duplikáty.</span><span class="sxs-lookup"><span data-stu-id="2b142-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="2b142-118">Kategórie projektových výdavkov sú zvyčajne zvládnuté vo Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="2b142-119">Ak však nie sú, alebo ak už boli kategórie výdavkov vytvorené v Project Service Automation, musíte ich najskôr synchronizovať pomocou šablóny kategórií výdavkov projektu (PSA až Fin a Ops).</span><span class="sxs-lookup"><span data-stu-id="2b142-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="2b142-120">Potom vykonajte synchronizáciu pomocou šablóny Kategórie výdavkov projektu (Fin and Ops to PSA).</span><span class="sxs-lookup"><span data-stu-id="2b142-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="2b142-121">Potom by ste mali synchronizáciu z Project Service Automation do Finance spustiť ešte raz.</span><span class="sxs-lookup"><span data-stu-id="2b142-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="2b142-122">Ak synchronizujete najskôr z Project Service Automation, pred spustením synchronizácie musia byť v službe Finance splnené nasledujúce požiadavky:</span><span class="sxs-lookup"><span data-stu-id="2b142-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="2b142-123">Zdieľaná kategória, ktorá sa zhoduje s kategóriou projektu, ktorá je nastavená v Project Service Automation, musí existovať a musí byť povolená pre **Projekt** aj **Výdavok**.</span><span class="sxs-lookup"><span data-stu-id="2b142-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="2b142-124">Pre každú právnickú entitu Finance s ktorou sa musí integrovať, musia existovať nasledujúce kategórie projektu:</span><span class="sxs-lookup"><span data-stu-id="2b142-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="2b142-125">Existuje **Kategória projektu**.</span><span class="sxs-lookup"><span data-stu-id="2b142-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="2b142-126">**Použiť do výdavkov** je aktivované.</span><span class="sxs-lookup"><span data-stu-id="2b142-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="2b142-127">**Aktívny v denníku** je aktivované.</span><span class="sxs-lookup"><span data-stu-id="2b142-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="2b142-128">**Typ transakcie** je nastavený na **Výdavok**.</span><span class="sxs-lookup"><span data-stu-id="2b142-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="2b142-129">Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="2b142-130">[![Tok údajov pre integráciu Project Service Automation s Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="2b142-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="2b142-131">Synchronizujte kategórie výdavkov projektu medzi Finance a Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2b142-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="2b142-132">Šablóna a úloha</span><span class="sxs-lookup"><span data-stu-id="2b142-132">Template and task</span></span>

<span data-ttu-id="2b142-133">Šablónu nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt** , kde si vyberiete verejné šablóny.</span><span class="sxs-lookup"><span data-stu-id="2b142-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="2b142-134">Nasledujúca šablóna a základná úloha sa používajú na synchronizáciu kategórií výdavkov z Finance do Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="2b142-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="2b142-135">**Názov šablóny v časti Integrácia údajov:** Kategórie transakcie výdavkov projektu (Fin a Ops do PSA)</span><span class="sxs-lookup"><span data-stu-id="2b142-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="2b142-136">**Názov úlohy v projekte:** Synchronizujte kategórie s PSA</span><span class="sxs-lookup"><span data-stu-id="2b142-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="2b142-137">Nastavenie entity</span><span class="sxs-lookup"><span data-stu-id="2b142-137">Entity set</span></span>

| <span data-ttu-id="2b142-138">Finance</span><span class="sxs-lookup"><span data-stu-id="2b142-138">Finance</span></span>                           | <span data-ttu-id="2b142-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2b142-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="2b142-140">Integračná entita pre kategórie</span><span class="sxs-lookup"><span data-stu-id="2b142-140">Integration entity for categories</span></span> | <span data-ttu-id="2b142-141">Kategórie transakcií</span><span class="sxs-lookup"><span data-stu-id="2b142-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="2b142-142">Tok entity</span><span class="sxs-lookup"><span data-stu-id="2b142-142">Entity flow</span></span>

<span data-ttu-id="2b142-143">Kategórie projektových výdavkov sa spravujú vo Finance a synchronizujú sa s Project Service Automation ako kategórie transakcií.</span><span class="sxs-lookup"><span data-stu-id="2b142-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="2b142-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="2b142-144">Power Query</span></span>

<span data-ttu-id="2b142-145">Pri synchronizácii s Project Service Automation musíte na nastavenie typu fakturácie v kategórii transakcií použiť Microsoft Power Query for Excel.</span><span class="sxs-lookup"><span data-stu-id="2b142-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="2b142-146">Šablóna Kategórie výdavkov projektu (Fin and Ops to PSA) poskytuje predvolený stĺpec a mapovanie.</span><span class="sxs-lookup"><span data-stu-id="2b142-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="2b142-147">Ak vytvárate vlastnú šablónu, musíte pridať podmienený stĺpec v Power Query.</span><span class="sxs-lookup"><span data-stu-id="2b142-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="2b142-148">Postupujte nasledovne.</span><span class="sxs-lookup"><span data-stu-id="2b142-148">Follow these steps.</span></span>

1. <span data-ttu-id="2b142-149">Kliknutím na šípku otvoríte mapovanie úlohy kategórií výdavkov projektu v šablóne Kategórie transakcií výdavkov projektu (Fin a Ops do PSA).</span><span class="sxs-lookup"><span data-stu-id="2b142-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="2b142-150">Kliknite na prepojenie **Pokročilý dotaz a filtrovanie** , čím otvoríte Power Query.</span><span class="sxs-lookup"><span data-stu-id="2b142-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="2b142-151">Stlačte možnosť **Pridať podmienený stĺpec**.</span><span class="sxs-lookup"><span data-stu-id="2b142-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="2b142-152">Zadajte názov nového stĺpca, napríklad **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="2b142-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="2b142-153">Zadajte nasledujúcu podmienku: **ak CATEGORYID sa nerovná null, potom 19235001, inak null**.</span><span class="sxs-lookup"><span data-stu-id="2b142-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="2b142-154">V stĺpci kliknite na možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="2b142-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="2b142-155">Nezabudnite tento nový stĺpec namapovať na mapovacej stránke.</span><span class="sxs-lookup"><span data-stu-id="2b142-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="2b142-156">Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov.</span><span class="sxs-lookup"><span data-stu-id="2b142-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="2b142-157">Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2b142-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="2b142-158">[![Kategória výdavkov projektu na priradenie šablóny Project Service Automation](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="2b142-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="2b142-159">Synchronizujte kategórie výdavkov projektu z Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="2b142-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="2b142-160">Šablóna a úloha</span><span class="sxs-lookup"><span data-stu-id="2b142-160">Template and task</span></span>

<span data-ttu-id="2b142-161">Nasledujúca šablóna a základná úloha sa používajú na synchronizáciu kategórií výdavkov z Project Service Automation do Finance:</span><span class="sxs-lookup"><span data-stu-id="2b142-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="2b142-162">**Názov šablóny v časti Integrácia údajov:** Kategórie transakcie výdavkov projektu (PSA do Fin a Ops)</span><span class="sxs-lookup"><span data-stu-id="2b142-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="2b142-163">**Názov úlohy v projekte:** Synchronizujte kategórie do Fin Ops</span><span class="sxs-lookup"><span data-stu-id="2b142-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="2b142-164">Nastavenie entity</span><span class="sxs-lookup"><span data-stu-id="2b142-164">Entity set</span></span>

| <span data-ttu-id="2b142-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="2b142-165">Project Service Automation</span></span> | <span data-ttu-id="2b142-166">Financie</span><span class="sxs-lookup"><span data-stu-id="2b142-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="2b142-167">Kategórie transakcií</span><span class="sxs-lookup"><span data-stu-id="2b142-167">Transaction categories</span></span>     | <span data-ttu-id="2b142-168">Integračná entita pre kategórie</span><span class="sxs-lookup"><span data-stu-id="2b142-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="2b142-169">Tok entity</span><span class="sxs-lookup"><span data-stu-id="2b142-169">Entity flow</span></span>

<span data-ttu-id="2b142-170">Kategórie projektových výdavkov sa spravujú vo Finance a synchronizujú sa s Project Service Automation ako kategórie transakcií.</span><span class="sxs-lookup"><span data-stu-id="2b142-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="2b142-171">Synchronizácia späť do Finance aktualizuje kategóriu projektu vo FInance s ID integrácie z Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2b142-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="2b142-172">Mapovanie šablón v integrácii údajov</span><span class="sxs-lookup"><span data-stu-id="2b142-172">Template mapping in Data integration</span></span>

<span data-ttu-id="2b142-173">Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov.</span><span class="sxs-lookup"><span data-stu-id="2b142-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="2b142-174">Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="2b142-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="2b142-175">[![Priradenie šablóny Project Service Automation to Finance](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="2b142-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
