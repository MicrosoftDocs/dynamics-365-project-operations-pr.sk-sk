---
title: Použitie existujúceho poľa v Project Service ako cenovej dimenzie
description: Táto téma poskytuje informácie o používaní existujúcich polí Project Service ako cenových dimenzií.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
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
ms.openlocfilehash: 415e346f88e60cb064f3327bfb35e21bd1c89014
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084442"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="0410b-103">Použitie existujúceho poľa v Project Service ako cenovej dimenzie</span><span class="sxs-lookup"><span data-stu-id="0410b-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="0410b-104">Project Service Automation (PSA) má veľa polí v entite **Skutočné hodnoty** , ktoré môžu byť použité ako cenové dimenzie pre ceny založení na zdroji v projektových organizáciách.</span><span class="sxs-lookup"><span data-stu-id="0410b-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="0410b-105">Jedným z bežných polí je **Rezervovateľný zdroj**.</span><span class="sxs-lookup"><span data-stu-id="0410b-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="0410b-106">Menšie spoločnosti, ktoré majú menej ako 20-30 fakturovateľných zdrojov môže zistiť, že fakturovanie a sadzby nákladov špecifické pre každý zdroj je jednoduchší prístup.</span><span class="sxs-lookup"><span data-stu-id="0410b-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="0410b-107">Avšak, ako fakturovateľná pracovná sila rastie, mohlo by to stať nerealistické udržať ako náklady na zdroje a sadzby fakturácie sa začnú líšiť pri povyšovaní zdrojov, získavaní viacerých skúseností alebo získavaní rôznych súborov zručností.</span><span class="sxs-lookup"><span data-stu-id="0410b-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="0410b-108">Keďže tento prístup stále funguje pre spoločnosti určitej veľkosti, pozrite si tému, [Použiť rezervovateľný zdroj ako cenovú dimenziu](bookable-resource-pricing-dimension.md), aby ste pochopili, ako je možné použiť existujúcu oblasť Project Service ako cenovú dimenziu.</span><span class="sxs-lookup"><span data-stu-id="0410b-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="0410b-109">Ďalším príkladom je transakcie kategórie.</span><span class="sxs-lookup"><span data-stu-id="0410b-109">Another example is that of transaction category.</span></span> <span data-ttu-id="0410b-110">Zákazníci a realizátori použili kategóriu transakcií v PSA na klasifikáciu práce a využitie poľa na cenu a náklady na základe kategórie práce.</span><span class="sxs-lookup"><span data-stu-id="0410b-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="0410b-111">Ďalšie informácie nájdete v téme [Použiť kategóriu transakcií ako dimenziu cien](transaction-category-pricing-dimension.md).</span><span class="sxs-lookup"><span data-stu-id="0410b-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>