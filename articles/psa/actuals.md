---
title: Prehľad skutočných hodnôt
description: Táto téma poskytuje informácie o skutočných údajoch projektu.
author: rumant
ms.custom:
- dyn365-projectservice
- intro-internal
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
ms.openlocfilehash: cbb3e5c7f74cdf37ae4d259687bf7a98102a8131
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368180"
---
# <a name="actuals-overview"></a><span data-ttu-id="5e416-103">Prehľad skutočných hodnôt</span><span class="sxs-lookup"><span data-stu-id="5e416-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5e416-104">Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte.</span><span class="sxs-lookup"><span data-stu-id="5e416-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="5e416-105">Skutočné údaje projektu možno vystopovať späť do svojich zdrojových dokladov.</span><span class="sxs-lookup"><span data-stu-id="5e416-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="5e416-106">Tieto zdrojové doklady zahŕňajú čas, výdavky a účtovné záznamy, ako aj faktúry.</span><span class="sxs-lookup"><span data-stu-id="5e416-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Ako vystopovať skutočné údaje projektov na zdrojové dokumenty](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="5e416-108">Odoslanie časovej položky</span><span class="sxs-lookup"><span data-stu-id="5e416-108">Submitting a time entry</span></span>

<span data-ttu-id="5e416-109">V PSA, keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="5e416-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5e416-110">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="5e416-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5e416-111">Keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="5e416-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="5e416-112">Logika pre zadávanie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="5e416-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="5e416-113">Všetky hodnoty polí z časového záznamu sa skopírujú do účtovného denníka.</span><span class="sxs-lookup"><span data-stu-id="5e416-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="5e416-114">Tieto polia zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="5e416-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="5e416-115">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka**, spôsobujú, že v zázname účtovného denníka sa predvolene zadá primeraná cena.</span><span class="sxs-lookup"><span data-stu-id="5e416-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="5e416-116">Ak do časového záznamu pridáte vlastné pole a chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočná entita a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných údajov.</span><span class="sxs-lookup"><span data-stu-id="5e416-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="5e416-117">Odoslanie výdavkového záznamu</span><span class="sxs-lookup"><span data-stu-id="5e416-117">Submitting an expense entry</span></span>

<span data-ttu-id="5e416-118">V PSA, keď je predložený výdavkový záznam položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="5e416-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="5e416-119">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="5e416-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="5e416-120">Keď je predložený výdavkový záznam pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="5e416-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="5e416-121">Logika pre zadávanie predvolených cien výdavkov je založená na kategórii výdavkov, ktorá je vybratá na stránke **Výdavkový záznam**.</span><span class="sxs-lookup"><span data-stu-id="5e416-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="5e416-122">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="5e416-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="5e416-123">Pre samotnú cenu však čiastka zadaná používateľom je nastavená priamo na súvisiace výdavkové záznamy účtovného denníka pre náklady a predaje predvolene.</span><span class="sxs-lookup"><span data-stu-id="5e416-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="5e416-124">V aktuálnej verzii PSA, kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="5e416-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="5e416-125">Používanie účtovných záznamov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="5e416-126">V PSA vám účtovné záznamy umožňujú zaznamenávať náklady alebo výnosy materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="5e416-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="5e416-127">Denník má hlavičku, riadky a **Potvrdiť** akciu.</span><span class="sxs-lookup"><span data-stu-id="5e416-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="5e416-128">Tu je niekoľko scenárov, v ktorých možno použiť denník:</span><span class="sxs-lookup"><span data-stu-id="5e416-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="5e416-129">Musíte zaznamenať skutočné materiálne náklady a predaj na projekte.</span><span class="sxs-lookup"><span data-stu-id="5e416-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="5e416-130">Musíte presunúť transakcie skutočných údajov z iného systému na PSA.</span><span class="sxs-lookup"><span data-stu-id="5e416-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="5e416-131">Musíte zaznamenať náklady, ktoré sa vyskytli v inom systéme, ako napríklad obstarávacie alebo subdodávateľské náklady.</span><span class="sxs-lookup"><span data-stu-id="5e416-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e416-132">Účtovné záznamy by mal na vytváranie skutočných hodnôt používať iba používateľ, ktorý si je plne vedomý účtovného dopadu skutočných hodnôt na projekt.</span><span class="sxs-lookup"><span data-stu-id="5e416-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="5e416-133">Dôvodom je, že aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="5e416-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="5e416-134">Z dôvodu dopadu tohto typu záznamu v účtovnom denníku buďte pri vytváraní účtovných záznamov primerane opatrní.</span><span class="sxs-lookup"><span data-stu-id="5e416-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="5e416-135">Zaznamenávanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="5e416-135">Recording actuals based on project events</span></span>

