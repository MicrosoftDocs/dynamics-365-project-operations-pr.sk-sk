---
title: Odhad tržieb a nákladov projektu v prípade, keď rezervovateľný zdroj v projekte zastáva rôzne roly
description: Táto téma obsahuje informácie o tom, ako je možné použiť cenové dimenzie na podporu určovania cien a kalkulácie nákladov pre zdroj, ktorý v projekte zastáva rôzne roly.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084416"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="db872-103">Odhad tržieb a nákladov projektu v prípade, keď rezervovateľný zdroj v projekte zastáva rôzne roly</span><span class="sxs-lookup"><span data-stu-id="db872-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="db872-104">Spoločnosti s dôrazom na projekty často potrebujú jeden zdroj, ktorý by v projekte zastával rôzne roly.</span><span class="sxs-lookup"><span data-stu-id="db872-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="db872-105">Cena a náklady každej z týchto rolí by mohli byť odlišné, čo znamená, že čas, ktorý bude mať rovnaký zdroj v rámci projektu, by mohol nadobudnúť odlišný finančný odhad v závislosti od vyúčtovania a sadzieb nákladov pre každú z rolí.</span><span class="sxs-lookup"><span data-stu-id="db872-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="db872-106">Project Service Automation umožňuje nastavenie hodnôt v zázname člena tímu pre pomenovaný zdroj a umožňuje rozličné prepisovanie jednotlivých úloh, ku ktorým je člen tímu priradený.</span><span class="sxs-lookup"><span data-stu-id="db872-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="db872-107">Nasledujúci príklad vysvetľuje, ako jednoduché prepísanie tejto hodnoty umožňuje, aby mal zdroj viac rolí v projekte s rôznymi nákladmi a fakturačnými sadzbami.</span><span class="sxs-lookup"><span data-stu-id="db872-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="db872-108">Vytvorenie úloh</span><span class="sxs-lookup"><span data-stu-id="db872-108">Create tasks</span></span>
<span data-ttu-id="db872-109">Vytvorte dve projektové úlohy po 40 hodín, úlohu A a úlohu B. Vyberte úlohu A ako predchodcu úlohy B.</span><span class="sxs-lookup"><span data-stu-id="db872-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="db872-110">Nastavte rolu a organizačnú jednotku všeobecného člena projektového tímu</span><span class="sxs-lookup"><span data-stu-id="db872-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="db872-111">Na stránke **Plán** vyberte riadok **Úloha** úlohu A.</span><span class="sxs-lookup"><span data-stu-id="db872-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="db872-112">V poli **Zdroje** vyberte položku **Vytvoriť** z rozbaľovacieho zoznamu.</span><span class="sxs-lookup"><span data-stu-id="db872-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="db872-113">Na stránke **Rýchle vytvorenie člena tímu** zadajte atribúty všeobecného člena tímu, ktorý môže vykonávať túto úlohu.</span><span class="sxs-lookup"><span data-stu-id="db872-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="db872-114">Vyberte príslušnú rolu a organizačnú jednotku a potom vyberte položku **Uložiť a zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="db872-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="db872-115">Vytvorí sa všeobecný člen tímu a priradí sa k tejto úlohe.</span><span class="sxs-lookup"><span data-stu-id="db872-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="db872-116">Zopakujte tieto kroky pre úlohu B a uistite sa, že rola a organizačná jednotka člena generického tímu vytvoreného pre úlohu B je iná ako úloha A.</span><span class="sxs-lookup"><span data-stu-id="db872-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="db872-117">Nastavte rolu a organizačnú jednotku projektovej úlohy</span><span class="sxs-lookup"><span data-stu-id="db872-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="db872-118">Po vytvorení úlohy A vyberte úlohu a potom vyberte položku **Upraviť úlohu**.</span><span class="sxs-lookup"><span data-stu-id="db872-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="db872-119">Na stránke **Podrobnosti úlohy** stránku nájdite polia **Rola** a **Organizačná jednotka** , pridajte hodnoty, ktoré sa požadujú od zdroja, ktorý by vykonal túto úlohu.</span><span class="sxs-lookup"><span data-stu-id="db872-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="db872-120">Ak dokončujete tieto scenáre pomocou ukážkových údajov z Project Service Automation, vyberte rolu **Vedúci konzultant** pre rolu a organizačnú jednotku **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="db872-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="db872-121">Vyberte úlohu B a potom vyberte **Upraviť úlohu**.</span><span class="sxs-lookup"><span data-stu-id="db872-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="db872-122">Na stránke **Podrobnosti úlohy** stránku nájdite polia **Rola** a **Organizačná jednotka** , pridajte hodnoty, ktoré sa požadujú od zdroja, ktorý by vykonal túto úlohu.</span><span class="sxs-lookup"><span data-stu-id="db872-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="db872-123">Uistite sa, že hodnoty v poliach **Rola** a **Organizačná jednotka** sú pre úlohu B iné ako pre úlohu A.</span><span class="sxs-lookup"><span data-stu-id="db872-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="db872-124">Ak dokončujete tieto scenáre pomocou ukážkových údajov z Project Service Automation, vyberte rolu **Sieťový technik** pre rolu a organizačnú jednotku **Fabrikam US**.</span><span class="sxs-lookup"><span data-stu-id="db872-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="db872-125">Uložte a zatvorte stránku **Podrobnosti úlohy**.</span><span class="sxs-lookup"><span data-stu-id="db872-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="db872-126">Správanie členov tímu a odhadov</span><span class="sxs-lookup"><span data-stu-id="db872-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="db872-127">Na stránke **Podrobnosti úlohy** v časti **Člen tímu** vyberte dvoch všeobecných členov tímu a potom vyberte položku **Generovať požiadavky**.</span><span class="sxs-lookup"><span data-stu-id="db872-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="db872-128">Tým sa vygenerujú požiadavky zdrojov.</span><span class="sxs-lookup"><span data-stu-id="db872-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="db872-129">Vyberte riadok člena tímu pre položku **Vedúci konzultant** a potom vyberte položku **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="db872-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="db872-130">Otvorí sa tabuľa s rozvrhom a rezervuje sa zdroj na základe tejto požiadavky.</span><span class="sxs-lookup"><span data-stu-id="db872-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="db872-131">Vyberte riadok člena tímu pre položku **Sieťový technik** a potom vyberte položku **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="db872-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="db872-132">Otvorí sa tabuľa s rozvrhom a rezervuje sa rovnaký zdroj na základe tejto požiadavky.</span><span class="sxs-lookup"><span data-stu-id="db872-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="db872-133">Mriežka Člen tímu</span><span class="sxs-lookup"><span data-stu-id="db872-133">Team Member grid</span></span> 
<span data-ttu-id="db872-134">Na mriežke **Člen tímu** si všimnite, že dva všeobecné záznamy členov tímu sú odstránené a jeden zdroj bol nahradený.</span><span class="sxs-lookup"><span data-stu-id="db872-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="db872-135">Pre tento zdroj existuje jedna množina hodnôt, ktorá ukazuje predvolenú množinu hodnôt pre polia **Rola** a **Organizačná jednotka**.</span><span class="sxs-lookup"><span data-stu-id="db872-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="db872-136">Keď rozbalíte riadok záznamu daného člena tímu, uvidíte v zázname člena tímu odlišné priradenia pre obe tieto úlohy.</span><span class="sxs-lookup"><span data-stu-id="db872-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="db872-137">Každý riadok priradenia má hodnoty špecifické pre položky **Rola** a **Organizačná jednotka**.</span><span class="sxs-lookup"><span data-stu-id="db872-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="db872-138">Mriežka Odhady</span><span class="sxs-lookup"><span data-stu-id="db872-138">Estimates grid</span></span> 
<span data-ttu-id="db872-139">Keď prejdete na mriežku **Odhady** , všimnete si, že obidve priradenia toho istého zdroja majú rozdielnu cenu.</span><span class="sxs-lookup"><span data-stu-id="db872-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="db872-140">Cena za priradenie zdroja v úlohe A sa stanoví pomocou hodnoty atribútu **Rola** položky **Vedúci konzultant**.</span><span class="sxs-lookup"><span data-stu-id="db872-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="db872-141">Cena za priradenie rovnakého zdroja v úlohe B sa stanoví pomocou hodnoty atribútu **Rola** položky **Sieťový technik**.</span><span class="sxs-lookup"><span data-stu-id="db872-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





