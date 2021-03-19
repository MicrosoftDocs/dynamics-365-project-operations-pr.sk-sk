---
title: Nakonfigurujte štandardné náklady na prácu a výdavky
description: Táto téma vysvetľuje, ako nastaviť štandardné náklady na prácu a náklady na projekt.
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b16ed50584b2b4535d1c61fe7069708182a4820e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288353"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="e83f1-103">Nakonfigurujte štandardné náklady na prácu a výdavky</span><span class="sxs-lookup"><span data-stu-id="e83f1-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e83f1-104">Táto téma vysvetľuje, ako nastaviť štandardné náklady na prácu a náklady na projekt.</span><span class="sxs-lookup"><span data-stu-id="e83f1-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="e83f1-105">Táto úloha používa množinu údajov USSI.</span><span class="sxs-lookup"><span data-stu-id="e83f1-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="e83f1-106">Na navigačnej table prejdite do **Moduly > Projektové riadenie a účtovníctvo > Nastavenie > Ceny > Obstarávacia cena (hodina)**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="e83f1-107">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-107">Select **New**.</span></span>
3. <span data-ttu-id="e83f1-108">Do poľa **Dátum platnosti** zadajte dátum.</span><span class="sxs-lookup"><span data-stu-id="e83f1-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="e83f1-109">V poli **Obstarávacia cena** zadajte číslo.</span><span class="sxs-lookup"><span data-stu-id="e83f1-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e83f1-110">Pre kategóriu projektu môžete nastaviť štandardnú nákladovú cenu alebo môžete nastaviť nákladovú cenu podľa čísla pracovníka, čísla projektu, kategórie, dátumu alebo akejkoľvek ich kombinácie.</span><span class="sxs-lookup"><span data-stu-id="e83f1-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="e83f1-111">Použitá obstarávacia cena je obstarávacia cena s najvyššou úrovňou detailov.</span><span class="sxs-lookup"><span data-stu-id="e83f1-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="e83f1-112">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-112">Select **Save**.</span></span>
6. <span data-ttu-id="e83f1-113">Na navigačnej table prejdite do **Moduly > Projektové riadenie a účtovníctvo > Nastavenie > Ceny > Predajná cena (hodina)**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="e83f1-114">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-114">Select **New**.</span></span>
8. <span data-ttu-id="e83f1-115">Do poľa **Dátum platnosti** zadajte dátum.</span><span class="sxs-lookup"><span data-stu-id="e83f1-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="e83f1-116">V poli **Platné pre** zvoľte možnosť.</span><span class="sxs-lookup"><span data-stu-id="e83f1-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="e83f1-117">V poli **Ceny** zadajte číslo.</span><span class="sxs-lookup"><span data-stu-id="e83f1-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e83f1-118">Môžete nastaviť štandardnú predajnú cenu pre hodinové transakcie alebo pre kategóriu projektu.</span><span class="sxs-lookup"><span data-stu-id="e83f1-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="e83f1-119">Môžete tiež nastaviť predajné ceny podľa čísla pracovníka, čísla projektu, kategórie, dátumu transakcie alebo akejkoľvek ich kombinácie.</span><span class="sxs-lookup"><span data-stu-id="e83f1-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="e83f1-120">Skutočná predajná cena, ktorá sa použije, keď pracovník zadá transakciu do denníka hodín, je predajná cena s najvyššou úrovňou podrobností.</span><span class="sxs-lookup"><span data-stu-id="e83f1-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e83f1-121">Napríklad, ak je nastavená všeobecná predajná cena aj predajná cena špecifická pre pracovníka, použije sa predajná cena špecifická pre pracovníka.</span><span class="sxs-lookup"><span data-stu-id="e83f1-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="e83f1-122">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-122">Select **Save**.</span></span>
12. <span data-ttu-id="e83f1-123">Zatvorí stránku.</span><span class="sxs-lookup"><span data-stu-id="e83f1-123">Close the page.</span></span>
13. <span data-ttu-id="e83f1-124">Na navigačnej table prejdite do **Moduly > Riadenie projektu a účtovníctvo > Nastavenie > Ceny > Obstarávacia cena (výdavok)**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="e83f1-125">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-125">Select **New**.</span></span>
15. <span data-ttu-id="e83f1-126">Do poľa **Dátum platnosti** zadajte dátum.</span><span class="sxs-lookup"><span data-stu-id="e83f1-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="e83f1-127">V poli **Obstarávacia cena** zadajte číslo.</span><span class="sxs-lookup"><span data-stu-id="e83f1-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="e83f1-128">Môže sa vyplniť viac polí, ale to je minimum potrebné na uloženie záznamu.</span><span class="sxs-lookup"><span data-stu-id="e83f1-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="e83f1-129">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-129">Select **Save**.</span></span>
18. <span data-ttu-id="e83f1-130">Na navigačnej table prejdite do **Moduly > Riadenie projektu a účtovníctvo > Nastavenie > Ceny > Predajná cena (výdavok)**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="e83f1-131">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-131">Select **New**.</span></span>
20. <span data-ttu-id="e83f1-132">Do poľa **Dátum platnosti** zadajte dátum.</span><span class="sxs-lookup"><span data-stu-id="e83f1-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="e83f1-133">V poli **Platné pre** zvoľte možnosť.</span><span class="sxs-lookup"><span data-stu-id="e83f1-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="e83f1-134">V poli **Ceny** zadajte číslo.</span><span class="sxs-lookup"><span data-stu-id="e83f1-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="e83f1-135">Skutočná predajná cena, ktorá sa použije, keď pracovník zadá transakciu do denníka výdavkov, je predajná cena s najvyššou úrovňou podrobností.</span><span class="sxs-lookup"><span data-stu-id="e83f1-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="e83f1-136">Napríklad, ak je nastavená všeobecná aj predajná cena špecifická pre pracovníka, použije sa predajná cena špecifická pre pracovníka.</span><span class="sxs-lookup"><span data-stu-id="e83f1-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="e83f1-137">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e83f1-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]