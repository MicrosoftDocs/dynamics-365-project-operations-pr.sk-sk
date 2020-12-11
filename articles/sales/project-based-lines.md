---
title: Riadky príležitostí založených na projekte
description: Táto téma poskytuje informácie o práci s riadkami príležitostí založených na projekte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ede474e3d8830b420dc5b183f14327206c10288
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181966"
---
# <a name="project-based-opportunity-lines"></a><span data-ttu-id="ae914-103">Riadky príležitostí založených na projekte</span><span class="sxs-lookup"><span data-stu-id="ae914-103">Project-based opportunity lines</span></span>

<span data-ttu-id="ae914-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="ae914-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="ae914-105">Riadky príležitostí založené na projekte sú k dispozícii iba v prípade príležitostí založených na projekte.</span><span class="sxs-lookup"><span data-stu-id="ae914-105">Project-based opportunity lines are only available in project-based opportunities.</span></span> <span data-ttu-id="ae914-106">Záznamy príležitostí založených na projekte majú hodnoty poľa **Typ** nastavenú na **Založené na práci**.</span><span class="sxs-lookup"><span data-stu-id="ae914-106">Project-based opportunity records have the **Type** field value set to **Work-based**.</span></span>

<span data-ttu-id="ae914-107">Riadky príležitostí založené na projekte sú riadkové položky, ktoré sa zákazníkovi doručia pomocou projektu.</span><span class="sxs-lookup"><span data-stu-id="ae914-107">Project-based opportunity lines are the line items that will be delivered to the customer using a project.</span></span> <span data-ttu-id="ae914-108">Projekt však nemožno spojiť s riadkom príležitosti založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="ae914-108">However, a project can't be tied to a project-based opportunity line.</span></span> <span data-ttu-id="ae914-109">Projekty je možné naviazať ďalej na riadkové položky v etape **Cenová ponuka**, pretože príležitosť sa zvyčajne vyskytuje v počiatočnej etape obchodu.</span><span class="sxs-lookup"><span data-stu-id="ae914-109">Projects can be tied to line items from the **Quote** stage onwards because typically the opportunity occurs in an early stage of a deal.</span></span> <span data-ttu-id="ae914-110">Rozhodnutie, koľko projektov sa použije na dodanie diela pre zákazníka, je rozhodnutím, ktoré sa urobí neskôr vo fáze predaja.</span><span class="sxs-lookup"><span data-stu-id="ae914-110">The determination of how many projects will be used to deliver the work for the customer is a decision that is made later in the sales phase.</span></span> <span data-ttu-id="ae914-111">Využite fázu príležitosti na identifikáciu jednotlivých komponentov dodávky pre zákazníka.</span><span class="sxs-lookup"><span data-stu-id="ae914-111">Use the opportunity phase to identify the discrete delivery components for the customer.</span></span> <span data-ttu-id="ae914-112">Rozhodnutia týkajúce sa skutočného počtu projektov použitých na dodanie týchto komponentov je možné vytlačiť, kým nebudú známe ďalšie informácie o samotnej práci.</span><span class="sxs-lookup"><span data-stu-id="ae914-112">The decisions surrounding the actual number of projects used to deliver these components can be pushed out until more information is known about the work itself.</span></span>

<span data-ttu-id="ae914-113">Nižšie sú uvedené polia na riadku príležitostí založených na projekte:</span><span class="sxs-lookup"><span data-stu-id="ae914-113">Below are the fields on a project-based opportunity line:</span></span>

