---
title: Vytvorenie vlastných polí a entít ako cenových dimenzií
description: Táto téma poskytuje informácie o tom, ako vytvoriť vlastné množiny možností alebo entity.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9dd43be79f8e906298578911b3bff03e66c2f1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084402"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="3d20a-103">Vytvorenie vlastných polí a entít ako cenových dimenzií</span><span class="sxs-lookup"><span data-stu-id="3d20a-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="3d20a-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="3d20a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3d20a-105">Vykonajte nasledujúce kroky kedykoľvek, kedy chcete vytvoriť vlastnú množinu možností alebo entitu.</span><span class="sxs-lookup"><span data-stu-id="3d20a-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d20a-106">Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení.</span><span class="sxs-lookup"><span data-stu-id="3d20a-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="3d20a-107">Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu.</span><span class="sxs-lookup"><span data-stu-id="3d20a-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="3d20a-108">Potom, čo ste vykonali všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.</span><span class="sxs-lookup"><span data-stu-id="3d20a-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="3d20a-109">Vytvorenie vlastného riešenia pre dimenzie cien</span><span class="sxs-lookup"><span data-stu-id="3d20a-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="3d20a-110">Prejdite do ponuky **Nastavenia** > **Riešenia** a potom vyberte **Nové** , ak chcete vytvoriť nové riešenie.</span><span class="sxs-lookup"><span data-stu-id="3d20a-110">Go to **Settings** > **Solutions** , and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="3d20a-111">Pomenujte riešenie, **dimenzie cien \<your organization name>** , zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-111">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="3d20a-112">Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny</span><span class="sxs-lookup"><span data-stu-id="3d20a-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="3d20a-113">Cenový rozmer môže byť množina možností alebo entita.</span><span class="sxs-lookup"><span data-stu-id="3d20a-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="3d20a-114">Obidva musia byť vytvorené vo vašom cenovom riešení.</span><span class="sxs-lookup"><span data-stu-id="3d20a-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="3d20a-115">Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="3d20a-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="3d20a-116">Dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="3d20a-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="3d20a-117">Prejdite do ponuky **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-117">Go to **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="3d20a-118">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="3d20a-119">Vyberte **Nové** , ak chcete vytvoriť novú entitu s názvom **Štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="3d20a-120">Zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="3d20a-121">Dimenzie založené na množine možností</span><span class="sxs-lookup"><span data-stu-id="3d20a-121">Option set-based dimensions</span></span> 
<span data-ttu-id="3d20a-122">Môžete vytvoriť dve dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="3d20a-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="3d20a-123">Použite **miesto pracovného prostriedku** na sledovanie ceny na **domácom** mieste práce a **na mieste** práce a používania **zdrojových pracovných hodín** s hodnotami **pravidelný** a **nadčasy** ak chcete použiť značku pri dokončení práce.</span><span class="sxs-lookup"><span data-stu-id="3d20a-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="3d20a-124">Prejdite do ponuky **Nastavenia** > **Riešenia** a dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-124">Go to **Settings** > **Solutions** , and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3d20a-125">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Množina možností**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="3d20a-126">Vyberte **Nové** , ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="3d20a-127">Vytvorenie údajov pre dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="3d20a-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="3d20a-128">Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov.</span><span class="sxs-lookup"><span data-stu-id="3d20a-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="3d20a-129">Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="3d20a-130">Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.</span><span class="sxs-lookup"><span data-stu-id="3d20a-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="3d20a-131">Vyberte **Rozšírené vyhľadávanie** , vyberte entitu **Štandardný názov** a potom vyberte **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-131">Select **Advanced Find** , select the entity **Standard Title** , and then select **Results**.</span></span> <span data-ttu-id="3d20a-132">Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.</span><span class="sxs-lookup"><span data-stu-id="3d20a-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="3d20a-133">Vyberte **Nový** , v poli **Názov** zadajte „Systémový inžinier“ a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-133">Select **New** , and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="3d20a-134">Zatvorí formulár.</span><span class="sxs-lookup"><span data-stu-id="3d20a-134">Close the form.</span></span> 
4. <span data-ttu-id="3d20a-135">Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".</span><span class="sxs-lookup"><span data-stu-id="3d20a-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="3d20a-136">Pridajte všetky požadované entity a súvisiace súčasti do riešenia Dimenzia ceny</span><span class="sxs-lookup"><span data-stu-id="3d20a-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="3d20a-137">Budete musieť pridať nasledujúce entity do vášho cenového riešenia.</span><span class="sxs-lookup"><span data-stu-id="3d20a-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="3d20a-138">Postupujte podľa krokov v tomto postupe, tak aby sa niektoré dôležité zmeny schémy v cenovom riešení tak, že entity sa dozvedia o nových cenových dimenziách.</span><span class="sxs-lookup"><span data-stu-id="3d20a-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="3d20a-139">Vyberte **Nastavenia** > **Riešenia** a dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-139">Select **Settings** > **Solutions** , and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="3d20a-140">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Pridať existujúce** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="3d20a-141">V dialógovom okne **súčasti riešenia** vyberte nasledujúce entity:</span><span class="sxs-lookup"><span data-stu-id="3d20a-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="3d20a-142">Skutočná hodnota</span><span class="sxs-lookup"><span data-stu-id="3d20a-142">Actual</span></span>
  - <span data-ttu-id="3d20a-143">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="3d20a-143">Bookable Resource</span></span>
  - <span data-ttu-id="3d20a-144">Riadok odhadu</span><span class="sxs-lookup"><span data-stu-id="3d20a-144">Estimate Line</span></span>
  - <span data-ttu-id="3d20a-145">Podrobnosti o riadku faktúry</span><span class="sxs-lookup"><span data-stu-id="3d20a-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="3d20a-146">Záznam v účtovnom denníku</span><span class="sxs-lookup"><span data-stu-id="3d20a-146">Journal Line</span></span>
  - <span data-ttu-id="3d20a-147">Podrobnosti o riadku projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="3d20a-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="3d20a-148">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="3d20a-148">Project Team Member</span></span>
  - <span data-ttu-id="3d20a-149">Podrobnosti o riadku cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="3d20a-149">Quote Line Detail</span></span>
  - <span data-ttu-id="3d20a-150">Prirážka k cene roly</span><span class="sxs-lookup"><span data-stu-id="3d20a-150">Role Price Markup</span></span>
  - <span data-ttu-id="3d20a-151">Cena roly</span><span class="sxs-lookup"><span data-stu-id="3d20a-151">Role Price</span></span> 
  - <span data-ttu-id="3d20a-152">Zadanie času</span><span class="sxs-lookup"><span data-stu-id="3d20a-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="3d20a-153">Nezabudnite zahrnúť všetky formuláre a zobrazenia pre každú vybranú entitu.</span><span class="sxs-lookup"><span data-stu-id="3d20a-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="3d20a-154">Keď sa zobrazí výzva na zahrnutie všetkých závislých entít pre entity vybraté vyššie, vyberte **Nie**.</span><span class="sxs-lookup"><span data-stu-id="3d20a-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

