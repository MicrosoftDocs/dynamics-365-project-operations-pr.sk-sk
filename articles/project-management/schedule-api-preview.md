---
title: Používanie rozhraní API na plánovanie na vykonávanie operácií s entitami plánovania
description: Táto téma poskytuje informácie a ukážky používania rozhraní API na plánovanie.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950823"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Používanie rozhraní API na plánovanie na vykonávanie operácií s entitami plánovania

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

> [!IMPORTANT] 
> Niektoré alebo všetky z funkcií uvádzaných v tejto téme sú k dispozícii ako súčasť vydania verzie Preview. Obsah a funkcie sa môžu zmeniť. 

## <a name="scheduling-entities"></a>Entity na plánovanie

Rozhrania API na plánovanie poskytujú možnosť vykonávať operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania**. Tieto entity sú spravované prostredníctvom modulu Plánovanie v Projekte pre web. Operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania** boli obmedzené v skorších vydaniach Dynamics 365 Project Operations.

Nasledujúca tabuľka poskytuje úplný zoznam **Entít na plánovanie**.

| Názov entity  | Logický názov entity |
| --- | --- |
| Project | msdyn_project |
| Projektová úloha  | msdyn_projecttask  |
| Závislosť projektovej úlohy  | msdyn_projecttaskdependency  |
| Priradenie zdroja | msdyn_resourceassignment |
| Projektový kontajner  | msdyn_projectbucket |
| Člen projektového tímu | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet je vzor jednotky práce, ktorý je možné použiť, keď sa v rámci transakcie musí spracovať niekoľko požiadaviek ovplyvňujúcich plán.

## <a name="schedule-apis"></a>Rozhrania API pre plánovanie

Nasleduje zoznam aktuálnych rozhraní API pre plánovanie.

- **msdyn_CreateProjectV1**: Toto rozhranie API možno použiť na vytvorenie projektu. Projekt a predvolený kontajner projektu sa vytvorí okamžite.
- **msdyn_CreateTeamMemberV1**: Toto rozhranie API možno použiť na vytvorenie člena projektového tímu. Záznam o členovi tímu sa vytvorí okamžite.
- **msdyn_CreateOperationSetV1**: Toto API možno použiť na naplánovanie niekoľkých požiadaviek, ktoré sa musia vykonať v rámci transakcie.
- **msdyn_PSSCreateV1**: Toto API možno použiť na vytvorenie entity. Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu vytvorenia.
- **msdyn_PSSUpdateV1**: Toto API možno použiť na aktualizáciu entity. Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu aktualizácie.
- **msdyn_PSSDeleteV1**: Toto API možno použiť na odstránenie entity. Entita môže byť ktorákoľvek z entít plánovania, ktoré podporujú operáciu odstránenia.
- **msdyn_ExecuteOperationSetV1**: Toto API sa používa na vykonávanie všetkých operácií v rámci danej množiny operácií.

## <a name="using-schedule-apis-with-operationset"></a>Používanie rozhraní API plánovania s množinou OperationSet

Pretože záznamy s **CreateProjectV1** a **CreateTeamMemberV1** sú vytvorené okamžite, tieto API nemôžu byť použité v **OperationSet** priamo. Môžete však použiť API na vytvorenie potrebných záznamov, vytvorenie **OperationSet** a potom použiť tieto vopred vytvorené záznamy v **OperationSet**.

## <a name="supported-operations"></a>Podporované operácie

| Entita na plánovanie | Vytvoriť | Aktualizácia | Delete | Dôležité aspekty |
| --- | --- | --- | --- | --- |
Projektová úloha | Áno | Áno | Áno | Nie je |
| Závislosť projektovej úlohy | Áno | Áno | | Záznamy o závislosti od projektových úloh sa neaktualizujú. Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam. |
| Priradenie zdroja | Áno | Áno | | Operácie s nasledujúcimi poľami nie sú podporované: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**. Záznamy o priradení zdrojov sa neaktualizujú. Namiesto toho je možné odstrániť starý záznam a vytvoriť nový záznam. |
| Projektový kontajner | Nie je k dispozícii | Nie je k dispozícii | Nie je k dispozícii | Predvolený kontajner sa vytvára pomocou API **CreateProjectV1**. |
| Člen projektového tímu | Áno | Áno | Áno | Na operáciu vytvorenia použite API **CreateTeamMemberV1**. |
| Project | Áno | Áno | Nie je k dispozícii | Operácie s nasledujúcimi poľami nie sú podporované: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**. |

