---
title: Priebeh projektu a spotrebu nákladov
description: Táto téma poskytuje informácie o tom, ako sledovať priebeh projektu a spotrebu nákladov.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755644"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="99f72-103">Priebeh projektu a spotrebu nákladov</span><span class="sxs-lookup"><span data-stu-id="99f72-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="99f72-104">Potreba sledovať pokrok v rozvrhu sa líši v závislosti od odvetvia.</span><span class="sxs-lookup"><span data-stu-id="99f72-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="99f72-105">Niektoré odvetvia sledujú na komplexnej úrovni, zatiaľ čo iné odvetvia sledujú na vyššej úrovni.</span><span class="sxs-lookup"><span data-stu-id="99f72-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="99f72-106">Táto téma ukazuje, ako naplánovať, aby spĺňali požiadavky vašej organizácie.</span><span class="sxs-lookup"><span data-stu-id="99f72-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="99f72-107">Zobrazenie sledovania úsilia</span><span class="sxs-lookup"><span data-stu-id="99f72-107">Effort tracking view</span></span>

<span data-ttu-id="99f72-108">Zobrazenie **Sledovanie úsilia** zobrazuje pokrok úloh v pláne.</span><span class="sxs-lookup"><span data-stu-id="99f72-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="99f72-109">Porovnáva skutočné strávené hodiny, ktoré boli strávené na úlohe, s plánovanými hodinami úsilia pre danú úlohu.</span><span class="sxs-lookup"><span data-stu-id="99f72-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="99f72-110">PSA používa nasledujúce vzorce na výpočet metriky sledovania:</span><span class="sxs-lookup"><span data-stu-id="99f72-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="99f72-111">Percento priebehu = skutočné úsilie vynaložené k dnešnému dňu ÷ plánované úsilie na úlohu</span><span class="sxs-lookup"><span data-stu-id="99f72-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="99f72-112">Odhad do dokončenia (ETC) = plánované úsilie – skutočné úsilie vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="99f72-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="99f72-113">Odhad pri dokončení (EAC) = zostávajúce úsilie + skutočné úsilie vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="99f72-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="99f72-114">Odchýlka predpokladaného úsilia = Plánované úsilie – EAC</span><span class="sxs-lookup"><span data-stu-id="99f72-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="99f72-115">PSA ukazuje predpoklad variácie úsilia na úlohe.</span><span class="sxs-lookup"><span data-stu-id="99f72-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="99f72-116">Ak EAC je viac ako plánované úsilie, úloha sa plánuje trvať dlhšie, než bolo pôvodne naplánované.</span><span class="sxs-lookup"><span data-stu-id="99f72-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="99f72-117">Preto je pozadu za plánom.</span><span class="sxs-lookup"><span data-stu-id="99f72-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="99f72-118">Ak EAC je menej ako plánované úsilie, úloha sa plánuje trvať kratšie, než bolo pôvodne naplánované.</span><span class="sxs-lookup"><span data-stu-id="99f72-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="99f72-119">Preto je popredu pred plánom.</span><span class="sxs-lookup"><span data-stu-id="99f72-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="99f72-120">Opätovné predpokladanie úsilia</span><span class="sxs-lookup"><span data-stu-id="99f72-120">Re-projecting effort</span></span>

