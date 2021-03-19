---
title: Navigácia v používateľskom rozhraní
description: Táto téma poskytuje informácie o spravovaní projektu v Dynamics 365 Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 02dda534dcab4e8fee0a96a7e09759c32a669be5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286762"
---
# <a name="navigating-the-user-interface"></a><span data-ttu-id="63725-103">Navigácia v používateľskom rozhraní</span><span class="sxs-lookup"><span data-stu-id="63725-103">Navigating the user interface</span></span>

<span data-ttu-id="63725-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="63725-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="overview"></a><span data-ttu-id="63725-105">Prehľad</span><span class="sxs-lookup"><span data-stu-id="63725-105">Overview</span></span>

<span data-ttu-id="63725-106">Hlavný formulár projektu je rozdelený do niekoľkých kariet.</span><span class="sxs-lookup"><span data-stu-id="63725-106">The main project form is separated into several tabs.</span></span> <span data-ttu-id="63725-107">Každá karta predstavuje inú úroveň podrobností v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="63725-107">Each tab represents a different level of detail within the project.</span></span>

- <span data-ttu-id="63725-108">**Súhrn**: Poskytuje popis projektu a zlučuje plánovanú aj skutočnú výkonnosť projektu.</span><span class="sxs-lookup"><span data-stu-id="63725-108">**Summary**: Provides a description of the project and aggregates both the planned and actual project performance.</span></span>

    ![Karta a polia súhrnu](media/navigation7.png)

- <span data-ttu-id="63725-110">**Úlohy**: Poskytuje podrobnosti týkajúce sa štruktúry rozdelenia práce predstavovanej zobrazením mriežky, zobrazením tabule a Ganttovym grafom.</span><span class="sxs-lookup"><span data-stu-id="63725-110">**Tasks**: Provides the details regarding the work breakdown structure represented by a grid view, board view, and a gantt.</span></span>

    ![Karta a polia úlohy](media/navigation8.png)

- <span data-ttu-id="63725-112">**Tím** : Poskytuje podrobnosti týkajúce sa účastníkov projektu.</span><span class="sxs-lookup"><span data-stu-id="63725-112">**Team**: Provides details regarding the project participants.</span></span> <span data-ttu-id="63725-113">V tomto pohľade je zhrnuté aj vynaložené úsilie každého člena tímu.</span><span class="sxs-lookup"><span data-stu-id="63725-113">The assigned effort of each team member is also summarized in this view.</span></span>

    ![Karta a polia tímu](media/navigation9.png)

- <span data-ttu-id="63725-115">**Priradenia zdrojov**: Poskytuje časovo odstupňovaný pohľad na úsilie každého zdroja v projekte.</span><span class="sxs-lookup"><span data-stu-id="63725-115">**Resource assignments**: Provides a time-phased view of the effort for each resource on a project.</span></span>

    ![Karta a polia priradenia zdrojov](media/navigation10.png)

- <span data-ttu-id="63725-117">**Odsúhlasenie zdrojov** : Poskytuje časovo odstupňované zobrazenie rozdielov medzi priradeniami každého pomenovaného zdroja a ich rezerváciami.</span><span class="sxs-lookup"><span data-stu-id="63725-117">**Resource reconciliation**: Provides a time-phased view of the differences between the assignments of each named resource and their bookings.</span></span>

    ![Karta a polia odsúhlasenia zdroja](media/navigation11.png)

- <span data-ttu-id="63725-119">**Odhady**: Poskytuje časovo odstupňované zobrazenie odhadov nákladov a predaja projektu.</span><span class="sxs-lookup"><span data-stu-id="63725-119">**Estimates**: Provides a time-phased view of the cost and sales estimates of a project.</span></span>

    ![Karta a polia odhadov](media/navigation12.png)

- <span data-ttu-id="63725-121">**Sledovanie**: Poskytuje zobrazenie, ktoré zobrazuje priebeh úloh v štruktúre rozdelenia práce, pokiaľ ide o úsilie, náklady a predaj.</span><span class="sxs-lookup"><span data-stu-id="63725-121">**Tracking**: Provides a view that shows the progress of tasks in the work breakdown structure for effort, cost, and sales.</span></span>

    ![Karta a polia sledovania](media/navigation13.png)

- <span data-ttu-id="63725-123">**Predaj**: Poskytuje priame odkazy na ponuky a zmluvy spojené s projektom.</span><span class="sxs-lookup"><span data-stu-id="63725-123">**Sales**: Provides deep links to quotes and contracts associated with the project.</span></span>

- <span data-ttu-id="63725-124">**Odhady výdavkov**: Poskytuje mriežku, ktorá definuje náklady na projekt na základe kategórií organizačných výdavkov.</span><span class="sxs-lookup"><span data-stu-id="63725-124">**Expense Estimates**: Provides a grid that defines project expenses based upon organizational expense categories.</span></span>

    ![Karta a polia odhadov výdavkov](media/navigation14.png)

## <a name="grid-controls"></a><span data-ttu-id="63725-126">Ovládacie prvky mriežky</span><span class="sxs-lookup"><span data-stu-id="63725-126">Grid controls</span></span>

