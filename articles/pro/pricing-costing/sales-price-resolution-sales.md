---
title: Riešenie predajných cien pre odhady a skutočné hodnoty – čiastočné
description: Táto téma poskytuje informácie o tom, ako vyriešiť predajné ceny pre odhady a skutočné hodnoty.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 92cebbe851c3cface86d0580e7e060134295e8c2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176765"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a><span data-ttu-id="425a0-103">Riešenie predajných cien pre odhady a skutočné hodnoty – čiastočné</span><span class="sxs-lookup"><span data-stu-id="425a0-103">Resolve sales prices for estimates and actuals - lite</span></span>

<span data-ttu-id="425a0-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="425a0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="425a0-105">Keď sa predajné ceny na základe odhadov a skutočností vyriešia v rámci Dynamics 365 Project Operations, systém najskôr použije dátum a menu príslušnej ponuky alebo kontraktu na vyriešenie cenníka predajných cien.</span><span class="sxs-lookup"><span data-stu-id="425a0-105">When sales prices on estimates and actuals are resolved in Dynamics 365 Project Operations, the system first uses the date and currency of the related project quote or contract to resolve the sales price list.</span></span> <span data-ttu-id="425a0-106">Po vyriešení predajného cenníka systém vyrieši predajnú alebo fakturačnú sadzbu.</span><span class="sxs-lookup"><span data-stu-id="425a0-106">After the sales price list is resolved, the system resolves the sales or bill rate.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="425a0-107">Riešenie predajných sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre čas</span><span class="sxs-lookup"><span data-stu-id="425a0-107">Resolve sales rates on actual and estimate lines for time</span></span>

<span data-ttu-id="425a0-108">V rámci Project Operations sa riadky odhadu času používajú na označenie riadku ponuky a podrobností riadku kontraktu pre čas a priradenia zdrojov v projekte.</span><span class="sxs-lookup"><span data-stu-id="425a0-108">In Project Operations, estimate lines for time are used to denote the quote line and contract line details for time and the resource assignments on the project.</span></span>

<span data-ttu-id="425a0-109">Po vyriešení cenníka predaja systém dokončí nasledujúce kroky a predvolí fakturačnú sadzbu.</span><span class="sxs-lookup"><span data-stu-id="425a0-109">After a price list for sales is resolved, the system completes the following steps to default the bill rate.</span></span>

1. <span data-ttu-id="425a0-110">Systém používa polia **Rola**, **Zdrojová jednotka** a na riadku odhadu času, aby sa zhodovali s riadkami cenníka roly vo vyriešenom cenníku.</span><span class="sxs-lookup"><span data-stu-id="425a0-110">The system uses the **Role** and **Resourcing Unit** fields on the estimate line for time, to match against the role price lines in the resolved price list.</span></span> <span data-ttu-id="425a0-111">Táto zhoda predpokladá, že používate cenové dimenzie dostupné pre využívané sadzby fakturácie.</span><span class="sxs-lookup"><span data-stu-id="425a0-111">This matching assumes that out-of-box pricing dimensions for bill rates are being used.</span></span> <span data-ttu-id="425a0-112">Ak ste konfigurovali cenu na základe akýchkoľvek iných polí namiesto, alebo okrem položiek **Rola** a **Zdrojová jednotka**, tak sa na získanie zodpovedajúceho riadka s cenou roly použije iná kombinácia.</span><span class="sxs-lookup"><span data-stu-id="425a0-112">If you have configured pricing based on any other fields instead of, or in addition to **Role** and **Resourcing Unit**, then that is the combination that will be used to retrieve a matching role price line.</span></span>
2. <span data-ttu-id="425a0-113">Ak systém nájde riadok s cenou roly s fakturačnou sadzbou pre kombináciu polí **Rola** a **Zdrojová jednotka**, bude daná fakturačná sadzba predvolená.</span><span class="sxs-lookup"><span data-stu-id="425a0-113">If the system finds a role price line that has a bill rate for the **Role** and **Resourcing Unit** field combination, then that bill rate is defaulted.</span></span>
3. <span data-ttu-id="425a0-114">Ak sa systém nemôže zhodovať s hodnotami polí **Rola** a **Zdrojová jednotka**, tak načíta riadky s cenami rolí so zodpovedajúcou rolou, ale s nulovými hodnotami parametra **Zdrojová jednotka**.</span><span class="sxs-lookup"><span data-stu-id="425a0-114">If the system is unable to match the **Role** and **Resourcing Unit** field values, then it retrieves role price lines with a matching role but null values of **Resource Unit**.</span></span> <span data-ttu-id="425a0-115">Keď systém nájde záznam ceny zodpovedajúcej role, predvolene nastaví fakturačnú sadzbu z tohto záznamu.</span><span class="sxs-lookup"><span data-stu-id="425a0-115">After the system finds a matching role price record, it will default the bill rate from that record.</span></span> <span data-ttu-id="425a0-116">Toto priradenie predpokladá predpripravenú konfiguráciu relatívnej priority **Rola** vs **Zdrojová jednotka** ako dimenzia predajných cien.</span><span class="sxs-lookup"><span data-stu-id="425a0-116">This matching assumes an out-of-the-box configuration for the relative priority of **Role** vs **Resourcing Unit** as a sales pricing dimension.</span></span>

