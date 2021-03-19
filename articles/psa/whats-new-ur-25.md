---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 25, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 25, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280462"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="438e3-103">Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 25, V3</span><span class="sxs-lookup"><span data-stu-id="438e3-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="438e3-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="438e3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="438e3-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="438e3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="438e3-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="438e3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="438e3-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="438e3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="438e3-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="438e3-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="438e3-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation V3, aktualizované vydanie 25. Táto verzia má číslo zostavenia V 3.10.43.76 a je všeobecne dostupná prostredníctvom automatickej aktualizácie v októbri 2020.</span><span class="sxs-lookup"><span data-stu-id="438e3-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="438e3-110">Aktualizácia vydania 25</span><span class="sxs-lookup"><span data-stu-id="438e3-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="438e3-111">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="438e3-111">Bug fixes</span></span>

<span data-ttu-id="438e3-112">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="438e3-112">**Time and Expense**</span></span>

<span data-ttu-id="438e3-113">Nasledujúci problém bol opravený:</span><span class="sxs-lookup"><span data-stu-id="438e3-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="438e3-114">Graf zadávania času zobrazujúci ďalšie údaje na základe príliš veľkého intervalu, ktorý sa načítava.</span><span class="sxs-lookup"><span data-stu-id="438e3-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="438e3-115">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="438e3-115">**Resource Management**</span></span>

<span data-ttu-id="438e3-116">Nasledujúci problém bol opravený:</span><span class="sxs-lookup"><span data-stu-id="438e3-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="438e3-117">Pridaný kód pre Package Deployer na preskočenie importu opravy Universal Resource Scheduling, ak už existuje opravná aktualizácia vyššej verzie.</span><span class="sxs-lookup"><span data-stu-id="438e3-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="438e3-118">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="438e3-118">**Project Management**</span></span>

<span data-ttu-id="438e3-119">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="438e3-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="438e3-120">Opravené nezrovnalosti pri zaokrúhľovaní a výmennom kurze, ktoré majú za následok nesprávne plánované náklady v mriežke sledovania projektu.</span><span class="sxs-lookup"><span data-stu-id="438e3-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="438e3-121">Podpora možnosti zobrazenia dvoch alebo viacerých reagujúcich mriežok vo formulári **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="438e3-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="438e3-122">Poskytnuté overenie na riešenie schopnosti priradiť úlohu po dátume ukončenia kalendára, čo má za následok neúspešné priradenie zdroja.</span><span class="sxs-lookup"><span data-stu-id="438e3-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="438e3-123">Vylepšené spracovanie chýb pri riešení výnimky Null Reference vygenerovanej z nasledujúcich:</span><span class="sxs-lookup"><span data-stu-id="438e3-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="438e3-124">doplnok **PreValidateProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="438e3-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="438e3-125">**PreValidateProjectTaskCreate** keď je projektová úloha vytvorená bez pridruženého projektu</span><span class="sxs-lookup"><span data-stu-id="438e3-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="438e3-126">doplnok **PreProjectTeamMemberCreate**</span><span class="sxs-lookup"><span data-stu-id="438e3-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="438e3-127">doplnok **PostProjectTeamMemberDelete**</span><span class="sxs-lookup"><span data-stu-id="438e3-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="438e3-128">doplnok **PreValidateProjectTaskDelete**</span><span class="sxs-lookup"><span data-stu-id="438e3-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="438e3-129">**Sales**</span><span class="sxs-lookup"><span data-stu-id="438e3-129">**Sales**</span></span>

<span data-ttu-id="438e3-130">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="438e3-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="438e3-131">Vylepšené spracovanie chýb pri riešení výnimiek Null Reference vygenerovaných z **Kopírovať projekt: Odhady správy HelperResource**.</span><span class="sxs-lookup"><span data-stu-id="438e3-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="438e3-132">**Nepripravené na fakturáciu** a **Backlog pre fakturáciu času a materiálu** nevymaže stav fakturácie.</span><span class="sxs-lookup"><span data-stu-id="438e3-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="438e3-133">Opravené nesprávne označené tlačidlá **Ceny** na karte **Cena roly** a **Katalógové položky**.</span><span class="sxs-lookup"><span data-stu-id="438e3-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]