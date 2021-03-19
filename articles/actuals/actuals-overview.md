---
title: Skutočné hodnoty
description: Táto téma poskytuje informácie o tom, ako pracovať so skutočnými údajmi v aplikácii Microsoft Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 6a94bd143b0d0dad2a08511a34e592a057b6d2a1
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291818"
---
# <a name="actuals"></a><span data-ttu-id="3cd84-103">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="3cd84-103">Actuals</span></span> 

<span data-ttu-id="3cd84-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="3cd84-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3cd84-105">Skutočné údaje sú množstvo práce, ktorá bola dokončená na projekte.</span><span class="sxs-lookup"><span data-stu-id="3cd84-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="3cd84-106">Vytvárajú sa ako výsledok časových a výdavkových záznamov a účtovných záznamov a faktúr.</span><span class="sxs-lookup"><span data-stu-id="3cd84-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="3cd84-107">Záznamy v účtovnom denníku a časový záznam</span><span class="sxs-lookup"><span data-stu-id="3cd84-107">Journal lines and time submission</span></span>

<span data-ttu-id="3cd84-108">Viac informácií o časovom zázname nájdete na [Prehľad časového záznamu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cd84-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3cd84-109">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="3cd84-109">Time and materials</span></span>

<span data-ttu-id="3cd84-110">Keď je zadaný časový záznam prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="3cd84-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3cd84-111">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-111">Fixed price</span></span>

<span data-ttu-id="3cd84-112">Keď je predložená časová položka prepojená s projektom ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="3cd84-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3cd84-113">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-113">Default pricing</span></span>

<span data-ttu-id="3cd84-114">Logika pre vytváranie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="3cd84-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="3cd84-115">Hodnoty polí z časového záznamu sa skopírujú do záznamu v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="3cd84-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="3cd84-116">Tieto hodnoty zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="3cd84-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="3cd84-117">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Organizačná Jednotka**, sa používajú na určenie primeranej ceny v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="3cd84-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="3cd84-118">K časovému záznamu môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="3cd84-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="3cd84-119">Ak chcete, aby sa hodnota poľa šírila na skutočné údaje, vytvorte pole v entite Skutočné hodnoty a použite priradenia polí na skopírovanie poľa z časového záznamu do skutočných hodnôt.</span><span class="sxs-lookup"><span data-stu-id="3cd84-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="3cd84-120">Záznamy v účtovnom denníku a predloženie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="3cd84-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="3cd84-121">Viac informácií o zázname o výdavku nájdete na [Prehľad výdavkov](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3cd84-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3cd84-122">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="3cd84-122">Time and materials</span></span>

<span data-ttu-id="3cd84-123">Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="3cd84-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3cd84-124">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-124">Fixed price</span></span>

<span data-ttu-id="3cd84-125">Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="3cd84-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3cd84-126">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-126">Default pricing</span></span>

<span data-ttu-id="3cd84-127">Logika zadávania predvolených cien pre výdavky je založená na kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="3cd84-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="3cd84-128">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="3cd84-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="3cd84-129">Predvolene je však pre samotnú cenu čiastka zadaná používateľom nastavená priamo na súvisiace výdavkové záznamy v účtovnom denníku pre náklady a predaje.</span><span class="sxs-lookup"><span data-stu-id="3cd84-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="3cd84-130">Kategoricky-založené zadávanie predvolenej ceny na jednotku na položky výdavkov nie je k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="3cd84-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="3cd84-131">Používanie účtovných záznamov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-131">Use entry journals to record costs</span></span>

<span data-ttu-id="3cd84-132">Účtovné záznamy môžete použiť na zaznamenávanie nákladov alebo výnosov materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="3cd84-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="3cd84-133">Denníky možno použiť na nasledujúce účely:</span><span class="sxs-lookup"><span data-stu-id="3cd84-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="3cd84-134">Zaznamenávanie skutočných nákladov na materiál a predaja projektu.</span><span class="sxs-lookup"><span data-stu-id="3cd84-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="3cd84-135">Presuňte transakcie skutočných údajov z iného systému do aplikácie Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3cd84-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="3cd84-136">Záznam nákladov, ktoré sa vyskytli v inom systéme.</span><span class="sxs-lookup"><span data-stu-id="3cd84-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="3cd84-137">Tieto náklady môžu zahŕňať náklady na obstaranie alebo subdodávky.</span><span class="sxs-lookup"><span data-stu-id="3cd84-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3cd84-138">Aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="3cd84-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="3cd84-139">Preto iba používateľ, ktorý si je plne vedomý účtovných dopadov, ktoré môžu mať skutočné hodnoty na projekt, by mal na vytváranie skutočných hodnôt používať účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="3cd84-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="3cd84-140">Z dôvodu vplyvu tohto typu denníka by ste si mali starostlivo zvoliť, kto má prístup k vytváraniu účtovných záznamov.</span><span class="sxs-lookup"><span data-stu-id="3cd84-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="3cd84-141">Zaznamenanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="3cd84-141">Record actuals based on project events</span></span>

<span data-ttu-id="3cd84-142">Project Operations zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="3cd84-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="3cd84-143">Tieto transakcie sa zaznamenávajú ako skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="3cd84-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="3cd84-144">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="3cd84-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="3cd84-145">Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="3cd84-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3cd84-146">Udalosť</span><span class="sxs-lookup"><span data-stu-id="3cd84-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3cd84-147">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="3cd84-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3cd84-148">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="3cd84-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3cd84-149">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="3cd84-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3cd84-150">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="3cd84-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3cd84-151">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3cd84-152">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="3cd84-152">Actuals</span></span></th>
<th><span data-ttu-id="3cd84-153">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="3cd84-153">Transaction currency</span></span></th>
<th><span data-ttu-id="3cd84-154">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-154">Fixed price</span></span></th>
<th><span data-ttu-id="3cd84-155">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="3cd84-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3cd84-156">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="3cd84-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3cd84-157">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="3cd84-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-158">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="3cd84-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3cd84-159">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="3cd84-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3cd84-160">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="3cd84-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3cd84-161">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-161">Cost actual</span></span></td>
<td><span data-ttu-id="3cd84-162">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-163">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-164">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="3cd84-165">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-166">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-167">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="3cd84-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3cd84-168">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3cd84-169">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="3cd84-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3cd84-170">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-170">Cost actual</span></span></td>
<td><span data-ttu-id="3cd84-171">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-172">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-173">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-174">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-175">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-176">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="3cd84-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3cd84-177">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-178">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="3cd84-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3cd84-179">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3cd84-180">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="3cd84-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3cd84-181">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3cd84-182">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-183">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="3cd84-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-184">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-185">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-186">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-187">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-187">Billed sales</span></span></td>
<td><span data-ttu-id="3cd84-188">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3cd84-189">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="3cd84-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3cd84-190">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3cd84-191">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-192">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-193">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-194">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-195">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-196">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="3cd84-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3cd84-197">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-198">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="3cd84-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3cd84-199">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3cd84-200">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="3cd84-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3cd84-201">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="3cd84-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3cd84-202">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3cd84-203">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="3cd84-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3cd84-204">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="3cd84-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3cd84-205">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-206">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-207">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-208">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-208">Billed sales</span></span></td>
<td><span data-ttu-id="3cd84-209">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3cd84-210">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="3cd84-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3cd84-211">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="3cd84-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3cd84-212">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-213">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="3cd84-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3cd84-214">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-215">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="3cd84-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3cd84-216">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="3cd84-217">Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="3cd84-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3cd84-218">Udalosť</span><span class="sxs-lookup"><span data-stu-id="3cd84-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3cd84-219">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="3cd84-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3cd84-220">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="3cd84-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3cd84-221">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="3cd84-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3cd84-222">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="3cd84-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3cd84-223">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3cd84-224">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="3cd84-224">Actuals</span></span></th>
<th><span data-ttu-id="3cd84-225">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="3cd84-225">Transaction currency</span></span></th>
<th><span data-ttu-id="3cd84-226">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="3cd84-226">Fixed price</span></span></th>
<th><span data-ttu-id="3cd84-227">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="3cd84-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3cd84-228">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="3cd84-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3cd84-229">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="3cd84-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-230">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="3cd84-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3cd84-231">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="3cd84-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3cd84-232">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="3cd84-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3cd84-233">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-233">Cost actual</span></span></td>
<td><span data-ttu-id="3cd84-234">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3cd84-235">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3cd84-236">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3cd84-237">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3cd84-238">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-239">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="3cd84-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3cd84-240">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-241">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3cd84-242">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-243">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="3cd84-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3cd84-244">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3cd84-245">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="3cd84-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3cd84-246">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-246">Cost actual</span></span></td>
<td><span data-ttu-id="3cd84-247">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-248">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-249">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-250">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-251">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="3cd84-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-252">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3cd84-253">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-254">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="3cd84-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3cd84-255">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="3cd84-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-256">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="3cd84-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3cd84-257">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-258">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="3cd84-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3cd84-259">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3cd84-260">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="3cd84-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3cd84-261">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3cd84-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-263">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="3cd84-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-264">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-265">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3cd84-266">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-267">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-267">Billed sales</span></span></td>
<td><span data-ttu-id="3cd84-268">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3cd84-269">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="3cd84-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3cd84-270">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3cd84-271">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-272">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-273">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-274">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3cd84-275">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-276">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="3cd84-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3cd84-277">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-278">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="3cd84-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3cd84-279">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3cd84-280">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="3cd84-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3cd84-281">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="3cd84-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3cd84-282">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3cd84-283">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="3cd84-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3cd84-284">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="3cd84-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3cd84-285">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-286">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3cd84-287">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="3cd84-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-288">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="3cd84-288">Billed sales</span></span></td>
<td><span data-ttu-id="3cd84-289">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3cd84-290">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="3cd84-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3cd84-291">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="3cd84-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3cd84-292">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-293">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="3cd84-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3cd84-294">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3cd84-295">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="3cd84-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3cd84-296">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3cd84-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]