---
title: Hromadné opravy skutočností vytvorených schválenými záznamami času a výdavkov
description: Táto téma vysvetľuje, ako môže správca vykonať jednoduché alebo hromadné opravy predtým schválených položiek času alebo výdavkov, ak fakturácia nie je dokončená.
author: rumant
manager: AnnBe
ms.date: 04/02/2020
ms.topic: article
ms.service: dynamics-ax-applications
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 6d6c03cc74d47ca3ae7c2bd7d0aa0720bb2f3c01
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084540"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a><span data-ttu-id="2888e-103">Hromadné opravy skutočností vytvorených schválenými záznamami času a výdavkov</span><span class="sxs-lookup"><span data-stu-id="2888e-103">Bulk corrections of actuals created by approved time and expense entries</span></span>

<span data-ttu-id="2888e-104">Príležitostne môže byť nesprávne zadaný údaj o čase alebo výdavkoch.</span><span class="sxs-lookup"><span data-stu-id="2888e-104">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="2888e-105">Napríklad poradca môže zvoliť nesprávny dátum pri vytváraní časového záznamu alebo môže transponovať čísla pri zadávaní výdavkov.</span><span class="sxs-lookup"><span data-stu-id="2888e-105">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="2888e-106">Ak konzultant nemôže vykonať aktualizácie predložených záznamov, správca môže priamo opraviť záznam pre projekt.</span><span class="sxs-lookup"><span data-stu-id="2888e-106">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="2888e-107">Na dokončenie postupov v tejto téme budete potrebovať oprávnenia správcu.</span><span class="sxs-lookup"><span data-stu-id="2888e-107">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="2888e-108">Opravte schválené časové záznamy</span><span class="sxs-lookup"><span data-stu-id="2888e-108">Correct approved time entries</span></span>     

<span data-ttu-id="2888e-109">Ak chcete opraviť jednorazové alebo viacnásobné zadania projektu, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="2888e-109">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="2888e-110">V oblasti **Sales** zvoľte možnosť **Transakcie** a potom stlačte možnosť **Schválený čas**.</span><span class="sxs-lookup"><span data-stu-id="2888e-110">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="2888e-111">V zozname **Schválený čas** vyhľadajte a vyberte jeden alebo viac schválených záznamov času, ktoré chcete opraviť.</span><span class="sxs-lookup"><span data-stu-id="2888e-111">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="2888e-112">Pomocou filtra môžete vyhľadať súvisiace položky.</span><span class="sxs-lookup"><span data-stu-id="2888e-112">You can use the filter to locate related entries.</span></span> <span data-ttu-id="2888e-113">Môžete napríklad filtrovať ID projektu a vybrať všetky schválené časové záznamy s týmto ID projektu.</span><span class="sxs-lookup"><span data-stu-id="2888e-113">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="2888e-114">Zvoľte možnosť **Opraviť záznamy**.</span><span class="sxs-lookup"><span data-stu-id="2888e-114">Select **Correct entries**.</span></span> <span data-ttu-id="2888e-115">Automaticky sa vytvorí nový denník korekcií s priradeným typom **Oprava času**.</span><span class="sxs-lookup"><span data-stu-id="2888e-115">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="2888e-116">Vybraté položky sa pridajú do denníka.</span><span class="sxs-lookup"><span data-stu-id="2888e-116">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="2888e-117">Na stránke **Nový denník** zadajte **Trvanie** svojho denníka korekcií a potom stlačte kartu **Opravy zadaní času**.</span><span class="sxs-lookup"><span data-stu-id="2888e-117">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  
5. <span data-ttu-id="2888e-118">V časti **Nové hodnoty pre zadania času** aktualizujte v prípade potreby polia so správnymi informáciami.</span><span class="sxs-lookup"><span data-stu-id="2888e-118">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="2888e-119">Napríklad môžete zmeniť priradený projekt alebo rezervovateľný zdroj.</span><span class="sxs-lookup"><span data-stu-id="2888e-119">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="2888e-120">Stlačte možnosť **Ukážka**.</span><span class="sxs-lookup"><span data-stu-id="2888e-120">Select **Preview**.</span></span> <span data-ttu-id="2888e-121">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="2888e-121">In the dialog box, select **OK**.</span></span> <span data-ttu-id="2888e-122">Na karte **Záznamy v účtovnom denníku** si môžete zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými časovými položkami, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené.</span><span class="sxs-lookup"><span data-stu-id="2888e-122">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="2888e-123">Ak je potrebné vykonať ďalšie opravy, opakujte kroky 5 a 6.</span><span class="sxs-lookup"><span data-stu-id="2888e-123">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="2888e-124">Všetky opravené skutočnosti budú mať rovnaké hodnoty, aké ste vybrali v sekcii **Nové hodnoty pre zadania času**.</span><span class="sxs-lookup"><span data-stu-id="2888e-124">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="2888e-125">Ak sa opravy zobrazia podľa očakávania, vyberte položku **Potvrdiť**.</span><span class="sxs-lookup"><span data-stu-id="2888e-125">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="2888e-126">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="2888e-126">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="2888e-127">Vráťte sa do oblasti **Sales** , zvoľte možnosť **Projekty** a potom otvorte projekt, pre ktoré ste práve aktualizovali časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="2888e-127">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="2888e-128">Na stránke **Projekty** na karte **Skutočné údaje** si zobrazte vykonané zmeny.</span><span class="sxs-lookup"><span data-stu-id="2888e-128">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="2888e-129">Ak karta **Skutočné údaje** nie je viditeľná, zvoľte možnosť **Súvisiace** > **Skutočné údaje**.</span><span class="sxs-lookup"><span data-stu-id="2888e-129">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="2888e-130">V zozname **Priradené zobrazenie skutočných hodnôt** môžete vidieť, že pôvodné časové záznamy, ktoré boli zvrátené, sú stále uvedené, ako aj zodpovedajúce opravené časové položky.</span><span class="sxs-lookup"><span data-stu-id="2888e-130">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="2888e-131">Napríklad na nasledujúcej grafike sú dve riadkové položky s množstvom 8,00, ktorých debety sú uvedené v stĺpci Suma.</span><span class="sxs-lookup"><span data-stu-id="2888e-131">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="2888e-132">Ďalej sú v stĺpci Suma dve riadkové položky s množstvom -8,00, ktoré zobrazujú pripísané sumy.</span><span class="sxs-lookup"><span data-stu-id="2888e-132">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="2888e-133">Tieto korekcie znižujú množstvo na nulu.</span><span class="sxs-lookup"><span data-stu-id="2888e-133">These corrections bring the quantity to zero.</span></span>

