---
title: Domovská stránka dimenzíí ceny a ocenenia
description: Táto téma poskytuje prehľad dimenzií cien.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755567"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="1e285-103">Domovská stránka dimenzíí ceny a ocenenia</span><span class="sxs-lookup"><span data-stu-id="1e285-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="1e285-104">Dimenzie, ktoré sa používajú v ľudských zdrojoch na stanovenie cien a nákladov, spadajú do dvoch kategórií:</span><span class="sxs-lookup"><span data-stu-id="1e285-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="1e285-105">Ľudia</span><span class="sxs-lookup"><span data-stu-id="1e285-105">People</span></span>
- <span data-ttu-id="1e285-106">Plánovaná práca</span><span class="sxs-lookup"><span data-stu-id="1e285-106">Planned work</span></span>

<span data-ttu-id="1e285-107">Z tohto dôvodu existujú dva typy hodnôt dimenzie ceny k dispozícii v Project Service Automation (PSA):</span><span class="sxs-lookup"><span data-stu-id="1e285-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="1e285-108">**Množina možností** – dimenzie, ktoré sú pevnými enumeráciami pre množinu hodnôt.</span><span class="sxs-lookup"><span data-stu-id="1e285-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="1e285-109">**Hodnoty založené na entite** - Dimenzie, ktoré môžu byť rôznorodá množina hodnôt.</span><span class="sxs-lookup"><span data-stu-id="1e285-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="1e285-110">Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="1e285-110">Pricing dimensions</span></span>

<span data-ttu-id="1e285-111">PSA lode s predvolenou sadou cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="1e285-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="1e285-112">Tieto môžete zobraziť tak, že prejdete **Project Service** > **parametre**.</span><span class="sxs-lookup"><span data-stu-id="1e285-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="1e285-113">V zázname parametra, karta **cenové dimenzie založené na čiastke**, overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="1e285-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="1e285-114">To vám umožní nastaviť cenu a náklady pre každú rolu a organizačnú jednotku kombinácie.</span><span class="sxs-lookup"><span data-stu-id="1e285-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Screenshot z parametrov Project Service so zvýrazneným "použiteľné pre predaj"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="1e285-116">Ak ste boli používateľom polí role out-of-box a organizačnej jednotky ako cenové dimenzie pred verziou 3 PSA, nebudú žiadne pozorovateľné zmeny.</span><span class="sxs-lookup"><span data-stu-id="1e285-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="1e285-117">Môžete naďalej používať Project Service ako zvyčajne.</span><span class="sxs-lookup"><span data-stu-id="1e285-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="1e285-118">Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie.</span><span class="sxs-lookup"><span data-stu-id="1e285-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="1e285-119">Ďalšie informácie nájdete v nasledujúcich témach, avšak uvedomte si, že musíte vykonať postupy v uvedenom poradí:</span><span class="sxs-lookup"><span data-stu-id="1e285-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="1e285-120">Vytvorte vlastné polia a entity</span><span class="sxs-lookup"><span data-stu-id="1e285-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="1e285-121">Pridanie vlastných polí do cenového nastavenia a transakčných entít</span><span class="sxs-lookup"><span data-stu-id="1e285-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="1e285-122">Nastavenie vlastných polí ako dimenzií cien</span><span class="sxs-lookup"><span data-stu-id="1e285-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="1e285-123">Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien</span><span class="sxs-lookup"><span data-stu-id="1e285-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="1e285-124">Ceny ľudských zdrojov času</span><span class="sxs-lookup"><span data-stu-id="1e285-124">Pricing human resource time</span></span>
<span data-ttu-id="1e285-125">Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie.</span><span class="sxs-lookup"><span data-stu-id="1e285-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="1e285-126">Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.</span><span class="sxs-lookup"><span data-stu-id="1e285-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="1e285-127">Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu.</span><span class="sxs-lookup"><span data-stu-id="1e285-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="1e285-128">Polia ako **transakčná kategória** (**msdyn_transactioncategory**) a **rezervovateľný zdroj** (**bookableresource**) sú príklady kandidátov dimenzie.</span><span class="sxs-lookup"><span data-stu-id="1e285-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="1e285-129">Mali by ste tiež zvážiť, či by mal byť váš cenový rozmer tabuľka alebo množina možností.</span><span class="sxs-lookup"><span data-stu-id="1e285-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="1e285-130">Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12 a potrebujete ďalšie atribúty týchto hodnôt, môžete vytvoriť entitu, a nie množinu možností.</span><span class="sxs-lookup"><span data-stu-id="1e285-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="1e285-131">Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina používateľov.</span><span class="sxs-lookup"><span data-stu-id="1e285-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="1e285-132">Nasledujúci príklad zobrazuje fakturačné sadzby, ktoré sú nastavené na základe role a zdrojov organizačnej jednotky, ku ktorej zdroj patrí.</span><span class="sxs-lookup"><span data-stu-id="1e285-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="1e285-133">Ceny sú zvyčajne založené na platovom pásme zamestnanca a organizačnej jednotky, ku ktorej patria.</span><span class="sxs-lookup"><span data-stu-id="1e285-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="1e285-134">V tomto príklade budú tabuľky fakturačnej a nákladovej sadzby vyzerať takto.</span><span class="sxs-lookup"><span data-stu-id="1e285-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="1e285-135">**Vzorka fakturačných sadzieb**</span><span class="sxs-lookup"><span data-stu-id="1e285-135">**Sample bill rates**</span></span>

