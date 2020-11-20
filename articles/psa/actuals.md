---
title: Prehľad skutočných hodnôt
description: Táto téma poskytuje informácie o skutočných údajoch projektu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: cf9e36c99790b77f0ed6490f49b4ebeb043bcdf6
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129787"
---
# <a name="actuals-overview"></a><span data-ttu-id="d32a7-103">Prehľad skutočných hodnôt</span><span class="sxs-lookup"><span data-stu-id="d32a7-103">Actuals overview</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d32a7-104">Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte.</span><span class="sxs-lookup"><span data-stu-id="d32a7-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d32a7-105">Skutočné údaje projektu možno vystopovať späť do svojich zdrojových dokladov.</span><span class="sxs-lookup"><span data-stu-id="d32a7-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="d32a7-106">Tieto zdrojové doklady zahŕňajú čas, výdavky a účtovné záznamy, ako aj faktúry.</span><span class="sxs-lookup"><span data-stu-id="d32a7-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Ako vystopovať skutočné údaje projektov na zdrojové dokumenty](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="d32a7-108">Odoslanie časovej položky</span><span class="sxs-lookup"><span data-stu-id="d32a7-108">Submitting a time entry</span></span>

<span data-ttu-id="d32a7-109">V PSA, keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="d32a7-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d32a7-110">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="d32a7-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d32a7-111">Keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="d32a7-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="d32a7-112">Logika pre zadávanie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="d32a7-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="d32a7-113">Všetky hodnoty polí z časového záznamu sa skopírujú do účtovného denníka.</span><span class="sxs-lookup"><span data-stu-id="d32a7-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="d32a7-114">Tieto polia zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="d32a7-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="d32a7-115">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka**, spôsobujú, že v zázname účtovného denníka sa predvolene zadá primeraná cena.</span><span class="sxs-lookup"><span data-stu-id="d32a7-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="d32a7-116">Ak do časového záznamu pridáte vlastné pole a chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočná entita a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných údajov.</span><span class="sxs-lookup"><span data-stu-id="d32a7-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="d32a7-117">Odoslanie výdavkového záznamu</span><span class="sxs-lookup"><span data-stu-id="d32a7-117">Submitting an expense entry</span></span>

<span data-ttu-id="d32a7-118">V PSA, keď je predložený výdavkový záznam položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="d32a7-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="d32a7-119">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="d32a7-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="d32a7-120">Keď je predložený výdavkový záznam pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="d32a7-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="d32a7-121">Logika pre zadávanie predvolených cien výdavkov je založená na kategórii výdavkov, ktorá je vybratá na stránke **Výdavkový záznam**.</span><span class="sxs-lookup"><span data-stu-id="d32a7-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="d32a7-122">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="d32a7-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d32a7-123">Pre samotnú cenu však čiastka zadaná používateľom je nastavená priamo na súvisiace výdavkové záznamy účtovného denníka pre náklady a predaje predvolene.</span><span class="sxs-lookup"><span data-stu-id="d32a7-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="d32a7-124">V aktuálnej verzii PSA, kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="d32a7-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="d32a7-125">Používanie účtovných záznamov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="d32a7-126">V PSA vám účtovné záznamy umožňujú zaznamenávať náklady alebo výnosy materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="d32a7-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d32a7-127">Denník má hlavičku, riadky a **Potvrdiť** akciu.</span><span class="sxs-lookup"><span data-stu-id="d32a7-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="d32a7-128">Tu je niekoľko scenárov, v ktorých možno použiť denník:</span><span class="sxs-lookup"><span data-stu-id="d32a7-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="d32a7-129">Musíte zaznamenať skutočné materiálne náklady a predaj na projekte.</span><span class="sxs-lookup"><span data-stu-id="d32a7-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="d32a7-130">Musíte presunúť transakcie skutočných údajov z iného systému na PSA.</span><span class="sxs-lookup"><span data-stu-id="d32a7-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="d32a7-131">Musíte zaznamenať náklady, ktoré sa vyskytli v inom systéme, ako napríklad obstarávacie alebo subdodávateľské náklady.</span><span class="sxs-lookup"><span data-stu-id="d32a7-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d32a7-132">Účtovné záznamy by mal na vytváranie skutočných hodnôt používať iba používateľ, ktorý si je plne vedomý účtovného dopadu skutočných hodnôt na projekt.</span><span class="sxs-lookup"><span data-stu-id="d32a7-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="d32a7-133">Dôvodom je, že aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="d32a7-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d32a7-134">Z dôvodu dopadu tohto typu záznamu v účtovnom denníku buďte pri vytváraní účtovných záznamov primerane opatrní.</span><span class="sxs-lookup"><span data-stu-id="d32a7-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="d32a7-135">Zaznamenávanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="d32a7-135">Recording actuals based on project events</span></span>