![Zoznam priradeného zobrazenia skutočných hodnôt](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="2888e-135">Opravte schválené záznamy výdavkov</span><span class="sxs-lookup"><span data-stu-id="2888e-135">Correct approved expense entries</span></span>

<span data-ttu-id="2888e-136">Ak chcete opraviť jednu alebo viac položiek výdavkov, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="2888e-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="2888e-137">V oblasti **Sales** v ľavej navigačnej table v časti **Transakcie** zvoľte možnosť **Schválené výdavky**.</span><span class="sxs-lookup"><span data-stu-id="2888e-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="2888e-138">V zozname **Schválené výdavky** zvoľte projekt, ktorý chcete opraviť, a potom stlačte možnosť **Opraviť záznamy**.</span><span class="sxs-lookup"><span data-stu-id="2888e-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="2888e-139">Automaticky sa vytvorí nový denník korekcií s priradeným typom **Oprava výdavku**.</span><span class="sxs-lookup"><span data-stu-id="2888e-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="2888e-140">Na stránke **Nový denník** zadajte **Opis** opravy a na karte **Oprava výdavku** v sekcii **Nové hodnoty pre výdavky** zvoľte dátové polia, ktoré chcete pri vybratých riadkoch nákladov opraviť.</span><span class="sxs-lookup"><span data-stu-id="2888e-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="2888e-141">Napríklad môžete priradiť náklady inému **Projektu** alebo opraviť **Kategória výdavku** , **Dátum výdavku** alebo **Rezervovateľný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="2888e-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="2888e-142">Stlačte možnosť **Ukážka**.</span><span class="sxs-lookup"><span data-stu-id="2888e-142">Select **Preview**.</span></span> <span data-ttu-id="2888e-143">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="2888e-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="2888e-144">Skontrolujte opravy na karte **Záznamy v účtovnom denníku**. Môžete si zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými výdavkovými položkami, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené.</span><span class="sxs-lookup"><span data-stu-id="2888e-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="2888e-145">Ak sú opravené hodnoty podľa očakávania, vyberte položku **Potvrdiť**.</span><span class="sxs-lookup"><span data-stu-id="2888e-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="2888e-146">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="2888e-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="2888e-147">Ak sa hodnoty nezobrazujú podľa očakávania, vyberte položku **Zrušiť** , čím sa vrátite do zoznamu **Schválené výdavky**.</span><span class="sxs-lookup"><span data-stu-id="2888e-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="2888e-148">Opakujte kroky 2 až 5.</span><span class="sxs-lookup"><span data-stu-id="2888e-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="2888e-149">Opravené skutočné hodnoty budú mať rovnaké hodnoty, aké ste vybrali v sekcii **Nové hodnoty pre výdavky**.</span><span class="sxs-lookup"><span data-stu-id="2888e-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="2888e-150">Po potvrdení denníka opráv prejdite späť na projekt alebo projekty, ktoré ste aktualizovali, aby ste si prezreli zmeny.</span><span class="sxs-lookup"><span data-stu-id="2888e-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="2888e-151">Na stránke projektu na karte **Skutočné hodnoty** skontrolujte **Priradené zobrazenie skutočných hodnôt**.</span><span class="sxs-lookup"><span data-stu-id="2888e-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="2888e-152">Uvádzajú sa pôvodné záznamy a opravené položky.</span><span class="sxs-lookup"><span data-stu-id="2888e-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="2888e-153">Nasledujúca grafika zobrazuje pôvodné sumy vstupných nákladov a zodpovedajúce opravené položky vstupných nákladov.</span><span class="sxs-lookup"><span data-stu-id="2888e-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 

![Skutočné hodnoty výdavkov](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)
