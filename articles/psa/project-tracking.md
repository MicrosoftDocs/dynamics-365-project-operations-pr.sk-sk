---
title: Priebeh projektu a využitie nákladov
description: Táto téma poskytuje informácie o tom, ako sledovať priebeh projektu a spotrebu nákladov.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 73b23aad2976c8ccbb542fc2dda1d96dd9f5714b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283657"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="96dc2-103">Priebeh projektu a využitie nákladov</span><span class="sxs-lookup"><span data-stu-id="96dc2-103">Project progress and cost consumption</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="96dc2-104">Potreba sledovať pokrok v rozvrhu sa líši v závislosti od odvetvia.</span><span class="sxs-lookup"><span data-stu-id="96dc2-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="96dc2-105">Niektoré odvetvia sledujú na komplexnej úrovni, zatiaľ čo iné odvetvia sledujú na vyššej úrovni.</span><span class="sxs-lookup"><span data-stu-id="96dc2-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="96dc2-106">Táto téma ukazuje, ako naplánovať, aby spĺňali požiadavky vašej organizácie.</span><span class="sxs-lookup"><span data-stu-id="96dc2-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="96dc2-107">Zobrazenie sledovania úsilia</span><span class="sxs-lookup"><span data-stu-id="96dc2-107">Effort tracking view</span></span>

<span data-ttu-id="96dc2-108">Zobrazenie **Sledovanie úsilia** zobrazuje pokrok úloh v pláne.</span><span class="sxs-lookup"><span data-stu-id="96dc2-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="96dc2-109">Porovnáva skutočné strávené hodiny úsilia na úlohe s plánovanými hodinami úsilia na úlohe.</span><span class="sxs-lookup"><span data-stu-id="96dc2-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="96dc2-110">Project Service Automation používa nasledujúce vzorce na výpočet metriky sledovania:</span><span class="sxs-lookup"><span data-stu-id="96dc2-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="96dc2-111">Na začiatku pri vytváraní úlohy: Plánované náklady sa nastavia na Odhad nákladov pri dokončení.</span><span class="sxs-lookup"><span data-stu-id="96dc2-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="96dc2-112">Po zaznamenaní skutočných hodnôt v úlohe sa objaví nasledujúci výpočet v zobrazení sledovania úsilia</span><span class="sxs-lookup"><span data-stu-id="96dc2-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="96dc2-113">Percento priebehu = skutočné úsilie vynaložené k dnešnému dňu ÷ odhad pri dokončení (EAC)</span><span class="sxs-lookup"><span data-stu-id="96dc2-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="96dc2-114">Odhad do dokončenia (ETC) = Odhad pri dokončení (EAC) - skutočné úsilie vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="96dc2-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="96dc2-115">Odhad pri dokončení (EAC) = zostávajúce úsilie + skutočné úsilie vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="96dc2-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="96dc2-116">Odchýlka predpokladaného úsilia = Plánované úsilie – EAC</span><span class="sxs-lookup"><span data-stu-id="96dc2-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="96dc2-117">Project Service Automation ukazuje predpoklad variácie úsilia na úlohe.</span><span class="sxs-lookup"><span data-stu-id="96dc2-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="96dc2-118">Ak EAC je viac ako plánované úsilie, úloha sa plánuje trvať dlhšie, než bolo pôvodne naplánované.</span><span class="sxs-lookup"><span data-stu-id="96dc2-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="96dc2-119">Preto je pozadu za plánom.</span><span class="sxs-lookup"><span data-stu-id="96dc2-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="96dc2-120">Ak EAC je menej ako plánované úsilie, úloha sa plánuje trvať kratšie, než bolo pôvodne naplánované.</span><span class="sxs-lookup"><span data-stu-id="96dc2-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="96dc2-121">Preto je popredu pred plánom.</span><span class="sxs-lookup"><span data-stu-id="96dc2-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="96dc2-122">Opätovné predpokladanie úsilia</span><span class="sxs-lookup"><span data-stu-id="96dc2-122">Reprojecting effort</span></span>

