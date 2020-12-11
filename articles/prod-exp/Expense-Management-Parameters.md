---
title: Parametre správy výdavkov
description: Nasledujúce parametre riadia správanie v správe výdavkov.
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: af49187a3ad530919376fbfdb5a0fbc288b7c28c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084408"
---
# <a name="expense-management-parameters"></a><span data-ttu-id="03bdb-103">Parametre správy výdavkov</span><span class="sxs-lookup"><span data-stu-id="03bdb-103">Expense management parameters</span></span>

[!include [banner](../includes/banner.md)]

-----------------------------

<span data-ttu-id="03bdb-104">Parametre riadia všeobecné správanie v správe výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-104">The parameters control the general behavior in Expense management.</span></span>

### <a name="general"></a><span data-ttu-id="03bdb-105">Všeobecné</span><span class="sxs-lookup"><span data-stu-id="03bdb-105">General</span></span>

| <span data-ttu-id="03bdb-106">**Pole**</span><span class="sxs-lookup"><span data-stu-id="03bdb-106">**Field**</span></span>                                                | <span data-ttu-id="03bdb-107">**Popis**</span><span class="sxs-lookup"><span data-stu-id="03bdb-107">**Description**</span></span>                                                 |
|----------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="03bdb-108">**Štandardná sadzba na najazdené kilometre**</span><span class="sxs-lookup"><span data-stu-id="03bdb-108">**Standard rate of mileage**</span></span>                             | <span data-ttu-id="03bdb-109">Zadajte sadzbu náhrady výdavkov na najazdené kilometre.</span><span class="sxs-lookup"><span data-stu-id="03bdb-109">Enter the reimbursement rate for mileage expenses.</span></span> <span data-ttu-id="03bdb-110">Táto sadzba sa vynásobí počtom kilometrov, ktoré sa zadajú do výdavku na výpočet refundovanej sumy za cestovné náklady.</span><span class="sxs-lookup"><span data-stu-id="03bdb-110">The rate will be multiplied by the mileage entered on the expense to calculate the amount reimbursed for the travel expense.</span></span>                       |
|<span data-ttu-id="03bdb-111">**Osobné výdavky uhradené osobou**</span><span class="sxs-lookup"><span data-stu-id="03bdb-111">**Personal expenses paid by**</span></span>                             | <span data-ttu-id="03bdb-112">Vyberte, kto je zodpovedný za zaplatenie všetkých čiastok transakcií kreditnou kartou kategorizovaných ako osobné.</span><span class="sxs-lookup"><span data-stu-id="03bdb-112">Select who is responsible for paying any credit card transaction amounts categorized as personal.</span></span>                                                                                                     |
|<span data-ttu-id="03bdb-113">**Zobraziť celú správu o výdavkoch pri návrate**</span><span class="sxs-lookup"><span data-stu-id="03bdb-113">**Display entire expense report on drillback**</span></span>               | <span data-ttu-id="03bdb-114">Vyberte túto možnosť, ak chcete zobraziť všetky výdavky výkazu výdavkov, keď sa zobrazia podrobnosti pôvodného dokumentu pre konkrétny poukaz, ktorý bol vygenerovaný pri zaúčtovaní výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-114">Select this option to display all expenses for an expense report when viewing the details of the original document for a specific voucher that was generated when the expense report was posted.</span></span>              |
|<span data-ttu-id="03bdb-115">**Predbežná autorizácia cesty je povinná**</span><span class="sxs-lookup"><span data-stu-id="03bdb-115">**Pre-authorization of travel is mandatory**</span></span>                 | <span data-ttu-id="03bdb-116">Vyberte túto možnosť, ak chcete, aby zamestnanec mohol predložiť správu o výdavkoch, aby bola predložená a schválená cestovná požiadavka.</span><span class="sxs-lookup"><span data-stu-id="03bdb-116">Select this option to require that a travel requisition be submitted and approved before an employee can submit an expense report.</span></span>                                                                    |
|<span data-ttu-id="03bdb-117">**Pred uverejnením príspevku povoľte úpravy distribúcií**</span><span class="sxs-lookup"><span data-stu-id="03bdb-117">**Allow editing of distributions before posting**</span></span>            | <span data-ttu-id="03bdb-118">Vyberte, či možno rozdelenia výkazu výdavkov upravovať pred zaúčtovaním.</span><span class="sxs-lookup"><span data-stu-id="03bdb-118">Select whether the distributions of an expense report can be edited prior to posting.</span></span>                                                                                                                 |
|<span data-ttu-id="03bdb-119">**Vyhodnoťte politiky riadenia výdavkov**</span><span class="sxs-lookup"><span data-stu-id="03bdb-119">**Evaluate expense management policies**</span></span>                     | <span data-ttu-id="03bdb-120">Vyberte, kedy sa majú výdavky vyhodnocovať, aby ste určili, či došlo k porušeniu politiky výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-120">Select when expenses are evaluated to determine if an expense policy has been violated.</span></span> <span data-ttu-id="03bdb-121">Porušenie výdavkov je možné skontrolovať pri zadaní a uložení záznamu o výdavkoch alebo po predložení výdavku na schválenie.</span><span class="sxs-lookup"><span data-stu-id="03bdb-121">Expenses can be checked for violations when the expense entry is entered and saved or when the expense is submitted for approval.</span></span> <span data-ttu-id="03bdb-122">Po uložení riadku výdavkov sa skontrolujú pravidlá politiky pre požadované potvrdenia.</span><span class="sxs-lookup"><span data-stu-id="03bdb-122">The policy rules for receipts required will be checked when the expense line is saved.</span></span>                   |
|<span data-ttu-id="03bdb-123">**Povoliť medzipodnikové výdavkové riadky**</span><span class="sxs-lookup"><span data-stu-id="03bdb-123">**Allow intercompany expense lines**</span></span>                         | <span data-ttu-id="03bdb-124">Vyberte, či je možné do výkazu výdavkov zadávať výdavky pre iné právnické osoby.</span><span class="sxs-lookup"><span data-stu-id="03bdb-124">Select whether to allow entry of expenses for other legal entities within an expense report.</span></span>                                                                                                          |
|<span data-ttu-id="03bdb-125">**Povoliť úpravy výmenného kurzu výdavkov kreditnej karty**</span><span class="sxs-lookup"><span data-stu-id="03bdb-125">**Allow editing the exchange rate for credit card expenses**</span></span> | <span data-ttu-id="03bdb-126">Vyberte túto možnosť, aby ste používateľovi umožnili upravovať výmenný kurz importovaných výdavkov na kreditnú kartu.</span><span class="sxs-lookup"><span data-stu-id="03bdb-126">Select this option to allow the user to edit the exchange rate for imported credit card expenses.</span></span>                                                                        |
|<span data-ttu-id="03bdb-127">**Polia viacúrovňovej hierarchie, ktoré sa majú zobraziť**</span><span class="sxs-lookup"><span data-stu-id="03bdb-127">**Multi-level hierarchy fields to display**</span></span>                  | <span data-ttu-id="03bdb-128">Vyberte, ktoré polia schvaľovateľa sa zobrazia, keď je typ priradenia pracovného postupu výkazu výdavkov nastavený na hierarchiu, a výber Hierarchia je nastavený na použitie hierarchie viacúrovňového schválenia výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-128">Select which approver fields to display when the expense report workflow assignment type is set to be hierarchy and the hierarchy selection is set to use the Expense multi-level approval hierarchy.</span></span> <span data-ttu-id="03bdb-129">Keď sa pre pracovný postup použije viacúrovňová schvaľovacia hierarchia, vybraté polia sa zobrazia a môžu sa upravovať vo výkaze výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-129">When the multi-level approval hierarchy is used for workflow, the selected fields will be displayed and editable in the Expense report.</span></span> |
|<span data-ttu-id="03bdb-130">**Zadajte číslo kreditnej karty zamestnanca (aktualizácia z júla 2017)**</span><span class="sxs-lookup"><span data-stu-id="03bdb-130">**Enter employee credit card number (July 2017 update)**</span></span>     | <span data-ttu-id="03bdb-131">Vyberte, či možno zadať 15- alebo 16-znakové číslo a uložiť ho do poľa **ID karty** na stránke **Kreditné karty** pre zamestnanca.</span><span class="sxs-lookup"><span data-stu-id="03bdb-131">Select whether a 15-or 16-character number can be entered and saved in the **Card ID** field in the **Credit cards** page for an employee.</span></span>                                                                          |

