---
title: Prehľad cenových dimenzií
description: Táto téma poskytuje informácie o cenových dimenziách v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 6b1ebdc97ec4704ba256acb521c0f2e7c474940b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084471"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="28a52-103">Prehľad cenových dimenzií</span><span class="sxs-lookup"><span data-stu-id="28a52-103">Pricing dimensions overview</span></span>

<span data-ttu-id="28a52-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="28a52-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="28a52-105">Dimenzie, ktoré sa používajú v ľudských zdrojoch na stanovenie cien a nákladov, spadajú do dvoch kategórií:</span><span class="sxs-lookup"><span data-stu-id="28a52-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="28a52-106">Ľudia</span><span class="sxs-lookup"><span data-stu-id="28a52-106">People</span></span>
- <span data-ttu-id="28a52-107">Plánovaná práca</span><span class="sxs-lookup"><span data-stu-id="28a52-107">Planned work</span></span>

<span data-ttu-id="28a52-108">Z tohto dôvodu existujú dva typy hodnôt cenovej dimenzie:</span><span class="sxs-lookup"><span data-stu-id="28a52-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="28a52-109">**Množiny možností** : Dimenzie, ktoré sú pevnými enumeráciami pre množinu hodnôt.</span><span class="sxs-lookup"><span data-stu-id="28a52-109">**Option sets** : Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="28a52-110">**Hodnoty založené na entite** : Dimenzie, ktoré môžu byť rôznorodými množinami hodnôt.</span><span class="sxs-lookup"><span data-stu-id="28a52-110">**Entity-based values** : Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="28a52-111">Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="28a52-111">Pricing dimensions</span></span>

<span data-ttu-id="28a52-112">Dynamics 365 Project Operations sa dodáva s predvolenou množinou cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="28a52-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="28a52-113">Tieto cenové dimenzie môžete zobraziť tak, že prejdete do **Project Operations** > **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="28a52-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="28a52-114">V zázname parametra, karta **cenové dimenzie založené na čiastke** , overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="28a52-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="28a52-115">Po povolení týchto polí môžete nastavovať cenu a náklady pre kombináciu každej roly a organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="28a52-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="28a52-116">Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie.</span><span class="sxs-lookup"><span data-stu-id="28a52-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="28a52-117">Ceny ľudských zdrojov času</span><span class="sxs-lookup"><span data-stu-id="28a52-117">Pricing human resource time</span></span>
<span data-ttu-id="28a52-118">Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie.</span><span class="sxs-lookup"><span data-stu-id="28a52-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="28a52-119">Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.</span><span class="sxs-lookup"><span data-stu-id="28a52-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="28a52-120">Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu.</span><span class="sxs-lookup"><span data-stu-id="28a52-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="28a52-121">Polia ako **transakčná kategória** ( **msdyn_transactioncategory** ) a **rezervovateľný zdroj** ( **bookableresource** ) sú príklady kandidátov dimenzie.</span><span class="sxs-lookup"><span data-stu-id="28a52-121">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="28a52-122">Zvážte, či by mala byť vaša cenová dimenzia tabuľkou alebo množinou možností.</span><span class="sxs-lookup"><span data-stu-id="28a52-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="28a52-123">Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12 a potrebujete ďalšie atribúty týchto hodnôt, môžete vytvoriť entitu, a nie množinu možností.</span><span class="sxs-lookup"><span data-stu-id="28a52-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="28a52-124">Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina používateľov.</span><span class="sxs-lookup"><span data-stu-id="28a52-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="28a52-125">Nasledujúci príklad zobrazuje fakturačné sadzby, ktoré sú nastavené na základe role a zdrojov organizačnej jednotky, ku ktorej zdroj patrí.</span><span class="sxs-lookup"><span data-stu-id="28a52-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="28a52-126">Ceny sú zvyčajne založené na platovom pásme zamestnanca a organizačnej jednotky, ku ktorej patria.</span><span class="sxs-lookup"><span data-stu-id="28a52-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="28a52-127">V tomto príklade budú tabuľky fakturačnej a nákladovej sadzby vyzerať takto.</span><span class="sxs-lookup"><span data-stu-id="28a52-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="28a52-128">**Vzorka fakturačných sadzieb**</span><span class="sxs-lookup"><span data-stu-id="28a52-128">**Sample bill rates**</span></span>

