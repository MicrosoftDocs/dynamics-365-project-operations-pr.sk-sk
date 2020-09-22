---
title: Príručka správcu zdrojov
description: Príručka k správe zdrojov v Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 4a3f3fa7-ae1a-4139-974b-f61cc8a8bda7
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 67b400fe3e6bb60775ee144c1d3720a311204d7d
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755661"
---
# <a name="resource-manager-guide-project-service"></a><span data-ttu-id="fb647-103">Príručka správou zdrojov (Project Service)</span><span class="sxs-lookup"><span data-stu-id="fb647-103">Resource manager guide (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="fb647-104">Možnosti [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] vám pomôžu nájsť správne zdroje v správnom čase na správny projekt a uistiť sa, že všetky zdroje sú využívané efektívne.</span><span class="sxs-lookup"><span data-stu-id="fb647-104">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] help you find the right resources at the right time for the right project and make sure all resources are utilized efficiently.</span></span>  
  
 <span data-ttu-id="fb647-105">Účinne a efektívne nasadiť konzultantov spoločnosti s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="fb647-105">Deploy your company’s consultants efficiently and effectively with the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="fb647-106">Ponúkne vám to nástroje, ktoré potrebujete pri plánovaní prostriedkov na základe požiadaviek a plánov konzultačných projektov a schopností a dostupnosti vašich poradcov.</span><span class="sxs-lookup"><span data-stu-id="fb647-106">These provide you with the tools you need to schedule resources based on the requirements and schedules of consulting projects and on the skills and availability of your consultants.</span></span> <span data-ttu-id="fb647-107">Môžete rýchlo nájsť najviac kvalifikovaných konzultantov, ktorí sú k dispozícii pre prácu na projektoch, a môžete ľahko zistiť, ako ich lepšie naplánovať v priebehu každého projektu.</span><span class="sxs-lookup"><span data-stu-id="fb647-107">You can quickly find the most qualified consultants who are available to work on projects, and you can easily see how to better schedule them during the course of each project.</span></span>  
  
 <span data-ttu-id="fb647-108">Plánovanie prostriedkov umožňuje vykonanie nasledovného:</span><span class="sxs-lookup"><span data-stu-id="fb647-108">Resource scheduling helps you do the following:</span></span>  
  
- <span data-ttu-id="fb647-109">Priradiť zdroje na projekty založené na tom, ako dobre sa zručnosti a spôsobilosti zhodujú s požiadavkami na zdroje projektu.</span><span class="sxs-lookup"><span data-stu-id="fb647-109">Match resources to projects, based on how well their skills and proficiency levels match the project resource requirements.</span></span>  
  
- <span data-ttu-id="fb647-110">Priraďte plány zdrojov ku kalendáru projektu na základe ich dostupnosti a plánovaného času voľna.</span><span class="sxs-lookup"><span data-stu-id="fb647-110">Match a resource’s schedule to a project calendar, based on their availability and scheduled time off.</span></span> <span data-ttu-id="fb647-111">Farebný kalendár vám dáva vizuálne signály o dostupnosti zdrojov.</span><span class="sxs-lookup"><span data-stu-id="fb647-111">The color-coded calendar gives you visual cues about resource availability.</span></span>  
  
- <span data-ttu-id="fb647-112">Prehodnoťte kapacity každého konzultant a zistite, ako sa v súčasnosti používa táto kapacita.</span><span class="sxs-lookup"><span data-stu-id="fb647-112">Review the capacity of each consultant and determine how that capacity is currently used.</span></span> <span data-ttu-id="fb647-113">To vám pomôže nájsť, kde by mohol byť konzultant nadmerne alebo podpriemerne využitý, prípadne to, že robia nad svoju kapacitu.</span><span class="sxs-lookup"><span data-stu-id="fb647-113">This can help you find where a consultant might be under- or over-utilized, or if they’re working at capacity.</span></span>  
  
- <span data-ttu-id="fb647-114">Percento alebo určitý počet hodín pre pracovníka kapacity k projektu.</span><span class="sxs-lookup"><span data-stu-id="fb647-114">Assign a percentage or a specific number of hours for a worker’s capacity to a project.</span></span>  
  
- <span data-ttu-id="fb647-115">Robte skupinové rezervácie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="fb647-115">Make group resource bookings.</span></span>  
  
- <span data-ttu-id="fb647-116">Robte jemnú alebo pevnú rezerváciu zdrojov a jemné rezervované hodiny premieňajte na pevné hodiny len pomocou jedného kroku.</span><span class="sxs-lookup"><span data-stu-id="fb647-116">Soft book or hard book resources, and convert soft-booked hours into hard-booked hours in one step.</span></span>  
  
- <span data-ttu-id="fb647-117">Automaticky vytvorí projektový tím na základe zdrojov podľa štruktúry rozdelenia práce pre projekt.</span><span class="sxs-lookup"><span data-stu-id="fb647-117">Automatically form a project team based on resources defined in a work breakdown structure for a project.</span></span>  
  
