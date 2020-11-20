---
title: Polia Project Operations ako cenové dimenzie
description: Táto téma poskytuje informácie o používaní polí ako cenových dimenzií v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 59367b35f15f806b109f606e912edc487d9e7685
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119257"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="64310-103">Polia Project Operations ako cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="64310-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="64310-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="64310-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="64310-105">Entita **Skutočné hodnoty** má veľa polí, ktoré možno použiť ako cenové dimenzie pre naceňovanie založené na zdrojoch.</span><span class="sxs-lookup"><span data-stu-id="64310-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="64310-106">Jedným z bežných polí je **Rezervovateľný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="64310-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="64310-107">Menšie spoločnosti, ktoré majú menej ako 20-30 fakturovateľných zdrojov môže zistiť, že fakturovanie a sadzby nákladov špecifické pre každý zdroj je jednoduchší prístup.</span><span class="sxs-lookup"><span data-stu-id="64310-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="64310-108">S rastom zúčtovateľnej pracovnej sily by sa však udržiavanie sadzieb závislé od zdrojov mohlo stať nereálnou.</span><span class="sxs-lookup"><span data-stu-id="64310-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="64310-109">Náklady na zdroje a fakturačné sadzby sa začnú líšiť v závislosti od propagácie zdrojov, získania ďalších skúseností alebo získania iného súboru zručností.</span><span class="sxs-lookup"><span data-stu-id="64310-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="64310-110">Ďalším príkladom je transakcie kategórie.</span><span class="sxs-lookup"><span data-stu-id="64310-110">Another example is that of transaction category.</span></span> <span data-ttu-id="64310-111">Zákazníci a realizátori použili kategóriu transakcií na klasifikáciu práce a využitie poľa na cenu a náklady na základe kategórie práce.</span><span class="sxs-lookup"><span data-stu-id="64310-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>
