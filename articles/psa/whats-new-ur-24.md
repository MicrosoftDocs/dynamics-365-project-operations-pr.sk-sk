---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 24, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 24, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 956dcd2a06fad1eec488ad81bec2de4bd0550e82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948934"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="8be34-103">Aktualizácia pre Project Service Automation, vydanie 24, V3</span><span class="sxs-lookup"><span data-stu-id="8be34-103">Project Service Automation Update Release 24, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="8be34-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="8be34-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="8be34-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="8be34-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="8be34-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="8be34-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="8be34-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="8be34-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="8be34-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="8be34-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="8be34-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 24.</span><span class="sxs-lookup"><span data-stu-id="8be34-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="8be34-110">Táto verzia má číslo V 3.10.42.43 a vo všeobecnosti je k dispozícii prostredníctvom samostatnej aktualizácie z októbra 2020.</span><span class="sxs-lookup"><span data-stu-id="8be34-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="8be34-111">Aktualizácia vydania 24</span><span class="sxs-lookup"><span data-stu-id="8be34-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="8be34-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="8be34-112">Bug fixes</span></span>

<span data-ttu-id="8be34-113">**Sales**</span><span class="sxs-lookup"><span data-stu-id="8be34-113">**Sales**</span></span>

<span data-ttu-id="8be34-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="8be34-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="8be34-115">Problém pri nastavovaní predvoleného cenníka produktov.</span><span class="sxs-lookup"><span data-stu-id="8be34-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="8be34-116">Výkon využitia cenovej ponuky je pomalý kvôli kopírovaniu vložených cenníkov a záznamov cien rolí.</span><span class="sxs-lookup"><span data-stu-id="8be34-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="8be34-117">**Projektová zmluva/Centrum predaja** > **Položka skupiny produktov/Počet riadkov objednávky** sa automaticky zaokrúhľuje na najbližšie celé číslo.</span><span class="sxs-lookup"><span data-stu-id="8be34-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="8be34-118">Povýšenie na systémové oprávnenia pri čítaní denníkov.</span><span class="sxs-lookup"><span data-stu-id="8be34-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="8be34-119">Skopírujte polia adresy zákazníka **address1_freighttermscode** a **address1_shippingmethodcode** na cenovú ponuku/objednávku.</span><span class="sxs-lookup"><span data-stu-id="8be34-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="8be34-120">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="8be34-120">**Time and Expense**</span></span>

<span data-ttu-id="8be34-121">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="8be34-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="8be34-122">**Mriežka časového vstupu** nepodporuje správanie času položky **Iba dátum**.</span><span class="sxs-lookup"><span data-stu-id="8be34-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="8be34-123">**Časový vstup** sa automaticky neobnovuje.</span><span class="sxs-lookup"><span data-stu-id="8be34-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="8be34-124">Vyžaduje sa manuálne obnovenie.</span><span class="sxs-lookup"><span data-stu-id="8be34-124">A manual refresh is required.</span></span>
- <span data-ttu-id="8be34-125">Nie je možné importovať časové vstupy z priradenia, keď je v priradeniach zdroja prestávka (0 hodín).</span><span class="sxs-lookup"><span data-stu-id="8be34-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="8be34-126">Pri vytváraní časového záznamu nastavte začiatok na rovnakú hodnotu ako **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="8be34-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="8be34-127">Znova povoľte hromadné úpravy časového vstupu.</span><span class="sxs-lookup"><span data-stu-id="8be34-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="8be34-128">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="8be34-128">**Resource Management**</span></span>

<span data-ttu-id="8be34-129">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="8be34-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="8be34-130">Pokus o aktualizáciu stavu rezervácie počas dňa bez požiadavky vyvolá výnimku s nulovými referenčnými hodnotami.</span><span class="sxs-lookup"><span data-stu-id="8be34-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="8be34-131">Chyba pri načítavaní súboru **Zobrazenie vyrovnania**.</span><span class="sxs-lookup"><span data-stu-id="8be34-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="8be34-132">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="8be34-132">**Project Management**</span></span>

<span data-ttu-id="8be34-133">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="8be34-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="8be34-134">V časti **Plán projektu** sa pri zmene z položky **Manuálny** na **Automatický** nedokončuje automatické ukladanie.</span><span class="sxs-lookup"><span data-stu-id="8be34-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="8be34-135">Náklady by sa nemali počítať smerom k odchýlke v **mriežke sledovania projektu**.</span><span class="sxs-lookup"><span data-stu-id="8be34-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="8be34-136">Nekonzistentné správanie pre stĺpce **Značka odhadov** počas načítavania v porovnaní so zmenou typu **Časová fáza**.</span><span class="sxs-lookup"><span data-stu-id="8be34-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="8be34-137">Skutočné náklady na projekt nemusia reflektovať celkové hodnoty z časti **Skutočné hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="8be34-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="8be34-138">**Odhadovaný dátum dokončenia** na karte **Zhrnutie** sa nezhoduje s položkou **Plán WBS**.</span><span class="sxs-lookup"><span data-stu-id="8be34-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="8be34-139">**Aktualizácia skutočných hodín** pri odsadení nefunguje správne.</span><span class="sxs-lookup"><span data-stu-id="8be34-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="8be34-140">Projektový manažér mimo koreňovej **BU** nemôže vytvoriť projekt.</span><span class="sxs-lookup"><span data-stu-id="8be34-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="8be34-141">Zmeny úlohy alebo kategórie v časti **Odhady výdavkov** sa nezachovávajú.</span><span class="sxs-lookup"><span data-stu-id="8be34-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="8be34-142">**Kópia zmluvy** skopíruje plány faktúr a stav priebehu.</span><span class="sxs-lookup"><span data-stu-id="8be34-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="8be34-143">Tlačidlo **Obnoviť skutočné hodnoty** nesprávne vypočítava súhrnné úlohy.</span><span class="sxs-lookup"><span data-stu-id="8be34-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="8be34-144">Doplnok Microsoft Project: Oprava nulovej referenčnej chyby v prípade, ak má ktorýkoľvek člen tímu prázdnu zdrojovú jednotku.</span><span class="sxs-lookup"><span data-stu-id="8be34-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]