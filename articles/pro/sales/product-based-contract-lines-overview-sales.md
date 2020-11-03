---
title: Prehľad riadkov zmlúv založených na produkte
description: Táto téma poskytuje informácie o riadkoch zmluvy založenej na produkte.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 794a80b0dd6b8717b43e712b96b9ac077517c226
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084291"
---
# <a name="product-based-contract-lines-overview"></a><span data-ttu-id="eef0f-103">Prehľad riadkov zmlúv založených na produkte</span><span class="sxs-lookup"><span data-stu-id="eef0f-103">Product-based contract lines overview</span></span>

<span data-ttu-id="eef0f-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="eef0f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eef0f-105">V Dynamics 365 Project Operations môžete vytvárať produktové riadky zmluvy.</span><span class="sxs-lookup"><span data-stu-id="eef0f-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="eef0f-106">Produktové riadky zmlúv môžu byť manuálne vytvorenými riadkami alebo môžu byť položkami z katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="eef0f-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="eef0f-107">Katalóg produktov</span><span class="sxs-lookup"><span data-stu-id="eef0f-107">Product catalog</span></span>

<span data-ttu-id="eef0f-108">Produkty v katalógu produktov majú predvolenú jednotku a jednotkovú skupinu.</span><span class="sxs-lookup"><span data-stu-id="eef0f-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="eef0f-109">Ak niekoľko produktov zdieľa rovnakú množinu atribútov, môžete vytvoriť produktovú rodinu, ktorá má tiež tieto atribúty.</span><span class="sxs-lookup"><span data-stu-id="eef0f-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="eef0f-110">Všetky produkty v jednej produktovej rodine zdedia rovnakú množinu atribútov.</span><span class="sxs-lookup"><span data-stu-id="eef0f-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="eef0f-111">Spoločnosť napríklad predáva licencie na predplatné pre rôzne druhy softvéru.</span><span class="sxs-lookup"><span data-stu-id="eef0f-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="eef0f-112">Všetky predplatné softvéry májú nasledujúce dva atribúty:</span><span class="sxs-lookup"><span data-stu-id="eef0f-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="eef0f-113">Počet používateľov</span><span class="sxs-lookup"><span data-stu-id="eef0f-113">Number of users</span></span>
- <span data-ttu-id="eef0f-114">Trvanie predplatného (v mesiacoch)</span><span class="sxs-lookup"><span data-stu-id="eef0f-114">Subscription duration (in months)</span></span>

<span data-ttu-id="eef0f-115">Ak chcete zachovať tento typ katalógu, vytvorte rodinu produktov s názvom **Predplatený softvér**.</span><span class="sxs-lookup"><span data-stu-id="eef0f-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="eef0f-116">Pridajte atribúty **Počet používateľov** a **Trvanie predplatného** do rodiny výrobkov.</span><span class="sxs-lookup"><span data-stu-id="eef0f-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="eef0f-117">Potom pridajte jednotlivé produkty do produktovej rodiny **Predplatený softvér**.</span><span class="sxs-lookup"><span data-stu-id="eef0f-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="eef0f-118">Pridanie položiek katalógu produktov k projektovej zmluve</span><span class="sxs-lookup"><span data-stu-id="eef0f-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="eef0f-119">Projektové zmluvy majú sekcie pre dva typy riadkov: riadky založené na projekte a založené na produkte.</span><span class="sxs-lookup"><span data-stu-id="eef0f-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="eef0f-120">Produktové rady zahŕňajú všetky produkty a jednotky uvedené v cenníku produktov na zmluve.</span><span class="sxs-lookup"><span data-stu-id="eef0f-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="eef0f-121">Možno pridávať produkty, ktoré nie sú súčasťou produktového cenníka zmluvy.</span><span class="sxs-lookup"><span data-stu-id="eef0f-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="eef0f-122">Produkty si môžete vybrať z iných cenníkov alebo priamo z produktového katalógu.</span><span class="sxs-lookup"><span data-stu-id="eef0f-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="eef0f-123">Keď vyberiete produkty priamo z katalógu produktov, na získanie predajnej ceny produktu sa použije predvolený cenník daného produktu.</span><span class="sxs-lookup"><span data-stu-id="eef0f-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="eef0f-124">Ak predvolený cenník nie je nastavený, cena je nastavená na hodnotu 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="eef0f-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="eef0f-125">Ak je riadok zmluvy založený na katalógu produktov, predajnú cenu môžete prepísať priamo v riadku.</span><span class="sxs-lookup"><span data-stu-id="eef0f-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="eef0f-126">Riadok zmluvy disponuje poľom **Tvorba ceny** s dvomi hodnotami:</span><span class="sxs-lookup"><span data-stu-id="eef0f-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="eef0f-127">**Prepíšte cenu**</span><span class="sxs-lookup"><span data-stu-id="eef0f-127">**Override pricing**</span></span>
- <span data-ttu-id="eef0f-128">**Použiť predvolenú hodnotu**</span><span class="sxs-lookup"><span data-stu-id="eef0f-128">**Use default**</span></span>

<span data-ttu-id="eef0f-129">Ak nastavíte toto pole **Tvorba ceny** na **Prepísať cenu** , predvolená cena sa nenastaví.</span><span class="sxs-lookup"><span data-stu-id="eef0f-129">If you set the **Pricing** field to **Override pricing** , the default price isn't set.</span></span> <span data-ttu-id="eef0f-130">Do riadka zmluvy zadajte cenu produktu.</span><span class="sxs-lookup"><span data-stu-id="eef0f-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="eef0f-131">Ak nastavíte pole na **Použiť predvolené** , použije sa predvolená predajná cena a pole nebude možné upraviť.</span><span class="sxs-lookup"><span data-stu-id="eef0f-131">If you set the field to **Use default** , the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="eef0f-132">Po nainštalovaní Project Operations sa predvolené predajné ceny zapisujú do riadkov na základe zmluvy.</span><span class="sxs-lookup"><span data-stu-id="eef0f-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="eef0f-133">Pole **Ceny** sa potom nastaví na **Prepíšte cenu** , aby ste mohli upraviť predvolenú cenu v riadkoch zmluvy.</span><span class="sxs-lookup"><span data-stu-id="eef0f-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="eef0f-134">Toto je špecifické prepísanie v rámci Project Operations na produktoch v aplikácii Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="eef0f-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