### <a name="financial"></a><span data-ttu-id="03bdb-132">Financial</span><span class="sxs-lookup"><span data-stu-id="03bdb-132">Financial</span></span>

| <span data-ttu-id="03bdb-133">**Pole**</span><span class="sxs-lookup"><span data-stu-id="03bdb-133">**Field**</span></span>                                                            | <span data-ttu-id="03bdb-134">**Opis**</span><span class="sxs-lookup"><span data-stu-id="03bdb-134">**Description**</span></span>     |
|----------------------------------------------------------------------|------------------------------------|
|<span data-ttu-id="03bdb-135">**Názov denného účtovného denníka hlavnej knihy**</span><span class="sxs-lookup"><span data-stu-id="03bdb-135">**Ledger daily journal name**</span></span>                                         | <span data-ttu-id="03bdb-136">Vyberte názov denníka hlavnej knihy, do ktorého sa účtujú schválené výkazy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-136">Select the name of the ledger journal that approved expense reports are posted to.</span></span>            |
|<span data-ttu-id="03bdb-137">**Povoliť vrátenie daní z výdavkov**</span><span class="sxs-lookup"><span data-stu-id="03bdb-137">**Enable tax recovery from expenses**</span></span>                                  | <span data-ttu-id="03bdb-138">Vyberte túto možnosť, ak chcete povoliť vrátenie dane z výdavkov pre oprávnené výdavky.</span><span class="sxs-lookup"><span data-stu-id="03bdb-138">Select this option to enable expense tax recovery for eligible expenses.</span></span> <span data-ttu-id="03bdb-139">Túto možnosť nie je možné povoliť, ak sú povolené americké dane z obratu a dane z používania.</span><span class="sxs-lookup"><span data-stu-id="03bdb-139">This option cannot be enabled if US sales tax and use tax rules are enabled.</span></span>      |
|<span data-ttu-id="03bdb-140">**Okamžité zverejnenie platby vopred v hotovosti**</span><span class="sxs-lookup"><span data-stu-id="03bdb-140">**Post cash advances immediately**</span></span>                                     | <span data-ttu-id="03bdb-141">Vyberte túto možnosť, ak chcete po dokončení procesu platby a prevodu zaúčtovať schválenú platbu vopred v hotovosti.</span><span class="sxs-lookup"><span data-stu-id="03bdb-141">Select this option to post an approved cash advance when the process to Pay and transfer is completed.</span></span> <span data-ttu-id="03bdb-142">Ak táto možnosť nie je vybratá, proces platby a prevodu vygeneruje nezverejnený všeobecný denník.</span><span class="sxs-lookup"><span data-stu-id="03bdb-142">If this option is not selected, the Pay and transfer process will generate an unposted general journal.</span></span> |
|<span data-ttu-id="03bdb-143">**Správny účtovný dátum počas zverejnenia**</span><span class="sxs-lookup"><span data-stu-id="03bdb-143">**Correct accounting date during posting**</span></span>                             | <span data-ttu-id="03bdb-144">Vyberte túto možnosť, ak chcete aktualizovať účtovný dátum pri zaúčtovaní výdavkov, ak je súčasné obdobie pozastavené alebo uzavreté.</span><span class="sxs-lookup"><span data-stu-id="03bdb-144">Select this option to update the accounting date when posting expenses if the current period is on hold or closed.</span></span> <span data-ttu-id="03bdb-145">Účtovný dátum bude nastavený na nasledujúce otvorené obdobie.</span><span class="sxs-lookup"><span data-stu-id="03bdb-145">The accounting date will be set to the next open period.</span></span>   |
|<span data-ttu-id="03bdb-146">**Povoliť zoskupovanie transakcií na základe účtu s odchýlkami uvedeného v spôsobe platby**</span><span class="sxs-lookup"><span data-stu-id="03bdb-146">**Allow grouping of transactions based on offset account specified in payment method**</span></span>      | <span data-ttu-id="03bdb-147">Vyberte túto možnosť, ak chcete zosumarizovať nákladové transakcie pre výkaz výdavkov na základe účtu s odchýlkami, ktorý je uvedený v spôsobe platby pre výdavky.</span><span class="sxs-lookup"><span data-stu-id="03bdb-147">Select this option to summarize the expense transactions for an expense report, based on the offset account specified in the payment method for the expenses.</span></span>   
|<span data-ttu-id="03bdb-148">**Vrátane dane**</span><span class="sxs-lookup"><span data-stu-id="03bdb-148">**Tax included**</span></span>                                                   | <span data-ttu-id="03bdb-149">Vyberte túto možnosť, ak chcete do sumy výdavkov predvolene zahrnúť daň z predaja.</span><span class="sxs-lookup"><span data-stu-id="03bdb-149">Select this option to include sales tax in the expense amount by default.</span></span>             |
|<span data-ttu-id="03bdb-150">**Uvoľniť ťarchy pri zatváraní cestovných požiadaviek**</span><span class="sxs-lookup"><span data-stu-id="03bdb-150">**Release encumbrances on closing travel requisitions**</span></span>            | <span data-ttu-id="03bdb-151">Vyberte túto možnosť, aby ste uvoľnili zaťažené prostriedky po zatvorení schválenej cestovnej požiadavky.</span><span class="sxs-lookup"><span data-stu-id="03bdb-151">Select this option to release encumbered funds when an approved travel requisition is closed.</span></span>                                                                                   |
|<span data-ttu-id="03bdb-152">**Povoliť predloženie cestovnej požiadavky pri prekročení rozpočtu pre register rozpočtu a rozpočet projektu**</span><span class="sxs-lookup"><span data-stu-id="03bdb-152">**Allow travel requisition submit on budget overrun for budget register and project budget**</span></span> | <span data-ttu-id="03bdb-153">Vyberte túto možnosť, aby ste zamestnancom umožnili predkladať cestovné požiadavky na schválenie, ktoré presahujú povolený rozpočet nastavený v registri rozpočtu alebo povolený rozpočet projektu.</span><span class="sxs-lookup"><span data-stu-id="03bdb-153">Select this option to allow employees to submit travel requisitions for approval that exceed either the allowed budget that is set in the budget register or the allowed budget for a project.</span></span>            |
|<span data-ttu-id="03bdb-154">**Povoliť predloženie výkazu výdavkov pri prekročení rozpočtu pre register rozpočtu a rozpočet projektu**</span><span class="sxs-lookup"><span data-stu-id="03bdb-154">**Allow expense report submit on budget overrun for budget register and project budget**</span></span>    | <span data-ttu-id="03bdb-155">Vyberte túto možnosť, aby ste zamestnancom umožnili predkladať výkazy výdavkov na schválenie, ktoré presahujú povolený rozpočet nastavený v registri rozpočtu alebo povolený rozpočet projektu.</span><span class="sxs-lookup"><span data-stu-id="03bdb-155">Select this option to allow employees to submit expense reports for approval that exceed either the allowed budget that is set in the budget register or the allowed budget for a project.</span></span>                |
|<span data-ttu-id="03bdb-156">**Povoliť schválenie výkazu výdavkov pri prekročení rozpočtu iba pre register rozpočtu**</span><span class="sxs-lookup"><span data-stu-id="03bdb-156">**Allow expense report approval on budget overrun for budget register only**</span></span>                | <span data-ttu-id="03bdb-157">Vyberte túto možnosť, aby ste schvaľovateľom umožnili schvaľovať výkazy výdavkov, ktoré presahujú povolený rozpočet nastavený v registri rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="03bdb-157">Select this option to allow approvers to approve expense reports that exceed the allowed budget that is set in the budget register.</span></span>                                                                       |