- <span data-ttu-id="fb647-118">Splnenie požiadaviek zdroja (rezervácia, návrh, vyhľadanie náhradných zdrojov).</span><span class="sxs-lookup"><span data-stu-id="fb647-118">Fulfill resource requests (book, propose, find substitute resources).</span></span>  
  
- <span data-ttu-id="fb647-119">Priradiť prostriedky podľa centrálneho (správa priradenia zdrojov) alebo hybridného modelu (môže ich priradiť správca zdrojov alebo iní správcovia).</span><span class="sxs-lookup"><span data-stu-id="fb647-119">Assign resources according to a central (resource manager assigns) or hybrid model (resource manager and other managers can assign).</span></span> <span data-ttu-id="fb647-120">Ďalšie informácie o nastavení centrálneho alebo hybridného modelu riadenia zdrojov sa dozviete v článku [Konfigurovať doplňujúce parametre nastavenia (Project Service)](../project-service/configure-additional-parameters-settings.md).</span><span class="sxs-lookup"><span data-stu-id="fb647-120">For more information about setting a central versus hybrid resource management model, see [Configure additional parameters settings (Project Service)](../project-service/configure-additional-parameters-settings.md).</span></span>  
  
  <span data-ttu-id="fb647-121">Môžete efektívne spravovať prostriedky cez projekty a zabezpečiť, že projekty pracujú správne.</span><span class="sxs-lookup"><span data-stu-id="fb647-121">You can manage resources efficiently across projects and ensure that projects are staffed appropriately.</span></span> <span data-ttu-id="fb647-122">Budete potrebovať vykonať nasledovnú úlohy:</span><span class="sxs-lookup"><span data-stu-id="fb647-122">You’ll need to perform the following tasks:</span></span>  
  
- <span data-ttu-id="fb647-123">[Správa žiadostí na zdroje](../project-service/manage-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="fb647-123">[Manage resource requests](../project-service/manage-resource-requests.md).</span></span> <span data-ttu-id="fb647-124">Priraďte schopnosti a zručnosti vašich konzultantov k tým správnym projektom.</span><span class="sxs-lookup"><span data-stu-id="fb647-124">Match the skills and proficiencies of your consultants to the right projects.</span></span>  
  
- <span data-ttu-id="fb647-125">[Zobrazenie prostriedkov dostupnosti](../project-service/view-resource-availability.md)</span><span class="sxs-lookup"><span data-stu-id="fb647-125">[View resource availability](../project-service/view-resource-availability.md).</span></span> <span data-ttu-id="fb647-126">Dostupnosti pre konzultantov v zobrazení kalendára.</span><span class="sxs-lookup"><span data-stu-id="fb647-126">Check consultants’ availability in a calendar view.</span></span>  
  
- <span data-ttu-id="fb647-127">[Zobrazenie využitie zdroja](../project-service/view-resource-utilization.md)</span><span class="sxs-lookup"><span data-stu-id="fb647-127">[View resource utilization](../project-service/view-resource-utilization.md).</span></span> <span data-ttu-id="fb647-128">Pozrite sa na percento času, počas ktorého sú vaši poradcovia momentálne rezervovaní.</span><span class="sxs-lookup"><span data-stu-id="fb647-128">See the percentage of time that your consultants are currently booked.</span></span>  
  
- <span data-ttu-id="fb647-129">[Naplánujte zdroje pre projekt](../project-service/schedule-resources-project.md)</span><span class="sxs-lookup"><span data-stu-id="fb647-129">[Schedule resources for a project](../project-service/schedule-resources-project.md).</span></span> <span data-ttu-id="fb647-130">Naplánujte konzultantov pre projekt.</span><span class="sxs-lookup"><span data-stu-id="fb647-130">Schedule consultants for a project.</span></span>  
  
  <span data-ttu-id="fb647-131">Ďalšie informácie o podávaní žiadostí zdrojov pre jednotlivé projekty uvidíte v časti [Odoslanie žiadostí na zdroje](../project-service/submit-resource-requests.md).</span><span class="sxs-lookup"><span data-stu-id="fb647-131">For more information about submitting resource requests for individual projects, see [Submit resource requests](../project-service/submit-resource-requests.md).</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="fb647-132">Pozrite si tiež</span><span class="sxs-lookup"><span data-stu-id="fb647-132">See Also</span></span>  
 <span data-ttu-id="fb647-133">[Prehľad Project Service](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="fb647-133">[Overview of Project Service](../project-service/overview.md) </span></span>  
 <span data-ttu-id="fb647-134">[Príručka správcu](../project-service/admin-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fb647-134">[Administrator Guide](../project-service/admin-guide.md) </span></span>  
 <span data-ttu-id="fb647-135">[Príručka manažéra obchodného vzťahu](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fb647-135">[Account Manager Guiden](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="fb647-136">[Príručka projektového manažéra](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="fb647-136">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 [<span data-ttu-id="fb647-137">Príručka časom, nákladmi a spoluprácou</span><span class="sxs-lookup"><span data-stu-id="fb647-137">Time, Expense, and Collaboration Guide</span></span>](../project-service/time-expense-collaboration-guide.md)
