---
title: Výnosy a náklady projektu
description: Táto téma poskytuje informácie o odhadovaní projektových nákladov a výnosov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 282950c0ee21f430a2f20b21128830891c76c84a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127987"
---
# <a name="project-costs-and-revenue"></a><span data-ttu-id="7d32d-103">Výnosy a náklady projektu</span><span class="sxs-lookup"><span data-stu-id="7d32d-103">Project costs and revenue</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7d32d-104">Odhady projektu poskytujú finančné náhľady pre prácu, ktorá sa odhaduje a plánuje v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-104">Project estimates provide the financial view for work that is estimated and scheduled in the project schedule.</span></span> <span data-ttu-id="7d32d-105">Na karte **odhady** na stránke **projekty** sa zobrazuje vplyv nákladov a výnosov práce, ktorú plánujete.</span><span class="sxs-lookup"><span data-stu-id="7d32d-105">The **Estimates** tab on the **Projects** page shows the cost and revenue impact of the work that you’re planning.</span></span> <span data-ttu-id="7d32d-106">Poskytuje tiež informácie o mnohých preddefinovaných rozmeroch.</span><span class="sxs-lookup"><span data-stu-id="7d32d-106">It also provides information about many predefined dimensions.</span></span> 

> ![Karta odhadov](media/project-5.png)

## <a name="cost-and-sales-values-of-the-project"></a><span data-ttu-id="7d32d-108">Náklady a predajná hodnota projektu</span><span class="sxs-lookup"><span data-stu-id="7d32d-108">Cost and sales values of the project</span></span>

<span data-ttu-id="7d32d-109">Cenníky stanovujú cenu a sadzby fakturácie pre roly v projekte.</span><span class="sxs-lookup"><span data-stu-id="7d32d-109">Price lists define the cost and bill rates for roles in a project.</span></span> <span data-ttu-id="7d32d-110">Na základe rolí, priradených k názvu pozície a pomenovaného zdroja priradeného k úlohe, môžete určiť vplyv práce na náklady a výnosy.</span><span class="sxs-lookup"><span data-stu-id="7d32d-110">You can determine the cost and revenue impact of the work, based on the roles that are associated with the position name and the named resource that is assigned to a task.</span></span> <span data-ttu-id="7d32d-111">Ak existujú úlohy, ktoré nemajú žiadne priradenia (všeobecné alebo pomenované), nemôžete získať odhady nákladov alebo predaja.</span><span class="sxs-lookup"><span data-stu-id="7d32d-111">If there are tasks that don't have any assignments (generic or named), you can’t get cost or sales estimates.</span></span> <span data-ttu-id="7d32d-112">Hodnoty nákladov a predaja zohľadňujú dátum definovaný v cenníkoch.</span><span class="sxs-lookup"><span data-stu-id="7d32d-112">Cost and sales values consider the date that is defined in the price lists.</span></span>

### <a name="default-cost-price"></a><span data-ttu-id="7d32d-113">Predvolený cenník nákladov</span><span class="sxs-lookup"><span data-stu-id="7d32d-113">Default cost price</span></span>  

<span data-ttu-id="7d32d-114">Každý projekt patrí do organizácie.</span><span class="sxs-lookup"><span data-stu-id="7d32d-114">Every project belongs to an organization.</span></span> <span data-ttu-id="7d32d-115">Táto organizácia sa zobrazuje v poli **zmluvná jednotka** projektu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-115">This organization is shown in the **Contracting Unit** field in the project.</span></span> <span data-ttu-id="7d32d-116">Cenník, ktorý je priradený k zmluvnej jednotke, sa používa na určenie obstarávacej ceny jednotky.</span><span class="sxs-lookup"><span data-stu-id="7d32d-116">The price list that is associated with the contracting unit is used to determine the unit cost price.</span></span> <span data-ttu-id="7d32d-117">Na určenie správnej obstarávacej ceny rolí pre dátumu definovaný v odhadovom riadku, kombináciu role, jednotky a organizačnej jednotky v cenníku nákladov.</span><span class="sxs-lookup"><span data-stu-id="7d32d-117">To determine the correct cost prices on roles for the date that is defined on estimate lines, search for the combination of role, unit, and organizational unit in the cost price list.</span></span> 

