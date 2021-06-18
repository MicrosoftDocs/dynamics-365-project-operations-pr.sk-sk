---
title: Definovanie kalendárov projektu
description: Táto téma poskytuje informácie o tom, ako použiť šablónu kalendára na projekt na sledovanie harmonogramu projektu.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999015"
---
# <a name="define-project-calendars"></a><span data-ttu-id="5b515-103">Definovanie kalendárov projektu</span><span class="sxs-lookup"><span data-stu-id="5b515-103">Define project calendars</span></span>

<span data-ttu-id="5b515-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="5b515-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5b515-105">Ak chcete vytvoriť a spravovať projekt, musíte na projekt použiť šablónu kalendára.</span><span class="sxs-lookup"><span data-stu-id="5b515-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="5b515-106">Šablóna kalendára definuje nasledujúce atribúty projektu:</span><span class="sxs-lookup"><span data-stu-id="5b515-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="5b515-107">Pracovná doba vrátane času začiatku a konca</span><span class="sxs-lookup"><span data-stu-id="5b515-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="5b515-108">Pracovné dni</span><span class="sxs-lookup"><span data-stu-id="5b515-108">Working days</span></span>
- <span data-ttu-id="5b515-109">Výnimky z kalendára, napríklad dni pracovného pokoja</span><span class="sxs-lookup"><span data-stu-id="5b515-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="5b515-110">Šablóna kalendára, ktorá sa použije na projekt, je kópiou šablóny kalendára definovanej v nastaveniach vašej organizácie.</span><span class="sxs-lookup"><span data-stu-id="5b515-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="5b515-111">Ak zmeníte šablónu kalendára, tieto zmeny sa neprenesú na pracovnú dobu projektu.</span><span class="sxs-lookup"><span data-stu-id="5b515-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="5b515-112">Pre zmenu pracovnej doby projektu je potrebné použiť novú šablónu.</span><span class="sxs-lookup"><span data-stu-id="5b515-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="5b515-113">Na vytvorenie šablóny kalendára pre vašu organizáciu existujú dve kľúčové požiadavky:</span><span class="sxs-lookup"><span data-stu-id="5b515-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="5b515-114">Definujte požadovaný pracovný čas šablóny pomocou nového alebo existujúceho rezervovateľného zdroja.</span><span class="sxs-lookup"><span data-stu-id="5b515-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="5b515-115">Vytvorte novú šablónu kalendára a priraďte ju k rezervovateľnému prostriedku.</span><span class="sxs-lookup"><span data-stu-id="5b515-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="5b515-116">**Definovať pracovný čas šablóny**</span><span class="sxs-lookup"><span data-stu-id="5b515-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="5b515-117">Prejdite do **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="5b515-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="5b515-118">Vytvorte nový zdroj, ktorý bude odkazovať v šablóne kalendára, alebo vyberte existujúci zdroj.</span><span class="sxs-lookup"><span data-stu-id="5b515-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="5b515-119">Stlačte kartu **Pracovný čas** na karte zdroja a vykonajte pokyny v priečinku v časti [Nastavenie pracovnej doby zdroja](/dynamics365/field-service/set-work-hours-resource.md) a nakonfigurujte pravidlá kalendára.</span><span class="sxs-lookup"><span data-stu-id="5b515-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="5b515-120">**Vytvorí novú šablónu kalendára**</span><span class="sxs-lookup"><span data-stu-id="5b515-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="5b515-121">Prejdite do ponuky **Nastavenia** \> **Šablóna kalendára**.</span><span class="sxs-lookup"><span data-stu-id="5b515-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="5b515-122">Stlačte možnosť **Nový** a zadajte názov, popis a prostriedok šablóny.</span><span class="sxs-lookup"><span data-stu-id="5b515-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="5b515-123">Keď sa na prostriedok odkazuje v šablóne kalendára, kópia kalendára prostriedku je spojená so šablónou kalendára.</span><span class="sxs-lookup"><span data-stu-id="5b515-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="5b515-124">Ak dôjde k zmene pracovného času skopírovanej šablóny, tieto zmeny sa nezanesú do šablóny kalendára.</span><span class="sxs-lookup"><span data-stu-id="5b515-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="5b515-125">Šablónu práce teraz môžete priradiť k šablóne kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="5b515-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