> [!NOTE]
> <span data-ttu-id="425a0-117">Ak nakonfigurujete inú prioritu pre položky **Rola** a **Zdrojová jednotka**, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, toto správanie sa zodpovedajúcim spôsobom zmení.</span><span class="sxs-lookup"><span data-stu-id="425a0-117">If you configured a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="425a0-118">Systém načítava záznamy cien rolí s hodnotami, ktoré sa zhodujú s každou z hodnôt dimenzií ceny, v poradí podľa priority s riadkami, ktoré majú nulové hodnoty pre tieto dimenzie prichádzajúce ako posledné.</span><span class="sxs-lookup"><span data-stu-id="425a0-118">The system retrieves the role price records with matching values of each of the pricing dimension values in the order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="425a0-119">Riešenie predajných sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre výdavky</span><span class="sxs-lookup"><span data-stu-id="425a0-119">Resolve sales rates on actual and estimate lines for expense</span></span>

<span data-ttu-id="425a0-120">V rámci Project Operations sa riadky odhadu výdavkov používajú na označenie riadku ponuky a podrobností riadku kontraktu pre výdavky a riadok s odhadom výdavkov v projekte.</span><span class="sxs-lookup"><span data-stu-id="425a0-120">In Project Operations, estimate lines for expense are used to denote the quote line and contract line details for expenses and the expense estimate lines on the project.</span></span>

<span data-ttu-id="425a0-121">Po vyriešení cenníka predaja systém dokončí nasledujúce kroky a predvolí fakturačnú predajnú jednotkovú sadzbu.</span><span class="sxs-lookup"><span data-stu-id="425a0-121">After a price list for sales is resolved, the system completes the following steps to default the unit sales price.</span></span>

