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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146142"
---
# <a name="actuals-overview"></a><span data-ttu-id="f972d-103">Prehľad skutočných hodnôt</span><span class="sxs-lookup"><span data-stu-id="f972d-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f972d-104">Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte.</span><span class="sxs-lookup"><span data-stu-id="f972d-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="f972d-105">Skutočné údaje projektu možno vystopovať späť do svojich zdrojových dokladov.</span><span class="sxs-lookup"><span data-stu-id="f972d-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="f972d-106">Tieto zdrojové doklady zahŕňajú čas, výdavky a účtovné záznamy, ako aj faktúry.</span><span class="sxs-lookup"><span data-stu-id="f972d-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Ako vystopovať skutočné údaje projektov na zdrojové dokumenty](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="f972d-108">Odoslanie časovej položky</span><span class="sxs-lookup"><span data-stu-id="f972d-108">Submitting a time entry</span></span>

<span data-ttu-id="f972d-109">V PSA, keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="f972d-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f972d-110">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="f972d-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f972d-111">Keď je predložená časová položka pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="f972d-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="f972d-112">Logika pre zadávanie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="f972d-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="f972d-113">Všetky hodnoty polí z časového záznamu sa skopírujú do účtovného denníka.</span><span class="sxs-lookup"><span data-stu-id="f972d-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="f972d-114">Tieto polia zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="f972d-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="f972d-115">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka**, spôsobujú, že v zázname účtovného denníka sa predvolene zadá primeraná cena.</span><span class="sxs-lookup"><span data-stu-id="f972d-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="f972d-116">Ak do časového záznamu pridáte vlastné pole a chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočná entita a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných údajov.</span><span class="sxs-lookup"><span data-stu-id="f972d-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="f972d-117">Odoslanie výdavkového záznamu</span><span class="sxs-lookup"><span data-stu-id="f972d-117">Submitting an expense entry</span></span>

<span data-ttu-id="f972d-118">V PSA, keď je predložený výdavkový záznam položka pre projekt, ktorý je priradený k riadku zmluvy s časom a materiálom, vytvoria sa dva účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="f972d-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="f972d-119">Jeden riadok je pre náklad, a druhý riadok je pre nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="f972d-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="f972d-120">Keď je predložený výdavkový záznam pre projekt, ktorý je priradený k riadku zmluvy s pevnou cenou, záznam v účtovnom denníku je vytvorený len pre náklady.</span><span class="sxs-lookup"><span data-stu-id="f972d-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="f972d-121">Logika pre zadávanie predvolených cien výdavkov je založená na kategórii výdavkov, ktorá je vybratá na stránke **Výdavkový záznam**.</span><span class="sxs-lookup"><span data-stu-id="f972d-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="f972d-122">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="f972d-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f972d-123">Pre samotnú cenu však čiastka zadaná používateľom je nastavená priamo na súvisiace výdavkové záznamy účtovného denníka pre náklady a predaje predvolene.</span><span class="sxs-lookup"><span data-stu-id="f972d-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="f972d-124">V aktuálnej verzii PSA, kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="f972d-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="f972d-125">Používanie účtovných záznamov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="f972d-126">V PSA vám účtovné záznamy umožňujú zaznamenávať náklady alebo výnosy materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="f972d-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f972d-127">Denník má hlavičku, riadky a **Potvrdiť** akciu.</span><span class="sxs-lookup"><span data-stu-id="f972d-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="f972d-128">Tu je niekoľko scenárov, v ktorých možno použiť denník:</span><span class="sxs-lookup"><span data-stu-id="f972d-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="f972d-129">Musíte zaznamenať skutočné materiálne náklady a predaj na projekte.</span><span class="sxs-lookup"><span data-stu-id="f972d-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="f972d-130">Musíte presunúť transakcie skutočných údajov z iného systému na PSA.</span><span class="sxs-lookup"><span data-stu-id="f972d-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="f972d-131">Musíte zaznamenať náklady, ktoré sa vyskytli v inom systéme, ako napríklad obstarávacie alebo subdodávateľské náklady.</span><span class="sxs-lookup"><span data-stu-id="f972d-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f972d-132">Účtovné záznamy by mal na vytváranie skutočných hodnôt používať iba používateľ, ktorý si je plne vedomý účtovného dopadu skutočných hodnôt na projekt.</span><span class="sxs-lookup"><span data-stu-id="f972d-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="f972d-133">Dôvodom je, že aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="f972d-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="f972d-134">Z dôvodu dopadu tohto typu záznamu v účtovnom denníku buďte pri vytváraní účtovných záznamov primerane opatrní.</span><span class="sxs-lookup"><span data-stu-id="f972d-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="f972d-135">Zaznamenávanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="f972d-135">Recording actuals based on project events</span></span>

