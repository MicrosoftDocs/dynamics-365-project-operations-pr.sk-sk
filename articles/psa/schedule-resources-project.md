---
title: Naplánujte zdroje pre projekt
description: Ako naplánovať zdroje pre projekt v Project Service
author: JohnPBurrows
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
ms.openlocfilehash: 1479bf920be897a6ee3498aada7a6c36692a01fc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132171"
---
# <a name="schedule-resources-for-a-project-project-service"></a><span data-ttu-id="ac094-103">Plánovanie zdrojov projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ac094-103">Schedule resources for a project (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="ac094-104">Môžete skontrolovať dostupnosť na získanie celkový prehľad o spôsobe využitia vašich zdrojov, alebo môžete filtrovať zobrazenie podľa zručností, tímu, umiestnenia a ďalších možností.</span><span class="sxs-lookup"><span data-stu-id="ac094-104">You can check resource availability to get an overall view of how booked your resources are, or you can filter the view by skills, team, location, and other options.</span></span>  
  
<span data-ttu-id="ac094-105">Tabuľa plánovania ukazuje zoznam zdrojov a ich dostupnosti.</span><span class="sxs-lookup"><span data-stu-id="ac094-105">The schedule board shows list of resources and their availability.</span></span> <span data-ttu-id="ac094-106">Vyberte režim zobrazenia zobraziť dostupnosť podľa **hodinami**, **deň**, **týždeň**, alebo **mesiac**.</span><span class="sxs-lookup"><span data-stu-id="ac094-106">Select a view mode to show availability by **Hours**, **Day**, **Week**, or **Month**.</span></span>  
  
