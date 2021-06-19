---
title: Prenos rozpočtov projektu na konci fiškálneho roka
description: Tento článok poskytuje informácie o tom, ako previesť zostávajúce sumy rozpočtu do budúcich rokov a ako vytvoriť podrobnosti rozpočtového registra.
author: Yowelle
ms.date: 03/23/2020
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
ms.openlocfilehash: be3dc039b92e88cac6f6b3b7f72bc32ecf587539
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008060"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="553f4-103">Prenos rozpočtov projektu na konci fiškálneho roka</span><span class="sxs-lookup"><span data-stu-id="553f4-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="553f4-104">Pri práci na viacročnom projekte vám môže zostať zvyšný rozpočet na konci fiškálny rok.</span><span class="sxs-lookup"><span data-stu-id="553f4-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="553f4-105">Môžete previesť zostávajúce sumy rozpočtu do budúceho roka a vytvoriť podrobnosti registra rozpočtu pre sumy v priradených účtoch hlavnej knihy.</span><span class="sxs-lookup"><span data-stu-id="553f4-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="553f4-106">Než prenesiete zostávajúce sumy, skontrolujte a analyzujte zostávajúce sumy rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="553f4-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="553f4-107">Skontrolujte a analyzujte zostávajúce sumy rozpočtu</span><span class="sxs-lookup"><span data-stu-id="553f4-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="553f4-108">Vykonajte nasledujúce kroky, aby ste skontrolovali koncoročné rozpočtové sumy pre projekty, ale sumy nepreniesli ďalej.</span><span class="sxs-lookup"><span data-stu-id="553f4-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="553f4-109">Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Rozpočty** > **Prenos rozpočtov**.</span><span class="sxs-lookup"><span data-stu-id="553f4-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="553f4-110">Na stránke **Proces prenosu rozpočtu projektu** na karte **Koncoročné možnosti** overte, že možnosť **Preniesť zostávajúce sumy rozpočtu projektu** nie je povolená.</span><span class="sxs-lookup"><span data-stu-id="553f4-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="553f4-111">Na karte **Parametre** v poli **Rozpočtový rok projektu** vyberte fiškálny rok, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="553f4-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="553f4-112">V poli **Otvárací fiškálny rok** projektu vyberte fiškálny rok, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="553f4-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="553f4-113">V poli **Model z predpovede** stlačte možnosť **Zostávajúci rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="553f4-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="553f4-114">Ak chcete zahrnúť projekty, ktoré vyhovujú vybraným kritériám a nemajú zostávajúci rozpočet, vyberte **Zobraziť nulový zostatok**.</span><span class="sxs-lookup"><span data-stu-id="553f4-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="553f4-115">Na karte **Vybrať rozpočty**, stlačte možnosť **Načítať všetky rozpočty** na načítanie všetkých rozpočtov, ktoré zodpovedajú vybraným kritériám, a potom vyberte možnosť **Spracovať**.</span><span class="sxs-lookup"><span data-stu-id="553f4-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="553f4-116">Ak chcete navrhnúť databázový dotaz, ktorý načíta konkrétnu skupinu rozpočtov do panela, vyberte možnosť **Načítať vybrané rozpočty**.</span><span class="sxs-lookup"><span data-stu-id="553f4-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="553f4-117">Ak chcete získať ďalšie informácie o konkrétnom riadku na table, vyberte riadok a potom stlačte **Zobraziť podrobnosti rozpočtu** alebo **Zobraziť účty**.</span><span class="sxs-lookup"><span data-stu-id="553f4-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="553f4-118">Preniesť zostávajúce sumy rozpočtu</span><span class="sxs-lookup"><span data-stu-id="553f4-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="553f4-119">Keď spracujete zostávajúce sumy rozpočtu, môžete v hlavnej knihe vytvoriť transakcie pre sumy, ktoré prenášate ďalej.</span><span class="sxs-lookup"><span data-stu-id="553f4-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="553f4-120">Ak chcete vytvoriť transakcie hlavnej knihy, vykonajte kroky v časti [Preneste sumy rozpočtu a vytvárajte transakcie hlavnej knihy](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="553f4-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="553f4-121">Sumy rozpočtu, ktoré sa prenášajú ďalej, sa prevedú do predpovedného modelu, ktorý je vybratý na stránke **Predpovedné modely** ako model predpovede prenosu.</span><span class="sxs-lookup"><span data-stu-id="553f4-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="553f4-122">Preneste sumy rozpočtu a vytvárajte transakcie hlavnej knihy</span><span class="sxs-lookup"><span data-stu-id="553f4-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="553f4-123">Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Rozpočty** > **Prenos rozpočtov**.</span><span class="sxs-lookup"><span data-stu-id="553f4-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="553f4-124">Na stránke **Proces prenosu rozpočtu projektu** stlačte možnosť **Koniec roka**, a potom povoľte **Preniesť zostávajúce sumy rozpočtu projektu** a **Vytvorte položky registra rozpočtu v hlavnej knihe**.</span><span class="sxs-lookup"><span data-stu-id="553f4-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="553f4-125">Na karte **Parametre** v skupine poľa **Parametre projektu** vyberte nasledovné:</span><span class="sxs-lookup"><span data-stu-id="553f4-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="553f4-126">**Projektový rozpočtový rok**: Zvoľte začiatok fiškálneho roka, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="553f4-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="553f4-127">**Zisk a strata**: Vytvorte transakcie ziskov a strát v hlavnej knihe.</span><span class="sxs-lookup"><span data-stu-id="553f4-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="553f4-128">**WIP**: Vytvorenie transakcií Work in Progress (WIP) v hlavnej knihe.</span><span class="sxs-lookup"><span data-stu-id="553f4-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="553f4-129">**Mzda**: Vytvorte transakcie alokácie miezd v hlavnej knihe.</span><span class="sxs-lookup"><span data-stu-id="553f4-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="553f4-130">V skupine poľa **Hlavná účtovná kniha** uveďte nasledujúce informácie:</span><span class="sxs-lookup"><span data-stu-id="553f4-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="553f4-131">V poli **Otvárací fiškálny rok** vyberte fiškálny rok, pre ktorý chcete zobraziť prenosnú sumu rozpočtu pre projekty.</span><span class="sxs-lookup"><span data-stu-id="553f4-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="553f4-132">Predvolená hodnota je jeden rok po hodnote v poli **Rozpočtový rok projektu**.</span><span class="sxs-lookup"><span data-stu-id="553f4-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="553f4-133">V poli **Prenosové obdobie**, vyberte obdobie, pre ktoré chcete vytvoriť podrobnosti registra rozpočtu v hlavnej knihe.</span><span class="sxs-lookup"><span data-stu-id="553f4-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="553f4-134">Toto je zvyčajne prvé obdobie v úvodnom fiškálnom roku.</span><span class="sxs-lookup"><span data-stu-id="553f4-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="553f4-135">V skupine poľa **Skopírovať od/do** uveďte nasledujúce informácie:</span><span class="sxs-lookup"><span data-stu-id="553f4-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="553f4-136">V poli **Z predpovedného modelu** vyberte model prognózy rozpočtu projektu spojený so zostávajúcimi čiastkami rozpočtu, ktoré chcete previesť na projekty.</span><span class="sxs-lookup"><span data-stu-id="553f4-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="553f4-137">V poli **Z modelu hlavnej účtovnej knihy** vyberte model prognózy rozpočtu hlavnej účtovnej knihy spojený so zostávajúcimi čiastkami rozpočtu, ktoré chcete previesť do hlavnej účtovnej knihy.</span><span class="sxs-lookup"><span data-stu-id="553f4-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="553f4-138">Stlačte možnosť **Mena prevodu predaja** a použite ponuku predaja projektu na transakcie hlavnej knihy, ktoré sa vytvoria pri prenose súm rozpočtu pre projekty.</span><span class="sxs-lookup"><span data-stu-id="553f4-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="553f4-139">Ak táto možnosť nie je vybratá, transakcie používajú účtovnú menu.</span><span class="sxs-lookup"><span data-stu-id="553f4-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="553f4-140">Stlačte možnosť **Zobraziť nulový zostatok** na zahrnutie projektov, ktoré nemajú zostávajúce sumy rozpočtu, ale spĺňajú ďalšie kritériá, ktoré vyberiete v projektoch zobrazených v dolnom paneli.</span><span class="sxs-lookup"><span data-stu-id="553f4-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="553f4-141">Na karte **Vybrať rozpočty**, stlačte možnosť **Načítať všetky rozpočty** na načítanie všetkých rozpočtov, ktoré zodpovedajú vybraným kritériám.</span><span class="sxs-lookup"><span data-stu-id="553f4-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="553f4-142">Ak chcete navrhnúť databázový dotaz, ktorý načíta konkrétnu skupinu projektových rozpočtov do panela, vyberte možnosť **Načítať vybrané rozpočty**.</span><span class="sxs-lookup"><span data-stu-id="553f4-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="553f4-143">Pre každý projekt, ktorý chcete spracovať, vyberte možnosť na začiatku riadku pre projekt.</span><span class="sxs-lookup"><span data-stu-id="553f4-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="553f4-144">Ak chcete vybrať všetky alebo väčšinu projektov, začiarknite políčko v ľavom hornom rohu.</span><span class="sxs-lookup"><span data-stu-id="553f4-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="553f4-145">Ak chcete vylúčiť spracovanie ľubovoľného projektu, zrušte jeho začiarknutie.</span><span class="sxs-lookup"><span data-stu-id="553f4-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="553f4-146">Ak chcete previesť zostávajúce sumy rozpočtu pre vybrané projekty do vybranej fiškálny rok a vytvoriť podrobnosti registra rozpočtu v hlavnej knihe, vyberte možnosť **Spracovať**.</span><span class="sxs-lookup"><span data-stu-id="553f4-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="553f4-147">Preneste sumy rozpočtu bez vytvorenia transakcie hlavnej knihy</span><span class="sxs-lookup"><span data-stu-id="553f4-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="553f4-148">Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Rozpočty** > **Prenos rozpočtov**.</span><span class="sxs-lookup"><span data-stu-id="553f4-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="553f4-149">Na stránke **Proces prenosu rozpočtu projektu** v poli **Koncoročné možnosti** overte, že možnosť **Preniesť zostávajúce sumy rozpočtu projektu** nie je povolená.</span><span class="sxs-lookup"><span data-stu-id="553f4-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="553f4-150">V skupine **Parametre** v poli **Rozpočtový rok projektu** vyberte fiškálny rok, pre ktorý chcete zobraziť zostávajúcu sumu rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="553f4-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="553f4-151">V skupine poľa **Skopírovať od/do** uveďte nasledujúce informácie:</span><span class="sxs-lookup"><span data-stu-id="553f4-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="553f4-152">V poli **Z predpovedného modelu** vyberte model prognózy rozpočtu projektu spojený so zostávajúcimi čiastkami rozpočtu, ktoré chcete previesť na projekty.</span><span class="sxs-lookup"><span data-stu-id="553f4-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="553f4-153">Ak chcete zahrnúť projekty, ktoré vyhovujú vybraným kritériám a nemajú zostávajúci rozpočet, vyberte **Zobraziť nulový zostatok**.</span><span class="sxs-lookup"><span data-stu-id="553f4-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="553f4-154">V skupine **Vybrať rozpočty**, stlačte možnosť **Načítať všetky rozpočty** na načítanie všetkých rozpočtov, ktoré zodpovedajú vybraným kritériám.</span><span class="sxs-lookup"><span data-stu-id="553f4-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="553f4-155">Ak chcete navrhnúť databázový dotaz, ktorý načíta konkrétnu skupinu projektových rozpočtov do panela, vyberte možnosť **Načítať vybrané rozpočty**.</span><span class="sxs-lookup"><span data-stu-id="553f4-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="553f4-156">Pre každý projekt, ktorý chcete spracovať, vyberte možnosť na začiatku riadku pre projekt.</span><span class="sxs-lookup"><span data-stu-id="553f4-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="553f4-157">Vyberte možnosť **Spracovať** a preneste zostávajúce sumy rozpočtu pre vybrané projekty do vybratého fiškálneho roka.</span><span class="sxs-lookup"><span data-stu-id="553f4-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]