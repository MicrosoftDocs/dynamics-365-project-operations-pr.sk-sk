---
title: Nastavenie zdrojov pre projekty
description: Táto téma poskytuje informácie o nastavení alebo požadovaní zdrojov projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7eec8ad5d78019219b2e04ca75eeaa5a3c8a748f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084536"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="46009-103">Nastavenie zdrojov pre projekty</span><span class="sxs-lookup"><span data-stu-id="46009-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="46009-104">Musíte si pripraviť kalendár a priradiť ho k zamestnancovi alebo pracovníkovi.</span><span class="sxs-lookup"><span data-stu-id="46009-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="46009-105">Kalendár sa používa na plánovanie projektu a pracovného času zdrojov, ktoré sú rezervované pre projekt.</span><span class="sxs-lookup"><span data-stu-id="46009-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="46009-106">Počas nastavovania kalendára môžu projektoví manažéri v rámci optimalizácie zdrojov vykonať optimalizáciu zdrojov.</span><span class="sxs-lookup"><span data-stu-id="46009-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="46009-107">Na základe harmonogramu kalendára je možné uvaliť obmedzenia na zdroje.</span><span class="sxs-lookup"><span data-stu-id="46009-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="46009-108">Kalendár si môžete nastaviť na stránke **Kalendáre**.</span><span class="sxs-lookup"><span data-stu-id="46009-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="46009-109">Keď nastavujete pracovníka ako zdroj projektu, môžete si vybrať z pracovníkov, ktorí pracujú v spoločnosti, pre ktorú nastavujete zdroje.</span><span class="sxs-lookup"><span data-stu-id="46009-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="46009-110">Prípadne si môžete vybrať pracovníkov z iných spoločností vo vašej organizácii.</span><span class="sxs-lookup"><span data-stu-id="46009-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="46009-111">Títo pracovníci sú známi ako medzipodnikové zdroje.</span><span class="sxs-lookup"><span data-stu-id="46009-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="46009-112">Nasledujúce postupy vysvetľujú, ako nastaviť pracovníka ako zdroj projektu vo vašej spoločnosti a ako nastaviť medzipodnikový zdroj projektu.</span><span class="sxs-lookup"><span data-stu-id="46009-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="46009-113">Nastavenie pracovníka ako zdroja projektu</span><span class="sxs-lookup"><span data-stu-id="46009-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="46009-114">Na stránke **Pracovníci** v zozname **Pracovníci** vyberte pracovníka, ktorého pridávate ako zdroje projektu, a otvorte záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="46009-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="46009-115">Na table Akcia vyberte možnosť **Projekt** &gt; **Nastaviť** &gt; **Nastavenie projektu**.</span><span class="sxs-lookup"><span data-stu-id="46009-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="46009-116">Vyberte kalendár a potom stránku zavrite.</span><span class="sxs-lookup"><span data-stu-id="46009-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="46009-117">Môžete tiež určiť predvolené projekty pre zdroj ako typ predbežného priradenia.</span><span class="sxs-lookup"><span data-stu-id="46009-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="46009-118">Predbežné priradenia je možné použiť, keď manažér zdrojov alebo projektový manažér vopred vedia, na ktorých projektoch bude zdroj pracovať.</span><span class="sxs-lookup"><span data-stu-id="46009-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="46009-119">Predbežné priradenia môžu byť tiež založené na žiadosti sponzora projektu alebo zákazníka.</span><span class="sxs-lookup"><span data-stu-id="46009-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="46009-120">Na predbežné priradenie projektu vyberte na stránke **Priradiť projekty** na karte **Projekty** v zozname **Zostávajúce projekty** príslušný projekt.</span><span class="sxs-lookup"><span data-stu-id="46009-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="46009-121">Nastavenie medzipodnikového zdroja</span><span class="sxs-lookup"><span data-stu-id="46009-121">Set up an intercompany resource</span></span>

<span data-ttu-id="46009-122">Keď nastavíte pracovníka ako medzipodnikový zdroj, musíte dokončiť nastavenie v spoločnosti, ktorá ho prenajíma, ale aj ktorá si ho prenajíma.</span><span class="sxs-lookup"><span data-stu-id="46009-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="46009-123">V spoločnosti, ktorá prenajíma</span><span class="sxs-lookup"><span data-stu-id="46009-123">In the lending company</span></span>

