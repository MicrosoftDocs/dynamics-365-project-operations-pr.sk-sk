---
title: Skutočné hodnoty
description: Táto téma poskytuje informácie o tom, ako pracovať so skutočnými údajmi v aplikácii Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996630"
---
# <a name="actuals"></a><span data-ttu-id="f23fd-103">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f23fd-103">Actuals</span></span> 

<span data-ttu-id="f23fd-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="f23fd-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f23fd-105">Skutočné hodnoty predstavujú skontrolované a schválené finančné údaje a naplánovaný postup projektu.</span><span class="sxs-lookup"><span data-stu-id="f23fd-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="f23fd-106">Vytvárajú sa na základe schválenia časových položiek, výdavkových položiek, položiek použitia materiálu, účtovných záznamov a faktúr.</span><span class="sxs-lookup"><span data-stu-id="f23fd-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="f23fd-107">Záznamy v účtovnom denníku a časový záznam</span><span class="sxs-lookup"><span data-stu-id="f23fd-107">Journal lines and time submission</span></span>

<span data-ttu-id="f23fd-108">Viac informácií o časovom zázname nájdete na [Prehľad časového záznamu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f23fd-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f23fd-109">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f23fd-109">Time and materials</span></span>

<span data-ttu-id="f23fd-110">Keď je zadaný časový záznam prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="f23fd-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f23fd-111">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-111">Fixed price</span></span>

<span data-ttu-id="f23fd-112">Keď je predložená časová položka prepojená s projektom ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="f23fd-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f23fd-113">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-113">Default pricing</span></span>

<span data-ttu-id="f23fd-114">Logika pre vytváranie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="f23fd-115">Hodnoty polí z časového záznamu sa skopírujú do záznamu v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="f23fd-116">Tieto hodnoty zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="f23fd-117">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Zdrojová jednotka** sa používajú na určenie primeranej ceny v zázname v účtovom denníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f23fd-118">K časovému záznamu môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="f23fd-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="f23fd-119">Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**.</span><span class="sxs-lookup"><span data-stu-id="f23fd-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f23fd-120">Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií.</span><span class="sxs-lookup"><span data-stu-id="f23fd-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f23fd-121">Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f23fd-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="f23fd-122">Záznamy v účtovnom denníku a predloženie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="f23fd-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="f23fd-123">Viac informácií o zázname o výdavku nájdete na [Prehľad výdavkov](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f23fd-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f23fd-124">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f23fd-124">Time and materials</span></span>

<span data-ttu-id="f23fd-125">Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="f23fd-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f23fd-126">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-126">Fixed price</span></span>

<span data-ttu-id="f23fd-127">Keď je predložený základný výdavkový záznam prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="f23fd-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f23fd-128">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-128">Default pricing</span></span>

<span data-ttu-id="f23fd-129">Logika zadávania predvolených cien pre výdavky je založená na kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="f23fd-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="f23fd-130">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený a mena sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="f23fd-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f23fd-131">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Kategória transakcie** a **Jednotka**, sa používajú na určenie primeranej ceny v zázname v účtovom denníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f23fd-132">Funguje to však iba vtedy, keď je v cenníku cenová metóda **Cena za jednotku**.</span><span class="sxs-lookup"><span data-stu-id="f23fd-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="f23fd-133">Ak je cenová metóda **V rámci nákladov** alebo **Prirážka nad rámec nákladov**, pre náklady sa použije cena zadaná pri vytvorení položky výdaja a cena predaja v zázname v účtovnom denníku sa vypočíta na základe metódy oceňovania.</span><span class="sxs-lookup"><span data-stu-id="f23fd-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="f23fd-134">Do záznamu výdavkov môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="f23fd-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="f23fd-135">Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**.</span><span class="sxs-lookup"><span data-stu-id="f23fd-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f23fd-136">Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií.</span><span class="sxs-lookup"><span data-stu-id="f23fd-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f23fd-137">Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f23fd-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="f23fd-138">Záznamy v účtovnom denníku a odoslanie denníka použitia materiálu</span><span class="sxs-lookup"><span data-stu-id="f23fd-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="f23fd-139">Viac informácií o zadávaní výdavkov nájdete v článku [Denník použitia materiálu](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="f23fd-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f23fd-140">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f23fd-140">Time and materials</span></span>

<span data-ttu-id="f23fd-141">Keď je zadaná položka denníka použitia materiálu spojená s projektom, ktorý je namapovaný na riadok zmluvy s časom a materiálom, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a druhý pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="f23fd-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f23fd-142">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-142">Fixed price</span></span>

<span data-ttu-id="f23fd-143">Keď je odoslaný záznam denníka použitia materiálu prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="f23fd-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f23fd-144">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-144">Default pricing</span></span>

<span data-ttu-id="f23fd-145">Logika zadávania predvolených cien materiálu je založená na kombinácii produktu a jednotky.</span><span class="sxs-lookup"><span data-stu-id="f23fd-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="f23fd-146">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený a mena sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="f23fd-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f23fd-147">Polia, ktoré ovplyvňujú predvolené ceny, ako je **ID produktu** a **Zdrojová jednotka** sa používajú na určenie primeranej ceny v zázname v účtovom denníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f23fd-148">Toto však funguje iba pre katalógové produkty.</span><span class="sxs-lookup"><span data-stu-id="f23fd-148">However, this only works for catalog products.</span></span> <span data-ttu-id="f23fd-149">Pre pridávané produkty sa cena zadaná pri vytvorení záznamu v denníku použitia materiálu použije pre náklady a predajnú cenu v záznamoch v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="f23fd-150">Do záznamu **Denník použitia materiálu** môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="f23fd-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="f23fd-151">Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**.</span><span class="sxs-lookup"><span data-stu-id="f23fd-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="f23fd-152">Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií.</span><span class="sxs-lookup"><span data-stu-id="f23fd-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="f23fd-153">Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="f23fd-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="f23fd-154">Používanie účtovných záznamov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-154">Use entry journals to record costs</span></span>

<span data-ttu-id="f23fd-155">Účtovné záznamy môžete použiť na zaznamenávanie nákladov alebo výnosov materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="f23fd-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f23fd-156">Denníky možno použiť na nasledujúce účely:</span><span class="sxs-lookup"><span data-stu-id="f23fd-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="f23fd-157">Presuňte transakcie skutočných údajov z iného systému do aplikácie Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f23fd-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="f23fd-158">Záznam nákladov, ktoré sa vyskytli v inom systéme.</span><span class="sxs-lookup"><span data-stu-id="f23fd-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="f23fd-159">Tieto náklady môžu zahŕňať náklady na obstaranie alebo subdodávky.</span><span class="sxs-lookup"><span data-stu-id="f23fd-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f23fd-160">Aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="f23fd-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="f23fd-161">Preto iba používateľ, ktorý si je plne vedomý účtovných dopadov, ktoré môžu mať skutočné hodnoty na projekt, by mal na vytváranie skutočných hodnôt používať účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="f23fd-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="f23fd-162">Z dôvodu vplyvu tohto typu denníka by ste si mali starostlivo zvoliť, kto má prístup k vytváraniu účtovných záznamov.</span><span class="sxs-lookup"><span data-stu-id="f23fd-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="f23fd-163">Zaznamenanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="f23fd-163">Record actuals based on project events</span></span>

<span data-ttu-id="f23fd-164">Project Operations zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="f23fd-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f23fd-165">Tieto transakcie sa zaznamenávajú ako skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="f23fd-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="f23fd-166">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="f23fd-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="f23fd-167">Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="f23fd-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f23fd-168">Udalosť</span><span class="sxs-lookup"><span data-stu-id="f23fd-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f23fd-169">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="f23fd-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f23fd-170">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="f23fd-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f23fd-171">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="f23fd-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f23fd-172">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f23fd-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f23fd-173">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f23fd-174">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f23fd-174">Actuals</span></span></th>
<th><span data-ttu-id="f23fd-175">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f23fd-175">Transaction currency</span></span></th>
<th><span data-ttu-id="f23fd-176">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-176">Fixed price</span></span></th>
<th><span data-ttu-id="f23fd-177">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f23fd-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f23fd-178">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="f23fd-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f23fd-179">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f23fd-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-180">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="f23fd-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f23fd-181">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f23fd-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f23fd-182">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f23fd-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f23fd-183">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-183">Cost actual</span></span></td>
<td><span data-ttu-id="f23fd-184">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-185">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-186">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f23fd-187">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-188">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-189">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="f23fd-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f23fd-190">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f23fd-191">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f23fd-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f23fd-192">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-192">Cost actual</span></span></td>
<td><span data-ttu-id="f23fd-193">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-194">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-195">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-196">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-197">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-198">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f23fd-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f23fd-199">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-200">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f23fd-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f23fd-201">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f23fd-202">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="f23fd-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f23fd-203">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f23fd-204">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-205">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f23fd-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-206">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-207">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-208">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-209">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-209">Billed sales</span></span></td>
<td><span data-ttu-id="f23fd-210">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f23fd-211">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="f23fd-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f23fd-212">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f23fd-213">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-214">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-215">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-216">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-217">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-218">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f23fd-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f23fd-219">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-220">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f23fd-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f23fd-221">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f23fd-222">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f23fd-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f23fd-223">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f23fd-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f23fd-224">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f23fd-225">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f23fd-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f23fd-226">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="f23fd-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f23fd-227">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-228">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-229">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-230">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-230">Billed sales</span></span></td>
<td><span data-ttu-id="f23fd-231">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f23fd-232">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f23fd-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f23fd-233">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f23fd-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f23fd-234">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-235">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f23fd-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f23fd-236">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-237">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f23fd-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f23fd-238">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="f23fd-239">Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="f23fd-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f23fd-240">Udalosť</span><span class="sxs-lookup"><span data-stu-id="f23fd-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f23fd-241">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="f23fd-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f23fd-242">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="f23fd-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f23fd-243">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="f23fd-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f23fd-244">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="f23fd-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f23fd-245">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f23fd-246">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="f23fd-246">Actuals</span></span></th>
<th><span data-ttu-id="f23fd-247">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f23fd-247">Transaction currency</span></span></th>
<th><span data-ttu-id="f23fd-248">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="f23fd-248">Fixed price</span></span></th>
<th><span data-ttu-id="f23fd-249">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="f23fd-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f23fd-250">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="f23fd-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f23fd-251">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f23fd-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-252">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="f23fd-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f23fd-253">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="f23fd-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f23fd-254">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f23fd-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f23fd-255">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-255">Cost actual</span></span></td>
<td><span data-ttu-id="f23fd-256">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f23fd-257">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f23fd-258">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f23fd-259">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f23fd-260">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-261">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="f23fd-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f23fd-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-263">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f23fd-264">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-265">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="f23fd-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f23fd-266">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f23fd-267">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="f23fd-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f23fd-268">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-268">Cost actual</span></span></td>
<td><span data-ttu-id="f23fd-269">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-270">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-271">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-272">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-273">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="f23fd-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-274">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f23fd-275">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-276">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="f23fd-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f23fd-277">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="f23fd-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-278">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f23fd-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f23fd-279">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-280">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f23fd-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f23fd-281">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f23fd-282">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="f23fd-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f23fd-283">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f23fd-284">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-285">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f23fd-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-286">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-287">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f23fd-288">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-289">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-289">Billed sales</span></span></td>
<td><span data-ttu-id="f23fd-290">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f23fd-291">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="f23fd-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f23fd-292">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f23fd-293">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-294">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-295">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-296">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f23fd-297">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-298">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f23fd-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f23fd-299">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-300">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f23fd-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f23fd-301">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f23fd-302">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f23fd-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f23fd-303">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f23fd-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f23fd-304">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f23fd-305">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="f23fd-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f23fd-306">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="f23fd-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f23fd-307">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-308">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f23fd-309">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="f23fd-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-310">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="f23fd-310">Billed sales</span></span></td>
<td><span data-ttu-id="f23fd-311">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f23fd-312">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="f23fd-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f23fd-313">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="f23fd-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f23fd-314">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-315">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="f23fd-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f23fd-316">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f23fd-317">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="f23fd-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f23fd-318">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="f23fd-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
