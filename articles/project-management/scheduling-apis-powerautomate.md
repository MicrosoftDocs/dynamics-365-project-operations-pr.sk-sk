---
title: Použitie rozhraní API plánovania projektov so službou Power Automate
description: Tento článok poskytuje vzorový tok, ktorý používa rozhrania API na plánovanie aplikácií.
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

Nasleduje úplný zoznam krokov, ktoré sú zdokumentované v toku vzorky v tomto článku:

1. [Vytvor PowerApps spúšťač](#1)
2. [Vytvoriť projekt](#2)
3. [Inicializujte premennú pre člena tímu](#3)
4. [Vytvorte všeobecného člena tímu](#4)
5. [Vytvorte súpravu operácií](#5)
6. [Vytvorte skupinu projektov](#6)
7. [Inicializujte premennú pre stav prepojenia](#7)
8. [Inicializujte premennú pre počet úloh](#8)
9. [Inicializujte premennú pre ID projektovej úlohy](#9)
10. [Urobte do](#10)
11. [Nastavte projektovú úlohu](#11)
12. [Vytvorte projektovú úlohu](#12)
13. [Vytvorte priradenie zdroja](#13)
14. [Znížte premennú](#14)
15. [Premenujte projektovú úlohu](#15)
16. [Spustite sadu operácií](#16)

## <a name="assumptions"></a>Predpoklady

Tento článok predpokladá, že máte základné znalosti o Dataverse platforma, cloud toky a Project Schedule Application Programming Interface (API). Viac informácií nájdete na [Referencie](#references) časť ďalej v tomto článku.

## <a name="create-a-flow"></a>Vytvorte postup

### <a name="select-an-environment"></a>Vyberte prostredie

Môžete vytvoriť Power Automate prúdenie vo vašom prostredí.

1. Ísť do<https://flow.microsoft.com> a na prihlásenie použite svoje poverenia správcu.
2. V pravom hornom rohu vyberte **Prostredia**.
3. V zozname vyberte prostredie, kde Dynamics 365 Project Operations je nainštalovaný.

### <a name="create-a-solution"></a>Vytvorenie riešenia

Podľa týchto krokov vytvorte a [tok uvedomujúci si riešenie](/power-automate/overview-solution-flows). Vytvorením toku so zreteľom na riešenie môžete tok jednoduchšie exportovať a použiť ho neskôr.

1. Na navigačnej table vyberte **Riešenia**.
2. Na **Riešenia** stránku, vyberte **Nové riešenie**.
3. V **Nové riešenie** dialógovom okne nastavte požadované polia a potom vyberte **Vytvorte**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> Krok 1: Vytvorte a PowerApps spúšťač

1. Na **Riešenia** stránku, vyberte riešenie, ktoré ste vytvorili, a potom vyberte **Nový**.
2. Na ľavej table vyberte **Cloud toky** \> **automatizácia** \> **Cloud flow** \> **Okamžité**.
3. V **Názov toku** pole, zadajte **Naplánujte tok ukážky rozhrania API**.
4. V **Vyberte spôsob spustenia tohto toku** zoznam, vyberte **Power Apps**. Keď vytvoríte a Power Apps spúšť, logika je na vás ako autorovi. V tomto článku ponechajte vstupné parametre prázdne na účely testovania.
5. Vyberte položku **Vytvoriť**.

## <a name="step-2-create-a-project"></a><a id="2"></a>Krok 2: Vytvorenie projektu

Ak chcete vytvoriť vzorový projekt, postupujte podľa týchto krokov.

1. V toku, ktorý ste vytvorili, vyberte **Nový krok**.

    ![Pridáva sa nový krok.](media/newstep.png)

2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.

    ![Výber operácie.](media/chooseactiontab.png)

3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.

![Premenovanie kroku.](media/renamestep.png)

4. Premenujte krok **Vytvoriť projekt**.
5. V **Názov akcie** pole, vyberte **msdyn\_ CreateProjectV1**.
6. Pod **msdyn\_ predmet** pole, vyberte **Pridajte dynamický obsah**.
7. Na **Výraz** do poľa funkcie zadajte **Názov projektu - utcNow()**.
8. Vyberte položku **OK**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> Krok 3: Inicializujte premennú pre člena tímu

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **inicializovať premennú**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Člen init tímu**.
5. V **názov** pole, zadajte **TeamMemberAction**.
6. V **Typ** pole, vyberte **Reťazec**.
7. V **Hodnota** pole, zadajte **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> Krok 4: Vytvorte všeobecného člena tímu

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Vytvoriť člena tímu**.
5. Pre **Názov akcie** pole, vyberte **TeamMemberAction** v **Dynamický obsah** dialógové okno.
6. V **Akčné parametre** zadajte nasledujúce informácie o parametroch.

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

    - **\@\@ odata.typ** – Názov entity. Napríklad zadajte **"Microsoft.Dynamics.CRM.msdyn\_ projektová skupina"**.
    - **msdyn\_ projektteamid** – Primárny kľúč ID projektového tímu. Hodnota je výraz globálneho jedinečného identifikátora (GUID).   ID sa generuje z karty výraz.

    - **msdyn\_ projektu\@ odata.viazať** – ID projektu vlastníka projektu. Hodnota bude dynamický obsah, ktorý pochádza z odpovede kroku „Vytvoriť projekt“. Uistite sa, že ste zadali celú cestu a pridali dynamický obsah do zátvoriek. Úvodzovky sú povinné. Napríklad zadajte **"/msdyn\_ projekty (PRIDAŤ DYNAMICKÝ OBSAH)“**.
    - **msdyn\_ názov** – Meno člena tímu. Napríklad zadajte **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> Krok 5: Vytvorte súpravu operácií

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Vytvorte súpravu operácií**.
5. V **Názov akcie** vyberte pole **msdyn\_ CreateOperationSetV1** Dataverse vlastná akcia.
6. V **Popis** pole, zadajte **ScheduleAPIDemoOperationSet**.
7. V **Projekt** pole, zadajte **/msdyn\_ projekty(**.
8. V **Dynamický obsah** dialógovom okne vyberte **msdyn\_ CreateProjectV1Response ProjectId**.
9. V **Projekt** pole, zadajte **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> Krok 6: Vytvorte skupinu projektov

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **pridať nový riadok**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Vytvoriť vedierko**.
5. V **Názov tabuľky** pole, vyberte **Project Buckets**.
6. V **názov** pole, zadajte **ScheduleAPIDemoBucket1**.
7. Pre **Projekt** pole, vyberte **msdyn\_ CreateProjectV1Response ProjectId** v **Dynamický obsah** dialógové okno.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> Krok 7: Inicializujte premennú pre stav prepojenia

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **inicializovať premennú**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Stav prepojenia**.
5. V **názov** pole, zadajte **stav prepojenia**.
6. V **Typ** pole, vyberte **Celé číslo**.
7. V **Hodnota** pole, zadajte **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> Krok 8: Inicializujte premennú pre počet úloh

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **inicializovať premennú**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Init Počet úloh**.
5. V **názov** pole, zadajte **počet úloh**.
6. V **Typ** pole, vyberte **Celé číslo**.
7. V **Hodnota** pole, zadajte **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> Krok 9: Inicializujte premennú pre ID projektovej úlohy

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **inicializovať premennú**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Spustite ProjectTaskID**.
5. V **názov** pole, zadajte **počet úloh**.
6. V **Typ** pole, vyberte **Reťazec**.
7. Pre **Hodnota** pole, zadajte **guid()** v nástroji na tvorbu výrazov.

## <a name="step-10-do-until"></a><a id="10"></a> Krok 10: Urobte do

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **robiť do**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. Nastavte prvú hodnotu v podmienenom príkaze na **počet úloh** premenná z **Dynamický obsah** dialógové okno.
4. Nastavte podmienku na **menej ako rovné**.
5. Nastavte druhú hodnotu v podmienenom príkaze na **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> Krok 11: Nastavte projektovú úlohu

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **nastaviť premennú**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V novom kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Nastaviť úlohu projektu**.
5. V **názov** pole, vyberte **msdyn\_ projecttaskid**.
6. Pre **Hodnota** pole, zadajte **guid()** v nástroji na tvorbu výrazov.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> Krok 12: Vytvorte projektovú úlohu

Podľa týchto krokov vytvorte projektovú úlohu, ktorá má jedinečné ID, ktoré patrí aktuálnemu projektu a skupine projektov, ktorú ste vytvorili.

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Vytvorenie projektovej úlohy**.
5. V **Názov akcie** pole, vyberte **msdyn\_ PssCreateV1**.
6. V **Entita** zadajte nasledujúce informácie o parametroch.

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

    - **\@\@ odata.typ** – Názov entity. Napríklad zadajte **"Microsoft.Dynamics.CRM.msdyn\_ projektová úloha"**.
    - **msdyn\_ projecttaskid** – Jedinečné ID úlohy. Hodnota by mala byť nastavená na dynamickú premennú z **msdyn\_ projecttaskid**.
    - **msdyn\_ projektu\@ odata.viazať** – ID projektu vlastníka projektu. Hodnota bude dynamický obsah, ktorý pochádza z odpovede kroku „Vytvoriť projekt“. Uistite sa, že ste zadali celú cestu a pridali dynamický obsah do zátvoriek. Úvodzovky sú povinné. Napríklad zadajte **"/msdyn\_ projekty (PRIDAŤ DYNAMICKÝ OBSAH)“**.
    - **msdyn\_ predmet** – Ľubovoľný názov úlohy.
    - **msdyn\_ projectbucket\@ odata.viazať** – Skupina projektu, ktorá obsahuje úlohy. Hodnota bude dynamický obsah, ktorý pochádza z odozvy kroku „Vytvoriť vedro“. Uistite sa, že ste zadali celú cestu a pridali dynamický obsah do zátvoriek. Úvodzovky sú povinné. Napríklad zadajte **"/msdyn\_ projectbuckets (PRIDAŤ DYNAMICKÝ OBSAH)"**.
    - **msdyn\_ začať** – Dynamický obsah pre dátum začiatku. Napríklad zajtrajšok bude reprezentovaný ako **"addDays(utcNow(), 1)"**.
    - **msdyn\_ plánovaný štart** – Plánovaný dátum začiatku. Napríklad zajtrajšok bude reprezentovaný ako **"addDays(utcNow(), 1)"**.
    - **msdyn\_ harmonogram** – Plánovaný dátum ukončenia. Vyberte dátum v budúcnosti. Napríklad špecifikujte **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – Stav prepojenia. Napríklad zadajte **"192350000"**.

7. Pre **OperationSetId** pole, vyberte **msdyn\_ CreateOperationSetV1Response** v **Dynamický obsah** dialógové okno.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> Krok 13: Vytvorte priradenie zdroja

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Vytvoriť zadanie**.
5. V **Názov akcie** pole, vyberte **msdyn\_ PssCreateV1**.
6. V **Entita** zadajte nasledujúce informácie o parametroch.

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

7. Pre **OperationSetId** pole, vyberte **msdyn\_ CreateOperationSetV1Response** v **Dynamický obsah** dialógové okno.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> Krok 14: Znížte premennú

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **dekrementovať premennú**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V **názov** pole, vyberte **počet úloh**.
4. V **Hodnota** pole, zadajte **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> Krok 15: Premenujte úlohu projektu

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Premenovať úlohu projektu**.
5. V **Názov akcie** pole, vyberte **msdyn\_ PssUpdateV1**.
6. V **Entita** zadajte nasledujúce informácie o parametroch.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Pre **OperationSetId** pole, vyberte **msdyn\_ CreateOperationSetV1Response** v **Dynamický obsah** dialógové okno.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> Krok 16: Spustite sadu operácií

1. V toku vyberte **Nový krok**.
2. V **Vyberte operáciu** v dialógovom okne zadajte do vyhľadávacieho poľa **vykonať neviazanú akciu**. Potom na **Akcie** vyberte operáciu v zozname výsledkov.
3. V kroku vyberte elipsu (**...**) a potom vyberte **Premenovať**.
4. Premenujte krok **Vykonajte sadu operácií**.
5. V **Názov akcie** pole, vyberte **msdyn\_ ExecuteOperationSetV1**.
6. Pre **OperationSetId** pole, vyberte **msdyn\_ CreateOperationSetV1Response OperationSetId** v **Obsah dynamiky** dialógové okno.

## <a name="references"></a>Odkazy

- [Prehľad toho, ako integrovať toky s Dataverse -Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu](schedule-api-preview.md)
- [Prehľad cloudových tokov -Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Prehľad tokov zameraných na riešenie -Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
