---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 18, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 18, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 1d7ea200531dd24d56a829f879e3a2532a9b38dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084318"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="a489f-103">Aktualizácia pre Project Service Automation, vydanie 18, V3</span><span class="sxs-lookup"><span data-stu-id="a489f-103">Project Service Automation Update Release 18, V3</span></span>

<span data-ttu-id="a489f-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a489f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a489f-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="a489f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a489f-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="a489f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a489f-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="a489f-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="a489f-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a489f-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a489f-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 18.</span><span class="sxs-lookup"><span data-stu-id="a489f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="a489f-110">Táto verzia má číslo V3.10.8.12 a v apríli 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="a489f-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="a489f-111">Aktualizácia vydania 18</span><span class="sxs-lookup"><span data-stu-id="a489f-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a489f-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="a489f-112">Bug fixes</span></span>

<span data-ttu-id="a489f-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="a489f-113">**Time and Expense**</span></span>

- <span data-ttu-id="a489f-114">Opravené: Toky **Odvolať** , **Vyžiadať** a **Zrušiť schválenie** vyvolávajú výnimky s nejasnými chybovými hláseniami.</span><span class="sxs-lookup"><span data-stu-id="a489f-114">Fixed: **Recall** , **Request** , and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="a489f-115">Opravené: Ak zlyhá tok **Zrušiť schválenie** pre výdavok, nevyvolá sa príslušná výnimka.</span><span class="sxs-lookup"><span data-stu-id="a489f-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="a489f-116">Opravené: Mriežka so zadaniami času po prepnutí letného času (DST) v októbri nesprávne spracováva dni pracovného pokoja v Austrálii.</span><span class="sxs-lookup"><span data-stu-id="a489f-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="a489f-117">Opravené: Nesprávna predvolená logika bráni zadávaniu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="a489f-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="a489f-118">Opravené: Ak zlyhá schválenie zadania, toto schválenie zostáva v stave **Nevybavené**.</span><span class="sxs-lookup"><span data-stu-id="a489f-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="a489f-119">Opravené: Chyby SQL pri hromadných schváleniach (zablokovanie/časový limit).</span><span class="sxs-lookup"><span data-stu-id="a489f-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="a489f-120">Opravené: Závažné problémy s výkonom v používateľskom rozhraní spôsobené aktualizáciou členov tímu počas schvaľovania zadaní času.</span><span class="sxs-lookup"><span data-stu-id="a489f-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="a489f-121">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="a489f-121">**Project Management**</span></span>

- <span data-ttu-id="a489f-122">Opravené: Oznámenie o časovom pásme bolo presunuté zo zobrazenia **Vyrovnanie** na hlavný formulár **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="a489f-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="a489f-123">Opravené: Šablóna kalendára nie je správne predvolená po otvorení nového formulára projektu.</span><span class="sxs-lookup"><span data-stu-id="a489f-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="a489f-124">Opravené: Pri prehliadačoch založených na technológii Chromium nemôžu používatelia jednoducho vybrať predchádzajúce úlohy na odstránenie.</span><span class="sxs-lookup"><span data-stu-id="a489f-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="a489f-125">Opravené: Vytvorením alebo skopírovaním **Projektu z prázdnej šablóny** sa načítajú nesúvisiace priradenia.</span><span class="sxs-lookup"><span data-stu-id="a489f-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="a489f-126">Opravené: V konkrétnych okrajových prípadoch povedie vytvorenie nového priradenia z mriežky úloh k vytvoreniu duplicitných záznamov.</span><span class="sxs-lookup"><span data-stu-id="a489f-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="a489f-127">Opravené: V manuálnom režime nemôžu používatelia aktualizovať dátum začatia úlohy na neskorší dátum ako ten, ktorý je aktuálne uložený.</span><span class="sxs-lookup"><span data-stu-id="a489f-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="a489f-128">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="a489f-128">**Resource Management**</span></span>

- <span data-ttu-id="a489f-129">Opravené: V riadku medzisúčtu v zobrazení **Vyrovnanie** sa nesprávne vypočíta odchýlka v rezerváciách po rozšírení rezervácií.</span><span class="sxs-lookup"><span data-stu-id="a489f-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="a489f-130">Opravené: V zobrazení **Vyrovnanie** sa nesprávne zobrazia priradenia zdrojov, ak rezervovateľný zdroj obsahuje kalendár, ktorý sa nezhoduje s kalendárom projektu.</span><span class="sxs-lookup"><span data-stu-id="a489f-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="a489f-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="a489f-131">**Sales**</span></span>

- <span data-ttu-id="a489f-132">Opravené: Pri opätovnom schválení zadaní času ( **Schváliť > Zrušiť >** Opätovne schváliť) sa vytvorí duplikát skutočnej neúčtovanej sumy.</span><span class="sxs-lookup"><span data-stu-id="a489f-132">Fixed: When time entries are re-approved ( **Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
