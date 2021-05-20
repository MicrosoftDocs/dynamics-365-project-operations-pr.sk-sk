---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 31, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 31, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945554"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="19cdb-103">Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 31, V3</span><span class="sxs-lookup"><span data-stu-id="19cdb-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="19cdb-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="19cdb-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="19cdb-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="19cdb-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="19cdb-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="19cdb-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="19cdb-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="19cdb-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="19cdb-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="19cdb-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="19cdb-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 31.</span><span class="sxs-lookup"><span data-stu-id="19cdb-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="19cdb-110">Táto verzia má číslo V3.10.52.77 a v máji 2021 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="19cdb-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="19cdb-111">Aktualizácia vydania 31</span><span class="sxs-lookup"><span data-stu-id="19cdb-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="19cdb-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="19cdb-112">Bug fixes</span></span>

<span data-ttu-id="19cdb-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="19cdb-113">**Time and Expense**</span></span>

<span data-ttu-id="19cdb-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="19cdb-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="19cdb-115">Ovládacie tlačidlá príkazu na zadanie času na stránke **Rezervovateľný zdroj** bola neprehľadná.</span><span class="sxs-lookup"><span data-stu-id="19cdb-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="19cdb-116">V systéme bola vygenerovaná nulová referenčná výnimka **Project.SetTrackingFields** pri schvaľovaní časového záznamu.</span><span class="sxs-lookup"><span data-stu-id="19cdb-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="19cdb-117">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="19cdb-117">**Resource Management**</span></span>

<span data-ttu-id="19cdb-118">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="19cdb-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="19cdb-119">**Vytvoriť člena tímu** nezobrazuje správne nastavenie metadát nastavenia rezervácie pre server **Predvolený stav potvrdenia rezervácie**.</span><span class="sxs-lookup"><span data-stu-id="19cdb-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="19cdb-120">Pri aktualizácii z PSA 1.X na 3.X proces aktualizácie zlyhá pri **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="19cdb-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="19cdb-121">**Predaj**</span><span class="sxs-lookup"><span data-stu-id="19cdb-121">**Sales**</span></span>

<span data-ttu-id="19cdb-122">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="19cdb-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="19cdb-123">Skutočný príjem prevádza sumy v sledovacej mriežke na menu projektu.</span><span class="sxs-lookup"><span data-stu-id="19cdb-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="19cdb-124">Predvolené meny sú nejasné pri vytváraní riadkov denníka, riadkov ponúk a kontraktov v scenároch, kde sa základná mena organizácie líši od meny projektu.</span><span class="sxs-lookup"><span data-stu-id="19cdb-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="19cdb-125">**Čaká sa na overenie denníka opráv** dopyt nefiltruje podľa projektu.</span><span class="sxs-lookup"><span data-stu-id="19cdb-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="19cdb-126">Zvyšný predaj sa v projekte počíta nesprávne.</span><span class="sxs-lookup"><span data-stu-id="19cdb-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="19cdb-127">Cenové ponuky založené na kontakte zlyhajú, keď sú vytvorené bez cenníka.</span><span class="sxs-lookup"><span data-stu-id="19cdb-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="19cdb-128">Po výbere možnosti **Potvrdiť faktúru** sa nezobrazí žiadny číselník spracovania.</span><span class="sxs-lookup"><span data-stu-id="19cdb-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="19cdb-129">Po výbere možnosti **Vytvoriť faktúru** sa nezobrazí žiadny číselník spracovania.</span><span class="sxs-lookup"><span data-stu-id="19cdb-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="19cdb-130">Uzatvorenie cenovej ponuky za stratené nezruší rezervácie.</span><span class="sxs-lookup"><span data-stu-id="19cdb-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







