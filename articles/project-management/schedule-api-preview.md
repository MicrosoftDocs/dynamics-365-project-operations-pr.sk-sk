---
title: Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu
description: Tento článok poskytuje informácie a ukážky používania rozhraní API plánovania projektu.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541144"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


**Entity na plánovanie**

Rozhrania API pre plánovanie projektu umožňujú vykonávať operácie vytvárania, aktualizácie a mazania pomocou **Entít plánovania**. Tieto entity sú spravované prostredníctvom modulu Plánovanie v Projekte pre web. Operácie vytvárania, aktualizácie a odstraňovania pomocou **Entít plánovania** boli obmedzené v skorších vydaniach Dynamics 365 Project Operations.

Nasledujúca tabuľka poskytuje úplný zoznam entít plánovania projektu.

| **Názov entity**         | **Logický názov entity**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektová úloha            | msdyn_projecttask           |
| Závislosť projektovej úlohy | msdyn_projecttaskdependency |
| Priradenie zdroja     | msdyn_resourceassignment    |
| Projektový kontajner          | msdyn_projectbucket         |
| Člen projektového tímu     | msdyn_projectteam           |
| Kontrolné zoznamy projektu      | msdyn_projectchecklist      |
| Označenie projektu           | msdyn_projectlabel          |
| Projektová úloha na označenie   | msdyn_projecttasktolabel    |
| Šprint projektu          | msdyn_projectsprint         |

**OperationSet**

OperationSet je vzor jednotky práce, ktorý je možné použiť, keď sa v rámci transakcie musí spracovať niekoľko požiadaviek ovplyvňujúcich plán.

**API plánovania projektu**

Nasleduje zoznam aktuálnych rozhraní API plánovania projektu.

| **API**                                 | Description                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Toto API sa používa na vytvorenie projektu. Projekt a predvolený sektor projektu sa vytvoria okamžite.                         |
| **msdyn_CreateTeamMemberV1**            | Toto API sa používa na vytvorenie člena projektového tímu. Záznam o členovi tímu sa vytvorí okamžite.                                  |
| **msdyn_CreateOperationSetV1**          | Toto API sa používa na plánovanie niekoľkých požiadaviek, ktoré sa musia vykonať v rámci transakcie.                                        |
| **msdyn_PssCreateV1**                   | Toto API sa používa na vytvorenie entity. Entitou môže byť ktorákoľvek z entít plánovania projektu, ktoré podporujú operáciu vytvorenia. |
| **msdyn_PssUpdateV1**                   | Toto API sa používa na aktualizáciu entity. Entitou môže byť ktorákoľvek z entít plánovania projektu, ktoré podporujú operáciu aktualizácie  |
| **msdyn_PssDeleteV1**                   | Toto API sa používa na odstránenie entity. Entitou môže byť ktorákoľvek z entít plánovania projektu, ktoré podporujú operáciu vymazania. |
| **msdyn_ExecuteOperationSetV1**         | Toto API sa používa na vykonávanie všetkých operácií v rámci danej sady operácií.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Toto API sa používa na aktualizáciu plánovaného pracovného obrysu priradenia prostriedkov.                                                        |



**Používanie rozhraní API pre plánovanie projektu s OperationSet**

Pretože záznamy s **CreateProjectV1** a **CreateTeamMemberV1** sú vytvorené okamžite, tieto API nemôžu byť použité v **OperationSet** priamo. Môžete však použiť API na vytvorenie potrebných záznamov, vytvorenie **OperationSet** a potom použiť tieto vopred vytvorené záznamy v **OperationSet**.

**Podporované operácie**

