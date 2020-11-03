---
title: Projektové zmluvy
description: Táto téma poskytuje príklady projektových zmlúv, ktoré môžete vytvoriť pre rôzne typy projektov a zdrojov financovania, a ako môžete spravovať zmluvy a fakturovať zákazníkom projektu.
author: Yowelle
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b7d15523f1b22bb8813a47f9f822f12bc4162104
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084495"
---
# <a name="project-contracts"></a><span data-ttu-id="c9ffd-103">Projektové zmluvy</span><span class="sxs-lookup"><span data-stu-id="c9ffd-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9ffd-104">Tento článok poskytuje príklady projektových zmlúv, ktoré môžete vytvoriť pre rôzne typy projektov a zdrojov financovania, a ako môžete spravovať zmluvy a fakturovať zákazníkom projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="c9ffd-105">Typ projektu, ktorý vytvoríte pre projektovú zmluvu, určuje metódu, ktorá sa používa na fakturáciu zákazníkom projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="c9ffd-106">Môžete upraviť projektovú zmluvu a súvisiaci projekt, ale nemôžete zmeniť typ projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="c9ffd-107">Použitím projektovej zmluvy môžete fakturovať jeden alebo viac projektov súčasne.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="c9ffd-108">Zmluva o projekte tiež pomáha zaručiť konzistentný postup fakturácie pre každý podprojekt v štruktúre projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="c9ffd-109">Každý projekt, ktorý bude fakturovaný, musí byť spojený s projektovou zmluvou.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="c9ffd-110">Nastavenia projektovej zmluvy sa vzťahujú na všetky projekty a čiastkové projekty, ktoré sú spojené s danou projektovou zmluvou.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="c9ffd-111">V projektovej zmluve môže byť uvedený jeden alebo viac zdrojov financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="c9ffd-112">Preto môžete rozdeliť fakturáciu medzi viacerých poskytovateľov financovania, nastaviť limity financovania tak, aby sa zdrojom financovania neúčtovalo viac ako zadaná suma, a nakonfigurovať pravidlá financovania účtovania výdavkov.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="c9ffd-113">Financovanie projektových zmlúv</span><span class="sxs-lookup"><span data-stu-id="c9ffd-113">Funding for project contracts</span></span>
<span data-ttu-id="c9ffd-114">Niektoré zmluvy o projekte určujú, že zodpovednosť za financovanie nákladov na projekt je zdieľaných viac strán.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="c9ffd-115">Tu sú niektoré príklady:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-115">Here are some examples:</span></span>

