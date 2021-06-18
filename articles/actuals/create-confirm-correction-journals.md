---
title: Vytvorenie a potvrdenie účtovných denníkov opráv
description: Táto téma poskytuje informácie o tom, ako vytvoriť a potvrdiť účtovný denník opravy.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9d242741b2070f086bf8d3f1d40a5380c2a0f518
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996675"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="33d00-103">Vytvorenie a potvrdenie účtovných denníkov opráv</span><span class="sxs-lookup"><span data-stu-id="33d00-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="33d00-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="33d00-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33d00-105">Príležitostne môže byť nesprávne zadaný údaj o čase alebo výdavkoch.</span><span class="sxs-lookup"><span data-stu-id="33d00-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="33d00-106">Napríklad poradca môže zvoliť nesprávny dátum pri vytváraní časového záznamu alebo môže transponovať čísla pri zadávaní výdavkov.</span><span class="sxs-lookup"><span data-stu-id="33d00-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="33d00-107">Ak konzultant nemôže vykonať aktualizácie predložených záznamov, správca môže priamo opraviť záznam pre projekt.</span><span class="sxs-lookup"><span data-stu-id="33d00-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="33d00-108">Na dokončenie postupov v tejto téme budete potrebovať oprávnenia správcu.</span><span class="sxs-lookup"><span data-stu-id="33d00-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="33d00-109">Opravte schválené časové záznamy</span><span class="sxs-lookup"><span data-stu-id="33d00-109">Correct approved time entries</span></span>     

<span data-ttu-id="33d00-110">Ak chcete opraviť jednorazové alebo viacnásobné zadania projektu, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="33d00-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="33d00-111">V oblasti **Sales** zvoľte možnosť **Transakcie** a potom stlačte možnosť **Schválený čas**.</span><span class="sxs-lookup"><span data-stu-id="33d00-111">In the **Sales** area, select **Transactions**, and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="33d00-112">V zozname **Schválený čas** vyhľadajte a vyberte jeden alebo viac schválených záznamov času, ktoré chcete opraviť.</span><span class="sxs-lookup"><span data-stu-id="33d00-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="33d00-113">Pomocou filtra môžete vyhľadať súvisiace položky.</span><span class="sxs-lookup"><span data-stu-id="33d00-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="33d00-114">Môžete napríklad filtrovať ID projektu a vybrať všetky schválené časové záznamy s týmto ID projektu.</span><span class="sxs-lookup"><span data-stu-id="33d00-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="33d00-115">Zvoľte možnosť **Opraviť záznamy**.</span><span class="sxs-lookup"><span data-stu-id="33d00-115">Select **Correct entries**.</span></span> <span data-ttu-id="33d00-116">Automaticky sa vytvorí nový denník korekcií s priradeným typom **Oprava času**.</span><span class="sxs-lookup"><span data-stu-id="33d00-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="33d00-117">Vybraté položky sa pridajú do denníka.</span><span class="sxs-lookup"><span data-stu-id="33d00-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="33d00-118">Na stránke **Nový denník** zadajte **Trvanie** svojho denníka korekcií a potom stlačte kartu **Opravy zadaní času**.</span><span class="sxs-lookup"><span data-stu-id="33d00-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="33d00-119">V časti **Nové hodnoty pre zadania času** aktualizujte v prípade potreby polia so správnymi informáciami.</span><span class="sxs-lookup"><span data-stu-id="33d00-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="33d00-120">Napríklad môžete zmeniť priradený projekt alebo rezervovateľný zdroj.</span><span class="sxs-lookup"><span data-stu-id="33d00-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="33d00-121">Stlačte možnosť **Ukážka**.</span><span class="sxs-lookup"><span data-stu-id="33d00-121">Select **Preview**.</span></span> <span data-ttu-id="33d00-122">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="33d00-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="33d00-123">Na karte **Záznamy v účtovnom denníku** si môžete zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými časovými položkami, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené.</span><span class="sxs-lookup"><span data-stu-id="33d00-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="33d00-124">Ak je potrebné vykonať ďalšie opravy, opakujte kroky 5 a 6.</span><span class="sxs-lookup"><span data-stu-id="33d00-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="33d00-125">Všetky opravené skutočnosti budú mať rovnaké hodnoty, aké ste vybrali v sekcii **Nové hodnoty pre zadania času**.</span><span class="sxs-lookup"><span data-stu-id="33d00-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="33d00-126">Ak sa opravy zobrazia podľa očakávania, vyberte položku **Potvrdiť**.</span><span class="sxs-lookup"><span data-stu-id="33d00-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="33d00-127">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="33d00-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="33d00-128">Vráťte sa do oblasti **Sales**, zvoľte možnosť **Projekty** a potom otvorte projekt, pre ktoré ste práve aktualizovali časové záznamy.</span><span class="sxs-lookup"><span data-stu-id="33d00-128">Return to the **Sales** area, select **Projects**, and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="33d00-129">Na stránke **Projekty** na karte **Skutočné údaje** si zobrazte vykonané zmeny.</span><span class="sxs-lookup"><span data-stu-id="33d00-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="33d00-130">Ak karta **Skutočné údaje** nie je viditeľná, zvoľte možnosť **Súvisiace** > **Skutočné údaje**.</span><span class="sxs-lookup"><span data-stu-id="33d00-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="33d00-131">V zozname **Priradené zobrazenie skutočných hodnôt** môžete vidieť, že pôvodné časové záznamy, ktoré boli zvrátené, sú stále uvedené, ako aj zodpovedajúce opravené časové položky.</span><span class="sxs-lookup"><span data-stu-id="33d00-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="33d00-132">Napríklad na nasledujúcej grafike sú dve riadkové položky s množstvom 8,00, ktorých debety sú uvedené v stĺpci Suma.</span><span class="sxs-lookup"><span data-stu-id="33d00-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="33d00-133">Ďalej sú v stĺpci Suma dve riadkové položky s množstvom -8,00, ktoré zobrazujú pripísané sumy.</span><span class="sxs-lookup"><span data-stu-id="33d00-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="33d00-134">Tieto korekcie znižujú množstvo na nulu.</span><span class="sxs-lookup"><span data-stu-id="33d00-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="33d00-135">Opravte schválené záznamy výdavkov</span><span class="sxs-lookup"><span data-stu-id="33d00-135">Correct approved expense entries</span></span>