<span data-ttu-id="7d32d-118">Aby sa mohli vypočítať ich obstarávacie ceny, všetky úlohy musia byť priradené k zdroju.</span><span class="sxs-lookup"><span data-stu-id="7d32d-118">So that their cost prices can be calculated, all tasks must be assigned to a resource.</span></span> <span data-ttu-id="7d32d-119">Akékoľvek nepriradené úlohy budú mať obstarávaciu cenu 0,00.</span><span class="sxs-lookup"><span data-stu-id="7d32d-119">Any uwnassigned tasks will have a cost price of 0.00.</span></span>

<span data-ttu-id="7d32d-120">Ak kombinácia roly, jednotky a organizačnej jednotky nevráti obstarávaciu cenu z cenníka zmluvnej jednotky, systém túto jednotku ignoruje.</span><span class="sxs-lookup"><span data-stu-id="7d32d-120">If the combination of role, unit, and organizational unit doesn't return a cost price from the contracting unit's price list, the system ignores the unit.</span></span> <span data-ttu-id="7d32d-121">Namiesto toho vyhľadá kombináciu len roly a organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="7d32d-121">Instead, it searches for the combination of just role and organizational unit.</span></span> <span data-ttu-id="7d32d-122">Ak sa zistí obstarávacia cena, prepočítavacie koeficienty sa použijú na jej konvertovanie na jednotku, ktorú ste vybrali v riadku odhadu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-122">If a cost price is found, conversion factors are used to convert it to the unit that you selected on the estimate line.</span></span>

<span data-ttu-id="7d32d-123">Ak kombinácia roly a organizačnej jednotky nevráti obstarávaciu cenu z cenníka, systém túto jednotku ignoruje.</span><span class="sxs-lookup"><span data-stu-id="7d32d-123">If the combination of role and organizational unit doesn't return a cost price, the system ignores the organizational unit.</span></span> <span data-ttu-id="7d32d-124">Namiesto toho vyhľadá kombináciu roly a jednotky na nastavenie predvolenej ceny (po použití akejkoľvek konverzie).</span><span class="sxs-lookup"><span data-stu-id="7d32d-124">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="7d32d-125">Ak systém nenájde cenu pre rolu, potom bude obstarávacia cena nastavená na predvolenú hodnotu **0.00** riadku odhadu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-125">If the system doesn't find a price for the role, the cost price on the estimate line is set to a default value of **0.00**.</span></span> <span data-ttu-id="7d32d-126">Všetky hodnoty nákladov v riadkoch odhadov projektových nákladov sú zaznamenané v mene zmluvnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="7d32d-126">All cost amounts on the project cost estimate lines are recorded in the currency of the contracting unit.</span></span>

> [!NOTE]
> <span data-ttu-id="7d32d-127">Predvolene, Microsoft Dynamics 365 ukladá hodnoty nákladov vo vašej základnej mene.</span><span class="sxs-lookup"><span data-stu-id="7d32d-127">By default, Microsoft Dynamics 365 stores cost amounts in your base currency.</span></span> <span data-ttu-id="7d32d-128">Čiastky nákladov, ktoré sú uvedené na karte **odhady**, sú však v mene zmluvnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="7d32d-128">However, the cost amounts that are shown on the **Estimates** tab are in the currency of the contracting unit.</span></span>  

### <a name="default-sales-price"></a><span data-ttu-id="7d32d-129">Predvolené predajné ceny</span><span class="sxs-lookup"><span data-stu-id="7d32d-129">Default sales price</span></span> 