<span data-ttu-id="99f72-121">Je bežné, že projektový manažér reviduje pôvodné odhady úlohy.</span><span class="sxs-lookup"><span data-stu-id="99f72-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="99f72-122">Projektové opätovné predpoklady sú vnímaním odhadov projektovým manažérom vzhľadom na súčasný stav projektu.</span><span class="sxs-lookup"><span data-stu-id="99f72-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="99f72-123">Neodporúčame však, aby projektoví manažéri menili základné čísla, pretože projektový základ predstavuje etablovaný zdroj pravdivých informácií pre plán projektu a odhad nákladov, čo odsúhlasili všetci účastníci projektu.</span><span class="sxs-lookup"><span data-stu-id="99f72-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="99f72-124">Existujú dva spôsoby, ktoré projektový manažér môže znovu predpokladať úsilie na úlohy:</span><span class="sxs-lookup"><span data-stu-id="99f72-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="99f72-125">Prepísať predvolené ETC s novým odhadom skutočného zostávajúceho úsilia na úlohe.</span><span class="sxs-lookup"><span data-stu-id="99f72-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="99f72-126">Prepísať predvolené percento priebehu s novým odhadom skutočného priebehu úlohy.</span><span class="sxs-lookup"><span data-stu-id="99f72-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="99f72-127">Každý z týchto prístupov spôsobuje prepočítanie úlohy ETC, EAC a percento pokroku a predpokladané úsilie rozptylu úlohy.</span><span class="sxs-lookup"><span data-stu-id="99f72-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="99f72-128">EAC, ETC a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.</span><span class="sxs-lookup"><span data-stu-id="99f72-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="99f72-129">Opätovné predpokladanie úsilia na súhrnné úlohy</span><span class="sxs-lookup"><span data-stu-id="99f72-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="99f72-130">Úsilie o súhrnné úlohy alebo kontajnerové úlohy možno opätovne predpokladať.</span><span class="sxs-lookup"><span data-stu-id="99f72-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="99f72-131">Bez ohľadu na to, či používateľ znova predpokladá projekty pomocou zostávajúceho úsilia alebo percenta pokroku na súhrnné úlohy, začne sa nasledovný súbor výpočtov:</span><span class="sxs-lookup"><span data-stu-id="99f72-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="99f72-132">EAC, ETC a percento pokroku v úlohe sú vypočítané.</span><span class="sxs-lookup"><span data-stu-id="99f72-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="99f72-133">Nové EAC sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pri úlohe pôvodné EAC.</span><span class="sxs-lookup"><span data-stu-id="99f72-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="99f72-134">Vypočíta sa nový odhad pri dokončení na samostatné úlohy až po listový uzol.</span><span class="sxs-lookup"><span data-stu-id="99f72-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="99f72-135">Dotknuté podradené úlohy až po listový uzol majú svoj odhad pri dokončení a percento progresu prepočítané na základe hodnoty odhadu pri dokončení.</span><span class="sxs-lookup"><span data-stu-id="99f72-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="99f72-136">To má za následok nové predpoklady pre variáciu úsilia úlohy.</span><span class="sxs-lookup"><span data-stu-id="99f72-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="99f72-137">Vypočítajú sa súhrnné úlohy EAC až po koreňový uzol.</span><span class="sxs-lookup"><span data-stu-id="99f72-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="99f72-138">Zobrazenie sledovania nákladov</span><span class="sxs-lookup"><span data-stu-id="99f72-138">Cost tracking view</span></span> 

