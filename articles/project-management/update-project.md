---
title: Aktualizácia projektu
description: Táto téma poskytuje informácie o aktualizácii projektov Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8bcbc6c5a62d252398d541649647fbad49006a0c
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131452"
---
# <a name="update-a-project"></a><span data-ttu-id="bcb75-103">Aktualizácia projektu</span><span class="sxs-lookup"><span data-stu-id="bcb75-103">Update a project</span></span>

<span data-ttu-id="bcb75-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="bcb75-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bcb75-105">Ďalej je uvedený súhrn polí, ktoré je možné aktualizovať po vytvorení projektu, a všetkých príslušných dôsledkov aktualizácií.</span><span class="sxs-lookup"><span data-stu-id="bcb75-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="bcb75-106">Polia podrobností projektu</span><span class="sxs-lookup"><span data-stu-id="bcb75-106">Project detail fields</span></span>

- <span data-ttu-id="bcb75-107">**Názov**: Názov projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="bcb75-108">**Popis**: Prehľad projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="bcb75-109">**Zákazník**: Spoločnosť, ktorej bude projekt dodaný.</span><span class="sxs-lookup"><span data-stu-id="bcb75-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="bcb75-110">**Šablóna kalendára** : Pracovný čas projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="bcb75-111">Po zmene poľa sa prepočíta celý plán.</span><span class="sxs-lookup"><span data-stu-id="bcb75-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="bcb75-112">**Mena**: Mena pre projekt.</span><span class="sxs-lookup"><span data-stu-id="bcb75-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="bcb75-113">Toto pole je predvolené na základe meny definovanej v zmluvnej jednotke.</span><span class="sxs-lookup"><span data-stu-id="bcb75-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="bcb75-114">Keď sa aktualizuje zmluvná jednotka, aktualizuje sa aj pole.</span><span class="sxs-lookup"><span data-stu-id="bcb75-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="bcb75-115">**Zmluvná jednotka**: Organizačná jednotka, ktorá zastupuje skupinu spoločností alebo divízie, ktorá je primárne zodpovedná za získanie predaja a riadenie poskytovania práce a služieb zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="bcb75-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="bcb75-116">**Projektový manažér** : Člen projektového tímu, ktorý je oprávnený kontrolovať a schvaľovať časové zadania a výdavky.</span><span class="sxs-lookup"><span data-stu-id="bcb75-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="bcb75-117">Polia odhadu</span><span class="sxs-lookup"><span data-stu-id="bcb75-117">Estimate fields</span></span>

- <span data-ttu-id="bcb75-118">**Odhadovaný dátum začatia**: Dátum začiatku projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="bcb75-119">Po aktualizácii tohto poľa sa všetky úlohy v projekte presunú úmerne s novým dátumom začatia.</span><span class="sxs-lookup"><span data-stu-id="bcb75-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="bcb75-120">**Dátum dokončenia**: Dátum ukončenia projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="bcb75-121">**Úsilie**: Odhadované úsilie projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="bcb75-122">Po pridaní úloh do projektu už toto pole nie je možné upravovať.</span><span class="sxs-lookup"><span data-stu-id="bcb75-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="bcb75-123">**Odhadované mzdové náklady**: Odhadované mzdové náklady projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="bcb75-124">Po pridaní mzdových nákladov do projektu už toto pole nie je možné upravovať.</span><span class="sxs-lookup"><span data-stu-id="bcb75-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="bcb75-125">**Odhadované výdavky** : Odhadované výdavky na projekt.</span><span class="sxs-lookup"><span data-stu-id="bcb75-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="bcb75-126">Po pridaní výdavkov do projektu už toto pole nie je možné upravovať.</span><span class="sxs-lookup"><span data-stu-id="bcb75-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="bcb75-127">Skutočné polia projektu</span><span class="sxs-lookup"><span data-stu-id="bcb75-127">Project actual fields</span></span>
- <span data-ttu-id="bcb75-128">**Skutočný začiatok** : Dátum zahájenia projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="bcb75-129">**Skutočný koniec**: Bude aktualizované po dokončení projektu.</span><span class="sxs-lookup"><span data-stu-id="bcb75-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="bcb75-130">Polia pre stav projektu</span><span class="sxs-lookup"><span data-stu-id="bcb75-130">Project status fields</span></span>

- <span data-ttu-id="bcb75-131">**Celkový stav projektu**: Celkový stav projektu poskytnutý projektovým manažérom.</span><span class="sxs-lookup"><span data-stu-id="bcb75-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="bcb75-132">**Komentáre**: Popis týkajúci sa aktuálneho stavu projektu poskytnutý projektovým manažérom.</span><span class="sxs-lookup"><span data-stu-id="bcb75-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>
