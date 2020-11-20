---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 20, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 20, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ef24c20f3fa520b25a14773a15363a0f04f98d36
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126772"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="9dcee-103">Aktualizácia pre Project Service Automation, vydanie 20, V3</span><span class="sxs-lookup"><span data-stu-id="9dcee-103">Project Service Automation Update Release 20, V3</span></span>

<span data-ttu-id="9dcee-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="9dcee-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9dcee-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="9dcee-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9dcee-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="9dcee-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9dcee-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="9dcee-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9dcee-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9dcee-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9dcee-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 20.</span><span class="sxs-lookup"><span data-stu-id="9dcee-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="9dcee-110">Táto verzia má číslo V 3.10.31.37 a v júni 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="9dcee-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="9dcee-111">Aktualizácia vydania 20</span><span class="sxs-lookup"><span data-stu-id="9dcee-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9dcee-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="9dcee-112">Bug fixes</span></span>

<span data-ttu-id="9dcee-113">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="9dcee-113">**Project Management**</span></span>

<span data-ttu-id="9dcee-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="9dcee-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9dcee-115">Import členov projektového tímu s metódou pridelenia, ktorý si vyžaduje hodiny, vedie k nejasnému chybovému hláseniu, keď je uvedených nula hodín.</span><span class="sxs-lookup"><span data-stu-id="9dcee-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="9dcee-116">Používatelia uvidia nesprávnu chybu po zadaní maximálneho počtu znakov do poľa **Opis** pri projektovej úlohe.</span><span class="sxs-lookup"><span data-stu-id="9dcee-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="9dcee-117">Stránka **Stiahnutie doplnku Microsoft Dynamics 365 Project Service Automation** presmeruje na stránku sťahovania v angličtine, ak má používateľ nastavenia jazyka nastavené na japončinu.</span><span class="sxs-lookup"><span data-stu-id="9dcee-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="9dcee-118">Ak sa vyskytne chyba servera, niekedy sa zachová označenie synchronizácie na karte **Plán** vo formulári **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="9dcee-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="9dcee-119">Po zmene úlohy sa na server odosielajú redundantné aktualizácie úloh.</span><span class="sxs-lookup"><span data-stu-id="9dcee-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="9dcee-120">**Sales**</span><span class="sxs-lookup"><span data-stu-id="9dcee-120">**Sales**</span></span>

<span data-ttu-id="9dcee-121">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="9dcee-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="9dcee-122">Vo formulári **Zmluva** spôsobí dvojité kliknutie na položku **Vytvoriť faktúru** vytvorenie dvoch faktúr pre jeden skutočný záznam.</span><span class="sxs-lookup"><span data-stu-id="9dcee-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="9dcee-123">V aplikácii Internet Explorer 11 používatelia nemôžu vytvárať záznamy o výdavkoch.</span><span class="sxs-lookup"><span data-stu-id="9dcee-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="9dcee-124">Zrušenie nákladov a zrušenie nevyfakturovaných skutočných predajov nie je prepojené.</span><span class="sxs-lookup"><span data-stu-id="9dcee-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="9dcee-125">Tlačidlo **Obnoviť skutočné hodnoty** vo formulári **Projekt** neobnoví **Skutočný počet hodín úlohy**.</span><span class="sxs-lookup"><span data-stu-id="9dcee-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="9dcee-126">Doplnok **PreValidateProjectTeamMemberCreate** môže vytvoriť duplicitné všeobecné rezervovateľné zdroje, ak je atribút **msdyn_isgenericresourceprojectscoped** nastavený na hodnotu **False**.</span><span class="sxs-lookup"><span data-stu-id="9dcee-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="9dcee-127">**Prepočítať** slúži na vymazanie fakturovateľných nákladov podrobností o riadku cenovej ponuky na základe produktu a podrobností o riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="9dcee-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="9dcee-128">V určitých situáciách ukazuje doplnok **PostEstimateLineUpdate** chybu nulovej referenčnej výnimky.</span><span class="sxs-lookup"><span data-stu-id="9dcee-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="9dcee-129">Trvanie časovej fázy na **Grafe analýzy ziskovosti** sa nezhoduje s trvaním nákladov v podrobnostiach o riadku cenovej ponuky s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="9dcee-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="9dcee-130">Jednotka a jednotková skupina nemajú správnu predvolenú hodnotu pre kategórie výdavkov vo formulároch **Podrobnosti o riadku zmluvy** a **Podrobnosti o riadku cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="9dcee-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="9dcee-131">Zoznamy **Obstarávacej ceny organizačnej jednotky** umožňujú prekrývanie účinnosti podľa dátumu.</span><span class="sxs-lookup"><span data-stu-id="9dcee-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="9dcee-132">Používatelia nemajú povolené meniť hodnotu **OrgUnit**, keď typ objednávky nie je pracovný, pretože to bude mať za následok chybu nulovej referenčnej výnimky.</span><span class="sxs-lookup"><span data-stu-id="9dcee-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="9dcee-133">Pri pokuse o navigáciu z formulára **Podrobnosti o riadku cenovej ponuky** späť do formulára **Cenová ponuka** sa formulár obnoví a zobrazí sa karta **Zhrnutie**.</span><span class="sxs-lookup"><span data-stu-id="9dcee-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
