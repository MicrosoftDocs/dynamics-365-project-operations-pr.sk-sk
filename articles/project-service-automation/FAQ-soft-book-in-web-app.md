---
title: Ako môžem predbežne zarezervovať zdroje vo verzii aplikácie 2.x?
description: Tento článok popisuje ako predbežne zarezervovať členov tímu projektu pomocou Project Service.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: Applies to Project Service version 2.x
ms.technology: ''
ms.assetid: 27063de4-cb0c-436f-970e-c87ebcab92db
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: aad119c0907cdd31220a0d73e6e7d99ee63e2e13
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755596"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="d8016-103">Ako môžem predbežne zarezervovať zdroje vo webovej aplikácii (aplikácia Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="d8016-103">How do I "soft book" resources in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d8016-104">Predbežne môžete naplánovať alebo predbežne zarezervovať zdroj do tímu projektu, aby sa zobrazil váš plán priradenia zdroju k projektu.</span><span class="sxs-lookup"><span data-stu-id="d8016-104">You can tentatively schedule or "soft book" a resource onto a project team to show you plan to assign the resource to a project.</span></span> <span data-ttu-id="d8016-105">Predbežné rezervácie nespotrebúvajú dostupnú kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="d8016-105">Soft bookings don’t consume a resource’s available capacity.</span></span> <span data-ttu-id="d8016-106">Členovia tímu, ktorí sú predbežne rezervovaní, nemôžu byť priradení k úlohám projektu.</span><span class="sxs-lookup"><span data-stu-id="d8016-106">Soft-booked team members can’t be assigned to project tasks.</span></span> <span data-ttu-id="d8016-107">K úlohám možno priradiť iba zdroje so stavom Pevne rezervované a typom potvrdenia Potvrdené (za predpokladu, že majú dostatok hodín pevnej rezervácie, ktoré pokryjú snahu priradenia).</span><span class="sxs-lookup"><span data-stu-id="d8016-107">Only resources with the Status Hard Booked and Commit Type Committed can be assigned to tasks (assuming they have enough hard booking hours to cover the assignment effort).</span></span>

<span data-ttu-id="d8016-108">Členovia tímu projektu s predbežnou rezerváciou sa zobrazia v mriežke člena tímu s predbežne zarezervovanými hodinami zobrazenými v stĺpci Predbežne rezervovať</span><span class="sxs-lookup"><span data-stu-id="d8016-108">Soft-booked project team members show up in the Team Member grid with their soft-booked hours shown in the Soft Book column.</span></span> <span data-ttu-id="d8016-109">Zobrazia sa tiež na tabuli plánu.</span><span class="sxs-lookup"><span data-stu-id="d8016-109">They also show up on the schedule board.</span></span> <span data-ttu-id="d8016-110">Znova nesignalizujú žiadnu spotrebu kapacity, pretože predbežná rezervácia nespotrebúva kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="d8016-110">Again, they don’t indicate any consumption of capacity as soft-booking doesn’t consume capacity of a resource.</span></span>

<span data-ttu-id="d8016-111">Existujú tri spôsoby predbežnej rezervácie člena tímu k projektu pomocou Project Service verzie 2.x.</span><span class="sxs-lookup"><span data-stu-id="d8016-111">There are three ways to soft-book a team member onto a project with Project Service version 2.x.</span></span> <span data-ttu-id="d8016-112">Môžete vykonať predbežnú rezerváciu s tabuľou plánu, použiť funkciu správy rezervácií alebo vytvoriť všeobecnú rezerváciu.</span><span class="sxs-lookup"><span data-stu-id="d8016-112">You can soft-book with the schedule board, use the Maintain Bookings feature, or by creating a generic resource.</span></span> <span data-ttu-id="d8016-113">Tieto metódy sú popísané nižšie.</span><span class="sxs-lookup"><span data-stu-id="d8016-113">These methods are described below.</span></span>

## <a name="soft-book-with-the-schedule-board"></a><span data-ttu-id="d8016-114">Predbežná rezervácia použitím tabule plánovania</span><span class="sxs-lookup"><span data-stu-id="d8016-114">Soft-book with the schedule board</span></span>

