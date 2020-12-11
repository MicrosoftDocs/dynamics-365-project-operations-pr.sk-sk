---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 12, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 12, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: fc92a5dcc111688159f9be5b2839b7c040404a3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119977"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="819b9-103">Aktualizácia pre Project Service Automation, vydanie 12, V3</span><span class="sxs-lookup"><span data-stu-id="819b9-103">Project Service Automation Update Release 12, V3</span></span>
<span data-ttu-id="819b9-104">S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="819b9-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="819b9-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="819b9-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="819b9-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="819b9-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="819b9-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="819b9-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="819b9-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="819b9-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="819b9-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 12.</span><span class="sxs-lookup"><span data-stu-id="819b9-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="819b9-110">Táto verzia má číslo zostavy V3.10.2.34 a je všeobecne dostupná prostredníctvom samoaktualizácie v októbri 2019.</span><span class="sxs-lookup"><span data-stu-id="819b9-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="819b9-111">Aktualizácia vydania 12</span><span class="sxs-lookup"><span data-stu-id="819b9-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="819b9-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="819b9-112">Bug fixes</span></span>

- <span data-ttu-id="819b9-113">Čas a výdavky</span><span class="sxs-lookup"><span data-stu-id="819b9-113">Time and Expense</span></span>

    - <span data-ttu-id="819b9-114">Oprava: Chybové správy o zadaní času boli aktualizované s relevantnejším kontextom.</span><span class="sxs-lookup"><span data-stu-id="819b9-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="819b9-115">Oprava: Mriežka zadávania času a harmonogram správne zobrazujú vertikálny posúvač, ak je to potrebné.</span><span class="sxs-lookup"><span data-stu-id="819b9-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="819b9-116">Oprava: Odoslané výdavky a zadania času môžu byť schválené.</span><span class="sxs-lookup"><span data-stu-id="819b9-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="819b9-117">Oprava: Dialogové okno s potvrdením o zrušení schválenia bolo opravené, aby odrážalo stav schválenia pri zmene zo **Schválený** na **Predložený**.</span><span class="sxs-lookup"><span data-stu-id="819b9-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="819b9-118">Oprava: Polia **Cena**, **Jednotka** a **Množstvo** sú teraz uzamknuté v zázname Výdavok po ich schválení.</span><span class="sxs-lookup"><span data-stu-id="819b9-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="819b9-119">Riadenie projektov</span><span class="sxs-lookup"><span data-stu-id="819b9-119">Project Management</span></span>

    - <span data-ttu-id="819b9-120">Oprava: Akcia **Nový** v hlavnom formulári **Člen tímu** bola odstránená.</span><span class="sxs-lookup"><span data-stu-id="819b9-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="819b9-121">Oprava: Priradenia zdrojov boli aktualizované pre obchodný vzťah, aby sa zohľadnili chyby nepresného zaokrúhľovania, ktoré vedú k posunu dátumu ukončenia úlohy.</span><span class="sxs-lookup"><span data-stu-id="819b9-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="819b9-122">Oprava: V mriežke úloh sa používateľovi zobrazia príslušné chyby na strane servera.</span><span class="sxs-lookup"><span data-stu-id="819b9-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="819b9-123">Oprava: Meno člena tímu sa teraz v názve úlohy vykreslí namiesto názvu pozície.</span><span class="sxs-lookup"><span data-stu-id="819b9-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="819b9-124">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="819b9-124">Resource Management</span></span>

    - <span data-ttu-id="819b9-125">Oprava: Podrobnosti o požiadavkách na zdroje pre projekty vytvorené zo šablóny teraz používajú kalendár projektu.</span><span class="sxs-lookup"><span data-stu-id="819b9-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="819b9-126">Oprava: Zručnosti a kompetencie sú predvolené od kmeňových dát role po požiadavku na zdroje vytvorenú pre túto rolu.</span><span class="sxs-lookup"><span data-stu-id="819b9-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="819b9-127">Sales</span><span class="sxs-lookup"><span data-stu-id="819b9-127">Sales</span></span>

    - <span data-ttu-id="819b9-128">Oprava: Duplicitné ID objektov nájdené vo formulári **Hlavná zmluva**.</span><span class="sxs-lookup"><span data-stu-id="819b9-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="819b9-129">Oprava: Logika bola aktualizovaná, aby vytvorila viditeľnú kartu **Analýza ponuky**, aby zobrazovala nastavenie metadát karty.</span><span class="sxs-lookup"><span data-stu-id="819b9-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="819b9-130">Oprava: Účtovný dátum v skutočnom zázname teraz prichádza od dátumu vloženia času/výdavkov a nie od dátumu schválenia.</span><span class="sxs-lookup"><span data-stu-id="819b9-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>