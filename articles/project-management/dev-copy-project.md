---
title: Vytváranie šablóny projektu pomocou funkcie kopírovania projektu
description: Táto téma poskytuje informácie o tom, ako vytvoriť šablóny projektu pomocou vlastnej akcie kopírovania projektu.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949833"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="a6213-103">Vytváranie šablóny projektu pomocou funkcie kopírovania projektu</span><span class="sxs-lookup"><span data-stu-id="a6213-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="a6213-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="a6213-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a6213-105">Dynamics 365 Project Operations podporuje schopnosť kopírovať projekt a vrátiť všetky priradenia späť k všeobecným zdrojom, ktoré zastupujú danú rolu.</span><span class="sxs-lookup"><span data-stu-id="a6213-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="a6213-106">Zákazníci môžu pomocou tejto funkcie zostaviť základné šablóny projektu.</span><span class="sxs-lookup"><span data-stu-id="a6213-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="a6213-107">Keď vyberiete **Kopírovať projekt**, aktualizuje sa stav cieľového projektu.</span><span class="sxs-lookup"><span data-stu-id="a6213-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="a6213-108">Použite **Dôvod stavu** na určenie, kedy je akcia kopírovania dokončená.</span><span class="sxs-lookup"><span data-stu-id="a6213-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="a6213-109">Výberom možnosti **Kopírovať projekt** sa aktualizuje aj počiatočný dátum projektu na aktuálny počiatočný dátum, ak sa v entite cieľového projektu nezistí žiadny cieľový dátum.</span><span class="sxs-lookup"><span data-stu-id="a6213-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="a6213-110">Vlastná akcia kopírovania projektu</span><span class="sxs-lookup"><span data-stu-id="a6213-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="a6213-111">Meno</span><span class="sxs-lookup"><span data-stu-id="a6213-111">Name</span></span> 

<span data-ttu-id="a6213-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="a6213-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="a6213-113">Vstupné parametre</span><span class="sxs-lookup"><span data-stu-id="a6213-113">Input parameters</span></span>
<span data-ttu-id="a6213-114">Existujú tri vstupné parametre:</span><span class="sxs-lookup"><span data-stu-id="a6213-114">There are three input parameters:</span></span>

| <span data-ttu-id="a6213-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a6213-115">Parameter</span></span>          | <span data-ttu-id="a6213-116">Zadať</span><span class="sxs-lookup"><span data-stu-id="a6213-116">Type</span></span>   | <span data-ttu-id="a6213-117">Hodnoty</span><span class="sxs-lookup"><span data-stu-id="a6213-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="a6213-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="a6213-118">ProjectCopyOption</span></span>  | <span data-ttu-id="a6213-119">String</span><span class="sxs-lookup"><span data-stu-id="a6213-119">String</span></span> | <span data-ttu-id="a6213-120">**{"removeNamedResources":true}** alebo **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="a6213-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="a6213-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="a6213-121">SourceProject</span></span>      | <span data-ttu-id="a6213-122">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="a6213-122">Entity Reference</span></span> | <span data-ttu-id="a6213-123">Zdrojový projekt</span><span class="sxs-lookup"><span data-stu-id="a6213-123">Source Project</span></span> |
| <span data-ttu-id="a6213-124">Cieľ</span><span class="sxs-lookup"><span data-stu-id="a6213-124">Target</span></span>             | <span data-ttu-id="a6213-125">Odkaz na entitu</span><span class="sxs-lookup"><span data-stu-id="a6213-125">Entity Reference</span></span> | <span data-ttu-id="a6213-126">Cieľový projekt</span><span class="sxs-lookup"><span data-stu-id="a6213-126">Target Project</span></span> |


- <span data-ttu-id="a6213-127">**{"clearTeamsAndAssignments":true}**: Predvolené správanie pre Project for Web, ktoré odstráni všetky priradenia a členov tímu.</span><span class="sxs-lookup"><span data-stu-id="a6213-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="a6213-128">**{"removeNamedResources": true}** Predvolené správanie pre Project Operations, ktoré vráti priradenia k všeobecným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="a6213-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="a6213-129">Ďalšie predvolené hodnoty akcií nájdete v časti [Použitie akcií Web API](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="a6213-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="a6213-130">Zadajte polia, ktoré chcete kopírovať</span><span class="sxs-lookup"><span data-stu-id="a6213-130">Specify fields to copy</span></span> 
<span data-ttu-id="a6213-131">Po vyvolaní akcie bude funkcia **Kopírovať projekt** prehľadávať zobrazenie projektu **Kopírovať stĺpce projektu** na určenie, ktoré polia sa majú kopírovať pri kopírovaní projektu.</span><span class="sxs-lookup"><span data-stu-id="a6213-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="a6213-132">Príklad</span><span class="sxs-lookup"><span data-stu-id="a6213-132">Example</span></span>
<span data-ttu-id="a6213-133">Nasledujúci príklad ukazuje, ako vyvolať vlastnú akciu **CopyProject** pomocou súpravy parametrov **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="a6213-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]