---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 29, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 29, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499690"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="6377e-103">Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 29, V3</span><span class="sxs-lookup"><span data-stu-id="6377e-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6377e-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6377e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="6377e-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="6377e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="6377e-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="6377e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="6377e-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="6377e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="6377e-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="6377e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="6377e-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 29.</span><span class="sxs-lookup"><span data-stu-id="6377e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="6377e-110">Táto verzia má číslo zostavenia V3.10.45.98 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie vo februári 2021.</span><span class="sxs-lookup"><span data-stu-id="6377e-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="6377e-111">Aktualizácia vydania 29</span><span class="sxs-lookup"><span data-stu-id="6377e-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="6377e-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="6377e-112">Bug fixes</span></span>

<span data-ttu-id="6377e-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="6377e-113">**Time and Expense**</span></span>

<span data-ttu-id="6377e-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="6377e-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="6377e-115">Používateľom sa v mriežke na zadanie času nezobrazí pracovný čas zaznamenaný počas nepracovných dní.</span><span class="sxs-lookup"><span data-stu-id="6377e-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="6377e-116">Schválené záznamy výdavkov je možné upravovať v mriežke.</span><span class="sxs-lookup"><span data-stu-id="6377e-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="6377e-117">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="6377e-117">**Project Management**</span></span>

<span data-ttu-id="6377e-118">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="6377e-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="6377e-119">Chýba logika overenia, aby sa zabezpečilo, že hodiny úsilia priraďovania zdrojov nemôžu byť záporné.</span><span class="sxs-lookup"><span data-stu-id="6377e-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="6377e-120">Vlastná akcia **AssignResourcesForTask** aktualizuje všetky polia namiesto výhradne zmenených polí.</span><span class="sxs-lookup"><span data-stu-id="6377e-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="6377e-121">Pri kopírovaní projektu v prostredí s doplnkami alebo pracovnými postupmi, ktoré sú registrované v udalosti **CreateProject**, atribút **msdyn_bulkgenerationstatus** sa neaktualizuje, ak **CopyWBSToProject** zlyhá.</span><span class="sxs-lookup"><span data-stu-id="6377e-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="6377e-122">Pri rozbalení kalendára projektu nie sú pracovné dni zoradené vzostupne, čo spôsobí zlyhanie niektorých aktualizácií úloh projektu.</span><span class="sxs-lookup"><span data-stu-id="6377e-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="6377e-123">Zmena manažéra projektu pri existujúcom projekte spustí predvolenú logiku organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="6377e-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="6377e-124">**Predaj**</span><span class="sxs-lookup"><span data-stu-id="6377e-124">**Sales**</span></span>

<span data-ttu-id="6377e-125">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="6377e-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="6377e-126">Karta **Plnenie zmluvy** na stránke **Zmluva** počas inicializácie zlyhá, ak nie sú k dispozícii žiadne riadky zmluvy.</span><span class="sxs-lookup"><span data-stu-id="6377e-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