<span data-ttu-id="96dc2-123">Je bežné, že projektový manažér reviduje pôvodné odhady úlohy.</span><span class="sxs-lookup"><span data-stu-id="96dc2-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="96dc2-124">Projektové opätovné predpoklady sú vnímaním odhadov projektovým manažérom vzhľadom na súčasný stav projektu.</span><span class="sxs-lookup"><span data-stu-id="96dc2-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="96dc2-125">Neodporúčame však, aby projektoví manažéri menili základné čísla, pretože projektový základ predstavuje etablovaný zdroj pravdivých informácií pre plán projektu a odhad nákladov, čo odsúhlasili všetci účastníci projektu.</span><span class="sxs-lookup"><span data-stu-id="96dc2-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="96dc2-126">Existujú dva spôsoby, ktoré projektový manažér môže znovu predpokladať úsilie na úlohy:</span><span class="sxs-lookup"><span data-stu-id="96dc2-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="96dc2-127">Prepísať predvolené ETC s novým odhadom skutočného zostávajúceho úsilia na úlohe.</span><span class="sxs-lookup"><span data-stu-id="96dc2-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="96dc2-128">Prepísať predvolené percento priebehu s novým odhadom skutočného priebehu úlohy.</span><span class="sxs-lookup"><span data-stu-id="96dc2-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="96dc2-129">Každý z týchto prístupov spôsobuje prepočítanie úlohy ETC, EAC a percento pokroku a predpokladané úsilie rozptylu úlohy.</span><span class="sxs-lookup"><span data-stu-id="96dc2-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="96dc2-130">EAC, ETC a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový predpoklad variácie úsilia.</span><span class="sxs-lookup"><span data-stu-id="96dc2-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="96dc2-131">Opätovné predpokladanie úsilia na súhrnné úlohy</span><span class="sxs-lookup"><span data-stu-id="96dc2-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="96dc2-132">Úsilie o súhrnné úlohy alebo kontajnerové úlohy možno opätovne predpokladať.</span><span class="sxs-lookup"><span data-stu-id="96dc2-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="96dc2-133">Bez ohľadu na to, či používateľ znova predpokladá projekty pomocou zostávajúceho úsilia alebo percenta pokroku na súhrnné úlohy, začne sa nasledovný súbor výpočtov:</span><span class="sxs-lookup"><span data-stu-id="96dc2-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="96dc2-134">EAC, ETC a percento pokroku v úlohe sú vypočítané.</span><span class="sxs-lookup"><span data-stu-id="96dc2-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="96dc2-135">Nové EAC sa rozdelí na podradené úlohy v rovnakom pomere ako bolo pri úlohe pôvodné EAC.</span><span class="sxs-lookup"><span data-stu-id="96dc2-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="96dc2-136">Vypočíta sa nový odhad pri dokončení na samostatné úlohy až po listový uzol.</span><span class="sxs-lookup"><span data-stu-id="96dc2-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="96dc2-137">Dotknuté podradené úlohy až po listový uzol majú svoj odhad pri dokončení a percento progresu prepočítané na základe hodnoty odhadu pri dokončení.</span><span class="sxs-lookup"><span data-stu-id="96dc2-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="96dc2-138">To má za následok nové predpoklady pre variáciu úsilia úlohy.</span><span class="sxs-lookup"><span data-stu-id="96dc2-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="96dc2-139">Vypočítajú sa súhrnné úlohy EAC až po koreňový uzol.</span><span class="sxs-lookup"><span data-stu-id="96dc2-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="96dc2-140">Zobrazenie sledovania nákladov</span><span class="sxs-lookup"><span data-stu-id="96dc2-140">Cost tracking view</span></span> 

