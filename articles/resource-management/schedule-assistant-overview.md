---
title: Prehľad asistenta plánovania
description: Táto téma poskytuje informácie o práci s asistentom plánovania pri rezervácii zdrojov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084220"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="5a7d5-103">Prehľad asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="5a7d5-103">Schedule assistant overview</span></span>

<span data-ttu-id="5a7d5-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="5a7d5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5a7d5-105">Asistent plánovania sa používa na rezerváciu zdrojov na základe požiadaviek definovaných projektovým manažérom.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="5a7d5-106">Asistent plánovania sa pri hľadaní zdroja spolieha na parametre uvedené v požiadavke na zdroj.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="5a7d5-107">Asistent plánovania odporúča zdroje, ktoré zodpovedajú príslušným požiadavkám, ako sú časové okná alebo potrebné zručnosti.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="5a7d5-108">Po identifikácii vhodných zdrojov môže manažér zdrojov alebo projektu rezervovať zdroj pre prácu.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="5a7d5-109">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="5a7d5-109">Prerequisites</span></span>

<span data-ttu-id="5a7d5-110">Asistent plánovania je súčasťou riešenia Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="5a7d5-111">Toto riešenie je zahrnuté a nainštalované spolu s Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="5a7d5-112">Zosúlaďovanie požiadaviek a zdrojov</span><span class="sxs-lookup"><span data-stu-id="5a7d5-112">Matching requirements and resources</span></span>

<span data-ttu-id="5a7d5-113">Vygenerovaná požiadavka na zdroj je založená na podrobnostiach, ako napríklad:</span><span class="sxs-lookup"><span data-stu-id="5a7d5-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="5a7d5-114">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="5a7d5-114">Characteristics</span></span>
-   <span data-ttu-id="5a7d5-115">Roly</span><span class="sxs-lookup"><span data-stu-id="5a7d5-115">Roles</span></span>
-   <span data-ttu-id="5a7d5-116">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="5a7d5-116">Business units</span></span>
-   <span data-ttu-id="5a7d5-117">Predvoľby zdrojov</span><span class="sxs-lookup"><span data-stu-id="5a7d5-117">Resource preferences</span></span>
-   <span data-ttu-id="5a7d5-118">Obrysy úsilia</span><span class="sxs-lookup"><span data-stu-id="5a7d5-118">Effort contours</span></span>
-   <span data-ttu-id="5a7d5-119">Časové pásmo</span><span class="sxs-lookup"><span data-stu-id="5a7d5-119">Time zone</span></span>

<span data-ttu-id="5a7d5-120">Asistent plánovania používa tieto podrobnosti na filtrovanie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="5a7d5-121">Spustite asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="5a7d5-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="5a7d5-122">Existujú dva spôsoby spustenia asistenta plánovania.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="5a7d5-123">Ak používate hybridný režim, v mriežke člena tímu môžete vybrať ľubovoľného člena tímu s nesplnenou požiadavkou na zdroje a potom vybrať možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="5a7d5-124">Ak používate centrálny režim, správca zdrojov vyhľadá a vyberie zdroj.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="5a7d5-125">Filtre asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="5a7d5-125">Schedule assistant filters</span></span>

<span data-ttu-id="5a7d5-126">Po spustení asistenta plánovania sa podrobnosti z požiadavky na zdroj zobrazia ako filtrované hodnoty na ľavej table.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="5a7d5-127">Správca zdrojov alebo projektový manažér môže doladiť výsledky úpravou filtrov tak, aby vyhovovali potrebám plánovania.</span><span class="sxs-lookup"><span data-stu-id="5a7d5-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="5a7d5-128">Na table filtra sú zobrazené možnosti súvisiace s prácou, vrátane:</span><span class="sxs-lookup"><span data-stu-id="5a7d5-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="5a7d5-129">Začiatok a koniec práce</span><span class="sxs-lookup"><span data-stu-id="5a7d5-129">Work start and end</span></span>
-   <span data-ttu-id="5a7d5-130">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="5a7d5-130">Characteristics</span></span>
-   <span data-ttu-id="5a7d5-131">Roly</span><span class="sxs-lookup"><span data-stu-id="5a7d5-131">Roles</span></span>
-   <span data-ttu-id="5a7d5-132">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="5a7d5-132">Organizational units</span></span>
-   <span data-ttu-id="5a7d5-133">Spoločnosť zaisťujúca zdroje</span><span class="sxs-lookup"><span data-stu-id="5a7d5-133">Resourcing company</span></span>
-   <span data-ttu-id="5a7d5-134">Typy zdrojov</span><span class="sxs-lookup"><span data-stu-id="5a7d5-134">Resource types</span></span>
-   <span data-ttu-id="5a7d5-135">Preferované zdroje</span><span class="sxs-lookup"><span data-stu-id="5a7d5-135">Preferred resources</span></span>
