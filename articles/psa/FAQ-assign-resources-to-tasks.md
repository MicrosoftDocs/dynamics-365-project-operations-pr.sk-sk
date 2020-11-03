---
title: Priraďte zdroj k úlohe
description: Táto téma poskytuje informácie o tom, ako priradiť zdroje k úlohám.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084553"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="2d359-103">Priraďte zdroj k úlohe</span><span class="sxs-lookup"><span data-stu-id="2d359-103">Assign a resource to a task</span></span>

<span data-ttu-id="2d359-104">Existujú tri spôsoby, ako priradiť zdroj k úlohe v Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="2d359-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="2d359-105">Rezervujte si zdroj ako člen tímu a potom ho priradiť k úlohe.</span><span class="sxs-lookup"><span data-stu-id="2d359-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="2d359-106">Môžete zdroj priradiť k tímovému projektu a následne ho priradiť k úlohám v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="2d359-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="2d359-107">V karte **člen tímu** pridajte nového člena tímu stlačením možnosti **nový**.</span><span class="sxs-lookup"><span data-stu-id="2d359-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="2d359-108">Otvorí sa panel **rýchleho vytvorenia člena tímu** , kde si môžete zvoliť názov rezervovateľného zdroja a nastaviť mu rolu.</span><span class="sxs-lookup"><span data-stu-id="2d359-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="2d359-109">Vyberte jednu z nasledujúcich metód prideľovania pre rezerváciu zdroja:</span><span class="sxs-lookup"><span data-stu-id="2d359-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="2d359-110">**Plná kapacita** Táto metóda zarezervuje úplnú kapacitu zdroje pre stanovené dátumy od a do.</span><span class="sxs-lookup"><span data-stu-id="2d359-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="2d359-111">**Kapacita v percentách** zarezervuje zdroj pre percento kapacity zdroja pre stanovené dátumy od a do.</span><span class="sxs-lookup"><span data-stu-id="2d359-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="2d359-112">**Podľa rovnomerne rozmiestnených hodín** zarezervuje zdroj pre stanovený počet hodín, ktoré rovnomerne rozdelí na dni v rámci stanovených dátumov od a do.</span><span class="sxs-lookup"><span data-stu-id="2d359-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="2d359-113">**Podľa hodín počiatočného vyťaženia** zarezervuje prostriedok pre stanovený počet hodín, v rámci počiatočného vyťaženia denných hodín v rámci stanovených dátumov od a do.</span><span class="sxs-lookup"><span data-stu-id="2d359-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="2d359-114">Možnosť **Žiadne** zdroj pridá k tímu, no nevytvorí žiadne rezervácie, ktoré by využili kapacity zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="2d359-115">Na mriežke **plánov** pre úlohu, stlačte ikonu **Zdroj** v bunke zdroja a potom pod **členovia tímu** zvoľte člena tímu, ktorého ste práve pridali.</span><span class="sxs-lookup"><span data-stu-id="2d359-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="2d359-116">Na karte **člen tímu** aj na karte **odsúhlasenie** sa zdroj zobrazí spolu so zarezervovanými a pridelenými hodinami.</span><span class="sxs-lookup"><span data-stu-id="2d359-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="2d359-117">Hodiny by mali byť rovnaké, no nie je to požadované, pretože rezervácie a pridelenia nie sú úzko spojené.</span><span class="sxs-lookup"><span data-stu-id="2d359-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="2d359-118">Na karte **odsúhlasenia** nájdete podrobnosti v prípade, že sa budú líšiť. Ide napríklad o prípady, keď priradíte zdroju viac hodín, než ste zarezervovali.</span><span class="sxs-lookup"><span data-stu-id="2d359-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="2d359-119">Ak je to treba, môžete opraviť informácie rozšírením rezervácie zdroja alebo zmenou priradenia.</span><span class="sxs-lookup"><span data-stu-id="2d359-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="2d359-120">Vytvorte všeobecného člena tímu prostredníctvom priradenia úlohy</span><span class="sxs-lookup"><span data-stu-id="2d359-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="2d359-121">Keď vytvoríte všeobecného člena tímu prostredníctvom priradenia úlohy, vytvoríte zástupný alebo všeobecný zdroj, ktorý popisuje vlastnosti pomenovaného zdroja, ktorý chcete aby nakoniec pracoval na úlohách.</span><span class="sxs-lookup"><span data-stu-id="2d359-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="2d359-122">Následne vygenerujte požiadavku (alebo odošlite žiadosť pomocou požiadavky), ktorá sa použije na vyhľadávanie a rezerváciu pomenovaného zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="2d359-123">Na mriežke **plánu** stlačte ikonu **zdroja** v bunke zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="2d359-124">Zadajte názov, ktorý bude slúžiť ako zástupný znak názvu zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="2d359-125">Napríklad, programový manažér</span><span class="sxs-lookup"><span data-stu-id="2d359-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="2d359-126">Vybert **vytvoriť** a v poli **rýchle vytvorenie porjektového člena tímu** , nastavte rolu pre všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="2d359-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="2d359-127">Môžete pokračovať na priradenie úloh k tomuto zástupnému zdroju výberom zdroja v časti **výber zdroja** pre úlohy.</span><span class="sxs-lookup"><span data-stu-id="2d359-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="2d359-128">Sú uvedené pod **členmi tímu**.</span><span class="sxs-lookup"><span data-stu-id="2d359-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="2d359-129">Keď skončíte s priraďovaním všeobecného zdroja, zvoľte si na karte **Tím** všeobecný zdroj a stlačte možnosť **Generovať požiadavku** na vytvorenie požiadavky zdroja pre všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="2d359-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="2d359-130">Pri všeobecnom zdroji stlačte možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="2d359-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="2d359-131">Následne môžete použiť tabuľku plánu na vyhľadanie a rezerváciu skutočného zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="2d359-132">Požiadavku môžete tiež odoslať na vyplnenie manažérovi zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="2d359-133">Pri plnení všeobecného zdroja pomenovaným zdrojom sa všeobecný zdroj odstráni z tímu a priradenia úlohy pre všeobecný zdroj sa priradia k pomenovanému zdroju, ktorý vyplnil požiadavku na zdroj všeobecného zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="2d359-134">Priradenie pomenovaného zdroja zo zoznamu všetkých rezervovateľných zdrojov</span><span class="sxs-lookup"><span data-stu-id="2d359-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="2d359-135">Pole vyhľadávania možno vo **výbere zdroja** použiť na vyhľadanie všetkých rezervovateľných zdrojov a ich priradenie k úlohe.</span><span class="sxs-lookup"><span data-stu-id="2d359-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="2d359-136">Prostriedky pridelené týmto spôsobom sa pridajú do tímu bez akýchkoľvek rezervácií.</span><span class="sxs-lookup"><span data-stu-id="2d359-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="2d359-137">To je podobné ako pridanie člena tímu a výber nič ako spôsob prideľovania.</span><span class="sxs-lookup"><span data-stu-id="2d359-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="2d359-138">Zdroje sa zobrazia na karte **tím** a na karte **odsúhlasenie** ako zdroje s tým, že im bude chýbať priradenie a rezervácia.</span><span class="sxs-lookup"><span data-stu-id="2d359-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="2d359-139">Ak chcete využiť ich dostupnosť, zarezervujte ich.</span><span class="sxs-lookup"><span data-stu-id="2d359-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="2d359-140">Na mriežke **plánu** stlačte ikonu **zdroja** v bunke zdroja.</span><span class="sxs-lookup"><span data-stu-id="2d359-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="2d359-141">Začnite písať názov.</span><span class="sxs-lookup"><span data-stu-id="2d359-141">Start typing a name.</span></span> <span data-ttu-id="2d359-142">Výsledky vyhľadávania pre názov sú zobrazené vo **výbere zdroja** v časti **iné zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2d359-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="2d359-143">V zozname vyberte zdroj, ktorý chcete priradiť k úlohe.</span><span class="sxs-lookup"><span data-stu-id="2d359-143">Select the resource that you want to assign to the task.</span></span>

