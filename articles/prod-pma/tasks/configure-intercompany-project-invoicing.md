---
title: Konfigurácia fakturácie medzipodnikových projektov
description: Táto téma ukazuje, ako nastaviť fakturáciu projektu medzi dvoma spoločnosťami vo vašej organizácii.
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9df15cb3712356a164de3507f5dbc17a9ff9a652
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288398"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="34b8c-103">Konfigurácia fakturácie medzipodnikových projektov</span><span class="sxs-lookup"><span data-stu-id="34b8c-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="34b8c-104">Táto téma ukazuje, ako nastaviť fakturáciu projektu medzi dvoma spoločnosťami vo vašej organizácii.</span><span class="sxs-lookup"><span data-stu-id="34b8c-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="34b8c-105">Táto úloha používa množinu údajov USSI.</span><span class="sxs-lookup"><span data-stu-id="34b8c-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="34b8c-106">Na navigačnej table prejdite do **Moduly > Záväzky > Nákupné objednávky > Dodávatelia > Všetci dodávatelia**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="34b8c-107">V zozname **Všetci dodávatelia** vyhľadajte a vyberte požadovaný záznam.</span><span class="sxs-lookup"><span data-stu-id="34b8c-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="34b8c-108">Na table Akcia vyberte možnosť **Všeobecné**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="34b8c-109">Stlačte možnosť **Medzipodnikové**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="34b8c-110">Nastavte **Aktívne** na **Áno**, čím aktivujete medzipodnikové obchodovanie.</span><span class="sxs-lookup"><span data-stu-id="34b8c-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="34b8c-111">Do poľa **Spoločnosť zákazníka** zadajte alebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34b8c-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="34b8c-112">V poli **Môj účet** zadajte alebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34b8c-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="34b8c-113">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-113">Select **Save**.</span></span>
9. <span data-ttu-id="34b8c-114">Zatvorením stránok sa vrátite na domovskú stránku.</span><span class="sxs-lookup"><span data-stu-id="34b8c-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="34b8c-115">Na navigačnej table prejdite do **Moduly > Riadenie projektu a účtovníctvo > Nastavenie > Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="34b8c-116">Stlačte kartu **Medzipodnikové**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="34b8c-117">Posuňte posúvač na **Áno**, čím aktivujete medzipodnikové plánovanie zdrojov a časové rozvrhy.</span><span class="sxs-lookup"><span data-stu-id="34b8c-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="34b8c-118">V zozname označte vybratý riadok.</span><span class="sxs-lookup"><span data-stu-id="34b8c-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="34b8c-119">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-119">Select **New**.</span></span>
15. <span data-ttu-id="34b8c-120">V poli **Právnická osoba, ktorá si prenajíma** zadajte alebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34b8c-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="34b8c-121">Zaškrtnite pole **Zvýšený príjem**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="34b8c-122">V poli **Predvolená kategória časového rozvrhu** zadajte alebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34b8c-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="34b8c-123">V poli **Predvolená kategória výdavkov** zadajte alebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34b8c-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="34b8c-124">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-124">Select **Save**.</span></span>
20. <span data-ttu-id="34b8c-125">Zatvorí stránku.</span><span class="sxs-lookup"><span data-stu-id="34b8c-125">Close the page.</span></span>
21. <span data-ttu-id="34b8c-126">Na navigačnej table prejdite do **Moduly > Riadenie projektu a účtovníctvo > Nastavenie > Zverejňovanie > Nastavenia zverejňovania v hlavnej knihe**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="34b8c-127">V **Typy účtov hlavnej knihy** vyberte možnosť.</span><span class="sxs-lookup"><span data-stu-id="34b8c-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="34b8c-128">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-128">Select **New**.</span></span>
24. <span data-ttu-id="34b8c-129">V poli **Hlavný účet** do nového riadku zadajte požadované hodnoty.</span><span class="sxs-lookup"><span data-stu-id="34b8c-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="34b8c-130">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-130">Select **Save**.</span></span>
26. <span data-ttu-id="34b8c-131">Zatvorí stránku.</span><span class="sxs-lookup"><span data-stu-id="34b8c-131">Close the page.</span></span>
27. <span data-ttu-id="34b8c-132">Na navigačnej table prejdite do **Moduly > Projektové riadenie a účtovníctvo > Nastavenie > Ceny > Cena transferu**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="34b8c-133">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-133">Select **New**.</span></span>
29. <span data-ttu-id="34b8c-134">Do poľa **Dátum platnosti** zadajte dátum.</span><span class="sxs-lookup"><span data-stu-id="34b8c-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="34b8c-135">V poli **Právnická osoba, ktorá si prenajíma** zadajte alebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="34b8c-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="34b8c-136">V poli **Model prenosovej ceny** vyberte možnosť.</span><span class="sxs-lookup"><span data-stu-id="34b8c-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="34b8c-137">V poli **Ceny** zadajte číslo.</span><span class="sxs-lookup"><span data-stu-id="34b8c-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="34b8c-138">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="34b8c-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]