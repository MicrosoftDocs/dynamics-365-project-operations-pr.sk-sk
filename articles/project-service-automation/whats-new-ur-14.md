---
title: Čo je nové v aktualizácii Project Service Automation, vydanie 14, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 14, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755584"
---
# <a name="project-service-automation-v3-update-release-14"></a><span data-ttu-id="937a7-103">Aktualizácia Project Service Automation V3, vydanie 14</span><span class="sxs-lookup"><span data-stu-id="937a7-103">Project Service Automation V3, Update Release 14</span></span>
<span data-ttu-id="937a7-104">S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="937a7-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="937a7-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="937a7-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="937a7-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="937a7-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="937a7-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="937a7-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="937a7-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="937a7-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="937a7-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 14.</span><span class="sxs-lookup"><span data-stu-id="937a7-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="937a7-110">Táto verzia má číslo zostavenia V3.10.4.21 a je k dispozícii v nasledujúcom harmonograme:</span><span class="sxs-lookup"><span data-stu-id="937a7-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="937a7-111">**Všeobecná dostupnosť (samoaktualizácia):** Január 2020</span><span class="sxs-lookup"><span data-stu-id="937a7-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="937a7-112">**Automatická aktualizácia:** Február 2020</span><span class="sxs-lookup"><span data-stu-id="937a7-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="937a7-113">Aktualizácia vydania 14</span><span class="sxs-lookup"><span data-stu-id="937a7-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="937a7-114">Vylepšenia</span><span class="sxs-lookup"><span data-stu-id="937a7-114">Enhancements</span></span>

- <span data-ttu-id="937a7-115">Sales</span><span class="sxs-lookup"><span data-stu-id="937a7-115">Sales</span></span>

     - <span data-ttu-id="937a7-116">Vlastné hodnoty poľa z **Podrobnosti o riadku cenovej ponuky** sú skopírované do **Podrobnosti o riadku projektovej zmluvy** pri aktualizácii ponuky na **Uzavreté ako využité**.</span><span class="sxs-lookup"><span data-stu-id="937a7-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="937a7-117">Potvrdené projekty môžu byť **Uzavreté ako nevyužité**.</span><span class="sxs-lookup"><span data-stu-id="937a7-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="937a7-118">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="937a7-118">Resource Management</span></span>

     - <span data-ttu-id="937a7-119">Pri rozširovaní rezervácií budú používatelia vyzvaní dialógovým oknom s potvrdením, aby zhrnuli výsledky rezervácie a poskytli odkaz na zachovanie rezervácií.</span><span class="sxs-lookup"><span data-stu-id="937a7-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="937a7-120">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="937a7-120">Bug fixes</span></span>

- <span data-ttu-id="937a7-121">Čas a výdavky</span><span class="sxs-lookup"><span data-stu-id="937a7-121">Time and Expense</span></span>

     - <span data-ttu-id="937a7-122">Oprava: Vylepšené používateľské rozhranie, keď používateľ nevybral žiadne položky, ktoré sa majú opraviť.</span><span class="sxs-lookup"><span data-stu-id="937a7-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="937a7-123">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="937a7-123">Resource Management</span></span>

     - <span data-ttu-id="937a7-124">Oprava: Pri rezervácii zdroja viackrát pretečie názov rezervovateľného zdroja.</span><span class="sxs-lookup"><span data-stu-id="937a7-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="937a7-125">Sales</span><span class="sxs-lookup"><span data-stu-id="937a7-125">Sales</span></span>

     - <span data-ttu-id="937a7-126">Oprava: Celková predajná cena sa nevypočítava, kým používateľ nevloží obstarávaciu cenu pre odhady výdavkov na projekt.</span><span class="sxs-lookup"><span data-stu-id="937a7-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="937a7-127">Oprava: Zatvorenie cenovej ponuky ako **Využitá** zlyhá, ak súvisiaca projektová zmluva nie je v stave **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="937a7-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>