-   <span data-ttu-id="c9ffd-116">Veľký zákazník, ktorý má viac divízií, požaduje, aby sa financovanie projektu rozdelilo podľa divízií.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="c9ffd-117">Vaša spoločnosť zdieľa náklady na veľký projekt s externou organizáciou.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="c9ffd-118">Cestný projekt spolufinancujú dve obce.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="c9ffd-119">Prepojovací projekt je financovaný z vládneho grantu a súkromnej spoločnosti.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="c9ffd-120">V Dynamics 365 Finance, môžete rozdeliť fakturáciu za jednu transakciu alebo za celý projekt medzi viacerých zákazníkov, granty alebo organizácie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="c9ffd-121">V prípade projektov, ktoré majú viacerých donorov, sa všetky strany, ktoré prispievajú na financovanie pokročilého projektu financovania, nazývajú zdroje financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="c9ffd-122">Keď je zákazník, organizácia alebo grant definovaný ako zdroj financovania, možno ho priradiť k jednému alebo viacerým pravidlám financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="c9ffd-123">Pravidlá financovania obsahujú kritériá, ktoré určujú spôsob alokovania poplatkov pre rôzne zdroje financovania projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="c9ffd-124">Pretože položky na sklade, napríklad tie, ktoré sa objavujú na požiadavkách na objednávku a objednávkach, nemožno rozdeliť, nie je možné v čase distribúcie rozdeliť sumu nákladov medzi viac zdrojov financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="c9ffd-125">Preto hodnota zdroja financovania zostáva 0 (nula) až do zaúčtovania emisie zásob.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="c9ffd-126">Keď sa zaúčtuje výdaj zásob, čiastka nákladov sa rozdelí podľa pravidiel distribúcie účtov pre projekt.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="c9ffd-127">Tu je niekoľko krokov, ktoré môžete urobiť, aby ste uľahčili rozdelenie fakturácie medzi viac zdrojov financovania:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="c9ffd-128">Zadajte, aby všetky transakcie, ktoré sú zadané pre projekt, používali rovnakú menu predaja ako zmluva o projekte.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="c9ffd-129">Nastavte limity financovania tak, aby sa za projekt nefinancoval zdroj financovania vyšší ako stanovená suma.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="c9ffd-130">Nakonfigurujte pravidlá financovania a limity financovania pre každého pracovníka, položku, kategóriu, skupinu kategórií a typ transakcie (alebo pre všetky typy transakcií).</span><span class="sxs-lookup"><span data-stu-id="c9ffd-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="c9ffd-131">Vyberte voliteľné dátumy začatia a ukončenia, aby ste určili obdobie, v ktorom je každé pravidlo financovania platné.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="c9ffd-132">Uveďte percento, za ktoré je zodpovedný každý zdroj financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="c9ffd-133">Uveďte, ktorý zdroj financovania je zodpovedný za zaokrúhľovanie rozdielov, ktoré sú spôsobené výpočtami alokácie financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="c9ffd-134">Nastavte pravidlá, ktoré určujú, ako sa náklady na projekt fakturujú externým zákazníkom a účtujú interným organizáciám.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="c9ffd-135">Transakcie zaznamenávajte na pozdržanom finančnom účte, až kým nezískate ďalšie financovanie alebo kým sa nerozhodnete znášať náklady interne.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="c9ffd-136">Na určenie, ktorá daňová skupina sa má priradiť k transakcii, sa v projekte vyhľadá priradenie daňovej skupiny.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="c9ffd-137">Ak na úrovni projektu nebolo vykonané žiadne priradenie daňových skupín, prehľadá sa projektová zmluva.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="c9ffd-138">Príklad: Viacero zdrojov financovania (jednoduché)</span><span class="sxs-lookup"><span data-stu-id="c9ffd-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="c9ffd-139">Nasledujúca tabuľka poskytuje scenáre riadenia alokácie financovania medzi viacerými zdrojmi financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="c9ffd-140">Tieto scenáre sú založené na nasledujúcich predpokladoch:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="c9ffd-141">Nastavenie priorít sa zohľadňuje v alokácii finančných prostriedkov pred uplatnením ďalších kritérií pravidla financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="c9ffd-142">Nebolo určené žiadne časové rozpätie, ktoré by definovalo obdobie d, kedy je pravidlo financovania platné.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9ffd-143"><strong>Scenár</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffd-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="c9ffd-144"><strong>Zdroj financovania</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffd-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="c9ffd-145"><strong>Percento pridelenia</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffd-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="c9ffd-146"><strong>Pridelenie priority</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffd-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9ffd-147">Chcete alokovať náklady na jeden zdroj financovania, kým sa nevyčerpajú jeho finančné prostriedky, alokovať náklady na druhý zdroj financovania, kým sa nevyčerpajú jeho finančné prostriedky, a nakoniec alokovať zvyšné náklady na tretí zdroj financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="c9ffd-148">Zdroj　financovania　1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="c9ffd-149">Zdroj　financovania　2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="c9ffd-150">Zdroj　financovania　3</span><span class="sxs-lookup"><span data-stu-id="c9ffd-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-151">100 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-151">100%</span></span></li>
<li><span data-ttu-id="c9ffd-152">100 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-152">100%</span></span></li>
<li><span data-ttu-id="c9ffd-153">100 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-154">1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-154">1</span></span></li>
<li><span data-ttu-id="c9ffd-155">2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-155">2</span></span></li>
<li><span data-ttu-id="c9ffd-156">3</span><span class="sxs-lookup"><span data-stu-id="c9ffd-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9ffd-157">Chcete prideliť 75 percent nákladov jednému zdroju financovania a 25 percent druhému zdroju financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="c9ffd-158">Keď je ktorýkoľvek z týchto zdrojov financovania vyčerpaný, chcete zaplatiť zostávajúce náklady z tretieho zdroja financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="c9ffd-159">Zdroj　financovania　1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="c9ffd-160">Zdroj　financovania　2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="c9ffd-161">Zdroj　financovania　3</span><span class="sxs-lookup"><span data-stu-id="c9ffd-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-162">75 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-162">75%</span></span></li>
<li><span data-ttu-id="c9ffd-163">25 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-163">25%</span></span></li>
<li><span data-ttu-id="c9ffd-164">100 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-165">1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-165">1</span></span></li>
<li><span data-ttu-id="c9ffd-166">1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-166">1</span></span></li>
<li><span data-ttu-id="c9ffd-167">2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9ffd-168">Chcete prideliť 75 percent nákladov jednému zdroju financovania a 25 percent druhému zdroju financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="c9ffd-169">Keď je ktorýkoľvek z týchto zdrojov financovania vyčerpaný, chcete rozdeliť zostávajúce náklad medzi tretí zdroj financovania a štvrtý zdroj financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="c9ffd-170">Zdroj　financovania　1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="c9ffd-171">Zdroj　financovania　2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="c9ffd-172">Zdroj　financovania　3</span><span class="sxs-lookup"><span data-stu-id="c9ffd-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="c9ffd-173">Zdroj　financovania　4</span><span class="sxs-lookup"><span data-stu-id="c9ffd-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-174">75 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-174">75%</span></span></li>
<li><span data-ttu-id="c9ffd-175">25 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-175">25%</span></span></li>
<li><span data-ttu-id="c9ffd-176">50 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-176">50%</span></span></li>
<li><span data-ttu-id="c9ffd-177">50 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-178">1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-178">1</span></span></li>
<li><span data-ttu-id="c9ffd-179">1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-179">1</span></span></li>
<li><span data-ttu-id="c9ffd-180">2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-180">2</span></span></li>
<li><span data-ttu-id="c9ffd-181">2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9ffd-182">Chcete prideliť prvých 25 percent nákladov jednému zdroju financovania a zvyšok druhému zdroju financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="c9ffd-183">Zdroj　financovania　1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="c9ffd-184">Zdroj　financovania　2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-185">25 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-185">25%</span></span></li>
<li><span data-ttu-id="c9ffd-186">100 %</span><span class="sxs-lookup"><span data-stu-id="c9ffd-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c9ffd-187">1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-187">1</span></span></li>
<li><span data-ttu-id="c9ffd-188">2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="c9ffd-189">Príklad: Viacero zdrojov financovania (komplexné)</span><span class="sxs-lookup"><span data-stu-id="c9ffd-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="c9ffd-190">Máte tri zdroje financovania, ktoré chcete použiť v nasledujúcom poradí:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="c9ffd-191">Používajte zdroj financovania 2 a zdroj financovania 3 rovnako, kým sa nevyčerpá zdroj financovania 2.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="c9ffd-192">Pokračujte v používaní zdroja financovania 3, kým sa nevyčerpá.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="c9ffd-193">Použite zdroj financovania 1 po vyčerpaní zdroja financovania 3.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="c9ffd-194">Ak chcete dosiahnuť tento cieľ, musíte najprv vykonať nasledujúci postup:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="c9ffd-195">Nastavte limity financovania pre zdroj financovania 2 a zdroj financovania 3 pre ich príslušné výšky.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="c9ffd-196">Vytvorte si nasledujúce pravidlá financovania:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="c9ffd-197">Pravidlo 1 (Priorita 1): Prideliť 50 percent transakcií na zdroj financovania 2 a 50 percent na zdroj financovania 3.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="c9ffd-198">Pravidlo 2 (Priorita 2): Prideliť 100 percent transakcií zdroju financovania 3.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="c9ffd-199">Pravidlo 3 (Priorita 3): Prideliť 100 percent transakcií zdroju financovania 1.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="c9ffd-200">Toto nastavenie funguje, pretože transakcie sa kontrolujú podľa pravidiel a obmedzení, aby sa určilo, či sa niektoré z nich na danú transakciu vzťahujú.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="c9ffd-201">Ak sa na transakciu nevzťahujú žiadne konkrétne pravidlá alebo limity, použije sa pravidlo Všetky transakcie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="c9ffd-202">Pravidlo Všetky transakcie sa zhoduje so všetkými transakciami.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="c9ffd-203">Ak sa zistí pravidlo, ktoré sa zhoduje s transakciou, použije sa najskôr percento, ktoré bolo v danom pravidle pridelené, ale až potom, čo sa zhody porovnajú s limitmi, ktoré boli stanovené.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="c9ffd-204">Ak bol limit splnený a zdroje zdroja financovania sú vyčerpané, pravidlo financovania spojené s limitom financovania sa nebude brať do úvahy a program skontroluje ďalšie platné pravidlo.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="c9ffd-205">V niektorých prípadoch možno podľa pravidla prideliť iba časť transakcie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="c9ffd-206">Môže sa to stať, pretože pri alokácii transakcie sa dosiahne limit.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="c9ffd-207">V takom prípade je podľa tohto pravidla pridelená iba určitá suma, napríklad 50 percent na každý zdroj financovania.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="c9ffd-208">To je prípad pravidla 1, ktoré je opísané skôr v tejto časti.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="c9ffd-209">Zvyšok je pridelený podľa nasledujúceho pravidla v poradí.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="c9ffd-210">Nasledujúca tabuľka skúma tento scenár podrobnejšie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9ffd-211"><strong>Zameranie</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffd-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="c9ffd-212"><strong>Podrobné informácie</strong></span><span class="sxs-lookup"><span data-stu-id="c9ffd-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9ffd-213">Pravidlá financovania</span><span class="sxs-lookup"><span data-stu-id="c9ffd-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="c9ffd-214">Pravidlo 1 (priorita 1): Všetky transakcie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="c9ffd-215">Zdroj 2 prideľte na 50% a zdroj financovania 3 na 50%.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="c9ffd-216">Pravidlo 2 (priorita 2): Všetky transakcie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="c9ffd-217">Prideľte zdroj financovania 3 na 100%.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="c9ffd-218">Pravidlo 3 (priorita 2): Všetky transakcie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="c9ffd-219">Prideľte zdroj financovania 1 na 100%.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9ffd-220">Limity financovania</span><span class="sxs-lookup"><span data-stu-id="c9ffd-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="c9ffd-221">Limit zdroja financovania 1 = 10,000.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="c9ffd-222">Limit zdroja financovania 2 = 500.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="c9ffd-223">Limit zdroja financovania 3 = 750.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9ffd-224">Transakcia 1</span><span class="sxs-lookup"><span data-stu-id="c9ffd-224">Transaction 1</span></span></td>
<td><span data-ttu-id="c9ffd-225"><strong>Hodnota transakcie:</strong> 100.00<strong>Financovanie:</strong> Transakcia je platená iba podľa pravidla 1, pretože transakcia je úplne zaplatená po uplatnení pravidla 1.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="c9ffd-226">Transakcia je financovaná rovnakým dielom medzi zdrojom financovania 2 a zdrojom financovania 3.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="c9ffd-227">Zdroj financovania 2: 50.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="c9ffd-228">Zdroj financovania 3: 50.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9ffd-229">Transakcia 2</span><span class="sxs-lookup"><span data-stu-id="c9ffd-229">Transaction 2</span></span></td>
<td><span data-ttu-id="c9ffd-230"><strong>Hodnota transakcie:</strong> 5,000.00<strong>Financovanie:</strong> Transakcia sa platí podľa všetkých troch pravidiel.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="c9ffd-231"><strong>Pravidlo 1</strong>
</span><span class="sxs-lookup"><span data-stu-id="c9ffd-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="c9ffd-232">Zdroj financovania 2: 450.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="c9ffd-233">Zdroj financovania 3: 450.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="c9ffd-234">
<strong>Pravidlo 2</strong>
</span><span class="sxs-lookup"><span data-stu-id="c9ffd-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="c9ffd-235">Zdroj financovania 3: 250.00 (= 750.00 – 50.00 – 450.00)</span><span class="sxs-lookup"><span data-stu-id="c9ffd-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="c9ffd-236">
<strong>Pravidlo 3</strong>
</span><span class="sxs-lookup"><span data-stu-id="c9ffd-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="c9ffd-237">Zdroj financovania 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span><span class="sxs-lookup"><span data-stu-id="c9ffd-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9ffd-238">Celkové prostriedky, ktoré sú rozdelené pre každý zdroj financovania</span><span class="sxs-lookup"><span data-stu-id="c9ffd-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="c9ffd-239">Zdroj financovania 1: 3,850.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="c9ffd-240">Zdroj financovania 2: 500.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="c9ffd-241">Zdroj financovania 3: 750.00</span><span class="sxs-lookup"><span data-stu-id="c9ffd-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="c9ffd-242">Pravidlá fakturácie</span><span class="sxs-lookup"><span data-stu-id="c9ffd-242">Billing rules</span></span>
<span data-ttu-id="c9ffd-243">Pri rokovaniach o zákazke na projekt so zákazníkom definujete, ako a kedy môžete zákazníkovi fakturovať prácu na projekte.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="c9ffd-244">Po nastavení zmluvy o projekte a projektu môžete nastaviť fakturačné pravidlá pre projekt.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="c9ffd-245">Pravidlá fakturácie vychádzajú z podmienok projektu, ktoré sú uvedené v projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="c9ffd-246">Pravidlá fakturácie, ktoré môžete vytvoriť, závisia od podmienok zmluvy o projekte a typu projektu, napríklad Čas a materiál alebo Fixná cena, ktorý priradíte k pravidlu fakturácie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="c9ffd-247">Pre projektovú zmluvu môžete vytvoriť viac ako jedno fakturačné pravidlo.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="c9ffd-248">Pravidlo fakturácie môžete tiež priradiť viacerým projektom, ktoré sú spojené s rovnakou zmluvou o projekte a majú podobné fakturačné podmienky.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="c9ffd-249">Môžete nastaviť nasledujúce typy pravidiel fakturácie:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="c9ffd-250">**Jednotka dodávky** – Fakturujte zákazníka, keď dokončíte jednotku dodávky.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="c9ffd-251">Jednotky dodávky definujete v zmluve.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="c9ffd-252">**Pokrok** - Fakturujte zákazníka, keď dokončíte stanovené percento projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="c9ffd-253">Môžete nastaviť fakturačné pravidlo na automatický výpočet percenta dokončenej práce alebo môžete ručne vypočítať percento dokončenej práce a sumu, ktorá sa má fakturovať zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="c9ffd-254">**Medzník** – Fakturujte zákazníkovi celú sumu medzníka projektu, keď sa tento míľnik dosiahne.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="c9ffd-255">**Poplatok** – Fakturujte zákazníka za svoje služby plus poplatok za správu, čo je zvyčajne percento z ceny služieb.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="c9ffd-256">**Čas a materiál** – Fakturovať zákazníka za hodnotu času a materiálov použitých na projekte.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="c9ffd-257">Pre všetky typy pravidiel fakturácie môžete určiť percento zadržania, ktoré sa odpočíta z faktúr zákazníka, kým projekt nedosiahne dohodnutú fázu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="c9ffd-258">Percento zadržania platby je uvedené v projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="c9ffd-259">Suma sa počíta na základe a od celkovej hodnoty riadkov vo faktúre od zákazníka.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="c9ffd-260">Pre pravidlá fakturácie **Čas a materiál** a **Pokrok** môžete priradiť spoplatnené kategórie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="c9ffd-261">Spoplatnené kategórie označujú transakcie, ktoré by mali byť zahrnuté vo faktúrach zákazníkov.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="c9ffd-262">Keď ste pripravení fakturovať zákazníkovi, suma fakturovaná za projekt sa vypočíta na základe pravidiel fakturácie a vygeneruje sa návrh faktúry projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="c9ffd-263">Nasledujúce časti poskytujú príklady, ktoré ukazujú, ako nastaviť a spravovať pravidlá fakturácie pre projekt.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="c9ffd-264">Príklad: Vytvorte fakturačné pravidlo založené na počte dodaných jednotiek</span><span class="sxs-lookup"><span data-stu-id="c9ffd-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="c9ffd-265">Vaša organizácia uzatvára dohodu o poskytnutí celkovo piatich školení zamestnancom zákazníka za cenu 10 000 za školenie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="c9ffd-266">Fakturujete zákazníkovi po každom školení.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="c9ffd-267">Pri nastavovaní pravidiel fakturácie pre zmluvu používate tieto hodnoty:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="c9ffd-268">Jednotkou dodávky je jedno školenie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="c9ffd-269">Jednotková cena je 10 000 za školenie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="c9ffd-270">Celkový počet jednotiek je päť školení.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="c9ffd-271">Po absolvovaní jedného školenia môžete vytvoriť faktúru za 10 000 kusov za prvú dodanú jednotku a odoslať faktúru zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="c9ffd-272">Príklad: Vytvorte fakturačné pravidlo, ktoré je založené na zadanom percente dokončenia projektu (manuálny výpočet)</span><span class="sxs-lookup"><span data-stu-id="c9ffd-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="c9ffd-273">Vaša organizácia, softvérová konzultačná spoločnosť, uzavrie so zákazníkom dohodu o vývoji časti produktu, ktorý zákazník vyvíja.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="c9ffd-274">Vaša organizácia súhlasí s dodaním softvérového kódu v priebehu šiestich mesiacov.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="c9ffd-275">Zákazník súhlasí s tým, že zaplatí vašej organizácii za prácu celkovo 100 000.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="c9ffd-276">Pravidlo fakturácie vytvoríte tak, aby ste zákazníkovi fakturovali na základe percenta práce dokončenej na projekte, ako je uvedené v zmluve.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="c9ffd-277">Na konci prvého mesiaca sa stretnete so zákazníkom, aby ste určili percento dokončenej práce.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="c9ffd-278">Keď zákazník a zákazník skontrolujú projekt, rozhodnete sa, že je projekt dokončený na 15 percent.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="c9ffd-279">Vytvoríte faktúru za 15,000 (15 percent zo 100 000) a odošlete ju zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="c9ffd-280">Príklad: Vytvorte fakturačné pravidlo, ktoré je založené na zadanom percente dokončenia projektu (automatický výpočet)</span><span class="sxs-lookup"><span data-stu-id="c9ffd-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="c9ffd-281">Vaša organizácia, firma zaoberajúca sa vývojom softvéru, súhlasí s vytvorením balíka mzdového účtovníctva pre zákazníka za 30 000.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="c9ffd-282">Zákazník súhlasí s tým, že zaplatí vašej organizácii na základe percentuálnej hodnoty dokončenej práce.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="c9ffd-283">Odhadujete, že náklady na projekt sú 20 000.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="c9ffd-284">Zmluva o projekte špecifikuje kategórie prác, ktoré použijete v procese fakturácie.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="c9ffd-285">Nastavíte pravidlá fakturácie, ktoré automaticky počítajú čiastky faktúry za percento práce dokončenej pre každú kategóriu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="c9ffd-286">Nastavíte rozpočet pre každú kategóriu:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="c9ffd-287">**Vývoj** - Náklady 15 000 a výnosy 20 000</span><span class="sxs-lookup"><span data-stu-id="c9ffd-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="c9ffd-288">**Inštalácia** - Náklady 5 000 a výnosy 10 000</span><span class="sxs-lookup"><span data-stu-id="c9ffd-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="c9ffd-289">Pri prvom vytváraní zákazníckej faktúry sa suma faktúry automaticky počíta na základe nasledujúcich informácií:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="c9ffd-290">Po mesiaci pracovník projektu odovzdá časový harmonogram projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="c9ffd-291">Náklady na hodiny pracovníka sú 5 000 za vývoj a 1 000 za inštaláciu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="c9ffd-292">Vývojové práce sú dokončené na 33 percent (5 000 skutočných nákladov/15 000 rozpočtových nákladov) a inštalačné práce sú dokončené z 20 percent (1 000 skutočných nákladov/5 000 rozpočtových nákladov).</span><span class="sxs-lookup"><span data-stu-id="c9ffd-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="c9ffd-293">Suma faktúry 8 667 sa počíta automaticky (33 percent z 20 000 + 20 percent z 10 000).</span><span class="sxs-lookup"><span data-stu-id="c9ffd-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="c9ffd-294">Vytvoríte faktúru za 8,667 a odošlete ju zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="c9ffd-295">Príklad: Vytvorte pravidlo fakturácie založené na dohodnutých míľnikoch</span><span class="sxs-lookup"><span data-stu-id="c9ffd-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="c9ffd-296">Vaša organizácia, manažérska poradenská firma, súhlasí s uskutočnením prieskumu trhu so spotrebným produktom, ktorý zákazník plánuje predať.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="c9ffd-297">Zákazník súhlasí s používaním vašich služieb po dobu troch mesiacov, počnúc marcom, a zaväzuje sa zaplatiť vašej organizácii 50 000.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="c9ffd-298">Projekt má tri míľniky:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-298">The project has three milestones:</span></span>

