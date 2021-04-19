---
title: Cenníky produktov
description: Táto téma poskytuje informácie o cenníkoch v katalógových cenách používaných pre projektové cenové ponuky a zmluvy.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877509"
---
# <a name="product-price-lists"></a><span data-ttu-id="d4eb8-103">Cenníky produktov</span><span class="sxs-lookup"><span data-stu-id="d4eb8-103">Product price lists</span></span>

<span data-ttu-id="d4eb8-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="d4eb8-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="d4eb8-105">V Project Operations **Cenníky produktov** a súvisiace entity položiek cenníka podporujú funkciu určovania cien produktov na základe riadkov produktových cenových ponúk a zmlúv.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="d4eb8-106">Pri produktoch použitých v projektoch sa používajú záznamy položiek v cenníku pre cenníky projektov.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="d4eb8-107">Produkty by mali byť nastavené tak, aby mali predvolené náklady a cenníky v katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="d4eb8-108">Ak chcete konfigurovať predvolené náklady a cenník, použite cenník, štandardné náklady a obstarávaciu cenu.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="d4eb8-109">Predvolený cenník sa používa v riadku cenovej ponuky alebo v riadku projektovej zmluvy iba vtedy, keď systém nemôže nájsť riadok cenníka pre daný produkt v cenovom zozname produktov pre cenovú ponuku alebo projektovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="d4eb8-110">Nákladová cena riadkov katalógu produktov sa môže zmeniť medzi cenovými ponukami.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="d4eb8-111">Táto schopnosť je dôležitá, pretože ak nechcete presne sledovať náklady, nemôžete určiť prevádzkové zisky na projektových angažmánoch.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="d4eb8-112">Predvolene sú štandardné náklady na produkt použíté ako obstarávacia cena.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="d4eb8-113">Predvolená cena však môže byť aktualizovaná v riadku cenovej ponuky, ak je pre túto cenovú ponuku odlišná cena.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="d4eb8-114">Položky v cenníku</span><span class="sxs-lookup"><span data-stu-id="d4eb8-114">Price list items</span></span>

<span data-ttu-id="d4eb8-115">Produkty z katalógu produktov môžete pridať do rôznych cenníkov.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="d4eb8-116">Riadky cenníka pre produkty vždy odkazujú na konkrétnu jednotku.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="d4eb8-117">Ceny za produkt na položkách cenníka možno konfigurovať ako čiastku meny.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="d4eb8-118">Alternatívne môže byť nakonfigurovaný ako funkcia cenník, aktuálna cena, alebo štandardná cena.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="d4eb8-119">Funkcia určovania cien podporuje rôzne možnosti zaokrúhľovania, keď sú ceny produktov nakonfigurované ako funkcia cenníka, štandardných nákladov alebo aktuálnych cien.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="d4eb8-120">Okrem užívania viacerých cenových metód a možností zaokrúhľovania môžete priradiť zoznamy zliav k položkám cenníka.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="d4eb8-121">Predvolený cenník produktov.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-121">Default product price list</span></span>
<span data-ttu-id="d4eb8-122">Každý záznam zákazníka má **predvolené pole cenníka**, kde môžete zadať cenník, ktorý zodpovedá mene zákazníka.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="d4eb8-123">V tomto poli sa automaticky nezadá predvolená hodnota.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="d4eb8-124">Ak existuje vlastná cenová zmluva s konkrétnym zákazníkom, môžete použiť toto pole na priradenie cenníka k danému zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="d4eb8-125">Príležitosti, cenová ponuka a pEntityrojektové zmluvy používajú nasledovný príkaz na zadanie predvolených cenníkov produktov.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="d4eb8-126">Rovnaká objednávka sa používa pre projektové cenníky.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="d4eb8-127">Ponuka</span><span class="sxs-lookup"><span data-stu-id="d4eb8-127">Quote</span></span>
2.  <span data-ttu-id="d4eb8-128">Príležitosť</span><span class="sxs-lookup"><span data-stu-id="d4eb8-128">Opportunity</span></span>
3.  <span data-ttu-id="d4eb8-129">Zákazník</span><span class="sxs-lookup"><span data-stu-id="d4eb8-129">Customer</span></span>
4.  <span data-ttu-id="d4eb8-130">Globálne nastavenia</span><span class="sxs-lookup"><span data-stu-id="d4eb8-130">Global settings</span></span> 

<span data-ttu-id="d4eb8-131">V predvolenom nastavení obsahuje pole **produkt** v riadku cenovej ponuky všetky aktívne produkty v cenníkoch produktov cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="d4eb8-132">Ak bol produkt inaktivovaný, alebo ak ide o koncept produktu, nie je uvedený v zozname, a to ani v prípade, že je v cenníku.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="d4eb8-133">Riadky katalógu produktov sa pridajú ako riadky faktúry na prvej faktúre vytvorenej pre projektovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="d4eb8-134">V návrhu faktúry možno tieto riadky faktúry odstrániť.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="d4eb8-135">V takom prípade sa riadky zobrazia na nasledujúcej faktúre, až kým nebudú fakturované, alebo kým sa faktúra neodošle zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="d4eb8-136">Nie je možné fakturovať čiastočné množstvo riadka faktúry produktu.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="d4eb8-137">Po fakturácii riadkov produktov z projektovej zmluvy sa vytvoria skutočné hodnoty.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="d4eb8-138">Tieto skutočné hodnoty však nie sú prepojené s entitou súvisiaceho projektu.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="d4eb8-139">Inými slovami, riadky projektových zmlúv na základe produktu sú nezávislé od akýchkoľvek projektových použití.</span><span class="sxs-lookup"><span data-stu-id="d4eb8-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
