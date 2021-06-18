---
title: Vytvorenie zmlúv založených na zálohách pre fakturácie na základe priebehu
description: Táto téma vysvetľuje, ako vytvoriť projektové zmluvy, aby ste zákazníkom mohli generovať faktúry na základe percenta z dokončenej práce.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3b445488100e0a8335a05505405953b173ff836c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999690"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="dc702-103">Vytvorenie zmlúv založených na zálohách pre fakturácie na základe priebehu</span><span class="sxs-lookup"><span data-stu-id="dc702-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc702-104">Táto téma vysvetľuje, ako vytvoriť projektové zmluvy, aby ste zákazníkom mohli generovať faktúry na základe percenta z dokončenej práce.</span><span class="sxs-lookup"><span data-stu-id="dc702-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="dc702-105">Čiastky faktúry sa automaticky počítajú pre rozpočtové kategórie práce, ktoré ste nastavili pre projekt.</span><span class="sxs-lookup"><span data-stu-id="dc702-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="dc702-106">Načasovanie faktúry sa nastaví pri rokovaniach so zákazníkom o projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="dc702-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="dc702-107">Postupy v tejto téme použite na nastavenie zmluvy, súvisiaceho projektu a fakturačných pravidiel, ktoré počítajú sumy faktúr pre rozpočtové kategórie prác, ktoré ste pre projekt nastavili.</span><span class="sxs-lookup"><span data-stu-id="dc702-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="dc702-108">Po vytvorení zmluvy a projektu môžete nastaviť podrobnosti projektu.</span><span class="sxs-lookup"><span data-stu-id="dc702-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="dc702-109">Môžete napríklad definovať činnosti a priradiť pracovníkov k projektu.</span><span class="sxs-lookup"><span data-stu-id="dc702-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="dc702-110">Príklad</span><span class="sxs-lookup"><span data-stu-id="dc702-110">Example</span></span>

<span data-ttu-id="dc702-111">Vaša organizácia je firma na vývoj softvéru.</span><span class="sxs-lookup"><span data-stu-id="dc702-111">Your organization is a software development firm.</span></span> <span data-ttu-id="dc702-112">Súhlasíte s vytvorením balíka mzdového účtovníctva pre zákazníka za celkový poplatok 20 000 amerických dolárov (USD).</span><span class="sxs-lookup"><span data-stu-id="dc702-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="dc702-113">Vaša organizácia sa zaväzuje fakturovať zákazníkovi po dokončení konkrétnych percent projektu.</span><span class="sxs-lookup"><span data-stu-id="dc702-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="dc702-114">Pre prácu ste nastavili nasledujúce kategórie projektu, aby ste ich mohli použiť v procese fakturácie:</span><span class="sxs-lookup"><span data-stu-id="dc702-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="dc702-115">Consulting</span><span class="sxs-lookup"><span data-stu-id="dc702-115">Consulting</span></span>
- <span data-ttu-id="dc702-116">Dizajn</span><span class="sxs-lookup"><span data-stu-id="dc702-116">Design</span></span>
- <span data-ttu-id="dc702-117">Inštalácia</span><span class="sxs-lookup"><span data-stu-id="dc702-117">Installation</span></span>

<span data-ttu-id="dc702-118">Nastavíte pravidlá fakturácie, ktoré automaticky počítajú čiastky faktúry za percento projektovej práce dokončenej pre každú kategóriu.</span><span class="sxs-lookup"><span data-stu-id="dc702-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="dc702-119">Rozpočtový manažér vytvorí rozpočet pre kategórie projektu.</span><span class="sxs-lookup"><span data-stu-id="dc702-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="dc702-120">Množstvo dokončenej práce sa automaticky počíta ako percento skutočnej práce v porovnaní s rozpočtovanými sumami.</span><span class="sxs-lookup"><span data-stu-id="dc702-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="dc702-121">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="dc702-121">Prerequisites</span></span>