Tieto rozhrania API je možné volať s objektmi entít, ktoré obsahujú vlastné polia.

Toto ID vlastnosti je voliteľné. Ak je uvedené, systém sa ho pokúsi použiť a v prípade, že ho nemožno použiť, vyvolá výnimku. Ak nie je uvedené, systém ho vygeneruje.

## <a name="restricted-fields"></a>Obmedzené polia

Nasledujúce tabuľky definujú polia, ktoré sú obmedzené v rámci možností **Vytvoriť** a **Upraviť**.

### <a name="project-task"></a>Projektová úloha

| **Logický názov**                       | **Môže vytvoriť** | **Môže upravovať**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | nie             | nie               |
| msdyn_actualcost_base                  | nie             | nie               |
| msdyn_actualend                        | nie             | nie               |
| msdyn_actualsales                      | nie             | nie               |
| msdyn_actualsales_base                 | nie             | nie               |
| msdyn_actualstart                      | nie             | nie               |
| msdyn_costatcompleteestimate           | nie             | nie               |
| msdyn_costatcompleteestimate_base      | nie             | nie               |
| msdyn_costconsumptionpercentage        | nie             | nie               |
| msdyn_effortcompleted                  | nie             | nie               |
| msdyn_effortestimateatcomplete         | nie             | nie               |
| msdyn_iscritical                       | nie             | nie               |
| msdyn_iscriticalname                   | nie             | nie               |
| msdyn_ismanual                         | nie             | nie               |
| msdyn_ismanualname                     | nie             | nie               |
| msdyn_ismilestone                      | nie             | nie               |
| msdyn_ismilestonename                  | nie             | nie               |
| msdyn_LinkStatus                       | nie             | nie               |
| msdyn_linkstatusname                   | nie             | nie               |
| msdyn_msprojectclientid                | nie             | nie               |
| msdyn_plannedcost                      | nie             | nie               |
| msdyn_plannedcost_base                 | nie             | nie               |
| msdyn_plannedsales                     | nie             | nie               |
| msdyn_plannedsales_base                | nie             | nie               |
| msdyn_pluginprocessingdata             | nie             | nie               |
| msdyn_progress                         | nie             | nie (áno pre P4W) |
| msdyn_remainingcost                    | nie             | nie               |
| msdyn_remainingcost_base               | nie             | nie               |
| msdyn_remainingsales                   | nie             | nie               |
| msdyn_remainingsales_base              | nie             | nie               |
| msdyn_requestedhours                   | nie             | nie               |
| msdyn_resourcecategory                 | nie             | nie               |
| msdyn_resourcecategoryname             | nie             | nie               |
| msdyn_resourceorganizationalunitid     | nie             | nie               |
| msdyn_resourceorganizationalunitidname | nie             | nie               |
| msdyn_salesconsumptionpercentage       | nie             | nie               |
| msdyn_salesestimateatcomplete          | nie             | nie               |
| msdyn_salesestimateatcomplete_base     | nie             | nie               |
| msdyn_salesvariance                    | nie             | nie               |
| msdyn_salesvariance_base               | nie             | nie               |
| msdyn_scheduleddurationminutes         | nie             | nie               |
| msdyn_scheduledend                     | nie             | nie               |
| msdyn_scheduledstart                   | nie             | nie               |
| msdyn_schedulevariance                 | nie             | nie               |
| msdyn_skipupdateestimateline           | nie             | nie               |
| msdyn_skipupdateestimatelinename       | nie             | nie               |
| msdyn_summary                          | nie             | nie               |
| msdyn_varianceofcost                   | nie             | nie               |
| msdyn_varianceofcost_base              | nie             | nie               |

### <a name="project-task-dependency"></a>Závislosť projektovej úlohy

