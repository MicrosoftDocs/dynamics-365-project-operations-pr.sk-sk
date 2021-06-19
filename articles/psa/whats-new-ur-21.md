---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 21, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 21, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002346"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="33737-103">Aktualizácia pre Project Service Automation, vydanie 21, V3</span><span class="sxs-lookup"><span data-stu-id="33737-103">Project Service Automation Update Release 21, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="33737-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="33737-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="33737-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="33737-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="33737-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="33737-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="33737-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="33737-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="33737-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="33737-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="33737-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 21.</span><span class="sxs-lookup"><span data-stu-id="33737-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="33737-110">Táto verzia má číslo V 3.10.32.50 a v júni 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="33737-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="33737-111">Aktualizácia vydania 21</span><span class="sxs-lookup"><span data-stu-id="33737-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="33737-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="33737-112">Bug fixes</span></span>

<span data-ttu-id="33737-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="33737-113">**Time and Expense**</span></span>

<span data-ttu-id="33737-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="33737-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="33737-115">Pri hosťovaní **Ovládacieho prvku mriežky so zadaniami času** v tabuliach táto mriežka nevyužíva celú šírku kontajnera mriežky tabule.</span><span class="sxs-lookup"><span data-stu-id="33737-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="33737-116">Pokiaľ ide o konkrétne časové pásma, ovládací prvok mriežky **Zadanie času** nezobrazuje záznamy.</span><span class="sxs-lookup"><span data-stu-id="33737-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="33737-117">Zadania času, ktoré sú po 21:00, sa zobrazujú v nesprávny deň.</span><span class="sxs-lookup"><span data-stu-id="33737-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="33737-118">Používatelia nemôžu odosielať výdavky, ak kategória výdavkov **Vyžaduje sa potvrdenie o výdavkoch** nemá žiadnu hodnotu.</span><span class="sxs-lookup"><span data-stu-id="33737-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="33737-119">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="33737-119">**Resource Management**</span></span>

<span data-ttu-id="33737-120">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="33737-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="33737-121">Neaktívne rezervácie sa zobrazujú v zobrazení **Vyrovnanie**.</span><span class="sxs-lookup"><span data-stu-id="33737-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="33737-122">Pri plnení všeobecných požiadaviek na zdroje chýbalo overenie, ktoré by zabezpečilo, že existuje platný stav rezervácie.</span><span class="sxs-lookup"><span data-stu-id="33737-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="33737-123">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="33737-123">**Project Management**</span></span>

<span data-ttu-id="33737-124">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="33737-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="33737-125">Mriežky formulára **Projekt** (**Priradenie zdroja**, **Úloha**, **Vyrovnanie**, **Odhady výdavkov**) sa dajú upravovať, aj keď projekt nie je aktívny.</span><span class="sxs-lookup"><span data-stu-id="33737-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="33737-126">Duplicitní zákazníci sa nemôžu zlúčiť so zákazníkmi, ktorí sú spojení s potvrdenými projektovými zmluvami.</span><span class="sxs-lookup"><span data-stu-id="33737-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="33737-127">Po pridaní zdroja, ktorý nemá platný kalendár, systém nevráti používateľsky prístupné chybové hlásenie.</span><span class="sxs-lookup"><span data-stu-id="33737-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="33737-128">Tlačidlo **Pridať úlohu** na mriežke úloh je povolené, keď je projekt prepojený s **doplnkom Microsoft Project**.</span><span class="sxs-lookup"><span data-stu-id="33737-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="33737-129">Úsilie rastie nekontrolovateľne, keď je úloha s kategóriou priradená k zdroju, pre ktorý je definovaná obstarávacia cena.</span><span class="sxs-lookup"><span data-stu-id="33737-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="33737-130">**Sales**</span><span class="sxs-lookup"><span data-stu-id="33737-130">**Sales**</span></span>

<span data-ttu-id="33737-131">Vykonali sme nasledovné vylepšenia:</span><span class="sxs-lookup"><span data-stu-id="33737-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="33737-132">**Frekvencia fakturácie** a **Začiatok fakturácie** boli presunuté na kartu **Plán fakturácie**.</span><span class="sxs-lookup"><span data-stu-id="33737-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="33737-133">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="33737-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="33737-134">**Celková predajná cena** je nula (0) pre položku **Kategória**, aj keď má **Rola** celkovú predajnú cenu, ktorá nie je nula.</span><span class="sxs-lookup"><span data-stu-id="33737-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="33737-135">Zákazníci nemôžu zmeniť hodnotu poľa **Stav faktúry** na **Pripravené na fakturáciu**, keď iný prispôsobený proces aktualizuje ďalšie pole.</span><span class="sxs-lookup"><span data-stu-id="33737-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="33737-136">Tlačidlo **Obnoviť riadky faktúry** môže vytvoriť viac duplicitných riadkov, ak je opakovane vybrané.</span><span class="sxs-lookup"><span data-stu-id="33737-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="33737-137">Tlačidlo **Aktualizovať ceny** nefunguje na vedľajšej mriežke **Ceny rolí** vo formulári **Rýchle zobrazenie**.</span><span class="sxs-lookup"><span data-stu-id="33737-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="33737-138">Logika **Vyriešenie predajného cenníka** nesprávne spracúva časové pásma, čo vedie k nesprávnemu výberu cenníkov.</span><span class="sxs-lookup"><span data-stu-id="33737-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="33737-139">**Celkové skutočné náklady** projektu môžu byť nepresné o zlomkovú sumu po schválení jedného zadania času.</span><span class="sxs-lookup"><span data-stu-id="33737-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="33737-140">Logika **Vyriešenie ceny** neposkytuje používateľsky prístupné chybové hlásenie, ak **Získaná cena roly** nemá hodnoty v poli **„Primárna jednotka“** a **„Cena v primárnej jednotke“**.</span><span class="sxs-lookup"><span data-stu-id="33737-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]