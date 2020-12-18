---
title: Prehľad cenových dimenzií
description: Táto téma poskytuje informácie o cenových dimenziách v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 11/30/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 33f55976eafedd046fba952ab6381c297ab4e271
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650229"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="5dc97-103">Prehľad cenových dimenzií</span><span class="sxs-lookup"><span data-stu-id="5dc97-103">Pricing dimensions overview</span></span>

<span data-ttu-id="5dc97-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="5dc97-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5dc97-105">Dimenzie, ktoré sa používajú v ľudských zdrojoch na stanovenie cien a nákladov, spadajú do dvoch kategórií:</span><span class="sxs-lookup"><span data-stu-id="5dc97-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="5dc97-106">Ľudia</span><span class="sxs-lookup"><span data-stu-id="5dc97-106">People</span></span>
- <span data-ttu-id="5dc97-107">Plánovaná práca</span><span class="sxs-lookup"><span data-stu-id="5dc97-107">Planned work</span></span>

<span data-ttu-id="5dc97-108">Z tohto dôvodu existujú dva typy hodnôt cenovej dimenzie:</span><span class="sxs-lookup"><span data-stu-id="5dc97-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="5dc97-109">**Množiny možností**: Dimenzie, ktoré sú pevnými enumeráciami pre množinu hodnôt.</span><span class="sxs-lookup"><span data-stu-id="5dc97-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="5dc97-110">**Hodnoty založené na entite**: Dimenzie, ktoré môžu byť rôznorodými množinami hodnôt.</span><span class="sxs-lookup"><span data-stu-id="5dc97-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="5dc97-111">Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="5dc97-111">Pricing dimensions</span></span>

<span data-ttu-id="5dc97-112">Dynamics 365 Project Operations sa dodáva s predvolenou množinou cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="5dc97-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="5dc97-113">Tieto cenové dimenzie môžete zobraziť tak, že prejdete do **Project Operations** > **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="5dc97-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="5dc97-114">V zázname parametra, karta **cenové dimenzie založené na čiastke**, overuje, že role, **msdyn_resourcecategory** a zdrojová organizačná jednotka, **msdyn_organizationalunit** majú polia **Vzťahujúce sa na predaj** a **vzťahujúce sa na náklad** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="5dc97-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="5dc97-115">Po povolení týchto polí môžete nastavovať cenu a náklady pre kombináciu každej roly a organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="5dc97-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

![Screenshot z parametrov Project Service so zvýrazneným "použiteľné pre predaj"](media/PS-OOB-parameters.png)

<span data-ttu-id="5dc97-117">Ak potrebujete ceny alebo náklady na svoje zdroje pomocou ďalších atribútov, môžete vytvoriť prispôsobené polia, entity a dimenzie.</span><span class="sxs-lookup"><span data-stu-id="5dc97-117">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="5dc97-118">Ďalšie informácie nájdete v nasledujúcej téme.</span><span class="sxs-lookup"><span data-stu-id="5dc97-118">For more information, see the following topics.</span></span> 
  
  > [!NOTE]
  > <span data-ttu-id="5dc97-119">Postupy musia byť ukončené v poradí, v akom sú uvedené.</span><span class="sxs-lookup"><span data-stu-id="5dc97-119">The procedures must be completed in the order they are listed.</span></span>