| **Logický názov**              | **Môže vytvoriť** | **Môže upravovať** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | nie             | nie           |
| msdyn_linktypename            | nie             | nie           |
| msdyn_predecessortask         | áno            | nie           |
| msdyn_predecessortaskname     | áno            | nie           |
| msdyn_project                 | áno            | nie           |
| msdyn_projectname             | áno            | nie           |
| msdyn_projecttaskdependencyid | áno            | nie           |
| msdyn_successortask           | áno            | nie           |
| msdyn_successortaskname       | áno            | nie           |

### <a name="resource-assignment"></a>Priradenie zdroja

| **Logický názov**             | **Môže vytvoriť** | **Môže upravovať** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | áno            | nie           |
| msdyn_bookableresourceidname | áno            | nie           |
| msdyn_bookingstatusid        | nie             | nie           |
| msdyn_bookingstatusidname    | nie             | nie           |
| msdyn_committype             | nie             | nie           |
| msdyn_committypename         | nie             | nie           |
| msdyn_effort                 | nie             | nie           |
| msdyn_effortcompleted        | nie             | nie           |
| msdyn_effortremaining        | nie             | nie           |
| msdyn_finish                 | nie             | nie           |
| msdyn_plannedcost            | nie             | nie           |
| msdyn_plannedcost_base       | nie             | nie           |
| msdyn_plannedcostcontour     | nie             | nie           |
| msdyn_plannedsales           | nie             | nie           |
| msdyn_plannedsales_base      | nie             | nie           |
| msdyn_plannedsalescontour    | nie             | nie           |
| msdyn_plannedwork            | nie             | nie           |
| msdyn_projectid              | áno            | nie           |
| msdyn_projectidname          | nie             | nie           |
| msdyn_projectteamid          | nie             | nie           |
| msdyn_projectteamidname      | nie             | nie           |
| msdyn_start                  | nie             | nie           |
| msdyn_taskid                 | nie             | nie           |
| msdyn_taskidname             | nie             | nie           |
| msdyn_userresourceid         | nie             | nie           |

### <a name="project-team-member"></a>Člen projektového tímu

| **Logický názov**                                 | **Môže vytvoriť** | **Môže upravovať** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | nie             | nie           |
| msdyn_creategenericteammemberwithrequirementname | nie             | nie           |
| msdyn_deletestatus                               | nie             | nie           |
| msdyn_deletestatusname                           | nie             | nie           |
| msdyn_effort                                     | nie             | nie           |
| msdyn_effortcompleted                            | nie             | nie           |
| msdyn_effortremaining                            | nie             | nie           |
| msdyn_finish                                     | nie             | nie           |
| msdyn_hardbookedhours                            | nie             | nie           |
| msdyn_hours                                      | nie             | nie           |
| msdyn_markedfordeletiontimer                     | nie             | nie           |
| msdyn_markedfordeletiontimestamp                 | nie             | nie           |
| msdyn_msprojectclientid                          | nie             | nie           |
| msdyn_percentage                                 | nie             | nie           |
| msdyn_requiredhours                              | nie             | nie           |
| msdyn_softbookedhours                            | nie             | nie           |
| msdyn_start                                      | nie             | nie           |

### <a name="project"></a>Project

