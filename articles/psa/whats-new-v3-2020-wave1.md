---
title: Čo je nové alebo zmenené v Project Service Automation verzia 3.x, vlna 1 2020
description: Táto téma poskytuje informácie o tom, čo je nové a zmenené v Project Service Automation verzia 3, vlna 1 2020.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: f77c881c62428e423e0dab66eb34b033628a2a1b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996855"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="f4f70-103">Čo je nové alebo zmenené v Project Service Automation verzia 3, vlna 1 2020</span><span class="sxs-lookup"><span data-stu-id="f4f70-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f4f70-104">Táto téma zdôrazňuje kľúčové aspekty modernizácie pri prechode na najnovšie vydanie Project Service Automation (PSA), verzia 3.x, vlna 1 2020.</span><span class="sxs-lookup"><span data-stu-id="f4f70-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="f4f70-105">Zadanie času</span><span class="sxs-lookup"><span data-stu-id="f4f70-105">Time entry</span></span>
<span data-ttu-id="f4f70-106">Rozhranie zadávania času bolo rozšírené, aby poskytovalo možnosti na vloženie časového vstupu do viacerých scenárov zákazníkov.</span><span class="sxs-lookup"><span data-stu-id="f4f70-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="f4f70-107">Zahŕňa to možnosť pridávať typy položiek, ktoré teraz riadia špecifické správanie na základe názvu schémy poľa **Nastavenia zadania času**, zobrazené ako **Zdroj času**.</span><span class="sxs-lookup"><span data-stu-id="f4f70-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="f4f70-108">Na podporu tejto funkcie bolo pridané nové riešenie s názvom Čas, výdavky, štatúty a schválenia (TESA).</span><span class="sxs-lookup"><span data-stu-id="f4f70-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="f4f70-109">Informácie o inovácii</span><span class="sxs-lookup"><span data-stu-id="f4f70-109">Upgrade consideration</span></span>
<span data-ttu-id="f4f70-110">Na podporu tejto funkcie boli roly v rámci PSA aktualizované tak, aby obsahovali nové oprávnenia.</span><span class="sxs-lookup"><span data-stu-id="f4f70-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="f4f70-111">Tieto oprávnenia poskytujú prístup na čítanie novej entity, **Nastavenia zadania času**.</span><span class="sxs-lookup"><span data-stu-id="f4f70-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="f4f70-112">Používatelia, ktorí požadujú možnosť zaznamenávania času, by mali mať pridelenú rolu používateľa **Používateľ zadania času** okrem existujúcich rol.</span><span class="sxs-lookup"><span data-stu-id="f4f70-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="f4f70-113">Táto rola zahŕňa novú funkčnosť a zaisťuje, aby zadávanie času naďalej fungovalo.</span><span class="sxs-lookup"><span data-stu-id="f4f70-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="f4f70-114">Ak máte okrem toho ešte vlastné moduly aplikácií, ktoré zahŕňajú všetky formuláre pre entitu zadania času, budete musieť z modulu odstrániť **Formulár rýchleho vytvorenia zadaní času TESA**.</span><span class="sxs-lookup"><span data-stu-id="f4f70-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="f4f70-115">Aktuálne rozšírené zmeny zadávania času</span><span class="sxs-lookup"><span data-stu-id="f4f70-115">Currently extended time entry changes</span></span>
<span data-ttu-id="f4f70-116">Aby sa minimalizoval vplyv zadávania času na súčasných používateľov, je táto zmena roly jedinou základnou požiadavkou potrebnou na pokračovanie vo využívaní zadávania času.</span><span class="sxs-lookup"><span data-stu-id="f4f70-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="f4f70-117">Ak ste vytvorili vlastné zobrazenia alebo oddelené rozhrania so zadávaním času, musíte nastaviť polia **Nastavenie zadania času** na správnu hodnotu PSA.</span><span class="sxs-lookup"><span data-stu-id="f4f70-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]