### <a name="per-diem"></a><span data-ttu-id="03bdb-158">Denne</span><span class="sxs-lookup"><span data-stu-id="03bdb-158">Per diem</span></span>

| <span data-ttu-id="03bdb-159">**Pole**</span><span class="sxs-lookup"><span data-stu-id="03bdb-159">**Field**</span></span>                             | <span data-ttu-id="03bdb-160">**Popis**</span><span class="sxs-lookup"><span data-stu-id="03bdb-160">**Description**</span></span>             |
|---------------------------------------|--------------------------------------------------------------------------------------|
|<span data-ttu-id="03bdb-161">**Minimálne hodiny pre diéty**</span><span class="sxs-lookup"><span data-stu-id="03bdb-161">**Minimum hours for per diem**</span></span>           | <span data-ttu-id="03bdb-162">Zadajte predvolený minimálny počet hodín, ktoré musí zamestnanec za deň odpracovať, aby mohol dostávať diéty za cestovné náklady.</span><span class="sxs-lookup"><span data-stu-id="03bdb-162">Enter the default minimum number of hours that an employee must work in a day to be eligible to receive a per diem for travel-related expenses.</span></span>  <span data-ttu-id="03bdb-163">Táto hodnota sa používa ako predvolená hodnota iba pre pole Minimálne hodiny pre úrovne denných diét.</span><span class="sxs-lookup"><span data-stu-id="03bdb-163">This value is only used as a default value for the Minimum hours field on per diem rate tiers.</span></span>                                                                                      |
|<span data-ttu-id="03bdb-164">**Percento jedla**</span><span class="sxs-lookup"><span data-stu-id="03bdb-164">**Meal percent**</span></span>                          | <span data-ttu-id="03bdb-165">Zadajte predvolené percento diét ktoré sa používa v prvý a posledný deň výdavkov spojených s cestovaním, keď je pole **Vypočítať zníženie stravného o** je nastavené buď na **Typ jedla za deň** alebo **Počet jedál za deň**.</span><span class="sxs-lookup"><span data-stu-id="03bdb-165">Enter the default percentage of the per diem for meals that is used on the first and last days of the travel-related expense when the **Calculate meal reduction by** field is set to either **Meal type per day** or **Number of meals per day**.</span></span> <span data-ttu-id="03bdb-166">Pracovný deň v prvý a posledný deň môže byť kratší ako štandardný pracovný deň.</span><span class="sxs-lookup"><span data-stu-id="03bdb-166">The work day on the first and last days may be shorter than a standard work day.</span></span> <span data-ttu-id="03bdb-167">Preto sa výška diét v tieto dni môže líšiť od štandardnej sumy.</span><span class="sxs-lookup"><span data-stu-id="03bdb-167">Therefore, the amount of the per diem on these days may differ from the standard amount.</span></span> <span data-ttu-id="03bdb-168">Ak je percento nastavené na 0, odpočty prvého a posledného dňa budú 0,00.</span><span class="sxs-lookup"><span data-stu-id="03bdb-168">If the percent is set to 0, then the first and last day deductions will be 0.00.</span></span> |
|<span data-ttu-id="03bdb-169">**Percentá pre hotel**</span><span class="sxs-lookup"><span data-stu-id="03bdb-169">**Hotel percent**</span></span>                        | <span data-ttu-id="03bdb-170">Zadajte predvolené percento diéty pre hotely, ktoré sa používajú v prvý a posledný deň výdavkov spojených s cestovaním.</span><span class="sxs-lookup"><span data-stu-id="03bdb-170">Enter the default percentage of the per diem for hotels that is used on the first and last days of the travel-related expense.</span></span> <span data-ttu-id="03bdb-171">Pracovný deň v prvý a posledný deň môže byť kratší ako štandardný pracovný deň.</span><span class="sxs-lookup"><span data-stu-id="03bdb-171">The work day on the first and last days may be shorter than a standard work day.</span></span> <span data-ttu-id="03bdb-172">Preto sa výška diét v tieto dni môže líšiť od štandardnej sumy.</span><span class="sxs-lookup"><span data-stu-id="03bdb-172">Therefore, the amount of the per diem on these days may differ from the standard amount.</span></span> <span data-ttu-id="03bdb-173">Ak je percento nastavené na 0, odpočty prvého a posledného dňa budú 0,00.</span><span class="sxs-lookup"><span data-stu-id="03bdb-173">If the percent is set to 0, then the first and last day deductions will be 0.00.</span></span>                                              |
|<span data-ttu-id="03bdb-174">**Ostatné percentá**</span><span class="sxs-lookup"><span data-stu-id="03bdb-174">**Other percent**</span></span>                        | <span data-ttu-id="03bdb-175">Zadajte predvolené percento diéty pre rôzne výdavky, ktoré sa používajú v prvý a posledný deň výdavkov spojených s cestovaním.</span><span class="sxs-lookup"><span data-stu-id="03bdb-175">Enter the default percentage of the per diem for miscellaneous expenses that is used on the first and last days of the travel-related expense.</span></span> <span data-ttu-id="03bdb-176">Pracovný deň v prvý a posledný deň môže byť kratší ako štandardný pracovný deň.</span><span class="sxs-lookup"><span data-stu-id="03bdb-176">The work day on the first and last days may be shorter than a standard work day.</span></span> <span data-ttu-id="03bdb-177">Preto sa výška diét v tieto dni môže líšiť od štandardnej sumy.</span><span class="sxs-lookup"><span data-stu-id="03bdb-177">Therefore, the amount of the per diem on these days may differ from the standard amount.</span></span> <span data-ttu-id="03bdb-178">Ak je percento nastavené na 0, odpočty prvého a posledného dňa budú 0,00.</span><span class="sxs-lookup"><span data-stu-id="03bdb-178">If the percent is set to 0, then the first and last day deductions will be 0.00.</span></span>                                                                                                     |
|<span data-ttu-id="03bdb-179">**Zníženie percenta na raňajky**</span><span class="sxs-lookup"><span data-stu-id="03bdb-179">**Reduction in percentage for breakfast**</span></span> | <span data-ttu-id="03bdb-180">Zadajte čiastku, o ktorú sa diéty znižujú na raňajky.</span><span class="sxs-lookup"><span data-stu-id="03bdb-180">Enter the amount that the per diem is reduced for breakfast.</span></span> <span data-ttu-id="03bdb-181">Napríklad, ak zamestnanec dostane bezplatné raňajky, možno budete chcieť znížiť sumu diét o 10 percent.</span><span class="sxs-lookup"><span data-stu-id="03bdb-181">For example, if an employee receives a complimentary breakfast, you may want to reduce the amount of the per diem by 10 percent.</span></span>                               |
|<span data-ttu-id="03bdb-182">**Zníženie percenta na obed**</span><span class="sxs-lookup"><span data-stu-id="03bdb-182">**Reduction in percentage for lunch**</span></span>    | <span data-ttu-id="03bdb-183">Zadajte čiastku, o ktorú sa diéty znižujú na obed.</span><span class="sxs-lookup"><span data-stu-id="03bdb-183">Enter the amount that the per diem is reduced for lunch.</span></span> <span data-ttu-id="03bdb-184">Napríklad, ak zamestnanec dostane bezplatný obed, možno budete chcieť znížiť sumu diét o 15 percent.</span><span class="sxs-lookup"><span data-stu-id="03bdb-184">For example, if an employee receives a complimentary lunch, you may want to reduce the amount of the per diem by 15 percent.</span></span>                                       |
|<span data-ttu-id="03bdb-185">**Zníženie percenta na večeru**</span><span class="sxs-lookup"><span data-stu-id="03bdb-185">**Reduction in percentage for dinner**</span></span>   | <span data-ttu-id="03bdb-186">Zadajte čiastku, o ktorú sa diéty znižujú na večeru.</span><span class="sxs-lookup"><span data-stu-id="03bdb-186">Enter the amount that the per diem is reduced for dinner.</span></span> <span data-ttu-id="03bdb-187">Napríklad, ak zamestnanec dostane bezplatnú večeru, možno budete chcieť znížiť sumu diét o 25 percent.</span><span class="sxs-lookup"><span data-stu-id="03bdb-187">For example, if an employee receives a complimentary dinner, you may want to reduce the amount of the per diem by 25 percent.</span></span>                                     |
|<span data-ttu-id="03bdb-188">**Vypočítať zníženie jedla o**</span><span class="sxs-lookup"><span data-stu-id="03bdb-188">**Calculate meal reduction by**</span></span>         | <span data-ttu-id="03bdb-189">Vyberte, ako má systém vypočítať zníženie denných diét výberom, či je zníženie založené na type jedla na cestu alebo na deň, alebo či je zníženie založené na počte povolených jedál za deň.</span><span class="sxs-lookup"><span data-stu-id="03bdb-189">Select how the system should calculate the per diem meal reduction by selecting if the reduction is based on the meal type per trip or per day, or if the reduction is based on the number of meals allowed per day.</span></span>|
|<span data-ttu-id="03bdb-190">**Zaokrúhľovanie diét**</span><span class="sxs-lookup"><span data-stu-id="03bdb-190">**Per diem rounding**</span></span>                  | <span data-ttu-id="03bdb-191">Vyberte typ zaokrúhľovania, ktorý sa použije pri výdavkoch na diéty.</span><span class="sxs-lookup"><span data-stu-id="03bdb-191">Select the type of rounding that is used for per diem expenses.</span></span> <span data-ttu-id="03bdb-192">Ak vyberiete bežné zaokrúhľovanie, všetky náklady na diéty, ktoré majú čiastku 0,50, sa zaokrúhlia na 1,00 a všetky diéty, ktoré majú menej ako 0,50, sa zaokrúhlia nadol na 0,00.</span><span class="sxs-lookup"><span data-stu-id="03bdb-192">If you select normal rounding, any per diem expense that has an amount of 0.50 is rounded up to 1.00, and any per diem expense that has an amount that is less than 0.50 is rounded down to 0.00.</span></span>                                                                                              |
|<span data-ttu-id="03bdb-193">**Výpočet základu diéty na**</span><span class="sxs-lookup"><span data-stu-id="03bdb-193">**Base per diem calculation on**</span></span>         | <span data-ttu-id="03bdb-194">Vyberte, či sa výška diéty zakladá na kalendárnom dni alebo 24-hodinovom období.</span><span class="sxs-lookup"><span data-stu-id="03bdb-194">Select whether a per diem amount is based on a calendar day or a 24-hour period.</span></span>       |

