---
title: Zobrazuje riadky cenovej ponuky založené na produkte.
description: Táto téma poskytuje informácie o riadkoch cenovej ponuky založenej na produkte.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084544"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="a6dec-103">Zobrazuje riadky cenovej ponuky založené na produkte.</span><span class="sxs-lookup"><span data-stu-id="a6dec-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="a6dec-104">Môžete vytvoriť riadky cenových ponúk v Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="a6dec-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="a6dec-105">Riadky cenových ponúk založené na produkte môžu byť riadky "Write-in" alebo môžu byť položkami z katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="a6dec-106">Katalóg produktov</span><span class="sxs-lookup"><span data-stu-id="a6dec-106">Product catalog</span></span>

<span data-ttu-id="a6dec-107">Produkty v katalógu produktov Dynamics 365 majú predvolenú jednotku a jednotkovú skupinu.</span><span class="sxs-lookup"><span data-stu-id="a6dec-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="a6dec-108">Ak niekoľko produktov zdieľa rovnakú množinu atribútov, môžete vytvoriť produktovú rodinu, ktorá má tiež tieto atribúty.</span><span class="sxs-lookup"><span data-stu-id="a6dec-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="a6dec-109">Všetky produkty v jednej produktovej rodine zdedia rovnakú množinu atribútov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="a6dec-110">Spoločnosť napríklad predáva licencie na predplatné pre celý rad softvéru.</span><span class="sxs-lookup"><span data-stu-id="a6dec-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="a6dec-111">Všetky predplatné softvéry májú nasledujúce dva atribúty:</span><span class="sxs-lookup"><span data-stu-id="a6dec-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="a6dec-112">Počet používateľov</span><span class="sxs-lookup"><span data-stu-id="a6dec-112">Number of users</span></span> 
- <span data-ttu-id="a6dec-113">Trvanie predplatného (v mesiacoch)</span><span class="sxs-lookup"><span data-stu-id="a6dec-113">Subscription duration (in months)</span></span>

<span data-ttu-id="a6dec-114">Dobrým spôsobom, ako zachovať tento typ katalógu, je vytvorenie produktovej rodiny, ktorá je pomenovaná **predplatným softvérom** , a ktorá má **počet používateľov** a **trvanie predplatného** ako atribúty.</span><span class="sxs-lookup"><span data-stu-id="a6dec-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software** , and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="a6dec-115">Potom môžete pridať jednotlivé produkty, ako je napríklad **Dynamics 365 Sales** alebo **Dynamics 365 Field Service** do **predplatenej softvérovej** rodiny produktov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="a6dec-116">Pridanie položiek katalógu produktov do projektovej ponuky</span><span class="sxs-lookup"><span data-stu-id="a6dec-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="a6dec-117">Projektová ponuka a strany projektovej zmluvy majú sekcie pre dva typy riadkov: riadky založené na projekte a založené na produkte.</span><span class="sxs-lookup"><span data-stu-id="a6dec-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="a6dec-118">Pre riadky založené na produkte sa Dynamics 365 používa na pridávanie položiek z katalógu produktov do cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="a6dec-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="a6dec-119">Rozbaľovací zoznam v riadku cenovej ponuky alebo projektovej zmluvy obsahuje všetky produkty a jednotky v cenníku produktov, ktorý je priložený k cenovej ponuke alebo projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="a6dec-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="a6dec-120">Môžete tiež pridať produkty, ktoré nie sú súčasťou cenovej ponuky cenníka produktov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="a6dec-121">Okrem toho môžete vybrať produkty z iných cenníkov, alebo môžete vybrať produkty priamo z katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="a6dec-122">Keď vyberiete produkty priamo z katalógu produktov, na získanie predajnej ceny produktu sa použije predvolený cenník daného produktu.</span><span class="sxs-lookup"><span data-stu-id="a6dec-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="a6dec-123">Ak predvolený cenník nie je nastavený, cena je nastavená na hodnotu 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="a6dec-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="a6dec-124">Ak je riadok cenovej ponuky založený na katalógu produktov, predajnú cenu môžete prepísať priamo v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="a6dec-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="a6dec-125">Všimnite si, že riadok cenovej ponuky v Dynamics 365 má **cenové** pole.</span><span class="sxs-lookup"><span data-stu-id="a6dec-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="a6dec-126">K dispozícii sú dve hodnoty:</span><span class="sxs-lookup"><span data-stu-id="a6dec-126">Two values are available:</span></span>

- <span data-ttu-id="a6dec-127">Prepíšte cenu</span><span class="sxs-lookup"><span data-stu-id="a6dec-127">Override pricing</span></span>  
- <span data-ttu-id="a6dec-128">Použite predvolenú hodnotu</span><span class="sxs-lookup"><span data-stu-id="a6dec-128">Use default</span></span>

