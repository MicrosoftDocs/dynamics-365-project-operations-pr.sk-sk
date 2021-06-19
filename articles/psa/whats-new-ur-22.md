---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 22, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 22, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 5694aa27afe7618cfca6b27444393634a9686600
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006575"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="88de1-103">Aktualizácia pre Project Service Automation, vydanie 22, V3</span><span class="sxs-lookup"><span data-stu-id="88de1-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="88de1-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="88de1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="88de1-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="88de1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="88de1-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="88de1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="88de1-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="88de1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="88de1-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="88de1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="88de1-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 22.</span><span class="sxs-lookup"><span data-stu-id="88de1-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="88de1-110">Táto verzia má číslo V 3.10.33.48 a v júni 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="88de1-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="88de1-111">Aktualizácia vydania 22</span><span class="sxs-lookup"><span data-stu-id="88de1-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="88de1-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="88de1-112">Bug fixes</span></span>



<span data-ttu-id="88de1-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="88de1-113">**Time and Expense**</span></span>

<span data-ttu-id="88de1-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="88de1-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="88de1-115">**Zadania času** sa po importovaní automaticky nepridajú do plánu zadaní času.</span><span class="sxs-lookup"><span data-stu-id="88de1-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="88de1-116">Nástroj na výber dátumu v mriežke **Zadanie času** nerozpoznáva regionálne nastavenia používateľa.</span><span class="sxs-lookup"><span data-stu-id="88de1-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="88de1-117">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="88de1-117">**Resource Management**</span></span>

<span data-ttu-id="88de1-118">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="88de1-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="88de1-119">V manuálnom režime sa zmeny kontúr **Priradenie zdroja** pri generovaní **Požiadaviek na zdroje** nerozpoznávajú.</span><span class="sxs-lookup"><span data-stu-id="88de1-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="88de1-120">**Požiadavky na zdroje** nepodporujú vlastné stavy požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="88de1-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="88de1-121">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="88de1-121">**Project Management**</span></span>

<span data-ttu-id="88de1-122">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="88de1-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="88de1-123">Dvojité kliknutie na EstimateGridControl nebude mať za následok správnu analýzu čísel holandského formátu.</span><span class="sxs-lookup"><span data-stu-id="88de1-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="88de1-124">Priradené hodiny sa neaktualizujú správne, keď sa priradenia zmenia pomocou doplnku klienta pre osobné počítače Microsoft Project.</span><span class="sxs-lookup"><span data-stu-id="88de1-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="88de1-125">Mriežky na sledovanie projektov a odhady ukazujú nesprávny kód meny predaja, keď je mena zmluvy iná ako mena zákazníka, a organizácia je nakonfigurovaná tak, aby namiesto symbolov meny ukazovala kódy meny.</span><span class="sxs-lookup"><span data-stu-id="88de1-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="88de1-126">Dátum dokončenia pre člena tímu pridá jeden deň, ak je rozvrhnutie pracovnej doby 24 hodín denne.</span><span class="sxs-lookup"><span data-stu-id="88de1-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="88de1-127">V pláne projektu nebude mať pridanie kategórie transakcií do úlohy za následok spustenie automatického ukladania.</span><span class="sxs-lookup"><span data-stu-id="88de1-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="88de1-128">Pri pridaní člena tímu do šablóny projektu sa zobrazí nasledujúca chyba: „Požiadavky na zdroje nemožno priradiť k šablónam projektu“.</span><span class="sxs-lookup"><span data-stu-id="88de1-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="88de1-129">Skript pravidla pre pás s nástrojmi „msdyn.Approval.CanApproveOrReject“ ukazuje chybu časového limitu.</span><span class="sxs-lookup"><span data-stu-id="88de1-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="88de1-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="88de1-130">**Sales**</span></span>

<span data-ttu-id="88de1-131">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="88de1-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="88de1-132">Chybové hlásenie o overení sa nezobrazí, keď je vo vyhľadávaní v cenníku vo formulári/entite „Nový projektový cenník pre cenovú ponuku“ vybratý Cenník obstarávacích cien.</span><span class="sxs-lookup"><span data-stu-id="88de1-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="88de1-133">Uzatvorenie cenovej ponuky ako získanej nemá za následok presun na vytvorenú zmluvu, ak je BPF pripojená k cenovej ponuke v záverečnej etape.</span><span class="sxs-lookup"><span data-stu-id="88de1-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="88de1-134">Vrátenie položky **Nefakturovaný predaj** je spojené s pôvodnými nákladmi, keď je odvolané zadanie času.</span><span class="sxs-lookup"><span data-stu-id="88de1-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="88de1-135">Po výbere tlačidla **Potvrdiť** sa stav faktúry nezmení na **Potvrdená**, pokiaľ sa faktúra neobnoví.</span><span class="sxs-lookup"><span data-stu-id="88de1-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]