| <span data-ttu-id="1e285-136">Rola</span><span class="sxs-lookup"><span data-stu-id="1e285-136">Role</span></span>        | <span data-ttu-id="1e285-137">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="1e285-137">Org Unit</span></span>    |<span data-ttu-id="1e285-138">Jednotka</span><span class="sxs-lookup"><span data-stu-id="1e285-138">Unit</span></span>      |<span data-ttu-id="1e285-139">Cena</span><span class="sxs-lookup"><span data-stu-id="1e285-139">Price</span></span>      |<span data-ttu-id="1e285-140">Mena</span><span class="sxs-lookup"><span data-stu-id="1e285-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1e285-141">Vývojár</span><span class="sxs-lookup"><span data-stu-id="1e285-141">Developer</span></span>   | <span data-ttu-id="1e285-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1e285-142">Contoso US</span></span>  |<span data-ttu-id="1e285-143">Hour</span><span class="sxs-lookup"><span data-stu-id="1e285-143">Hour</span></span> | <span data-ttu-id="1e285-144">200</span><span class="sxs-lookup"><span data-stu-id="1e285-144">200</span></span>|<span data-ttu-id="1e285-145">USD</span><span class="sxs-lookup"><span data-stu-id="1e285-145">USD</span></span>     |
| <span data-ttu-id="1e285-146">Vývojár</span><span class="sxs-lookup"><span data-stu-id="1e285-146">Developer</span></span>   | <span data-ttu-id="1e285-147">Blaho India</span><span class="sxs-lookup"><span data-stu-id="1e285-147">Contoso India</span></span> |<span data-ttu-id="1e285-148">Hour</span><span class="sxs-lookup"><span data-stu-id="1e285-148">Hour</span></span>|   <span data-ttu-id="1e285-149">112</span><span class="sxs-lookup"><span data-stu-id="1e285-149">112</span></span>|<span data-ttu-id="1e285-150">USD</span><span class="sxs-lookup"><span data-stu-id="1e285-150">USD</span></span>     |


<span data-ttu-id="1e285-151">**Vzorka nákladových sadzieb**</span><span class="sxs-lookup"><span data-stu-id="1e285-151">**Sample cost rates**</span></span>

| <span data-ttu-id="1e285-152">Platové pásmo</span><span class="sxs-lookup"><span data-stu-id="1e285-152">Salary Band</span></span>     | <span data-ttu-id="1e285-153">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="1e285-153">Org Unit</span></span>    |<span data-ttu-id="1e285-154">Jednotka</span><span class="sxs-lookup"><span data-stu-id="1e285-154">Unit</span></span>      |<span data-ttu-id="1e285-155">Cena</span><span class="sxs-lookup"><span data-stu-id="1e285-155">Price</span></span>      |<span data-ttu-id="1e285-156">Mena</span><span class="sxs-lookup"><span data-stu-id="1e285-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="1e285-157">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="1e285-157">My company_Band1</span></span> | <span data-ttu-id="1e285-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="1e285-158">Contoso US</span></span>  |<span data-ttu-id="1e285-159">Hour</span><span class="sxs-lookup"><span data-stu-id="1e285-159">Hour</span></span> | <span data-ttu-id="1e285-160">145</span><span class="sxs-lookup"><span data-stu-id="1e285-160">145</span></span>|<span data-ttu-id="1e285-161">USD</span><span class="sxs-lookup"><span data-stu-id="1e285-161">USD</span></span>     |
| <span data-ttu-id="1e285-162">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="1e285-162">My company_Band2</span></span> | <span data-ttu-id="1e285-163">Blaho India</span><span class="sxs-lookup"><span data-stu-id="1e285-163">Contoso India</span></span> |<span data-ttu-id="1e285-164">Hour</span><span class="sxs-lookup"><span data-stu-id="1e285-164">Hour</span></span>|   <span data-ttu-id="1e285-165">67</span><span class="sxs-lookup"><span data-stu-id="1e285-165">67</span></span>|<span data-ttu-id="1e285-166">USD</span><span class="sxs-lookup"><span data-stu-id="1e285-166">USD</span></span>     |
