---
title: Prehľad režimov správy zdrojov
description: Táto téma poskytuje informácie o funkcii Správa zdrojov v aplikácii Dynamics 365 Project Operations.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94db65a2ddbdc6a7226c70907bcce4c45b4a3923
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000905"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="da4d8-103">Prehľad režimov správy zdrojov</span><span class="sxs-lookup"><span data-stu-id="da4d8-103">Resource management modes overview</span></span>

<span data-ttu-id="da4d8-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="da4d8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="da4d8-105">Dynamics 365 Project Operations podporuje dva režimy, aby ste mohli vykonať celkový postup rezervácie.</span><span class="sxs-lookup"><span data-stu-id="da4d8-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="da4d8-106">Režim správy je definovaný ako parameter projektu a je možné ho upraviť, ak sa zmenia vaše obchodné potreby.</span><span class="sxs-lookup"><span data-stu-id="da4d8-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="da4d8-107">Centrálny režim</span><span class="sxs-lookup"><span data-stu-id="da4d8-107">Central mode</span></span>
<span data-ttu-id="da4d8-108">Pre organizácie, ktoré centralizujú pridelenie zdrojov k projektom poskytuje centrálny režim spôsob, ako zabezpečiť, aby manažéri projektu mohli definovať požiadavky na zdroje na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="da4d8-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="da4d8-109">Splnenie požiadaviek na zdroje sa deleguje na manažéra zdrojov.</span><span class="sxs-lookup"><span data-stu-id="da4d8-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="da4d8-110">Projektoví manažéri môžu prijímať alebo odmietať zdroje, ktoré navrhuje manažér zdrojov.</span><span class="sxs-lookup"><span data-stu-id="da4d8-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centrálny režim](./media/resource-management-central.png)

<span data-ttu-id="da4d8-112">Informácie o správe zdrojov v centrálnom režime nájdete na:</span><span class="sxs-lookup"><span data-stu-id="da4d8-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="da4d8-113">Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="da4d8-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="da4d8-114">Rezervácia pomenovaných zdrojov z požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="da4d8-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="da4d8-115">Odoslanie žiadosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="da4d8-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="da4d8-116">Splnenie požiadavky na zdroj</span><span class="sxs-lookup"><span data-stu-id="da4d8-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="da4d8-117">Prijatie alebo odmietnutie navrhovaného prostriedku projektu zo žiadosti o prostriedok</span><span class="sxs-lookup"><span data-stu-id="da4d8-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="da4d8-118">Hybridný režim</span><span class="sxs-lookup"><span data-stu-id="da4d8-118">Hybrid mode</span></span>
<span data-ttu-id="da4d8-119">Pre organizácie, ktoré požadujú flexibilitu pri prideľovaní zdrojov, umožňuje hybridný režim rezervovať zdroje projektovým manažérom aj manažérom zdrojov.</span><span class="sxs-lookup"><span data-stu-id="da4d8-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridný režim](./media/resource-management-hybrid.png)

<span data-ttu-id="da4d8-121">Okrem podporovaného procesu v centrálnom režime nájdete v nasledujúcich témach správu všetkých ostatných podporovaných tokov rezervácie v hybridnom režime:</span><span class="sxs-lookup"><span data-stu-id="da4d8-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="da4d8-122">Priama rezervácia zdroja pre projekt:</span><span class="sxs-lookup"><span data-stu-id="da4d8-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="da4d8-123">Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh</span><span class="sxs-lookup"><span data-stu-id="da4d8-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="da4d8-124">Rezervácia zdroja z požiadaviek zdrojov:</span><span class="sxs-lookup"><span data-stu-id="da4d8-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="da4d8-125">Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="da4d8-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="da4d8-126">Rezervácia pomenovaných zdrojov z požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="da4d8-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]