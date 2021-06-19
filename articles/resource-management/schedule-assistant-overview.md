---
title: Prehľad asistenta plánovania
description: Táto téma poskytuje informácie o práci s asistentom plánovania pri rezervácii zdrojov.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d58f5f45ca54691b6e736dee5aab7b273a8e042
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014135"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="6a60d-103">Prehľad asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="6a60d-103">Schedule assistant overview</span></span>

<span data-ttu-id="6a60d-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="6a60d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6a60d-105">Asistent plánovania sa používa na rezerváciu zdrojov na základe požiadaviek definovaných projektovým manažérom.</span><span class="sxs-lookup"><span data-stu-id="6a60d-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="6a60d-106">Asistent plánovania sa pri hľadaní zdroja spolieha na parametre uvedené v požiadavke na zdroj.</span><span class="sxs-lookup"><span data-stu-id="6a60d-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="6a60d-107">Asistent plánovania odporúča zdroje, ktoré zodpovedajú príslušným požiadavkám, ako sú časové okná alebo potrebné zručnosti.</span><span class="sxs-lookup"><span data-stu-id="6a60d-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="6a60d-108">Po identifikácii vhodných zdrojov môže manažér zdrojov alebo projektu rezervovať zdroj pre prácu.</span><span class="sxs-lookup"><span data-stu-id="6a60d-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="6a60d-109">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="6a60d-109">Prerequisites</span></span>

<span data-ttu-id="6a60d-110">Asistent plánovania je súčasťou riešenia Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="6a60d-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="6a60d-111">Toto riešenie je zahrnuté a nainštalované do Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="6a60d-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="6a60d-112">Zosúlaďovanie požiadaviek a zdrojov</span><span class="sxs-lookup"><span data-stu-id="6a60d-112">Matching requirements and resources</span></span>

<span data-ttu-id="6a60d-113">Vygenerovaná požiadavka na zdroj je založená na podrobnostiach, ako napríklad:</span><span class="sxs-lookup"><span data-stu-id="6a60d-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="6a60d-114">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="6a60d-114">Characteristics</span></span>
-   <span data-ttu-id="6a60d-115">Roly</span><span class="sxs-lookup"><span data-stu-id="6a60d-115">Roles</span></span>
-   <span data-ttu-id="6a60d-116">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="6a60d-116">Business units</span></span>
-   <span data-ttu-id="6a60d-117">Predvoľby zdrojov</span><span class="sxs-lookup"><span data-stu-id="6a60d-117">Resource preferences</span></span>
-   <span data-ttu-id="6a60d-118">Obrysy úsilia</span><span class="sxs-lookup"><span data-stu-id="6a60d-118">Effort contours</span></span>
-   <span data-ttu-id="6a60d-119">Časové pásmo</span><span class="sxs-lookup"><span data-stu-id="6a60d-119">Time zone</span></span>

<span data-ttu-id="6a60d-120">Asistent plánovania používa tieto podrobnosti na filtrovanie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="6a60d-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="6a60d-121">Spustite asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="6a60d-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="6a60d-122">Existujú dva spôsoby spustenia asistenta plánovania.</span><span class="sxs-lookup"><span data-stu-id="6a60d-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="6a60d-123">Ak používate hybridný režim, v mriežke člena tímu môžete vybrať ľubovoľného člena tímu s nesplnenou požiadavkou na zdroje a potom vybrať možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="6a60d-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="6a60d-124">Ak používate centrálny režim, správca zdrojov vyhľadá a vyberie zdroj.</span><span class="sxs-lookup"><span data-stu-id="6a60d-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="6a60d-125">Filtre asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="6a60d-125">Schedule assistant filters</span></span>

<span data-ttu-id="6a60d-126">Po spustení asistenta plánovania sa podrobnosti z požiadavky na zdroj zobrazia ako filtrované hodnoty na ľavej table.</span><span class="sxs-lookup"><span data-stu-id="6a60d-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="6a60d-127">Správca zdrojov alebo projektový manažér môže doladiť výsledky úpravou filtrov tak, aby vyhovovali potrebám plánovania.</span><span class="sxs-lookup"><span data-stu-id="6a60d-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="6a60d-128">Na table filtra sú zobrazené možnosti súvisiace s prácou, vrátane:</span><span class="sxs-lookup"><span data-stu-id="6a60d-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="6a60d-129">Začiatok a koniec práce</span><span class="sxs-lookup"><span data-stu-id="6a60d-129">Work start and end</span></span>
-   <span data-ttu-id="6a60d-130">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="6a60d-130">Characteristics</span></span>
-   <span data-ttu-id="6a60d-131">Roly</span><span class="sxs-lookup"><span data-stu-id="6a60d-131">Roles</span></span>
-   <span data-ttu-id="6a60d-132">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="6a60d-132">Organizational units</span></span>
-   <span data-ttu-id="6a60d-133">Spoločnosť zaisťujúca zdroje</span><span class="sxs-lookup"><span data-stu-id="6a60d-133">Resourcing company</span></span>
-   <span data-ttu-id="6a60d-134">Typy zdrojov</span><span class="sxs-lookup"><span data-stu-id="6a60d-134">Resource types</span></span>
-   <span data-ttu-id="6a60d-135">Preferované zdroje</span><span class="sxs-lookup"><span data-stu-id="6a60d-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]