<span data-ttu-id="f972d-136">PSA zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="f972d-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f972d-137">Tieto transakcie sa zaznamenávajú ako **skutočné údaje**.</span><span class="sxs-lookup"><span data-stu-id="f972d-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="f972d-138">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="f972d-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="f972d-139">**Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="f972d-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f972d-140">Udalosť</span><span class="sxs-lookup"><span data-stu-id="f972d-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f972d-141">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="f972d-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f972d-142">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="f972d-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f972d-143">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="f972d-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f972d-144">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f972d-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f972d-145">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f972d-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f972d-146">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f972d-146">Actuals</span></span></th>
<th><span data-ttu-id="f972d-147">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f972d-147">Transaction currency</span></span></th>
<th><span data-ttu-id="f972d-148">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f972d-148">Fixed price</span></span></th>
<th><span data-ttu-id="f972d-149">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f972d-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f972d-150">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="f972d-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f972d-151">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f972d-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-152">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="f972d-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f972d-153">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f972d-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f972d-154">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f972d-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f972d-155">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-155">Cost actual</span></span></td>
<td><span data-ttu-id="f972d-156">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-157">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-158">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f972d-159">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-160">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-161">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="f972d-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f972d-162">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f972d-163">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f972d-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f972d-164">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-164">Cost actual</span></span></td>
<td><span data-ttu-id="f972d-165">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-166">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-167">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-168">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-169">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-170">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f972d-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f972d-171">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-172">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f972d-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f972d-173">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f972d-174">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="f972d-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f972d-175">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f972d-176">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-177">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f972d-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-178">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-179">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-180">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-181">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-181">Billed sales</span></span></td>
<td><span data-ttu-id="f972d-182">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f972d-183">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="f972d-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f972d-184">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f972d-185">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-186">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-187">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-188">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-189">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-190">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f972d-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f972d-191">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-192">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f972d-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f972d-193">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f972d-194">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f972d-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f972d-195">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f972d-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f972d-196">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f972d-197">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f972d-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f972d-198">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="f972d-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f972d-199">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-200">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-201">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-202">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-202">Billed sales</span></span></td>
<td><span data-ttu-id="f972d-203">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f972d-204">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f972d-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f972d-205">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f972d-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f972d-206">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-207">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f972d-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f972d-208">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-209">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f972d-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f972d-210">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="f972d-211">**Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu**</span><span class="sxs-lookup"><span data-stu-id="f972d-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f972d-212">Udalosť</span><span class="sxs-lookup"><span data-stu-id="f972d-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f972d-213">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="f972d-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f972d-214">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="f972d-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f972d-215">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="f972d-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f972d-216">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f972d-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f972d-217">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f972d-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f972d-218">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f972d-218">Actuals</span></span></th>
<th><span data-ttu-id="f972d-219">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f972d-219">Transaction currency</span></span></th>
<th><span data-ttu-id="f972d-220">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f972d-220">Fixed price</span></span></th>
<th><span data-ttu-id="f972d-221">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f972d-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f972d-222">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="f972d-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f972d-223">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f972d-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-224">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="f972d-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f972d-225">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f972d-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f972d-226">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f972d-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f972d-227">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-227">Cost actual</span></span></td>
<td><span data-ttu-id="f972d-228">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f972d-229">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f972d-230">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f972d-231">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f972d-232">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-233">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="f972d-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f972d-234">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-235">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f972d-236">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-237">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="f972d-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f972d-238">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f972d-239">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f972d-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f972d-240">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-240">Cost actual</span></span></td>
<td><span data-ttu-id="f972d-241">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-242">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-243">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-244">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-245">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f972d-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-246">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f972d-247">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-248">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="f972d-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f972d-249">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f972d-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-250">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f972d-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f972d-251">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-252">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f972d-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f972d-253">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f972d-254">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="f972d-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f972d-255">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f972d-256">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-257">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f972d-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-258">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-259">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f972d-260">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-261">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-261">Billed sales</span></span></td>
<td><span data-ttu-id="f972d-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f972d-263">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="f972d-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f972d-264">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f972d-265">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-266">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-267">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-268">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f972d-269">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-270">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f972d-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f972d-271">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-272">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f972d-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f972d-273">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f972d-274">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f972d-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f972d-275">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f972d-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f972d-276">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f972d-277">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f972d-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f972d-278">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="f972d-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f972d-279">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-280">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f972d-281">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f972d-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-282">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f972d-282">Billed sales</span></span></td>
<td><span data-ttu-id="f972d-283">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f972d-284">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f972d-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f972d-285">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f972d-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f972d-286">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-287">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f972d-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f972d-288">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f972d-289">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f972d-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f972d-290">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f972d-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