-   <span data-ttu-id="c9ffd-299">Medzník 1: Zhromažďovanie údajov o spotrebiteľoch - 31. marca</span><span class="sxs-lookup"><span data-stu-id="c9ffd-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="c9ffd-300">Míľnik 2: Analýza spotrebiteľských údajov - 30. apríla</span><span class="sxs-lookup"><span data-stu-id="c9ffd-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="c9ffd-301">Míľnik 3: Predstavte návrh životaschopnosti produktu - 31. mája</span><span class="sxs-lookup"><span data-stu-id="c9ffd-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="c9ffd-302">Zákazník súhlasí s tým, že zaplatí vašej organizácii 10 000 za prvý míľnik, 20 000 za druhý míľnik a 20 000 za tretí míľnik.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="c9ffd-303">Pri vytváraní projektovej zmluvy súhlasíte s tým, že zákazníkovi vyúčtujete fakturáciu na základe míľnika, ktorý bol dokončený.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="c9ffd-304">Nastavenie pravidla fakturácie obsahuje nasledujúce kroky:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="c9ffd-305">Definujte míľniky projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-305">Define the project milestones.</span></span>
-   <span data-ttu-id="c9ffd-306">Definujte sumu, ktorá sa má fakturovať zákazníkovi po dokončení každého míľnika.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="c9ffd-307">Keď je prvý míľnik dokončený 31. marca, označíte míľnik ako dokončený, potom vytvoríte faktúru za 10 000 a pošlete ju zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="c9ffd-308">Faktúru za míľnik nemôžete vytvoriť, kým neoznačíte míľnik ako dokončený.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="c9ffd-309">Príklad: Vytvorte fakturačné pravidlo založené na službách plus poplatok za správu</span><span class="sxs-lookup"><span data-stu-id="c9ffd-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="c9ffd-310">Vaša organizácia, konzultačná spoločnosť v oblasti riadenia, súhlasí s vykonaním prieskumu trhu s cieľom vyhodnotiť životaschopnosť produktu, ktorý vyvíja zákazník, maloobchodná spoločnosť.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="c9ffd-311">Podmienky dohody určujú, že budete poskytovať služby svojim trom najlepším konzultantom v oblasti riadenia, ktorí budú výskum uskutočňovať na základe času a materiálov.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="c9ffd-312">Zákazník súhlasí s tým, že zaplatí 100 za hodinu plus 10-percentný poplatok za správu za konzultačné hodiny účtované projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="c9ffd-313">Keď nastavujete projektovú zmluvu, vytvorte pravidlo fakturácie a pripočítajte 10-percentný poplatok za správu k konzultačným hodinám účtovaným projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="c9ffd-314">Pri vytváraní faktúry pre zákazníka sa zákazníkovi účtuje 10-percentný poplatok za správu plus cena za konzultačné hodiny.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="c9ffd-315">Napríklad ak traja konzultanti na projekte pracovali spolu 200 hodín, na základe tohto výpočtu sa vytvorí faktúra za 22 000 kusov:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="c9ffd-316">200 hodín pri 100 za hodinu = 20 000</span><span class="sxs-lookup"><span data-stu-id="c9ffd-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="c9ffd-317">10-percentný poplatok za správu = 2 000</span><span class="sxs-lookup"><span data-stu-id="c9ffd-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="c9ffd-318">Celková suma faktúry = 22 000</span><span class="sxs-lookup"><span data-stu-id="c9ffd-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="c9ffd-319">Ak sú poplatky zdaniteľné zákazníkom a v projektovej zmluve vyberiete skupinu dane z obratu, skupina dane z obratu sa automaticky zadá do pravidla fakturácie poplatkov.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="c9ffd-320">Príklad: Vytvorte fakturačné pravidlo pre hodnotu času a materiálov</span><span class="sxs-lookup"><span data-stu-id="c9ffd-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="c9ffd-321">Vaša organizácia, spoločnosť zaoberajúca sa softvérovým poradenstvom, súhlasí s poskytnutím piatich technických konzultantov na prácu na projekte vývoja softvéru pre zákazníka na nasledujúcich šesť mesiacov.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="c9ffd-322">Zákazník sa zaväzuje zaplatiť 150 za každú konzultačnú hodinu plus náklady na kancelárske potreby.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="c9ffd-323">Vaša organizácia zašle zákazníkovi na konci každého mesiaca faktúru.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="c9ffd-324">Pri uzatváraní zmluvy o projekte súhlasíte s tým, že budete zákazníkovi každý mesiac fakturovať čas a materiály týkajúce sa projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="c9ffd-325">Vytvoríte fakturačné pravidlo, ktoré obsahuje nasledujúce informácie:</span><span class="sxs-lookup"><span data-stu-id="c9ffd-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="c9ffd-326">Zmluvné obdobie je šesť mesiacov.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-326">The contract period is six months.</span></span>
-   <span data-ttu-id="c9ffd-327">Konzultačný čas sa počíta so sadzbou 150 za hodinu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="c9ffd-328">Kancelárske potreby sa fakturujú v cene a celkové náklady na projekt nesmú prekročiť 10 000.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="c9ffd-329">Zákaznícku faktúru vytvoríte na konci každého kalendárneho mesiaca počas projektu.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="c9ffd-330">Počas prvého mesiaca konzultanti projektu zaznamenali spolu 800 hodín.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="c9ffd-331">Náklady na kancelárske potreby, ktoré sa účtujú za projekt, sú 2 000.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="c9ffd-332">Preto na konci mesiaca vytvoríte faktúru za 122 000, ktorá sa počíta ako 800 hodín pri 150 za hodinu, plus 2 000 za kancelárske potreby.</span><span class="sxs-lookup"><span data-stu-id="c9ffd-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>