1. <span data-ttu-id="425a0-122">Po vyriešení cenníka nákladov systém použije kombináciu polí **Kategória** a **Jednotka** pre kombináciu poľa a odhadu nákladov, ktorý sa zhoduje s riadkami ceny kategórie vo vyriešenom cenníku.</span><span class="sxs-lookup"><span data-stu-id="425a0-122">The system uses the **Category** and **Unit** field combination on the estimate line for expense to match against the category price lines in the price list that was resolved.</span></span>
2. <span data-ttu-id="425a0-123">Ak systém nájde riadok s cenou kategórie, ktorá má predajnú sadzbu pre kombináciu polí **Kategória** a **Jednotka**, predajná sadzba bude predvolená.</span><span class="sxs-lookup"><span data-stu-id="425a0-123">If the system finds a category price line that has a sales rate for the **Category** and **Unit** field combination, then that sales rate is defaulted.</span></span>
3. <span data-ttu-id="425a0-124">Ak systém nájde cenový riadok zodpovedajúcej kategórie, môže sa na predvolenie predajnej ceny použiť metóda určovania cien.</span><span class="sxs-lookup"><span data-stu-id="425a0-124">If the system finds a matching category price line, the pricing method may be used to default the sales price.</span></span> <span data-ttu-id="425a0-125">Nasledujúca tabuľka nižšie zobrazuje predvolené správanie ceny výdavkov v Project Operations.</span><span class="sxs-lookup"><span data-stu-id="425a0-125">The following table below shows the expense price defaulting behavior in Project Operations.</span></span>

    | <span data-ttu-id="425a0-126">Kontext</span><span class="sxs-lookup"><span data-stu-id="425a0-126">Context</span></span> | <span data-ttu-id="425a0-127">Spôsob oceňovania</span><span class="sxs-lookup"><span data-stu-id="425a0-127">Pricing method</span></span> | <span data-ttu-id="425a0-128">Predvolená cena</span><span class="sxs-lookup"><span data-stu-id="425a0-128">Price defaulted</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="425a0-129">Odhadované</span><span class="sxs-lookup"><span data-stu-id="425a0-129">Estimate</span></span> | <span data-ttu-id="425a0-130">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="425a0-130">Price per unit</span></span> | <span data-ttu-id="425a0-131">Na základe riadka kategórie ceny</span><span class="sxs-lookup"><span data-stu-id="425a0-131">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="425a0-132">V rámci nákladov</span><span class="sxs-lookup"><span data-stu-id="425a0-132">At cost</span></span> | <span data-ttu-id="425a0-133">0.00</span><span class="sxs-lookup"><span data-stu-id="425a0-133">0.00</span></span> |
    | &nbsp; | <span data-ttu-id="425a0-134">Prirážka nad rámec nákladov</span><span class="sxs-lookup"><span data-stu-id="425a0-134">Markup over cost</span></span> | <span data-ttu-id="425a0-135">0.00</span><span class="sxs-lookup"><span data-stu-id="425a0-135">0.00</span></span> |
    | <span data-ttu-id="425a0-136">Skutočnosť</span><span class="sxs-lookup"><span data-stu-id="425a0-136">Actual</span></span> | <span data-ttu-id="425a0-137">Cena za jednotku</span><span class="sxs-lookup"><span data-stu-id="425a0-137">Price per unit</span></span> | <span data-ttu-id="425a0-138">Na základe riadka kategórie ceny</span><span class="sxs-lookup"><span data-stu-id="425a0-138">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="425a0-139">V rámci nákladov</span><span class="sxs-lookup"><span data-stu-id="425a0-139">At cost</span></span> | <span data-ttu-id="425a0-140">Na základe súvisiacej skutočnej ceny</span><span class="sxs-lookup"><span data-stu-id="425a0-140">Based on the related cost actual</span></span> |
    | &nbsp; | <span data-ttu-id="425a0-141">Prirážka nad rámec nákladov</span><span class="sxs-lookup"><span data-stu-id="425a0-141">Markup over cost</span></span> | <span data-ttu-id="425a0-142">Uplatnením prirážky definovanej v riadku ceny kategórie na sadzbu jednotkových nákladov súvisiacej skutočnej ceny</span><span class="sxs-lookup"><span data-stu-id="425a0-142">Apply a markup as defined by the category price line on the unit cost rate of the related cost actual</span></span> |

4. <span data-ttu-id="425a0-143">Ak systém nedokáže priradiť hodnoty polí **Kategória** a **Jednotka**, sadzba predaja je predvolene nastavená na nulu (0).</span><span class="sxs-lookup"><span data-stu-id="425a0-143">If the system is unable to match the **Category** and **Unit** field values, the sales rate defaults to zero(0).</span></span>