| **Logický názov**                       | **Môže vytvoriť** | **Môže upravovať** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | nie             | nie           |
| msdyn_actualexpensecost_base           | nie             | nie           |
| msdyn_actuallaborcost                  | nie             | nie           |
| msdyn_actuallaborcost_base             | nie             | nie           |
| msdyn_actualsales                      | nie             | nie           |
| msdyn_actualsales_base                 | nie             | nie           |
| msdyn_contractlineproject              | áno            | nie           |
| msdyn_contractorganizationalunitid     | áno            | nie           |
| msdyn_contractorganizationalunitidname | áno            | nie           |
| msdyn_costconsumption                  | nie             | nie           |
| msdyn_costestimateatcomplete           | nie             | nie           |
| msdyn_costestimateatcomplete_base      | nie             | nie           |
| msdyn_costvariance                     | nie             | nie           |
| msdyn_costvariance_base                | nie             | nie           |
| msdyn_duration                         | nie             | nie           |
| msdyn_effort                           | nie             | nie           |
| msdyn_effortcompleted                  | nie             | nie           |
| msdyn_effortestimateatcompleteeac      | nie             | nie           |
| msdyn_effortremaining                  | nie             | nie           |
| msdyn_finish                           | áno            | áno          |
| msdyn_globalrevisiontoken              | nie             | nie           |
| msdyn_islinkedtomsprojectclient        | nie             | nie           |
| msdyn_islinkedtomsprojectclientname    | nie             | nie           |
| msdyn_linkeddocumenturl                | nie             | nie           |
| msdyn_msprojectdocument                | nie             | nie           |
| msdyn_msprojectdocumentname            | nie             | nie           |
| msdyn_plannedexpensecost               | nie             | nie           |
| msdyn_plannedexpensecost_base          | nie             | nie           |
| msdyn_plannedlaborcost                 | nie             | nie           |
| msdyn_plannedlaborcost_base            | nie             | nie           |
| msdyn_plannedsales                     | nie             | nie           |
| msdyn_plannedsales_base                | nie             | nie           |
| msdyn_progress                         | nie             | nie           |
| msdyn_remainingcost                    | nie             | nie           |
| msdyn_remainingcost_base               | nie             | nie           |
| msdyn_remainingsales                   | nie             | nie           |
| msdyn_remainingsales_base              | nie             | nie           |
| msdyn_replaylogheader                  | nie             | nie           |
| msdyn_salesconsumption                 | nie             | nie           |
| msdyn_salesestimateatcompleteeac       | nie             | nie           |
| msdyn_salesestimateatcompleteeac_base  | nie             | nie           |
| msdyn_salesvariance                    | nie             | nie           |
| msdyn_salesvariance_base               | nie             | nie           |
| msdyn_scheduleperformance              | nie             | nie           |
| msdyn_scheduleperformancename          | nie             | nie           |
| msdyn_schedulevariance                 | nie             | nie           |
| msdyn_taskearlieststart                | nie             | nie           |
| msdyn_teamsize                         | nie             | nie           |
| msdyn_teamsize_date                    | nie             | nie           |
| msdyn_teamsize_state                   | nie             | nie           |
| msdyn_totalactualcost                  | nie             | nie           |
| msdyn_totalactualcost_base             | nie             | nie           |
| msdyn_totalplannedcost                 | nie             | nie           |
| msdyn_totalplannedcost_base            | nie             | nie           |


## <a name="limitations-and-known-issues"></a>Obmedzenia a známe problémy
Nasleduje zoznam obmedzení a známych problémov:

- API pre plánovanie môžu používať iba **Používatelia s licenciou Microsoft Project**. Nemôžu ich používať:
    - Používatelia aplikácie
    - Systémoví používatelia
    - Používatelia integrácie
    - Ostatní používatelia, ktorí nemajú požadovanú licenciu
- Každá množina **OperationSet** môže mať maximálne 100 operácií.
- Každý používateľ môže mať maximálne 10 otvorených množín **OperationSets**.
- Project Operations v súčasnosti podporuje v projekte celkovo maximálne 500 úloh.
- Stav zlyhania množiny **OperationSet** a protokoly zlyhaní nie sú momentálne k dispozícii.
- Rozhrania API pre plánovanie sú vo verejnej verzii Preview. Spoločnosť Microsoft nepodporuje použitie týchto rozhraní API v produkčnom prostredí.
- [Hranice projektov a úloh](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Spracovanie chýb

   - Ak chcete skontrolovať chyby generované z množín operácií, prejdite na **Nastavenie**\> **Integrácia plánu** \> **Množiny operácií**.
   - Ak chcete skontrolovať chyby generované službou plánovania projektu, choďte na **Nastavenia** \> **Integrácia plánu** \> **Denníky chýb PSS**.

## <a name="sample-scenario"></a>Vzorový scenár

V tomto scenári vytvoríte projekt, člena tímu, štyri úlohy a dve priradenia zdrojov. Ďalej aktualizujete jednu úlohu, projekt, odstránite jednu úlohu, odstránite jedno priradenie zdroja a vytvoríte závislosť úlohy.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Ďalšie ukážky

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
