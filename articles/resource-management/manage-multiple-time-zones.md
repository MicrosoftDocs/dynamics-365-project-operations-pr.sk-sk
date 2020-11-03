---
title: Správa časových pásiem
description: Po vytvorení projektu je jeho časové pásmo založené na časovom pásme definovanom v použitej šablóne pracovnej doby.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084302"
---
# <a name="manage-time-zones"></a><span data-ttu-id="797ea-103">Správa časových pásiem</span><span class="sxs-lookup"><span data-stu-id="797ea-103">Manage time zones</span></span>

<span data-ttu-id="797ea-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="797ea-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="797ea-105">Projekty</span><span class="sxs-lookup"><span data-stu-id="797ea-105">Projects</span></span>

<span data-ttu-id="797ea-106">Po vytvorení projektu je časové pásmo založené na časovom pásme definovanom v použitej šablóne pracovnej doby.</span><span class="sxs-lookup"><span data-stu-id="797ea-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="797ea-107">Vo formulári **Projekt** sú dátumy vždy relatívne k časovému pásmu používateľa, ktorý je prihlásený na každej karte, s výnimkou karty **Úloha**. Pri zobrazení štruktúry rozdelenia práce sa dátumy vždy zobrazia v časovom pásme projektu.</span><span class="sxs-lookup"><span data-stu-id="797ea-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="797ea-108">Úlohy</span><span class="sxs-lookup"><span data-stu-id="797ea-108">Tasks</span></span>

<span data-ttu-id="797ea-109">Po vytvorení úlohy sa začiatočný čas, konečný čas a hodiny/deň riadia pracovnými hodinami projektu.</span><span class="sxs-lookup"><span data-stu-id="797ea-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="797ea-110">Napríklad, ak je úloha vytvorená s projektom, ktorého časové pásmo je -8 PST a má nasledujúcu pracovnú dobu: pondelok až piatok od 9:00 do 17:00, každá úloha vytvorená bez priradenia bude rešpektovať čas začiatku a konečný čas kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="797ea-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="797ea-111">Správa zdrojov s časovými pásmami</span><span class="sxs-lookup"><span data-stu-id="797ea-111">Manage resources with time zones</span></span>

<span data-ttu-id="797ea-112">Pre presné a predvídateľné výsledky pri používaní možnosti **Predĺžiť rezerváciu** musia byť splnené dva kľúčové predpoklady:</span><span class="sxs-lookup"><span data-stu-id="797ea-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="797ea-113">Používateľ musí nakonfigurovať časové pásmo svojho zariadenia tak, aby zodpovedalo časovému pásmu definovanému v časti **Nastavenia prispôsobení** v systéme.</span><span class="sxs-lookup"><span data-stu-id="797ea-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Nastavenia časového pásma v systéme Windows 10](media/reconcile-assignments-03.png)

  ![Nastavenia časového pásma v nastaveniach prispôsobenia](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="797ea-116">Rezervovateľný zdroj musí mať najmenej jednu minútu pracovného času, ktorá sa prekrýva s obrysmi, ktoré sa používajú na definovanie požadovaného rozšírenia.</span><span class="sxs-lookup"><span data-stu-id="797ea-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="797ea-117">Napríklad, nasledujúce zdroje s pracovnou dobou, ktorá spadá od 9:00 do 19:00.</span><span class="sxs-lookup"><span data-stu-id="797ea-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Porovnanie obrysov zdrojov](media/reconcile-assignments-05.png)

<span data-ttu-id="797ea-119">Nasledujúca tabuľka zobrazuje:</span><span class="sxs-lookup"><span data-stu-id="797ea-119">The following table shows:</span></span>

- <span data-ttu-id="797ea-120">Šablóna kalendára projektu</span><span class="sxs-lookup"><span data-stu-id="797ea-120">A project calendar template</span></span>
- <span data-ttu-id="797ea-121">Zdroj A: Tento zdroj má rovnaký kalendár a je v rovnakom časovom pásme ako projekt.</span><span class="sxs-lookup"><span data-stu-id="797ea-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="797ea-122">Čas začiatku rezervácie bude 9.00.</span><span class="sxs-lookup"><span data-stu-id="797ea-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="797ea-123">Zdroj B: Tento zdroj sa nachádza v inom časovom pásme ako projekt a začína sa o 7:00 v danom časovom pásme.</span><span class="sxs-lookup"><span data-stu-id="797ea-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="797ea-124">Rezervácie sa však začnú o 9.00, pretože ide o najskorší čas začiatku obrysu priradenia.</span><span class="sxs-lookup"><span data-stu-id="797ea-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="797ea-125">Zdroje C a D: Zdroje sa nachádzajú v rôznych časových pásmach, ktoré sa navzájom líšia a líšia sa od projektu, a ich rezervácie sa začínajú najskôr v príslušných dostupných začiatočných časoch.</span><span class="sxs-lookup"><span data-stu-id="797ea-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="797ea-126">Entita</span><span class="sxs-lookup"><span data-stu-id="797ea-126">Entity</span></span>  |<span data-ttu-id="797ea-127">Kalendár</span><span class="sxs-lookup"><span data-stu-id="797ea-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="797ea-128">Šablóna kalendára projektu</span><span class="sxs-lookup"><span data-stu-id="797ea-128">Project calendar template</span></span>   | ![kalendár projektu](media/reconcile-assignments-06.png) |
|<span data-ttu-id="797ea-130">Zdroj A</span><span class="sxs-lookup"><span data-stu-id="797ea-130">Resource A</span></span>  | ![Kalendár zdroja A](media/reconcile-assignments-06.png) |
|<span data-ttu-id="797ea-132">Zdroj B</span><span class="sxs-lookup"><span data-stu-id="797ea-132">Resource B</span></span>  |  ![Kalendár zdroja B](media/reconcile-assignments-07.png) |
|<span data-ttu-id="797ea-134">Zdroj C</span><span class="sxs-lookup"><span data-stu-id="797ea-134">Resource C</span></span>  |  ![Kalendár zdroja C](media/reconcile-assignments-08.png) |
|<span data-ttu-id="797ea-136">Zdroj D</span><span class="sxs-lookup"><span data-stu-id="797ea-136">Resource D</span></span>  | ![Kalendár zdroja D](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="797ea-138">Keď prejdete na zobrazenie **Vyrovnanie** zobrazia sa priradenia zdrojov a súvisiace nedostatky rezervácií.</span><span class="sxs-lookup"><span data-stu-id="797ea-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Zobrazenie odsúhlasenia pred predĺžením](media/reconcile-assignments-10.png)

<span data-ttu-id="797ea-140">Po použití funkcie rozšíreného rezervovania pre každý zdroj sa rezervácie úspešne rozšíria na každý zdroj, pretože pracovná doba každého zdroja sa prekrýva s obrysmi nedostatku.</span><span class="sxs-lookup"><span data-stu-id="797ea-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Zobrazenie odsúhlasenia po rozšírení rezervácie](media/reconcile-assignments-11.png) 

<span data-ttu-id="797ea-142">Upozorňujeme, že bližší pohľad na podrobnosti rezervácií ukazuje rozdiely v začiatočnom čase rezervácií.</span><span class="sxs-lookup"><span data-stu-id="797ea-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="797ea-143">Rezervácie sa začnú najskôr ako začiatočný čas obrysu priradenia a najskôr ako dostupný začiatočný čas zdroja.</span><span class="sxs-lookup"><span data-stu-id="797ea-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Nové rezervácie zdrojov na tabuli plánovania](media/reconcile-assignments-12.png)
