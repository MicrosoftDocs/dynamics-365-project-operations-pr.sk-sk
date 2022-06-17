---
title: Denníky plánovania projektov
description: Tento článok poskytuje informácie a ukážky, ktoré vám pomôžu používať denníky plánovania projektu na sledovanie zlyhaní, ktoré súvisia so službou plánovania projektu a rozhraniami API plánovania projektu.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923714"
---
# <a name="project-scheduling-logs"></a>Denníky plánovania projektov

_**Týka sa:** Projektové operácie pre scenáre založené na zdrojoch/nezásobách, nasadenie Lite – fakturácia od dohody k zálohovej fakturácii_, _pre web_

Microsoft Dynamics 365 Project Operations používa [Projekt pre web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) ako jeho primárny motor plánovania. Namiesto použitia štandardu Microsoft Dataverse Webové aplikačné programovacie rozhrania (API), Project Operations používa nové Project Scheduling API na vytváranie, aktualizáciu a odstraňovanie projektových úloh, priradení zdrojov, závislostí úloh, projektových segmentov a členov projektových tímov. Keď sú však operácie vytvorenia, aktualizácie alebo vymazania programovo spustené na entitách štruktúry rozpisu práce (WBS), môžu sa vyskytnúť chyby. Na sledovanie týchto chýb a histórie operácií boli implementované dva nové administratívne protokoly: **Operačná sada** a **Služba plánovania projektov (PSS)**. Ak chcete získať prístup k týmto denníkom, prejdite na **nastavenie** \> **Plán integrácie**.

Nasledujúca ilustrácia zobrazuje dátový model pre denníky plánovania projektu.

