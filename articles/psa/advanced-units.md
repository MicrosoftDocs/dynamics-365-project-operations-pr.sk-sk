---
title: Jednotkové skupiny a jednotky
description: Táto téma poskytuje informácie o jednotkových skupinách a jednotkách.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
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
ms.openlocfilehash: e981f39bbb6ca4277778382a5816952df2a8a1fb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009590"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="9a8ba-103">Jednotkové skupiny a jednotky</span><span class="sxs-lookup"><span data-stu-id="9a8ba-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9a8ba-104">Jednotkové skupiny a jednotky sú základnými entitami v Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="9a8ba-105">Jednotka je jediná merná jednotka a viacero jednotiek je možné zoskupiť do skupín jednotiek.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="9a8ba-106">Jednotková skupina sa niekedy označuje ako jednotkový plán v používateľskom rozhraní Dynamics 365 (UI).</span><span class="sxs-lookup"><span data-stu-id="9a8ba-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="9a8ba-107">Tu je niekoľko príkladov jednotiek a jednotkových skupín:</span><span class="sxs-lookup"><span data-stu-id="9a8ba-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="9a8ba-108">**Unit group**: Vzdialenosť</span><span class="sxs-lookup"><span data-stu-id="9a8ba-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="9a8ba-109">**Units**: Míle, Kilometer, a tak ďalej.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="9a8ba-110">**Unit group**: Čas</span><span class="sxs-lookup"><span data-stu-id="9a8ba-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="9a8ba-111">**Units**: Hodina, deň, týždeň, a tak ďalej.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="9a8ba-112">Keď nastavíte viacero jednotiek v jednotkovej skupine, musíte nastaviť tiež konverzný faktor medzi nimi určovaním prvej jednotky, ktorú nastavíte ako predvolenú alebo primárnu jednotku pre jednotkovú skupinu.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="9a8ba-113">Na príklad, ak v jednotkovej skupine **Time** nastavíte **Hour** ako prvú jednotku, systém určí **Hour** ako predvolenú jednotku.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="9a8ba-114">Ak je ďalšia jednotka, ktorú nastavíte, **Day**, musíte nastaviť konverzný faktor **Day** na **Hour**.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="9a8ba-115">Ak potom pridáte **Week** ako tretiu jednotku, musíte nastaviť konverzný faktor pre **Week**, pokiaľ ide o **Day** alebo **Hour**.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="9a8ba-116">Nasledujúci obrázok zobrazuje príklad nastavenia pre jednotku **Day**, kde pole **Quantity** zobrazuje počet hodín, ktoré sú v dni a **Week**, kde pole **Quantity** zobrazuje počet dní, ktoré sú v týždni.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Jednotková skupina: informačná stránka](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="9a8ba-118">Používanie jednotiek a jednotkových skupín</span><span class="sxs-lookup"><span data-stu-id="9a8ba-118">Using units and unit groups</span></span>