<span data-ttu-id="5e416-136">PSA zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="5e416-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="5e416-137">Tieto transakcie sa zaznamenávajú ako **skutočné údaje**.</span><span class="sxs-lookup"><span data-stu-id="5e416-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="5e416-138">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="5e416-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="5e416-139">**Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="5e416-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5e416-140">Udalosť</span><span class="sxs-lookup"><span data-stu-id="5e416-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5e416-141">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="5e416-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5e416-142">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="5e416-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5e416-143">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="5e416-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5e416-144">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="5e416-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5e416-145">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="5e416-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5e416-146">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="5e416-146">Actuals</span></span></th>
<th><span data-ttu-id="5e416-147">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="5e416-147">Transaction currency</span></span></th>
<th><span data-ttu-id="5e416-148">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="5e416-148">Fixed price</span></span></th>
<th><span data-ttu-id="5e416-149">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="5e416-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5e416-150">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="5e416-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5e416-151">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="5e416-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-152">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="5e416-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5e416-153">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="5e416-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5e416-154">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="5e416-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5e416-155">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-155">Cost actual</span></span></td>
<td><span data-ttu-id="5e416-156">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-157">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-158">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="5e416-159">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-160">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-161">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="5e416-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5e416-162">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5e416-163">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="5e416-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5e416-164">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-164">Cost actual</span></span></td>
<td><span data-ttu-id="5e416-165">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-166">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-167">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-168">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-169">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-170">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="5e416-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5e416-171">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-172">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="5e416-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5e416-173">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5e416-174">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="5e416-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5e416-175">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5e416-176">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-177">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="5e416-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-178">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-179">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-180">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-181">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-181">Billed sales</span></span></td>
<td><span data-ttu-id="5e416-182">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5e416-183">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="5e416-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5e416-184">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5e416-185">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-186">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-187">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-188">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-189">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-190">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="5e416-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5e416-191">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-192">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="5e416-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5e416-193">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5e416-194">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="5e416-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5e416-195">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="5e416-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5e416-196">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5e416-197">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="5e416-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5e416-198">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="5e416-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5e416-199">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-200">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-201">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-202">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-202">Billed sales</span></span></td>
<td><span data-ttu-id="5e416-203">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5e416-204">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="5e416-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5e416-205">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="5e416-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5e416-206">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-207">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="5e416-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5e416-208">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-209">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="5e416-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5e416-210">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="5e416-211">**Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="5e416-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="5e416-212">Udalosť</span><span class="sxs-lookup"><span data-stu-id="5e416-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="5e416-213">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="5e416-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="5e416-214">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="5e416-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="5e416-215">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="5e416-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="5e416-216">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="5e416-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="5e416-217">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="5e416-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="5e416-218">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="5e416-218">Actuals</span></span></th>
<th><span data-ttu-id="5e416-219">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="5e416-219">Transaction currency</span></span></th>
<th><span data-ttu-id="5e416-220">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="5e416-220">Fixed price</span></span></th>
<th><span data-ttu-id="5e416-221">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="5e416-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="5e416-222">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="5e416-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="5e416-223">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="5e416-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-224">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="5e416-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="5e416-225">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="5e416-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="5e416-226">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="5e416-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5e416-227">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-227">Cost actual</span></span></td>
<td><span data-ttu-id="5e416-228">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5e416-229">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5e416-230">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="5e416-231">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="5e416-232">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-233">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="5e416-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="5e416-234">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-235">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5e416-236">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-237">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="5e416-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5e416-238">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="5e416-239">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="5e416-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="5e416-240">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-240">Cost actual</span></span></td>
<td><span data-ttu-id="5e416-241">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-242">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-243">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-244">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-245">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="5e416-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-246">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="5e416-247">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-248">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="5e416-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="5e416-249">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="5e416-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-250">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="5e416-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5e416-251">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-252">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="5e416-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5e416-253">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5e416-254">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="5e416-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5e416-255">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5e416-256">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-257">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="5e416-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-258">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-259">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="5e416-260">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-261">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-261">Billed sales</span></span></td>
<td><span data-ttu-id="5e416-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5e416-263">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="5e416-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="5e416-264">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="5e416-265">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-266">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-267">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-268">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="5e416-269">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-270">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="5e416-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="5e416-271">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-272">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="5e416-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="5e416-273">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="5e416-274">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="5e416-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5e416-275">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="5e416-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5e416-276">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="5e416-277">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="5e416-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="5e416-278">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="5e416-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="5e416-279">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-280">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="5e416-281">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="5e416-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-282">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="5e416-282">Billed sales</span></span></td>
<td><span data-ttu-id="5e416-283">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="5e416-284">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="5e416-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="5e416-285">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="5e416-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="5e416-286">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-287">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="5e416-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="5e416-288">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="5e416-289">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="5e416-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="5e416-290">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5e416-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]