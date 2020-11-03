---
title: Domovská stránka dimenzíí ceny a ocenenia
description: Táto téma poskytuje prehľad dimenzií cien.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 515a2e2e518614884b414ca43702e8bfea2c6919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084405"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="70da1-103">Domovská stránka dimenzíí ceny a ocenenia</span><span class="sxs-lookup"><span data-stu-id="70da1-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="70da1-104">Dimenzie použité na stanovenie cien a nákladov práce v projektových organizáciách ovplyvňujú nasledujúce atribúty:</span><span class="sxs-lookup"><span data-stu-id="70da1-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="70da1-105">Ľudia, ktorí vykonávajú prácu súvisiacu s ich skúsenosťami, rolou alebo geografickou polohou</span><span class="sxs-lookup"><span data-stu-id="70da1-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="70da1-106">Práca, ktorá sa má vykonávať, súvisí s jej mierou zložitosti alebo dennou dobou</span><span class="sxs-lookup"><span data-stu-id="70da1-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="70da1-107">Vzhľadom na typický charakter týchto atribútov práce a ľudí potrebných na výkon práce sú v aplikácii Project Service Automation k dispozícii dva typy hodnôt cenových dimenzií:</span><span class="sxs-lookup"><span data-stu-id="70da1-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="70da1-108">**Množiny možností** – Atribúty, ktoré sú pevnými enumeráciami pre množinu hodnôt.</span><span class="sxs-lookup"><span data-stu-id="70da1-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="70da1-109">**Hodnoty založené na entite** - Atribúty, ktoré môžu mať rôznorodú množinu hodnôt, ktoré sú konečné, ale môžu sa časom meniť.</span><span class="sxs-lookup"><span data-stu-id="70da1-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="70da1-110">Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="70da1-110">Pricing dimensions</span></span>

