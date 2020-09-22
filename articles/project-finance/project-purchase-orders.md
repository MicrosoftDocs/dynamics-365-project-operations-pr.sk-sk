---
title: Nákupné objednávky pre projekt
description: Tento článok popisuje rôzne metódy, ktoré môžete použiť na vytvorenie nákupných objednávok pre projekt. Metóda, ktorú použijete, závisí od účelu nákupnej objednávky a od toho, kedy sa zakúpené položky spotrebujú a zaúčtujú v rámci projektu.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755573"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="8ea9c-104">Nákupné objednávky pre projekt</span><span class="sxs-lookup"><span data-stu-id="8ea9c-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ea9c-105">Tento článok popisuje rôzne metódy, ktoré môžete použiť na vytvorenie nákupných objednávok pre projekt.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="8ea9c-106">Metóda, ktorú použijete, závisí od účelu nákupnej objednávky a od toho, kedy sa zakúpené položky spotrebujú a zaúčtujú v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="8ea9c-107">Metódy vytvárania nákupnej objednávky</span><span class="sxs-lookup"><span data-stu-id="8ea9c-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="8ea9c-108">Môžete použiť jednu z nasledujúcich metód na vytvorenie nákupnej objednávky v časti Projektové riadenie a účtovníctvo.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="8ea9c-109">Účel nákupnej objednávky určuje, kedy sa nákupná objednávka spotrebuje, a tým pádom kedy sa položky zaúčtujú v rámci projektu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8ea9c-110">Spôsob</span><span class="sxs-lookup"><span data-stu-id="8ea9c-110">Method</span></span></th>
<th><span data-ttu-id="8ea9c-111">Účel</span><span class="sxs-lookup"><span data-stu-id="8ea9c-111">Purpose</span></span></th>
<th><span data-ttu-id="8ea9c-112">Spotreba položiek</span><span class="sxs-lookup"><span data-stu-id="8ea9c-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ea9c-113">Vytvorte nákupnú objednávku priamo z projektu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="8ea9c-114">Použite túto metóda na nákup položiek od externého dodávateľa na spotrebu v projekte.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="8ea9c-115">Nákupnú objednávku môžete vytvoriť dvoma spôsobmi:</span><span class="sxs-lookup"><span data-stu-id="8ea9c-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="8ea9c-116">Zo samotného projektu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-116">From the project itself.</span></span> <span data-ttu-id="8ea9c-117">V takom prípade je projekt už pre nákupnú objednávku definovaný.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="8ea9c-118">Navigáciou k nákupnej objednávke projektu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="8ea9c-119">Musíte vybrať dodávateľa aj projekt, pre ktorý chcete vytvoriť nákupnú objednávku.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="8ea9c-120">Položky sa spotrebujú, keď sa aktualizuje faktúra dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ea9c-121">Vytvorte nákupnú objednávku z predajnej objednávky.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="8ea9c-122">Táto metóda sa používa na nákup položiek, keď vytvárate predajnú objednávku z projektu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="8ea9c-123">Položky sa spotrebujú, keď sa predajná objednávka fakturuje zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ea9c-124">Vytvorte nákupnú objednávku z požiadavky na položku.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="8ea9c-125">Táto metóda sa používa na nákup položiek, keď vytvárate požiadavku na položku z projektu.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="8ea9c-126">Položky sa spotrebujú, keď sa aktualizuje dodací list s požiadavkou na položku.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="8ea9c-127">Pri aktualizácii faktúry dodávateľa alebo dodacieho listu sa zobrazí výzva na aktualizáciu dodacieho listu podľa požiadavky na položku.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="8ea9c-128">Viac informácií sa dozviete v časti [Príjem položiek z nákupnej objednávky z požiadaviek na položku](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="8ea9c-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