<span data-ttu-id="d8016-115">Na predbežnú rezerváciu pomocou tabule plánovania postupujte nasledovne:</span><span class="sxs-lookup"><span data-stu-id="d8016-115">To soft-book with the schedule board, follow this procedure:</span></span> 
1. <span data-ttu-id="d8016-116">Otvorte tabuľu plánovania.</span><span class="sxs-lookup"><span data-stu-id="d8016-116">Open the schedule board.</span></span>
2. <span data-ttu-id="d8016-117">Zvoľte si kartu Projekt v spodnej časti panela Požiadavky na rezervácie tabule plánovania.</span><span class="sxs-lookup"><span data-stu-id="d8016-117">Select the Project tab on the bottom Booking Requirements panel of the schedule board.</span></span>
3. <span data-ttu-id="d8016-118">Vyhľadajte si projekt, ku ktorému chcete predbežne zarezervovať zdroj.</span><span class="sxs-lookup"><span data-stu-id="d8016-118">Find the project you wish to soft-book a resource on.</span></span> <span data-ttu-id="d8016-119">Ak máte veľa projektov, kliknite na hlavičku stĺpca projekt a potom použite filter na vyhľadanie projektu.</span><span class="sxs-lookup"><span data-stu-id="d8016-119">If you have many projects, click on the Project column header and then use the filter to find your project.</span></span>
4. <span data-ttu-id="d8016-120">Kliknite na projekt a potom potiahnite a pustite ho na časovú os zdroja.</span><span class="sxs-lookup"><span data-stu-id="d8016-120">Click on the project, then drag and drop it on the resource’s time grid.</span></span>
5. <span data-ttu-id="d8016-121">Tým sa vpravo otvorí panel vytvorenia zdroja rezervácie.</span><span class="sxs-lookup"><span data-stu-id="d8016-121">This opens the Create Resource Booking panel on the right.</span></span> <span data-ttu-id="d8016-122">Upravte dátum začiatku a ukončenia, zvoľte si stav rezervácie ako predbežná a nastavte hodiny.</span><span class="sxs-lookup"><span data-stu-id="d8016-122">Adjust the start and end date, select the Booking Status as Soft and set the hours.</span></span> 
6. <span data-ttu-id="d8016-123">Kliknite na rezervovať.</span><span class="sxs-lookup"><span data-stu-id="d8016-123">Click Book.</span></span>
7. <span data-ttu-id="d8016-124">Späť v projekte sa zdroj začne zobrazovať ako člen tímu s predbežne zarezervovanými hodinami v stĺpci Predbežná rezervácia.</span><span class="sxs-lookup"><span data-stu-id="d8016-124">Back on the project, the resource will now show as a team member with the soft booked hours in the Soft Book column.</span></span>

<span data-ttu-id="d8016-125">Upozorňujeme, že ich nemožno priraďovať k úlohám v štruktúre rozdelenia práce (WBS), pretože zdroje sa musia na priradenie k tímu zarezervovať pevne.</span><span class="sxs-lookup"><span data-stu-id="d8016-125">Note that you can’t assign them to tasks on the work breakdown structure (WBS) as resources must be hard booked on the team to be assigned.</span></span>

## <a name="soft-book-using-the-maintain-bookings-feature"></a><span data-ttu-id="d8016-126">Predbežná rezervácia použitím funkcie Spravovať rezervácie</span><span class="sxs-lookup"><span data-stu-id="d8016-126">Soft-book using the Maintain Bookings feature</span></span>

