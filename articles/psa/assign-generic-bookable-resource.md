---
title: Priradenie všeobecných rezervovateľných zdrojov k úlohe a projektovému tímu
description: Táto téma poskytuje informácie o rezervovaní všeobecných zdrojoch pre úlohy a projektové tímy.
author: JohnPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: a1e22337d3fd3e7ff4147a9547fd3c272f4185d3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009410"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="dbfcd-103">Priradenie všeobecných rezervovateľných zdrojov k úlohe a generovanie zdrojových požiadaviek</span><span class="sxs-lookup"><span data-stu-id="dbfcd-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dbfcd-104">Okrem rezervácie a priraďovania pomenovaných alebo skutočných zdrojov do vášho projektu môžete priradiť všeobecné zdroje k úlohám projektu.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="dbfcd-105">Tieto zdroje môžu slúžiť ako zástupné symboly pre pomenované zdroje, kým nie ste pripravení na zamestnanie vášho projektu s pomenovaním zdrojov.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="dbfcd-106">V Project Service Automation (PSA), otvorte stránku **Project** a na karte **Schedule**, zadajte názov pozície všeobecného prostriedku v bunke plánu **Resource**.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="dbfcd-107">Alebo kliknite na ikonu **Resource** v bunke k otvoreniu výberu zdrojov a potom zadajte názov všeobecného prostriedku, ktorý chcete vytvoriť.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![Vytvorenie a priradenie všeobecného člena tímu](media/RM-how-to-9.png)

<span data-ttu-id="dbfcd-109">Otvorí sa panel **Quick Create: Project Team Member**.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="dbfcd-110">Zadajte rolu a organizačnú jednotku člena tímu všeobecného zdroja a kliknite na tlačidlo **Save**.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![Rýchle vytvorenie všeobecného člena tímu](media/RM-how-to-10.png)

3. <span data-ttu-id="dbfcd-112">Po vytvorení nového člena tímu všeobecného zdroja, je priradený k úlohe.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="dbfcd-113">Môžete pokračovať v priraďovaní tohto všeobecného zdroja k iným úlohám v pláne úloh.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![Priradenie existujúceho všeobecného člena tímu k úlohám](media/RM-how-to-11.png)

4. <span data-ttu-id="dbfcd-115">Po priradení všeobecného zdroja môžete vygenerovať zdrojovú požiadavku a naplniť ju priamo rezerváciou alebo odoslaním zdrojovej požiadavky správcovi prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![Generovanie požiadavky na všeobecného člena tímu](media/RM-how-to-12.png)

<span data-ttu-id="dbfcd-117">Na mriežke člena tímu, okrem toho, že je možné použiť výber zdrojov, ako je uvedené vyššie, môžete pridať všeobecné zdroje priamo.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="dbfcd-118">Prostriedky sa pridávajú so zdrojovou požiadavkou, ktorá je založená na start/end dátumoch a metóde pridelenia zadanej v paneli **Quick Create: Project Team Member**.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="dbfcd-119">Môžete vidieť rozdiel, ak pridáte všeobecného člena tímu priamo a potom priradíte viac úloh na všeobecný zdroj, ako majú požadovaných hodín na pokrytie.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="dbfcd-120">Kliknite na **Generate Requirement** na regeneráciu požiadavky na vyváženie požadovaných hodín proti priradeniam.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="dbfcd-121">Môžete tiež kliknúť na **Resource requirement** odkaz v tímovej mriežke na otvorenie požiadavky a pridanie zručnosti, preferované zdroje, atď.</span><span class="sxs-lookup"><span data-stu-id="dbfcd-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![Požiadavka na zdroj](media/RM-how-to-13.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]