---
title: Nastavenie predajného cenníka
description: Táto téma poskytuje informácie o cenníkoch predaja pre naceňovanie projektov.
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
ms.openlocfilehash: 712dedb6766ff36181e261a66f3af99469449574
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004910"
---
# <a name="set-up-a-sales-price-list"></a><span data-ttu-id="e5bf1-103">Nastavenie predajného cenníka</span><span class="sxs-lookup"><span data-stu-id="e5bf1-103">Set up a sales price list</span></span>

<span data-ttu-id="e5bf1-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="e5bf1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5bf1-105">V prípade projektových ponúk a zmlúv má cenník projektu odlišný vzor prepísania ceny ako cenník produktov.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="e5bf1-106">V radku cenovej ponuky založenej na katalógu produktov, môžete prepísať cenu do rolí a kategórií priamo v riadku cenovej ponuky, pretože každý riadok cenovej ponuky poukazuje na presne jednu položku katalógu.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="e5bf1-107">V riadku cenovej ponuky založenej na projekte však nie je možné prepísať cenu na roly a kategórie priamo v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="e5bf1-108">Môžete použiť cenník projektu na prácu s dvoma odlišnými vzormi prepísania.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="e5bf1-109">Odporúčame, že máte samostatný cenník pre vaše projektové zdroje a položky katalógu, kvôli rozdielom v správaní medzi oboma pri prepismi cenotvorby.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="e5bf1-110">Každá z nasledujúcich entít môže mať jednu alebo viac priradených predajných cenníkov pre cenotvorbu projektu:</span><span class="sxs-lookup"><span data-stu-id="e5bf1-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="e5bf1-111">Zákaznícke (konto)</span><span class="sxs-lookup"><span data-stu-id="e5bf1-111">Customer (account)</span></span> 
- <span data-ttu-id="e5bf1-112">Príležitosť</span><span class="sxs-lookup"><span data-stu-id="e5bf1-112">Opportunity</span></span> 
- <span data-ttu-id="e5bf1-113">Cenová ponuka</span><span class="sxs-lookup"><span data-stu-id="e5bf1-113">Quote</span></span> 
- <span data-ttu-id="e5bf1-114">Projektová zmluva</span><span class="sxs-lookup"><span data-stu-id="e5bf1-114">Project Contract</span></span>

<span data-ttu-id="e5bf1-115">Združenie týchto entít s cenníkmi je indikované projektovými cenníkmi.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="e5bf1-116">Môžete priradiť jeden alebo viac cenníkov s entitami zákazníka, príležitosti, cenovej ponuky a projektovej predajnej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="e5bf1-117">Predvolený zoznam projektových cenníkov nie je automaticky zadaný v zázname zákazníka.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="e5bf1-118">Zoznam projektových cenníkov však môžete manuálne priložiť k záznamu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="e5bf1-119">Avšak, mali by ste manuálne priložiť projektový cenník len vtedy, ak máte vlastnú cenovú dohodu so zákazníkom.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="e5bf1-120">Ak je zoznam projektových cenníkov pripojený k predajnej entite, overujú sa nasledujúce informácie:</span><span class="sxs-lookup"><span data-stu-id="e5bf1-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="e5bf1-121">Cenník má kontext **Predaj**.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="e5bf1-122">Mena zákazníka sa musí zhodovať s menou uvedenou v cenníku.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="e5bf1-123">Na projektovej zmluve sa používa nasledujúce poradie priority na automatické nastavenie súvisiacich projektových cenníkov:</span><span class="sxs-lookup"><span data-stu-id="e5bf1-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="e5bf1-124">Ponuka</span><span class="sxs-lookup"><span data-stu-id="e5bf1-124">Quote</span></span>
2. <span data-ttu-id="e5bf1-125">Príležitosť</span><span class="sxs-lookup"><span data-stu-id="e5bf1-125">Opportunity</span></span>
3. <span data-ttu-id="e5bf1-126">Zákazník</span><span class="sxs-lookup"><span data-stu-id="e5bf1-126">Customer</span></span> 
4. <span data-ttu-id="e5bf1-127">Globálne nastavenia</span><span class="sxs-lookup"><span data-stu-id="e5bf1-127">Global settings</span></span> 

<span data-ttu-id="e5bf1-128">Ak je projektový cenník predvolene zadaný, systém overí, či mena zodpovedá mene zákazníka, a či predvolené cenníky, ktoré boli zadané, majú kontext **Predaj**.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="e5bf1-129">Môžete priradiť viacero cenníkov s entitami zákazníka, príležitosti, cenovej ponuky a projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="e5bf1-130">Táto funkcia podporuje predvolený dátum predvolené ceny pre dlho-bežiaci projekt zmluvy, kde môžete požadovať viac ako jeden cenník na účet pre cenové aktualizácie, ktoré nastanú z dôvodu inflácie.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="e5bf1-131">Ak však cenové zoznamy, ktoré priradíte k entite zákazník, príležitosť, cenová ponuka alebo zmluva o projekte, majú prekrývajúcu sa účinnosť dátumu, predvolené ceny môžu byť nesprávne.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="e5bf1-132">Preto by ste sa mali uistiť, že projektové cenníky, ktoré majú prekrývanie dátumovej efektívnosti nie sú spojené s týmito entitami.</span><span class="sxs-lookup"><span data-stu-id="e5bf1-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]