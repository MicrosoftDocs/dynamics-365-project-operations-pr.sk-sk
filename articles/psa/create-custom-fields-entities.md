---
title: Vytvorte vlastné polia a entity
description: Táto téma vysvetľuje, ako vytvoriť množiny možností a entity vo vlastnom riešení v platforme Power Apps.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3d838bde8a3d7cbc15e06fb3289924468c284a8a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998970"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="b13da-103">Vytvorte vlastné polia a entity</span><span class="sxs-lookup"><span data-stu-id="b13da-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="b13da-104">Dokončite nasledujúce kroky kedykoľvek, kedy chcete vytvoriť vlastnú množinu možností alebo entitu na Power Apps platforme.</span><span class="sxs-lookup"><span data-stu-id="b13da-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="b13da-105">Postupy v tejto téme by mali byť dokončené pomocou webového rozhrania Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="b13da-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b13da-106">Odporúčame, aby ste robili všetky zmeny cenových dimenzií v samostatnom riešení.</span><span class="sxs-lookup"><span data-stu-id="b13da-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b13da-107">Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu.</span><span class="sxs-lookup"><span data-stu-id="b13da-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b13da-108">Potom, čo ste vykonali všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.</span><span class="sxs-lookup"><span data-stu-id="b13da-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b13da-109">Vytvorte vlastné polia a množiny možností v riešení dimenzie ceny</span><span class="sxs-lookup"><span data-stu-id="b13da-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b13da-110">Cenový rozmer môže byť množina možností alebo entita.</span><span class="sxs-lookup"><span data-stu-id="b13da-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b13da-111">Obidva musia byť vytvorené vo vašom cenovom riešení.</span><span class="sxs-lookup"><span data-stu-id="b13da-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b13da-112">Postup v tomto procese vysvetľuje, ako vytvoriť dimenzie založené na entite a dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="b13da-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b13da-113">Dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="b13da-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="b13da-114">V PSA kliknite na položku **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="b13da-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b13da-115">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **entity**.</span><span class="sxs-lookup"><span data-stu-id="b13da-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b13da-116">Kliknite na **nové**, ak chcete vytvoriť novú entitu s názvom **štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="b13da-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="b13da-117">Zadajte zostávajúce požadované informácie a kliknite na **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="b13da-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Definícia entity so Štandardným nadpisom](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="b13da-119">Dimenzie založené na množine možností</span><span class="sxs-lookup"><span data-stu-id="b13da-119">Option set-based dimensions</span></span> 
<span data-ttu-id="b13da-120">Môžete vytvoriť dve dimenzie založené na množine možností.</span><span class="sxs-lookup"><span data-stu-id="b13da-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="b13da-121">Použite **miesto pracovného prostriedku** na sledovanie ceny na **domácom** mieste práce a **na mieste** práce a používania **zdrojových pracovných hodín** s hodnotami **pravidelný** a **nadčasy** ak chcete použiť značku pri dokončení práce.</span><span class="sxs-lookup"><span data-stu-id="b13da-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="b13da-122">V PSA kliknite na položku **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="b13da-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b13da-123">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Množina možností**.</span><span class="sxs-lookup"><span data-stu-id="b13da-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b13da-124">Kliknite na **nové**, ak chcete vytvoriť novú množinu možností, zadajte zostávajúce požadované informácie a potom kliknite na **uložiť**.</span><span class="sxs-lookup"><span data-stu-id="b13da-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="b13da-125">Množina možností na základe cenovej dimenzie nazvanej pracovná poloha zdroja</span><span class="sxs-lookup"><span data-stu-id="b13da-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="b13da-126">Množina možností na základe cenovej dimenzie nazvanej hodinová poloha zdroja</span><span class="sxs-lookup"><span data-stu-id="b13da-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b13da-127">Vytvorenie údajov pre dimenzie založené na entite</span><span class="sxs-lookup"><span data-stu-id="b13da-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b13da-128">Údaje pre dimenzie založené na entite môžete vytvoriť manuálne alebo pomocou Microsoft Excel importu alebo služobných hovorov.</span><span class="sxs-lookup"><span data-stu-id="b13da-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b13da-129">Použite kroky v tomto postupe na vytvorenie dvoch štandardných titulov, **systémový inžinier** a **starší systémový inžinier** z dimenzie založenej na entite, **štandardný nadpis**.</span><span class="sxs-lookup"><span data-stu-id="b13da-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b13da-130">Ak sú údaje, ktoré chcete vytvoriť, malé, ako je to v nasledovnom príklade, môžete použiť štandardný formulár.</span><span class="sxs-lookup"><span data-stu-id="b13da-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b13da-131">V PSA kliknite na **Rozšírené vyhľadávanie**.</span><span class="sxs-lookup"><span data-stu-id="b13da-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="b13da-132">Vyberte entitu **štandardný nadpis** a potom kliknite na **výsledky**.</span><span class="sxs-lookup"><span data-stu-id="b13da-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="b13da-133">Zobrazia sa všetky riadky v entite **štandardnej** nadpisu.</span><span class="sxs-lookup"><span data-stu-id="b13da-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="b13da-134">Kliknite na položku **Nový**.</span><span class="sxs-lookup"><span data-stu-id="b13da-134">Click **New**.</span></span> <span data-ttu-id="b13da-135">V poli **Názov** zadajte text " Systémový inžinier" a potom kliknite na tlačidlo **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="b13da-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="b13da-136">Zavrite formulár.</span><span class="sxs-lookup"><span data-stu-id="b13da-136">Close the form.</span></span> 
4. <span data-ttu-id="b13da-137">Opakujte kroky 1 - 3 na vytvorenie ďalšieho štandardného názvu pre "Starší Systémový inžinier".</span><span class="sxs-lookup"><span data-stu-id="b13da-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="b13da-138">Vzorové údaje pre štandardný nadpis entity.</span><span class="sxs-lookup"><span data-stu-id="b13da-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]