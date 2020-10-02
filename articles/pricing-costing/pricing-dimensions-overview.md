---
title: Prehľad cenových dimenzií
description: Táto téma poskytuje informácie o cenových dimenziách v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: fe2ab3a1b12c00e346e27709d66b5a0cb81a3b56
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898235"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="cfe32-103">Prehľad cenových dimenzií</span><span class="sxs-lookup"><span data-stu-id="cfe32-103">Pricing dimensions overview</span></span>

<span data-ttu-id="cfe32-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="cfe32-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cfe32-105">Dimenzie, ktoré sa používajú v ľudských zdrojoch na stanovenie cien a nákladov, spadajú do dvoch kategórií:</span><span class="sxs-lookup"><span data-stu-id="cfe32-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="cfe32-106">Ľudia</span><span class="sxs-lookup"><span data-stu-id="cfe32-106">People</span></span>
- <span data-ttu-id="cfe32-107">Plánovaná práca</span><span class="sxs-lookup"><span data-stu-id="cfe32-107">Planned work</span></span>

<span data-ttu-id="cfe32-108">Z tohto dôvodu existujú dva typy hodnôt cenovej dimenzie:</span><span class="sxs-lookup"><span data-stu-id="cfe32-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="cfe32-109">**Množiny možností**: Dimenzie, ktoré sú pevnými enumeráciami pre množinu hodnôt.</span><span class="sxs-lookup"><span data-stu-id="cfe32-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="cfe32-110">**Hodnoty založené na entite**: Dimenzie, ktoré môžu byť rôznorodými množinami hodnôt.</span><span class="sxs-lookup"><span data-stu-id="cfe32-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="cfe32-111">Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="cfe32-111">Pricing dimensions</span></span>

<span data-ttu-id="cfe32-112">Dynamics 365 Project Operations sa dodáva s predvolenou množinou cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="cfe32-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="cfe32-113">Tieto cenové dimenzie môžete zobraziť tak, že prejdete do **Project Operations** > **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="cfe32-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="cfe32-114">V zázname parametra, karta **cenové dimenzie založené na čiastke**, overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="cfe32-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="cfe32-115">Po povolení týchto polí môžete nastavovať cenu a náklady pre kombináciu každej roly a organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="cfe32-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="cfe32-116">Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie.</span><span class="sxs-lookup"><span data-stu-id="cfe32-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="cfe32-117">Ceny ľudských zdrojov času</span><span class="sxs-lookup"><span data-stu-id="cfe32-117">Pricing human resource time</span></span>
<span data-ttu-id="cfe32-118">Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie.</span><span class="sxs-lookup"><span data-stu-id="cfe32-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="cfe32-119">Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.</span><span class="sxs-lookup"><span data-stu-id="cfe32-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="cfe32-120">Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu.</span><span class="sxs-lookup"><span data-stu-id="cfe32-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="cfe32-121">Polia ako **transakčná kategória** (**msdyn_transactioncategory**) a **rezervovateľný zdroj** (**bookableresource**) sú príklady kandidátov dimenzie.</span><span class="sxs-lookup"><span data-stu-id="cfe32-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="cfe32-122">Zvážte, či by mala byť vaša cenová dimenzia tabuľkou alebo množinou možností.</span><span class="sxs-lookup"><span data-stu-id="cfe32-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="cfe32-123">Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12 a potrebujete ďalšie atribúty týchto hodnôt, môžete vytvoriť entitu, a nie množinu možností.</span><span class="sxs-lookup"><span data-stu-id="cfe32-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="cfe32-124">Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina používateľov.</span><span class="sxs-lookup"><span data-stu-id="cfe32-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="cfe32-125">Nasledujúci príklad zobrazuje fakturačné sadzby, ktoré sú nastavené na základe role a zdrojov organizačnej jednotky, ku ktorej zdroj patrí.</span><span class="sxs-lookup"><span data-stu-id="cfe32-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="cfe32-126">Ceny sú zvyčajne založené na platovom pásme zamestnanca a organizačnej jednotky, ku ktorej patria.</span><span class="sxs-lookup"><span data-stu-id="cfe32-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="cfe32-127">V tomto príklade budú tabuľky fakturačnej a nákladovej sadzby vyzerať takto.</span><span class="sxs-lookup"><span data-stu-id="cfe32-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="cfe32-128">**Vzorka fakturačných sadzieb**</span><span class="sxs-lookup"><span data-stu-id="cfe32-128">**Sample bill rates**</span></span>

