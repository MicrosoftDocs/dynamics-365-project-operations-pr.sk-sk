---
title: Prehľad riadkov cenových ponúk založených na produkte – čiastočné
description: Táto téma poskytuje informácie o práci s riadkami cenovej ponuky založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29d82637c6c8bb5b5cde7707d181d5b3d3b235c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272587"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="156de-103">Prehľad riadkov cenových ponúk založených na produkte – čiastočné</span><span class="sxs-lookup"><span data-stu-id="156de-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="156de-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="156de-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="156de-105">Môžete vytvoriť riadky cenových ponúk v Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="156de-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="156de-106">Riadky cenových ponúk založených na produkte je možné pridávať ručne alebo môžu byť položkami z katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="156de-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="156de-107">Katalóg produktov</span><span class="sxs-lookup"><span data-stu-id="156de-107">Product catalog</span></span>

<span data-ttu-id="156de-108">Každý produkt v katalógu produktov má predvolenú jednotku a jednotkovú skupinu.</span><span class="sxs-lookup"><span data-stu-id="156de-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="156de-109">Ak viac produktov zdieľa rovnakú množinu atribútov, môžete vytvoriť produktovú rodinu, ktorá zdieľa tieto atribúty.</span><span class="sxs-lookup"><span data-stu-id="156de-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="156de-110">Spoločnosť napríklad predáva licencie na predplatné pre rôzne druhy softvéru.</span><span class="sxs-lookup"><span data-stu-id="156de-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="156de-111">Všetky predplatné softvéry májú nasledujúce dva atribúty:</span><span class="sxs-lookup"><span data-stu-id="156de-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="156de-112">Počet používateľov</span><span class="sxs-lookup"><span data-stu-id="156de-112">Number of users</span></span>
- <span data-ttu-id="156de-113">Trvanie predplatného merané v mesiacoch</span><span class="sxs-lookup"><span data-stu-id="156de-113">A subscription duration measured in months</span></span>

<span data-ttu-id="156de-114">Ak chcete udržiavať tento typ katalógu, vytvorte rodinu produktov s názvom **Predplatné softvéru** a ako atribúty pridajte počet používateľov a trvanie predplatného.</span><span class="sxs-lookup"><span data-stu-id="156de-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="156de-115">Ďalej môžete do rodiny produktov **Predplatné softvéru** pridať jednotlivé produkty.</span><span class="sxs-lookup"><span data-stu-id="156de-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="156de-116">Pridanie položiek katalógu produktov do projektovej cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="156de-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="156de-117">Stránky **Projektová cenová ponuka** a **Projektová zmluva** majú sekcie pre riadky založené na projekte a riadky založené na produkte.</span><span class="sxs-lookup"><span data-stu-id="156de-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="156de-118">Pre riadky založené na produkte rozbaľovací zoznam v riadku cenovej ponuky alebo riadku projektovej zmluvy obsahuje všetky produkty a jednotky v cenníku produktov.</span><span class="sxs-lookup"><span data-stu-id="156de-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="156de-119">Môžete tiež pridať produkty, ktoré nie sú súčasťou cenníka produktov.</span><span class="sxs-lookup"><span data-stu-id="156de-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="156de-120">Okrem toho môžete vybrať produkty z iných cenníkov alebo priamo z katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="156de-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="156de-121">Keď vyberiete produkty priamo z katalógu produktov, na získanie predajnej ceny produktu sa použije predvolený cenník daného produktu.</span><span class="sxs-lookup"><span data-stu-id="156de-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="156de-122">Ak predvolený cenník nie je nastavený, cena je nastavená na hodnotu nula (0).</span><span class="sxs-lookup"><span data-stu-id="156de-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="156de-123">Ak je riadok cenovej ponuky založený na katalógu produktov, predajnú cenu môžete prepísať priamo v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="156de-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="156de-124">Cenová ponuka v poli **Ceny** s dvoma dostupnými hodnotami:</span><span class="sxs-lookup"><span data-stu-id="156de-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="156de-125">**Prepísanie ceny**</span><span class="sxs-lookup"><span data-stu-id="156de-125">**Override Pricing**</span></span>
- <span data-ttu-id="156de-126">**Použiť predvolený**</span><span class="sxs-lookup"><span data-stu-id="156de-126">**Use Default**</span></span>

<span data-ttu-id="156de-127">Ak vyberiete **Prepísať ceny**, predvolená cena nie je nastavená.</span><span class="sxs-lookup"><span data-stu-id="156de-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="156de-128">Namiesto toho musíte zadať cenu produktu v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="156de-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="156de-129">Ak vyberiete **Použiť predvolené**, použije sa predvolená predajná cena a pole je pre úpravy uzamknuté.</span><span class="sxs-lookup"><span data-stu-id="156de-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="156de-130">Predvolené predajné ceny sa zapisujú do riadkov na základe produktov v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="156de-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="156de-131">Pole **Ceny** sa potom nastaví na **Prepísanie cien**, aby ste mohli upraviť predvolenú cenu v riadkoch cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="156de-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="156de-132">Toto je prepísanie riadkov založených na produktoch špecifické pre aplikáciu Project Operations v Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="156de-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]