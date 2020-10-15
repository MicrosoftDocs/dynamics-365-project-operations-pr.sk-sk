---
title: Domovská stránka skutočných hodnôt
description: Táto téma poskytuje informácie o spôsobe práce so skutočnými hodnotami v Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907337"
---
# <a name="actuals"></a><span data-ttu-id="d3345-103">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="d3345-103">Actuals</span></span>

<span data-ttu-id="d3345-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="d3345-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d3345-105">Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte.</span><span class="sxs-lookup"><span data-stu-id="d3345-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="d3345-106">Vytvárajú sa ako výsledok časových a výdavkových záznamov a účtovných záznamov a faktúr.</span><span class="sxs-lookup"><span data-stu-id="d3345-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="d3345-107">Záznamy v účtovnom denníku a časový záznam</span><span class="sxs-lookup"><span data-stu-id="d3345-107">Journal lines and time submission</span></span>

<span data-ttu-id="d3345-108">Viac informácií o časovom zázname nájdete na [Prehľad časového záznamu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d3345-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d3345-109">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="d3345-109">Time and materials</span></span>

<span data-ttu-id="d3345-110">Keď je zadaný časový záznam prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="d3345-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d3345-111">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d3345-111">Fixed price</span></span>

<span data-ttu-id="d3345-112">Keď je predložená časová položka prepojená s projektom ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="d3345-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d3345-113">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="d3345-113">Default pricing</span></span>

<span data-ttu-id="d3345-114">Logika pre vytváranie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="d3345-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="d3345-115">Hodnoty polí z časového záznamu sa skopírujú do záznamu v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="d3345-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="d3345-116">Tieto hodnoty zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="d3345-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="d3345-117">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka**, sa používajú na určenie primeranej ceny v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="d3345-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="d3345-118">K časovému záznamu môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="d3345-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="d3345-119">Ak chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočné hodnoty a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných hodnôt.</span><span class="sxs-lookup"><span data-stu-id="d3345-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="d3345-120">Záznamy v účtovnom denníku a predloženie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="d3345-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="d3345-121">Viac informácií o zázname o výdavku nájdete na [Prehľad výdavkov](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="d3345-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="d3345-122">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="d3345-122">Time and materials</span></span>

<span data-ttu-id="d3345-123">Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="d3345-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="d3345-124">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d3345-124">Fixed price</span></span>

<span data-ttu-id="d3345-125">Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="d3345-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="d3345-126">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="d3345-126">Default pricing</span></span>

<span data-ttu-id="d3345-127">Logika zadávania predvolených cien pre výdavky je založená na kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="d3345-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="d3345-128">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="d3345-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="d3345-129">Predvolene je však pre samotnú cenu čiastka zadaná používateľom nastavená priamo na súvisiace výdavkové záznamy v účtovnom denníku pre náklady a predaje.</span><span class="sxs-lookup"><span data-stu-id="d3345-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="d3345-130">Kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="d3345-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="d3345-131">Používanie účtovných záznamov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-131">Use entry journals to record costs</span></span>

<span data-ttu-id="d3345-132">Účtovné záznamy môžete použiť na zaznamenávanie nákladov alebo výnosov materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="d3345-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="d3345-133">Denníky možno použiť na nasledujúce účely:</span><span class="sxs-lookup"><span data-stu-id="d3345-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="d3345-134">Zaznamenávanie skutočných nákladov na materiál a predaja projektu.</span><span class="sxs-lookup"><span data-stu-id="d3345-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="d3345-135">Presun skutočných údajov transakcie z iného systému do Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d3345-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="d3345-136">Záznam nákladov, ktoré sa vyskytli v inom systéme.</span><span class="sxs-lookup"><span data-stu-id="d3345-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="d3345-137">Tieto náklady môžu zahŕňať náklady na obstaranie alebo subdodávky.</span><span class="sxs-lookup"><span data-stu-id="d3345-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3345-138">Aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="d3345-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="d3345-139">Preto iba používateľ, ktorý si je plne vedomý účtovných dopadov, ktoré môžu mať skutočné hodnoty na projekt, by mal na vytváranie skutočných hodnôt používať účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="d3345-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="d3345-140">Z dôvodu vplyvu tohto typu denníka by ste si mali starostlivo zvoliť, kto má prístup k vytváraniu účtovných záznamov.</span><span class="sxs-lookup"><span data-stu-id="d3345-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="d3345-141">Zaznamenanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="d3345-141">Record actuals based on project events</span></span>

<span data-ttu-id="d3345-142">Project Operations zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="d3345-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="d3345-143">Tieto transakcie sa zaznamenávajú ako skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="d3345-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="d3345-144">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="d3345-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="d3345-145">Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="d3345-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d3345-146">Udalosť</span><span class="sxs-lookup"><span data-stu-id="d3345-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d3345-147">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="d3345-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d3345-148">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="d3345-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d3345-149">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="d3345-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d3345-150">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="d3345-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d3345-151">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d3345-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d3345-152">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="d3345-152">Actuals</span></span></th>
<th><span data-ttu-id="d3345-153">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d3345-153">Transaction currency</span></span></th>
<th><span data-ttu-id="d3345-154">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d3345-154">Fixed price</span></span></th>
<th><span data-ttu-id="d3345-155">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d3345-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3345-156">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="d3345-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d3345-157">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d3345-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-158">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="d3345-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d3345-159">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d3345-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d3345-160">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d3345-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d3345-161">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-161">Cost actual</span></span></td>
<td><span data-ttu-id="d3345-162">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-163">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-164">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="d3345-165">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-166">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-167">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="d3345-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d3345-168">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d3345-169">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d3345-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d3345-170">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-170">Cost actual</span></span></td>
<td><span data-ttu-id="d3345-171">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-172">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-173">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-174">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-175">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-176">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d3345-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d3345-177">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-178">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d3345-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d3345-179">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d3345-180">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="d3345-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d3345-181">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d3345-182">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-183">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d3345-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-184">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-185">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-186">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-187">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-187">Billed sales</span></span></td>
<td><span data-ttu-id="d3345-188">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d3345-189">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="d3345-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d3345-190">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d3345-191">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-192">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-193">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-194">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-195">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-196">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d3345-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d3345-197">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-198">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d3345-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d3345-199">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d3345-200">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d3345-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d3345-201">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d3345-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d3345-202">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d3345-203">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d3345-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d3345-204">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="d3345-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d3345-205">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-206">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-207">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-208">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-208">Billed sales</span></span></td>
<td><span data-ttu-id="d3345-209">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d3345-210">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d3345-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d3345-211">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d3345-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d3345-212">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-213">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d3345-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d3345-214">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-215">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d3345-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d3345-216">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="d3345-217">Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="d3345-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="d3345-218">Udalosť</span><span class="sxs-lookup"><span data-stu-id="d3345-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="d3345-219">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="d3345-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="d3345-220">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="d3345-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="d3345-221">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="d3345-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="d3345-222">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="d3345-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="d3345-223">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d3345-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="d3345-224">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="d3345-224">Actuals</span></span></th>
<th><span data-ttu-id="d3345-225">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d3345-225">Transaction currency</span></span></th>
<th><span data-ttu-id="d3345-226">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d3345-226">Fixed price</span></span></th>
<th><span data-ttu-id="d3345-227">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="d3345-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="d3345-228">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="d3345-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="d3345-229">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d3345-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-230">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="d3345-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="d3345-231">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="d3345-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="d3345-232">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d3345-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d3345-233">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-233">Cost actual</span></span></td>
<td><span data-ttu-id="d3345-234">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d3345-235">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d3345-236">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="d3345-237">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="d3345-238">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-239">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="d3345-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="d3345-240">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-241">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d3345-242">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-243">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="d3345-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d3345-244">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="d3345-245">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="d3345-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="d3345-246">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-246">Cost actual</span></span></td>
<td><span data-ttu-id="d3345-247">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-248">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-249">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-250">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-251">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="d3345-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-252">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="d3345-253">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-254">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="d3345-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="d3345-255">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="d3345-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-256">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d3345-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d3345-257">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-258">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d3345-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d3345-259">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d3345-260">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="d3345-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d3345-261">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d3345-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-263">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d3345-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-264">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-265">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="d3345-266">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-267">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-267">Billed sales</span></span></td>
<td><span data-ttu-id="d3345-268">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d3345-269">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="d3345-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="d3345-270">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="d3345-271">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-272">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-273">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-274">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="d3345-275">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-276">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d3345-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="d3345-277">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-278">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d3345-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="d3345-279">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="d3345-280">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d3345-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d3345-281">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d3345-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d3345-282">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="d3345-283">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="d3345-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="d3345-284">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="d3345-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="d3345-285">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-286">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="d3345-287">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="d3345-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-288">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="d3345-288">Billed sales</span></span></td>
<td><span data-ttu-id="d3345-289">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="d3345-290">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="d3345-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="d3345-291">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="d3345-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="d3345-292">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-293">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="d3345-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="d3345-294">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="d3345-295">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="d3345-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="d3345-296">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="d3345-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
