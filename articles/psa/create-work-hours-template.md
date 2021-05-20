---
title: Vytvorenie šablóny pracovnej doby
description: Táto téma opisuje postup vytvorenia šablóny pracovných hodín v Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981274"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="6f1dd-103">Vytvorenie šablóny pracovných hodín (Project Service)</span><span class="sxs-lookup"><span data-stu-id="6f1dd-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6f1dd-104">Ak chcete vytvoriť a spravovať projekt, musíte na projekt použiť šablónu kalendára.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="6f1dd-105">Šablóna kalendára definuje nasledujúce atribúty projektu:</span><span class="sxs-lookup"><span data-stu-id="6f1dd-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="6f1dd-106">Pracovná doba vrátane času začiatku a konca</span><span class="sxs-lookup"><span data-stu-id="6f1dd-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="6f1dd-107">Pracovné dni</span><span class="sxs-lookup"><span data-stu-id="6f1dd-107">Working days</span></span>
- <span data-ttu-id="6f1dd-108">Výnimky z kalendára, napríklad dni pracovného pokoja</span><span class="sxs-lookup"><span data-stu-id="6f1dd-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="6f1dd-109">Šablóna kalendára, ktorá sa použije na projekt, je kópiou šablóny kalendára definovanej v nastaveniach vašej organizácie.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="6f1dd-110">Ak zmeníte šablónu kalendára, tieto zmeny sa neprenesú na pracovnú dobu projektu.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="6f1dd-111">Pre zmenu pracovnej doby projektu je potrebné použiť novú šablónu.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="6f1dd-112">Na vytvorenie šablóny kalendára pre vašu organizáciu existujú dve kľúčové požiadavky:</span><span class="sxs-lookup"><span data-stu-id="6f1dd-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="6f1dd-113">Definujte požadovaný pracovný čas šablóny pomocou nového alebo existujúceho rezervovateľného zdroja.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="6f1dd-114">Vytvorte novú šablónu kalendára a priraďte ju k rezervovateľnému prostriedku.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="6f1dd-115">**Definovať pracovný čas šablóny**</span><span class="sxs-lookup"><span data-stu-id="6f1dd-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="6f1dd-116">Prejdite do **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="6f1dd-117">Vytvorte nový zdroj, ktorý bude odkazovať v šablóne kalendára, alebo vyberte existujúci zdroj.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="6f1dd-118">Stlačte kartu **Pracovný čas** na karte zdroja a vykonajte pokyny v priečinku v časti [Nastavenie pracovnej doby zdroja](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) a nakonfigurujte pravidlá kalendára.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="6f1dd-119">**Vytvorí novú šablónu kalendára**</span><span class="sxs-lookup"><span data-stu-id="6f1dd-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="6f1dd-120">Prejdite do ponuky **Nastavenia** \> **Šablóna kalendára**.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="6f1dd-121">Stlačte možnosť **Nový** a zadajte názov, popis a prostriedok šablóny.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="6f1dd-122">Keď sa na prostriedok odkazuje v šablóne kalendára, kópia kalendára prostriedku je spojená so šablónou kalendára.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="6f1dd-123">Ak dôjde k zmene pracovného času skopírovanej šablóny, tieto zmeny sa nezanesú do šablóny kalendára.</span><span class="sxs-lookup"><span data-stu-id="6f1dd-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="6f1dd-124">Pozrite si tiež</span><span class="sxs-lookup"><span data-stu-id="6f1dd-124">See Also</span></span>  
 [<span data-ttu-id="6f1dd-125">Nastavenie zdrojov</span><span class="sxs-lookup"><span data-stu-id="6f1dd-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
