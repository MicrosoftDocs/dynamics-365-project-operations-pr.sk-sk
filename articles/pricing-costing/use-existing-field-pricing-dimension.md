---
title: Polia Project Operations ako cenové dimenzie
description: Táto téma poskytuje informácie s využitím polí, ako sú cenové dimenzie v aplikácii Dynamics 365 Project Operations.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a29460b2a9dc9a9755e7e28a6cd9712c6b06e8c6
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004505"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="a8d81-103">Polia aplikácie Project Operations ako cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="a8d81-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="a8d81-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="a8d81-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a8d81-105">Entita **Skutočné hodnoty** má veľa polí, ktoré možno použiť ako cenové dimenzie pre naceňovanie založené na zdrojoch.</span><span class="sxs-lookup"><span data-stu-id="a8d81-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="a8d81-106">Jedným z bežných polí je **Rezervovateľný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="a8d81-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="a8d81-107">Menšie spoločnosti, ktoré majú menej ako 20-30 fakturovateľných zdrojov môže zistiť, že fakturovanie a sadzby nákladov špecifické pre každý zdroj je jednoduchší prístup.</span><span class="sxs-lookup"><span data-stu-id="a8d81-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="a8d81-108">S rastom zúčtovateľnej pracovnej sily by sa však udržiavanie sadzieb závislé od zdrojov mohlo stať nereálnou.</span><span class="sxs-lookup"><span data-stu-id="a8d81-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="a8d81-109">Náklady na zdroje a fakturačné sadzby sa začnú líšiť v závislosti od propagácie zdrojov, získania ďalších skúseností alebo získania iného súboru zručností.</span><span class="sxs-lookup"><span data-stu-id="a8d81-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="a8d81-110">Ďalším príkladom je transakcie kategórie.</span><span class="sxs-lookup"><span data-stu-id="a8d81-110">Another example is that of transaction category.</span></span> <span data-ttu-id="a8d81-111">Zákazníci a realizátori použili kategóriu transakcií na klasifikáciu práce a využitie poľa na cenu a náklady na základe kategórie práce.</span><span class="sxs-lookup"><span data-stu-id="a8d81-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]