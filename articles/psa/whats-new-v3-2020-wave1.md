---
title: Čo je nové alebo zmenené v Project Service Automation verzia 3.x, vlna 1 2020
description: Táto téma poskytuje informácie o tom, čo je nové a zmenené v Project Service Automation verzia 3, vlna 1 2020.
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 16b51995f863d9ee54172625dacbf081c51c8556
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084310"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="c36d5-103">Čo je nové alebo zmenené v Project Service Automation verzia 3, vlna 1 2020</span><span class="sxs-lookup"><span data-stu-id="c36d5-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="c36d5-104">Táto téma zdôrazňuje kľúčové aspekty modernizácie pri prechode na najnovšie vydanie Project Service Automation (PSA), verzia 3.x, vlna 1 2020.</span><span class="sxs-lookup"><span data-stu-id="c36d5-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="c36d5-105">Zadanie času</span><span class="sxs-lookup"><span data-stu-id="c36d5-105">Time entry</span></span>
<span data-ttu-id="c36d5-106">Rozhranie zadávania času bolo rozšírené, aby poskytovalo možnosti na vloženie časového vstupu do viacerých scenárov zákazníkov.</span><span class="sxs-lookup"><span data-stu-id="c36d5-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="c36d5-107">Zahŕňa to možnosť pridávať typy položiek, ktoré teraz riadia špecifické správanie na základe názvu schémy poľa **Nastavenia zadania času** , zobrazené ako **Zdroj času**.</span><span class="sxs-lookup"><span data-stu-id="c36d5-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings** , displayed as **Time Source**.</span></span> <span data-ttu-id="c36d5-108">Na podporu tejto funkcie bolo pridané nové riešenie s názvom Čas, výdavky, štatúty a schválenia (TESA).</span><span class="sxs-lookup"><span data-stu-id="c36d5-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="c36d5-109">Informácie o inovácii</span><span class="sxs-lookup"><span data-stu-id="c36d5-109">Upgrade consideration</span></span>
<span data-ttu-id="c36d5-110">Na podporu tejto funkcie boli roly v rámci PSA aktualizované tak, aby obsahovali nové oprávnenia.</span><span class="sxs-lookup"><span data-stu-id="c36d5-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="c36d5-111">Tieto oprávnenia poskytujú prístup na čítanie novej entity, **Nastavenia zadania času**.</span><span class="sxs-lookup"><span data-stu-id="c36d5-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="c36d5-112">Používatelia, ktorí požadujú možnosť zaznamenávania času, by mali mať pridelenú rolu používateľa **Používateľ zadania času** okrem existujúcich rol.</span><span class="sxs-lookup"><span data-stu-id="c36d5-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="c36d5-113">Táto rola zahŕňa novú funkčnosť a zaisťuje, aby zadávanie času naďalej fungovalo.</span><span class="sxs-lookup"><span data-stu-id="c36d5-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="c36d5-114">Ak máte okrem toho ešte vlastné moduly aplikácií, ktoré zahŕňajú všetky formuláre pre entitu zadania času, budete musieť z modulu odstrániť **Formulár rýchleho vytvorenia zadaní času TESA**.</span><span class="sxs-lookup"><span data-stu-id="c36d5-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="c36d5-115">Aktuálne rozšírené zmeny zadávania času</span><span class="sxs-lookup"><span data-stu-id="c36d5-115">Currently extended time entry changes</span></span>
<span data-ttu-id="c36d5-116">Aby sa minimalizoval vplyv zadávania času na súčasných používateľov, je táto zmena roly jedinou základnou požiadavkou potrebnou na pokračovanie vo využívaní zadávania času.</span><span class="sxs-lookup"><span data-stu-id="c36d5-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="c36d5-117">Ak ste vytvorili vlastné zobrazenia alebo oddelené rozhrania so zadávaním času, musíte nastaviť polia **Nastavenie zadania času** na správnu hodnotu PSA.</span><span class="sxs-lookup"><span data-stu-id="c36d5-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
