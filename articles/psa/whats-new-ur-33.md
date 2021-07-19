---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 33, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 33, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334599"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="03e7f-103">Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 33, V3</span><span class="sxs-lookup"><span data-stu-id="03e7f-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="03e7f-104">S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="03e7f-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="03e7f-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="03e7f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="03e7f-106">Je kompatibilná s verziou Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="03e7f-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="03e7f-107">Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="03e7f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="03e7f-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="03e7f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="03e7f-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 33.</span><span class="sxs-lookup"><span data-stu-id="03e7f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="03e7f-110">Táto verzia má číslo zostavenia V3.10.54.98 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie z júla 2021.</span><span class="sxs-lookup"><span data-stu-id="03e7f-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="03e7f-111">Aktualizácia vydania 33</span><span class="sxs-lookup"><span data-stu-id="03e7f-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="03e7f-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="03e7f-112">Bug fixes</span></span>

<span data-ttu-id="03e7f-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="03e7f-113">**Time and Expense**</span></span>

<span data-ttu-id="03e7f-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="03e7f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="03e7f-115">Dve zamknuté polia, **msdyn_description** a **msdyn_externaldescription** sú editovateľné po odoslaní.</span><span class="sxs-lookup"><span data-stu-id="03e7f-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="03e7f-116">Chybové hlásenie sa objaví, ak sa vytvorí výdaj, ktorý nesúvisí s projektom.</span><span class="sxs-lookup"><span data-stu-id="03e7f-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="03e7f-117">Keď je vytvorený časový záznam, predvolená rola prostriedku je neaktívna.</span><span class="sxs-lookup"><span data-stu-id="03e7f-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="03e7f-118">Riadky denníka spojené s odvolaným a odstráneným výdavkom sa neodstránia.</span><span class="sxs-lookup"><span data-stu-id="03e7f-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="03e7f-119">V rámci položky **Formulár rýchleho vytvorenia zadania času** aktualizujte zobrazenie **Zoznam projektových úloh** a zmeňte predvolene zobrazený dátum na dátum začatia úlohy.</span><span class="sxs-lookup"><span data-stu-id="03e7f-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="03e7f-120">Keď vytvoríte časový záznam na karte **Súvisiace**, na záložke rezervovateľného zdroja je pre prihláseného používateľa nesprávne vytvorený časový údaj namiesto nadradeného rezervovateľného prostriedku.</span><span class="sxs-lookup"><span data-stu-id="03e7f-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="03e7f-121">Do dialógového okna **Hromadné schválenie MDD** sú pridané ďalšie polia.</span><span class="sxs-lookup"><span data-stu-id="03e7f-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="03e7f-122">**Plánovanie projektu**</span><span class="sxs-lookup"><span data-stu-id="03e7f-122">**Project planning**</span></span>

<span data-ttu-id="03e7f-123">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="03e7f-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="03e7f-124">K pomalému výkonu pri vytváraní projektu dochádza, keď sa šablóny pracovných hodín projektu používajú so zložitými kalendármi.</span><span class="sxs-lookup"><span data-stu-id="03e7f-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="03e7f-125">Keď je počiatočný dátum väčší ako konečný dátum, na šablóne projektu kopírovania sa zobrazí chyba z dôvodu rozdielov v časovej zložke každého poľa.</span><span class="sxs-lookup"><span data-stu-id="03e7f-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="03e7f-126">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="03e7f-126">**Resource management**</span></span>

<span data-ttu-id="03e7f-127">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="03e7f-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="03e7f-128">V dotaze na využitie prostriedkov sa používa nesprávny parameter a XML vedie k nesprávnym výsledkom filtra v mriežke **Využitie zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="03e7f-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="03e7f-129">Potvrdenie **Rozšíriť rezervácie** zobrazí nesprávny dátum ukončenia rezervácie.</span><span class="sxs-lookup"><span data-stu-id="03e7f-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="03e7f-130">**Predaj**</span><span class="sxs-lookup"><span data-stu-id="03e7f-130">**Sales**</span></span>

<span data-ttu-id="03e7f-131">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="03e7f-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="03e7f-132">Ak sa vytvorí cena kategórie s chýbajúcimi hodnotami, zobrazí sa chybové hlásenie.</span><span class="sxs-lookup"><span data-stu-id="03e7f-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="03e7f-133">Chybové hlásenie sa objaví, ak sa míľnik riadka zmluvy vytvorí bez riadku objednávky.</span><span class="sxs-lookup"><span data-stu-id="03e7f-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
