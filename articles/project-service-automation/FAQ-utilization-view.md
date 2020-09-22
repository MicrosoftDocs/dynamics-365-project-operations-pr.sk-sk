---
title: Zobrazte fakturovateľné využívanie zdrojov
description: Táto téma poskytuje informácie o zobrazení využitia zdrojov.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.prod: Applies to all versions of Project Service
ms.technology: Applies to all versions of Project Service
ms.assetid: 656511ac-6851-42d6-abd4-0c7e77ea5d9c
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8953015ced24ff10f0bec2570a840cf4e130b01a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755534"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="f93f7-103">Zobrazte fakturovateľné využívanie zdrojov</span><span class="sxs-lookup"><span data-stu-id="f93f7-103">View chargeable utilization for resources</span></span>
 
<span data-ttu-id="f93f7-104">**Zobrazenie využitia** na stránke **využitie zdrojov Project Service** zobrazuje účtovateľné využitie pre každý rezervovateľný zdroj.</span><span class="sxs-lookup"><span data-stu-id="f93f7-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="f93f7-105">Pretože je zobrazenie založené na tabule plánovania, vďaka čomu tu nájdete veľa rovnakých funkcií.</span><span class="sxs-lookup"><span data-stu-id="f93f7-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Snímka obrazovky zobrazenia využitia](media/FAQ-utilization-1.png)
 

<span data-ttu-id="f93f7-107">Výpočet spoplatneného využitia funguje nasledovne:</span><span class="sxs-lookup"><span data-stu-id="f93f7-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="f93f7-108">Spoplatnené využitie = (Spoplatnená skutočná kapacita hodín) / (kapacita zdroja)</span><span class="sxs-lookup"><span data-stu-id="f93f7-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="f93f7-109">Bunky predstavujú vypočítané spoplatnené využívanie za obdobie vybrané na zobrazenie (dni, týždne alebo mesiace).</span><span class="sxs-lookup"><span data-stu-id="f93f7-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="f93f7-110">Farby v každej bunke zobrazujú spoplatnené využívanie zdroja v porovnaní s ich cieľovým spoplatneným využitím.</span><span class="sxs-lookup"><span data-stu-id="f93f7-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="f93f7-111">Cieľové využitie môžete nastaviť na predvolené roly zdroja, alebo samotných individuálnych zdrojov.</span><span class="sxs-lookup"><span data-stu-id="f93f7-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="f93f7-112">Pri výpočte sa zohľadňuje najprv jednotlivý cieľ, potom predvolená rola zdroja.</span><span class="sxs-lookup"><span data-stu-id="f93f7-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="f93f7-113">Nastaviť cieľ na zdroj</span><span class="sxs-lookup"><span data-stu-id="f93f7-113">Set target on a resource</span></span>