<span data-ttu-id="33d00-136">Ak chcete opraviť jednu alebo viac položiek výdavkov, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="33d00-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="33d00-137">V oblasti **Sales** v ľavej navigačnej table v časti **Transakcie** zvoľte možnosť **Schválené výdavky**.</span><span class="sxs-lookup"><span data-stu-id="33d00-137">In the **Sales** area, in the left navigation pane, under **Transactions**, select **Approved Expenses**.</span></span>

2. <span data-ttu-id="33d00-138">V zozname **Schválené výdavky** zvoľte projekt, ktorý chcete opraviť, a potom stlačte možnosť **Opraviť záznamy**.</span><span class="sxs-lookup"><span data-stu-id="33d00-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="33d00-139">Automaticky sa vytvorí nový denník korekcií s priradeným typom **Oprava výdavku**.</span><span class="sxs-lookup"><span data-stu-id="33d00-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="33d00-140">Na stránke **Nový denník** zadajte **Opis** opravy a na karte **Oprava výdavku** v sekcii **Nové hodnoty pre výdavky** zvoľte dátové polia, ktoré chcete pri vybratých riadkoch nákladov opraviť.</span><span class="sxs-lookup"><span data-stu-id="33d00-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="33d00-141">Napríklad môžete priradiť náklady inému **Projektu** alebo opraviť **Kategória výdavku**, **Dátum výdavku** alebo **Rezervovateľný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="33d00-141">For example, you can assign the expense to another **Project**, or correct the **Expense Category**, **Expense Date**, or **Bookable Resource**.</span></span>

4. <span data-ttu-id="33d00-142">Stlačte možnosť **Ukážka**.</span><span class="sxs-lookup"><span data-stu-id="33d00-142">Select **Preview**.</span></span> <span data-ttu-id="33d00-143">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="33d00-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="33d00-144">Skontrolujte opravy na karte **Záznamy v účtovnom denníku**. Môžete si zobraziť zoznam pôvodných skutočností, ktoré súvisia s vybratými výdavkovými položkami, ktoré boli zmenené, a opravené zodpovedajúce riadky, ktoré boli vytvorené.</span><span class="sxs-lookup"><span data-stu-id="33d00-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="33d00-145">Ak sú opravené hodnoty podľa očakávania, vyberte položku **Potvrdiť**.</span><span class="sxs-lookup"><span data-stu-id="33d00-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="33d00-146">V dialógovom okne stlačte možnosť **OK**.</span><span class="sxs-lookup"><span data-stu-id="33d00-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="33d00-147">Ak sa hodnoty nezobrazujú podľa očakávania, vyberte položku **Zrušiť**, čím sa vrátite do zoznamu **Schválené výdavky**.</span><span class="sxs-lookup"><span data-stu-id="33d00-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="33d00-148">Opakujte kroky 2 až 5.</span><span class="sxs-lookup"><span data-stu-id="33d00-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="33d00-149">Opravené skutočné hodnoty budú mať rovnaké hodnoty, aké ste vybrali v sekcii **Nové hodnoty pre výdavky**.</span><span class="sxs-lookup"><span data-stu-id="33d00-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="33d00-150">Po potvrdení denníka opráv prejdite späť na projekt alebo projekty, ktoré ste aktualizovali, aby ste si prezreli zmeny.</span><span class="sxs-lookup"><span data-stu-id="33d00-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="33d00-151">Na stránke projektu na karte **Skutočné hodnoty** skontrolujte **Priradené zobrazenie skutočných hodnôt**.</span><span class="sxs-lookup"><span data-stu-id="33d00-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="33d00-152">Uvádzajú sa pôvodné záznamy a opravené položky.</span><span class="sxs-lookup"><span data-stu-id="33d00-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="33d00-153">Nasledujúca grafika zobrazuje pôvodné sumy vstupných nákladov a zodpovedajúce opravené položky vstupných nákladov.</span><span class="sxs-lookup"><span data-stu-id="33d00-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 




[!INCLUDE[footer-include](../includes/footer-banner.md)]