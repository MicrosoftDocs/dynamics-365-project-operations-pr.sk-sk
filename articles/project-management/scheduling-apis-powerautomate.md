---
title: Použitie rozhraní API plánovania projektov so službou Power Automate
description: Tento článok poskytuje vzorový postup, ktorý používa rozhrania API na plánovanie projektov.
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404465"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Použitie rozhraní API plánovania projektov so službou Power Automate

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok popisuje vzorový postup, ktorý ukazuje, ako vytvoriť úplný plán projektu pomocou Microsoft Power Automate, ako vytvoriť množinu operácií a ako aktualizovať entitu. Príklad ukazuje, ako vytvoriť projekt, člena projektového tímu, množiny operácií, projektové úlohy a priradenia zdrojov. Tento článok tiež vysvetľuje, ako aktualizovať entitu a spustiť množinu operácií.

Nasleduje úplný zoznam krokov, ktoré sú zdokumentované vo vzorovom postupe v tomto článku:

1. [Vytvorenie spúšťača PowerApps](#1)
2. [Vytvoriť projekt](#2)
3. [Inicializácia premennej pre člena tímu](#3)
4. [Vytvorenie všeobecného člena tímu](#4)
5. [Vytvorenie množiny operácií](#5)
6. [Vytvorenie kontajnera projektu](#6)
7. [Inicializácia premennej pre stav prepojenia](#7)
8. [Inicializácia premennej pre počet úloh](#8)
9. [Inicializácia premennej pre ID projektovej úlohy](#9)
10. [Vykonať do](#10)
11. [Nastavenie projektovej úlohy](#11)
12. [Vytvorenie projektovej úlohy](#12)
13. [Vytvorenie priradenia zdroja](#13)
14. [Zníženie hodnoty premennej](#14)
15. [Premenovanie projektovej úlohy](#15)
16. [Spustenie množiny operácií](#16)

## <a name="assumptions"></a>Predpoklady

Tento článok predpokladá, že máte základné znalosti o platforme Dataverse, postupoch v cloude a rozhraní na programovanie aplikácií (API) pre plánovanie projektov. Ďalšie informácie nájdete v časti [Odkazy](#references) ďalej v tomto článku.

## <a name="create-a-flow"></a>Vytvorte postup

### <a name="select-an-environment"></a>Vyberte prostredie

Vo svojom prostredí môžete vytvoriť postup Power Automate.

1. Prejdite do <https://flow.microsoft.com> a prihláste sa pomocou svojich poverení správcu.
2. V pravom hornom rohu vyberte **Prostredia**.
3. V zozname vyberte prostredie, kde je nainštalované Dynamics 365 Project Operations.

### <a name="create-a-solution"></a>Vytvorenie riešenia

Ak chcete vytvoriť [postup podporujúci riešenie](/power-automate/overview-solution-flows), postupujte podľa týchto krokov. Vytvorením postupu podporujúceho riešenie môžete postup jednoduchšie exportovať a použiť ho neskôr.

1. Na navigačnej table kliknite na položku **Riešenia**.
2. Na stránke **Riešenia** vyberte **Nové riešenie**.
3. V dialógovom okne **Nové riešenie** nastavte povinné polia a následne vyberte **Vytvoriť**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>Krok 1: Vytvorte spúšťač PowerApps

1. Na stránke **Riešenia** vyberte riešenie, ktoré ste vytvorili, a následne vyberte **Nové**.
2. Na ľavej table vyberte **Postupy v cloude** \> **Automatizácia** \> **Postup v cloude** \> **Okamžité**.
3. V poli **Názov postupu** zadajte **Schedule API Demo Flow**.
4. V zozname **Vyberte spôsob spustenia tohto postupu** vyberte **Power Apps**. Keď vytvoríte spúšťač Power Apps, logika je na vás ako autorovi. V tomto článku ponechajte vstupné parametre prázdne na účely testovania.
5. Vyberte položku **Vytvoriť**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Krok 2: Vytvorenie projektu

Ak chcete vytvoriť vzorový projekt, postupujte podľa týchto krokov.

1. V postupe, ktorý ste vytvorili, vyberte **Nový krok**.

    ![Pridanie nového kroku.](media/newstep.png)

2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.

    ![Výber operácie.](media/chooseactiontab.png)

3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.

![Premenovanie kroku.](media/renamestep.png)

4. Premenujte krok **Vytvoriť projekt**.
5. V poli **Názov akcie** vyberte **msdyn\_CreateProjectV1**.
6. V poli **msdyn\_subject** vyberte **Pridať dynamický obsah**.
7. Na karte **Výraz** do poľa funkcie zadajte **Názov projektu – utcNow()**.
8. Vyberte položku **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>Krok 3: Inicializácia premennej pre člena tímu

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **inicializácia premennej**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Inicializácia člena tímu**.
5. V poli **Názov** zadajte **TeamMemberAction**.
6. V poli **Typ** vyberte **Reťazec**.
7. V poli **Hodnota** zadajte **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>Krok 4: Vytvorenie všeobecného člena tímu

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Vytvorenie člena tímu**.
5. Pre pole **Názov akcie** vyberte **TeamMemberAction** v dialógovom okne **Dynamický obsah**.
6. V poli **Parametre akcie** zadajte nasledujúce informácie o parametroch.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Tu je vysvetlenie parametrov:

    - **\@\@odata.type** – Názov entity. Napríklad zadajte **„Microsoft.Dynamics.CRM.msdyn\_projectteam“**.
    - **msdyn\_projektteamid** – Primárny kľúč ID projektového tímu. Hodnota je výraz jednoznačného globálneho identifikátora (GUID).   ID sa generuje z karty výrazu.

    - **msdyn\_project\@odata.bind** – ID projektu vlastníka projektu. Hodnota bude dynamický obsah, ktorý pochádza z odozvy kroku „Vytvoriť projekt“. Uistite sa, že ste zadali celú cestu a pridali dynamický obsah do zátvoriek. Úvodzovky sú povinné. Napríklad zadajte **„/msdyn\_projects(PRIDAŤ DYNAMICKÝ OBSAH)“**.
    - **msdyn\_name** – Meno člena tímu. Napríklad zadajte **„ScheduleAPIDemoTM1“**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>Krok 5: Vytvorenie množiny operácií

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Vytvorenie množiny operácií**.
5. V poli **Názov akcie** vyberte vlastnú akciu **msdyn\_CreateOperationSetV1** Dataverse.
6. V poli **Popis** zadajte **ScheduleAPIDemoOperationSet**.
7. V poli **Projekt** zadajte **/msdyn\_projects(**.
8. V dialógovom okne **Dynamický obsah** vyberte **msdyn\_CreateProjectV1Response ProjectId**.
9. V poli **Projekt** zadajte **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>Krok 6: Vytvorenie kontajnera projektu

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **pridať nový riadok**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Vytvoriť kontajner**.
5. V poli **Názov tabuľky** vyberte možnosť **Projektové kontajnery**.
6. V poli **Názov** zadajte **ScheduleAPIDemoBucket1**.
7. Pre pole **Projekt** vyberte **msdyn\_CreateProjectV1Response ProjectId** v dialógovom okne **Dynamický obsah**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>Krok 7: Inicializácia premennej pre stav prepojenia

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **inicializácia premennej**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Inicializovať linkstatus**.
5. V poli **Názov** zadajte **linkstatus**.
6. V poli **Typ** vyberte **Celé číslo**.
7. V poli **Hodnota** zadajte **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>Krok 8: Inicializácia premennej pre počet úloh

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **inicializácia premennej**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Inicializácia počtu úloh**.
5. V poli **Názov** zadajte **počet úloh**.
6. V poli **Typ** vyberte **Celé číslo**.
7. V poli **Hodnota** zadajte **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>Krok 9: Inicializácia premennej pre ID projektovej úlohy

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **inicializácia premennej**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Inicializácia ProjectTaskID**.
5. V poli **Názov** zadajte **počet úloh**.
6. V poli **Typ** vyberte **Reťazec**.
7. Pre pole **Hodnota** zadajte **guid()** v nástroji na tvorbu výrazov.

## <a name="step-10-do-until"></a><a id="10"></a>Krok 10: Do until

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **do until**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. Nastavte prvú hodnotu v podmienenom príkaze na premennú **počet úloh** z dialógového okna **Dynamický obsah**.
4. Nastavte podmienku na **menšie než alebo sa rovná**.
5. Nastavte druhú hodnotu v podmienenom príkaze na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>Krok 11: Nastavenie projektovej úlohy

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **nastaviť premennú**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Nastaviť projektovú úlohu**.
5. V poli **Názov** vyberte **msdyn\_projecttaskid**.
6. Pre pole **Hodnota** zadajte **guid()** v nástroji na tvorbu výrazov.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>Krok 12: Vytvorenie projektovej úlohy

Podľa týchto krokov vytvorte projektovú úlohu, ktorá má jedinečné ID, ktoré patrí aktuálnemu projektu a kontajneru projektov, ktorý ste vytvorili.

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Vytvoriť projektovú úlohu**.
5. V poli **Názov akcie** vyberte **msdyn\_PssCreateV1**.
6. V poli **Entita** zadajte nasledujúce informácie o parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Tu je vysvetlenie parametrov:

    - **\@\@odata.type** – Názov entity. Napríklad zadajte **„Microsoft.Dynamics.CRM.msdyn\_projecttask“**.
    - **msdyn\_projecttaskid** – Jedinečné ID úlohy. Hodnota by mala byť nastavená na dynamickú premennú z **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – ID projektu vlastníka projektu. Hodnota bude dynamický obsah, ktorý pochádza z odozvy kroku „Vytvoriť projekt“. Uistite sa, že ste zadali celú cestu a pridali dynamický obsah do zátvoriek. Úvodzovky sú povinné. Napríklad zadajte **„/msdyn\_projects(PRIDAŤ DYNAMICKÝ OBSAH)“**.
    - **msdyn\_subject** – Ľubovoľný názov úlohy.
    - **msdyn\_projectbucket\@odata.bind** – Kontajner projektu, ktorý obsahuje úlohy. Hodnota bude dynamický obsah, ktorý pochádza z odozvy kroku „Vytvoriť kontajner“. Uistite sa, že ste zadali celú cestu a pridali dynamický obsah do zátvoriek. Úvodzovky sú povinné. Napríklad zadajte **„/msdyn\_projectbuckets(PRIDAŤ DYNAMICKÝ OBSAH)“**.
    - **msdyn\_start** – Dynamický obsah pre dátum začiatku. Napríklad zajtrajšok bude reprezentovaný ako **„addDays(utcNow(), 1)“**.
    - **msdyn\_scheduledstart** – Plánovaný dátum začiatku. Napríklad zajtrajšok bude reprezentovaný ako **„addDays(utcNow(), 1)“**.
    - **msdyn\_scheduleend** – Plánovaný dátum ukončenia. Vyberte budúci dátum. Napríklad špecifikujte **„addDays(utcNow(), 5)“**.
    - **msdyn\_LinkStatus** – Stav prepojenia. Napríklad zadajte **„192350000“**.

7. Pre pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response** v dialógovom okne **Dynamický obsah**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>Krok č. 13: Vytvorte priradenie zdrojov

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Vytvoriť priradenie**.
5. V poli **Názov akcie** vyberte **msdyn\_PssCreateV1**.
6. V poli **Entita** zadajte nasledujúce informácie o parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Pre pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response** v dialógovom okne **Dynamický obsah**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Krok 14: Zníženie hodnoty premennej

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **zníženie hodnoty premennej**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V poli **Názov** vyberte **počet úloh**.
4. V poli **Hodnota** zadajte **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>Krok 15: Premenovanie projektovej úlohy

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Premenovať projektovú úlohu**.
5. V poli **Názov akcie** vyberte **msdyn\_PssUpdateV1**.
6. V poli **Entita** zadajte nasledujúce informácie o parametri.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Pre pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response** v dialógovom okne **Dynamický obsah**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>Krok 16: Spustenie množiny operácií

1. V postupe vyberte možnosť **Nový krok**.
2. V dialógovom okne **Vyberte operáciu** zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na karte **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte tri bodky (**...**) a potom vyberte možnosť **Premenovať**.
4. Premenujte krok **Spustiť množinu operácií**.
5. V poli **Názov akcie** vyberte **msdyn\_ExecuteOperationSetV1**.
6. Pre pole **OperationSetId** vyberte **msdyn\_CreateOperationSetV1Response OperationSetId** v dialógovom okne **Dynamický obsah**.

## <a name="references"></a>Odkazy

- [Prehľad spôsobu integrácie postupov s Dataverse – Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu](schedule-api-preview.md)
- [Prehľad postupov v cloude – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Prehľad postupov zodpovedajúcich riešeniu – Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
