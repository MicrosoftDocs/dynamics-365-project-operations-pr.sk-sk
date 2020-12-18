---
title: Vytváranie šablóny projektu pomocou funkcie kopírovania projektu
description: Táto téma poskytuje informácie o tom, ako vytvoriť šablóny projektu pomocou vlastnej akcie kopírovania projektu.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 22976730ef3c8c22ea028b27a6eb5f14fb88993e
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642427"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="93c20-103">Vytváranie šablóny projektu pomocou funkcie kopírovania projektu</span><span class="sxs-lookup"><span data-stu-id="93c20-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="93c20-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="93c20-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="93c20-105">Dynamics 365 Project Operations podporuje schopnosť kopírovať projekt a vrátiť všetky priradenia späť k všeobecným zdrojom, ktoré zastupujú danú rolu.</span><span class="sxs-lookup"><span data-stu-id="93c20-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="93c20-106">Zákazníci môžu pomocou tejto funkcie zostaviť základné šablóny projektu.</span><span class="sxs-lookup"><span data-stu-id="93c20-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="93c20-107">Keď vyberiete **Kopírovať projekt**, aktualizuje sa stav cieľového projektu.</span><span class="sxs-lookup"><span data-stu-id="93c20-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="93c20-108">Použite **Dôvod stavu** na určenie, kedy je akcia kopírovania dokončená.</span><span class="sxs-lookup"><span data-stu-id="93c20-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="93c20-109">Výberom možnosti **Kopírovať projekt** sa aktualizuje aj počiatočný dátum projektu na aktuálny počiatočný dátum, ak sa v entite cieľového projektu nezistí žiadny cieľový dátum.</span><span class="sxs-lookup"><span data-stu-id="93c20-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="93c20-110">Vlastná akcia kopírovania projektu</span><span class="sxs-lookup"><span data-stu-id="93c20-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="93c20-111">Meno</span><span class="sxs-lookup"><span data-stu-id="93c20-111">Name</span></span> 

<span data-ttu-id="93c20-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="93c20-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="93c20-113">Vstupné parametre</span><span class="sxs-lookup"><span data-stu-id="93c20-113">Input parameters</span></span>
<span data-ttu-id="93c20-114">Existujú tri vstupné parametre:</span><span class="sxs-lookup"><span data-stu-id="93c20-114">There are three input parameters:</span></span>

| <span data-ttu-id="93c20-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="93c20-115">Parameter</span></span>          | <span data-ttu-id="93c20-116">Zadať</span><span class="sxs-lookup"><span data-stu-id="93c20-116">Type</span></span>   | <span data-ttu-id="93c20-117">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="93c20-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="93c20-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="93c20-118">ProjectCopyOption</span></span>  | <span data-ttu-id="93c20-119">String</span><span class="sxs-lookup"><span data-stu-id="93c20-119">String</span></span> | <span data-ttu-id="93c20-120">**{"removeNamedResources":true}** alebo **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="93c20-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="93c20-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="93c20-121">SourceProject</span></span>      | <span data-ttu-id="93c20-122">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="93c20-122">Entity Reference</span></span> | <span data-ttu-id="93c20-123">Zdrojový projekt</span><span class="sxs-lookup"><span data-stu-id="93c20-123">Source Project</span></span> |
| <span data-ttu-id="93c20-124">Cieľ</span><span class="sxs-lookup"><span data-stu-id="93c20-124">Target</span></span>             | <span data-ttu-id="93c20-125">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="93c20-125">Entity Reference</span></span> | <span data-ttu-id="93c20-126">Cieľový projekt</span><span class="sxs-lookup"><span data-stu-id="93c20-126">Target Project</span></span> |


- <span data-ttu-id="93c20-127">**{"clearTeamsAndAssignments":true}**: Predvolené správanie pre Project for Web, ktoré odstráni všetky priradenia a členov tímu.</span><span class="sxs-lookup"><span data-stu-id="93c20-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="93c20-128">**{"removeNamedResources": true}** Predvolené správanie pre Project Operations, ktoré vráti priradenia k všeobecným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="93c20-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="93c20-129">Ďalšie predvolené hodnoty akcií nájdete v časti [Použitie akcií Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="93c20-129">For more defaults on actions, see [Use Web API actions](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="93c20-130">Zadajte polia, ktoré chcete kopírovať</span><span class="sxs-lookup"><span data-stu-id="93c20-130">Specify fields to copy</span></span> 
<span data-ttu-id="93c20-131">Po vyvolaní akcie bude funkcia **Kopírovať projekt** prehľadávať zobrazenie projektu **Kopírovať stĺpce projektu** na určenie, ktoré polia sa majú kopírovať pri kopírovaní projektu.</span><span class="sxs-lookup"><span data-stu-id="93c20-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>