### <a name="fax-cover-pages"></a><span data-ttu-id="03bdb-195">Titulné strany faxu</span><span class="sxs-lookup"><span data-stu-id="03bdb-195">Fax cover pages</span></span>

| <span data-ttu-id="03bdb-196">**Pole**</span><span class="sxs-lookup"><span data-stu-id="03bdb-196">**Field**</span></span>                      | <span data-ttu-id="03bdb-197">**Popis**</span><span class="sxs-lookup"><span data-stu-id="03bdb-197">**Description**</span></span>            |
|--------------------------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="03bdb-198">**Pokyny**</span><span class="sxs-lookup"><span data-stu-id="03bdb-198">**Instructions**</span></span>                   | <span data-ttu-id="03bdb-199">Zadajte pokyny, ktoré musia zamestnanci dodržiavať pri vytváraní titulnej stránky pre fax, ktorý sa používa na odosielanie potvrdeniek týkajúcich sa výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-199">Enter the instructions that employees must follow when they create a cover page for a fax that is used to send receipts that are related to an expense report.</span></span> <span data-ttu-id="03bdb-200">Kliknutím na tlačidlo **Preklady** zadajte text, ktorý sa zobrazí v konkrétnom jazyku, na základe jazyka používateľa.</span><span class="sxs-lookup"><span data-stu-id="03bdb-200">Click the **Translations** button to enter language-specific text that will be displayed based on the user language.</span></span> |
|<span data-ttu-id="03bdb-201">**ID používateľa (informácie o čiarovom kóde)**</span><span class="sxs-lookup"><span data-stu-id="03bdb-201">**User ID (Bar code information)**</span></span> | <span data-ttu-id="03bdb-202">Vyberte túto možnosť, ak chcete uložiť jedinečný identifikátor zamestnanca do čiarového kódu použitého na titulnej strane faxu.</span><span class="sxs-lookup"><span data-stu-id="03bdb-202">Select this option to store an employee’s unique identifier in the bar code that is used on the cover page of the fax.</span></span>                 |
|<span data-ttu-id="03bdb-203">**Čiarový kód**</span><span class="sxs-lookup"><span data-stu-id="03bdb-203">**Bar code**</span></span>                      | <span data-ttu-id="03bdb-204">Vyberte čiarový kód, ktorý sa použije na titulnej strane faxu.</span><span class="sxs-lookup"><span data-stu-id="03bdb-204">Select the bar code that is used on the cover page of the fax.</span></span> <span data-ttu-id="03bdb-205">V správe výdavkov sú podporované čiarové kódy 39 a 128.</span><span class="sxs-lookup"><span data-stu-id="03bdb-205">Bar codes 39 and 128 are supported with Expense management.</span></span>               |

