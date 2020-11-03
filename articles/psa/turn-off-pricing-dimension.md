---
title: Vypnutie cenovej dimenzie
description: Táto téma ukazuje, ako nastaviť dimenzie cien v riešení Project Service.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 1ae95430c368370145c7081a5d94d6161a7700b4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084449"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="19110-103">Vypnutie cenovej dimenzie</span><span class="sxs-lookup"><span data-stu-id="19110-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="19110-104">Možno budete musieť skontrolovať a aktualizovať svoje cenové stratégie každých niekoľko rokov.</span><span class="sxs-lookup"><span data-stu-id="19110-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="19110-105">Všetky aktualizácie, ktoré vykonáte, môžu vyžadovať vypnutie existujúcej dimenzie cien a vytvorenie novej.</span><span class="sxs-lookup"><span data-stu-id="19110-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="19110-106">Napríklad, možno ste predtým oceňovali na základe **Roly** , ale teraz ste sa rozhodli pre cenu podľa **pracovných skúseností**.</span><span class="sxs-lookup"><span data-stu-id="19110-106">For example, you may have previously priced by **Role** , but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="19110-107">To môže vyžadovať vypnutie **Role** ako cenovej dimenzie a vytvorenie **pracovných skúseností** ako novej cenovej dimenzie.</span><span class="sxs-lookup"><span data-stu-id="19110-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="19110-108">Vypnutie cenovej dimenzie, bez ohľadu na to, či je predpripravená alebo vlastná, možno vykonať nastavením možnosti **Vzťahuje sa na náklady** a **Vzťahuje sa na predaj** polia dimenzie cien na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="19110-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="19110-109">Avšak, keď to urobíte, môže sa zobraziť nasledujúce chybové hlásenie.</span><span class="sxs-lookup"><span data-stu-id="19110-109">However, when you do this, you might receive the following error message.</span></span>

![Chyba obchodného procesu pravdepodobne pri vypnutí cenovej dimenzie](media/Business-Process-Error.png)


<span data-ttu-id="19110-111">Toto chybové hlásenie naznačuje, že existujú cenové záznamy, ktoré boli predtým nastavené pre dimenziu, ktorá je vypnutá.</span><span class="sxs-lookup"><span data-stu-id="19110-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="19110-112">Všetky záznamy **Cena roly** a **Prirážka k cene roly** , ktoré odkazujú na dimenziu, musia byť odstránené pred tým, ako môže byť použiteľnosť na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="19110-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="19110-113">Toto pravidlo sa vzťahuje na dimenzie cien, ktoré nie sú predpripravené, a na všetky vlastné dimenzie cien, ktoré ste mohli vytvoriť.</span><span class="sxs-lookup"><span data-stu-id="19110-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="19110-114">Dôvodom tohto overenia je, že Project Service má obmedzenie, aby každý záznam **Cena roly** mal jedinečnú kombináciu dimenzií.</span><span class="sxs-lookup"><span data-stu-id="19110-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="19110-115">Napríklad na cenníku s názvom **US Cost Rates 2018** máte nasledovné riadky **Cena roly**.</span><span class="sxs-lookup"><span data-stu-id="19110-115">For example, on a price list called **US Cost Rates 2018** , you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="19110-116">Štandardný názov</span><span class="sxs-lookup"><span data-stu-id="19110-116">Standard Title</span></span>         | <span data-ttu-id="19110-117">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="19110-117">Org Unit</span></span>    |<span data-ttu-id="19110-118">Jednotka</span><span class="sxs-lookup"><span data-stu-id="19110-118">Unit</span></span>   |<span data-ttu-id="19110-119">Cena</span><span class="sxs-lookup"><span data-stu-id="19110-119">Price</span></span>  |<span data-ttu-id="19110-120">Mena</span><span class="sxs-lookup"><span data-stu-id="19110-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="19110-121">Systémový inžinier</span><span class="sxs-lookup"><span data-stu-id="19110-121">Systems Engineer</span></span>|<span data-ttu-id="19110-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="19110-122">Contoso US</span></span>|<span data-ttu-id="19110-123">Hour</span><span class="sxs-lookup"><span data-stu-id="19110-123">Hour</span></span>| <span data-ttu-id="19110-124">100</span><span class="sxs-lookup"><span data-stu-id="19110-124">100</span></span>|<span data-ttu-id="19110-125">USD</span><span class="sxs-lookup"><span data-stu-id="19110-125">USD</span></span>|
| <span data-ttu-id="19110-126">Vyšší systémový inžinier</span><span class="sxs-lookup"><span data-stu-id="19110-126">Senior Systems Engineer</span></span>|<span data-ttu-id="19110-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="19110-127">Contoso US</span></span>|<span data-ttu-id="19110-128">Hour</span><span class="sxs-lookup"><span data-stu-id="19110-128">Hour</span></span>| <span data-ttu-id="19110-129">150</span><span class="sxs-lookup"><span data-stu-id="19110-129">150</span></span>| <span data-ttu-id="19110-130">USD</span><span class="sxs-lookup"><span data-stu-id="19110-130">USD</span></span>|


<span data-ttu-id="19110-131">Keď vypnete **štandardný názov** ako cenový rozmer a nástroj na určovanie cien Project Service vyhľadáva cenu, použije sa iba hodnota **Organizačná jednotka** z kontextu vstupu.</span><span class="sxs-lookup"><span data-stu-id="19110-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="19110-132">Ak je **Organizačná jednotka** vstupného kontextu “Contoso US”, výsledok nebude určujúci, pretože sa budú zhodovať obidva riadky.</span><span class="sxs-lookup"><span data-stu-id="19110-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="19110-133">Ak chcete predísť tomuto scenáru, pri záznamoch **Cena roly** , Project Service overuje, že kombinácia dimenzií je jedinečná.</span><span class="sxs-lookup"><span data-stu-id="19110-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="19110-134">Ak je rozmer vypnutý po vytvorení záznamov **Cena roly** , toto obmedzenie môže byť porušené.</span><span class="sxs-lookup"><span data-stu-id="19110-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="19110-135">Preto je potrebné, aby ste pred vypnutím dimenzie vymazali všetky riadky **Ceny roly** a **Prirážka k cene roly** , ktoré majú vyplnenú hodnotu dimenzie.</span><span class="sxs-lookup"><span data-stu-id="19110-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

