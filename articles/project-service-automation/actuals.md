---
title: Skutočné hodnoty
description: Táto téma poskytuje informácie o skutočných údajoch projektu.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755648"
---
# <a name="actuals"></a><span data-ttu-id="f6996-103">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f6996-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f6996-104">Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte.</span><span class="sxs-lookup"><span data-stu-id="f6996-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="f6996-105">Skutočné údaje projektu možno vystopovať späť do svojich zdrojových dokladov.</span><span class="sxs-lookup"><span data-stu-id="f6996-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="f6996-106">Tieto zdrojové doklady zahŕňajú čas, výdavky a účtovné záznamy, ako aj faktúry.</span><span class="sxs-lookup"><span data-stu-id="f6996-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Ako vystopovať skutočné údaje projektov na zdrojové dokumenty](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="f6996-108">Odoslanie časovej položky</span><span class="sxs-lookup"><span data-stu-id="f6996-108">Submitting a time entry</span></span>

<span data-ttu-id="f6996-109">V PSA, keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="f6996-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f6996-110">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="f6996-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f6996-111">Keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="f6996-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="f6996-112">Logika pre zadávanie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="f6996-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="f6996-113">Všetky hodnoty polí z časového záznamu sa skopírujú do účtovného denníka.</span><span class="sxs-lookup"><span data-stu-id="f6996-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="f6996-114">Tieto polia zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="f6996-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="f6996-115">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka**, spôsobujú, že v zázname účtovného denníka sa predvolene zadá primeraná cena.</span><span class="sxs-lookup"><span data-stu-id="f6996-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="f6996-116">Ak do časového záznamu pridáte vlastné pole a chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočná entita a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných údajov.</span><span class="sxs-lookup"><span data-stu-id="f6996-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="f6996-117">Odoslanie výdavkového záznamu</span><span class="sxs-lookup"><span data-stu-id="f6996-117">Submitting an expense entry</span></span>

<span data-ttu-id="f6996-118">V PSA, keď je predložený výdavkový záznam položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="f6996-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f6996-119">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="f6996-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f6996-120">Keď je predložený výdavkový záznam pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="f6996-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="f6996-121">Logika pre zadávanie predvolených cien výdavkov je založená na kategórii výdavkov, ktorá je vybratá na stránke **Výdavkový záznam**.</span><span class="sxs-lookup"><span data-stu-id="f6996-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="f6996-122">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="f6996-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f6996-123">Pre samotnú cenu však čiastka zadaná používateľom je nastavená priamo na súvisiace výdavkové záznamy účtovného denníka pre náklady a predaje predvolene.</span><span class="sxs-lookup"><span data-stu-id="f6996-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="f6996-124">V aktuálnej verzii PSA, kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="f6996-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="f6996-125">Používanie denníkov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-125">Using journals to record costs</span></span>

<span data-ttu-id="f6996-126">V PSA vám denníky umožňujú zaznamenávať náklady alebo výnosy materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="f6996-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f6996-127">Denník má hlavičku, riadky a **Potvrdiť** akciu.</span><span class="sxs-lookup"><span data-stu-id="f6996-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="f6996-128">Tu je niekoľko scenárov, v ktorých možno použiť denník:</span><span class="sxs-lookup"><span data-stu-id="f6996-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="f6996-129">Musíte zaznamenať skutočné materiálne náklady a predaj na projekte.</span><span class="sxs-lookup"><span data-stu-id="f6996-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="f6996-130">Musíte presunúť transakcie skutočných údajov z iného systému na PSA.</span><span class="sxs-lookup"><span data-stu-id="f6996-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="f6996-131">Musíte zaznamenať náklady, ktoré sa vyskytli v inom systéme, ako napríklad obstarávacie alebo subdodávateľské náklady.</span><span class="sxs-lookup"><span data-stu-id="f6996-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="f6996-132">Zaznamenávanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="f6996-132">Recording actuals based on project events</span></span>