### <a name="anti-corruption"></a><span data-ttu-id="03bdb-206">Protikorupčné opatrenia</span><span class="sxs-lookup"><span data-stu-id="03bdb-206">Anti-corruption</span></span>

|                 <span data-ttu-id="03bdb-207"><strong>Pole</strong></span><span class="sxs-lookup"><span data-stu-id="03bdb-207"><strong>Field</strong></span></span>                 |                                                                                                                                                                                            <span data-ttu-id="03bdb-208"><strong>Opis</strong></span><span class="sxs-lookup"><span data-stu-id="03bdb-208"><strong>Description</strong></span></span>                                                                                                                                                                                             |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  <span data-ttu-id="03bdb-209"><strong>Zobraziť protikorupčné osvedčenie</strong></span><span class="sxs-lookup"><span data-stu-id="03bdb-209"><strong>Display anti-corruption attestation</strong></span></span>  | <span data-ttu-id="03bdb-210">Vyberte túto možnosť, ak chcete zobraziť protikorupčný text pri vytváraní nového výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-210">Select this option to display the anti-corruption text when creating a new expense report.</span></span> <span data-ttu-id="03bdb-211">Potom je možné povoliť konkrétne kategórie výdavkov, ktoré budú vyžadovať výber protikorupčného osvedčenia vo výkaze výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-211">Specific expense categories can then be enabled that will require the anti-corruption attestation to be selected on the expense report.</span></span> <span data-ttu-id="03bdb-212">Napríklad kategória darčekov, ktorá sa týka výdavkov vládnej organizácie, môže vyžadovať, aby zamestnanec potvrdil, že výdavky zodpovedajú politike spoločnosti, ktorá sa týka úradníkov vládnej organizácie.</span><span class="sxs-lookup"><span data-stu-id="03bdb-212">For example, a gift category related to a government official expense may require the employee to confirm that the expense meets company policy related to government officials.</span></span> |
| <span data-ttu-id="03bdb-213"><strong>Protikorupčná správa pre zadávateľa</strong></span><span class="sxs-lookup"><span data-stu-id="03bdb-213"><strong>Anti-corruption message for submitter</strong></span></span> |                                                                                             <span data-ttu-id="03bdb-214">Zadajte text, ktorý sa zamestnancovi zobrazí pri vytváraní nového výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-214">Enter the text that will be displayed to the employee when creating a new expense report.</span></span> <span data-ttu-id="03bdb-215">Kliknutím na tlačidlo <strong>Preklady</strong> zadajte text, ktorý sa zobrazí v konkrétnom jazyku, na základe jazyka používateľa.</span><span class="sxs-lookup"><span data-stu-id="03bdb-215">Click the <strong>Translations</strong> button to enter language specific text that will be displayed based on the user language.</span></span>                                                                                             |
| <span data-ttu-id="03bdb-216"><strong>Protikorupčná správa pre schvaľovateľa</strong></span><span class="sxs-lookup"><span data-stu-id="03bdb-216"><strong>Anti-corruption message for approver</strong></span></span>  |                                                                                             <span data-ttu-id="03bdb-217">Zadajte text, ktorý sa schvaľovateľovi zobrazí pri vytváraní nového výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="03bdb-217">Enter the text that will be displayed to the approver when creating a new expense report.</span></span> <span data-ttu-id="03bdb-218">Kliknutím na tlačidlo <strong>Preklady</strong> zadajte text, ktorý sa zobrazí v konkrétnom jazyku, na základe jazyka používateľa.</span><span class="sxs-lookup"><span data-stu-id="03bdb-218">Click the <strong>Translations</strong> button to enter language specific text that will be displayed based on the user language.</span></span>                                                                                             |