1. <span data-ttu-id="46009-124">V službe Financie skontrolujte, či je vybratá spoločnosť, ktorá prenajíma, a potom dokončite postup v predchádzajúcej časti „Nastavenie pracovníka ako zdroja projektu“.</span><span class="sxs-lookup"><span data-stu-id="46009-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="46009-125">Na stránke **Účtovanie medzi spoločnosťami** vyberte možnosť **Nové**.</span><span class="sxs-lookup"><span data-stu-id="46009-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="46009-126">V poli **ID právnickej osoby** vyberte spoločnosť, ktorá prenajíma.</span><span class="sxs-lookup"><span data-stu-id="46009-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="46009-127">Vyplňte príslušné polia zodpovedajúcim spôsobom a potom vyberte položku **Uložiť a Zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="46009-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="46009-128">Na stránke **Cena transferu** vyberte možnosť **Nové**.</span><span class="sxs-lookup"><span data-stu-id="46009-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="46009-129">V poli **Právnická osoba, ktorá si prenajíma** vyberte príslušnú spoločnosť.</span><span class="sxs-lookup"><span data-stu-id="46009-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="46009-130">Ak chcete prenajať spoločnosti, ktorá si prenajíma, iba ten zdroj, ktorý ste vytvorili na začiatku tejto časti v poli **Zdroj** , vyberte názov zdroja, ktorý ste vytvorili.</span><span class="sxs-lookup"><span data-stu-id="46009-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="46009-131">Ak chcete v spoločnosti, ktorá prenajíma, sprístupniť všetky zdroje pre spoločnosť, ktorá si prenajíma, nechajte pole **Zdroje** prázdne.</span><span class="sxs-lookup"><span data-stu-id="46009-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="46009-132">Na stránke **Parametre projektového riadenia a účtovníctva** , na karte **Medzipodnikové** , nastavte možnosť **Povoliť medzipodnikové plánovanie zdrojov a časové rozvrhy** na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="46009-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="46009-133">V spoločnosti, ktorá si prenajíma</span><span class="sxs-lookup"><span data-stu-id="46009-133">In the borrowing company</span></span>

- <span data-ttu-id="46009-134">Na stránke **Zoznam zdrojov** vo filtri vyhľadávania zadajte názov zdroja, ktorý ste vytvorili pre spoločnosť, ktorá prenajíma, aby ste overili, či je uvedený v zozname zdrojov spoločnosti, ktorá si prenajíma.</span><span class="sxs-lookup"><span data-stu-id="46009-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="46009-135">Žiadosť o zdroje pre projekty</span><span class="sxs-lookup"><span data-stu-id="46009-135">Request project resources</span></span>
<span data-ttu-id="46009-136">Funkcie pre plánovanie zdrojov projektu slúži iba na to, aby správcovia zdrojov distribuovali personálne zdroje na zákazky alebo projekty.</span><span class="sxs-lookup"><span data-stu-id="46009-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="46009-137">Ak chcete povoliť túto funkciu, dokončite nasledujúce úlohy alebo skontrolujte, či boli dokončené:</span><span class="sxs-lookup"><span data-stu-id="46009-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="46009-138">Nastaviť číselné sekvencie.</span><span class="sxs-lookup"><span data-stu-id="46009-138">Set up number sequences.</span></span>
- <span data-ttu-id="46009-139">Nastavte pracovné postupy riadenia projektu a účtovníctva.</span><span class="sxs-lookup"><span data-stu-id="46009-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="46009-140">Povoliť pracovné postupy týkajúce sa požiadaviek na zdroje.</span><span class="sxs-lookup"><span data-stu-id="46009-140">Enable resource request workflows.</span></span>

<span data-ttu-id="46009-141">Po dokončení predchádzajúcich úloh môžete podľa potreby dokončiť nasledujúce úlohy:</span><span class="sxs-lookup"><span data-stu-id="46009-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="46009-142">Vytvoriť požiadavku na zdroj z personálne obsadeného zdroja s predbežnou rezerváciou.</span><span class="sxs-lookup"><span data-stu-id="46009-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="46009-143">Monitorovať požiadavky na zdroje.</span><span class="sxs-lookup"><span data-stu-id="46009-143">Monitor resource requests.</span></span>
- <span data-ttu-id="46009-144">Splniť požiadavky na zdroje.</span><span class="sxs-lookup"><span data-stu-id="46009-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="46009-145">Vyžiadajte si personálny zdroj zo štruktúry WBS.</span><span class="sxs-lookup"><span data-stu-id="46009-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="46009-146">Zarezervujte si zdroje pre projekt bez toho, aby ste museli vyžadovať personálny zdroj.</span><span class="sxs-lookup"><span data-stu-id="46009-146">Book resources to a project without having a request for a staffed resource.</span></span>
