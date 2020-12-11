---
title: Projektové šablóny
description: Táto téma poskytuje informácie o používaní šablón projektov na rýchle nastavenie projektu.
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
ms.openlocfilehash: 4fd618e15524c5cef5b6da9b282f449e3dfb7973
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123052"
---
# <a name="project-templates"></a><span data-ttu-id="fe094-103">Projektové šablóny</span><span class="sxs-lookup"><span data-stu-id="fe094-103">Project templates</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="fe094-104">Šablóna projektu je preddefinovaný rámec, ktorý vám pomôže rýchlo a ľahko spustiť projekt.</span><span class="sxs-lookup"><span data-stu-id="fe094-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="fe094-105">Preddefinované šablóny môžete použiť na vytvorenie nového projektu jediným kliknutím.</span><span class="sxs-lookup"><span data-stu-id="fe094-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="fe094-106">Čo sa týka projektov, musíte definovať predpoklady pre šablóny projektu.</span><span class="sxs-lookup"><span data-stu-id="fe094-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="fe094-107">Musíte definovať kalendár projektu pre každú šablónu projektu a roly a cenníky musia byť preddefinované v organizácii tak, aby súčasti šablóny mali užitočné údaje.</span><span class="sxs-lookup"><span data-stu-id="fe094-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="fe094-108">Šablóna projektu pozostáva z troch súčastí: plánu, odhadov projektu a členov projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="fe094-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="fe094-109">Plánovanie</span><span class="sxs-lookup"><span data-stu-id="fe094-109">Schedule</span></span>

<span data-ttu-id="fe094-110">Plán v šablóne projektu má rovnaký súbor prvkov ako plán v projekte.</span><span class="sxs-lookup"><span data-stu-id="fe094-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="fe094-111">Môžete si vytvoriť hierarchiu úloh, priradiť role k úlohám, zadefinovať atribúty plánov, a nastaviť závislosti.</span><span class="sxs-lookup"><span data-stu-id="fe094-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="fe094-112">Plán v šablóne projektu tiež podporuje režimy úloh pre každú úlohu.</span><span class="sxs-lookup"><span data-stu-id="fe094-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="fe094-113">Preto podporuje plánovací engine.</span><span class="sxs-lookup"><span data-stu-id="fe094-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="fe094-114">Musíte priradiť projektový kalendár k projektu.</span><span class="sxs-lookup"><span data-stu-id="fe094-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="fe094-115">Pri vytváraní pracovného plánu neexistuje žiadny rozdiel medzi šablónou projektu a projektom.</span><span class="sxs-lookup"><span data-stu-id="fe094-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="fe094-116">Odhady projektu</span><span class="sxs-lookup"><span data-stu-id="fe094-116">Project estimates</span></span>

<span data-ttu-id="fe094-117">Odhady projektu v šablóne projektu fungujú rovnakým spôsobom ako odhady projektov v projekte.</span><span class="sxs-lookup"><span data-stu-id="fe094-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="fe094-118">Však náklady a predajné ceny sú stiahnuté z predvolených nákladov a predajných cenníkov , ktoré sú definované v parametroch.</span><span class="sxs-lookup"><span data-stu-id="fe094-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="fe094-119">Vytvorenie projektu zo šablóny</span><span class="sxs-lookup"><span data-stu-id="fe094-119">Creating a project from a template</span></span>
 
<span data-ttu-id="fe094-120">Existuje niekoľko spôsobov, ako vytvoriť projekt zo šablóny projektu:</span><span class="sxs-lookup"><span data-stu-id="fe094-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="fe094-121">Pri vytváraní projektu z cenovej ponuky si môžete vybrať šablónu projektu v dialógovom okne **rýchle vytvorenie projektu**.</span><span class="sxs-lookup"><span data-stu-id="fe094-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Zobrazí sa dialógové okno rýchle vytvorenie: projektu](media/project-11.png)

- <span data-ttu-id="fe094-123">Keď vytvoríte projekt výbraním **nový projekt**, stránka **projekt** sa zobrazí pred tým ako sa záznam uloží.</span><span class="sxs-lookup"><span data-stu-id="fe094-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="fe094-124">V poli **vybrať šablónu** vyberte jednu z preddefinovaných šablón projektu v organizácii.</span><span class="sxs-lookup"><span data-stu-id="fe094-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="fe094-125">Použite **vytvoriť projekt zo šablóny** na stránke **entity šablóny**.</span><span class="sxs-lookup"><span data-stu-id="fe094-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="fe094-126">Kopírovanie komponentov šablóny do projektu</span><span class="sxs-lookup"><span data-stu-id="fe094-126">Copying components of template to project</span></span>

<span data-ttu-id="fe094-127">Pri kopírovaní súčastí šablóny projektu do projektu, sa môže vyskytnúť niekoľko prepisov v závislosti od nastavení v projekte.</span><span class="sxs-lookup"><span data-stu-id="fe094-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="fe094-128">Kopírovanie plánu</span><span class="sxs-lookup"><span data-stu-id="fe094-128">Copying the schedule</span></span>

<span data-ttu-id="fe094-129">Ak má projekt rozdielny projektový kalendár ako šablóna, pri kopírovaní plánu zo šablóny projektu, použije sa v pláne úlohy pracovný čas z projektového kalendára.</span><span class="sxs-lookup"><span data-stu-id="fe094-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="fe094-130">Týmto spôsobom sa upraví plán tak, aby zodpovedal záložnému kalendáru projektu.</span><span class="sxs-lookup"><span data-stu-id="fe094-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="fe094-131">Podobne si začiatočný dátum projektu prevezme aj prvá úloha v pláne a plán ostatných hierarchií je aktualizovaný na základe trvania a závislostí, ktoré sú stanovené v šablóne.</span><span class="sxs-lookup"><span data-stu-id="fe094-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="fe094-132">Kopírovanie odhadov projektu</span><span class="sxs-lookup"><span data-stu-id="fe094-132">Copying project estimates</span></span> 

<span data-ttu-id="fe094-133">Pri kopírovaní naprieč riadkami odhadu projektu, sú cenníky aktualizované.</span><span class="sxs-lookup"><span data-stu-id="fe094-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="fe094-134">Pre cenník nákladov, sú tieto aktualizácie založené na vlastniacej jednotke projektu.</span><span class="sxs-lookup"><span data-stu-id="fe094-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="fe094-135">Predajné cenníky sú založené na zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="fe094-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="fe094-136">Pre projekty, ktoré sú priradené k predajným entitám, sú jednotkové ceny nákladov a predajov stanovené na základe týchto cenníkov.</span><span class="sxs-lookup"><span data-stu-id="fe094-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="fe094-137">Kopírovanie projektového tímu</span><span class="sxs-lookup"><span data-stu-id="fe094-137">Copying a project team</span></span>

<span data-ttu-id="fe094-138">Keď je projektový tím kopírovaný z projektovej šablóny, sú skopírované všeobecné zdroje spolu so zručnosťami a schopnosťami, ktoré sú definované v šablóne.</span><span class="sxs-lookup"><span data-stu-id="fe094-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="fe094-139">Priradenie všeobecných zdrojov sa zachová rovnaké ako bolo pri šablóne projektu.</span><span class="sxs-lookup"><span data-stu-id="fe094-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="fe094-140">Pomenované zdroje nie sú podporované v šablónach projektov.</span><span class="sxs-lookup"><span data-stu-id="fe094-140">Named resources aren't supported in project templates.</span></span>