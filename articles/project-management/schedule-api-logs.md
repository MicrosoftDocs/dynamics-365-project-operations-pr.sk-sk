---
title: Denníky plánovania projektov
description: Tento článok obsahuje informácie a ukážky, ktoré vám pomôžu používať denníky plánovania projektu na sledovanie zlyhaní, ktoré súvisia so službou plánovania projektu a rozhraniami API plánovania projektu.
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

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách, nasadenie Lite – dohoda o proforma fakturácii_, _Project for the Web_

Microsoft Dynamics 365 Project Operations používa [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) ako svoj primárny nástroj plánovania. Namiesto použitia štandardného webových aplikačných programovacích rozhraní (API) Microsoft Dataverse, používa Project Operations nové API plánovania projektov na vytváranie, aktualizáciu a odstraňovanie projektových úloh, priradení zdrojov, závislostí úloh, projektových kontajnerov a členov projektových tímov. Keď sú však operácie vytvorenia, aktualizácie alebo vymazania programovo spustené na entitách štruktúry rozdelenia práce (WBS), môžu sa vyskytnúť chyby. Na sledovanie týchto chýb a histórie operácií boli implementované dva nové administratívne protokoly: **Množina operácií** a **Služba plánovania projektov (PSS)**. Ak chcete získať prístup k týmto denníkom, prejdite na **Nastavenie** \> **Integrácia plánu**.

Nasledujúca ilustrácia zobrazuje dátový model pre denníky plánovania projektu.

