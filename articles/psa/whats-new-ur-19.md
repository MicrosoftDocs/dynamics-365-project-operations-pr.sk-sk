---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 19, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 19, V3
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: ecc923cccfad21985025ab9d8006aaff16afc25f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084317"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="4d15a-103">Aktualizácia pre Project Service Automation, vydanie 19, V3</span><span class="sxs-lookup"><span data-stu-id="4d15a-103">Project Service Automation Update Release 19, V3</span></span>

<span data-ttu-id="4d15a-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="4d15a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4d15a-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="4d15a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4d15a-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="4d15a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4d15a-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="4d15a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4d15a-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4d15a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4d15a-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 19.</span><span class="sxs-lookup"><span data-stu-id="4d15a-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="4d15a-110">Táto verzia má číslo V3.10.30.41 a v máji 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="4d15a-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="4d15a-111">Aktualizácia vydania 19</span><span class="sxs-lookup"><span data-stu-id="4d15a-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4d15a-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="4d15a-112">Bug fixes</span></span>

<span data-ttu-id="4d15a-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="4d15a-113">**Time and Expense**</span></span>

<span data-ttu-id="4d15a-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="4d15a-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="4d15a-115">Chyby odvodené z importov zadania času sa nezobrazujú správne.</span><span class="sxs-lookup"><span data-stu-id="4d15a-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="4d15a-116">Mriežka zadania času nepodporuje správanie poľa **Iba dátum**.</span><span class="sxs-lookup"><span data-stu-id="4d15a-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="4d15a-117">Zdroje projektu nedokážu vytvoriť výdavok v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="4d15a-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="4d15a-118">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="4d15a-118">**Project Management**</span></span>

<span data-ttu-id="4d15a-119">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="4d15a-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="4d15a-120">Podriadená úloha druhej úrovne spôsobuje nesprávny odhad úsilia počas odhadu pri dokončení (EAC).</span><span class="sxs-lookup"><span data-stu-id="4d15a-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="4d15a-121">**Sales**</span><span class="sxs-lookup"><span data-stu-id="4d15a-121">**Sales**</span></span>

<span data-ttu-id="4d15a-122">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="4d15a-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="4d15a-123">Akcia **Prepočítať** nefunguje s podrobnosťami v riadku zmluvy pre výdavok alebo s podrobnosťami v riadku pre cenovú ponuku.</span><span class="sxs-lookup"><span data-stu-id="4d15a-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="4d15a-124">Pred odhad výdavkov chýba pole **Aktualizovať ceny**.</span><span class="sxs-lookup"><span data-stu-id="4d15a-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="4d15a-125">Zákazníci si na stránke **Projektová zmluva** nemôžu vybrať vlastné dôvody stavu zmluvy.</span><span class="sxs-lookup"><span data-stu-id="4d15a-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="4d15a-126">Pri vytváraní vlastného cenníka z cenovej ponuky zaznamenávajú zákazníci zhoršený výkon.</span><span class="sxs-lookup"><span data-stu-id="4d15a-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="4d15a-127">Zákazníci sa stretávajú s nekonzistentnosťou pri predvolených nastaveniach **jednotky** na stránke **Podrobnosti o riadku cenovej ponuky** a **Podrobnosti o riadku zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="4d15a-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="4d15a-128">Pridávanie položiek z kategórie nefakturovateľných transakcií do fakturovateľného riadku zmluvy nerešpektuje typ fakturácie **Nefakturovateľné** v rámci kategórie transakcií.</span><span class="sxs-lookup"><span data-stu-id="4d15a-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="4d15a-129">Novo pridané roly a kategórie nemôžu zákazníci použiť v rámci starších vytvorených zmlúv.</span><span class="sxs-lookup"><span data-stu-id="4d15a-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="4d15a-130">Zákazníci zaznamenávajú zhoršený výkon pri zbytočnom načítaní v PreValidateProjectTeamMemberUpdate.cs</span><span class="sxs-lookup"><span data-stu-id="4d15a-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="4d15a-131">Roly nastavené v zozname **Kategórie zdrojov** ako nefakturovateľné by sa mali pridať na kartu **Fakturovateľné roly** v riadku zmluvy projektu ako **Nefakturovateľné**.</span><span class="sxs-lookup"><span data-stu-id="4d15a-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="4d15a-132">Pri vytváraní projektu môžu zákazníci zaznamenať zhoršený výkon, pretože **GetBookableResourceIdFromUser** načíta všetky stĺpce rezervovateľných zdrojov namiesto výhradne primárneho ID.</span><span class="sxs-lookup"><span data-stu-id="4d15a-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="4d15a-133">Entita **TransactionType** nemá doplnok aktualizácie pred overením, ktorý zabraňuje vstupu používateľov do **Jednotiek** a **Jednotkových skupín** , ktoré nie sú platné pre typy transakcií.</span><span class="sxs-lookup"><span data-stu-id="4d15a-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="4d15a-134">Krok **Odstrániť** nefunguje pri importe zadania času.</span><span class="sxs-lookup"><span data-stu-id="4d15a-134">The **Remove** step does not work for time entry import.</span></span>
