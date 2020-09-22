---
title: Vytvoriť šablónu projektu
description: Ako vytvoriť projektovú šablónu v Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: ba15d6d5-a43b-456a-9488-db6e92023fa1
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 50e12d65d5ed957565485413490b8d9f0e2f47ab
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755545"
---
# <a name="create-a-project-template-project-service"></a><span data-ttu-id="c6360-103">Vytvorenie projektovej šablóny (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c6360-103">Create a project template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c6360-104">Šablóny projektu šetria čas v prípade, ak má vaša spoločnosť pravidelné ponuky alebo podobné typy projektov.</span><span class="sxs-lookup"><span data-stu-id="c6360-104">Project templates save you time if your company regularly bids on similar types of projects.</span></span> <span data-ttu-id="c6360-105">Poskytujú štandardné nastavenie rolí a odhadovaných hodín pre daný typ projektu.</span><span class="sxs-lookup"><span data-stu-id="c6360-105">They provide a standard set of roles and estimated hours for a type of project.</span></span> <span data-ttu-id="c6360-106">Správcovia účtu a projektoví manažéri môžu vytvárať projekty na základe projektovej šablóny, prípadne si môžu šablónu skopírovať a vytvoriť si tak vlastnú.</span><span class="sxs-lookup"><span data-stu-id="c6360-106">Account managers and project managers can create projects based on a project template, or they can copy the template and make one of their own.</span></span>  
  
## <a name="components-of-project-template"></a><span data-ttu-id="c6360-107">Súčasti šablóny projektu</span><span class="sxs-lookup"><span data-stu-id="c6360-107">Components of project template</span></span>
 <span data-ttu-id="c6360-108">Šablóna projektu pozostáva z troch zložiek:</span><span class="sxs-lookup"><span data-stu-id="c6360-108">A project template consists of three components:</span></span>  
  
- <span data-ttu-id="c6360-109">**Štruktúra rozdelenia práce**: Štruktúra rozdelenia práce je šablóna projektu s rovnakými prvkami, ktoré sú aj v projekte.</span><span class="sxs-lookup"><span data-stu-id="c6360-109">**Work breakdown structure**: A work breakdown structure in a project template has the same set of elements as in the project.</span></span> <span data-ttu-id="c6360-110">Môžete si vytvoriť hierarchiu úloh, priradiť role k úlohám, zadefinovať atribúty plánov, nastaviť závislosti a pozrieť si všetky údaje v Gantt.</span><span class="sxs-lookup"><span data-stu-id="c6360-110">You can create a task hierarchy, associate roles to task, define schedule attributes, set dependencies and view all the data in the Gantt.</span></span> <span data-ttu-id="c6360-111">Štruktúra rozdelenia práce predstavuje šablónu projektu, ktorá podporuje aj režime úloh pre jednotlivé úlohy.</span><span class="sxs-lookup"><span data-stu-id="c6360-111">The work breakdown structure in project templates also support task modes for each task.</span></span> <span data-ttu-id="c6360-112">Pri vytváraní pracovného harmonogramu neexistuje žiadny rozdiel medzi šablónou projektu a projektom.</span><span class="sxs-lookup"><span data-stu-id="c6360-112">There is no difference between a project template and a project when creating work schedule.</span></span>  
  
- <span data-ttu-id="c6360-113">**Projektové odhady**: projektové odhady v šablónach fungujú rovnako, ako v projektoch. Jediným rozdielom je cenník pre predvolené určenie nákladov a predajných cien, ktorý predstavuje predvolené cenníky nákladov a predajných cien zadefinovaných v parametre [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="c6360-113">**Project estimates**: Project estimates in templates work the same way as they do in projects, except the price lists for defaulting the cost and sales prices are always the default cost and sales price lists defined in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] parameters.</span></span> <span data-ttu-id="c6360-114">Zvyšok funkcií je rovnaký ako v projekte.</span><span class="sxs-lookup"><span data-stu-id="c6360-114">The rest of the functionality is the same as in a project.</span></span>  
  
- <span data-ttu-id="c6360-115">**Vytvorenie tímu projektu**: Pri vytváraní projektového tímu šablóny projektu si v nej nemôžete zarezervovať pomenovaný zdroj.</span><span class="sxs-lookup"><span data-stu-id="c6360-115">**Project team formation**: When forming a project team for a project template, you can’t book a named resource in a template.</span></span> <span data-ttu-id="c6360-116">V štruktúre rozdelenia prác môžete použiť funkciu **Generovať projektový tím**, čím vytvoríte súbor všeobecných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="c6360-116">You can use **Generate Project Team** in the work breakdown structure to generate a set of generic resources.</span></span> <span data-ttu-id="c6360-117">Môžete tiež zadať požadovaných schopnosti a zručností všeobecných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="c6360-117">You can also specify required skills and proficiencies for generic resources.</span></span> <span data-ttu-id="c6360-118">Všeobecný zdroj nemôžete nahradiť rezervovateľným zdrojom v šablónach projektu.</span><span class="sxs-lookup"><span data-stu-id="c6360-118">You can’t substitute a generic resource with a bookable resource in project templates.</span></span>  
  