<span data-ttu-id="dc702-122">Pred vytvorením projektu, ktorý používa fakturačné pravidlá, musíte nastaviť postupnosť čísel pre fakturačné pravidlá a denník poplatkov, ktorý sa používa na účtovanie postupových fakturácií.</span><span class="sxs-lookup"><span data-stu-id="dc702-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="dc702-123">Prejdite na **Projektové riadenie a účtovníctvo** \> **Nastaviť** \> **Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="dc702-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="dc702-124">Na stránke **Parametre projektového riadenia a účtovníctva** na karte **Číselné sekvencie** nastavte číselnú postupnosť, ktorú chcete použiť pri vytváraní fakturačných pravidiel.</span><span class="sxs-lookup"><span data-stu-id="dc702-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="dc702-125">Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Denníky** \> **Poplatky**.</span><span class="sxs-lookup"><span data-stu-id="dc702-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="dc702-126">Na stránke **Denník poplatkov** stlačte možnosť **Nový** a zadajte názov denníka.</span><span class="sxs-lookup"><span data-stu-id="dc702-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="dc702-127">Vytvorte zmluvu o postupných fakturáciách</span><span class="sxs-lookup"><span data-stu-id="dc702-127">Create a contract for progress billings</span></span>

<span data-ttu-id="dc702-128">Týmto postupom sa vytvorí projektová zmluva pre projekt s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="dc702-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="dc702-129">Faktúru za projekt vytvoríte, keď práca dokončená na projekte dosiahne určené percento.</span><span class="sxs-lookup"><span data-stu-id="dc702-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="dc702-130">Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Projektové zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="dc702-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="dc702-131">Na stránke **Projektové zmluvy** stlačte možnosť **Nová**.</span><span class="sxs-lookup"><span data-stu-id="dc702-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="dc702-132">V dialógovom okne **Nová projektová zmluva** nastavte nasledujúce polia:</span><span class="sxs-lookup"><span data-stu-id="dc702-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="dc702-133">**Názov**</span><span class="sxs-lookup"><span data-stu-id="dc702-133">**Name**</span></span>
    - <span data-ttu-id="dc702-134">**Typ financovania**</span><span class="sxs-lookup"><span data-stu-id="dc702-134">**Funding type**</span></span>
    - <span data-ttu-id="dc702-135">**Zdroj financovania**</span><span class="sxs-lookup"><span data-stu-id="dc702-135">**Funding source**</span></span>
    - <span data-ttu-id="dc702-136">**Mena predaja** - Štandardne sa táto mena používa pre faktúry zákazníkov, ktoré sú spojené so zmluvou o projekte.</span><span class="sxs-lookup"><span data-stu-id="dc702-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="dc702-137">Menu predaja však môžete zmeniť na konkrétnej faktúre zákazníka.</span><span class="sxs-lookup"><span data-stu-id="dc702-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="dc702-138">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc702-138">Select **OK**.</span></span> <span data-ttu-id="dc702-139">Informácie sa skopírujú do hlavičky stránky **Projektové zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="dc702-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="dc702-140">Na stránke **Projektové zmluvy** vyplňte zvyšné požadované informácie o projekte.</span><span class="sxs-lookup"><span data-stu-id="dc702-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="dc702-141">Vytvorte projekt o postupných fakturáciách</span><span class="sxs-lookup"><span data-stu-id="dc702-141">Create a project for progress billings</span></span>

<span data-ttu-id="dc702-142">Podľa týchto pokynov vytvorte projekt a všetky podprojekty, ktoré sú spojené so zmluvou o projekte.</span><span class="sxs-lookup"><span data-stu-id="dc702-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="dc702-143">Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Všetky projekty**.</span><span class="sxs-lookup"><span data-stu-id="dc702-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="dc702-144">Na stránke **Všetky projekty** kliknite vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="dc702-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="dc702-145">V dialógovom okne **Nový projekt** v poli **Typ projektu** stlačte možnosť **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="dc702-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="dc702-146">Vyberte si projektovú skupinu.</span><span class="sxs-lookup"><span data-stu-id="dc702-146">Select a project group.</span></span> <span data-ttu-id="dc702-147">Skupina projektov definuje informácie o účtovaní pre projekty, ktoré sú skupine priradené.</span><span class="sxs-lookup"><span data-stu-id="dc702-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="dc702-148">Vyberte **Vytvoriť projekt**.</span><span class="sxs-lookup"><span data-stu-id="dc702-148">Select **Create project**.</span></span>
6. <span data-ttu-id="dc702-149">Po vytvorení projektu nastavte fázu projektu na **Prebieha**.</span><span class="sxs-lookup"><span data-stu-id="dc702-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="dc702-150">Vytvorenie rozpočtu pre projekt</span><span class="sxs-lookup"><span data-stu-id="dc702-150">Create a budget for a project</span></span>