<span data-ttu-id="9a8ba-119">Dynamics 365 Project Service Automation používa jednotky a jednotkové skupiny na spracovanie odhadov a položiek pre výdavky aj čas.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="9a8ba-120">V prípade výdavkov má každá kategória výdavkov predvolenú jednotkovú skupinu a jednotku.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="9a8ba-121">Tieto hodnoty sa zadajú ako predvolené hodnoty položiek cenníka pre kategórie výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="9a8ba-122">Napríklad máte kategóriu výdavku ktorá sa nazýva **Mileage**.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="9a8ba-123">Má jednotkovú skupinu, ktorá je pomenovaná **Distance** a predvolenú jednotku, ktorá sa nazýva **Mile**.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="9a8ba-124">Ak nastavíte **Distance** jednotkovú skupinu tak, aby mala dve jednotky (**Mile** a **Kilometer**), môžete nastaviť dve ceny pre kategóriu **Mileage** v jednom cenníku: cena za míľu a cena za kilometer.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="9a8ba-125">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="9a8ba-125">Expense category</span></span>  | <span data-ttu-id="9a8ba-126">Jednotková skupina</span><span class="sxs-lookup"><span data-stu-id="9a8ba-126">Unit group</span></span>  | <span data-ttu-id="9a8ba-127">Jednotka</span><span class="sxs-lookup"><span data-stu-id="9a8ba-127">Unit</span></span>      | <span data-ttu-id="9a8ba-128">Spôsob oceňovania</span><span class="sxs-lookup"><span data-stu-id="9a8ba-128">Pricing method</span></span>  | <span data-ttu-id="9a8ba-129">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="9a8ba-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="9a8ba-130">Cestovné</span><span class="sxs-lookup"><span data-stu-id="9a8ba-130">Mileage</span></span>           | <span data-ttu-id="9a8ba-131">Vzdialenosť</span><span class="sxs-lookup"><span data-stu-id="9a8ba-131">Distance</span></span>      | <span data-ttu-id="9a8ba-132">Míľa</span><span class="sxs-lookup"><span data-stu-id="9a8ba-132">Mile</span></span>      | <span data-ttu-id="9a8ba-133">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="9a8ba-133">Price per unit</span></span>    | <span data-ttu-id="9a8ba-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="9a8ba-134">10 USD</span></span>            |
| <span data-ttu-id="9a8ba-135">Cestovné</span><span class="sxs-lookup"><span data-stu-id="9a8ba-135">Mileage</span></span>           | <span data-ttu-id="9a8ba-136">Vzdialenosť</span><span class="sxs-lookup"><span data-stu-id="9a8ba-136">Distance</span></span>      | <span data-ttu-id="9a8ba-137">Kilometer</span><span class="sxs-lookup"><span data-stu-id="9a8ba-137">Kilometer</span></span> | <span data-ttu-id="9a8ba-138">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="9a8ba-138">Price per unit</span></span>    |  <span data-ttu-id="9a8ba-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="9a8ba-139">6 USD</span></span>            |

<span data-ttu-id="9a8ba-140">Keď zadáte výdavky na projekte, systém určuje cenu prostredníctvom kombinácie kategórie a jednotky na výdavku.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="9a8ba-141">Popis výdavku</span><span class="sxs-lookup"><span data-stu-id="9a8ba-141">Expense description</span></span>        | <span data-ttu-id="9a8ba-142">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="9a8ba-142">Expense category</span></span>  | <span data-ttu-id="9a8ba-143">Jednotka</span><span class="sxs-lookup"><span data-stu-id="9a8ba-143">Unit</span></span>  | <span data-ttu-id="9a8ba-144">Množstvo</span><span class="sxs-lookup"><span data-stu-id="9a8ba-144">Quantity</span></span>  | <span data-ttu-id="9a8ba-145">Jednotková cena</span><span class="sxs-lookup"><span data-stu-id="9a8ba-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="9a8ba-146">Jazda ku klientovi</span><span class="sxs-lookup"><span data-stu-id="9a8ba-146">Drive to client location</span></span> | <span data-ttu-id="9a8ba-147">Cestovné</span><span class="sxs-lookup"><span data-stu-id="9a8ba-147">Mileage</span></span>             | <span data-ttu-id="9a8ba-148">Míľa</span><span class="sxs-lookup"><span data-stu-id="9a8ba-148">Mile</span></span>  | <span data-ttu-id="9a8ba-149">10</span><span class="sxs-lookup"><span data-stu-id="9a8ba-149">10</span></span>        | <span data-ttu-id="9a8ba-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="9a8ba-150">10 USD</span></span>         |