| <span data-ttu-id="28a52-129">Rola</span><span class="sxs-lookup"><span data-stu-id="28a52-129">Role</span></span>        | <span data-ttu-id="28a52-130">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="28a52-130">Org Unit</span></span>    |<span data-ttu-id="28a52-131">Jednotka</span><span class="sxs-lookup"><span data-stu-id="28a52-131">Unit</span></span>      |<span data-ttu-id="28a52-132">Cena</span><span class="sxs-lookup"><span data-stu-id="28a52-132">Price</span></span>      |<span data-ttu-id="28a52-133">Mena</span><span class="sxs-lookup"><span data-stu-id="28a52-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="28a52-134">Vývojár</span><span class="sxs-lookup"><span data-stu-id="28a52-134">Developer</span></span>   | <span data-ttu-id="28a52-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="28a52-135">Contoso US</span></span>  |<span data-ttu-id="28a52-136">Hour</span><span class="sxs-lookup"><span data-stu-id="28a52-136">Hour</span></span> | <span data-ttu-id="28a52-137">200</span><span class="sxs-lookup"><span data-stu-id="28a52-137">200</span></span>|<span data-ttu-id="28a52-138">USD</span><span class="sxs-lookup"><span data-stu-id="28a52-138">USD</span></span>     |
| <span data-ttu-id="28a52-139">Vývojár</span><span class="sxs-lookup"><span data-stu-id="28a52-139">Developer</span></span>   | <span data-ttu-id="28a52-140">Blaho India</span><span class="sxs-lookup"><span data-stu-id="28a52-140">Contoso India</span></span> |<span data-ttu-id="28a52-141">Hour</span><span class="sxs-lookup"><span data-stu-id="28a52-141">Hour</span></span>|   <span data-ttu-id="28a52-142">112</span><span class="sxs-lookup"><span data-stu-id="28a52-142">112</span></span>|<span data-ttu-id="28a52-143">USD</span><span class="sxs-lookup"><span data-stu-id="28a52-143">USD</span></span>     |


<span data-ttu-id="28a52-144">**Vzorka nákladových sadzieb**</span><span class="sxs-lookup"><span data-stu-id="28a52-144">**Sample cost rates**</span></span>

| <span data-ttu-id="28a52-145">Platové pásmo</span><span class="sxs-lookup"><span data-stu-id="28a52-145">Salary Band</span></span>     | <span data-ttu-id="28a52-146">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="28a52-146">Org Unit</span></span>    |<span data-ttu-id="28a52-147">Jednotka</span><span class="sxs-lookup"><span data-stu-id="28a52-147">Unit</span></span>      |<span data-ttu-id="28a52-148">Cena</span><span class="sxs-lookup"><span data-stu-id="28a52-148">Price</span></span>      |<span data-ttu-id="28a52-149">Mena</span><span class="sxs-lookup"><span data-stu-id="28a52-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="28a52-150">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="28a52-150">My company_Band1</span></span> | <span data-ttu-id="28a52-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="28a52-151">Contoso US</span></span>  |<span data-ttu-id="28a52-152">Hour</span><span class="sxs-lookup"><span data-stu-id="28a52-152">Hour</span></span> | <span data-ttu-id="28a52-153">145</span><span class="sxs-lookup"><span data-stu-id="28a52-153">145</span></span>|<span data-ttu-id="28a52-154">USD</span><span class="sxs-lookup"><span data-stu-id="28a52-154">USD</span></span>     |
| <span data-ttu-id="28a52-155">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="28a52-155">My company_Band2</span></span> | <span data-ttu-id="28a52-156">Blaho India</span><span class="sxs-lookup"><span data-stu-id="28a52-156">Contoso India</span></span> |<span data-ttu-id="28a52-157">Hour</span><span class="sxs-lookup"><span data-stu-id="28a52-157">Hour</span></span>|   <span data-ttu-id="28a52-158">67</span><span class="sxs-lookup"><span data-stu-id="28a52-158">67</span></span>|<span data-ttu-id="28a52-159">USD</span><span class="sxs-lookup"><span data-stu-id="28a52-159">USD</span></span>     |
