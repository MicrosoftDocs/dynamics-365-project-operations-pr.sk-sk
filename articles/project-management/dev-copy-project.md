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
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045028"
---
# <a name="develop-project-templates-with-copy-project"></a>Vytváranie šablóny projektu pomocou funkcie kopírovania projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations podporuje schopnosť kopírovať projekt a vrátiť všetky priradenia späť k všeobecným zdrojom, ktoré zastupujú danú rolu. Zákazníci môžu pomocou tejto funkcie zostaviť základné šablóny projektu.

Keď vyberiete **Kopírovať projekt**, aktualizuje sa stav cieľového projektu. Použite **Dôvod stavu** na určenie, kedy je akcia kopírovania dokončená. Výberom možnosti **Kopírovať projekt** sa aktualizuje aj počiatočný dátum projektu na aktuálny počiatočný dátum, ak sa v entite cieľového projektu nezistí žiadny cieľový dátum.

## <a name="copy-project-custom-action"></a>Vlastná akcia kopírovania projektu 

### <a name="name"></a>Meno 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Vstupné parametre
Existujú tri vstupné parametre:

| Parameter          | Zadať   | Hodnoty                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** alebo **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Odkaz na entitu | Zdrojový projekt |
| Cieľ             | Odkaz na entitu | Cieľový projekt |


- **{"clearTeamsAndAssignments":true}**: Predvolené správanie pre Project for Web, ktoré odstráni všetky priradenia a členov tímu.
- **{"removeNamedResources": true}** Predvolené správanie pre Project Operations, ktoré vráti priradenia k všeobecným zdrojom.

Ďalšie predvolené hodnoty akcií nájdete v časti [Použitie akcií Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Zadajte polia, ktoré chcete kopírovať 
Po vyvolaní akcie bude funkcia **Kopírovať projekt** prehľadávať zobrazenie projektu **Kopírovať stĺpce projektu** na určenie, ktoré polia sa majú kopírovať pri kopírovaní projektu.


### <a name="example"></a>Príklad
Nasledujúci príklad ukazuje, ako vyvolať vlastnú akciu **CopyProject** pomocou súpravy parametrov **removeNamedResources**.
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