1. [<span data-ttu-id="5dc97-120">Vytvorenie riešenia pre vlastné cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="5dc97-120">Create a solution for custom pricing dimensions</span></span>](../sales/create-solution-custompd.md)
2. [<span data-ttu-id="5dc97-121">Vytvorenie vlastných polí a entít</span><span class="sxs-lookup"><span data-stu-id="5dc97-121">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md)
3. [<span data-ttu-id="5dc97-122">Pridanie vlastných polí do entít nastavenia cien a transakcií </span><span class="sxs-lookup"><span data-stu-id="5dc97-122">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
4. [<span data-ttu-id="5dc97-123">Nastavenie vlastných polí ako cenových dimenzií </span><span class="sxs-lookup"><span data-stu-id="5dc97-123">Set up custom fields as pricing dimensions</span></span>](set-up-custom-fields-pricing-dimensions.md)
5. [<span data-ttu-id="5dc97-124">Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien</span><span class="sxs-lookup"><span data-stu-id="5dc97-124">Update plug-in attributes to include new pricing dimensions</span></span>](update-plugin-attributes-pd.md)


## <a name="pricing-human-resource-time"></a><span data-ttu-id="5dc97-125">Ceny ľudských zdrojov času</span><span class="sxs-lookup"><span data-stu-id="5dc97-125">Pricing human resource time</span></span>
<span data-ttu-id="5dc97-126">Ako organizácia ceny ľudských zdrojov času je často dôležitým strategickým vzhľadom, že priamo ovplyvňuje ziskovosť organizácie.</span><span class="sxs-lookup"><span data-stu-id="5dc97-126">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="5dc97-127">Práca s finančnými tímami a cvičením hláv, keď vaša organizácia je pripravená zistiť, ako chce nastaviť fakturáciu a ceny za ľudské zdroje času.</span><span class="sxs-lookup"><span data-stu-id="5dc97-127">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="5dc97-128">Ďalšie informácie o cenách zahŕňajú, či chcete opätovne použiť polia alebo entity, ktoré momentálne nie sú dimenziami cien, ale vzťahujú sa na dimenziu cien pre vašu organizáciu.</span><span class="sxs-lookup"><span data-stu-id="5dc97-128">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="5dc97-129">Polia ako **transakčná kategória** (**msdyn_transactioncategory**) a **rezervovateľný zdroj** (**bookableresource**) sú príklady kandidátov dimenzie.</span><span class="sxs-lookup"><span data-stu-id="5dc97-129">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="5dc97-130">Zvážte, či by mala byť vaša cenová dimenzia tabuľkou alebo množinou možností.</span><span class="sxs-lookup"><span data-stu-id="5dc97-130">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="5dc97-131">Ak predpokladáte zmeny hodnôt dimenzie, ktoré budú presahovať 10 alebo 12 a potrebujete ďalšie atribúty týchto hodnôt, môžete vytvoriť entitu, a nie množinu možností.</span><span class="sxs-lookup"><span data-stu-id="5dc97-131">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="5dc97-132">Udržiavanie množiny možností, ako napríklad pridávanie alebo odstraňovanie hodnôt, vyžaduje správcu alebo vývojára, zatiaľ čo pridávanie nových riadkov do tabuľky môže vykonať väčšina používateľov.</span><span class="sxs-lookup"><span data-stu-id="5dc97-132">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="5dc97-133">Nasledujúci príklad zobrazuje fakturačné sadzby, ktoré sú nastavené na základe role a zdrojov organizačnej jednotky, ku ktorej zdroj patrí.</span><span class="sxs-lookup"><span data-stu-id="5dc97-133">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="5dc97-134">Ceny sú zvyčajne založené na platovom pásme zamestnanca a organizačnej jednotky, ku ktorej patria.</span><span class="sxs-lookup"><span data-stu-id="5dc97-134">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="5dc97-135">V tomto príklade budú tabuľky fakturačnej a nákladovej sadzby vyzerať takto.</span><span class="sxs-lookup"><span data-stu-id="5dc97-135">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="5dc97-136">**Vzorka fakturačných sadzieb**</span><span class="sxs-lookup"><span data-stu-id="5dc97-136">**Sample bill rates**</span></span>

| <span data-ttu-id="5dc97-137">Rola</span><span class="sxs-lookup"><span data-stu-id="5dc97-137">Role</span></span>        | <span data-ttu-id="5dc97-138">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="5dc97-138">Org Unit</span></span>    |<span data-ttu-id="5dc97-139">Jednotka</span><span class="sxs-lookup"><span data-stu-id="5dc97-139">Unit</span></span>      |<span data-ttu-id="5dc97-140">Cena</span><span class="sxs-lookup"><span data-stu-id="5dc97-140">Price</span></span>      |<span data-ttu-id="5dc97-141">Mena</span><span class="sxs-lookup"><span data-stu-id="5dc97-141">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5dc97-142">Vývojár</span><span class="sxs-lookup"><span data-stu-id="5dc97-142">Developer</span></span>   | <span data-ttu-id="5dc97-143">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5dc97-143">Contoso US</span></span>  |<span data-ttu-id="5dc97-144">Hour</span><span class="sxs-lookup"><span data-stu-id="5dc97-144">Hour</span></span> | <span data-ttu-id="5dc97-145">200</span><span class="sxs-lookup"><span data-stu-id="5dc97-145">200</span></span>|<span data-ttu-id="5dc97-146">USD</span><span class="sxs-lookup"><span data-stu-id="5dc97-146">USD</span></span>     |
| <span data-ttu-id="5dc97-147">Vývojár</span><span class="sxs-lookup"><span data-stu-id="5dc97-147">Developer</span></span>   | <span data-ttu-id="5dc97-148">Blaho India</span><span class="sxs-lookup"><span data-stu-id="5dc97-148">Contoso India</span></span> |<span data-ttu-id="5dc97-149">Hour</span><span class="sxs-lookup"><span data-stu-id="5dc97-149">Hour</span></span>|   <span data-ttu-id="5dc97-150">112</span><span class="sxs-lookup"><span data-stu-id="5dc97-150">112</span></span>|<span data-ttu-id="5dc97-151">USD</span><span class="sxs-lookup"><span data-stu-id="5dc97-151">USD</span></span>     |


<span data-ttu-id="5dc97-152">**Vzorka nákladových sadzieb**</span><span class="sxs-lookup"><span data-stu-id="5dc97-152">**Sample cost rates**</span></span>

| <span data-ttu-id="5dc97-153">Platové pásmo</span><span class="sxs-lookup"><span data-stu-id="5dc97-153">Salary Band</span></span>     | <span data-ttu-id="5dc97-154">Org jednotka</span><span class="sxs-lookup"><span data-stu-id="5dc97-154">Org Unit</span></span>    |<span data-ttu-id="5dc97-155">Jednotka</span><span class="sxs-lookup"><span data-stu-id="5dc97-155">Unit</span></span>      |<span data-ttu-id="5dc97-156">Cena</span><span class="sxs-lookup"><span data-stu-id="5dc97-156">Price</span></span>      |<span data-ttu-id="5dc97-157">Mena</span><span class="sxs-lookup"><span data-stu-id="5dc97-157">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="5dc97-158">Moje company_Band1</span><span class="sxs-lookup"><span data-stu-id="5dc97-158">My company_Band1</span></span> | <span data-ttu-id="5dc97-159">Contoso US</span><span class="sxs-lookup"><span data-stu-id="5dc97-159">Contoso US</span></span>  |<span data-ttu-id="5dc97-160">Hour</span><span class="sxs-lookup"><span data-stu-id="5dc97-160">Hour</span></span> | <span data-ttu-id="5dc97-161">145</span><span class="sxs-lookup"><span data-stu-id="5dc97-161">145</span></span>|<span data-ttu-id="5dc97-162">USD</span><span class="sxs-lookup"><span data-stu-id="5dc97-162">USD</span></span>     |
| <span data-ttu-id="5dc97-163">Moje company_Band2</span><span class="sxs-lookup"><span data-stu-id="5dc97-163">My company_Band2</span></span> | <span data-ttu-id="5dc97-164">Blaho India</span><span class="sxs-lookup"><span data-stu-id="5dc97-164">Contoso India</span></span> |<span data-ttu-id="5dc97-165">Hour</span><span class="sxs-lookup"><span data-stu-id="5dc97-165">Hour</span></span>|   <span data-ttu-id="5dc97-166">67</span><span class="sxs-lookup"><span data-stu-id="5dc97-166">67</span></span>|<span data-ttu-id="5dc97-167">USD</span><span class="sxs-lookup"><span data-stu-id="5dc97-167">USD</span></span>     |