<span data-ttu-id="d8016-127">Na predbežnú rezerváciu pomocou funkcie Spravovať rezervácie postupujte nasledovne:</span><span class="sxs-lookup"><span data-stu-id="d8016-127">To soft-book with Maintain Bookings follow this procedure:</span></span>
1. <span data-ttu-id="d8016-128">Na mriežke člena tímu kliknite na tlačidlo Nové.</span><span class="sxs-lookup"><span data-stu-id="d8016-128">From the team member grid, Click New.</span></span>
2. <span data-ttu-id="d8016-129">Zvoľte si rezervovateľný zdroj, rolu, od/do.</span><span class="sxs-lookup"><span data-stu-id="d8016-129">Select the bookable resource, role, from/to.</span></span>
3. <span data-ttu-id="d8016-130">Vyberte metódu prideľovania inú než Žiadne:</span><span class="sxs-lookup"><span data-stu-id="d8016-130">Select an allocation method other than None:</span></span>
- <span data-ttu-id="d8016-131">Plná kapacita</span><span class="sxs-lookup"><span data-stu-id="d8016-131">Full Capacity</span></span>
- <span data-ttu-id="d8016-132">Kapacita v percentách</span><span class="sxs-lookup"><span data-stu-id="d8016-132">Percentage Capacity</span></span>
- <span data-ttu-id="d8016-133">Podľa rovnomerne rozmiestnených hodín</span><span class="sxs-lookup"><span data-stu-id="d8016-133">By Hours Distribute Evenly</span></span>
- <span data-ttu-id="d8016-134">Podľa hodín počiatočného vyťaženia</span><span class="sxs-lookup"><span data-stu-id="d8016-134">By Hours Front Load</span></span>
4. <span data-ttu-id="d8016-135">Kliknite na tlačidlo Uložiť.</span><span class="sxs-lookup"><span data-stu-id="d8016-135">Click Save.</span></span> <span data-ttu-id="d8016-136">Na mriežke tímu uvidíte zdroj a ich spolu s hodinami, ktorý bude mať označenie Pevný.</span><span class="sxs-lookup"><span data-stu-id="d8016-136">You’ll see the resource on the team grid and their hours indicated as Hard.</span></span>
5. <span data-ttu-id="d8016-137">Spravujte rezerváciu zdrojov kliknutím na možnosť Spravovať rezervácie.</span><span class="sxs-lookup"><span data-stu-id="d8016-137">Maintain the resource’s bookings by clicking Maintain Bookings.</span></span>
6. <span data-ttu-id="d8016-138">Po otvorení tabule plánovania si rozbaľte zdroj, čím si zobrazíte jeho rezervácie.</span><span class="sxs-lookup"><span data-stu-id="d8016-138">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="d8016-139">Stav rezervácie bude Pevná.</span><span class="sxs-lookup"><span data-stu-id="d8016-139">You will see the booking indicated as Hard.</span></span>
7. <span data-ttu-id="d8016-140">Kliknite pravým tlačidlom myši na rezerváciu. V časti Zmena stavu si zvoľte možnosť Predbežná rezervácia a potom Predbežne.</span><span class="sxs-lookup"><span data-stu-id="d8016-140">Right-click the booking, under Change Status, select Soft Book and then Soft.</span></span> <span data-ttu-id="d8016-141">Stav rezervácie bude Predbežne.</span><span class="sxs-lookup"><span data-stu-id="d8016-141">The booking status is now Soft.</span></span>
8. <span data-ttu-id="d8016-142">Po zatvorení tabule plánu uvidíte, že hodiny zdroja sa zmenili z Pevné na Predbežne na mriežke člena tímu.</span><span class="sxs-lookup"><span data-stu-id="d8016-142">After closing the schedule board, you’ll see that the hours for the resource have changed from Hard to Soft on the team member grid.</span></span>
<span data-ttu-id="d8016-143">Upozorňujeme, že ak pevne zarezervujete zdroj do tímu a následne im priradíte úlohy vo WBS, potom použijete správu rezervácií na zmenu stavu z Pevné na Predbežné. Odstráni sa priradenie z úloh daného zdroja, pretože iba pevne rezervované zdroje možno priradiť k úlohám.</span><span class="sxs-lookup"><span data-stu-id="d8016-143">Note that if you hard book a resource onto the team and then assign them tasks in the WBS, when you use maintain bookings to change the status of Hard to Soft, it will remove the assignments from the tasks for that resource, as only hard booked resources can be assigned to tasks.</span></span>

## <a name="soft-book-by-creating-a-generic-resource"></a><span data-ttu-id="d8016-144">Predbežná rezervácia všeobecného zdroja</span><span class="sxs-lookup"><span data-stu-id="d8016-144">Soft-book by creating a generic resource</span></span>

<span data-ttu-id="d8016-145">Predbežnú rezerváciu možno vytvoriť vytvorením všeobecného zdroja člena tímu, vyplnením pomocou tabule plánovania alebo požiadavky na zdroj a zmenou typu počas rezervácie.</span><span class="sxs-lookup"><span data-stu-id="d8016-145">You can create a soft-booking by generating a generic resource team member, fulfilling with schedule board or Resource Request and changing the type during the booking.</span></span>
<span data-ttu-id="d8016-146">Urobte tak nasledovným postupom:</span><span class="sxs-lookup"><span data-stu-id="d8016-146">To do this, use the following procedure:</span></span>

1. <span data-ttu-id="d8016-147">Na projekte WBS priraďte roly k úlohám, pre ktoré chcete vygenerovať všeobecných členov tímu.</span><span class="sxs-lookup"><span data-stu-id="d8016-147">On the project WBS, assign roles to the tasks you wish to generate generic team members for.</span></span>
2. <span data-ttu-id="d8016-148">Kliknite na možnosť Generovať projektový tím.</span><span class="sxs-lookup"><span data-stu-id="d8016-148">Click Generate Project Team.</span></span>
3. <span data-ttu-id="d8016-149">Na mriežke členov projektového tímu si vyberte všeobecný zdroj a kliknite na možnosť Rezervovať.</span><span class="sxs-lookup"><span data-stu-id="d8016-149">On the project team member grid, select the generic resource and click Book.</span></span>
4. <span data-ttu-id="d8016-150">Na tabuli plánovania si zvoľte zdroj, ktorý si chcete zarezervovať.</span><span class="sxs-lookup"><span data-stu-id="d8016-150">On the schedule board, select the resource that you wish to book.</span></span>
5. <span data-ttu-id="d8016-151">Na paneli tabule plánovania Vytvoriť rezerváciu zdroja zmeňte stav rezervácie na Predbežná.</span><span class="sxs-lookup"><span data-stu-id="d8016-151">On the schedule board’s Create Resource Booking panel, change the Booking Status to Soft.</span></span>
6. <span data-ttu-id="d8016-152">Kliknite na možnosť Rezervovať alebo Rezervovať a ukončiť.</span><span class="sxs-lookup"><span data-stu-id="d8016-152">Click Book or Book and Exit.</span></span>