<span data-ttu-id="7d32d-130">Predajný cenník je určený buď predajnou entitou, ku ktorej je projekt pripojený, alebo zákazníkom projektu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-130">The sales price list is determined by either the sales entity that the project is attached to or the project customer.</span></span> <span data-ttu-id="7d32d-131">Keď je predajná entita, ako napríklad príležitosť, cenová ponuka alebo zmluva, priradená k projektu, predajná cena entity predaja je určená cenníkom priradeným k cenovej ponuke alebo zmluve.</span><span class="sxs-lookup"><span data-stu-id="7d32d-131">When a sales entity, such as opportunity, quote, or contract, is associated with the project, the sales entity's sales price is determined by the price list that is associated with the quote or contract.</span></span> <span data-ttu-id="7d32d-132">Ak má cenová ponuka alebo zmluva vlastný cenník, ako predvolený predajný cenník pre odhady projektu je použitý tento predajný cenník.</span><span class="sxs-lookup"><span data-stu-id="7d32d-132">If the quote or contract has a custom price list, that price list is used as the default sales price list for project estimates.</span></span> <span data-ttu-id="7d32d-133">Ak neexistuje žiadna súvislosť s predajnými entitami, predvolený predajný cenník z parametrov sa použije ako predvolený predajný cenník projektu, ktorý je zhodný s menou zákazníka, ktorá je definovaná v projekte.</span><span class="sxs-lookup"><span data-stu-id="7d32d-133">If there is no association with sales entities, the default sales price list from the parameters is used as the project's default sales price list matched by the customer currency that is defined on the project.</span></span>

<span data-ttu-id="7d32d-134">Každý riadok odhadu má zdrojovú jednotku, ktorá je spojená s ním.</span><span class="sxs-lookup"><span data-stu-id="7d32d-134">Each estimate line has a resourcing unit that is associated with it.</span></span> <span data-ttu-id="7d32d-135">Zdrojová jednotka udáva organizačnú jednotku, z ktorej sú rezervované zdroje na dokončenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="7d32d-135">The resourcing unit indicates the organizational unit that resources are booked from to complete the task.</span></span> <span data-ttu-id="7d32d-136">Ak chcete určiť predajnú cenu priradených rolí, vyhľadajte kombináciu roly, jednotky a zdrojovej jednotky v predajnom cenníku.</span><span class="sxs-lookup"><span data-stu-id="7d32d-136">To determine the sales price for the associated roles, search for the combination of role, unit, and resourcing unit in the sales price list.</span></span> <span data-ttu-id="7d32d-137">Ak nie sú k dispozícii žiadne priradenia k úlohe, predajná cena úlohy je 0,00.</span><span class="sxs-lookup"><span data-stu-id="7d32d-137">If there are no assignments on the task, the sales price for the task is 0.00.</span></span>

<span data-ttu-id="7d32d-138">Ak kombinácia roly, jednotky a zdrojovej jednotky nevráti predajnú cenu z predajného cenníka, systém túto jednotku ignoruje.</span><span class="sxs-lookup"><span data-stu-id="7d32d-138">If the combination of role, unit, and resourcing unit doesn't return a sales price from the sales price list, the system ignores the unit.</span></span> <span data-ttu-id="7d32d-139">Namiesto toho vyhľadá kombináciu len roly a zdrojovej jednotky.</span><span class="sxs-lookup"><span data-stu-id="7d32d-139">Instead, it searches for the combination of just role and resourcing unit.</span></span> <span data-ttu-id="7d32d-140">Ak sa nájde predajná cena, prepočítavacie koeficienty sa použijú na jej konvertovanie na jednotku, ktorú ste vybrali v riadku odhadu predaja.</span><span class="sxs-lookup"><span data-stu-id="7d32d-140">If a sales price is found, conversion factors are used to convert it to the unit that you selected on the sales estimate line.</span></span> 