<span data-ttu-id="ac094-107">Predtým, ako použijete tabulu plánovania, je dôležité ju nastaviť.</span><span class="sxs-lookup"><span data-stu-id="ac094-107">Before you use the schedule board, it’s important to set it up.</span></span> <span data-ttu-id="ac094-108">Ďalšie informácie si prečítajte v časti [Konfigurácia tabule plánovania (Field Service alebo Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span><span class="sxs-lookup"><span data-stu-id="ac094-108">For more information, see [Configure the schedule board (Field Service or Project Service Automation)](https://docs.microsoft.com/dynamics365/field-service/configure-schedule-board).</span></span>
  
<span data-ttu-id="ac094-109">Ak používate staršiu verziu, pre dostupnosť zdrojov pozrite [Zobraziť dostupnosť zdroja](../psa/view-resource-availability.md).</span><span class="sxs-lookup"><span data-stu-id="ac094-109">If you are using an older version, for resource availability, see [View resource availability](../psa/view-resource-availability.md).</span></span>  

> [!IMPORTANT]
>  <span data-ttu-id="ac094-110">Na použitie funkcie tabule plánovanie, geografického označovania a služieb určovania polohy si budete musieť zapnúť mapy.</span><span class="sxs-lookup"><span data-stu-id="ac094-110">To use the schedule board booking functionality, geocoding, and location services, you need to turn on maps.</span></span>  
> 
> 1. <span data-ttu-id="ac094-111">V hlavnej ponuke kliknite na tlačidlo **Plánovanie zdrojov** > **Správa**.</span><span class="sxs-lookup"><span data-stu-id="ac094-111">On the main menu, select **Resource Scheduling** > **Administration**.</span></span>  
> 2. <span data-ttu-id="ac094-112">Kliknite na **Parametre plánovania**.</span><span class="sxs-lookup"><span data-stu-id="ac094-112">Click **Scheduling parameters**.</span></span>  
> 3. <span data-ttu-id="ac094-113">Otvorte záznam a prejdite nadol do sekcie **Resource Scheduling Optimization**.</span><span class="sxs-lookup"><span data-stu-id="ac094-113">Open record and scroll down to the **Resource Scheduling Optimization** section.</span></span>  
> 4. <span data-ttu-id="ac094-114">V poli **Pripojiť k mapám** zvoľte možnosť **Áno**.</span><span class="sxs-lookup"><span data-stu-id="ac094-114">On the **Connect to Maps** field, choose **Yes**.</span></span>  
> 5. <span data-ttu-id="ac094-115">Odsúhlaste podmienky a uložte záznam.</span><span class="sxs-lookup"><span data-stu-id="ac094-115">Accept terms and save the record.</span></span>  
> 6. <span data-ttu-id="ac094-116">V hlavnej ponuke zvoľte možnosť **Project Service** > **Tabuľa plánovania**.</span><span class="sxs-lookup"><span data-stu-id="ac094-116">On the main menu, select **Project Service** > **Schedule board**.</span></span> <span data-ttu-id="ac094-117">Existuje niekoľko spôsobov, ako odtiaľto manuálne naplánovať rezerváciu požiadavky:</span><span class="sxs-lookup"><span data-stu-id="ac094-117">From here, there are several ways to manually schedule a booking requirement.</span></span> <span data-ttu-id="ac094-118">Vyberte spôsob, ktorý vám vyhovuje.</span><span class="sxs-lookup"><span data-stu-id="ac094-118">Choose the method that works for you.</span></span>
  
## <a name="find-available-resources"></a><span data-ttu-id="ac094-119">Vyhľadanie dostupných zdrojov</span><span class="sxs-lookup"><span data-stu-id="ac094-119">Find available resources</span></span>

1.  <span data-ttu-id="ac094-120">V zozname **Požiadavka rezervácie** kliknite pravým tlačidlom myši na neplánovanú rezervácia a vyberte jednu z nasledujúcich možností:</span><span class="sxs-lookup"><span data-stu-id="ac094-120">From the **Booking Requirement** list, right-click an unscheduled booking and choose one of the following:</span></span>  
  
- <span data-ttu-id="ac094-121">Vybrať **nájsť dostupnosť - súčasné zdroje** nájsť dostupné zdroje v zozname zdrojov na palube plán.</span><span class="sxs-lookup"><span data-stu-id="ac094-121">Choose **Find availability - Current Resources** to find an available resource from the list on the schedule board.</span></span>  
- <span data-ttu-id="ac094-122">Vybrať **nájsť dostupnosť - všetky zdroje** a nájdite dostupné zdroje spomedzi zdrojov v systéme.</span><span class="sxs-lookup"><span data-stu-id="ac094-122">Choose **Find availability - All Resources**, to find an available resource from resources in the system</span></span>  
   > [!NOTE]
   >  <span data-ttu-id="ac094-123">Ak tak urobíte, pri filtorch sa zobrazia možnosti pre zvolení požiadavky rezervácie.</span><span class="sxs-lookup"><span data-stu-id="ac094-123">When you do this, the filters will show options for the selected booking requirement.</span></span>  
  
2. <span data-ttu-id="ac094-124">Keď vidíte dostupnej zásuvky kliknite pravým tlačidlom myši na časový úsek na palube rozvrh a vyberte **Rezervovať tu**.</span><span class="sxs-lookup"><span data-stu-id="ac094-124">When you see an available slot, right-click the time slot on the schedule board and choose **Book Here**.</span></span> <span data-ttu-id="ac094-125">Alebo drag and drop rezervácia požiadavka dostupného časového úseku.</span><span class="sxs-lookup"><span data-stu-id="ac094-125">Or, drag and drop the booking requirement to the available time slot.</span></span>  
  

## <a name="book-a-resource-using-the-daily-view-and-find-whos-under-booked"></a><span data-ttu-id="ac094-126">Rezervujte si prostriedok pomocou denného zobrazenia a zistite, kedy je málo rezervovaný</span><span class="sxs-lookup"><span data-stu-id="ac094-126">Book a resource using the daily view and find who’s under-booked</span></span>
  
1.  <span data-ttu-id="ac094-127">Na tabule plánovania, kliknite na tlačidlo **Režim zobrazenia** a vyberte **Dni**.</span><span class="sxs-lookup"><span data-stu-id="ac094-127">On the schedule board, select **View Mode** and select **Days**.</span></span>  
  
    <span data-ttu-id="ac094-128">V zobrazení mriežky sa zobrazuje koľko hodín prostriedok je rezervované denne a ktoré dni je voľný.</span><span class="sxs-lookup"><span data-stu-id="ac094-128">This shows a grid view of how many hours a resource is booked per day and which days they are free.</span></span>  
  
2.  <span data-ttu-id="ac094-129">Kliknite na názov prostriedku, ktorý chcete rezervovať, a potom kliknite na **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="ac094-129">Click the name of the resource you want to book, and then select **Book**.</span></span>  
  
3.  <span data-ttu-id="ac094-130">V dialógovom okne **Rezervácie zdrojov (vytvorenie)** vyberte projekt, ktorému chcete rezervovať prostriedok spolu s rezervácia metóda a časmi začatia a ukončenia.</span><span class="sxs-lookup"><span data-stu-id="ac094-130">On the **Resource booking (create)** dialog box, choose the project that you want to book the resource for along with booking method and start and end times.</span></span>  
  
4.  <span data-ttu-id="ac094-131">Po skončení vyberte položku **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="ac094-131">When you’re done, select **Book**.</span></span>  
  
## <a name="view-to-the-schedule-board"></a><span data-ttu-id="ac094-132">Zobrazenie tabule plánovania</span><span class="sxs-lookup"><span data-stu-id="ac094-132">View to the schedule board</span></span>
  
1.  <span data-ttu-id="ac094-133">Vyberte si nenaplánovanú požiadavku rezervácie zo zoznamu v spodnej časti.</span><span class="sxs-lookup"><span data-stu-id="ac094-133">Select an unscheduled booking requirement from the list at the bottom.</span></span>  
  
2.  <span data-ttu-id="ac094-134">Presuňte požiadavky rezervácie na dostupné zdroje a čas na tabuli plánovania.</span><span class="sxs-lookup"><span data-stu-id="ac094-134">Drag the booking requirement to an available resource/time slot on the schedule board.</span></span>  
  
3.  <span data-ttu-id="ac094-135">Po skončení vyberte položku **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="ac094-135">When you're done, select **Book**.</span></span>  
  
### <a name="additional-resources"></a><span data-ttu-id="ac094-136">Ďalšie zdroje</span><span class="sxs-lookup"><span data-stu-id="ac094-136">Additional resources</span></span>  
 [<span data-ttu-id="ac094-137">Príručka správcu zdrojov</span><span class="sxs-lookup"><span data-stu-id="ac094-137">Resource manager guide</span></span>](../psa/resource-manager-guide.md)
