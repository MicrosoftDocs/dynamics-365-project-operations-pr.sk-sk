---
title: Náklady v riadkoch zmlúv založených na produkte – čiastočné
description: Táto téma poskytuje informácie o vytváraní
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a81c972f36179621f0547c24fc53d294485f638c
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764478"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="29bf1-103">Náklady v riadkoch zmlúv založených na produkte – čiastočné</span><span class="sxs-lookup"><span data-stu-id="29bf1-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="29bf1-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="29bf1-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="29bf1-105">Riadky zmlúv založené na produkte Dynamics 365 Project Operations zahŕňajú pole **Obstarávacia cena**, v ktorom sa ukladá obstarávacia cena produktu pre následné výpočty ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="29bf1-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="29bf1-106">Keď sa pre katalógový produkt vytvorí riadok zmluvy založený na produkte, náklady v tomto riadku sa štandardne nastavia podľa poľa **Štandardné náklady** v katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="29bf1-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="29bf1-107">Pole **Štandardné náklady** v katalógu produktov je nastavené v základnej mene organizácie.</span><span class="sxs-lookup"><span data-stu-id="29bf1-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="29bf1-108">Keď sú jednotkové náklady predvolené pre riadok zmluvy, prevedú sa na menu predaja v zmluve.</span><span class="sxs-lookup"><span data-stu-id="29bf1-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="29bf1-109">Jednotkový náklad v riadku zmluvy založenej na produkte</span><span class="sxs-lookup"><span data-stu-id="29bf1-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="29bf1-110">Jednotkové náklady v riadku zmluvy založenej na produkte umožňujú rôzne produktové náklady pre každý predaj jednotky.</span><span class="sxs-lookup"><span data-stu-id="29bf1-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="29bf1-111">Aj keď to nie je vždy potrebné, existujú určité scenáre, pri ktorých môže dodávateľovi zákazníkovi odpočítať náklady na produkt.</span><span class="sxs-lookup"><span data-stu-id="29bf1-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="29bf1-112">Posúďte nasledujúci scenár:</span><span class="sxs-lookup"><span data-stu-id="29bf1-112">Consider the following scenario:</span></span>

<span data-ttu-id="29bf1-113">Spoločnosť Fabrikam Robotics inštaluje robotické ramená na montážnych linkách spoločnosti Adatum Corporation.</span><span class="sxs-lookup"><span data-stu-id="29bf1-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="29bf1-114">Spoločnosť Fabrikam poskytuje inštalačné služby, ale robotické ramená pochádzajú od spoločnosti Trey Research.</span><span class="sxs-lookup"><span data-stu-id="29bf1-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="29bf1-115">Ak inštalácia robotických ramien v spoločnosti Adatum Corporation otvorí novú priemyselnú vertikálu pre robotické ramená od spoločnosti Trey Research, môže poskytnúť spoločnosti Fabrikam špeciálnu zľavu za tento obchod.</span><span class="sxs-lookup"><span data-stu-id="29bf1-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="29bf1-116">V takom prípade vytvorí spoločnosť Fabrikam pre spoločnosť Robotic Arms riadok zmluvy založený na produkte.</span><span class="sxs-lookup"><span data-stu-id="29bf1-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="29bf1-117">Pri tejto zmluve sa zadáva jednotkový náklad.</span><span class="sxs-lookup"><span data-stu-id="29bf1-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="29bf1-118">Náklad sa líši od nákladu na robotické ramená od spoločnosti Trey Research.</span><span class="sxs-lookup"><span data-stu-id="29bf1-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>