<span data-ttu-id="63725-127">Sledovanie poskytuje stručný prehľad typických ovládacích prvkov, ktoré sa nachádzajú na rôznych kartách plánovania projektu.</span><span class="sxs-lookup"><span data-stu-id="63725-127">The follow is a brief overview of the typical controls found on the various project planning tabs.</span></span>

### <a name="refresh"></a><span data-ttu-id="63725-128">Obnoviť</span><span class="sxs-lookup"><span data-stu-id="63725-128">Refresh</span></span>

<span data-ttu-id="63725-129">**Obnoviť**: Načíta najnovšie údaje zo servera, ak po načítaní mriežky došlo k akýmkoľvek zmenám.</span><span class="sxs-lookup"><span data-stu-id="63725-129">**Refresh**: Retrieves the latest data from the server if any changes occurred after the grid was loaded.</span></span>

![Tlačidlo Obnoviť](media/navigation7.png)

### <a name="group-by"></a><span data-ttu-id="63725-131">Spôsob zoskupenia</span><span class="sxs-lookup"><span data-stu-id="63725-131">Group by</span></span>

<span data-ttu-id="63725-132">**Zoskupiť podľa**: Aktualizuje zoskupenie riadkov v mriežke tak, aby odrážali zdroje, roly alebo kategórie na základe potrieb používateľa.</span><span class="sxs-lookup"><span data-stu-id="63725-132">**Group by**: Updates the grouping of the rows in the grid to reflect either resources, roles, or categories based on the user's needs.</span></span>

![Zoskupenie podľa tlačidiel](media/navigation6.png)

### <a name="previousnext"></a><span data-ttu-id="63725-134">Predchádzajúce/nasledujúce</span><span class="sxs-lookup"><span data-stu-id="63725-134">Previous/Next</span></span>

<span data-ttu-id="63725-135">**Predchádzajúce**/**Nasledujúce**: Aktualizuje viditeľné časové obdobia na časovo rozložených mriežkach.</span><span class="sxs-lookup"><span data-stu-id="63725-135">**Previous**/**Next**: Update the visible time periods on the time-phased grids.</span></span>

![Tlačidlá Predchádzajúce a Nasledujúce](media/navigation2.png)

### <a name="timescale"></a><span data-ttu-id="63725-137">Časový rozsah</span><span class="sxs-lookup"><span data-stu-id="63725-137">Timescale</span></span>

<span data-ttu-id="63725-138">**Časový rozsah**: Zmena agregácie časovo rozložených údajov medzi dňami, týždňami, mesiacmi a rokmi.</span><span class="sxs-lookup"><span data-stu-id="63725-138">**Timescale**: Change the aggregation of the time-phased data between days, weeks, months, and years.</span></span>

![Tlačidlo časového rozsahu](media/navigation3.png)

### <a name="expand"></a><span data-ttu-id="63725-140">Rozbalenie</span><span class="sxs-lookup"><span data-stu-id="63725-140">Expand</span></span>

<span data-ttu-id="63725-141">**Rozbaliť**: Vykreslí viditeľnú mriežku na celú obrazovku, aby ste lepšie videli ďalšie roly.</span><span class="sxs-lookup"><span data-stu-id="63725-141">**Expand**: Render the visible grid to full screen providing more ability to see additional roles.</span></span>

![tlačidlo Rozbaliť](media/navigation4.png)

### <a name="time-phase-by"></a><span data-ttu-id="63725-143">Obdobie času podľa</span><span class="sxs-lookup"><span data-stu-id="63725-143">Time-phase by</span></span>

<span data-ttu-id="63725-144">**Obdobie času podľa**: Aktualizuje zoskupenie riadkov v mriežke tak, aby odrážalo odhady nákladov pre odhady predaja.</span><span class="sxs-lookup"><span data-stu-id="63725-144">**Time-phase by**: Update the grouping of the rows in the grid to reflect cost estimates for sales estimates.</span></span> <span data-ttu-id="63725-145">Tento ovládací prvok sa vzťahuje aj na skript odhadu a sledovaciu mriežku.</span><span class="sxs-lookup"><span data-stu-id="63725-145">This control also applies to the estimate script and the tracking grid.</span></span>

![Tlačidlo Obdobie času podľa](media/navigation0.png)

### <a name="add-column"></a><span data-ttu-id="63725-147">Pridá stĺpec</span><span class="sxs-lookup"><span data-stu-id="63725-147">Add column</span></span>

<span data-ttu-id="63725-148">**Pridať stĺpec**: Umožňuje používateľovi definovať viditeľné stĺpce v mriežke.</span><span class="sxs-lookup"><span data-stu-id="63725-148">**Add column**: Allows the user to define the visible columns in the grid.</span></span> <span data-ttu-id="63725-149">K mriežkam je možné pridať iba stĺpce dostupné po zakúpení vo formulári **Plánovanie projektu**.</span><span class="sxs-lookup"><span data-stu-id="63725-149">Only out-of-the-box columns can be added to the grids in the **Project Planning** form.</span></span>

![Tlačidlo Pridať stĺpec](media/navigation5.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]