---
title: Správa komplexných jednotiek pre riadky zmlúv založených na produkte – čiastočné
description: Táto téma poskytuje informácie o podpore predaja produktov založených na predplatnom.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a58a13c8186f36e6031fe3c6f3c3a57ea920ac9e
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177395"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="b2e2a-103">Správa komplexných jednotiek pre riadky zmlúv založených na produkte – čiastočné</span><span class="sxs-lookup"><span data-stu-id="b2e2a-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="b2e2a-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="b2e2a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b2e2a-105">Dynamics 365 Project Operations používa množstvo faktorov na podporu predaja produktov založených na predplatnom.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="b2e2a-106">V prípade produktov založených na predplatnom sa množstvo v riadku zmluvy alebo projektu vyjadrí ako počet používateľských mesiacov.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="b2e2a-107">Cena predplatného softvéru je uložená v katalógu ako cena za používateľa mesačne.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="b2e2a-108">Počas predajného procesu je cena v riadku zmluvy zvyčajne cena za používateľa, za mesiac, ktorá bola dohodnutá a zľavnená agentom predaja.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="b2e2a-109">Každý obchod má iný počet užívateľov a iný počet predplatných mesiacov.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="b2e2a-110">Množstvo, ktoré sa používa na výpočet čiastky riadka zmluvy, je produktom počtu používateľov a počtu mesiacov predplatného.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="b2e2a-111">Na podporu tohto druhu predaja, podporuje Project Operations koncept *faktorov kvantity*.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="b2e2a-112">Faktory kvantity sa spoliehajú na atribúty produktov.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="b2e2a-113">Keď nakonfigurujete špecifické vlastnosti produktu, môžete označiť podmnožinu týchto vlastností alebo všetky vlastnosti ako faktory kvantity.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="b2e2a-114">Project Operations overuje, že iba číselné vlastnosti alebo vlastnosti produktu, ktoré majú číselný typ údajov, sú označené ako faktory kvantity.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="b2e2a-115">Keď sa produkt s nakonfigurovanými faktormi kvantity pridá do riadku zmluvy, pole **Množstvo** sa zmení iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="b2e2a-116">Po zadaní hodnôt pre vlastnosti produktu, ktoré sú faktormi kvantity, Project Operations vypočíta množstvo riadka zmluvy.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="b2e2a-117">Napríklad, Dynamics 365 Sales môže mať nasledujúce vlastnosti:</span><span class="sxs-lookup"><span data-stu-id="b2e2a-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="b2e2a-118">**Počet používateľov**: Počet používateľov.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="b2e2a-119">**Počet mesiacov**: Počet mesiacov predplatného.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="b2e2a-120">**SKU produktu**: Skladová jednotka (SKU) pre produkt.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="b2e2a-121">Vlastnosti **Počet používateľov** a **Počet mesiacov** môžu byť označené ako faktory kvantity úpravou vlastnosti produktového riadku.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="b2e2a-122">Ak chcete z vlastností produktu vytvoriť faktory množstva, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="b2e2a-123">V časti **Project Operations** vyberte **Predajné produkty**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="b2e2a-124">Otvorte produkt, pre ktorý potrebujete nastaviť faktory kvantity.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="b2e2a-125">Skontrolujte, či má produkt už nastavené vlastnosti.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="b2e2a-126">Na stránke **Informácie o projekte** vyberte kartu **Faktory kvantity**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="b2e2a-127">Vo vedľajšej mriežke vyberte **+ Výpočet nového poľa**.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="b2e2a-128">Zadajte názov **Faktora kvantity** a vyberte hodnotu vlastnosti, ktorá sa mapuje na výpočet poľa.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="b2e2a-129">Uloží a zavrie formulár.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-129">Save and close the form.</span></span>
7. <span data-ttu-id="b2e2a-130">Opakujte kroky 2 až 6 pre všetky vlastnosti, ktoré spolu tvoria kvantitu riadok zmluvy založenej na produkte.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="b2e2a-131">Keď sú nastavené faktory kvantity, keď používateľ vytvorí pre tento produkt riadok zmluvy, kvantita riadka zmluvy sa uzamkne.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="b2e2a-132">Kvantita sa potom vypočíta ako súčin hodnôt vlastností pre daný riadok zmluvy.</span><span class="sxs-lookup"><span data-stu-id="b2e2a-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>