<span data-ttu-id="7d32d-141">Ak kombinácia roly a zdrojovej jednotky nevráti predajnú cenu z predajného cenníka, systém túto zdrojovú jednotku ignoruje.</span><span class="sxs-lookup"><span data-stu-id="7d32d-141">If the combination of role and resourcing unit doesn't return a sales price from the sales price list, the system ignores the resourcing unit.</span></span> <span data-ttu-id="7d32d-142">Namiesto toho vyhľadá kombináciu roly a jednotky na nastavenie predvolenej ceny (po použití akejkoľvek konverzie).</span><span class="sxs-lookup"><span data-stu-id="7d32d-142">Instead, it searches for the combination of role and unit to set the default price (after any conversion is applied).</span></span>

<span data-ttu-id="7d32d-143">Ak systém nenájde cenu pre rolu, potom bude predajná cena nastavená na predvolenú hodnotu **0.00** v riadku odhadu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-143">If the system doesn't find a price for the role, the sales price on the estimate line is set to a default value of **0.00**.</span></span>

<span data-ttu-id="7d32d-144">Karta **odhady** má zobrazenie mriežky, ktoré zobrazuje riadky odhadu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-144">The **Estimates** tab has a grid view that shows estimate lines.</span></span> <span data-ttu-id="7d32d-145">Mriežka obsahuje stĺpce pre jednotku, celkovú obstarávaciu cenu a celkovú predajnú cenu, ako je znázornené na nasledujúcom obrázku.</span><span class="sxs-lookup"><span data-stu-id="7d32d-145">The grid includes columns for the unit, total cost price, and total sales price, as shown in the following illustration.</span></span> 

> ![Zobrazenie mriežky na karte odhady](media/project-6.png)

## <a name="time-phased-view-of-project-estimates"></a><span data-ttu-id="7d32d-147">Odhady času postupne zobrazenie projektu</span><span class="sxs-lookup"><span data-stu-id="7d32d-147">Time-phased view of project estimates</span></span>

<span data-ttu-id="7d32d-148">Časovo delený pohľad na odhady projektov zobrazuje odhad údajov zo zobrazenia mriežky na časovej osi v časovej mierke, ktorú vyberiete.</span><span class="sxs-lookup"><span data-stu-id="7d32d-148">The time-phased view of project estimates shows the estimate data from the grid view across the timeline, in a time scale that you select.</span></span> <span data-ttu-id="7d32d-149">V predvolenom nastavení sa odhad údajov otáča na rozmer **rola**.</span><span class="sxs-lookup"><span data-stu-id="7d32d-149">By default, the estimate data is pivoted on the **Role** dimension.</span></span>

> ![Časovo delený pohľad na odhady projektu](media/project-7.png)

## <a name="allocating-estimated-effort-based-on-the-task-mode"></a><span data-ttu-id="7d32d-151">Pridelenie odhadu úsilia založené na režime úloh</span><span class="sxs-lookup"><span data-stu-id="7d32d-151">Allocating estimated effort based on the task mode</span></span>

<span data-ttu-id="7d32d-152">V zobrazení časového rozloženia rozdeľte celkové úsilie, ktoré je odhadnuté pre úlohu pridelením určitých hodín úsilia na jednotku času vo vybranej časovej mierke.</span><span class="sxs-lookup"><span data-stu-id="7d32d-152">In the time-phased view, you distribute the total effort that is estimated for the task by allocating effort hours per unit time period in the selected time scale.</span></span> <span data-ttu-id="7d32d-153">Režim úlohy určuje, ako sa rozdeľuje úsilie počas trvania úlohy.</span><span class="sxs-lookup"><span data-stu-id="7d32d-153">The task mode determines how effort is allocated across the duration of the task.</span></span> <span data-ttu-id="7d32d-154">Dva druhy pridelenia sú **pravidelné** a **založené na pracovnej dobe**.</span><span class="sxs-lookup"><span data-stu-id="7d32d-154">The two kinds of allocation are **Even** and **Work hours–based**.</span></span>

### <a name="work-hours-based-allocation"></a><span data-ttu-id="7d32d-155">Pridelenie založené na pracovnej dobe</span><span class="sxs-lookup"><span data-stu-id="7d32d-155">Work hours-based allocation</span></span>
 