<span data-ttu-id="9a8ba-151">Pre čas, má každá hlavička cenníka pole **Default Time Unit**.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="9a8ba-152">Hodnota sa nastaví pri vytváraní hlavičky cenníka.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="9a8ba-153">Táto jednotka sa potom použije na nastavenie všetkých cien založených na roli v tomto cenníku.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="9a8ba-154">Odhadované riadky pre pole **Time on Quote** možno vyjadriť v ktorejkoľvek časovej jednotke.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="9a8ba-155">Avšak, odhadované riadky na projektoch a časových záznamoch v projektoch však môže používať len **Hour** jednotku času.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="9a8ba-156">Ak jednotka v zázname času alebo riadok odhadu nezodpovedá jednotke v riadku cenníka pre túto rolu, systém skonvertuje cenu na jednotky, ktoré sú definované v projektovom odhade alebo v skutočnej transakcii projektu.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="9a8ba-157">Nasledujúci príklad ukazuje, ako PSA používa jednotkové skupiny, jednotky a konverzné faktory.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="9a8ba-158">Jednotky</span><span class="sxs-lookup"><span data-stu-id="9a8ba-158">Units</span></span>

   - <span data-ttu-id="9a8ba-159">**Unit group**: Čas</span><span class="sxs-lookup"><span data-stu-id="9a8ba-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="9a8ba-160">**Units**: Hodina</span><span class="sxs-lookup"><span data-stu-id="9a8ba-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="9a8ba-161">**Day** - Konverzný faktor: 8 hodín</span><span class="sxs-lookup"><span data-stu-id="9a8ba-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="9a8ba-162">**Week** - Konverzný faktor: 40 hodín</span><span class="sxs-lookup"><span data-stu-id="9a8ba-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="9a8ba-163">Nastavenie cenníka v Projekte A:</span><span class="sxs-lookup"><span data-stu-id="9a8ba-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="9a8ba-164">**Name**: UK predajné ceny 2016</span><span class="sxs-lookup"><span data-stu-id="9a8ba-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="9a8ba-165">**Default time unit**: Deň</span><span class="sxs-lookup"><span data-stu-id="9a8ba-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="9a8ba-166">**Mena**: GBP</span><span class="sxs-lookup"><span data-stu-id="9a8ba-166">**Currency**: GBP</span></span>

| <span data-ttu-id="9a8ba-167">Rola</span><span class="sxs-lookup"><span data-stu-id="9a8ba-167">Role</span></span>      | <span data-ttu-id="9a8ba-168">Jednotková skupina</span><span class="sxs-lookup"><span data-stu-id="9a8ba-168">Unit group</span></span> | <span data-ttu-id="9a8ba-169">Jednotka</span><span class="sxs-lookup"><span data-stu-id="9a8ba-169">Unit</span></span> | <span data-ttu-id="9a8ba-170">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="9a8ba-170">Organizational unit</span></span> | <span data-ttu-id="9a8ba-171">Cena</span><span class="sxs-lookup"><span data-stu-id="9a8ba-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="9a8ba-172">Vývojár</span><span class="sxs-lookup"><span data-stu-id="9a8ba-172">Developer</span></span> | <span data-ttu-id="9a8ba-173">Čas</span><span class="sxs-lookup"><span data-stu-id="9a8ba-173">Time</span></span>       | <span data-ttu-id="9a8ba-174">Deň</span><span class="sxs-lookup"><span data-stu-id="9a8ba-174">Day</span></span>  | <span data-ttu-id="9a8ba-175">Contoso UK</span><span class="sxs-lookup"><span data-stu-id="9a8ba-175">Contoso UK</span></span>          | <span data-ttu-id="9a8ba-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="9a8ba-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="9a8ba-177">Zadanie času</span><span class="sxs-lookup"><span data-stu-id="9a8ba-177">Time entry</span></span>

