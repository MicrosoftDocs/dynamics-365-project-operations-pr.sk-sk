---
title: Prehľad asistenta plánovania
description: Táto téma poskytuje informácie o práci s asistentom plánovania pri rezervácii zdrojov.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 83583c97e4ecb5f1fdc0d8d98098afe8e12d27e4
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368135"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="445a2-103">Prehľad asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="445a2-103">Schedule assistant overview</span></span>

<span data-ttu-id="445a2-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="445a2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="445a2-105">Asistent plánovania sa používa na rezerváciu zdrojov na základe požiadaviek definovaných projektovým manažérom.</span><span class="sxs-lookup"><span data-stu-id="445a2-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="445a2-106">Asistent plánovania sa pri hľadaní zdroja spolieha na parametre uvedené v požiadavke na zdroj.</span><span class="sxs-lookup"><span data-stu-id="445a2-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="445a2-107">Asistent plánovania odporúča zdroje, ktoré zodpovedajú príslušným požiadavkám, ako sú časové okná alebo potrebné zručnosti.</span><span class="sxs-lookup"><span data-stu-id="445a2-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="445a2-108">Po identifikácii vhodných zdrojov môže manažér zdrojov alebo projektu rezervovať zdroj pre prácu.</span><span class="sxs-lookup"><span data-stu-id="445a2-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="445a2-109">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="445a2-109">Prerequisites</span></span>

<span data-ttu-id="445a2-110">Asistent plánovania je súčasťou riešenia Universal Resource Scheduling.</span><span class="sxs-lookup"><span data-stu-id="445a2-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="445a2-111">Toto riešenie je zahrnuté a nainštalované do Dynamics 365 Project Operations, Dynamics 365 Field Service a Dynamics 365 Customer Service.</span><span class="sxs-lookup"><span data-stu-id="445a2-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="445a2-112">Zosúlaďovanie požiadaviek a zdrojov</span><span class="sxs-lookup"><span data-stu-id="445a2-112">Matching requirements and resources</span></span>

<span data-ttu-id="445a2-113">Vygenerovaná požiadavka na zdroj je založená na podrobnostiach, ako napríklad:</span><span class="sxs-lookup"><span data-stu-id="445a2-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="445a2-114">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="445a2-114">Characteristics</span></span>
-   <span data-ttu-id="445a2-115">Roly</span><span class="sxs-lookup"><span data-stu-id="445a2-115">Roles</span></span>
-   <span data-ttu-id="445a2-116">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="445a2-116">Business units</span></span>
-   <span data-ttu-id="445a2-117">Predvoľby zdrojov</span><span class="sxs-lookup"><span data-stu-id="445a2-117">Resource preferences</span></span>
-   <span data-ttu-id="445a2-118">Obrysy úsilia</span><span class="sxs-lookup"><span data-stu-id="445a2-118">Effort contours</span></span>
-   <span data-ttu-id="445a2-119">Časové pásmo</span><span class="sxs-lookup"><span data-stu-id="445a2-119">Time zone</span></span>

<span data-ttu-id="445a2-120">Asistent plánovania používa tieto podrobnosti na filtrovanie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="445a2-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="445a2-121">Spustite asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="445a2-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="445a2-122">Existujú dva spôsoby spustenia asistenta plánovania.</span><span class="sxs-lookup"><span data-stu-id="445a2-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="445a2-123">Ak používate hybridný režim, v mriežke člena tímu môžete vybrať ľubovoľného člena tímu s nesplnenou požiadavkou na zdroje a potom vybrať možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="445a2-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="445a2-124">Ak používate centrálny režim, správca zdrojov vyhľadá a vyberie zdroj.</span><span class="sxs-lookup"><span data-stu-id="445a2-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="445a2-125">Filtre asistenta plánovania</span><span class="sxs-lookup"><span data-stu-id="445a2-125">Schedule assistant filters</span></span>

<span data-ttu-id="445a2-126">Po spustení asistenta plánovania sa podrobnosti z požiadavky na zdroj zobrazia ako filtrované hodnoty na ľavej table.</span><span class="sxs-lookup"><span data-stu-id="445a2-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="445a2-127">Správca zdrojov alebo projektový manažér môže doladiť výsledky úpravou filtrov tak, aby vyhovovali potrebám plánovania.</span><span class="sxs-lookup"><span data-stu-id="445a2-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="445a2-128">Na table filtra sú zobrazené možnosti súvisiace s prácou, vrátane:</span><span class="sxs-lookup"><span data-stu-id="445a2-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="445a2-129">Začiatok a koniec práce</span><span class="sxs-lookup"><span data-stu-id="445a2-129">Work start and end</span></span>
-   <span data-ttu-id="445a2-130">Charakteristiky</span><span class="sxs-lookup"><span data-stu-id="445a2-130">Characteristics</span></span>
-   <span data-ttu-id="445a2-131">Roly</span><span class="sxs-lookup"><span data-stu-id="445a2-131">Roles</span></span>
-   <span data-ttu-id="445a2-132">Organizačné jednotky</span><span class="sxs-lookup"><span data-stu-id="445a2-132">Organizational units</span></span>
-   <span data-ttu-id="445a2-133">Spoločnosť zaisťujúca zdroje</span><span class="sxs-lookup"><span data-stu-id="445a2-133">Resourcing company</span></span>
-   <span data-ttu-id="445a2-134">Typy zdrojov</span><span class="sxs-lookup"><span data-stu-id="445a2-134">Resource types</span></span>
-   <span data-ttu-id="445a2-135">Preferované zdroje</span><span class="sxs-lookup"><span data-stu-id="445a2-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]