<span data-ttu-id="a6dec-129">Ak nastavíte toto pole na **prepísať ceny** , Dynamics 365 nenastaví predvolenú cenu.</span><span class="sxs-lookup"><span data-stu-id="a6dec-129">If you set this field to **Override pricing** , Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="a6dec-130">Musíte zadať cenu produktu v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="a6dec-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="a6dec-131">Ak nastavíte toto pole na **používať predvolené nastavenia** , Dynamics 365 použije predvolenú predajnú cenu a uzamkne pole, aby sa zabránilo úpravám.</span><span class="sxs-lookup"><span data-stu-id="a6dec-131">If you set this field to **Use default** , Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="a6dec-132">Po nainštalovaní PSA sa predvolené predajné ceny zapisujú do riadkov na základe produktov v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="a6dec-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="a6dec-133">Pole **ceny** sa potom nastaví na **prepísanie cien** , aby ste mohli upraviť predvolenú cenu v riadkoch cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="a6dec-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Nastavte prepisovanie cien](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="a6dec-135">Množstvo faktorov pre výrobky</span><span class="sxs-lookup"><span data-stu-id="a6dec-135">Quantity factors for products</span></span>

<span data-ttu-id="a6dec-136">PSA používa množstvo faktorov na podporu predaja produktov založených na predplatnom.</span><span class="sxs-lookup"><span data-stu-id="a6dec-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="a6dec-137">V prípade produktov založených na predplatnom sa množstvo v riadku cenovej ponuky alebo projektu vyjadrí ako počet používateľských mesiacov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="a6dec-138">Zvyčajne je cena predplatného softvéru uložená v katalógu ako cena za používateľa mesačne.</span><span class="sxs-lookup"><span data-stu-id="a6dec-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="a6dec-139">Avšak, môžete použiť iné časové popisy.</span><span class="sxs-lookup"><span data-stu-id="a6dec-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="a6dec-140">Počas predajného procesu je cena v riadku cenovej ponuky zvyčajne cena za používateľa, za mesiac, ktorá bola dohodnutá a zľavnená agentom predaja IT.</span><span class="sxs-lookup"><span data-stu-id="a6dec-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="a6dec-141">Každý obchod má iný počet užívateľov a iný počet predplatných mesiacov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="a6dec-142">Množstvo, ktoré sa používa na výpočet čiastky riadka cenovej ponuky, je produktom počtu používateľov a počtu mesiacov predplatného.</span><span class="sxs-lookup"><span data-stu-id="a6dec-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="a6dec-143">Na podporu tohto druhu predaja, PSA predstavil koncept kvantity faktorov.</span><span class="sxs-lookup"><span data-stu-id="a6dec-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="a6dec-144">Množstvo faktorov sa spolieha na atribúty v Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="a6dec-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="a6dec-145">Keď nakonfigurujete špecifické vlastnosti produktu, PSA vám umožní označiť podmnožinu týchto vlastností alebo všetky vlastnosti ako množstevné faktory.</span><span class="sxs-lookup"><span data-stu-id="a6dec-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="a6dec-146">PSA overuje, že iba číselné vlastnosti alebo vlastnosti produktu, ktoré majú číselný typ údajov, sú označené ako množstevné faktory.</span><span class="sxs-lookup"><span data-stu-id="a6dec-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="a6dec-147">Ak je produkt, na ktorý sú nakonfigurované množstevné faktory, pridaný do riadka cenovej ponuky, pole **množstvo** v riadku cenovej ponuky sa stáva poľom iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="a6dec-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="a6dec-148">Po zadaní hodnôt pre vlastnosti produktu, ktoré sú množstevné faktory, PSA vypočíta množstvo riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="a6dec-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="a6dec-149">Napríklad, Dynamics 365 môže mať nasledujúce vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="a6dec-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="a6dec-150">**No of users** - Počet používateľov</span><span class="sxs-lookup"><span data-stu-id="a6dec-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="a6dec-151">**NO of Months** - Počet mesiacov predplatného</span><span class="sxs-lookup"><span data-stu-id="a6dec-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="a6dec-152">**Produkt SKU**</span><span class="sxs-lookup"><span data-stu-id="a6dec-152">**Product SKU**</span></span> 

<span data-ttu-id="a6dec-153">Vlastnosti **No of Users** a **No of Months** môžu byť označené ako množstevné faktory úpravou vlastnosti produktového riadka.</span><span class="sxs-lookup"><span data-stu-id="a6dec-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![OznačovanieNo of Users a No of Months ako kvalitatívne faktory](media/basic-guide-11.png)
 