<span data-ttu-id="7d32d-156">V režime automatického plánovania úloh sa denné predvolené hodiny pre zdroje úlohy nastavujú v plnej pracovnej čase.</span><span class="sxs-lookup"><span data-stu-id="7d32d-156">In auto-scheduling task mode, the daily default hours for task resources are set at the full work hour rate.</span></span> <span data-ttu-id="7d32d-157">Toto správanie platí pri prideľovaní úsilia rozdelením naprieč trvaním úloh aj v časovo delenom zobrazení.</span><span class="sxs-lookup"><span data-stu-id="7d32d-157">This behavior applies when effort is allocated by splitting it across the duration of the task in the time-phased view.</span></span> <span data-ttu-id="7d32d-158">Napríklad ak odhadnete, že úlohu splní jeden zdroj v časovej mierke **deň**, snaha pridelená za deň nepresiahne počet pracovných hodín za deň stanovený v kalendári projektu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-158">For example, if you estimate that a task will be completed by one resource in the **Day** time scale, the effort that is allocated per day won't exceed the work hours per day that are defined in the project calendar.</span></span> <span data-ttu-id="7d32d-159">Preto pridelenie úsilia vždy zabezpečí, že zdroje sú odhadnuté tak, aby sa využívali počas celého dňa.</span><span class="sxs-lookup"><span data-stu-id="7d32d-159">Therefore, the effort allocation always makes sure that the resources are estimated to be used for the full day.</span></span>

### <a name="even-allocation"></a><span data-ttu-id="7d32d-160">Pravidelné pridelenie</span><span class="sxs-lookup"><span data-stu-id="7d32d-160">Even allocation</span></span>

<span data-ttu-id="7d32d-161">V manuálne naplánovanom režime úloh sa pracovné hodiny z kalendára projektu nepoužívajú.</span><span class="sxs-lookup"><span data-stu-id="7d32d-161">In manually scheduled task mode, the work hours from the project calendar aren't used.</span></span> <span data-ttu-id="7d32d-162">Namiesto toho, sa plán úlohy zakladá na vstupoch používateľa.</span><span class="sxs-lookup"><span data-stu-id="7d32d-162">Instead, the task schedule is based on user input.</span></span> <span data-ttu-id="7d32d-163">Pre tieto úlohy nemá úsilie pridelené na jednotku času zvolenej časovej mierky žiadne limitujúce faktory.</span><span class="sxs-lookup"><span data-stu-id="7d32d-163">For these tasks, the effort allocation per unit time period in the selected time scale doesn't have any limiting factor.</span></span> <span data-ttu-id="7d32d-164">Celkové úsilie na úlohu je rovnako rozdelené a pridelené pre každú jednotku času vo zvolenej časovej mierke.</span><span class="sxs-lookup"><span data-stu-id="7d32d-164">The total effort on the task is equally split and allocated for each unit time period in the selected time scale.</span></span> <span data-ttu-id="7d32d-165">Preto, režim úlohy, ktorý je definovaný na úlohe určujúcej rozdelenie úsilia, alebo pridelení úsilia k časovej jednotky v časovo rozdelených odhadoch.</span><span class="sxs-lookup"><span data-stu-id="7d32d-165">Therefore, the task mode that is defined on the task determines the effort distribution, or the allocation of effort per unit time period in time-phased estimates.</span></span>

## <a name="grouping-and-time-phasing-options"></a><span data-ttu-id="7d32d-166">Zoskupenie a možnosti fázovania času</span><span class="sxs-lookup"><span data-stu-id="7d32d-166">Grouping and time-phasing options</span></span>