<span data-ttu-id="f6996-133">PSA zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="f6996-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f6996-134">Tieto transakcie sa zaznamenávajú ako **skutočné údaje**.</span><span class="sxs-lookup"><span data-stu-id="f6996-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="f6996-135">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="f6996-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="f6996-136">**Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="f6996-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f6996-137">Udalosť</span><span class="sxs-lookup"><span data-stu-id="f6996-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f6996-138">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="f6996-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f6996-139">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="f6996-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f6996-140">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="f6996-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f6996-141">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f6996-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f6996-142">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f6996-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6996-143">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f6996-143">Actuals</span></span></th>
<th><span data-ttu-id="f6996-144">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f6996-144">Transaction currency</span></span></th>
<th><span data-ttu-id="f6996-145">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f6996-145">Fixed price</span></span></th>
<th><span data-ttu-id="f6996-146">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f6996-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6996-147">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="f6996-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f6996-148">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f6996-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-149">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="f6996-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f6996-150">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f6996-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6996-151">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f6996-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f6996-152">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-152">Cost actual</span></span></td>
<td><span data-ttu-id="f6996-153">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-154">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-155">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f6996-156">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-157">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-158">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="f6996-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f6996-159">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6996-160">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f6996-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f6996-161">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-161">Cost actual</span></span></td>
<td><span data-ttu-id="f6996-162">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-163">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-164">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-165">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-166">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-167">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f6996-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f6996-168">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-169">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f6996-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f6996-170">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6996-171">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="f6996-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f6996-172">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f6996-173">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-174">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f6996-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-175">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-176">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-177">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-178">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-178">Billed sales</span></span></td>
<td><span data-ttu-id="f6996-179">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6996-180">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="f6996-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f6996-181">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f6996-182">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-183">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-184">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-185">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-186">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-187">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f6996-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f6996-188">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-189">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f6996-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f6996-190">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6996-191">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f6996-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f6996-192">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f6996-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f6996-193">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f6996-194">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f6996-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f6996-195">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="f6996-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f6996-196">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-197">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-198">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-199">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-199">Billed sales</span></span></td>
<td><span data-ttu-id="f6996-200">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6996-201">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f6996-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f6996-202">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f6996-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f6996-203">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-204">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f6996-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f6996-205">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-206">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f6996-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f6996-207">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f6996-208">**Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="f6996-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f6996-209">Udalosť</span><span class="sxs-lookup"><span data-stu-id="f6996-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f6996-210">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="f6996-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f6996-211">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="f6996-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f6996-212">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="f6996-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f6996-213">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f6996-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f6996-214">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f6996-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f6996-215">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f6996-215">Actuals</span></span></th>
<th><span data-ttu-id="f6996-216">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f6996-216">Transaction currency</span></span></th>
<th><span data-ttu-id="f6996-217">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f6996-217">Fixed price</span></span></th>
<th><span data-ttu-id="f6996-218">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f6996-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f6996-219">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="f6996-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f6996-220">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f6996-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-221">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="f6996-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f6996-222">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f6996-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f6996-223">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f6996-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f6996-224">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-224">Cost actual</span></span></td>
<td><span data-ttu-id="f6996-225">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f6996-226">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f6996-227">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f6996-228">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f6996-229">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-230">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="f6996-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f6996-231">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-232">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f6996-233">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-234">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="f6996-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f6996-235">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f6996-236">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f6996-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f6996-237">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-237">Cost actual</span></span></td>
<td><span data-ttu-id="f6996-238">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-239">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-240">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-241">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-242">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f6996-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-243">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f6996-244">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-245">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="f6996-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f6996-246">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f6996-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-247">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f6996-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f6996-248">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-249">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f6996-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f6996-250">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6996-251">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="f6996-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f6996-252">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f6996-253">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-254">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f6996-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-255">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-256">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f6996-257">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-258">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-258">Billed sales</span></span></td>
<td><span data-ttu-id="f6996-259">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6996-260">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="f6996-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f6996-261">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f6996-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-263">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-264">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-265">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f6996-266">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-267">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f6996-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f6996-268">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-269">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f6996-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f6996-270">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f6996-271">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f6996-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f6996-272">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f6996-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f6996-273">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f6996-274">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f6996-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f6996-275">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="f6996-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f6996-276">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-277">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f6996-278">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f6996-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-279">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f6996-279">Billed sales</span></span></td>
<td><span data-ttu-id="f6996-280">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f6996-281">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f6996-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f6996-282">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f6996-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f6996-283">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-284">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f6996-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f6996-285">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f6996-286">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f6996-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f6996-287">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f6996-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