![Dátový model pre denníky plánovania projektu.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operácia Nastaviť protokol

Protokol množiny operácií sleduje vykonávanie množiny operácií, ktorá sa používa na spustenie jednej alebo viacerých operácií vytvorenia, aktualizácie alebo odstraňovania v dávke na projektoch, projektových úlohách, priradeniach zdrojov, závislosti úloh, segmentoch projektov alebo členoch projektového tímu. The **Operácia v stave** pole zobrazuje celkový stav množiny operácií. Podrobnosti o užitočnom zaťažení sady operácií sú zachytené v súvisiacich záznamoch podrobností sady operácií.

### <a name="operation-set"></a>Operačná sada

Nasledujúca tabuľka zobrazuje polia, ktoré súvisia s **Operačná sada** subjekt.

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Dátum/čas, kedy bola nastavená operácia dokončená alebo zlyhala.                                                | CompletedOn            |
| msdyn_correlationid   | The **correlationId** hodnotu požiadavky.                                                                  | CorrelationId          |
| msdyn_description     | Popis operačného súboru.                                                                        | Description            |
| msdyn_executedon      | Dátum/čas, kedy bol záznam spustený.                                                                       | Dátum vykonania            |
| msdyn_operationsetId  | Jedinečný identifikátor inštancií entity.                                                                   | OperationSet           |
| msdyn_Project         | Projekt, ktorý súvisí s prevádzkovým súborom.                                                            | Project                |
| msdyn_projectid       | The **projectId** hodnotu požiadavky.                                                                      | ProjectId (zastarané) |
| msdyn_projectName     | Nevzťahuje sa.                                                                                              | Nevzťahuje sa         |
| msdyn_PSSErrorLog     | Jedinečný identifikátor protokolu chýb služby Project Scheduling Service, ktorý je priradený k množine operácií. | Denník chýb služby PSS          |
| msdyn_PSSErrorLogName | Nevzťahuje sa.                                                                                              | Nevzťahuje sa         |
| msdyn_status          | Stav sady operácií.                                                                             | Status                 |
| msdyn_statusName      | Nevzťahuje sa.                                                                                              | Nevzťahuje sa         |
| msdyn_useraadid       | The Azure Active Directory (Azure AD) ID objektu používateľa, ktorému žiadosť patrí.                     | UserAADID              |

### <a name="operation-set-detail"></a>Podrobnosti nastavenia operácie

Nasledujúca tabuľka zobrazuje polia, ktoré súvisia s **Podrobnosti nastavenia operácie** subjekt.

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializované Dataverse polia žiadosti.                                            | CdsPayload            |
| msdyn_entityname           | Názov subjektu pre žiadosť.                                                     | EntityName            |
| msdyn_httpverb             | Metóda požiadavky.                                                                         | HTTPVerb (zastarané) |
| msdyn_httpverbName         | Nevzťahuje sa.                                                                             | Nevzťahuje sa        |
| msdyn_operationset         | Jedinečný identifikátor množiny operácií, do ktorej záznam patrí.                      | OperationSet          |
| msdyn_operationsetdetailId | Jedinečný identifikátor inštancií entity.                                                  | Podrobnosti o množine OperationSet   |
| msdyn_operationsetName     | Nevzťahuje sa.                                                                             | Nevzťahuje sa        |
| msdyn_operationtype        | Typ operácie detail sady operácií.                                             | Typ operácie         |
| msdyn_operationtypeName    | Nevzťahuje sa.                                                                             | Nevzťahuje sa        |
| msdyn_psspayload           | Serializované polia Project Scheduling Service pre požiadavku.                           | PssPayload            |
| msdyn_recordid             | Identifikátor záznamu žiadosti.                                                       | ID záznamu             |
| msdyn_requestnumber        | Automaticky vygenerované číslo, ktoré identifikuje objednávku, v ktorej boli žiadosti prijaté. | Číslo žiadosti        |

## <a name="project-scheduling-service-error-logs"></a>Protokoly chýb služby plánovania projektu

Protokoly chýb služby Project Scheduling Service zachytávajú zlyhania, ku ktorým dôjde, keď sa služba Project Scheduling Service pokúsi a **Uložiť** alebo **OTVORENÉ** prevádzka. Existujú tri podporované scenáre, v ktorých sa tieto protokoly generujú:

- Akcie spustené používateľom kriticky zlyhávajú (napríklad nemožno vytvoriť priradenie z dôvodu chýbajúcich privilégií).
- Služba plánovania projektu nemôže programovo vytvárať, aktualizovať, odstraňovať ani vykonávať žiadne iné kaskádové operácie na entite.
- Používateľ zaznamená chyby, keď sa záznam nepodarí otvoriť (napríklad keď sa otvorí projekt alebo sa aktualizujú informácie o členovi tímu).

### <a name="project-scheduling-service-log"></a>Denník služby plánovania projektu

Nasledujúca tabuľka zobrazuje polia, ktoré sú zahrnuté v denníku Project Scheduling Service.

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Zásobník volaní výnimky.                                               | Zásobník volaní     |
| msdyn_correlationid | ID korelácie chyby.                                               | CorrelationId  |
| msdyn_errorcode     | Pole, ktoré sa používa na uloženie Dataverse kód chyby alebo kód chyby HTTP. | Kód chyby     |
| msdyn_HelpLink      | Odkaz na verejnú dokumentáciu Pomocníka.                                       | Prepojenie na Pomocníka      |
| msdyn_log           | Denník zo služby plánovania projektu.                                   | Denník            |
| msdyn_project       | Projekt, ktorý je priradený k denníku chýb.                             | Project        |
| msdyn_projectName   | Názov projektu, ak sa zachová užitočné zaťaženie súboru operácií. | Nevzťahuje sa |
| msdyn_psserrorlogId | Jedinečný identifikátor inštancií entity.                                     | Denník chýb služby PSS  |
| msdyn_SessionId     | ID relácie projektu.                                                        | ID relácie     |

## <a name="error-log-cleanup"></a>Čistenie denníka chýb

V predvolenom nastavení možno denníky chýb služby plánovania projektu aj denník množiny operácií čistiť každých 90 dní. Všetky záznamy, ktoré sú staršie ako 90 dní, budú vymazané. Avšak zmenou hodnoty **msdyn_StateOperationSetAge** pole na **Parametre projektu** správcovia môžu upraviť rozsah čistenia tak, aby bol medzi 1 a 120 dňami. Na zmenu tejto hodnoty je k dispozícii niekoľko spôsobov:

- Prispôsobte si **Parameter projektu** vytvorením vlastnej stránky a pridaním **Zastarané operácie Nastaviť vek** lúka.
- Použite klientsky kód, ktorý používa [Súprava na vývoj softvéru WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Použite kód Service SDK, ktorý používa Xrm SDK **updateRecord** metóda (odkaz na klientske rozhranie API) v aplikáciách riadených modelom. Power Apps obsahuje popis a podporované parametre pre **updateRecord** metóda.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
