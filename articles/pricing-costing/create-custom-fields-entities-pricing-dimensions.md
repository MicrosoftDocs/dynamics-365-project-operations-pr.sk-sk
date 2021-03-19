---
title: Vytvorenie vlastných polí a entít ako cenových dimenzií
description: Táto téma poskytuje informácie o tom, ako vytvoriť vlastné množiny možností alebo entity.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275647"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="8d82c-103">Vytvorenie vlastných polí a entít ako cenových dimenzií</span><span class="sxs-lookup"><span data-stu-id="8d82c-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="8d82c-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="8d82c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8d82c-105">Vykonajte nasledujúce kroky vždy, keď chcete vytvoriť vlastnú množinu možností alebo entitu, ktorú budete používať ako cenovú dimenziu.</span><span class="sxs-lookup"><span data-stu-id="8d82c-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="8d82c-106">Ďalšie informácie sa dozviete v článku [Prehľad cenových dimenzií](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="8d82c-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="8d82c-107">Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení.</span><span class="sxs-lookup"><span data-stu-id="8d82c-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="8d82c-108">Tento dôležitý najlepší postup poskytuje v budúcnosti flexibilitu pri aktualizácii alebo odstraňovaní zmien podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="8d82c-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="8d82c-109">To tiež pomôže pri opätovnom použití vašej práce a uľahčí prenos týchto zmien do inej inštancie. Po vykonaní všetkých požadovaných zmien exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií, aby ste mohli znova použiť nastavenie cien.</span><span class="sxs-lookup"><span data-stu-id="8d82c-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="8d82c-110">Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny</span><span class="sxs-lookup"><span data-stu-id="8d82c-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="8d82c-111">Cenový rozmer môže byť množina možností alebo entita.</span><span class="sxs-lookup"><span data-stu-id="8d82c-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="8d82c-112">Obidva musia byť vytvorené vo vašom cenovom riešení.</span><span class="sxs-lookup"><span data-stu-id="8d82c-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="8d82c-113">Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="8d82c-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="8d82c-114">Dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="8d82c-114">Entity-based dimensions</span></span>
<span data-ttu-id="8d82c-115">Ak chcete vytvoriť dimenzie založené na entitách, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="8d82c-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="8d82c-116">Prejdite do ponuky **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="8d82c-117">V prehľadávači riešení, na ľavom navigačnom paneli, vyberte **Entity**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="8d82c-118">Vyberte **Nové**, ak chcete vytvoriť novú entitu s názvom **Štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="8d82c-119">Zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Definícia entity so Štandardným nadpisom](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="8d82c-121">Dimenzie založené na množine možností</span><span class="sxs-lookup"><span data-stu-id="8d82c-121">Option set-based dimensions</span></span> 
<span data-ttu-id="8d82c-122">Môžete vytvoriť dve dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="8d82c-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="8d82c-123">Použite **Miesto pracovného zdroja** na sledovanie ceny miesta práce **Doma** a práce **Na mieste**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="8d82c-124">Použite **Pracovná doba zdrojov** s hodnotami **Pravidelná** a **Nadčasy** na aplikovanie prirážky, keď je práca dokončená.</span><span class="sxs-lookup"><span data-stu-id="8d82c-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="8d82c-125">Nasledujúca grafika poskytuje pohľad na dimenziu **Miesto pracovného zdroja**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Množina možností na základe cenovej dimenzie nazvanej pracovná poloha zdroja](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="8d82c-127">Nasledujúca grafika poskytuje pohľad na dimenziu **Pracovná doba zdroja**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Množina možností na základe cenovej dimenzie nazvanej hodinová poloha zdroja](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="8d82c-129">Prejdite do ponuky **Nastavenia** > **Riešenia** a dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="8d82c-130">V prehľadávači riešení, na ľavom navigačnom paneli, vyberte **Množinu možností**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="8d82c-131">Vyberte **Nové**, ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="8d82c-132">Vytvorenie údajov pre dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="8d82c-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="8d82c-133">Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov.</span><span class="sxs-lookup"><span data-stu-id="8d82c-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="8d82c-134">Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="8d82c-135">Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.</span><span class="sxs-lookup"><span data-stu-id="8d82c-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="8d82c-136">Vyberte **Rozšírené vyhľadávanie**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="8d82c-137">Vyberte entitu **Štandardný nadpis** a potom vyberte **Výsledky**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="8d82c-138">Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.</span><span class="sxs-lookup"><span data-stu-id="8d82c-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="8d82c-139">Vyberte **Nový**, v poli **Názov** zadajte „Systémový inžinier“ a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="8d82c-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="8d82c-140">Zatvorí stránku.</span><span class="sxs-lookup"><span data-stu-id="8d82c-140">Close the page.</span></span> 
5. <span data-ttu-id="8d82c-141">Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".</span><span class="sxs-lookup"><span data-stu-id="8d82c-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Vzorové údaje pre entitu Štandardný nadpis](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]