| <span data-ttu-id="cfe32-129">Rola</span><span class="sxs-lookup"><span data-stu-id="cfe32-129">Role</span></span>        | <span data-ttu-id="cfe32-130">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="cfe32-130">Org Unit</span></span>    |<span data-ttu-id="cfe32-131">Jednotka</span><span class="sxs-lookup"><span data-stu-id="cfe32-131">Unit</span></span>      |<span data-ttu-id="cfe32-132">Cena</span><span class="sxs-lookup"><span data-stu-id="cfe32-132">Price</span></span>      |<span data-ttu-id="cfe32-133">Mena</span><span class="sxs-lookup"><span data-stu-id="cfe32-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="cfe32-134">Vývojár</span><span class="sxs-lookup"><span data-stu-id="cfe32-134">Developer</span></span>   | <span data-ttu-id="cfe32-135">Contoso US</span><span class="sxs-lookup"><span data-stu-id="cfe32-135">Contoso US</span></span>  |<span data-ttu-id="cfe32-136">Hour</span><span class="sxs-lookup"><span data-stu-id="cfe32-136">Hour</span></span> | <span data-ttu-id="cfe32-137">200</span><span class="sxs-lookup"><span data-stu-id="cfe32-137">200</span></span>|<span data-ttu-id="cfe32-138">USD</span><span class="sxs-lookup"><span data-stu-id="cfe32-138">USD</span></span>     |
| <span data-ttu-id="cfe32-139">Vývojár</span><span class="sxs-lookup"><span data-stu-id="cfe32-139">Developer</span></span>   | <span data-ttu-id="cfe32-140">Blaho India</span><span class="sxs-lookup"><span data-stu-id="cfe32-140">Contoso India</span></span> |<span data-ttu-id="cfe32-141">Hour</span><span class="sxs-lookup"><span data-stu-id="cfe32-141">Hour</span></span>|   <span data-ttu-id="cfe32-142">112</span><span class="sxs-lookup"><span data-stu-id="cfe32-142">112</span></span>|<span data-ttu-id="cfe32-143">USD</span><span class="sxs-lookup"><span data-stu-id="cfe32-143">USD</span></span>     |


<span data-ttu-id="cfe32-144">**Vzorka nákladových sadzieb**</span><span class="sxs-lookup"><span data-stu-id="cfe32-144">**Sample cost rates**</span></span>

| <span data-ttu-id="cfe32-145">Platové pásmo</span><span class="sxs-lookup"><span data-stu-id="cfe32-145">Salary Band</span></span>     | <span data-ttu-id="cfe32-146">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="cfe32-146">Org Unit</span></span>    |<span data-ttu-id="cfe32-147">Jednotka</span><span class="sxs-lookup"><span data-stu-id="cfe32-147">Unit</span></span>      |<span data-ttu-id="cfe32-148">Cena</span><span class="sxs-lookup"><span data-stu-id="cfe32-148">Price</span></span>      |<span data-ttu-id="cfe32-149">Mena</span><span class="sxs-lookup"><span data-stu-id="cfe32-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="cfe32-150">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="cfe32-150">My company_Band1</span></span> | <span data-ttu-id="cfe32-151">Contoso US</span><span class="sxs-lookup"><span data-stu-id="cfe32-151">Contoso US</span></span>  |<span data-ttu-id="cfe32-152">Hour</span><span class="sxs-lookup"><span data-stu-id="cfe32-152">Hour</span></span> | <span data-ttu-id="cfe32-153">145</span><span class="sxs-lookup"><span data-stu-id="cfe32-153">145</span></span>|<span data-ttu-id="cfe32-154">USD</span><span class="sxs-lookup"><span data-stu-id="cfe32-154">USD</span></span>     |
| <span data-ttu-id="cfe32-155">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="cfe32-155">My company_Band2</span></span> | <span data-ttu-id="cfe32-156">Blaho India</span><span class="sxs-lookup"><span data-stu-id="cfe32-156">Contoso India</span></span> |<span data-ttu-id="cfe32-157">Hour</span><span class="sxs-lookup"><span data-stu-id="cfe32-157">Hour</span></span>|   <span data-ttu-id="cfe32-158">67</span><span class="sxs-lookup"><span data-stu-id="cfe32-158">67</span></span>|<span data-ttu-id="cfe32-159">USD</span><span class="sxs-lookup"><span data-stu-id="cfe32-159">USD</span></span>     |