| **Entita na plánovanie**   | **Vytvoriť** | **Aktualizácia** | **Delete** | **Dôležité aspekty**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektová úloha            | Áno        | Áno        | Áno        | The **Pokrok**, **dokončené**, a **Zostávajúce úsilie** polia je možné upravovať v Project for the Web, ale nie je možné ich upravovať v Project Operations.                                                                                                                                                                                             |
| Závislosť projektovej úlohy | Áno        | No         | Áno        | Záznamy o závislosti od projektových úloh sa neaktualizujú. Namiesto toho je možné starý záznam vymazať a vytvoriť nový.                                                                                                                                                                                                                                 |
| Priradenie zdroja     | Áno        | Áno\*      | Áno        | Operácie s nasledujúcimi poľami nie sú podporované: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining** a **PlannedWork**. Záznamy o priradení zdrojov sa neaktualizujú. Namiesto toho je možné starý záznam vymazať a vytvoriť nový. Na aktualizáciu obrysov priradenia zdrojov bolo poskytnuté samostatné rozhranie API. |
| Projektový kontajner          | Áno        | Áno        | Áno        | Predvolený segment sa vytvorí pomocou **CreateProjectV1** API. V aktualizácii Release 16 bola pridaná podpora na vytváranie a odstraňovanie sektorov projektov.                                                                                                                                                                                                   |
| Člen projektového tímu     | Áno        | Áno        | Áno        | Na operáciu vytvorenia použite API **CreateTeamMemberV1**.                                                                                                                                                                                                                                                                                           |
| Project                 | Áno        | Áno        |            | Operácie s nasledujúcimi poľami nie sú podporované: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart** a **Duration**.                                                                                       |
| Kontrolné zoznamy projektu      | Áno        | Áno        | Áno        |                                                                                                                                                                                                                                                                                                                                                         |
| Označenie projektu           | No         | Áno        | No         | Názvy štítkov je možné zmeniť. Táto funkcia je dostupná len pre Project for the Web                                                                                                                                                                                                                                                                      |
| Projektová úloha na označenie   | Áno        | No         | Áno        | Táto funkcia je dostupná len pre Project for the Web                                                                                                                                                                                                                                                                                                  |
| Šprint projektu          | Áno        | Áno        | Áno        | The **Štart** pole musí mať dátum skorší ako **Skončiť** lúka. Šprinty toho istého projektu sa nemôžu navzájom prekrývať. Táto funkcia je dostupná len pre Project for the Web                                                                                                                                                                    |




Toto ID vlastnosti je voliteľné. Ak je uvedené, systém sa ho pokúsi použiť a v prípade, že ho nemožno použiť, vyvolá výnimku. Ak nie je uvedené, systém ho vygeneruje.

**Obmedzenia a známe problémy**

Nasleduje zoznam obmedzení a známych problémov:

-   Rozhrania Project Schedule API môžu používať iba používatelia **Používatelia s licenciou Microsoft Project**. Nemôžu ich používať:
    -   Používatelia aplikácie
    -   Systémoví používatelia
    -   Používatelia integrácie
    -   Ostatní používatelia, ktorí nemajú požadovanú licenciu
-   Každá množina **OperationSet** môže mať maximálne 100 operácií.
-   Každý používateľ môže mať maximálne 10 otvorených množín **OperationSets**.
-   Project Operations v súčasnosti podporuje v projekte celkovo maximálne 500 úloh.
-   Každá operácia Update Resource Assignment Contour sa počíta ako jedna operácia.
-   Každý zoznam aktualizovaných obrysov môže obsahovať maximálne 100 časových rezov.
-   Stav zlyhania množiny **OperationSet** a protokoly zlyhaní nie sú momentálne k dispozícii.
-   Na jeden projekt je maximálne 400 šprintov.
-   [Limity a hranice projektov a úloh](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Menovky sú momentálne dostupné len pre Project for the Web.

**Spracovanie chýb**

-   Ak chcete skontrolovať chyby generované z množín operácií, prejdite na **Nastavenie**\> **Integrácia plánu** \> **Množiny operácií**.
-   Ak chcete skontrolovať chyby generované službou plánovania projektu, prejdite na **Nastavenia** \> **Integrácia plánu** \> **Denník chýb PSS**.

**Úprava obrysov priradenia zdrojov**

Na rozdiel od všetkých ostatných API plánovania projektov, ktoré aktualizujú entitu, API obrysu priradenia prostriedkov je výhradne zodpovedné za aktualizácie jedného poľa msdyn_plannedwork v jednej entite msydn_resourceassignment.

Daný režim plánovania je:

-   **pevné jednotky**
-   Projektový kalendár je 9-17 hodín je 9-5 pst, pondelok, utorok, štvrtok, piatok (BEZ PRACOVNEJ STREDY)
-   A kalendár zdrojov je 9-1p PST od pondelka do piatka

Táto úloha je na jeden týždeň, štyri hodiny denne. Je to preto, že kalendár zdrojov je od 9 do 1 PST alebo štyri hodiny denne.

| &nbsp;     | Úloha | Počiatočný dátum | Konečný dátum  | Množstvo | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 pracovník |  T1  | 6. 2022  | 6. 2022 | 20       | 4         | 4         | 4         | 4         | 4         |

Napríklad, ak chcete, aby pracovník tento týždeň pracoval iba tri hodiny denne a jednu hodinu si nechal na iné úlohy.

#### <a name="updatedcontours-sample-payload"></a>Aktualizované užitočné zaťaženie vzorky Contours:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Toto je priradenie po spustení rozhrania Update Contour Schedule API.

| &nbsp;     | Úloha | Počiatočný dátum | Konečný dátum  | Množstvo | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 | 6. 2022 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9-1 pracovník | T1   | 6. 2022  | 6. 2022 | 15       | 3         | 3         | 3         | 3         | 3         |


**Vzorový scenár**

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

** Ďalšie vzorky

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
