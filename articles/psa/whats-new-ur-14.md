---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 14, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 14, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8754f8eace50f1fa5743c5611d94f8c86693ebc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006890"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="5bdc3-103">Aktualizácia pre Project Service Automation, vydanie 14, V3</span><span class="sxs-lookup"><span data-stu-id="5bdc3-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="5bdc3-104">S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="5bdc3-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="5bdc3-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="5bdc3-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="5bdc3-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="5bdc3-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="5bdc3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="5bdc3-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 14.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="5bdc3-110">Táto verzia má číslo zostavenia V3.10.4.21 a je k dispozícii v nasledujúcom harmonograme:</span><span class="sxs-lookup"><span data-stu-id="5bdc3-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="5bdc3-111">**Všeobecná dostupnosť (samoaktualizácia):** Január 2020</span><span class="sxs-lookup"><span data-stu-id="5bdc3-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="5bdc3-112">**Automatická aktualizácia:** Február 2020</span><span class="sxs-lookup"><span data-stu-id="5bdc3-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="5bdc3-113">Aktualizácia vydania 14</span><span class="sxs-lookup"><span data-stu-id="5bdc3-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="5bdc3-114">Vylepšenia</span><span class="sxs-lookup"><span data-stu-id="5bdc3-114">Enhancements</span></span>

- <span data-ttu-id="5bdc3-115">Sales</span><span class="sxs-lookup"><span data-stu-id="5bdc3-115">Sales</span></span>

     - <span data-ttu-id="5bdc3-116">Vlastné hodnoty poľa z **Podrobnosti o riadku cenovej ponuky** sú skopírované do **Podrobnosti o riadku projektovej zmluvy** pri aktualizácii ponuky na **Uzavreté ako využité**.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="5bdc3-117">Potvrdené projekty môžu byť **Uzavreté ako nevyužité**.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="5bdc3-118">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="5bdc3-118">Resource Management</span></span>

     - <span data-ttu-id="5bdc3-119">Pri rozširovaní rezervácií budú používatelia vyzvaní dialógovým oknom s potvrdením, aby zhrnuli výsledky rezervácie a poskytli odkaz na zachovanie rezervácií.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="5bdc3-120">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="5bdc3-120">Bug fixes</span></span>

- <span data-ttu-id="5bdc3-121">Čas a výdavky</span><span class="sxs-lookup"><span data-stu-id="5bdc3-121">Time and Expense</span></span>

     - <span data-ttu-id="5bdc3-122">Oprava: Vylepšené používateľské rozhranie, keď používateľ nevybral žiadne položky, ktoré sa majú opraviť.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="5bdc3-123">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="5bdc3-123">Resource Management</span></span>

     - <span data-ttu-id="5bdc3-124">Oprava: Pri rezervácii zdroja viackrát pretečie názov rezervovateľného zdroja.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="5bdc3-125">Sales</span><span class="sxs-lookup"><span data-stu-id="5bdc3-125">Sales</span></span>

     - <span data-ttu-id="5bdc3-126">Oprava: Celková predajná cena sa nevypočítava, kým používateľ nevloží obstarávaciu cenu pre odhady výdavkov na projekt.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="5bdc3-127">Oprava: Zatvorenie cenovej ponuky ako **Využitá** zlyhá, ak súvisiaca projektová zmluva nie je v stave **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="5bdc3-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]