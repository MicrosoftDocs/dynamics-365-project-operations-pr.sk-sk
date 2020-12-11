---
title: Nastavenie kategórií výdavkov
description: Táto téma poskytuje informácie o tom, ako nastaviť kategórie výdavkov a zdieľané kategórie pre výkazy výdavkov.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 13e72e4b852fd0edac5ad35d5162e74b016bce33
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123802"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="ae5f5-103">Nastavenie kategórií výdavkov</span><span class="sxs-lookup"><span data-stu-id="ae5f5-103">Set up expense categories</span></span>

<span data-ttu-id="ae5f5-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="ae5f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ae5f5-105">Keď zamestnanci vytvárajú výkazy výdavkov, každý výdavok, ktorý zaznamenajú, musí byť priradený ku kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="ae5f5-106">Kategórie výdavkov sú odvodené od zdieľaných kategórií, ktoré je možné zdieľať medzi právnymi entitami vo vašej organizácii.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="ae5f5-107">V závislosti od toho, ako je definovaná vaša organizácia, je možné tieto kategórie výdavkov zdieľať aj v iných oblastiach.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="ae5f5-108">Na základe definície vašej organizácie a pokynov implementačného tímu musíte určiť, či sa kategórie, ktoré sa používajú v správe výdavkov, použijú iba v správe výdavkov, alebo či sa majú zdieľať v iných oblastiach.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="ae5f5-109">Tieto kategórie možno zdieľať medzi projektovým manažmentom a účtovníctvom a riadením výdavkov alebo medzi projektovým riadením a účtovníctvom a produkciou.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="ae5f5-110">Nemôžu sa však zdieľať medzi správou výdavkov a produkciou.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="ae5f5-111">Predtým, ako začnete s procesom nastavenia, musíte urobiť nasledujúce rozhodnutia pre každú kategóriu výdavkov:</span><span class="sxs-lookup"><span data-stu-id="ae5f5-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="ae5f5-112">Čo je kategória výdavku?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-112">What is the expense category?</span></span> <span data-ttu-id="ae5f5-113">Príklady zahŕňajú kategórie letov, hotelov alebo najazdených kilometrov.</span><span class="sxs-lookup"><span data-stu-id="ae5f5-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="ae5f5-114">Dá sa kategória výdavkov použiť aj v projektovom manažmente a účtovníctve?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="ae5f5-115">Ak je to možné, musíte uskutočniť aj tieto rozhodnutia:</span><span class="sxs-lookup"><span data-stu-id="ae5f5-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="ae5f5-116">Ktoré nákladové účty sa použijú na nasledujúce výdavky?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="ae5f5-117">Náklady</span><span class="sxs-lookup"><span data-stu-id="ae5f5-117">Cost</span></span>
        - <span data-ttu-id="ae5f5-118">Alokácia miezd</span><span class="sxs-lookup"><span data-stu-id="ae5f5-118">Payroll allocation</span></span>
        - <span data-ttu-id="ae5f5-119">Hodnota nákladov WIP</span><span class="sxs-lookup"><span data-stu-id="ae5f5-119">WIP-cost value</span></span>
        - <span data-ttu-id="ae5f5-120">Nákladová položka</span><span class="sxs-lookup"><span data-stu-id="ae5f5-120">Cost-item</span></span>
        - <span data-ttu-id="ae5f5-121">WIP – nákladová hodnota – položka</span><span class="sxs-lookup"><span data-stu-id="ae5f5-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="ae5f5-122">Akumulovaná strata</span><span class="sxs-lookup"><span data-stu-id="ae5f5-122">Accrued loss</span></span>
        - <span data-ttu-id="ae5f5-123">WIP – akumulovaná strata</span><span class="sxs-lookup"><span data-stu-id="ae5f5-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="ae5f5-124">Ktoré obchodné vzťahy s výnosmi sa použijú pre nasledujúce zdroje výnosov?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="ae5f5-125">Fakturovaný príjem</span><span class="sxs-lookup"><span data-stu-id="ae5f5-125">Invoiced revenue</span></span>
        - <span data-ttu-id="ae5f5-126">Akumulované výnosy – hodnota predaja</span><span class="sxs-lookup"><span data-stu-id="ae5f5-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="ae5f5-127">WIP – hodnota predaja</span><span class="sxs-lookup"><span data-stu-id="ae5f5-127">WIP-sales value</span></span>
        - <span data-ttu-id="ae5f5-128">Akumulované výnosy – produkcia</span><span class="sxs-lookup"><span data-stu-id="ae5f5-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="ae5f5-129">WIP – produkcia</span><span class="sxs-lookup"><span data-stu-id="ae5f5-129">WIP-production</span></span>
        - <span data-ttu-id="ae5f5-130">Akumulované výnosy – zisk</span><span class="sxs-lookup"><span data-stu-id="ae5f5-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="ae5f5-131">WIP – zisk</span><span class="sxs-lookup"><span data-stu-id="ae5f5-131">WIP-profit</span></span>
        - <span data-ttu-id="ae5f5-132">Akumulované výnosy – predplatné</span><span class="sxs-lookup"><span data-stu-id="ae5f5-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="ae5f5-133">WIP – predplatné</span><span class="sxs-lookup"><span data-stu-id="ae5f5-133">WIP-subscription</span></span>

- <span data-ttu-id="ae5f5-134">Čo je typ výdavku?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-134">What is the expense type?</span></span>
- <span data-ttu-id="ae5f5-135">Aký je predvolený spôsob platby pre kategóriu výdavkov?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="ae5f5-136">Musia byť výdavky v kategórii výdavkov rozpísané na jednotlivé položky?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="ae5f5-137">Aký je hlavný predvolený obchodný vzťah pre kategóriu výdavkov?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="ae5f5-138">Aká je predvolená skupina dane z predaja položky pre kategóriu výdavkov?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="ae5f5-139">Sú pre kategóriu výdavkov povolené ďalšie spôsoby platby?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="ae5f5-140">Ak áno, ktoré to sú?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-140">If so, what are they?</span></span>
- <span data-ttu-id="ae5f5-141">Existujú v tejto kategórii výdavkov podkategórie?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="ae5f5-142">Ak existujú podkategórie, musíte uskutočniť aj nasledujúce rozhodnutia:</span><span class="sxs-lookup"><span data-stu-id="ae5f5-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="ae5f5-143">Je niektorá z podkategórií vylúčená z vrátenia dane?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="ae5f5-144">Čo je skupina dane z predaja položky v podkategóriách?</span><span class="sxs-lookup"><span data-stu-id="ae5f5-144">What is the item sales tax group of the subcategories?</span></span>