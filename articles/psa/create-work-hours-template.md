---
title: Vytvorí šablónu pracovných hodín
description: Ako na vytvorenie šablóny pracovných hodín v Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: c34634817fc8e4c993261024a8b19d45052bf5e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084374"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="e74f0-103">Vytvorenie šablóny pracovných hodín (Project Service)</span><span class="sxs-lookup"><span data-stu-id="e74f0-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e74f0-104">Pred vytvorením projektové plány, musíte vytvoriť kalendár, ktorý určuje počet pracovných hodín prispôsobený denne v harmonograme a odstávkach podnikania.</span><span class="sxs-lookup"><span data-stu-id="e74f0-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="e74f0-105">Vykonáte to pomocou šablóny hodín, ktorá obsahuje podrobnosti o pracovných hodín za deň, dni voľna a žiadne ďalšie zatvorenia prevádzok.</span><span class="sxs-lookup"><span data-stu-id="e74f0-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="e74f0-106">Pri vytváraní projektu, priradíte pracovnú šablónu na kalendár, ktorý sa použije pri plánovaní tohto projektu.</span><span class="sxs-lookup"><span data-stu-id="e74f0-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="e74f0-107">Šablóny pracovných hodín môžete vytvoriť dvoma spôsobmi:</span><span class="sxs-lookup"><span data-stu-id="e74f0-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="e74f0-108">Vytvorenie šablóny pracovných hodín na základe kalendára zdroja.</span><span class="sxs-lookup"><span data-stu-id="e74f0-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="e74f0-109">Vytvorí novú šablónu pracovných hodín.</span><span class="sxs-lookup"><span data-stu-id="e74f0-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="e74f0-110">Vytvoriť šablónu pracovných hodín na základe kalendára prostriedku.</span><span class="sxs-lookup"><span data-stu-id="e74f0-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="e74f0-111">Prejdite na **Project Service > Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="e74f0-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="e74f0-112">Vyberte zdroj, na základe ktorého chcete vytvoriť pracovné hodiny.</span><span class="sxs-lookup"><span data-stu-id="e74f0-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="e74f0-113">Kliknite na tlačidlo **Uložiť kalendár ako** , zadajte názov pre šablónu pracovných hodín, a potom kliknite na tlačidlo **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e74f0-113">Click **Save Calendar As** , enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="e74f0-114">Keď dokončíte vykonávanie zmien, kliknite na položku **Uložiť a zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="e74f0-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="e74f0-115">Kliknite na tlačidlo **Uložiť** v pravom dolnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="e74f0-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="e74f0-116">Vytvorenie novej šablóny pracovných hodín.</span><span class="sxs-lookup"><span data-stu-id="e74f0-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="e74f0-117">Prejdite na **Project Service > Šablóny pracovných hodín**.</span><span class="sxs-lookup"><span data-stu-id="e74f0-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="e74f0-118">Kliknite na položku **Nový**.</span><span class="sxs-lookup"><span data-stu-id="e74f0-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="e74f0-119">Zadajte názov šablóny pracovných hodín.</span><span class="sxs-lookup"><span data-stu-id="e74f0-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="e74f0-120">Vyberte zdroj pracovných hodín, z ktorého sa vychádza, a potom kliknite na **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e74f0-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="e74f0-121">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="e74f0-121">See Also</span></span>  
 [<span data-ttu-id="e74f0-122">Nastavenie prostriedkov</span><span class="sxs-lookup"><span data-stu-id="e74f0-122">Set up resources</span></span>](../psa/set-up-resources.md)