<span data-ttu-id="70da1-111">PSA lode s predvolenou sadou cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="70da1-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="70da1-112">Tieto môžete zobraziť tak, že prejdete **Project Service** > **parametre**.</span><span class="sxs-lookup"><span data-stu-id="70da1-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="70da1-113">V zázname parametra, karta **cenové dimenzie založené na čiastke** , overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="70da1-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="70da1-114">To vám umožní nastaviť cenu a náklady pre každú rolu a organizačnú jednotku kombinácie.</span><span class="sxs-lookup"><span data-stu-id="70da1-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![Screenshot z parametrov Project Service so zvýrazneným "použiteľné pre predaj"](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="70da1-116">Ak ste boli používateľom polí role out-of-box a organizačnej jednotky ako cenové dimenzie pred verziou 3 PSA, nebudú žiadne pozorovateľné zmeny.</span><span class="sxs-lookup"><span data-stu-id="70da1-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="70da1-117">Môžete naďalej používať Project Service ako zvyčajne.</span><span class="sxs-lookup"><span data-stu-id="70da1-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="70da1-118">Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie.</span><span class="sxs-lookup"><span data-stu-id="70da1-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="70da1-119">Ďalšie informácie nájdete v nasledujúcich témach, avšak uvedomte si, že musíte vykonať postupy v uvedenom poradí:</span><span class="sxs-lookup"><span data-stu-id="70da1-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="70da1-120">Vytvorte vlastné polia a entity</span><span class="sxs-lookup"><span data-stu-id="70da1-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="70da1-121">Pridanie vlastných polí do cenového nastavenia a transakčných entít</span><span class="sxs-lookup"><span data-stu-id="70da1-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="70da1-122">Nastavenie vlastných polí ako cenových dimenzií </span><span class="sxs-lookup"><span data-stu-id="70da1-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="70da1-123">Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien</span><span class="sxs-lookup"><span data-stu-id="70da1-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="70da1-124">Ceny ľudských zdrojov času</span><span class="sxs-lookup"><span data-stu-id="70da1-124">Pricing human resource time</span></span>
<span data-ttu-id="70da1-125">Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie.</span><span class="sxs-lookup"><span data-stu-id="70da1-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="70da1-126">Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.</span><span class="sxs-lookup"><span data-stu-id="70da1-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="70da1-127">Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu.</span><span class="sxs-lookup"><span data-stu-id="70da1-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="70da1-128">Polia ako **transakčná kategória** ( **msdyn_transactioncategory** ) a **rezervovateľný zdroj** ( **bookableresource** ) sú príklady kandidátov dimenzie.</span><span class="sxs-lookup"><span data-stu-id="70da1-128">Fields like **Transaction Category** ( **msdyn_transactioncategory** ) and **Bookable Resource** ( **bookableresource** ) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="70da1-129">Zvážte, či by mala byť vaša cenová dimenzia tabuľkou alebo množinou možností.</span><span class="sxs-lookup"><span data-stu-id="70da1-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="70da1-130">Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12, a potrebujete ďalšie atribúty týchto hodnôt, vytvorte entitu, a nie množinu možností.</span><span class="sxs-lookup"><span data-stu-id="70da1-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="70da1-131">Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina obchodných používateľov.</span><span class="sxs-lookup"><span data-stu-id="70da1-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="70da1-132">Nasledujúci príklad zobrazuje fakturačné sadzby, ktoré sú nastavené na základe role a zdrojov organizačnej jednotky, ku ktorej zdroj patrí.</span><span class="sxs-lookup"><span data-stu-id="70da1-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="70da1-133">Ceny sú zvyčajne založené na platovom pásme zamestnanca a organizačnej jednotky, ku ktorej patria.</span><span class="sxs-lookup"><span data-stu-id="70da1-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="70da1-134">V tomto príklade budú tabuľky fakturačnej a nákladovej sadzby vyzerať takto.</span><span class="sxs-lookup"><span data-stu-id="70da1-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="70da1-135">**Vzorka fakturačných sadzieb**</span><span class="sxs-lookup"><span data-stu-id="70da1-135">**Sample bill rates**</span></span>

| <span data-ttu-id="70da1-136">Rola</span><span class="sxs-lookup"><span data-stu-id="70da1-136">Role</span></span>        | <span data-ttu-id="70da1-137">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="70da1-137">Org Unit</span></span>    |<span data-ttu-id="70da1-138">Jednotka</span><span class="sxs-lookup"><span data-stu-id="70da1-138">Unit</span></span>      |<span data-ttu-id="70da1-139">Cena</span><span class="sxs-lookup"><span data-stu-id="70da1-139">Price</span></span>      |<span data-ttu-id="70da1-140">Mena</span><span class="sxs-lookup"><span data-stu-id="70da1-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="70da1-141">Vývojár</span><span class="sxs-lookup"><span data-stu-id="70da1-141">Developer</span></span>   | <span data-ttu-id="70da1-142">Contoso US</span><span class="sxs-lookup"><span data-stu-id="70da1-142">Contoso US</span></span>  |<span data-ttu-id="70da1-143">Hour</span><span class="sxs-lookup"><span data-stu-id="70da1-143">Hour</span></span> | <span data-ttu-id="70da1-144">200</span><span class="sxs-lookup"><span data-stu-id="70da1-144">200</span></span>|<span data-ttu-id="70da1-145">USD</span><span class="sxs-lookup"><span data-stu-id="70da1-145">USD</span></span>     |
| <span data-ttu-id="70da1-146">Vývojár</span><span class="sxs-lookup"><span data-stu-id="70da1-146">Developer</span></span>   | <span data-ttu-id="70da1-147">Blaho India</span><span class="sxs-lookup"><span data-stu-id="70da1-147">Contoso India</span></span> |<span data-ttu-id="70da1-148">Hour</span><span class="sxs-lookup"><span data-stu-id="70da1-148">Hour</span></span>|   <span data-ttu-id="70da1-149">112</span><span class="sxs-lookup"><span data-stu-id="70da1-149">112</span></span>|<span data-ttu-id="70da1-150">USD</span><span class="sxs-lookup"><span data-stu-id="70da1-150">USD</span></span>     |


<span data-ttu-id="70da1-151">**Vzorka nákladových sadzieb**</span><span class="sxs-lookup"><span data-stu-id="70da1-151">**Sample cost rates**</span></span>

| <span data-ttu-id="70da1-152">Platové pásmo</span><span class="sxs-lookup"><span data-stu-id="70da1-152">Salary Band</span></span>     | <span data-ttu-id="70da1-153">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="70da1-153">Org Unit</span></span>    |<span data-ttu-id="70da1-154">Jednotka</span><span class="sxs-lookup"><span data-stu-id="70da1-154">Unit</span></span>      |<span data-ttu-id="70da1-155">Cena</span><span class="sxs-lookup"><span data-stu-id="70da1-155">Price</span></span>      |<span data-ttu-id="70da1-156">Mena</span><span class="sxs-lookup"><span data-stu-id="70da1-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="70da1-157">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="70da1-157">My company_Band1</span></span> | <span data-ttu-id="70da1-158">Contoso US</span><span class="sxs-lookup"><span data-stu-id="70da1-158">Contoso US</span></span>  |<span data-ttu-id="70da1-159">Hour</span><span class="sxs-lookup"><span data-stu-id="70da1-159">Hour</span></span> | <span data-ttu-id="70da1-160">145</span><span class="sxs-lookup"><span data-stu-id="70da1-160">145</span></span>|<span data-ttu-id="70da1-161">USD</span><span class="sxs-lookup"><span data-stu-id="70da1-161">USD</span></span>     |
| <span data-ttu-id="70da1-162">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="70da1-162">My company_Band2</span></span> | <span data-ttu-id="70da1-163">Blaho India</span><span class="sxs-lookup"><span data-stu-id="70da1-163">Contoso India</span></span> |<span data-ttu-id="70da1-164">Hour</span><span class="sxs-lookup"><span data-stu-id="70da1-164">Hour</span></span>|   <span data-ttu-id="70da1-165">67</span><span class="sxs-lookup"><span data-stu-id="70da1-165">67</span></span>|<span data-ttu-id="70da1-166">USD</span><span class="sxs-lookup"><span data-stu-id="70da1-166">USD</span></span>     |
