---
title: Prehľad režimov správy zdrojov
description: Táto téma poskytuje informácie o funkciách Správa zdrojov v Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 73ba6190e2e366f22372102d14d26f6d71ba0bc1
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118537"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="eb671-103">Prehľad režimov správy zdrojov</span><span class="sxs-lookup"><span data-stu-id="eb671-103">Resource management modes overview</span></span>

<span data-ttu-id="eb671-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="eb671-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="eb671-105">Dynamics 365 Project Operations podporuje dva režimy, aby ste mohli vykonať celkový tok rezervácií.</span><span class="sxs-lookup"><span data-stu-id="eb671-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="eb671-106">Režim správy je definovaný ako parameter projektu a je možné ho upraviť, ak sa zmenia vaše obchodné potreby.</span><span class="sxs-lookup"><span data-stu-id="eb671-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="eb671-107">Centrálny režim</span><span class="sxs-lookup"><span data-stu-id="eb671-107">Central mode</span></span>
<span data-ttu-id="eb671-108">Pre organizácie, ktoré centralizujú pridelenie zdrojov k projektom poskytuje centrálny režim spôsob, ako zabezpečiť, aby manažéri projektu mohli definovať požiadavky na zdroje na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="eb671-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="eb671-109">Splnenie požiadaviek na zdroje sa deleguje na manažéra zdrojov.</span><span class="sxs-lookup"><span data-stu-id="eb671-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="eb671-110">Projektoví manažéri môžu prijímať alebo odmietať zdroje, ktoré navrhuje manažér zdrojov.</span><span class="sxs-lookup"><span data-stu-id="eb671-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centrálny režim](./media/resource-management-central.png)

<span data-ttu-id="eb671-112">Informácie o správe zdrojov v centrálnom režime nájdete na:</span><span class="sxs-lookup"><span data-stu-id="eb671-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="eb671-113">Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="eb671-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="eb671-114">Rezervácia pomenovaných zdrojov z požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="eb671-114">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="eb671-115">Odoslanie žiadosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="eb671-115">Submit a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="eb671-116">Splnenie požiadavky na zdroj</span><span class="sxs-lookup"><span data-stu-id="eb671-116">Fulfill a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="eb671-117">Prijatie alebo odmietnutie navrhovaného prostriedku projektu zo žiadosti o prostriedok</span><span class="sxs-lookup"><span data-stu-id="eb671-117">Accept or reject a proposed project resource from a resource request</span></span>](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="eb671-118">Hybridný režim</span><span class="sxs-lookup"><span data-stu-id="eb671-118">Hybrid mode</span></span>
<span data-ttu-id="eb671-119">Pre organizácie, ktoré požadujú flexibilitu pri prideľovaní zdrojov, umožňuje hybridný režim rezervovať zdroje projektovým manažérom aj manažérom zdrojov.</span><span class="sxs-lookup"><span data-stu-id="eb671-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hybridný režim](./media/resource-management-hybrid.png)

<span data-ttu-id="eb671-121">Okrem podporovaného procesu v centrálnom režime nájdete v nasledujúcich témach správu všetkých ostatných podporovaných tokov rezervácie v hybridnom režime:</span><span class="sxs-lookup"><span data-stu-id="eb671-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="eb671-122">Priama rezervácia zdroja pre projekt:</span><span class="sxs-lookup"><span data-stu-id="eb671-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="eb671-123">Rezervácia pomenovaných rezervovateľných zdrojov pre projektový tímu a priradenie úloh</span><span class="sxs-lookup"><span data-stu-id="eb671-123">Book named bookable resources to a project team and assign tasks</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="eb671-124">Rezervácia zdroja z požiadaviek zdrojov:</span><span class="sxs-lookup"><span data-stu-id="eb671-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="eb671-125">Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="eb671-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="eb671-126">Rezervácia pomenovaných zdrojov z požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="eb671-126">Book named resources from resource requirements</span></span>](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
