---
title: Vytvorte rezerváciu projektu z tabule plánovania
description: Táto téma poskytuje informácie o tom, ako vytvoriť projektovú rezerváciu z tabule plánovania.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286132"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="e8d9f-103">Vytvorte rezerváciu projektu z tabule plánovania</span><span class="sxs-lookup"><span data-stu-id="e8d9f-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e8d9f-104">Môžete si rezervovať zdroj na projekte buď priamo na karte **tím**, alebo vytvorením požiadavky zdroja pri všeobecnom priradení člena tímu a následnom vyplnení vygenerovaných požiadaviek použitím člena tímu projektu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="e8d9f-105">Môžete si rezervovať prostriedok do projektu priamo z plánovacej tabule.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="e8d9f-106">Existujú tri spôsoby, ako sa s tým vysporiadať:</span><span class="sxs-lookup"><span data-stu-id="e8d9f-106">There are three ways to do this:</span></span>

- <span data-ttu-id="e8d9f-107">**Rezervujte požiadavku z vygenerovaného zdroja:** po vytvorení všeobecného prostriedku môžete vygenerovať požiadavku na zdroj a priradiť úlohy v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="e8d9f-108">**Rezervácia z primárnej požiadavky:** primárne požiadavky sa zobrazia na tabuli plánovania na karte **projekt**.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="e8d9f-109">**Rezervácia z požiadavky nového zdroja:** môžete vytvoriť požiadavku na zdroj od nuly a priradiť ho k projektu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="e8d9f-110">Na tabule plánovania sa tieto požiadavky zdrojov zobrazia v karte **Otvorené požiadavky**.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="e8d9f-111">Zarezervujte prostredníctvom vygenerovanej požiadavky zdroja.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="e8d9f-112">Môžete vytvoriť všeobecný zdroj a priradiť mu úlohu alebo viacero úloh v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="e8d9f-113">Potom vygenerujete požiadavku zdroja zo všeobecného člena tímu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="e8d9f-114">Na tabuli plánovania sa tento zdroj objaví na karte **otvorené požiadavky**. Možno bude potrebné použiť filtre stĺpcov na mriežke v prípade, že máte priveľa otvorených požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="e8d9f-115">![Otvorenie karty Požiadavky na tabuli plánovania](media/FAQ-Project-Booking-Schedule-Board-1.png "Snímka obrazovky rezervácií a tabuľka priradenia")</span><span class="sxs-lookup"><span data-stu-id="e8d9f-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e8d9f-116">Vyberte si požiadavku.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-116">Select the requirement.</span></span> <span data-ttu-id="e8d9f-117">Karta **Hľadať dostupnosť** sa zobrazí v hornej časti vybraného riadka.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="e8d9f-118">Výberom karty dôjde k spusteniu režimu asistenta plánovania tabule plánovania a k odfiltrovaniu dostupných zdrojov, ktoré spĺňajú požiadavky zdroja.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="e8d9f-119">Po tomto si môžete rezervovať zdroj.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="e8d9f-120">Vybratý riadok môžete tiež presunúť zo spodnej časti tabule plánovania k bunke zdroja v mriežke.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="e8d9f-121">Po rozbalení sa vpravo otvorí panel **Vytvoriť rezerváciu zdroja**.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="e8d9f-122">Stlačením možnosti **Rezervovať** sa zdroj zarezervuje do tímu projektu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-122">Selecting **Book** books the resource onto the project team.</span></span>

![Vytvorte panel rezervácie zdroja](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="e8d9f-124">Rezervácia zo základnej požiadavky</span><span class="sxs-lookup"><span data-stu-id="e8d9f-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="e8d9f-125">Vytvorením projektu v Project Service sa automaticky vytvorí požiadavky na zdroj s názvom Hlavná požiadavka.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="e8d9f-126">Ide o prázdnu požiadavku, ktorá sa používa na rýchlu rezerváciu zdroja pomocou tabule plánovania bez toho, aby sa vygenerovala požiadavka alebo sa vytvárala od nuly.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="e8d9f-127">Pretože je požiadavka prázdna, budete musieť zadať dátumy spolu so spôsobom pridelenia a hodín, ak sú uplatniteľné.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="e8d9f-128">Na rezerváciu zdroja prostredníctvom hlavnej požiadavky stlačte na tabuli plánovania kartu **Projekt**. Možno bude potrebné použiť filter stĺpcov na stĺpci **Projekt** v prípade, že máte priveľa projektov.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="e8d9f-129">![Filtrovanie stĺpcov na tabuli plánovania](media/FAQ-Project-Booking-Schedule-Board-2.png "Snímka obrazovky rezervácií a tabuľka priradenia")</span><span class="sxs-lookup"><span data-stu-id="e8d9f-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="e8d9f-130">Vyberte požiadavku, ktorá má názov projektu ako názov a trvanie má nul (0).</span><span class="sxs-lookup"><span data-stu-id="e8d9f-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="e8d9f-131">Zvoľte kartu **Hľadať dostupnosť**, ktorá sa objaví na riadku.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="e8d9f-132">Týmto sa tabuľa plánovania spustí do režimu asistenta plánovania a zobrazia sa dostupné zdroje, ktoré možno zarezervovať do projektu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="e8d9f-133">Pretože **hlavná požiadavka** predstavuje prázdnu požiadavku s trvaním nula (0), budete musieť nastaviť trvanie na paneli **Vytvoriť rezerváciu zdroja** pri výbere a rezervácii zdroja.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="e8d9f-134">Môžete si tiež vybrať **primárnu požiadavku projektu** v spodnej časti tabule plánovania a presunúť ju na zdroj, čím sa zarezervuje.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="e8d9f-135">Pretože **hlavná požiadavka** predstavuje prázdnu požiadavku s trvaním nula (0), budete musieť nastaviť trvanie na paneli **Vytvoriť rezerváciu zdroja** pri výbere a rezervácii zdroja.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="e8d9f-136">Keď si zarezervujete zdroj cez **hlavnú požiadavku** na paneli plánovania, pridáte ju k tímu projektu bez akéhokoľvek priradenia.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="e8d9f-137">Rezervácia z novej požiadavky zdroja</span><span class="sxs-lookup"><span data-stu-id="e8d9f-137">Book from a new resource requirement</span></span>
<span data-ttu-id="e8d9f-138">Ak chcete rezervovať z novej požiadavky zdroja, postupujte podľa nasledujúcich krokov.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="e8d9f-139">Prejdite na **Požiadavky na zdroje** a zvoľte možnosť **Nová**, čím vytvoríte novú požiadavku na zdroje.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="e8d9f-140">Na karte **projekt**, vyberte projekt na priradenie požiadavky k projektu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="e8d9f-141">Táto novovytvorená požiadavka sa zobrazí ako **otvorená požiadavka** na tabuli plánovania, kde ju možno vyplniť.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="e8d9f-142">Rezervujte zdroj na jeho pridanie k projektovému tímu.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="e8d9f-143">Teraz keď je zdroj zarezervovaný, musíte manuálne priradiť úlohy.</span><span class="sxs-lookup"><span data-stu-id="e8d9f-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]