<span data-ttu-id="dc702-151">Kategórie rozpočtu sa používajú na automatický výpočet čiastky faktúry za percento práce dokončenej pre každú kategóriu.</span><span class="sxs-lookup"><span data-stu-id="dc702-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="dc702-152">Podľa týchto pokynov vytvoríte rozpočtové kategórie pre odhadované náklady.</span><span class="sxs-lookup"><span data-stu-id="dc702-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="dc702-153">Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Všetky projekty**.</span><span class="sxs-lookup"><span data-stu-id="dc702-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="dc702-154">Na stránke **Všetky projekty** stlačte a otvorte požadovaný projekt.</span><span class="sxs-lookup"><span data-stu-id="dc702-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="dc702-155">Na stránke **Projekty**, na paneli akcií, na karte **Plán** v skupine **Rozpočet** stlačte možnosť **Rozpočet projektu**.</span><span class="sxs-lookup"><span data-stu-id="dc702-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="dc702-156">Na stránke **Rozpočet projektu** zadajte odhadované náklady pre každú kategóriu v projekte.</span><span class="sxs-lookup"><span data-stu-id="dc702-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="dc702-157">Vytvorte pravidlá fakturácie pre fakturácie priebehu</span><span class="sxs-lookup"><span data-stu-id="dc702-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="dc702-158">Prejdite do časti **Riadenie projektu a účtovníctvo** \> **Projekty** \> **Projektové zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="dc702-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="dc702-159">Na stránke zoznamu **Projektové zmluvy** vyberte a otvorte projektovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="dc702-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="dc702-160">Na stránke zmluvy o projekte na karte FastTab **Pravidlá fakturácie** stlačte možnosť **Pridať**.</span><span class="sxs-lookup"><span data-stu-id="dc702-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="dc702-161">Na stránke **Pravidlo fakturácie** v poli **Typ riadka** stlačte možnosť **Priebeh**.</span><span class="sxs-lookup"><span data-stu-id="dc702-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="dc702-162">Na karte FastTab **Podrobnosti riadka pravidla fakturácie** v poli **Hodnota zmluvy** do poľa zadajte celkovú hodnotu zmluvy.</span><span class="sxs-lookup"><span data-stu-id="dc702-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="dc702-163">V poli **Kategória** vyberte kategóriu, do ktorej sa má účtovať poplatková transakcia.</span><span class="sxs-lookup"><span data-stu-id="dc702-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="dc702-164">V poli **Projekt** vyberte projekt, ktorý používa toto pravidlo fakturácie.</span><span class="sxs-lookup"><span data-stu-id="dc702-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="dc702-165">Voliteľné: Priraďte pravidlo fakturácie ďalším projektom.</span><span class="sxs-lookup"><span data-stu-id="dc702-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="dc702-166">Na karte FastTab **Projekt** v časti **Dostupné projekty** vyberte projekt a potom kliknutím na tlačidlo so šípkou doprava pridajte projekt do časti **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="dc702-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="dc702-167">Voliteľné: Vypočítajte percentuálnu čiastku, ktorú zákazník zadržuje z platieb na faktúre.</span><span class="sxs-lookup"><span data-stu-id="dc702-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="dc702-168">Na karte FastTab **Podmienky uchovania platby** vyberte zdroj financovania a potom do poľa **Percento zadržania** zadajte percento zadržania.</span><span class="sxs-lookup"><span data-stu-id="dc702-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="dc702-169">Opakovaním týchto krokov vytvoríte ďalšie pravidlá fakturácie pre projektovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="dc702-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]