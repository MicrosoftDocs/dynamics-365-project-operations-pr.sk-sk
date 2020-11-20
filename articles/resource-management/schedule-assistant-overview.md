---
title: Prehľad asistenta plánovania
description: Táto téma poskytuje informácie o práci s asistentom plánovania pri rezervácii zdrojov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 92b12bd9272805a736286bf7e0ff926cb6361c05
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125647"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="30d44-103">Prehľad asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="30d44-103">Schedule assistant overview</span></span>

<span data-ttu-id="30d44-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="30d44-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="30d44-105">Asistent plánovania sa používa na rezerváciu zdrojov na základe požiadaviek definovaných projektovým manažérom.</span><span class="sxs-lookup"><span data-stu-id="30d44-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="30d44-106">Asistent plánovania sa pri hľadaní zdroja spolieha na parametre uvedené v požiadavke na zdroj.</span><span class="sxs-lookup"><span data-stu-id="30d44-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="30d44-107">Asistent plánovania odporúča zdroje, ktoré zodpovedajú príslušným požiadavkám, ako sú časové okná alebo potrebné zručnosti.</span><span class="sxs-lookup"><span data-stu-id="30d44-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="30d44-108">Po identifikácii vhodných zdrojov môže manažér zdrojov alebo projektu rezervovať zdroj pre prácu.</span><span class="sxs-lookup"><span data-stu-id="30d44-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="30d44-109">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="30d44-109">Prerequisites</span></span>

<span data-ttu-id="30d44-110">Asistent plánovania je súčasťou riešenia Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="30d44-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="30d44-111">Toto riešenie je zahrnuté a nainštalované spolu s Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="30d44-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="30d44-112">Zosúlaďovanie požiadaviek a zdrojov</span><span class="sxs-lookup"><span data-stu-id="30d44-112">Matching requirements and resources</span></span>

<span data-ttu-id="30d44-113">Vygenerovaná požiadavka na zdroj je založená na podrobnostiach, ako napríklad:</span><span class="sxs-lookup"><span data-stu-id="30d44-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="30d44-114">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="30d44-114">Characteristics</span></span>
-   <span data-ttu-id="30d44-115">Roly</span><span class="sxs-lookup"><span data-stu-id="30d44-115">Roles</span></span>
-   <span data-ttu-id="30d44-116">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="30d44-116">Business units</span></span>
-   <span data-ttu-id="30d44-117">Predvoľby zdrojov</span><span class="sxs-lookup"><span data-stu-id="30d44-117">Resource preferences</span></span>
-   <span data-ttu-id="30d44-118">Obrysy úsilia</span><span class="sxs-lookup"><span data-stu-id="30d44-118">Effort contours</span></span>
-   <span data-ttu-id="30d44-119">Časové pásmo</span><span class="sxs-lookup"><span data-stu-id="30d44-119">Time zone</span></span>

<span data-ttu-id="30d44-120">Asistent plánovania používa tieto podrobnosti na filtrovanie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="30d44-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="30d44-121">Spustite asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="30d44-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="30d44-122">Existujú dva spôsoby spustenia asistenta plánovania.</span><span class="sxs-lookup"><span data-stu-id="30d44-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="30d44-123">Ak používate hybridný režim, v mriežke člena tímu môžete vybrať ľubovoľného člena tímu s nesplnenou požiadavkou na zdroje a potom vybrať možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="30d44-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="30d44-124">Ak používate centrálny režim, správca zdrojov vyhľadá a vyberie zdroj.</span><span class="sxs-lookup"><span data-stu-id="30d44-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="30d44-125">Filtre asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="30d44-125">Schedule assistant filters</span></span>

<span data-ttu-id="30d44-126">Po spustení asistenta plánovania sa podrobnosti z požiadavky na zdroj zobrazia ako filtrované hodnoty na ľavej table.</span><span class="sxs-lookup"><span data-stu-id="30d44-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="30d44-127">Správca zdrojov alebo projektový manažér môže doladiť výsledky úpravou filtrov tak, aby vyhovovali potrebám plánovania.</span><span class="sxs-lookup"><span data-stu-id="30d44-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="30d44-128">Na table filtra sú zobrazené možnosti súvisiace s prácou, vrátane:</span><span class="sxs-lookup"><span data-stu-id="30d44-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="30d44-129">Začiatok a koniec práce</span><span class="sxs-lookup"><span data-stu-id="30d44-129">Work start and end</span></span>
-   <span data-ttu-id="30d44-130">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="30d44-130">Characteristics</span></span>
-   <span data-ttu-id="30d44-131">Roly</span><span class="sxs-lookup"><span data-stu-id="30d44-131">Roles</span></span>
-   <span data-ttu-id="30d44-132">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="30d44-132">Organizational units</span></span>
-   <span data-ttu-id="30d44-133">Spoločnosť zaisťujúca zdroje</span><span class="sxs-lookup"><span data-stu-id="30d44-133">Resourcing company</span></span>
-   <span data-ttu-id="30d44-134">Typy zdrojov</span><span class="sxs-lookup"><span data-stu-id="30d44-134">Resource types</span></span>
-   <span data-ttu-id="30d44-135">Preferované zdroje</span><span class="sxs-lookup"><span data-stu-id="30d44-135">Preferred resources</span></span>
