---
title: Vytvorenie a aplikovanie podmienok uchovania platieb dodávateľa
description: Táto téma poskytuje informácie o tom, ako nastaviť a udržiavať podmienky uchovania platieb dodávateľa.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084501"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="fc0a3-103">Vytvorenie a aplikovanie podmienok uchovania platieb dodávateľa</span><span class="sxs-lookup"><span data-stu-id="fc0a3-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="fc0a3-104">Nastavenie podmienok uchovania platieb dodávateľa pre projekt je užitočné, keď chce vaša organizácia ponechať časť uskutočnených platieb dodávateľovi.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="fc0a3-105">Napríklad, keď chcete zadržať platbu pre dodávateľa, kým dodané produkty nesplnia vaše očakávania.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="fc0a3-106">Podmienky uchovania platby dodávateľa je možné určiť pri rokovaniach o dodávateľskej zmluve.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="fc0a3-107">Vytvorenie podmienok uchovania platieb dodávateľa</span><span class="sxs-lookup"><span data-stu-id="fc0a3-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="fc0a3-108">Môžete zadať percento platby dodávateľa na uchovanie a percento predtým uchovaných súm, ktoré sa majú uvoľniť.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="fc0a3-109">Čiastky sa automaticky uchovávajú na faktúrach dodávateľov, kým zmluva nedosiahne určený stav dokončenia.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="fc0a3-110">Po nastavení podmienok uchovania ich môžete použiť na akýkoľvek projekt pre daného dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="fc0a3-111">Pomocou nasledujúcich krokov môžete nastaviť a udržiavať podmienky uchovania pre platby dodávateľov.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="fc0a3-112">Prejdite do časti **Projektové riadenie a účtovníctvo** > **Uchovanie** > **Podmienky uchovania platby dodávateľa**.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="fc0a3-113">Vyberte **Nový** na pridanie nových podmienok uchovania pre dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="fc0a3-114">Automaticky sa zadá hodnota **ID pravidla** pre nové podmienky.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="fc0a3-115">Zadajte stručný popis do poľa **Popis** a na rýchlej karte **Podmienky** vyberte možnosť **Pridať riadok** na zadanie hodnoty podmienok pre nasledujúce položky:</span><span class="sxs-lookup"><span data-stu-id="fc0a3-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="fc0a3-116">**Percento dodaných jednotiek** : Zadajte percento dokončenia pre podmienku.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="fc0a3-117">Čiastky sa automaticky uchovávajú na faktúrach dodávateľov, kým sa fáza dokončenia projektu nebude rovnať stanovenému percentu.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="fc0a3-118">Napríklad, ak zadáte 50,00, sumy sa uchovajú, kým nebude projekt dokončený na 50 percent.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="fc0a3-119">**Percento na uchovanie** : Zadajte percento z čiastky faktúry dodávateľa, ktoré sa má uchovať.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="fc0a3-120">Napríklad, ak zadáte 10,00, tak sa 10 percent zo sumy na faktúre dodávateľa ponechá, kým projekt nedosiahne percentuálny podiel dokončenia stanovený v poli **Percento dodaných jednotiek**.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="fc0a3-121">**Percento na uvoľnenie** : Vyberte **Pridať riadok** na zadanie percenta zo všetkých predtým uchovaných súm, ktoré sa majú uvoľniť pre zvolenú úroveň dokončenia projektu.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="fc0a3-122">Ak máte viac ako jeden medzník pre rôzne úrovne dokončenia projektu, zadajte samostatný riadok podmienky uchovania pre dodávateľa pre každé pravidlo uchovania.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="fc0a3-123">Každý riadok môže určiť iné percento uchovania a iné percento uvoľnenia pre každú určenú úroveň dokončenia projektu.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="fc0a3-124">Po vytvorení podmienok uchovania pre dodávateľa môžete použiť tieto podmienky pre projekt.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="fc0a3-125">Použitie dodávateľských podmienok uchovania pre projekt</span><span class="sxs-lookup"><span data-stu-id="fc0a3-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="fc0a3-126">Prejdite na položku **Projektové riadenie a účtovníctvo** > **Projekty** > **Všetky projekty** a otvorte projekt na stránke so zoznamom projektov.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="fc0a3-127">Na karte FastTab **Zmluvy s predajcom** stlačte možnosť **Pridať riadok**.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="fc0a3-128">V poli **Kód účtu** vyberte jednu z nasledujúcich možností:</span><span class="sxs-lookup"><span data-stu-id="fc0a3-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="fc0a3-129">**Tabuľka** : Podmienky uchovania dodávateľa sa vzťahujú na jedného dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="fc0a3-130">**Skupina** : Podmienky uchovania dodávateľa sa vzťahujú na všetkých dodávateľov v skupine dodávateľov.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="fc0a3-131">**Všetky** : Podmienky uchovania dodávateľa sa vzťahujú na všetkých dodávateľov.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="fc0a3-132">V poli **Dodávateľ/skupina dodávateľov** vyberte dodávateľa alebo skupinu dodávateľov, na ktorých sa vzťahujú podmienky uchovania dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="fc0a3-133">Ak ste vybrali **Všetky** v predchádzajúcom kroku nie je toto pole k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="fc0a3-134">V poli **Podmienky uchovania dodávateľa** vyberte retenčné podmienky, ktoré ste vytvorili v predchádzajúcom postupe.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="fc0a3-135">Ak má projekt pre dodávateľa nastavené aj podmienky typu „zaplatiť po zaplatení“ (PWP), zadajte limitnú hodnotu pre projekt do poľa **Percentuálna hodnota prahovej hodnoty PWP**.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="fc0a3-136">Podmienky uchovania dodávateľa sa zobrazia aj na objednávkach, ktoré vytvoríte pre dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="fc0a3-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