<span data-ttu-id="99f72-139">Zobrazenie **Sledovanie nákladov** porovnáva skutočné náklady, ktoré sa vynaložili na úlohu na plánované náklady na úlohu.</span><span class="sxs-lookup"><span data-stu-id="99f72-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="99f72-140">Toto zobrazenie zobrazuje iba náklady na pracovnú silu a nezahŕňa náklady z odhadov výdavkov.</span><span class="sxs-lookup"><span data-stu-id="99f72-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="99f72-141">PSA používa nasledujúce vzorce na výpočet metriky sledovania:</span><span class="sxs-lookup"><span data-stu-id="99f72-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="99f72-142">Percento spotrebovaných nákladov = skutočné náklady vynaložené k dátumu ÷ plánované náklady na úlohu</span><span class="sxs-lookup"><span data-stu-id="99f72-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="99f72-143">Náklady na dokončenie (CTC) = plánované náklady– skutočné náklady vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="99f72-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="99f72-144">EAC = CTC + skutočné náklady vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="99f72-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="99f72-145">Predpokladaná odchýlka nákladov = plánované náklady – EAC</span><span class="sxs-lookup"><span data-stu-id="99f72-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="99f72-146">Predpoklad variácie nákladov sa zobrazuje v úlohe.</span><span class="sxs-lookup"><span data-stu-id="99f72-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="99f72-147">Ak EAC je viac ako plánované náklady, úloha plánuje stáť viac, než bolo pôvodne naplánované.</span><span class="sxs-lookup"><span data-stu-id="99f72-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="99f72-148">Preto sa to vyvíja nad rozpočtom.</span><span class="sxs-lookup"><span data-stu-id="99f72-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="99f72-149">Ak EAC je menej ako plánované náklady, úloha plánuje stáť menej, než bolo pôvodne naplánované.</span><span class="sxs-lookup"><span data-stu-id="99f72-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="99f72-150">Preto sa to vyvíja pod rozpočtom.</span><span class="sxs-lookup"><span data-stu-id="99f72-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="99f72-151">Opätovné predpokladanie nákladov zo strany projektového manažéra</span><span class="sxs-lookup"><span data-stu-id="99f72-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="99f72-152">Keď je snaha znova predpokladaná, dôjde k spotrebovaniu percenta nákladov CTC, EAC, a prepočítaniu predpokladanej variácie nákladov v zobrazení **Sledovanie nákladov**.</span><span class="sxs-lookup"><span data-stu-id="99f72-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="99f72-153">Súhrn stavu projektu</span><span class="sxs-lookup"><span data-stu-id="99f72-153">Project status summary</span></span>

<span data-ttu-id="99f72-154">Sledovanie údajov v zobrazení **Sledovanie úsilia** a **Sledovania nákladov** zobrazuje priebeh a spotrebu nákladov v koreňovom uzle projektu, súhrnných úlohách a úrovniach úloh listového uzla.</span><span class="sxs-lookup"><span data-stu-id="99f72-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="99f72-155">Časť **Stav** na stránke **Projektová entita** zobrazuje súhrn stavov na projektovej úrovni.</span><span class="sxs-lookup"><span data-stu-id="99f72-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="99f72-156">Polia súhrnu stavu</span><span class="sxs-lookup"><span data-stu-id="99f72-156">Status summary fields</span></span>

<span data-ttu-id="99f72-157">Pole **Celkový stav projektu** je editovateľné pole, ktoré zobrazuje celkový stav projektu.</span><span class="sxs-lookup"><span data-stu-id="99f72-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="99f72-158">Používa farebné kódovanie, ako je zelená, žltá a červená, na označenie rastúceho rizika.</span><span class="sxs-lookup"><span data-stu-id="99f72-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="99f72-159">Pole **Poznámky** umožňuje správcovi projektu zadať konkrétne poznámky o stave.</span><span class="sxs-lookup"><span data-stu-id="99f72-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="99f72-160">Pole **Stav aktualizovaný dňa** nie je možné upravovať a hodnota je časová pečiatka, ktorá indikuje, kedy bol stav naposledy aktualizovaný.</span><span class="sxs-lookup"><span data-stu-id="99f72-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="99f72-161">Polia **Výkonnosť plánu** a **Výkonnosť nákladov** sa nastavujú od dátumu sledovania.</span><span class="sxs-lookup"><span data-stu-id="99f72-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="99f72-162">Keď plán a odchýlka nákladov pre koreňový uzol v zobrazení **Sledovanie úsilia** budú pozitívne, môžete nastaviť tieto polia na možnosť **Popredu**.</span><span class="sxs-lookup"><span data-stu-id="99f72-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="99f72-163">Keď časový rozvrh a odchýlka nákladov pre koreňový uzol sú záporné, môžete ich nastaviť na možnosť **Pozadu**.</span><span class="sxs-lookup"><span data-stu-id="99f72-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
