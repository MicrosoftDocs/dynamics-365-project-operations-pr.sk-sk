---
title: Ako môžem priradiť rezervovateľný zdroj k úlohe vo webovej aplikácii
description: Prehľad spôsobov, ako môžete priradiť rezervovateľné zdroje.
author: JohnPBurrows
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 2.x on platform version 9.x
ms.assetid: 9db35b39-8dfc-4989-9160-fd841fe0ae5a
ms.author: john.burrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 521ea73c948619816d3cd06d72140fcc85366397
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755682"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="076ff-103">Ako priradiť prostriedok rezervovateľné úlohy vo webovej aplikácii (aplikácia Project Service v2.x)?</span><span class="sxs-lookup"><span data-stu-id="076ff-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="076ff-104">Existujú dva spôsoby, ako priradiť prostriedok k úlohe v Project Service.</span><span class="sxs-lookup"><span data-stu-id="076ff-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="076ff-105">Môžete rezervovať prostriedok ako člen tímu a potom ho priradiť k úlohe.</span><span class="sxs-lookup"><span data-stu-id="076ff-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="076ff-106">Alebo môžete vytvoriť všeobecného člena tímu cez priradenie roly v úlohách, vytvoriť tím a následne splniť požiadavky na personál s pomenovaným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="076ff-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="076ff-107">Upozorňujeme, že v prípade, ak chcete priradiť rezervovateľný zdroj k úlohe, rezervovateľný zdroj člena tímu musí mať dostatočne dostupné rezervácie.</span><span class="sxs-lookup"><span data-stu-id="076ff-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="076ff-108">Stav rezervácie musí predstavovať typ potvrdenie Pevne rezervované a stav musí byť Potvrdené.</span><span class="sxs-lookup"><span data-stu-id="076ff-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="076ff-109">Ak nie je k dispozícii dostatok rezervácií pre zdroj, Project Service odstráni priradenie a zobrazí nasledovné chybové hlásenie:</span><span class="sxs-lookup"><span data-stu-id="076ff-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="076ff-110">*Nie je možné priradiť prostriedok úlohe – nasledujúce zdroje nemajú dostatočný počet hodín zarezervovaný pre projekt*</span><span class="sxs-lookup"><span data-stu-id="076ff-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="076ff-111">Rezervujte si prostriedok ako člen tímu a potom ho priradiť k úlohe.</span><span class="sxs-lookup"><span data-stu-id="076ff-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="076ff-112">S touto metódou pridať prostriedok do projektového tímu a potom priradiť úlohy na prostriedok v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="076ff-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="076ff-113">Tu je, ako to urobiť:</span><span class="sxs-lookup"><span data-stu-id="076ff-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="076ff-114">V mriežke člen tímu pridajte nového člena tímu stlačením možnosti **Nový**.</span><span class="sxs-lookup"><span data-stu-id="076ff-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="076ff-115">Na obrazovke tím členských rýchle vytvorenie vyberte názov rezervovateľné prostriedku a nastaviť úlohu.</span><span class="sxs-lookup"><span data-stu-id="076ff-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="076ff-116">Zvoľte dátumy **Od** a **Do**.</span><span class="sxs-lookup"><span data-stu-id="076ff-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="076ff-117">![Snímka obrazovky pridania člena tímu](media/FAQ-Resources-to-Tasks2-1.png "Snímka obrazovky pridania člena tímu")</span><span class="sxs-lookup"><span data-stu-id="076ff-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="076ff-118">Vyberte jednu z nasledujúcich metód prideľovania pre rezerváciu prostriedku:</span><span class="sxs-lookup"><span data-stu-id="076ff-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="076ff-119">**Plná kapacita** Táto metóda zarezervuje úplnú kapacitu zdroje pre stanovené dátumy od a do.</span><span class="sxs-lookup"><span data-stu-id="076ff-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="076ff-120">**Kapacita v percentách** zarezervuje zdroj pre percento kapacity zdroja pre stanovené dátumy od a do.</span><span class="sxs-lookup"><span data-stu-id="076ff-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="076ff-121">**Podľa rovnomerne rozmiestnených hodín** zarezervuje prostriedok pre stanovený počet hodín, ktoré rovnomerne rozdelí na dni v rámci stanovených dátumov od a do.</span><span class="sxs-lookup"><span data-stu-id="076ff-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="076ff-122">**Podľa hodín počiatočného vyťaženia** zarezervuje prostriedok pre stanovený počet hodín, v rámci počiatočného vyťaženia denných hodín v rámci stanovených dátumov od a do.</span><span class="sxs-lookup"><span data-stu-id="076ff-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="076ff-123">Nestláčajte možnosť **Žiadne**, pretože sa tým zdroj pridá k tímu, no nevytvorí žiadne rezervácie, ktoré by využili kapacity zdroja.</span><span class="sxs-lookup"><span data-stu-id="076ff-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="076ff-124">Vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="076ff-124">Select **Save**.</span></span>

    <span data-ttu-id="076ff-125">Upozorňujeme, že hodiny rezervácie musia byť dostatočné na pokrytie hodín úsilia a rozsahov dátumov úlohy, ku ktorej tento zdroj priraďujete.</span><span class="sxs-lookup"><span data-stu-id="076ff-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="076ff-126">Ak nie sú zosúladené, nemôžete priradiť zdroj k úlohe.</span><span class="sxs-lookup"><span data-stu-id="076ff-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="076ff-127">Na štruktúre rozdelenia práce (WBS) úlohy kliknite na rozbaľovaciu ponuku bunky zdroja.</span><span class="sxs-lookup"><span data-stu-id="076ff-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="076ff-128">Potom:</span><span class="sxs-lookup"><span data-stu-id="076ff-128">Then:</span></span> 

    1. <span data-ttu-id="076ff-129">Stlačte možnosť **Pridať**.</span><span class="sxs-lookup"><span data-stu-id="076ff-129">Select **Add**.</span></span>
    2. <span data-ttu-id="076ff-130">Stlačte rozbaľovaciu ponuku v časti **Zdroje** a potom označte člena tímu, ktorého ste pridali.</span><span class="sxs-lookup"><span data-stu-id="076ff-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="076ff-131">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="076ff-131">Select **OK**.</span></span> <span data-ttu-id="076ff-132">Člen tímu je teraz priradený k úlohe.</span><span class="sxs-lookup"><span data-stu-id="076ff-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="076ff-133">![Snímka obrazovky pridania zdrojov pomocou WBS](media/FAQ-Resources-to-Tasks2-2.png "Snímka obrazovky pridania zdrojov pomocou WBS")</span><span class="sxs-lookup"><span data-stu-id="076ff-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="076ff-134">Na mriežke člena tímu uvidíte súčet priradených hodín zdroja v časti Priradené hodiny.</span><span class="sxs-lookup"><span data-stu-id="076ff-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="076ff-135">Hodnota bude menšia alebo rovná rezervovaným hodinám zdroja.</span><span class="sxs-lookup"><span data-stu-id="076ff-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="076ff-136">![Snímka obrazovky priradených hodín pre zdroj](media/FAQ-Resources-to-Tasks2-3.png "Snímka obrazovky priradených hodín pre zdroj")</span><span class="sxs-lookup"><span data-stu-id="076ff-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="076ff-137">V prípade, že úloha, ktorú sa pokúšate priradiť k zdroju začína po koncovom dátume rezervácie zdroja, zdroj sa v rozbaľovacej ponuke nezobrazí.</span><span class="sxs-lookup"><span data-stu-id="076ff-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="076ff-138">Všimnite si, že môžete priradiť prostriedok na viac hodín, než sú ich rezervované hodiny. Predpokladom je, aby zdroj ešte mal nepriradenú kapacitu.</span><span class="sxs-lookup"><span data-stu-id="076ff-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="076ff-139">V tomto prípade bude zdroj len čiastočne priradený k svojim rezerváciám.</span><span class="sxs-lookup"><span data-stu-id="076ff-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="076ff-140">Zostávajúce nepriradené hodiny úloh si môžete zobraziť pridaním stĺpca Počet hodín bez personálu k štruktúre rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="076ff-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="076ff-141">Ak sú zdroje priradené k ich zarezervovaným hodinám (ich zarezervované hodiny sa rovnajú priradeným hodinám), zobrazí sa vám pri pokuse o priradenie ich budúcich akcií nasledovné chybové hlásenie:</span><span class="sxs-lookup"><span data-stu-id="076ff-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="076ff-142">*Nie je možné priradiť prostriedok úlohe – nasledujúce zdroje nemajú dostatočný počet hodín zarezervovaný pre projekt.*</span><span class="sxs-lookup"><span data-stu-id="076ff-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="076ff-143">Okrem toho predvolený správca členov projektového tímu ktorý sa pridáva do tímu pri vytváraní projektu je pridané bez spomínaného a nemožno priradiť ľubovoľnú úlohu.</span><span class="sxs-lookup"><span data-stu-id="076ff-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="076ff-144">Nezobrazia sa v rozbaľovacej ponuke zdroja pre úlohy.</span><span class="sxs-lookup"><span data-stu-id="076ff-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="076ff-145">Ak chcete priradiť tento zdroj, musíte ich odstrániť z tímu a potom znova pridať metódu prideľovania, ktorá nebude mať príznak Žiadna.</span><span class="sxs-lookup"><span data-stu-id="076ff-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="076ff-146">Dôvod ich pridania do tímu pri vytvorení projektu je ten, že projekt má predvolene aspoň jedného schvaľovateľa projektu.</span><span class="sxs-lookup"><span data-stu-id="076ff-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="076ff-147">Vytvorenie všeobecného člena tímu prostredníctvom priradenia roly k úlohám</span><span class="sxs-lookup"><span data-stu-id="076ff-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="076ff-148">Týmto spôsobom sa zaručí, že zdroje majú dosť rezervácie pre úlohy.</span><span class="sxs-lookup"><span data-stu-id="076ff-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="076ff-149">Najprv vytvorte zástupný symbol alebo všeobecný zdroj, ktorý popisuje vlastnosti pomenovaného zdroja, ktorý chcete nakoniec priradiť k úlohám vytvorením tímu po priradení rol k úlohám.</span><span class="sxs-lookup"><span data-stu-id="076ff-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="076ff-150">Tu je, ako to urobiť:</span><span class="sxs-lookup"><span data-stu-id="076ff-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="076ff-151">Na štruktúre rozdelenia práce označte úlohu.</span><span class="sxs-lookup"><span data-stu-id="076ff-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="076ff-152">V bunke zdroja zvoľte ikonu rozbaľovacej ponuky **Priradená rola**.</span><span class="sxs-lookup"><span data-stu-id="076ff-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="076ff-153">V rozbaľovacej ponuke stlačte možnosť **Rola** a vyberte si rolu pre všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="076ff-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="076ff-154">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="076ff-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="076ff-155">![Snímka obrazovky použitia WBS na pridanie zdroja](media/FAQ-Resources-to-Tasks2-4.png "Snímka obrazovky použitia WBS na pridanie zdroja")</span><span class="sxs-lookup"><span data-stu-id="076ff-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="076ff-156">Po úspešnom dokončení rol priraďovania k úlohám vo WBS zvoľte možnosť **Generovať projektový tím**.</span><span class="sxs-lookup"><span data-stu-id="076ff-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="076ff-157">Služba Project Service vytvorí minimálny počet všeobecných členov tímu na základe rol, zdrojových organizačných jednotiek a kalendára projektu sčítaním priradení úlohy.</span><span class="sxs-lookup"><span data-stu-id="076ff-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="076ff-158">![Snímka obrazovky generovania projektového tímu](media/FAQ-Resources-to-Tasks2-5.png "Snímka obrazovky generovania projektového tímu")</span><span class="sxs-lookup"><span data-stu-id="076ff-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="076ff-159">Na mriežke členov tímu uvidíte zdroje všeobecného zdroja s rolou a názvom pozície.</span><span class="sxs-lookup"><span data-stu-id="076ff-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="076ff-160">Ak sú dva zdroje potrebné pre rolu na dokončenie práce, funkcia všeobecného tímu vytvorí dvoch členov tímu a použije názov pozície, aby ich rozdelil.</span><span class="sxs-lookup"><span data-stu-id="076ff-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="076ff-161">![Snímka obrazovky pridania dvoch všeobecných zdrojov](media/FAQ-Resources-to-Tasks2-6.png "Snímka obrazovky pridania dvoch všeobecných zdrojov")</span><span class="sxs-lookup"><span data-stu-id="076ff-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="076ff-162">Môžete si otvoriť záložné požiadavky zdroja pre všeobecného člena tímu stlačením odkazu v časti Požiadavka na zdroj.</span><span class="sxs-lookup"><span data-stu-id="076ff-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="076ff-163">![Snímka obrazovky otvorenia záložnej požiadavky na zdroj](media/FAQ-Resources-to-Tasks2-7.png "Snímka obrazovky otvorenia záložnej požiadavky na zdroj")</span><span class="sxs-lookup"><span data-stu-id="076ff-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="076ff-164">Stlačte možnosť **Rezervovať** pre všeobecný zdroj a potom môžete použiť tabuľu plánovania na vyhľadanie a rezerváciu skutočného zdroja.</span><span class="sxs-lookup"><span data-stu-id="076ff-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="076ff-165">Môžete tiež predložiť požiadavku na plnenie správcovi zdrojov stlačením možnosti **Odoslať žiadosť**.</span><span class="sxs-lookup"><span data-stu-id="076ff-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="076ff-166">Pri plnení všeobecného zdroja pomenovaným zdrojom sa všeobecný zdroj odstráni z tímu a priradenia úlohy pre všeobecný zdroj sa priradia k pomenovanému zdroju, ktorý vyplnil požiadavku na zdroj všeobecného zdroja.</span><span class="sxs-lookup"><span data-stu-id="076ff-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

