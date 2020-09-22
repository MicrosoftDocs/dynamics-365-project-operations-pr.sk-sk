---
title: Vytvorte vlastné polia a entity
description: Táto téma vysvetľuje, ako vytvoriť množiny možností a entity vo vlastnom riešení v platforme Power Apps.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755651"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="5907d-103">Vytvorte vlastné polia a entity</span><span class="sxs-lookup"><span data-stu-id="5907d-103">Create custom fields and entities</span></span> 

<span data-ttu-id="5907d-104">Dokončite nasledujúce kroky kedykoľvek, kedy chcete vytvoriť vlastnú množinu možností alebo entitu na Power Apps platforme.</span><span class="sxs-lookup"><span data-stu-id="5907d-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="5907d-105">Postupy v tejto téme by mali byť dokončené pomocou webového rozhrania Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="5907d-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5907d-106">Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení.</span><span class="sxs-lookup"><span data-stu-id="5907d-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="5907d-107">Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu.</span><span class="sxs-lookup"><span data-stu-id="5907d-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="5907d-108">Potom, čo ste vykonali všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.</span><span class="sxs-lookup"><span data-stu-id="5907d-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="5907d-109">Vytvorenie vlastného riešenia pre dimenzie cien</span><span class="sxs-lookup"><span data-stu-id="5907d-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="5907d-110">V PSA, kliknite na **nastavenia** > **riešenia** a potom kliknite na **nové** ak chcete vytvoriť nové riešenie.</span><span class="sxs-lookup"><span data-stu-id="5907d-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="5907d-111">Pomenujte riešenie, **\<názov vašej organizácie>dimenzie cien**, zadajte zostávajúce požadované informácie a potom kliknite na tlačidlo **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="5907d-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Vytvorenie vlastného riešenia pre dimenzie cien](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="5907d-113">Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny</span><span class="sxs-lookup"><span data-stu-id="5907d-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="5907d-114">Cenový rozmer môže byť množina možností alebo entita.</span><span class="sxs-lookup"><span data-stu-id="5907d-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="5907d-115">Obidva musia byť vytvorené vo vašom cenovom riešení.</span><span class="sxs-lookup"><span data-stu-id="5907d-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="5907d-116">Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="5907d-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="5907d-117">Dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="5907d-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="5907d-118">V PSA, kliknite na **nastavenia** > **riešenia** a potom dvojklik na **\<názov vašej organizácie> cenové dimenzie**.</span><span class="sxs-lookup"><span data-stu-id="5907d-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="5907d-119">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity**.</span><span class="sxs-lookup"><span data-stu-id="5907d-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="5907d-120">Kliknite na **nové**, ak chcete vytvoriť novú entitu s názvom **štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="5907d-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="5907d-121">Zadajte zostávajúce požadované informácie a kliknite na **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="5907d-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definícia entity so Štandardným nadpisom](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="5907d-123">Dimenzie založené na množine možností</span><span class="sxs-lookup"><span data-stu-id="5907d-123">Option set-based dimensions</span></span> 
<span data-ttu-id="5907d-124">Môžete vytvoriť dve dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="5907d-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="5907d-125">Použite **miesto pracovného prostriedku** na sledovanie ceny na **domácom** mieste práce a **na mieste** práce a používania **zdrojových pracovných hodín** s hodnotami **pravidelný** a **nadčasy** ak chcete použiť značku pri dokončení práce.</span><span class="sxs-lookup"><span data-stu-id="5907d-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="5907d-126">V PSA, kliknite **nastavenia** > **riešenia** a potom dvojklik na **\<názov vašej organizácie> cenové dimenzie**.</span><span class="sxs-lookup"><span data-stu-id="5907d-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="5907d-127">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Množina možností**.</span><span class="sxs-lookup"><span data-stu-id="5907d-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="5907d-128">Kliknite na **nové**, ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom kliknite na **uložiť**.</span><span class="sxs-lookup"><span data-stu-id="5907d-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="5907d-129">Množina možností na základe cenovej dimenzie nazvanej pracovná poloha zdroja</span><span class="sxs-lookup"><span data-stu-id="5907d-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="5907d-130">Množina možností na základe cenovej dimenzie nazvanej hodinová poloha zdroja</span><span class="sxs-lookup"><span data-stu-id="5907d-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="5907d-131">Vytvorenie údajov pre dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="5907d-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="5907d-132">Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov.</span><span class="sxs-lookup"><span data-stu-id="5907d-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="5907d-133">Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="5907d-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="5907d-134">Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.</span><span class="sxs-lookup"><span data-stu-id="5907d-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="5907d-135">V PSA kliknite na **Rozšírené vyhľadávanie**.</span><span class="sxs-lookup"><span data-stu-id="5907d-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="5907d-136">Vyberte entitu **štandardný nadpis** a potom kliknite na **výsledky**.</span><span class="sxs-lookup"><span data-stu-id="5907d-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="5907d-137">Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.</span><span class="sxs-lookup"><span data-stu-id="5907d-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="5907d-138">Kliknite na položku **Nový**.</span><span class="sxs-lookup"><span data-stu-id="5907d-138">Click **New**.</span></span> <span data-ttu-id="5907d-139">V poli **Názov** zadajte text " Systémový inžinier" a potom kliknite na tlačidlo **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="5907d-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="5907d-140">Zavrite formulár.</span><span class="sxs-lookup"><span data-stu-id="5907d-140">Close the form.</span></span> 
4. <span data-ttu-id="5907d-141">Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".</span><span class="sxs-lookup"><span data-stu-id="5907d-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="5907d-142">Vzorové údaje pre štandardný nadpis entity.</span><span class="sxs-lookup"><span data-stu-id="5907d-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="5907d-143">Pridajte všetky požadované entity PSA a súvisiace súčasti do riešenia dimenzie ceny</span><span class="sxs-lookup"><span data-stu-id="5907d-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="5907d-144">Budete musieť pridať nasledujúce entity služby Project Service na vaše cenové riešenie.</span><span class="sxs-lookup"><span data-stu-id="5907d-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="5907d-145">Postupujte podľa krokov v tomto postupe, tak aby sa niektoré dôležité zmeny schémy v cenovom riešení tak, že entity sa dozvedia o nových cenových dimenziách.</span><span class="sxs-lookup"><span data-stu-id="5907d-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="5907d-146">V PSA, kliknite na **nastavenia** > **riešenia** a potom dvojklik na **\<názov vašej organizácie> cenové dimenzie**.</span><span class="sxs-lookup"><span data-stu-id="5907d-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="5907d-147">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Pridať existujúce** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="5907d-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="5907d-148">V dialógovom okne **súčasti riešenia** vyberte nasledujúce entity:</span><span class="sxs-lookup"><span data-stu-id="5907d-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="5907d-149">Skutočná hodnota</span><span class="sxs-lookup"><span data-stu-id="5907d-149">Actual</span></span>
- <span data-ttu-id="5907d-150">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="5907d-150">Bookable Resource</span></span>
- <span data-ttu-id="5907d-151">Riadok odhadu</span><span class="sxs-lookup"><span data-stu-id="5907d-151">Estimate Line</span></span>
- <span data-ttu-id="5907d-152">Podrobnosti o riadku faktúry</span><span class="sxs-lookup"><span data-stu-id="5907d-152">Invoice Line Detail</span></span>
- <span data-ttu-id="5907d-153">Záznam v účtovnom denníku</span><span class="sxs-lookup"><span data-stu-id="5907d-153">Journal Line</span></span>
- <span data-ttu-id="5907d-154">Podrobnosti o riadku projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="5907d-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="5907d-155">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="5907d-155">Project Team Member</span></span>
- <span data-ttu-id="5907d-156">Podrobnosti o riadku cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="5907d-156">Quote Line Detail</span></span>
- <span data-ttu-id="5907d-157">Prirážka k cene roly</span><span class="sxs-lookup"><span data-stu-id="5907d-157">Role Price Markup</span></span>
- <span data-ttu-id="5907d-158">Cena roly</span><span class="sxs-lookup"><span data-stu-id="5907d-158">Role Price</span></span> 
- <span data-ttu-id="5907d-159">Zadanie času</span><span class="sxs-lookup"><span data-stu-id="5907d-159">Time Entry</span></span> 

> ![Pridanie existujúcich entít do riešenia cenových dimenzií](media/Existing-entities-to-PD-solution.png)

> ![Výber súčastí riešenia](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="5907d-162">Nezabudnite zahrnúť všetky formuláre a zobrazenia pre každú vybranú entitu.</span><span class="sxs-lookup"><span data-stu-id="5907d-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="5907d-163">Keď sa zobrazí výzva na zahrnutie všetkých závislých entít pre entity vybraté vyššie, kliknite na **nie**.</span><span class="sxs-lookup"><span data-stu-id="5907d-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Nezahrnúť súvisiace súčasti](media/Do-not-include-required.png)


