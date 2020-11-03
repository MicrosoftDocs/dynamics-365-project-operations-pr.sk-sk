---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 16, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 16, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: f277d23e3fb0517f072e51f6f80f855479ab8189
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084323"
---
# <a name="project-service-automation-update-release-16-v3"></a><span data-ttu-id="7beb5-103">Aktualizácia pre Project Service Automation, vydanie 16, V3</span><span class="sxs-lookup"><span data-stu-id="7beb5-103">Project Service Automation Update Release 16, V3</span></span>

<span data-ttu-id="7beb5-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="7beb5-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="7beb5-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="7beb5-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="7beb5-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="7beb5-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7beb5-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="7beb5-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="7beb5-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia preferovaného riešenia](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="7beb5-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span>
<span data-ttu-id="7beb5-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 16.</span><span class="sxs-lookup"><span data-stu-id="7beb5-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="7beb5-110">Táto verzia má číslo zostavy V3.10.6.34 a je všeobecne dostupná prostredníctvom samoaktualizácie v januári 2020.</span><span class="sxs-lookup"><span data-stu-id="7beb5-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020.</span></span>


## <a name="update-release-16"></a><span data-ttu-id="7beb5-111">Aktualizácia vydania 16</span><span class="sxs-lookup"><span data-stu-id="7beb5-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7beb5-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="7beb5-112">Bug fixes</span></span>

-   <span data-ttu-id="7beb5-113">Čas a výdavky</span><span class="sxs-lookup"><span data-stu-id="7beb5-113">Time and Expense</span></span>

    -   <span data-ttu-id="7beb5-114">Oprava: Používatelia, ktorí sa pokúšajú odoslať vymazané údaje o časoch a výdavkoch na schválenie, teraz dostanú príslušné chybové správy.</span><span class="sxs-lookup"><span data-stu-id="7beb5-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="7beb5-115">Riadenie projektov</span><span class="sxs-lookup"><span data-stu-id="7beb5-115">Project Management</span></span>

    -   <span data-ttu-id="7beb5-116">Oprava: Jednotky zabezpečujúce zdroje definované pre členov tímu v šablónach sa rešpektujú, pričom šablóny sa použijú na nový projekt.</span><span class="sxs-lookup"><span data-stu-id="7beb5-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="7beb5-117">Oprava: Vylepšené spracovanie opätovného pridelenia vlastníctva záznamu.</span><span class="sxs-lookup"><span data-stu-id="7beb5-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="7beb5-118">Oprava: Projekty, ktoré sa práve kopírujú, sa skopírujú až po dokončení všetkých operácií kopírovania.</span><span class="sxs-lookup"><span data-stu-id="7beb5-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="7beb5-119">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="7beb5-119">Resource Management</span></span>

    -   <span data-ttu-id="7beb5-120">Oprava: Rozšírenie rezervácií teraz zvláda krátke trvanie správne a pre predĺžené rezervácie už nevytvára nulové hodiny.</span><span class="sxs-lookup"><span data-stu-id="7beb5-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="7beb5-121">Oprava: Zobrazenie odsúhlasenia sa teraz vykreslí, keď je časové pásmo projektu +5:30 GMT a čas používateľa je iný.</span><span class="sxs-lookup"><span data-stu-id="7beb5-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="7beb5-122">Sales</span><span class="sxs-lookup"><span data-stu-id="7beb5-122">Sales</span></span>

    -   <span data-ttu-id="7beb5-123">Oprava: Keď sa odstráni projekt mapovaný na riadok zmluvy a mapuje sa nový projekt, skutočné záznamy o novom projekte neboli prehodnocované na základe pravidiel fakturácie a stanovovania cien definovaných v riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="7beb5-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="7beb5-124">Toto bolo v tomto vydaní opravené.</span><span class="sxs-lookup"><span data-stu-id="7beb5-124">This has been fixed in this release.</span></span> <span data-ttu-id="7beb5-125">Ceny a skutočné záznamy o novo mapovanom projekte sa zvrátia a znovu sa vytvoria správne na základe cenových a fakturačných pravidiel riadka zmluvy.</span><span class="sxs-lookup"><span data-stu-id="7beb5-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="7beb5-126">Skutočné záznamy nemapovaného projektu sa následne v dôsledku toho prehodnotia a znovu vytvoria.</span><span class="sxs-lookup"><span data-stu-id="7beb5-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="7beb5-127">Oprava: K riadku odhadu bola pridaná ďalšia validácia poľa **Čiastka** , aby sa zabezpečilo, že nulové hodnoty nebudú pretrvávať.</span><span class="sxs-lookup"><span data-stu-id="7beb5-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="7beb5-128">Oprava: Po aktualizácii skutočností v projekte bolo do hlavného formulára projektu pridané tlačidlo obnovenia, ktoré používateľom umožňuje opätovnú synchronizáciu skutočností.</span><span class="sxs-lookup"><span data-stu-id="7beb5-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="7beb5-129">Oprava: Keď používatelia vykonajú inováciu z 2.X na 3.X, budú povolené projekty s hodnotou NULL pre názov projektu.</span><span class="sxs-lookup"><span data-stu-id="7beb5-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

