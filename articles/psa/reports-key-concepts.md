---
title: Kľúčové koncepty
description: Táto téma obsahuje prepojenia na kľúčové koncepty pre riadenie zdrojov v Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 862e277d8109e810401bdecd4c45c2696275f8a8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120382"
---
# <a name="key-concepts"></a><span data-ttu-id="b9db8-103">Kľúčové koncepty</span><span class="sxs-lookup"><span data-stu-id="b9db8-103">Key concepts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b9db8-104">Nasledujúca tabuľka definuje kľúčové koncepty, ktoré sa používajú v aplikácii Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b9db8-104">The following table defines key concepts that are used in the Dynamics 365 Project Service Automation app.</span></span>

| <span data-ttu-id="b9db8-105">Koncept</span><span class="sxs-lookup"><span data-stu-id="b9db8-105">Concept</span></span>                    | <span data-ttu-id="b9db8-106">Definícia</span><span class="sxs-lookup"><span data-stu-id="b9db8-106">Definition</span></span> |
|----------------------------|------------|
| <span data-ttu-id="b9db8-107">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="b9db8-107">Project team member</span></span>        | <span data-ttu-id="b9db8-108">Ako súčasť projektového tímu môže byť členom projektového tímu pomenovaný zdroj, ktorý má rezervácie, pomenovaný zdroj, ktorý nemá rezervácie, alebo všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="b9db8-108">As part of the project team, a project team member can be a named resource that has bookings, a named resource that doesn't have bookings, or a generic resource.</span></span> <span data-ttu-id="b9db8-109">Všeobecné zdroje nemajú rezervácie, sú miestne pre projekt, a nemajú kapacitné obmedzenia naprieč projektmi.</span><span class="sxs-lookup"><span data-stu-id="b9db8-109">Generic resources don't have bookings, are local to the project, and don't have capacity constraints across projects.</span></span> |
| <span data-ttu-id="b9db8-110">Projektové generické zdroje</span><span class="sxs-lookup"><span data-stu-id="b9db8-110">Project generic resource</span></span>   | <span data-ttu-id="b9db8-111">Zástupný symbol prostriedku, ktorý vám umožní vytvoriť tím a zamestnanca projektového plánu bez toho, aby ste museli poznať pomenovaný prostriedok.</span><span class="sxs-lookup"><span data-stu-id="b9db8-111">A resource placeholder that lets you form a team and staff a project plan without having to know the named resource.</span></span> <span data-ttu-id="b9db8-112">Kalendár projektu sa používa ako kalendár všeobecného prostriedku.</span><span class="sxs-lookup"><span data-stu-id="b9db8-112">The project calendar is used as the generic resource's calendar.</span></span> <span data-ttu-id="b9db8-113">Všeobecné zdroje môžu byť pridané do projektového tímu a priradené k úlohám.</span><span class="sxs-lookup"><span data-stu-id="b9db8-113">Generic resources can be added to a project team and assigned to tasks.</span></span> |
| <span data-ttu-id="b9db8-114">Rezervované hodiny</span><span class="sxs-lookup"><span data-stu-id="b9db8-114">Booked hours</span></span>               | <span data-ttu-id="b9db8-115">Hodiny prostriedku sú ťažko rezervované proti projektu, ktorý pomáha zaručiť dokončenie projektovej práce.</span><span class="sxs-lookup"><span data-stu-id="b9db8-115">Resource hours are hard-booked against a project to help guarantee that the project work is completed.</span></span> <span data-ttu-id="b9db8-116">Rezervované hodiny sú spotrebované z celkovej kapacity zdroja.</span><span class="sxs-lookup"><span data-stu-id="b9db8-116">Booked hours are consumed from the resource's overall capacity.</span></span> <span data-ttu-id="b9db8-117">Rezervácie sú proti iba pomenované zdroje, nie proti všeobecným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="b9db8-117">Bookings are against named resources only, not against generic resources.</span></span> |
| <span data-ttu-id="b9db8-118">Priradené hodiny</span><span class="sxs-lookup"><span data-stu-id="b9db8-118">Assigned hours</span></span>             | <span data-ttu-id="b9db8-119">Hodiny prostriedkov sú priradené k úlohám v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="b9db8-119">Resource hours are assigned to tasks in the project schedule.</span></span> <span data-ttu-id="b9db8-120">Priradenia môžu byť proti buď pomenovaným zdrojom, alebo všeobecným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="b9db8-120">Assignments can be against either named resources or generic resources.</span></span> <span data-ttu-id="b9db8-121">Úlohy môžu byť nezávislé od rezervácií.</span><span class="sxs-lookup"><span data-stu-id="b9db8-121">Assignments can be independent of bookings.</span></span> |
| <span data-ttu-id="b9db8-122">Požadované hodiny</span><span class="sxs-lookup"><span data-stu-id="b9db8-122">Required hours</span></span>             | <span data-ttu-id="b9db8-123">Požadovaná kapacita, ktorá ešte nie je splnená zo strany pomenovaného prostriedku.</span><span class="sxs-lookup"><span data-stu-id="b9db8-123">The capacity that is required, but that isn't yet fulfilled by a named resource.</span></span> <span data-ttu-id="b9db8-124">Požadované hodiny sú relevantné len pre generických členov tímu, ktorí vygenerovali požiadavky na zdroje.</span><span class="sxs-lookup"><span data-stu-id="b9db8-124">Required hours are relevant only for generic team members that have generated resource requirements.</span></span> |
| <span data-ttu-id="b9db8-125">Dopyt</span><span class="sxs-lookup"><span data-stu-id="b9db8-125">Demand</span></span>                     | <span data-ttu-id="b9db8-126">Aktuálna a prichádzajúca pracovná záťaž.</span><span class="sxs-lookup"><span data-stu-id="b9db8-126">The current and incoming workload.</span></span> <span data-ttu-id="b9db8-127">V Project Service Automation dopyt sa zobrazuje ako zdroj požiadavky alebo požiadavky na zdroje.</span><span class="sxs-lookup"><span data-stu-id="b9db8-127">In Project Service Automation, demand is shown as resource requirements or resource requests.</span></span> |
| <span data-ttu-id="b9db8-128">Požiadavka na zdroj</span><span class="sxs-lookup"><span data-stu-id="b9db8-128">Resource requirement</span></span>       | <span data-ttu-id="b9db8-129">Entita, ktorá sa používa na zachytenie požadovaných hodín, začiatočného a koncového dátumu, zručnosti, geografie a iných cenových dimenzií pre požadované zdroje.</span><span class="sxs-lookup"><span data-stu-id="b9db8-129">An entity that is used to capture required hours, start and end dates, skills, geography, and other pricing dimensions for the required resources.</span></span> <span data-ttu-id="b9db8-130">Požiadavky na zdroje sú buď generované z členov projektového tímu, alebo jednotlivo vytvorené.</span><span class="sxs-lookup"><span data-stu-id="b9db8-130">Resource requirements are either generated from project team members or individually created.</span></span> |
| <span data-ttu-id="b9db8-131">Žiadosť o zdroj</span><span class="sxs-lookup"><span data-stu-id="b9db8-131">Resource request</span></span>           | <span data-ttu-id="b9db8-132">Entita, ktorá sa používa ako „obálka” na predstavenie požiadavky zdroja, ktorý je potrebné splniť zo strany manažéra zdroja.</span><span class="sxs-lookup"><span data-stu-id="b9db8-132">An entity that is used as an "envelope" to carry the resource requirement that must be fulfilled by a resource manager.</span></span> |
| <span data-ttu-id="b9db8-133">Predvolená rola zdroja</span><span class="sxs-lookup"><span data-stu-id="b9db8-133">Resource default role</span></span>      | <span data-ttu-id="b9db8-134">Rola, pod ktorou je prostriedok zoskupený do výpočtu využitia.</span><span class="sxs-lookup"><span data-stu-id="b9db8-134">The role that a resource is grouped under for utilization calculation.</span></span> <span data-ttu-id="b9db8-135">Predpokladá sa, že zdroj má požadované zručnosti pre rolu a spĺňa cieľové využitie tejto úlohy.</span><span class="sxs-lookup"><span data-stu-id="b9db8-135">The resource is assumed to have the required skills for the role and to meet the target utilization for that role.</span></span> |
| <span data-ttu-id="b9db8-136">Organizačná jednotka zdroja</span><span class="sxs-lookup"><span data-stu-id="b9db8-136">Resource organization unit</span></span> | <span data-ttu-id="b9db8-137">Organizačná jednotka, ktorá má priradený zdroj.</span><span class="sxs-lookup"><span data-stu-id="b9db8-137">The organizational unit that a resource is assigned to.</span></span> |
| <span data-ttu-id="b9db8-138">Kontúry</span><span class="sxs-lookup"><span data-stu-id="b9db8-138">Contour</span></span>                    | <span data-ttu-id="b9db8-139">Úloha, požiadavka alebo doba priradenia, pretože sú rozdelené do dennej distribúcie.</span><span class="sxs-lookup"><span data-stu-id="b9db8-139">Task, requirement, or assignment hours as they are broken down into a daily distribution.</span></span> <span data-ttu-id="b9db8-140">Napríklad, päťdňová, 40-hodinový úloha môže byť kontúrovaná do ôsmich hodín denne počas piatich dní.</span><span class="sxs-lookup"><span data-stu-id="b9db8-140">For example, a five-day, 40-hour task can be contoured into eight hours per day over five days.</span></span> |
| <span data-ttu-id="b9db8-141">Zobrazenie Vyrovnanie</span><span class="sxs-lookup"><span data-stu-id="b9db8-141">Reconciliation view</span></span>        | <span data-ttu-id="b9db8-142">Zobrazenie zobrazuje rezervácie a všetky priradenia pre každého člena projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="b9db8-142">A view that shows the bookings and assignments for each project team member.</span></span> <span data-ttu-id="b9db8-143">Toto zobrazenie umožňuje projektovým manažérom nájsť nesúlad medzi rezerváciami a priradeniami a prijať nápravné opatrenia, ak nastane akýkoľvek nesúlad.</span><span class="sxs-lookup"><span data-stu-id="b9db8-143">This view lets the project manager look for any mismatch between bookings and assignments, and to take corrective action if any mismatch occurs.</span></span> |
| <span data-ttu-id="b9db8-144">Pracovná doba</span><span class="sxs-lookup"><span data-stu-id="b9db8-144">Work hours</span></span>                 | <span data-ttu-id="b9db8-145">Entita, ktorá sa používa na identifikáciu kapacity zdroja a pracovných a nepracovných hodín.</span><span class="sxs-lookup"><span data-stu-id="b9db8-145">An entity that is used to identify resource capacity, and working and non-working hours.</span></span> <span data-ttu-id="b9db8-146">Táto entita sa označuje aj ako kalendár zdrojov.</span><span class="sxs-lookup"><span data-stu-id="b9db8-146">This entity is also referred to as the resource calendar.</span></span> |