1. <span data-ttu-id="f93f7-114">Prejdite do **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="f93f7-115">Kliknite na zdroj na otvorenie záznamu.</span><span class="sxs-lookup"><span data-stu-id="f93f7-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="f93f7-116">Na karte **Project Service** môžete nastaviť cieľové využitie zdroja.</span><span class="sxs-lookup"><span data-stu-id="f93f7-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Snímka obrazovky využitia karty Project Service na nastavenie cieľového využívania](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="f93f7-118">Nastavenie cieľového využitia na rolu</span><span class="sxs-lookup"><span data-stu-id="f93f7-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="f93f7-119">Prejdite do **Zdroje** \> **role zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="f93f7-120">Kliknite na rola a otvorte záznam.</span><span class="sxs-lookup"><span data-stu-id="f93f7-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="f93f7-121">Nastavte cieľové využitie roly.</span><span class="sxs-lookup"><span data-stu-id="f93f7-121">Set the target utilization for the role.</span></span>

> ![Snímka obrazovky používania Rol zdroja na stanovenie cieľového využitia](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="f93f7-123">Výpočet fakturovateľných využití zdrojov</span><span class="sxs-lookup"><span data-stu-id="f93f7-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="f93f7-124">Pre výpočet fakturovateľných využití zdroja, budete musieť splniť niektoré predpoklady.</span><span class="sxs-lookup"><span data-stu-id="f93f7-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="f93f7-125">Nastaviť predvolenú rolu pre jednotlivé zdroje</span><span class="sxs-lookup"><span data-stu-id="f93f7-125">Set default role for individual resource</span></span>

<span data-ttu-id="f93f7-126">Najprv je potrebné, aby bolo cieľové využitie nastavené buď na individuálnom zdroji alebo v rámci rolí zdroja.</span><span class="sxs-lookup"><span data-stu-id="f93f7-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="f93f7-127">Ak využívate roly zdroja pre ciele, každý jednotlivý zdroj musí mať predvolenú rolu.</span><span class="sxs-lookup"><span data-stu-id="f93f7-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="f93f7-128">Nastavte to v ponuke **Zdroje** a potom \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="f93f7-129">Vyberte zdroj, otvorte záznam a potom vyberte kartu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="f93f7-130">V mriežke **rolí zdroja** sa presvedčte, či je pre prostriedok jedna rola a je to **predvolená hodnota** nastavená na hodnotu **Áno.**</span><span class="sxs-lookup"><span data-stu-id="f93f7-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="f93f7-131">Zmeňte typ fakturácie pre túto rolu zdroja.</span><span class="sxs-lookup"><span data-stu-id="f93f7-131">Change billing type for resource role</span></span>

<span data-ttu-id="f93f7-132">Role prostriedkov je potrebné nastaviť tak, aby mali typ fakturácie **Účtovateľné**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="f93f7-133">Prejdite do **Zdroje** \> **role zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="f93f7-134">Otvorte záznam, ktorý chcete aktualizovať a následne nastavte predvolený typ fakturácie na **Fakturovateľné**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="f93f7-135">Nastavenie pracovnej doby pre role zdrojov</span><span class="sxs-lookup"><span data-stu-id="f93f7-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="f93f7-136">Zdroj musí mať na výpočet kapacity pracovné hodiny.</span><span class="sxs-lookup"><span data-stu-id="f93f7-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="f93f7-137">Prejdite do **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="f93f7-138">Kliknutím na zdroj otvorte záznam a následne kliknite na možnosť **Zobraziť pracovnú dobu**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="f93f7-139">Môžete hromadne aktualizovať zoznam zdrojov priradením **šablóny pracovná doba** zo **zoznamu zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="f93f7-140">Riešenie problémov účtovateľných skutočných údajov hodín</span><span class="sxs-lookup"><span data-stu-id="f93f7-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="f93f7-141">Účtovateľné skutočné údaje hodín sú získavané od entity **skutočných hodnôt**.</span><span class="sxs-lookup"><span data-stu-id="f93f7-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="f93f7-142">Skutočné hodnoty fakturačné typu **zdaniteľné** sú zahrnuté do výpočtu a z tohto dôvodu musíte mať projekty so skutočnými hodnotami, ktoré sú zdaniteľné.</span><span class="sxs-lookup"><span data-stu-id="f93f7-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="f93f7-143">Ak nevidíte účtovateľné využitie, tu sú niektoré veci môžete skontrolovať:</span><span class="sxs-lookup"><span data-stu-id="f93f7-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="f93f7-144">Zdroj má zadefinované pracovné hodiny pre kapacitu.</span><span class="sxs-lookup"><span data-stu-id="f93f7-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="f93f7-145">Prostriedok má buď jednotlivo definované využitie, alebo má priradenú predvolenú rolu.</span><span class="sxs-lookup"><span data-stu-id="f93f7-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="f93f7-146">Rola má zadefinované cieľové využitie.</span><span class="sxs-lookup"><span data-stu-id="f93f7-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="f93f7-147">Skutočné hodnoty majú fakturačný druh **zdaniteľné** na obdobie pre ktoré očakávate využitie výpočtu.</span><span class="sxs-lookup"><span data-stu-id="f93f7-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="f93f7-148">Skontrolujte nasledujúce, ak ste videli skutočné údaje s fakturáciou typy iné než zdaniteľná:</span><span class="sxs-lookup"><span data-stu-id="f93f7-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="f93f7-149">Úloha na skutočné má predvolené fakturačné typu niečo iné než zdaniteľná.</span><span class="sxs-lookup"><span data-stu-id="f93f7-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="f93f7-150">Úloha na riadku zmluvy projektu podporu projektu bol nastavený non-zdaniteľné.</span><span class="sxs-lookup"><span data-stu-id="f93f7-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="f93f7-151">Projekt nemá priradený riadok zmluvy.</span><span class="sxs-lookup"><span data-stu-id="f93f7-151">The project does not have an associated contract line.</span></span>

