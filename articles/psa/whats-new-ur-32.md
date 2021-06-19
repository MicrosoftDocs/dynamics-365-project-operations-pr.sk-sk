---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 32, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 32, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129685"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="451c4-103">Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 32, V3</span><span class="sxs-lookup"><span data-stu-id="451c4-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="451c4-104">S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="451c4-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="451c4-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="451c4-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="451c4-106">Je kompatibilná s verziou Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="451c4-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="451c4-107">Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="451c4-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="451c4-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="451c4-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="451c4-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 32.</span><span class="sxs-lookup"><span data-stu-id="451c4-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="451c4-110">Táto verzia má číslo V3.10.53.108 a je všeobecne dostupná prostredníctvom automatickej aktualizácie od júna 2021.</span><span class="sxs-lookup"><span data-stu-id="451c4-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="451c4-111">Aktualizácia vydania 32</span><span class="sxs-lookup"><span data-stu-id="451c4-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="451c4-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="451c4-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="451c4-113">Všeobecné</span><span class="sxs-lookup"><span data-stu-id="451c4-113">General</span></span>

- <span data-ttu-id="451c4-114">Ak hlavná aktualizácia zlyhá, mali by sa zablokovať iba hlavné vstupné body aplikácie, aby sa zabezpečilo, že zdieľané entity sú stále prístupné.</span><span class="sxs-lookup"><span data-stu-id="451c4-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="451c4-115">Čas a výdavky</span><span class="sxs-lookup"><span data-stu-id="451c4-115">Time and Expense</span></span>

<span data-ttu-id="451c4-116">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="451c4-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="451c4-117">**TimeEntriesImportFromResourceAssignment** neuchováva čas začiatku a konca pre časť krivky priradenia zdrojov.</span><span class="sxs-lookup"><span data-stu-id="451c4-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="451c4-118">Keď vyberiete možnosť **Otvoriť záznam** v mriežke **Časový záznam**, môže vám to zabrániť vo výbere ďalších formulárov.</span><span class="sxs-lookup"><span data-stu-id="451c4-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="451c4-119">Počas importu priradení k časovým záznamom by dotaz na kód klienta mohol vygenerovať dlhú adresu URL, ktorá spôsobí zlyhanie dotazu.</span><span class="sxs-lookup"><span data-stu-id="451c4-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="451c4-120">Na mriežke **Časový záznam** po odstránení hodnoty z bunky nezostane pozornosť zameraná na mriežku.</span><span class="sxs-lookup"><span data-stu-id="451c4-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="451c4-121">Tlačidlo **Odmietnuť** bolo odstránené zo zobrazenia **Spracúvanie schválení** v prípade moderných schválení.</span><span class="sxs-lookup"><span data-stu-id="451c4-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="451c4-122">Stabilita a výkon hromadného schválenia časového záznamu sú ovplyvnené blokovaním a nesprávnou manipuláciou s prispôsobeniami, ktoré sa týkajú entity **Časový záznam**.</span><span class="sxs-lookup"><span data-stu-id="451c4-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="451c4-123">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="451c4-123">Project Planning</span></span>

- <span data-ttu-id="451c4-124">Výnimka odkazu na hodnotu null sa vygeneruje, keď aktualizujete projekt, ktorý má v poli **Zmluvná jednotka** hodnotu null.</span><span class="sxs-lookup"><span data-stu-id="451c4-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="451c4-125">**Obnoviť súčty projektu** nesprávne vypočíta zostávajúce náklady a zostávajúce predaje v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="451c4-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="451c4-126">Nadbytočné výpočty cien ovplyvňujú výkon, ktorý súvisí s aktualizáciami kriviek priradenia zdrojov.</span><span class="sxs-lookup"><span data-stu-id="451c4-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="451c4-127">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="451c4-127">Resource Management</span></span>

<span data-ttu-id="451c4-128">Nasledujúci problém bol opravený:</span><span class="sxs-lookup"><span data-stu-id="451c4-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="451c4-129">Ak je kapacita kalendára rezervovateľného zdroja viac ako 1, Project Service Automation nesprávne rozpozná kapacitu ako 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="451c4-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="451c4-130">Preto sa v zobrazení plánu objaví nekonečná slučka.</span><span class="sxs-lookup"><span data-stu-id="451c4-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="451c4-131">Predaj</span><span class="sxs-lookup"><span data-stu-id="451c4-131">Sales</span></span>

<span data-ttu-id="451c4-132">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="451c4-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="451c4-133">Keď sa vytvorí záznam v účtovnom denníku, ktorý má vlastný typ transakcie, dôjde k nasledujúcej výnimke odkazu na hodnotu null: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType (TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="451c4-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="451c4-134">Roly a kategórie, ktoré sú neaktívne ešte pred skopírovaním cenovej ponuky, by sa nemali pridávať do zúčtovateľných rolí a kategórií v rámci novoskopírovanej cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="451c4-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="451c4-135">Dátum dokumentu a dátum zaúčtovania nie sú zosúladené s dátumom začiatku uvedeným v riadku faktúry, ktorý je vytvorený priamo z konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="451c4-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="451c4-136">Výnimky odkazu na hodnotu null sa generujú v scenároch, ktoré súvisia s deaktiváciou rolí a kategórií pred skopírovaním cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="451c4-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="451c4-137">Akcia **Aktualizovať ceny** na stránke **Projekty** neaktualizuje odhady výdavkov a odhady materiálov.</span><span class="sxs-lookup"><span data-stu-id="451c4-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
