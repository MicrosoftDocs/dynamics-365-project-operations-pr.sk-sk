---
title: Definovanie kalendárov projektu
description: Táto téma poskytuje informácie o používaní kalendára projektu na sledovanie harmonogramu projektu.
author: ruhercul
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 442a901af8754fa0335bbf43f4ac8c73b11f9499
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131677"
---
# <a name="define-project-calendars"></a><span data-ttu-id="d490c-103">Definovanie kalendárov projektu</span><span class="sxs-lookup"><span data-stu-id="d490c-103">Define project calendars</span></span>

<span data-ttu-id="d490c-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="d490c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d490c-105">Na vytvorenie projektového plánu, musíte vytvoriť šablónu projektového kalendára, ktorá určuje počet pracovných hodín za deň a počas zatváracej doby.</span><span class="sxs-lookup"><span data-stu-id="d490c-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="d490c-106">Ak chcete vytvoriť šablónu kalendára projektu, priradíte pracovnú šablónu s poľom **šablóna kalendára** projektu.</span><span class="sxs-lookup"><span data-stu-id="d490c-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="d490c-107">Ak chcete vytvoriť pracovnú šablónu, postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="d490c-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="d490c-108">Na ľavej navigačnej table vyberte **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="d490c-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="d490c-109">Na stránke zoznamu **zdroje**, otvrote užívateľské záznamy a vyberte **zobraziť pracovný čas**.</span><span class="sxs-lookup"><span data-stu-id="d490c-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="d490c-110">Uistite sa, že povolíte kontextové okná na stránke prehľadávača.</span><span class="sxs-lookup"><span data-stu-id="d490c-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="d490c-111">To vám umožní zobraziť pracovný čas nastavený pre zdroj.</span><span class="sxs-lookup"><span data-stu-id="d490c-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="d490c-112">Na karte **Mesačné zobrazenie** vyberte **Nastaviť**.</span><span class="sxs-lookup"><span data-stu-id="d490c-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="d490c-113">Zobrazí sa zoznam troch možností:</span><span class="sxs-lookup"><span data-stu-id="d490c-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="d490c-114">Nový týždenný plán</span><span class="sxs-lookup"><span data-stu-id="d490c-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="d490c-115">Pracovný plán na jeden deň</span><span class="sxs-lookup"><span data-stu-id="d490c-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="d490c-116">Voľno</span><span class="sxs-lookup"><span data-stu-id="d490c-116">Time Off</span></span>

4. <span data-ttu-id="d490c-117">Vyberte položku **nový týždenný plán** a potom nastavte možnosti pre tento plán prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="d490c-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="d490c-118">Môžete nastaviť opakujúci sa týždenný plán, parametre pre denné hodiny, zatváraciu dobu, a ďalšie.</span><span class="sxs-lookup"><span data-stu-id="d490c-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="d490c-119">Nastavte rozsah dátumov, vyberte **Uložiť** a potom vyberte **Zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="d490c-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="d490c-120">Vráťte sa na ziznam **zdrojov** a vyberte zdroj, pre ktorý nastavíte pracovnú dobu.</span><span class="sxs-lookup"><span data-stu-id="d490c-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="d490c-121">Ak chcete nastaviť pracovnú šablónu, vyberte položku **nastaviť kalendár ako**.</span><span class="sxs-lookup"><span data-stu-id="d490c-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="d490c-122">V dialógovom okne **pracovná šablóna** zadajte názov pracovnej šablóny a potom vyberte **použiť**.</span><span class="sxs-lookup"><span data-stu-id="d490c-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="d490c-123">Šablónu práce teraz môžete priradiť k šablóne kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="d490c-123">You can now associate the work template with a project calendar template.</span></span>