<span data-ttu-id="d32a7-136">PSA zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="d32a7-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d32a7-137">Tieto transakcie sa zaznamenávajú ako **skutočné údaje**.</span><span class="sxs-lookup"><span data-stu-id="d32a7-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="d32a7-138">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="d32a7-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="d32a7-139">**Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="d32a7-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d32a7-140">Udalosť</span><span class="sxs-lookup"><span data-stu-id="d32a7-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d32a7-141">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="d32a7-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d32a7-142">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="d32a7-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d32a7-143">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="d32a7-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d32a7-144">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="d32a7-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d32a7-145">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d32a7-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d32a7-146">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="d32a7-146">Actuals</span></span></th>
<th><span data-ttu-id="d32a7-147">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d32a7-147">Transaction currency</span></span></th>
<th><span data-ttu-id="d32a7-148">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d32a7-148">Fixed price</span></span></th>
<th><span data-ttu-id="d32a7-149">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d32a7-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d32a7-150">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="d32a7-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d32a7-151">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d32a7-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-152">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="d32a7-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d32a7-153">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d32a7-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d32a7-154">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d32a7-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d32a7-155">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-155">Cost actual</span></span></td>
<td><span data-ttu-id="d32a7-156">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-157">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-158">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d32a7-159">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-160">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-161">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="d32a7-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d32a7-162">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d32a7-163">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d32a7-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d32a7-164">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-164">Cost actual</span></span></td>
<td><span data-ttu-id="d32a7-165">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-166">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-167">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-168">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-169">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-170">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d32a7-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d32a7-171">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-172">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d32a7-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d32a7-173">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d32a7-174">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="d32a7-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d32a7-175">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d32a7-176">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-177">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d32a7-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-178">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-179">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-180">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-181">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-181">Billed sales</span></span></td>
<td><span data-ttu-id="d32a7-182">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d32a7-183">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="d32a7-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d32a7-184">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d32a7-185">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-186">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-187">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-188">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-189">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-190">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d32a7-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d32a7-191">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-192">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d32a7-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d32a7-193">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d32a7-194">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d32a7-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d32a7-195">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d32a7-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d32a7-196">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d32a7-197">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d32a7-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d32a7-198">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="d32a7-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d32a7-199">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-200">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-201">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-202">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-202">Billed sales</span></span></td>
<td><span data-ttu-id="d32a7-203">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d32a7-204">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d32a7-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d32a7-205">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d32a7-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d32a7-206">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-207">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d32a7-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d32a7-208">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-209">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d32a7-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d32a7-210">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="d32a7-211">**Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="d32a7-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d32a7-212">Udalosť</span><span class="sxs-lookup"><span data-stu-id="d32a7-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d32a7-213">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="d32a7-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d32a7-214">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="d32a7-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d32a7-215">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="d32a7-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d32a7-216">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="d32a7-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d32a7-217">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d32a7-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d32a7-218">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="d32a7-218">Actuals</span></span></th>
<th><span data-ttu-id="d32a7-219">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d32a7-219">Transaction currency</span></span></th>
<th><span data-ttu-id="d32a7-220">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d32a7-220">Fixed price</span></span></th>
<th><span data-ttu-id="d32a7-221">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d32a7-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d32a7-222">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="d32a7-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d32a7-223">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d32a7-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-224">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="d32a7-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d32a7-225">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d32a7-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d32a7-226">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d32a7-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d32a7-227">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-227">Cost actual</span></span></td>
<td><span data-ttu-id="d32a7-228">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d32a7-229">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d32a7-230">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d32a7-231">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d32a7-232">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-233">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="d32a7-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d32a7-234">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-235">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d32a7-236">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-237">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="d32a7-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d32a7-238">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d32a7-239">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d32a7-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d32a7-240">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-240">Cost actual</span></span></td>
<td><span data-ttu-id="d32a7-241">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-242">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-243">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-244">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-245">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d32a7-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-246">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d32a7-247">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-248">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="d32a7-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d32a7-249">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d32a7-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-250">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d32a7-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d32a7-251">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-252">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d32a7-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d32a7-253">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d32a7-254">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="d32a7-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d32a7-255">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d32a7-256">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-257">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d32a7-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-258">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-259">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d32a7-260">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-261">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-261">Billed sales</span></span></td>
<td><span data-ttu-id="d32a7-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d32a7-263">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="d32a7-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d32a7-264">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d32a7-265">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-266">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-267">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-268">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d32a7-269">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-270">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d32a7-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d32a7-271">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-272">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d32a7-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d32a7-273">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d32a7-274">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d32a7-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d32a7-275">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d32a7-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d32a7-276">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d32a7-277">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d32a7-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d32a7-278">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="d32a7-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d32a7-279">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-280">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d32a7-281">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d32a7-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-282">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d32a7-282">Billed sales</span></span></td>
<td><span data-ttu-id="d32a7-283">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d32a7-284">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d32a7-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d32a7-285">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d32a7-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d32a7-286">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-287">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d32a7-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d32a7-288">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d32a7-289">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d32a7-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d32a7-290">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d32a7-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