| <span data-ttu-id="ae914-114">**Pole**</span><span class="sxs-lookup"><span data-stu-id="ae914-114">**Field**</span></span> | <span data-ttu-id="ae914-115">**Miesto**</span><span class="sxs-lookup"><span data-stu-id="ae914-115">**Location**</span></span> | <span data-ttu-id="ae914-116">**Opis**</span><span class="sxs-lookup"><span data-stu-id="ae914-116">**Description**</span></span> | <span data-ttu-id="ae914-117">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="ae914-117">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="ae914-118">Typ produktu</span><span class="sxs-lookup"><span data-stu-id="ae914-118">Product Type</span></span> | <span data-ttu-id="ae914-119">Karta Všeobecné (skrytá)</span><span class="sxs-lookup"><span data-stu-id="ae914-119">General tab (hidden)</span></span> | <span data-ttu-id="ae914-120">Toto je pole množiny možností.</span><span class="sxs-lookup"><span data-stu-id="ae914-120">This is an option set field.</span></span> <span data-ttu-id="ae914-121">Ak máte nainštalované Dynamics 365 Operations, jednou z dostupných možností je **Služba založená na projekte**.</span><span class="sxs-lookup"><span data-stu-id="ae914-121">If you have Dynamics 365 Operations installed, one the available options is, **Project-based service**.</span></span>  | <span data-ttu-id="ae914-122">Hodnota tohto poľa sa nastaví na **Služba založená na projekte**, keď vytvoríte riadok príležitosti založenej na projekte z mriežky riadkov na základe projektu v príležitosti.</span><span class="sxs-lookup"><span data-stu-id="ae914-122">The value of this field is set to **Project-based service** when you create the project-based opportunity line from the project-based lines grid on the Opportunity.</span></span> <br> <span data-ttu-id="ae914-123">Ak túto hodnotu zmeníte alebo prepíšete, vo vašich riadkových položkách založených na projekte nebude povolená funkčnosť projektu.</span><span class="sxs-lookup"><span data-stu-id="ae914-123">If you change or override this value, the project functionality won't be enabled on your project-based line items.</span></span> |
| <span data-ttu-id="ae914-124">Príležitosť</span><span class="sxs-lookup"><span data-stu-id="ae914-124">Opportunity</span></span> | <span data-ttu-id="ae914-125">Karta Všeobecné</span><span class="sxs-lookup"><span data-stu-id="ae914-125">General tab</span></span> | <span data-ttu-id="ae914-126">Toto pole je iba na čítanie a odkazuje na nadradený záznam príležitosti, ku ktorému patrí táto riadková položka.</span><span class="sxs-lookup"><span data-stu-id="ae914-126">This field is read-only and references the parent Opportunity record to which this line item belongs.</span></span> | <span data-ttu-id="ae914-127">Toto pole nemá žiadny následný dopad.</span><span class="sxs-lookup"><span data-stu-id="ae914-127">There is no downstream impact of this field.</span></span> |
| <span data-ttu-id="ae914-128">Meno</span><span class="sxs-lookup"><span data-stu-id="ae914-128">Name</span></span> | <span data-ttu-id="ae914-129">Karta Všeobecné</span><span class="sxs-lookup"><span data-stu-id="ae914-129">General tab</span></span> | <span data-ttu-id="ae914-130">Toto je upraviteľné textové pole, ktoré možno použiť na zabezpečenie krátkej identity tejto riadkovej položky</span><span class="sxs-lookup"><span data-stu-id="ae914-130">This is an editable text field that can be used to give a short identity to this line item</span></span> | <span data-ttu-id="ae914-131">Táto hodnota sa prenesie do riadka cenovej ponuky, keď vytvoríte cenovú ponuku z tejto príležitosti</span><span class="sxs-lookup"><span data-stu-id="ae914-131">This value is carried over to the quote line when you create a quote from this opportunity</span></span> |
| <span data-ttu-id="ae914-132">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="ae914-132">Customer Budget</span></span> | <span data-ttu-id="ae914-133">Karta Všeobecné</span><span class="sxs-lookup"><span data-stu-id="ae914-133">General tab</span></span> | <span data-ttu-id="ae914-134">Toto editovateľné pole meny možno použiť na sledovanie sumy, ktorú je zákazník ochotný zaplatiť za túto riadkovú položku.</span><span class="sxs-lookup"><span data-stu-id="ae914-134">This editable currency field can be used to track the amount that the customer is willing to spend for this line item.</span></span> | <span data-ttu-id="ae914-135">Táto hodnota sa prenesie do príslušného poľa pre riadok cenovej ponuky, keď vytvoríte cenovú ponuku z tejto príležitosti</span><span class="sxs-lookup"><span data-stu-id="ae914-135">This value is carried over to the corresponding field on the quote line when you create a quote from this opportunity</span></span> |
| <span data-ttu-id="ae914-136">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="ae914-136">Billing Method</span></span> | <span data-ttu-id="ae914-137">Karta Všeobecné</span><span class="sxs-lookup"><span data-stu-id="ae914-137">General tab</span></span> | <span data-ttu-id="ae914-138">Toto upraviteľné pole má nasledujúce hodnoty:</span><span class="sxs-lookup"><span data-stu-id="ae914-138">This editable field has the following values:</span></span></br><span data-ttu-id="ae914-139">- Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="ae914-139">- Time and Material</span></span></br><span data-ttu-id="ae914-140">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="ae914-140">- Fixed Price</span></span> | <span data-ttu-id="ae914-141">Táto hodnota sa prenesie do príslušného poľa pre riadok cenovej ponuky, keď vytvoríte cenovú ponuku z tejto príležitosti.</span><span class="sxs-lookup"><span data-stu-id="ae914-141">This value is carried over to the corresponding field on the quote line when you create a quote from this opportunity.</span></span> <span data-ttu-id="ae914-142">Po vytvorení riadka cenovej ponuky je pole uzamknuté a nemožno ho zmeniť.</span><span class="sxs-lookup"><span data-stu-id="ae914-142">After the quote line is created, the field is locked and can't be changed.</span></span> <span data-ttu-id="ae914-143">Priraďte túto hodnotu poľa čo najpresnejšie.</span><span class="sxs-lookup"><span data-stu-id="ae914-143">Assign this field value as accurately as possible.</span></span> <span data-ttu-id="ae914-144">Ak potrebujete zmeniť hodnotu tohto poľa v riadku cenovej ponuky, riadok cenovej ponuky vymažte a znova vytvorte.</span><span class="sxs-lookup"><span data-stu-id="ae914-144">If you need to change the value of this field on the quote line, delete and re-create the quote line.</span></span> |