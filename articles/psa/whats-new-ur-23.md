---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 23, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 23, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131137"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="3476e-103">Aktualizácia pre Project Service Automation, vydanie 23, V3</span><span class="sxs-lookup"><span data-stu-id="3476e-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="3476e-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="3476e-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="3476e-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="3476e-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="3476e-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="3476e-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="3476e-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="3476e-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="3476e-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="3476e-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="3476e-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 23.</span><span class="sxs-lookup"><span data-stu-id="3476e-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="3476e-110">Táto verzia má číslo V 3.10.34.30 a vo všeobecnosti je k dispozícii prostredníctvom samostatnej aktualizácie z augusta 2020.</span><span class="sxs-lookup"><span data-stu-id="3476e-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="3476e-111">Aktualizácia vydania 23</span><span class="sxs-lookup"><span data-stu-id="3476e-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="3476e-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="3476e-112">Bug fixes</span></span>

<span data-ttu-id="3476e-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="3476e-113">**Time and Expense**</span></span>

<span data-ttu-id="3476e-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="3476e-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="3476e-115">Spracúvajte hraničné prípady v časti **Odstránenie člena projektového tímu** na poskytnutie zmysluplnej výnimky.</span><span class="sxs-lookup"><span data-stu-id="3476e-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="3476e-116">Výsledkom importu priradenia je prázdna obrazovka odstránenia.</span><span class="sxs-lookup"><span data-stu-id="3476e-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="3476e-117">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="3476e-117">**Resource Management**</span></span>

<span data-ttu-id="3476e-118">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="3476e-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="3476e-119">**Karta zdrojov mriežky využitia zdrojov** ukazuje nesprávne údaje, ak je časová škála dlhšia ako päť dní.</span><span class="sxs-lookup"><span data-stu-id="3476e-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="3476e-120">Keď zákazníci vytvoria rezervovateľný zdroj, doplnok občas zlyhá pri automatickom pridávaní zdroja do skupiny Microsoft Office 365.</span><span class="sxs-lookup"><span data-stu-id="3476e-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="3476e-121">Zobrazenie **Vyrovnanie** ukazuje nesprávne manuálne kontúry v zobrazení **Týždeň** alebo **Mesiac**.</span><span class="sxs-lookup"><span data-stu-id="3476e-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="3476e-122">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="3476e-122">**Project Management**</span></span>

<span data-ttu-id="3476e-123">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="3476e-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="3476e-124">Nadmerný počet entít **RetrieveMultiple for usersettings** spôsobuje zhoršenú výkonnosť pri schvaľovaní projektov a iných operáciách.</span><span class="sxs-lookup"><span data-stu-id="3476e-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="3476e-125">Vyhľadávanie zdrojov na mriežke **Plánovanie úloh** je obmedzené na zobrazenie iba piatich členov tímu z projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="3476e-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="3476e-126">Vyhľadávanie zdrojov na mriežke **Plánovanie úloh** nefiltruje neaktívne zdroje.</span><span class="sxs-lookup"><span data-stu-id="3476e-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="3476e-127">Manuálny režim nefunguje podľa očakávania v štruktúre rozdelenia práce pri plánovaní projektu.</span><span class="sxs-lookup"><span data-stu-id="3476e-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="3476e-128">Mriežka **Plánovanie úloh** ukazuje **Kategórie neaktívnych transakcií**.</span><span class="sxs-lookup"><span data-stu-id="3476e-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="3476e-129">Mriežka **Priradenie zdrojov** sa zaokrúhľuje nesprávne, keď má úloha viac priradení.</span><span class="sxs-lookup"><span data-stu-id="3476e-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="3476e-130">Hodnoty zaokrúhľovania sa líšia medzi plánovanými a skutočnými nákladmi na jednu úlohu.</span><span class="sxs-lookup"><span data-stu-id="3476e-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="3476e-131">**Sales**</span><span class="sxs-lookup"><span data-stu-id="3476e-131">**Sales**</span></span>

<span data-ttu-id="3476e-132">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="3476e-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="3476e-133">Dvojité kliknutie na položku **Načítať všetky kategórie transakcií** vytvorí viac riadkov.</span><span class="sxs-lookup"><span data-stu-id="3476e-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