<span data-ttu-id="9a8ba-178">Nasledujúca tabuľka zobrazuje výslednú transakciu na strane predaja vytvorenú spoločnosťou PSA pre trojhodinový projekt.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="9a8ba-179">Projekt</span><span class="sxs-lookup"><span data-stu-id="9a8ba-179">Project</span></span>   | <span data-ttu-id="9a8ba-180">Úloha</span><span class="sxs-lookup"><span data-stu-id="9a8ba-180">Task</span></span>    | <span data-ttu-id="9a8ba-181">Rola</span><span class="sxs-lookup"><span data-stu-id="9a8ba-181">Role</span></span>      | <span data-ttu-id="9a8ba-182">Množstvo</span><span class="sxs-lookup"><span data-stu-id="9a8ba-182">Quantity</span></span> | <span data-ttu-id="9a8ba-183">Jednotka</span><span class="sxs-lookup"><span data-stu-id="9a8ba-183">Unit</span></span>  | <span data-ttu-id="9a8ba-184">Jednotková cena</span><span class="sxs-lookup"><span data-stu-id="9a8ba-184">Unit price</span></span> | <span data-ttu-id="9a8ba-185">Suma nevyfakturovaného predaja</span><span class="sxs-lookup"><span data-stu-id="9a8ba-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="9a8ba-186">Projekt A</span><span class="sxs-lookup"><span data-stu-id="9a8ba-186">Project A</span></span> | <span data-ttu-id="9a8ba-187">Navrhnúť</span><span class="sxs-lookup"><span data-stu-id="9a8ba-187">Design</span></span>  | <span data-ttu-id="9a8ba-188">Vývojár</span><span class="sxs-lookup"><span data-stu-id="9a8ba-188">Developer</span></span> | <span data-ttu-id="9a8ba-189">3</span><span class="sxs-lookup"><span data-stu-id="9a8ba-189">3</span></span>        | <span data-ttu-id="9a8ba-190">Hour</span><span class="sxs-lookup"><span data-stu-id="9a8ba-190">Hour</span></span>  | <span data-ttu-id="9a8ba-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="9a8ba-191">100 GBP</span></span>    | <span data-ttu-id="9a8ba-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="9a8ba-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="9a8ba-193">FAQ časových jednotiek</span><span class="sxs-lookup"><span data-stu-id="9a8ba-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="9a8ba-194">Konvertuje PSA na rôzne jednotky v prípade výdavkov?</span><span class="sxs-lookup"><span data-stu-id="9a8ba-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="9a8ba-195">Nie.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-195">No.</span></span> <span data-ttu-id="9a8ba-196">Konverzia jednotky funguje len pre čas.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-196">Unit conversion works only for time.</span></span> <span data-ttu-id="9a8ba-197">Pre výdavky, ak systém nemôže nájsť cenu pre kombináciu výdavkovej kategórie a jednotky, cena je nastavená na 0,00 predvolene.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="9a8ba-198">Prečo PSA konvertuje časové jednotky?</span><span class="sxs-lookup"><span data-stu-id="9a8ba-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="9a8ba-199">V niektorých krajinách alebo regiónoch existuje zákonná požiadavka, aby sa fakturačné sadzby stanovili v dňoch.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="9a8ba-200">Cenové vyjednávanie a poskytovanie zliav počas cyklu cenovej ponuky sa vykonáva pomocou dennej sadzby pre každú fakturovateľnú rolu.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="9a8ba-201">Harmonogram odhadu a záznam času sa vykonáva v hodinách.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="9a8ba-202">Na podporu tohto rozdielu v časových jednotkách, PSA konvertuje časové jednotky.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="9a8ba-203">Je možné zmeniť časové jednotky na odhady projektu?</span><span class="sxs-lookup"><span data-stu-id="9a8ba-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="9a8ba-204">Nie.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-204">No.</span></span> <span data-ttu-id="9a8ba-205">Odhad plánu je momentálne obmedzený na hodiny a nedá sa zmeniť.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="9a8ba-206">Môžu byť jednotky a jednotkové skupiny upravené, vymazané a pridané?</span><span class="sxs-lookup"><span data-stu-id="9a8ba-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="9a8ba-207">Áno.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-207">Yes.</span></span> <span data-ttu-id="9a8ba-208">S výnimkou **Time** jednotkových skupín a **Hour** jednotky je možné všetky jednotky odstrániť alebo upraviť a pridať nové jednotky.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="9a8ba-209">V PSA nie je možné **Time** jednotkovú skupinu a **Hour** jednotku odstrániť.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="9a8ba-210">Avšak môžu byť aktualizované s preloženým textom pre pole **Name**.</span><span class="sxs-lookup"><span data-stu-id="9a8ba-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]