## <a name="create-a-project-from-a-template"></a><span data-ttu-id="c6360-119">Vytvorenie projektu zo šablóny</span><span class="sxs-lookup"><span data-stu-id="c6360-119">Create a project from a template</span></span>  
 <span data-ttu-id="c6360-120">Projekt zo šablóny môžete vytvoriť nasledovne:</span><span class="sxs-lookup"><span data-stu-id="c6360-120">You can create a project from a template in these following ways:</span></span>  
  
-   <span data-ttu-id="c6360-121">Pri vytváraní projektu z cenovej ponuky si môžete vybrať šablónu projektu vo formulári rýchleho vytvárania projektu.</span><span class="sxs-lookup"><span data-stu-id="c6360-121">When creating a project from the quote, you can choose a project template in the project quick create form.</span></span>  
  
-   <span data-ttu-id="c6360-122">Pri vytváraní projektu kliknutím na možnosť **nový projekt** sa pred uložením záznamu zobrazí formulár projektu.</span><span class="sxs-lookup"><span data-stu-id="c6360-122">When creating a project by clicking **New Project**, the project form displays before you save the record.</span></span> <span data-ttu-id="c6360-123">Tu môžete kliknúť na pole **vybrať šablónu**, čím si vyberiete zo zoznamu preddefinovaných projektových šablón svojej organizácie.</span><span class="sxs-lookup"><span data-stu-id="c6360-123">From here, you can click **Pick a template** field to choose from the list of pre-defined project templates in your organization.</span></span>  
  
-   <span data-ttu-id="c6360-124">Kliknite na tlačidlo **Vytvoriť projekt pomocou šablóny** na stránke **Šablóna projektu**, čím vytvoríte projekt zo šablóny.</span><span class="sxs-lookup"><span data-stu-id="c6360-124">Click **Create project from a template** on the **Project Template** page to create a project from the template.</span></span>  
  
## <a name="copying-components-of-a-template-to-a-project"></a><span data-ttu-id="c6360-125">Kopírovanie komponentov šablóny do projektu</span><span class="sxs-lookup"><span data-stu-id="c6360-125">Copying components of a template to a project</span></span>  
 <span data-ttu-id="c6360-126">Pri kopírovaní súčasti šablóny do projektu, existuje niekoľko vecí, ktoré by ste mali vedieť.</span><span class="sxs-lookup"><span data-stu-id="c6360-126">When you copy components of a template into a project, there are a few things you should know about.</span></span>  
  
 <span data-ttu-id="c6360-127">**Kopírovanie štruktúry rozdelenia práce**: pri kopírovaní štruktúry rozdelenia prác zo šablóny projektu, ak má projekt iný kalendár, než má šablóna, pracovné hodiny kalendára projektu sa použijú na plánovanie úloh.</span><span class="sxs-lookup"><span data-stu-id="c6360-127">**Copying a work breakdown structure**: When you copy the work breakdown structure from a project template, if the project has a different project calendar than the template, the work hours from the project’s calendar will be applied to the schedule of tasks.</span></span> <span data-ttu-id="c6360-128">Týmto sa upraví plán záložného kalendára projektu.</span><span class="sxs-lookup"><span data-stu-id="c6360-128">This adjusts the schedule to the backing project calendar.</span></span> <span data-ttu-id="c6360-129">Podobne si začiatočný dátum prevezme aj prvá úloha na štruktúre rozdelenia práce. Ďalšie úlohy v pláne hierarchie sa teda budú aktualizovať na základe trvania a závislostí stanovených v štruktúre rozdelenia prác šablóny.</span><span class="sxs-lookup"><span data-stu-id="c6360-129">Similarly, the first task on the work breakdown structure takes the project’s start date, so the rest of the task hierarchy schedule is updated based on the duration and dependencies specified in the template’s work breakdown structure.</span></span>  
  
 <span data-ttu-id="c6360-130">**Kopírovanie odhadov projektu**: pri kopírovaní medziprojektových odhadov sa cenníky aktualizujú na základe vlastníctva jednotiek projektu pre cenník obstarávacej ceny a zákazníka pre cenník predajnej ceny.</span><span class="sxs-lookup"><span data-stu-id="c6360-130">**Copying project estimates**: When you copy across project estimate lines, price lists are updated based on the owning unit of the project for the cost price list and customer for the sales price list.</span></span> <span data-ttu-id="c6360-131">Jednotkové náklady a predajné ceny sa odvíjajú z cenníkov v projekte, ktoré sú priradené k predajnej entite.</span><span class="sxs-lookup"><span data-stu-id="c6360-131">The unit cost and sales prices are determined from these price lists on projects that are associated to a sales entity.</span></span>  
  
 <span data-ttu-id="c6360-132">**Kopírovanie projektového tímu**: Pri kopírovaní projektového tímu zo šablóny do projektu sa skopírujú všeobecné zdroje spolu so zručnosťami a schopnosťami stanovenými v šablóne.</span><span class="sxs-lookup"><span data-stu-id="c6360-132">**Copying a project team**: When you copy the project team from the template to a project, the generic resources are copied across, along with the skills and proficiencies defined in the template.</span></span> <span data-ttu-id="c6360-133">Priradenie všeobecných zdrojov sa zachová rovnaké ako pri šablóne projektu.</span><span class="sxs-lookup"><span data-stu-id="c6360-133">Generic resource assignments are also maintained as in the project template.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c6360-134">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="c6360-134">See Also</span></span>  
 [<span data-ttu-id="c6360-135">Príručka projektového manažéra</span><span class="sxs-lookup"><span data-stu-id="c6360-135">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
