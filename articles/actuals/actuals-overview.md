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
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9e046602a3005930c41ab8c50472d5b1a72303c6
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368630"
---
# <a name="actuals"></a><span data-ttu-id="2aba3-103">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="2aba3-103">Actuals</span></span> 

<span data-ttu-id="2aba3-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="2aba3-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2aba3-105">Skutočné hodnoty predstavujú skontrolované a schválené finančné údaje a naplánovaný postup projektu.</span><span class="sxs-lookup"><span data-stu-id="2aba3-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="2aba3-106">Vytvárajú sa na základe schválenia časových položiek, výdavkových položiek, položiek použitia materiálu, účtovných záznamov a faktúr.</span><span class="sxs-lookup"><span data-stu-id="2aba3-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="2aba3-107">Záznamy v účtovnom denníku a časový záznam</span><span class="sxs-lookup"><span data-stu-id="2aba3-107">Journal lines and time submission</span></span>

<span data-ttu-id="2aba3-108">Viac informácií o časovom zázname nájdete na [Prehľad časového záznamu](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2aba3-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="2aba3-109">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="2aba3-109">Time and materials</span></span>

<span data-ttu-id="2aba3-110">Keď je zadaný časový záznam prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="2aba3-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="2aba3-111">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-111">Fixed price</span></span>

<span data-ttu-id="2aba3-112">Keď je predložená časová položka prepojená s projektom ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="2aba3-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="2aba3-113">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-113">Default pricing</span></span>

<span data-ttu-id="2aba3-114">Logika pre vytváranie predvolených cien býva ako záznam v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="2aba3-115">Hodnoty polí z časového záznamu sa skopírujú do záznamu v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="2aba3-116">Tieto hodnoty zahŕňajú dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený, a výsledok meny v príslušnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="2aba3-117">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Rola** a **Zdrojová jednotka** sa používajú na určenie primeranej ceny v zázname v účtovom denníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="2aba3-118">K časovému záznamu môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="2aba3-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="2aba3-119">Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**.</span><span class="sxs-lookup"><span data-stu-id="2aba3-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="2aba3-120">Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií.</span><span class="sxs-lookup"><span data-stu-id="2aba3-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="2aba3-121">Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="2aba3-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="2aba3-122">Záznamy v účtovnom denníku a predloženie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="2aba3-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="2aba3-123">Viac informácií o zázname o výdavku nájdete na [Prehľad výdavkov](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="2aba3-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="2aba3-124">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="2aba3-124">Time and materials</span></span>

<span data-ttu-id="2aba3-125">Keď je predložený základný záznam o výdavku prepojený s projektom, ktorý je namapovaný na riadok zmluvy času a materiálov, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a jeden pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="2aba3-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="2aba3-126">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-126">Fixed price</span></span>

<span data-ttu-id="2aba3-127">Keď je predložený základný výdavkový záznam prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="2aba3-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="2aba3-128">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-128">Default pricing</span></span>

<span data-ttu-id="2aba3-129">Logika zadávania predvolených cien pre výdavky je založená na kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="2aba3-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="2aba3-130">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený a mena sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="2aba3-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="2aba3-131">Polia, ktoré ovplyvňujú predvolené ceny, ako je **Kategória transakcie** a **Jednotka**, sa používajú na určenie primeranej ceny v zázname v účtovom denníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="2aba3-132">Funguje to však iba vtedy, keď je v cenníku cenová metóda **Cena za jednotku**.</span><span class="sxs-lookup"><span data-stu-id="2aba3-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="2aba3-133">Ak je cenová metóda **V rámci nákladov** alebo **Prirážka nad rámec nákladov**, pre náklady sa použije cena zadaná pri vytvorení položky výdaja a cena predaja v zázname v účtovnom denníku sa vypočíta na základe metódy oceňovania.</span><span class="sxs-lookup"><span data-stu-id="2aba3-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="2aba3-134">Do záznamu výdavkov môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="2aba3-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="2aba3-135">Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**.</span><span class="sxs-lookup"><span data-stu-id="2aba3-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="2aba3-136">Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií.</span><span class="sxs-lookup"><span data-stu-id="2aba3-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="2aba3-137">Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="2aba3-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="2aba3-138">Záznamy v účtovnom denníku a odoslanie denníka použitia materiálu</span><span class="sxs-lookup"><span data-stu-id="2aba3-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="2aba3-139">Viac informácií o zadávaní výdavkov nájdete v článku [Denník použitia materiálu](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="2aba3-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="2aba3-140">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="2aba3-140">Time and materials</span></span>

<span data-ttu-id="2aba3-141">Keď je zadaná položka denníka použitia materiálu spojená s projektom, ktorý je namapovaný na riadok zmluvy s časom a materiálom, systém vytvorí dva záznamy v účtovnom denníku, jeden pre náklady a druhý pre nevyfakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="2aba3-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="2aba3-142">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-142">Fixed price</span></span>

<span data-ttu-id="2aba3-143">Keď je odoslaný záznam denníka použitia materiálu prepojený s projektom, ktorý je priradený k riadku zmluvy s pevnou cenou, systém vytvorí jeden záznam v účtovnom denníku pre náklady.</span><span class="sxs-lookup"><span data-stu-id="2aba3-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="2aba3-144">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-144">Default pricing</span></span>

<span data-ttu-id="2aba3-145">Logika zadávania predvolených cien materiálu je založená na kombinácii produktu a jednotky.</span><span class="sxs-lookup"><span data-stu-id="2aba3-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="2aba3-146">Dátum transakcie, riadok zmluvy, ku ktorému je projekt priradený a mena sú všetky použité na určenie príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="2aba3-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="2aba3-147">Polia, ktoré ovplyvňujú predvolené ceny, ako je **ID produktu** a **Zdrojová jednotka** sa používajú na určenie primeranej ceny v zázname v účtovom denníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="2aba3-148">Toto však funguje iba pre katalógové produkty.</span><span class="sxs-lookup"><span data-stu-id="2aba3-148">However, this only works for catalog products.</span></span> <span data-ttu-id="2aba3-149">Pre pridávané produkty sa cena zadaná pri vytvorení záznamu v denníku použitia materiálu použije pre náklady a predajnú cenu v záznamoch v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="2aba3-150">Do záznamu **Denník použitia materiálu** môžete pridať vlastné pole.</span><span class="sxs-lookup"><span data-stu-id="2aba3-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="2aba3-151">Ak chcete, aby sa hodnota poľa rozšírila na skutočné hodnoty, vytvorte pole v tabuľkách **Skutočné hodnoty** a **Záznam v účtovnom denníku**.</span><span class="sxs-lookup"><span data-stu-id="2aba3-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="2aba3-152">Použite vlastný kód na šírenie vybratej hodnoty poľa z položky Časový vstup do položky Skutočné hodnoty cez záznam v účtovnom denníku pomocou počiatkov transakcií.</span><span class="sxs-lookup"><span data-stu-id="2aba3-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="2aba3-153">Ďalšie informácie o počiatkoch transakcií a pripojeniach nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="2aba3-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="2aba3-154">Používanie účtovných záznamov na zaznamenávanie nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-154">Use entry journals to record costs</span></span>

<span data-ttu-id="2aba3-155">Účtovné záznamy môžete použiť na zaznamenávanie nákladov alebo výnosov materiálov, poplatkov, času, výdavkov alebo daňových transakcií.</span><span class="sxs-lookup"><span data-stu-id="2aba3-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="2aba3-156">Denníky možno použiť na nasledujúce účely:</span><span class="sxs-lookup"><span data-stu-id="2aba3-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="2aba3-157">Presuňte transakcie skutočných údajov z iného systému do aplikácie Microsoft Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="2aba3-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="2aba3-158">Záznam nákladov, ktoré sa vyskytli v inom systéme.</span><span class="sxs-lookup"><span data-stu-id="2aba3-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="2aba3-159">Tieto náklady môžu zahŕňať náklady na obstaranie alebo subdodávky.</span><span class="sxs-lookup"><span data-stu-id="2aba3-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2aba3-160">Aplikácia neoveruje typ záznamu v účtovnom denníku alebo súvisiace ceny, ktoré sú zadané v zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="2aba3-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="2aba3-161">Preto iba používateľ, ktorý si je plne vedomý účtovných dopadov, ktoré môžu mať skutočné hodnoty na projekt, by mal na vytváranie skutočných hodnôt používať účtovné záznamy.</span><span class="sxs-lookup"><span data-stu-id="2aba3-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="2aba3-162">Z dôvodu vplyvu tohto typu denníka by ste si mali starostlivo zvoliť, kto má prístup k vytváraniu účtovných záznamov.</span><span class="sxs-lookup"><span data-stu-id="2aba3-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="2aba3-163">Zaznamenanie skutočných údajov na základe projektových podujatí</span><span class="sxs-lookup"><span data-stu-id="2aba3-163">Record actuals based on project events</span></span>

<span data-ttu-id="2aba3-164">Project Operations zaznamenáva finančné transakcie, ktoré nastanú počas projektu.</span><span class="sxs-lookup"><span data-stu-id="2aba3-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="2aba3-165">Tieto transakcie sa zaznamenávajú ako skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="2aba3-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="2aba3-166">Nasledujúce tabuľky zobrazujú rôzne typy skutočných údajov, ktoré sú vytvorené, v závislosti od toho, či je projekt, čas a materiály alebo projekt s pevnou cenou, je v štádiu predpredaja alebo je interným projektom.</span><span class="sxs-lookup"><span data-stu-id="2aba3-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="2aba3-167">Zdroj patrí k rovnakej organizačnej jednotke ako zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="2aba3-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="2aba3-168">Udalosť</span><span class="sxs-lookup"><span data-stu-id="2aba3-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="2aba3-169">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="2aba3-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="2aba3-170">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="2aba3-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="2aba3-171">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="2aba3-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="2aba3-172">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="2aba3-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="2aba3-173">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2aba3-174">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="2aba3-174">Actuals</span></span></th>
<th><span data-ttu-id="2aba3-175">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="2aba3-175">Transaction currency</span></span></th>
<th><span data-ttu-id="2aba3-176">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-176">Fixed price</span></span></th>
<th><span data-ttu-id="2aba3-177">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="2aba3-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2aba3-178">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="2aba3-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="2aba3-179">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="2aba3-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-180">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="2aba3-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="2aba3-181">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="2aba3-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2aba3-182">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="2aba3-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2aba3-183">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-183">Cost actual</span></span></td>
<td><span data-ttu-id="2aba3-184">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-185">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-186">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="2aba3-187">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-188">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-189">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="2aba3-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="2aba3-190">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2aba3-191">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="2aba3-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2aba3-192">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-192">Cost actual</span></span></td>
<td><span data-ttu-id="2aba3-193">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-194">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-195">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-196">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-197">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-198">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="2aba3-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2aba3-199">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-200">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="2aba3-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2aba3-201">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2aba3-202">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="2aba3-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2aba3-203">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2aba3-204">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-205">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="2aba3-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-206">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-207">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-208">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-209">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-209">Billed sales</span></span></td>
<td><span data-ttu-id="2aba3-210">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2aba3-211">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="2aba3-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2aba3-212">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2aba3-213">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-214">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-215">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-216">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-217">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-218">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="2aba3-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2aba3-219">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-220">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="2aba3-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2aba3-221">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2aba3-222">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="2aba3-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2aba3-223">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="2aba3-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2aba3-224">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="2aba3-225">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="2aba3-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="2aba3-226">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="2aba3-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="2aba3-227">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-228">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-229">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-230">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-230">Billed sales</span></span></td>
<td><span data-ttu-id="2aba3-231">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2aba3-232">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="2aba3-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2aba3-233">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="2aba3-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2aba3-234">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-235">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="2aba3-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="2aba3-236">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-237">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="2aba3-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="2aba3-238">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="2aba3-239">Zdroj patrí odlišnej organizačnej jednotke ako je zmluvná jednotka projektu</span><span class="sxs-lookup"><span data-stu-id="2aba3-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="2aba3-240">Udalosť</span><span class="sxs-lookup"><span data-stu-id="2aba3-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="2aba3-241">Fakturovateľný alebo predaný projekt</span><span class="sxs-lookup"><span data-stu-id="2aba3-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="2aba3-242">Projekt v štádiu predpredaja</span><span class="sxs-lookup"><span data-stu-id="2aba3-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="2aba3-243">Interný projekt</span><span class="sxs-lookup"><span data-stu-id="2aba3-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="2aba3-244">Čas a materiály</span><span class="sxs-lookup"><span data-stu-id="2aba3-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="2aba3-245">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="2aba3-246">Skutočné hodnoty</span><span class="sxs-lookup"><span data-stu-id="2aba3-246">Actuals</span></span></th>
<th><span data-ttu-id="2aba3-247">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="2aba3-247">Transaction currency</span></span></th>
<th><span data-ttu-id="2aba3-248">Pevná cena</span><span class="sxs-lookup"><span data-stu-id="2aba3-248">Fixed price</span></span></th>
<th><span data-ttu-id="2aba3-249">Mena transakcie</span><span class="sxs-lookup"><span data-stu-id="2aba3-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="2aba3-250">Časový záznam je vytvorený.</span><span class="sxs-lookup"><span data-stu-id="2aba3-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="2aba3-251">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="2aba3-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-252">Časový záznam je predložený.</span><span class="sxs-lookup"><span data-stu-id="2aba3-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="2aba3-253">Žiadna aktivita v entite skutočných údajov</span><span class="sxs-lookup"><span data-stu-id="2aba3-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="2aba3-254">Čas je schválený, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="2aba3-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2aba3-255">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-255">Cost actual</span></span></td>
<td><span data-ttu-id="2aba3-256">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="2aba3-257">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="2aba3-258">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="2aba3-259">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="2aba3-260">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-261">Nefakturované skutočné údaje predaja - Zahrnuté v cene</span><span class="sxs-lookup"><span data-stu-id="2aba3-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="2aba3-262">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-263">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="2aba3-264">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-265">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="2aba3-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="2aba3-266">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="2aba3-267">Čas je schválený, a žiadne zníženie fakturovateľných hodín nenastalo počas schvaľovania.</span><span class="sxs-lookup"><span data-stu-id="2aba3-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="2aba3-268">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-268">Cost actual</span></span></td>
<td><span data-ttu-id="2aba3-269">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-270">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-271">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-272">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-273">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="2aba3-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-274">Náklady zdrojovej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="2aba3-275">Zdrojová mena jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-276">Predaj medzi organizáciami</span><span class="sxs-lookup"><span data-stu-id="2aba3-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="2aba3-277">Meny zmluvnej jednotky</span><span class="sxs-lookup"><span data-stu-id="2aba3-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-278">Nefakturované skutočné údaje predaja - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="2aba3-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2aba3-279">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-280">Nefakturované skutočné údaje predaja - Nezahrnuté v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="2aba3-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2aba3-281">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2aba3-282">Faktúra je potvrdená, a žiadna zmena alebo zvýšenie fakturovateľných hodín nenastala.</span><span class="sxs-lookup"><span data-stu-id="2aba3-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2aba3-283">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2aba3-284">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-285">Fakturovaný predaj pre míľnik</span><span class="sxs-lookup"><span data-stu-id="2aba3-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-286">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-287">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="2aba3-288">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-289">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-289">Billed sales</span></span></td>
<td><span data-ttu-id="2aba3-290">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2aba3-291">Faktúra je potvrdená, a žiadne zníženie fakturovateľných hodín nenastalo.</span><span class="sxs-lookup"><span data-stu-id="2aba3-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="2aba3-292">Storno nefakturovaného predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="2aba3-293">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-294">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-295">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-296">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="2aba3-297">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-298">Fakturovaný predaj - Zahrnuté v cene pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="2aba3-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="2aba3-299">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-300">Fakturovaný predaj - Nezahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="2aba3-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="2aba3-301">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="2aba3-302">Faktúra je opravená na zvýšenie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="2aba3-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2aba3-303">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="2aba3-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2aba3-304">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="2aba3-305">Storno fakturovaného predaja pre míľnik</span><span class="sxs-lookup"><span data-stu-id="2aba3-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="2aba3-306">Zmena stavu míľnika z <strong>Fakturovanej</strong> na <strong>Pripravený na faktúru</strong></span><span class="sxs-lookup"><span data-stu-id="2aba3-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="2aba3-307">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-308">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="2aba3-309">Nevzťahuje sa</span><span class="sxs-lookup"><span data-stu-id="2aba3-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-310">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="2aba3-310">Billed sales</span></span></td>
<td><span data-ttu-id="2aba3-311">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="2aba3-312">Faktúra je opravená na zníženie množstva zahrnutého v cene.</span><span class="sxs-lookup"><span data-stu-id="2aba3-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="2aba3-313">Storno fakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="2aba3-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="2aba3-314">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-315">Fakturovaný predaj pre nové množstvo</span><span class="sxs-lookup"><span data-stu-id="2aba3-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="2aba3-316">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="2aba3-317">Nefakturovaný predaj - Zahrnutý v cene pre rozdiel</span><span class="sxs-lookup"><span data-stu-id="2aba3-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="2aba3-318">Meny projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="2aba3-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