<span data-ttu-id="d8016-153">Po zatvorení panelu plánovania sa vám zobrazí vybratý zdroj pridaný k tímu s predbežne zarezervovanými hodinami spolu s priradenými hodinami.</span><span class="sxs-lookup"><span data-stu-id="d8016-153">After closing the schedule board, you’ll see the selected resource added to the team with Soft booked hours as well as assigned hours.</span></span> <span data-ttu-id="d8016-154">Uvidíte tiež, že všeobecný prostriedok zostáva v tíme ako indikátor priradené úlohy jednotlivým predbežne zarezervovaným členom tímu.</span><span class="sxs-lookup"><span data-stu-id="d8016-154">You’ll also see that the generic resource remains on the team as an indicator that the tasks are assigned to a soft-booked team member.</span></span>

<span data-ttu-id="d8016-155">Keď budete pripravený na zmenu predbežne rezervovaného zdroja člena tímu na pevne rezervovaného člena tímu, aby ste ich mohli priradiť k úlohám, postupujte nasledovne:</span><span class="sxs-lookup"><span data-stu-id="d8016-155">When you’re ready to change a soft-booked team member resource to a hard-booked team member so that you can assign them to tasks, do the following:</span></span>

1. <span data-ttu-id="d8016-156">Označte zdroj a kliknite na možnosť Spravovať rezervácie.</span><span class="sxs-lookup"><span data-stu-id="d8016-156">Select that resource and click Maintain Bookings.</span></span>
2. <span data-ttu-id="d8016-157">Po otvorení tabule plánovania si rozbaľte zdroj, čím si zobrazíte jeho rezervácie.</span><span class="sxs-lookup"><span data-stu-id="d8016-157">When the schedule board opens, expand the resource to show their bookings.</span></span> <span data-ttu-id="d8016-158">Zobrazí sa vám rezervácia označená ako Predbežná.</span><span class="sxs-lookup"><span data-stu-id="d8016-158">You’ll see the booking marked as Soft.</span></span>
3. <span data-ttu-id="d8016-159">Kliknite pravým tlačidlom myši na rezerváciu. V časti Zmena stavu si zvoľte možnosť Pevná rezervácia a potom Pevná.</span><span class="sxs-lookup"><span data-stu-id="d8016-159">Right-click the booking, under Change Status, select Hard Book and then Hard.</span></span> <span data-ttu-id="d8016-160">Stav rezervácie bude Pevná.</span><span class="sxs-lookup"><span data-stu-id="d8016-160">The booking status is now Hard.</span></span>
4. <span data-ttu-id="d8016-161">Po zatvorení tabule plánu uvidíte, že hodiny zdroja sa zmenili z Predbežné na Pevné na mriežke člena tímu.</span><span class="sxs-lookup"><span data-stu-id="d8016-161">After closing the schedule board, you’ll see that the hours for the resource have changed from Soft to Hard on the team member grid.</span></span> <span data-ttu-id="d8016-162">Odteraz možno priraďovať zdroj k úlohám (za predpokladu, že je rovnováha medzi pevne zarezervovanými hodinami a hodinami úsilia pre priradenie).</span><span class="sxs-lookup"><span data-stu-id="d8016-162">You may now assign the resource to tasks (provided there is alignment between the hard-booked hours and the effort hours of the task for assignment).</span></span> <span data-ttu-id="d8016-163">Upozorňujeme, že v prípade dodržania krokov vypĺňania všeobecného zdroja v položke 3, pri zmene stavu predbežne rezervovaného rezervovateľného zdroja na pevný, sa z tímu odstráni všeobecný člen tímu.</span><span class="sxs-lookup"><span data-stu-id="d8016-163">Note that if you followed the generic resource fulfilment steps in item #3 above, when you change the status of the soft-booked bookable resource to hard, the generic team member is removed from the team.</span></span>