<span data-ttu-id="7d32d-167">Časovo rozdelené zobrazenie ukazuje rozdelenie úsilia, nákladové a predajné odhady na denných, týždenných, mesačných alebo ročných základoch.</span><span class="sxs-lookup"><span data-stu-id="7d32d-167">The time-phased view shows the distribution of the effort, cost, and sales estimates on a daily, weekly, monthly, or yearly basis.</span></span> <span data-ttu-id="7d32d-168">V predvolenom nastavení sa odhad údajov otáča na rozmer **rola**.</span><span class="sxs-lookup"><span data-stu-id="7d32d-168">By default, the estimate data is pivoted on the **Role** dimension.</span></span> <span data-ttu-id="7d32d-169">Môžete však použiť možnosť **zoskupiť podľa** kontingenčného ovládacieho prvku na dve ďalšie dimenzie: **Kategória** a **zdroj.**</span><span class="sxs-lookup"><span data-stu-id="7d32d-169">However, you can use the **Group By** option to pivot on two other dimensions: **Category** and **Resource**.</span></span>

<span data-ttu-id="7d32d-170">V zobrazení mriežky, aj v časovo delenom zobrazení môžete vybrať, ktoré polia sa zobrazia.</span><span class="sxs-lookup"><span data-stu-id="7d32d-170">In both the grid view and the time-phased view, you can select which fields are shown.</span></span> <span data-ttu-id="7d32d-171">Súčty pre každý časový blok sú zobrazené v spodnej časti projektu.</span><span class="sxs-lookup"><span data-stu-id="7d32d-171">Totals for each time block are shown at the bottom of the project.</span></span> <span data-ttu-id="7d32d-172">Ukazujú celkové odhadované úsilie, náklady a predaje za deň, týždeň, mesiac alebo rok.</span><span class="sxs-lookup"><span data-stu-id="7d32d-172">They show the total estimated effort, cost, and sales for the day, week, month, or year.</span></span> <span data-ttu-id="7d32d-173">Predvolená obstarávacia cena a predajná cena sú dátumovo-efektívne.</span><span class="sxs-lookup"><span data-stu-id="7d32d-173">The default cost price and sales price are date-effective.</span></span> <span data-ttu-id="7d32d-174">Inými slovami, sa zmenia pre každý zdroj, na základe časovo delených zobrazení, ktoré ste vybrali.</span><span class="sxs-lookup"><span data-stu-id="7d32d-174">In other words, they change for each resource, based on the time-phased view that you select.</span></span>

## <a name="expense-estimates"></a><span data-ttu-id="7d32d-175">Odhady nákladov</span><span class="sxs-lookup"><span data-stu-id="7d32d-175">Expense estimates</span></span>

<span data-ttu-id="7d32d-176">Tlačidlo **pridať nový odhad výdavkov** v zobrazení mriežky umožňuje zaznamenať všetky výdavky, ktoré vznikli v projekte, ale ktoré priamo nesúvisia s prácou.</span><span class="sxs-lookup"><span data-stu-id="7d32d-176">The **Add a New Expense Estimate** button in the grid view lets you record any expenses that are incurred in the project, but that aren't directly related to labor.</span></span> <span data-ttu-id="7d32d-177">Môžete zaznamenať odhady výdavkov pre konkrétnu úlohu alebo pre celý projekt.</span><span class="sxs-lookup"><span data-stu-id="7d32d-177">You can record the expense estimates for a specific task or for the entire project.</span></span> <span data-ttu-id="7d32d-178">Vyberte kategórie výdavkov a predbežný dátum, kedy očakávate, že vzniknú náklady.</span><span class="sxs-lookup"><span data-stu-id="7d32d-178">Select expense categories and the tentative date when you expect to incur the expense.</span></span> <span data-ttu-id="7d32d-179">Ak majú súvisiace cenníky nákladov a predajné cenníky predvolené ceny, (alebo sú definované percentá pre kategórie výdavkov), sú automaticky zadané do riadka odhadu keď sa vyskytne priradenie.</span><span class="sxs-lookup"><span data-stu-id="7d32d-179">If the associated cost price list and sales price list have default prices (or if markup percentages are defined for expense categories), they are automatically entered on the estimate line when the association occurs.</span></span>