<span data-ttu-id="96dc2-141">Zobrazenie **Sledovanie nákladov** porovnáva skutočné náklady, ktoré sa vynaložili na úlohu na plánované náklady.</span><span class="sxs-lookup"><span data-stu-id="96dc2-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="96dc2-142">Toto zobrazenie zobrazuje iba náklady na pracovnú silu a nezahŕňa náklady z odhadov výdavkov.</span><span class="sxs-lookup"><span data-stu-id="96dc2-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="96dc2-143">Project Service Automation používa nasledujúce vzorce na výpočet metriky sledovania:</span><span class="sxs-lookup"><span data-stu-id="96dc2-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="96dc2-144">Po vytvorení úlohy sa plánované náklady rovnajú odhadu nákladov pri dokončení.</span><span class="sxs-lookup"><span data-stu-id="96dc2-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="96dc2-145">Po zaznamenaní skutočných hodnôt v úlohe sa objaví nasledujúci výpočet v zobrazení **Sledovanie** pre náklady:</span><span class="sxs-lookup"><span data-stu-id="96dc2-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="96dc2-146">Percento spotrebovaných nákladov = skutočné náklady vynaložené k dátumu ÷ Odhad nákladov pri dokončení pre úlohu</span><span class="sxs-lookup"><span data-stu-id="96dc2-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="96dc2-147">Náklady na dokončenie (CTC) = Odhad nákladov pri dokončení – skutočné náklady vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="96dc2-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="96dc2-148">Odhad nákladov pri dokončení = CTC + skutočné náklady vynaložené k dnešnému dňu</span><span class="sxs-lookup"><span data-stu-id="96dc2-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="96dc2-149">Rozpätie predpokladaných nákladov = Plánované náklady - Odhad nákladov pri dokončení</span><span class="sxs-lookup"><span data-stu-id="96dc2-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="96dc2-150">Predpoklad variácie nákladov sa zobrazuje v úlohe.</span><span class="sxs-lookup"><span data-stu-id="96dc2-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="96dc2-151">Ak je odhad nákladov pri dokončení viac ako plánované náklady, predpokladá sa, že úloha bude stáť viac, než bolo pôvodne naplánované.</span><span class="sxs-lookup"><span data-stu-id="96dc2-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="96dc2-152">Preto sa to vyvíja nad rozpočtom.</span><span class="sxs-lookup"><span data-stu-id="96dc2-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="96dc2-153">Ak je odhad nákladov pri dokončení menej ako plánované náklady, predpokladá sa, že úloha bude stáť menej, než bolo pôvodne naplánované, a vyvíja sa v rámci rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="96dc2-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="96dc2-154">Opätovné predpokladanie nákladov zo strany projektového manažéra</span><span class="sxs-lookup"><span data-stu-id="96dc2-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="96dc2-155">Keď je snaha znova predpokladaná, dôjde k spotrebovaniu percenta nákladov CTC, odhadu nákladov pri dokončení, a prepočítaniu predpokladanej variácie nákladov v zobrazení **Sledovanie nákladov**.</span><span class="sxs-lookup"><span data-stu-id="96dc2-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="96dc2-156">Súhrn stavu projektu</span><span class="sxs-lookup"><span data-stu-id="96dc2-156">Project status summary</span></span>

<span data-ttu-id="96dc2-157">Sledovanie údajov v zobrazení **Sledovanie úsilia** a **Sledovania nákladov** zobrazuje priebeh a spotrebu nákladov v koreňovom uzle projektu, súhrnných úlohách a úrovniach úloh listového uzla.</span><span class="sxs-lookup"><span data-stu-id="96dc2-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="96dc2-158">Časť **Stav** na stránke **Projektová entita** zobrazuje súhrn stavov na projektovej úrovni.</span><span class="sxs-lookup"><span data-stu-id="96dc2-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="96dc2-159">Polia súhrnu stavu</span><span class="sxs-lookup"><span data-stu-id="96dc2-159">Status summary fields</span></span>

<span data-ttu-id="96dc2-160">Pole **Celkový stav projektu** je editovateľné pole, ktoré zobrazuje celkový stav projektu.</span><span class="sxs-lookup"><span data-stu-id="96dc2-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="96dc2-161">Používa farebné kódovanie, ako je zelená, žltá a červená, na označenie rastúceho rizika.</span><span class="sxs-lookup"><span data-stu-id="96dc2-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="96dc2-162">Pole **Poznámky** umožňuje správcovi projektu zadať konkrétne poznámky o stave.</span><span class="sxs-lookup"><span data-stu-id="96dc2-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="96dc2-163">Pole **Stav aktualizovaný dňa** nie je možné upravovať a hodnota je časová pečiatka, ktorá indikuje, kedy bol stav naposledy aktualizovaný.</span><span class="sxs-lookup"><span data-stu-id="96dc2-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="96dc2-164">Polia **Výkonnosť plánu** a **Výkonnosť nákladov** sa nastavujú od dátumu sledovania.</span><span class="sxs-lookup"><span data-stu-id="96dc2-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="96dc2-165">Keď plán a odchýlka nákladov pre koreňový uzol v zobrazení **Sledovanie úsilia** budú pozitívne, môžete nastaviť tieto polia na možnosť **Popredu**.</span><span class="sxs-lookup"><span data-stu-id="96dc2-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="96dc2-166">Keď časový rozvrh a odchýlka nákladov pre koreňový uzol sú záporné, môžete ich nastaviť na možnosť **Pozadu**.</span><span class="sxs-lookup"><span data-stu-id="96dc2-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]