![Dátový model pre denníky plánovania projektu.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Denník množiny operácií

Denník množiny operácií sleduje vykonávanie množiny operácií, ktorá sa používa na spustenie jednej alebo viacerých operácií vytvorenia, aktualizácie alebo odstraňovania v dávke na projektoch, projektových úlohách, priradeniach zdrojov, závislosti úloh, projektových kontajnerov alebo členov projektového tímu. Pole **Operácia v stave** zobrazuje celkový stav množiny operácií. Podrobnosti o údajovej časti množiny operácií sú zachytené v súvisiacich záznamoch Podrobnosti o množine operácií.

### <a name="operation-set"></a>Množina operácií

Nasledujúca tabuľka zobrazuje polia, ktoré sa týkajú entity **Množina operácií**.

| Názov schémy            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Dátum a čas, dokončenia alebo zlyhania množiny operácií.                                                | CompletedOn            |
| msdyn_correlationid   | Hodnota **correlationId** žiadosti.                                                                  | CorrelationId          |
| msdyn_description     | Opis množiny možností.                                                                        | Description            |
| msdyn_executedon      | Dátum/čas, kedy bol záznam spustený.                                                                       | Dátum vykonania            |
| msdyn_operationsetId  | Jednoznačný identifikátor inštancií entity.                                                                   | OperationSet           |
| msdyn_Project         | Projekt, ktorý súvisí s množinou operácií.                                                            | Project                |
| msdyn_projectid       | Hodnota **projectId** žiadosti.                                                                      | ProjectId (zastarané) |
| msdyn_projectName     | Nevzťahuje sa.                                                                                              | Nevzťahuje sa         |
| msdyn_PSSErrorLog     | Jednoznačný identifikátor protokolu chýb služby plánovania projektov, ktorý je priradený k množine operácií. | Denník chýb služby PSS          |
| msdyn_PSSErrorLogName | Nevzťahuje sa.                                                                                              | Nevzťahuje sa         |
| msdyn_status          | Stav množiny možností.                                                                             | Status                 |
| msdyn_statusName      | Nevzťahuje sa.                                                                                              | Nevzťahuje sa         |
| msdyn_useraadid       | ID objektu Azure Active Directory (Azure AD) používateľa, ktorému patrí žiadosť.                     | UserAADID              |

### <a name="operation-set-detail"></a>Podrobnosti o množine operácií

Nasledujúca tabuľka zobrazuje polia, ktoré sa týkajú entity **Podrobnosti o množine operácií**.

| Názov schémy                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Serializované polia Dataverse pre žiadosť.                                            | CdsPayload            |
| msdyn_entityname           | Názov entity pre žiadosť.                                                     | EntityName            |
| msdyn_httpverb             | Metóda žiadosti.                                                                         | HTTPVerb (zastarané) |
| msdyn_httpverbName         | Nevzťahuje sa.                                                                             | Nevzťahuje sa        |
| msdyn_operationset         | Jednoznačný identifikátor množiny možností, do ktorej patrí tento záznam.                      | OperationSet          |
| msdyn_operationsetdetailId | Jednoznačný identifikátor inštancií entity.                                                  | Podrobnosti o množine OperationSet   |
| msdyn_operationsetName     | Nevzťahuje sa.                                                                             | Nevzťahuje sa        |
| msdyn_operationtype        | Typ operácie podrobností množiny operácií.                                             | Typ operácie         |
| msdyn_operationtypeName    | Nevzťahuje sa.                                                                             | Nevzťahuje sa        |
| msdyn_psspayload           | Serializované polia služby plánovania projektu pre požiadavku.                           | PssPayload            |
| msdyn_recordid             | Identifikátor záznamu požiadavky.                                                       | ID záznamu             |
| msdyn_requestnumber        | Automaticky vygenerované číslo, ktoré identifikuje objednávky, v ktorej bola prijatá žiadosť. | Číslo žiadosti        |

## <a name="project-scheduling-service-error-logs"></a>Denníky chýb služby plánovania projektu

Denníky chýb služby plánovania projektu zachytávajú zlyhania, ku ktorým dôjde, keď sa služba plánovania projektu pokúsi vykonať operáciu **Uložiť** alebo **Otvoriť**. Existujú tri podporované scenáre, v ktorých sa tieto denníky generujú:

- Akcie spustené používateľom kriticky zlyhajú (napríklad nemožno vytvoriť priradenie z dôvodu chýbajúcich privilégií).
- Služba plánovania projektu nemôže programovo vytvárať, aktualizovať, odstraňovať ani vykonávať žiadne iné kaskádové operácie na entite.
- Používateľ zaznamená chyby, keď sa záznam nepodarí otvoriť (napríklad keď je otvorený projekt alebo sa aktualizujú informácie o členovi tímu).

### <a name="project-scheduling-service-log"></a>Denník služby plánovania projektu

Nasledujúca tabuľka zobrazuje polia, ktoré sú súčasťou denníka služby plánovania projektu.

| Názov schémy          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Zásobník volaní výnimky.                                               | Zásobník volaní     |
| msdyn_correlationid | ID korelácie chyby.                                               | CorrelationId  |
| msdyn_errorcode     | Pole, ktoré sa používa na uloženie kódu chyby Dataverse alebo kódu chyby HTTP. | Kód chyby     |
| msdyn_HelpLink      | Prepojenie na verejnú pomocnú dokumentáciu.                                       | Prepojenie na Pomocníka      |
| msdyn_log           | Denník zo služby plánovania projektu.                                   | Denník            |
| msdyn_project       | Projekt, ktorý je priradený k denníku chýb.                             | Project        |
| msdyn_projectName   | Názov projektu, ak sa zachová údajová časť množiny operácií. | Nevzťahuje sa |
| msdyn_psserrorlogId | Jednoznačný identifikátor inštancií entity.                                     | Denník chýb služby PSS  |
| msdyn_SessionId     | ID relácie projektu.                                                        | ID relácie     |

## <a name="error-log-cleanup"></a>Vymazanie denníka chýb

V predvolenom nastavení možno denníky chýb služby plánovania projektu aj denník množiny operácií čistiť každých 90 dní. Všetky záznamy, ktoré sú staršie ako 90 dní, sa odstránia. Avšak zmenou hodnoty poľa **msdyn_StateOperationSetAge** na stránke **Parametre projektu** správcovia môžu upraviť rozsah čistenia tak, aby bol medzi 1 a 120 dňami. Na zmenu tejto hodnoty je k dispozícii niekoľko spôsobov:

- Prispôsobte si entitu **Parameter projektu** vytvorením vlastnej stránky a pridaním poľa **Vek zastaranej množiny operácií**.
- Použite klientsky kód, ktorý používa [Súprava na vývoj softvéru WebApi (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Použite kód Service SDK, ktorý používa metóda Xrm SDK **updateRecord** (referencia na klientske rozhranie API) v modelom riadených aplikáciách. Power Apps obsahuje popis a podporované parametre pre metódu **updateRecord**.

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
