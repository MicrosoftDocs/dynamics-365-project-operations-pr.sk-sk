---
title: Vypnutie cenovej dimenzie
description: Táto téma poskytuje informácie o vypnutí cenových dimenzií.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004550"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="c5a15-103">Vypnutie cenovej dimenzie</span><span class="sxs-lookup"><span data-stu-id="c5a15-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="c5a15-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="c5a15-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c5a15-105">Možno budete musieť skontrolovať a aktualizovať svoje cenové stratégie každých niekoľko rokov.</span><span class="sxs-lookup"><span data-stu-id="c5a15-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="c5a15-106">Všetky aktualizácie, ktoré vykonáte, môžu vyžadovať vypnutie existujúcej dimenzie cien a vytvorenie novej.</span><span class="sxs-lookup"><span data-stu-id="c5a15-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="c5a15-107">Napríklad, možno ste predtým oceňovali na základe **Roly**, ale teraz ste sa rozhodli pre cenu podľa **pracovných skúseností**.</span><span class="sxs-lookup"><span data-stu-id="c5a15-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="c5a15-108">To môže vyžadovať vypnutie **Roly** ako cenovej dimenzie a vytvorenie **Pracovnej skúsenosti** ako novej cenovej dimenzie.</span><span class="sxs-lookup"><span data-stu-id="c5a15-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="c5a15-109">Vypnutie cenovej dimenzie, bez ohľadu na to, či je predpripravená alebo vlastná, možno vykonať nastavením možnosti **Vzťahuje sa na náklady** a **Vzťahuje sa na predaj** polia dimenzie cien na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="c5a15-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="c5a15-110">Keď to však urobíte, môže sa zobraziť chybové hlásenie **Cenovú dimenziu nie je možné aktualizovať ani vymazať, ak sú priradené záznamy o cenách**.</span><span class="sxs-lookup"><span data-stu-id="c5a15-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Chyba obchodného procesu pravdepodobne pri vypnutí cenovej dimenzie](media/Business-Process-Error.png)

<span data-ttu-id="c5a15-112">Toto chybové hlásenie naznačuje, že existujú cenové záznamy, ktoré boli predtým nastavené pre dimenziu, ktorá je vypnutá.</span><span class="sxs-lookup"><span data-stu-id="c5a15-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="c5a15-113">Všetky záznamy **Cena roly** a **Prirážka k cene roly**, ktoré odkazujú na dimenziu, musia byť odstránené pred tým, ako môže byť použiteľnosť na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="c5a15-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="c5a15-114">Toto pravidlo sa vzťahuje na dimenzie cien, ktoré nie sú predpripravené, a na všetky vlastné dimenzie cien, ktoré ste mohli vytvoriť.</span><span class="sxs-lookup"><span data-stu-id="c5a15-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="c5a15-115">Dôvodom tohto overenia je, že každý **Cena roly** musí mať jedinečnú kombináciu dimenzií.</span><span class="sxs-lookup"><span data-stu-id="c5a15-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="c5a15-116">Napríklad na cenníku s názvom **US Cost Rates 2018** máte nasledovné riadky **Cena roly**.</span><span class="sxs-lookup"><span data-stu-id="c5a15-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="c5a15-117">Štandardný názov</span><span class="sxs-lookup"><span data-stu-id="c5a15-117">Standard Title</span></span>         | <span data-ttu-id="c5a15-118">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="c5a15-118">Org Unit</span></span>    |<span data-ttu-id="c5a15-119">Jednotka</span><span class="sxs-lookup"><span data-stu-id="c5a15-119">Unit</span></span>   |<span data-ttu-id="c5a15-120">Cena</span><span class="sxs-lookup"><span data-stu-id="c5a15-120">Price</span></span>  |<span data-ttu-id="c5a15-121">Mena</span><span class="sxs-lookup"><span data-stu-id="c5a15-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="c5a15-122">Systémový inžinier</span><span class="sxs-lookup"><span data-stu-id="c5a15-122">Systems Engineer</span></span>|<span data-ttu-id="c5a15-123">Contoso – USA</span><span class="sxs-lookup"><span data-stu-id="c5a15-123">Contoso US</span></span>|<span data-ttu-id="c5a15-124">Hodina</span><span class="sxs-lookup"><span data-stu-id="c5a15-124">Hour</span></span>| <span data-ttu-id="c5a15-125">100</span><span class="sxs-lookup"><span data-stu-id="c5a15-125">100</span></span>|<span data-ttu-id="c5a15-126">USD</span><span class="sxs-lookup"><span data-stu-id="c5a15-126">USD</span></span>|
| <span data-ttu-id="c5a15-127">Vyšší systémový inžinier</span><span class="sxs-lookup"><span data-stu-id="c5a15-127">Senior Systems Engineer</span></span>|<span data-ttu-id="c5a15-128">Contoso – USA</span><span class="sxs-lookup"><span data-stu-id="c5a15-128">Contoso US</span></span>|<span data-ttu-id="c5a15-129">Hodina</span><span class="sxs-lookup"><span data-stu-id="c5a15-129">Hour</span></span>| <span data-ttu-id="c5a15-130">150</span><span class="sxs-lookup"><span data-stu-id="c5a15-130">150</span></span>| <span data-ttu-id="c5a15-131">USD</span><span class="sxs-lookup"><span data-stu-id="c5a15-131">USD</span></span>|


<span data-ttu-id="c5a15-132">Keď vypnete **Štandardný názov** ako cenovú dimenziu a nástroj na určovanie cien vyhľadáva cenu, použije sa iba hodnota **Organizačná jednotka** z kontextu vstupu.</span><span class="sxs-lookup"><span data-stu-id="c5a15-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="c5a15-133">Ak je **Organizačná jednotka** vstupného kontextu „Contoso US“, výsledok nebude určujúci, pretože sa budú zhodovať obidva riadky.</span><span class="sxs-lookup"><span data-stu-id="c5a15-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="c5a15-134">Ak chcete predísť tomuto scenáru, pri záznamoch **Cena roly** systém overuje, či je kombinácia dimenzií jedinečná.</span><span class="sxs-lookup"><span data-stu-id="c5a15-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="c5a15-135">Ak je rozmer vypnutý po vytvorení záznamov **Cena roly**, toto obmedzenie môže byť porušené.</span><span class="sxs-lookup"><span data-stu-id="c5a15-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="c5a15-136">Preto je potrebné, aby ste pred vypnutím dimenzie vymazali všetky riadky **Ceny roly** a **Prirážka k cene roly**, ktoré majú vyplnenú hodnotu dimenzie.</span><span class="sxs-lookup"><span data-stu-id="c5a15-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]