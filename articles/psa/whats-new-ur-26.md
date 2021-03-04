---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 26, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 26, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 14fcccf5804e5da0926dbc69bdfa040229a7f068
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143577"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="757be-103">Aktualizácia pre Project Service Automation, vydanie 26, V3</span><span class="sxs-lookup"><span data-stu-id="757be-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="757be-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="757be-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="757be-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="757be-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="757be-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="757be-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="757be-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="757be-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="757be-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="757be-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="757be-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 26, V3.</span><span class="sxs-lookup"><span data-stu-id="757be-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="757be-110">Táto verzia má číslo zostavenia V3.10.44.59 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie v decembri 2020.</span><span class="sxs-lookup"><span data-stu-id="757be-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="757be-111">Aktualizácia vydania 26</span><span class="sxs-lookup"><span data-stu-id="757be-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="757be-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="757be-112">Bug fixes</span></span>

<span data-ttu-id="757be-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="757be-113">**Time and Expense**</span></span>

<span data-ttu-id="757be-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="757be-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="757be-115">Používatelia môžu zmeniť úlohu pri zadaní času, ktorý bol schválený/odoslaný.</span><span class="sxs-lookup"><span data-stu-id="757be-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="757be-116">Chyba „Referencia objektu nie je nastavená“ pri ukladaní zadania času.</span><span class="sxs-lookup"><span data-stu-id="757be-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="757be-117">Importom časovej položky z priradení zdrojov sa vytvárajú časové položky s nesprávnymi hodnotami DateTime.</span><span class="sxs-lookup"><span data-stu-id="757be-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="757be-118">Keď sú nainštalované aplikácie Project Service Automation a Field Service, tlačidlo **Nový** sa dvakrát zobrazuje na paneli príkazov pre zadávanie času v aplikácii Field Service.</span><span class="sxs-lookup"><span data-stu-id="757be-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="757be-119">Aktualizácie buniek **Povoliť jednotky** a **Jednotková skupina** v mriežke **Odhady výdavkov** teraz fungujú.</span><span class="sxs-lookup"><span data-stu-id="757be-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="757be-120">Formulár **Aktualizovať Úpravu zadania času** obsahuje **Časovú os**.</span><span class="sxs-lookup"><span data-stu-id="757be-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="757be-121">Schválenie času pre časové údaje nesúvisiace s projektom blokuje systém pri hľadaní roly schvaľovateľa projektu.</span><span class="sxs-lookup"><span data-stu-id="757be-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="757be-122">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="757be-122">**Resource Management**</span></span>

<span data-ttu-id="757be-123">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="757be-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="757be-124">Pridaná validácia v doplnku **PostProjectCreate** na kontrolu primárnej požiadavky pred jej vytvorením.</span><span class="sxs-lookup"><span data-stu-id="757be-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="757be-125">Formulár rýchleho vytvorenia **člena projektového tímu** vyvolá výnimku odkazu na hodnotu null, ak sú polia odstránené z formulára.</span><span class="sxs-lookup"><span data-stu-id="757be-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="757be-126">Generovanie požiadaviek na 12 hodín v priebehu 1 roka zlyhá.</span><span class="sxs-lookup"><span data-stu-id="757be-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="757be-127">Vylepšené chybové hlásenie pri výnimke odkazu na hodnotu null počas vytvárania požiadavky na zdroj.</span><span class="sxs-lookup"><span data-stu-id="757be-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="757be-128">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="757be-128">**Project Management**</span></span>

<span data-ttu-id="757be-129">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="757be-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="757be-130">Vylepšené overovanie adresy s cieľom vylúčiť výnimku odkazu na hodnotu null vygenerovanú v doplnku **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="757be-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="757be-131">Projekty zverejnené doplnkom Microsoft Project pre počítač odstránia nepriradené priradenia.</span><span class="sxs-lookup"><span data-stu-id="757be-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="757be-132">Pridané nové overenie, keď je odkaz na úlohu projektu neplatný z dôvodu výnimky odkazu na hodnotu null v doplnku **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="757be-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="757be-133">Mriežka člena tímu nezobrazuje odlišné priradenia v zázname člena tímu.</span><span class="sxs-lookup"><span data-stu-id="757be-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="757be-134">Pridané nové overovacie a chybové správy z dôvodu výnimky odkazu na hodnotu null v doplnku **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="757be-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="757be-135">**Sales**</span><span class="sxs-lookup"><span data-stu-id="757be-135">**Sales**</span></span>

<span data-ttu-id="757be-136">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="757be-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="757be-137">Pri výbere projektovej riadka v cenovej ponuke alebo zmluve by malo byť tlačidlo **Návrh** viditeľné iba pri výbere produktového riadka priradeného k existujúcemu produktu.</span><span class="sxs-lookup"><span data-stu-id="757be-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="757be-138">Rozdeľte oprávnenie **Vytvoriť_Produkt** z oprávnenia **Vytvoriť_ProjektováZmluva**.</span><span class="sxs-lookup"><span data-stu-id="757be-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="757be-139">Vymazanie riadka faktúry spôsobí, že dôjde k zlyhaniu odkazu na hodnotu null v **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="757be-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>
