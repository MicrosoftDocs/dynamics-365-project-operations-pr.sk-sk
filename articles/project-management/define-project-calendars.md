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
ms.openlocfilehash: e25b11b6b947627ca2ac88952e74aecccc346c89
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286987"
---
# <a name="define-project-calendars"></a><span data-ttu-id="fe0ce-103">Definovanie kalendárov projektu</span><span class="sxs-lookup"><span data-stu-id="fe0ce-103">Define project calendars</span></span>

<span data-ttu-id="fe0ce-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="fe0ce-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fe0ce-105">Na vytvorenie projektového plánu, musíte vytvoriť šablónu projektového kalendára, ktorá určuje počet pracovných hodín za deň a počas zatváracej doby.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="fe0ce-106">Ak chcete vytvoriť šablónu kalendára projektu, priradíte pracovnú šablónu s poľom **šablóna kalendára** projektu.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="fe0ce-107">Ak chcete vytvoriť pracovnú šablónu, postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="fe0ce-108">Na ľavej navigačnej table vyberte **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="fe0ce-109">Na stránke zoznamu **zdroje**, otvrote užívateľské záznamy a vyberte **zobraziť pracovný čas**.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="fe0ce-110">Uistite sa, že povolíte kontextové okná na stránke prehľadávača.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="fe0ce-111">To vám umožní zobraziť pracovný čas nastavený pre zdroj.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="fe0ce-112">Na karte **Mesačné zobrazenie** vyberte **Nastaviť**.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="fe0ce-113">Zobrazí sa zoznam troch možností:</span><span class="sxs-lookup"><span data-stu-id="fe0ce-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="fe0ce-114">Nový týždenný plán</span><span class="sxs-lookup"><span data-stu-id="fe0ce-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="fe0ce-115">Pracovný plán na jeden deň</span><span class="sxs-lookup"><span data-stu-id="fe0ce-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="fe0ce-116">Voľno</span><span class="sxs-lookup"><span data-stu-id="fe0ce-116">Time Off</span></span>

4. <span data-ttu-id="fe0ce-117">Vyberte položku **nový týždenný plán** a potom nastavte možnosti pre tento plán prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-117">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="fe0ce-118">Môžete nastaviť opakujúci sa týždenný plán, parametre pre denné hodiny, zatváraciu dobu, a ďalšie.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="fe0ce-119">Nastavte rozsah dátumov, vyberte **Uložiť** a potom vyberte **Zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-119">Set the date range, select **Save**, and then select **Close**.</span></span> 
6. <span data-ttu-id="fe0ce-120">Vráťte sa na ziznam **zdrojov** a vyberte zdroj, pre ktorý nastavíte pracovnú dobu.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="fe0ce-121">Ak chcete nastaviť pracovnú šablónu, vyberte položku **nastaviť kalendár ako**.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="fe0ce-122">V dialógovom okne **pracovná šablóna** zadajte názov pracovnej šablóny a potom vyberte **použiť**.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="fe0ce-123">Šablónu práce teraz môžete priradiť k šablóne kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="fe0ce-123">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]