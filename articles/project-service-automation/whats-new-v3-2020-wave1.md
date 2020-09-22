---
title: Čo je nové alebo zmenené v Project Service Automation verzia 3.x, vlna 1 2020
description: Táto téma poskytuje informácie o tom, čo je nové a zmenené v Project Service Automation verzia 3, vlna 1 2020.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755581"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="4c90b-103">Čo je nové alebo zmenené v Project Service Automation verzia 3, vlna 1 2020</span><span class="sxs-lookup"><span data-stu-id="4c90b-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="4c90b-104">Táto téma zdôrazňuje kľúčové aspekty modernizácie pri prechode na najnovšie vydanie Project Service Automation (PSA), verzia 3.x, vlna 1 2020.</span><span class="sxs-lookup"><span data-stu-id="4c90b-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="4c90b-105">Zadanie času</span><span class="sxs-lookup"><span data-stu-id="4c90b-105">Time entry</span></span>
<span data-ttu-id="4c90b-106">Rozhranie zadávania času bolo rozšírené, aby poskytovalo možnosti na vloženie časového vstupu do viacerých scenárov zákazníkov.</span><span class="sxs-lookup"><span data-stu-id="4c90b-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="4c90b-107">Zahŕňa to možnosť pridávať typy položiek, ktoré teraz riadia špecifické správanie na základe názvu schémy poľa **Nastavenia zadania času**, zobrazené ako **Zdroj času**.</span><span class="sxs-lookup"><span data-stu-id="4c90b-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="4c90b-108">Informácie o inovácii</span><span class="sxs-lookup"><span data-stu-id="4c90b-108">Upgrade consideration</span></span>
<span data-ttu-id="4c90b-109">Na podporu tejto funkcie boli roly v rámci PSA aktualizované tak, aby obsahovali nové oprávnenia.</span><span class="sxs-lookup"><span data-stu-id="4c90b-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="4c90b-110">Tieto oprávnenia poskytujú prístup na čítanie novej entity, **Nastavenia zadania času**.</span><span class="sxs-lookup"><span data-stu-id="4c90b-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="4c90b-111">Používatelia, ktorí požadujú možnosť zaznamenávania času, by mali mať pridelenú rolu používateľa **Používateľ zadania času** okrem existujúcich rol.</span><span class="sxs-lookup"><span data-stu-id="4c90b-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="4c90b-112">Táto rola zahŕňa novú funkčnosť a zaisťuje, aby zadávanie času naďalej fungovalo.</span><span class="sxs-lookup"><span data-stu-id="4c90b-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="4c90b-113">Aktuálne rozšírené zmeny zadávania času</span><span class="sxs-lookup"><span data-stu-id="4c90b-113">Currently extended time entry changes</span></span>
<span data-ttu-id="4c90b-114">Aby sa minimalizoval vplyv zadávania času na súčasných používateľov, je táto zmena roly jedinou základnou požiadavkou potrebnou na pokračovanie vo využívaní zadávania času.</span><span class="sxs-lookup"><span data-stu-id="4c90b-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="4c90b-115">Ak ste vytvorili vlastné zobrazenia alebo oddelené rozhrania so zadávaním času, musíte nastaviť polia **Nastavenie zadania času** na správnu hodnotu PSA.</span><span class="sxs-lookup"><span data-stu-id="4c90b-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
