---
title: Projektové nastavenia
description: Táto téma poskytuje informácie o nastaveniach projektového manažmentu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123127"
---
# <a name="project-settings"></a><span data-ttu-id="1e8ea-103">Projektové nastavenia</span><span class="sxs-lookup"><span data-stu-id="1e8ea-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1e8ea-104">Na prístup k funkciám plánovania projektu použite nasledujúce nastavenia.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="1e8ea-105">Šablóna práce</span><span class="sxs-lookup"><span data-stu-id="1e8ea-105">Work template</span></span>

<span data-ttu-id="1e8ea-106">Na vytvorenie projektového plánu, musíte vytvoriť šablónu projektového kalendára, ktorá určuje počet pracovných hodín za deň a počas zatváracej doby.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="1e8ea-107">Ak chcete vytvoriť šablónu kalendára projektu, priradíte pracovnú šablónu s poľom **šablóna kalendára** projektu.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="1e8ea-108">Ak chcete vytvoriť pracovnú šablónu, postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="1e8ea-109">V PSA na ľavom navigačnom paneli, kliknite na **zdroje**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="1e8ea-110">Na stránke zoznamu **zdroje**, otvrote užívateľské záznamy a vyberte **zobraziť pracovný čas**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="1e8ea-111">Uistite sa, že povolíte kontextové okná na stránke prehľadávača.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="1e8ea-112">To vám umožní zobraziť pracovný čas nastavený pre zdroj.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="1e8ea-113">Na karte **mesačné zobrazenie** kliknite na položku **nastaviť**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="1e8ea-114">Zobrazí sa zoznam troch možností:</span><span class="sxs-lookup"><span data-stu-id="1e8ea-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="1e8ea-115">Nový týždenný plán</span><span class="sxs-lookup"><span data-stu-id="1e8ea-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="1e8ea-116">Pracovný plán na jeden deň</span><span class="sxs-lookup"><span data-stu-id="1e8ea-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="1e8ea-117">Voľno</span><span class="sxs-lookup"><span data-stu-id="1e8ea-117">Time Off</span></span>

> ![Možnosti nastavenia](media/project-13.png)

4. <span data-ttu-id="1e8ea-119">Vyberte položku **nový týždenný plán** a potom nastavte možnosti pre tento plán prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="1e8ea-120">Môžete nastaviť opakujúci sa týždenný plán, parametre pre denné hodiny, zatváraciu dobu, a ďalšie.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="1e8ea-121">Nastavte rozsah dátumov, vyberte **uložiť** a potom kliknite na **zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="1e8ea-122">Vráťte sa na ziznam **zdrojov** a vyberte zdroj, pre ktorý nastavíte pracovnú dobu.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="1e8ea-123">Ak chcete nastaviť pracovnú šablónu, vyberte položku **nastaviť kalendár ako**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="1e8ea-124">V dialógovom okne **pracovná šablóna** zadajte názov pracovnej šablóny a potom vyberte **použiť**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="1e8ea-125">Šablónu práce teraz môžete priradiť k šablóne kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="1e8ea-126">Zdrojové roly</span><span class="sxs-lookup"><span data-stu-id="1e8ea-126">Resource roles</span></span>

<span data-ttu-id="1e8ea-127">Termín *zdrojová rola* odkazuje na množinu zručností, kompetencií a certifikátov, ktoré musí daná osoba vykonať, aby na projekte vykonala konkrétnu množinu úloh.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="1e8ea-128">PSA vám umožňuje oceniť a fakturovať role zdroja založené na čase, ku ktorému je zdroj priradený.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="1e8ea-129">Každá organizácia musí nastaviť tieto roly pomocou ľavej navigácie v ponuke **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="1e8ea-130">Každá organizácia musí tieto roly nastaviť na stránke **kategórie aktívnych zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="1e8ea-131">Ak chcete otvoriť túto stránku, na ľavom navigačnom paneli vyberte **roly prostriedku**.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="1e8ea-132">Cenníky</span><span class="sxs-lookup"><span data-stu-id="1e8ea-132">Price lists</span></span>

<span data-ttu-id="1e8ea-133">Cenníky vám umožňujú vidieť náklady a predajné ceny zdrojov rolí, výdavkových kategórií, produktov a iných prvkov v organizácii.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="1e8ea-134">Pred tým ako nastavíte finančné odhady pre prácu, ktorá musí byť dodaná do projektu, mali by ste vytvoriť sprievodný cenník nákladov a predajných cien.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="1e8ea-135">V časti parametre by ste tiež mali nastaviť predvolené náklady a predajný cenník, ktorý sa vzťahuje na všetky projekty vytvorené v organizácii.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="1e8ea-136">Na stránke **aktívne parametre projektu**, sa uistite, že nastavíte predvolené náklady a predajné cenníky.</span><span class="sxs-lookup"><span data-stu-id="1e8ea-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
