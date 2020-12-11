---
title: Príjem položiek z nákupnej objednávky z požiadaviek na položku
description: Táto téma vysvetľuje, ako prijímať položky na nákupnej objednávke z požiadavky na položku.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084531"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="dd4e2-103">Príjem položiek z nákupnej objednávky z požiadaviek na položku</span><span class="sxs-lookup"><span data-stu-id="dd4e2-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd4e2-104">Táto téma vysvetľuje, ako prijímať položky na nákupnej objednávke z požiadavky na položku.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="dd4e2-105">Použitím požiadavky na položku namiesto transakcie s položkou môžete naplánovať dodanie tesne pred skutočným použitím položky, vytvoriť objednávku, zahrnúť položku do rámca obchodnej zmluvy a zahrnúť požiadavku na položku do plánovania výroby.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="dd4e2-106">Táto úloha používa množinu údajov USSI.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="dd4e2-107">Na navigačnej table prejdite do **Moduly > Projektové riadenie a účtovníctvo > Projekty > Všetky projekty**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="dd4e2-108">V zozname vyberte odkaz v požadovanom riadku.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="dd4e2-109">Na table Akcia vyberte možnosť **Plán**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="dd4e2-110">Vyberte **Požiadavky na položku**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="dd4e2-111">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-111">Select **New**.</span></span>
6. <span data-ttu-id="dd4e2-112">V novom riadku zadajte alebo vyberte hodnotu v poli **Číslo položky**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="dd4e2-113">V poli **Množstvo** zadajte číslo.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="dd4e2-114">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-114">Select **Save**.</span></span>
9. <span data-ttu-id="dd4e2-115">Na table Akcia vyberte možnosť **Správa**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="dd4e2-116">Vyberte **Funkcie**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-116">Select **Functions**.</span></span>
11. <span data-ttu-id="dd4e2-117">Vyberte **Vytvorenie nákupnej objednávky**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="dd4e2-118">Vyberte začiarkavacie políčko **Zahrnúť všetko**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="dd4e2-119">V poli **Účet predajcu** zadajte alebo vyberte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="dd4e2-120">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-120">Select **OK**.</span></span>
15. <span data-ttu-id="dd4e2-121">Na navigačnej table prejdite do **Moduly > Záväzky > Nákupné objednávky > Všetky nákupné objednávky**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="dd4e2-122">V zozname vyberte odkaz v požadovanom riadku.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="dd4e2-123">Na table Akcia vyberte možnosť **Kúpiť**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="dd4e2-124">Vyberte položku **Potvrdiť**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="dd4e2-125">Na table Akcia vyberte možnosť **Prijať**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="dd4e2-126">Vyberte **Príjem produktu**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="dd4e2-127">V poli **Príjem produktu** zadajte hodnotu.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="dd4e2-128">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd4e2-128">Select **OK**.</span></span>
