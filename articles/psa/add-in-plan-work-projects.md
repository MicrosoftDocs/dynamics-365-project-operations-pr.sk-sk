---
title: Naplánujte si svoju prácu v programe Microsoft Project pomocou doplnku Project Service
description: Táto téma poskytuje informácie o tom ako používať doplnok Microsoft Project add-in pre službu Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 01/07/2021
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
ms.openlocfilehash: 87387ff870a7ef3ed0689f4ae38daad8cf220b46
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145962"
---
# <a name="plan-your-work-in-microsoft-project-with-the-project-service-add-in"></a>Naplánujte si svoju prácu v programe Microsoft Project pomocou doplnku Project Service

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3x](../includes/cc-applies-to-psa-app-3x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vám zjednodušuje plánovanie projektov vrátane odhadov. Môžete si definovať prácu tak, aby náklady, úsilie a predajná hodnota boli jasné pri odoslaní finálneho návrhu.  

Môžete nainštalovať [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] a naplánovať si svoju prácu v známom prostredí [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Použite robustné možnosti plánovania a správy [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a následne si aktualizujte svoj plán projektu v Project Service Automation.  

> [!IMPORTANT]
> - Na použitie správy dokumentov SharePoint na ukladanie vašich súborov [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pre projekty [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], váš správca [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vám bude musieť zapnúť funkciu správy dokumentov. 
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je kompatibilné len s [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Stiahnite a nainštalujte si doplnok  
 Pripravte si svoje prihlasovacie informácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Tieto informácie budete potrebovať na pripojenie z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  V stredisku pre prevzatie softvéru si prevezmite doplnok pre vašu podporovanú verziu programu Project Service buď [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) alebo [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Vyberte odkaz na stiahnutie.  

3.  Po dokončení sťahovania vyberte možnosť **Áno**, čím doplnok nainštalujete.  

## <a name="configure-the-add-in"></a>Nakonfigurujte prídavok  

1. Otvorte program [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a vyberte kartu **Project Service**.  

2. Vyberte možnosť **Pripojiť**.  

3. Zadajte vaše prihlasovacie údaje a vyberte **Prihlásiť**.  

   Teraz môžete začať s používaním prídavku.  

## <a name="read-from-a-template"></a>Čítanie zo šablóny  
 Čítanie zo šablóny, ktorú ste si vytvorili v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a skopírovali ich do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] na začatie projektového plánovania. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Vytvorenie šablóny projektu (Project Service Automation)](../psa/create-project-template.md)  

1.  Na karte **Project Service** vyberte možnosť **Čítať** > **Šablóna Project Service Automation**.  

2.  Zo zoznamu si vyberte šablónu a potom vyberte možnosť **Otvoriť**.  

    > [!NOTE]
    >  Predvolene sa úlohy skopírované zo šablóny do projektu nastavia ako manuálne plánované.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Priradiť [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] role k projektovým zdrojom  

1.  Otvorte projekt a vyberte pás s nástrojmi **Úloha**.  

2. Vyberte ponuku **Ganttovho grafu** a potom vyberte **Hárok zdrojov**.  

3. V hárku zdrojov vyberte rozbaľovaciu ponuku **Rola prostriedku Project Service** a vyberte rolu Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Zaplňte svoj projekt zdrojmi  

1.  Na karte Project Service vyberte riadok a vyberte **Vyhľadať zdroje**.  

2.  Na obrazovke **Rezervovať zdroj** vyberte zdroj, ktorý chcete použiť pre projekt.  

3.  Stlačte **Rezervovať** a potom vyberte **OK**.  

## <a name="publish-your-project"></a>Zverejnite svoj projekt  
Pri plánovaní projektu je ďalším krokom importovanie a zverejnenie projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt sa naimportuje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Použije sa projekt oceňovania a vytvárania tímov. Otvorte projekt v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a zistite, že tím, projektové odhady a štruktúra rozdelenia práce boli vytvorené. Nasledujúca tabuľka ukazuje, kde nájsť výsledky.


|              Microsoft Project                                                           |                      Project Service Automation                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganttov graf**   | Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Štruktúra rozdelenia práce**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Hárok zdrojov** |   Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Členovia projektového tímu**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Použiť využitie**    |    Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Odhady projektu**.     |

**Importovať a publikovať svoj projekt**  
1. Na karte **Project Service** prejdite na možnosť **Publikovať** > **Nový projekt Project Service Automation**.  

2. V dialógovom okne **Publikovanie v novom projekte v rámci služby Project Service** zadajte **Názov projektu** a vyberte **Zákazník**.  

3. Môžete tiež vybrať **Prepojiť plán projektu so systémom Project Service Automation** na prepojenie súboru projektu s automatizáciou Project Service.  

4. Stlačte možnosť **Publikovať**.  

   Prepojenie súboru projektu na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] urobí súbor projektu hlavným a nastaví štruktúru rozdelenia práce v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iba na čítanie.  S cieľom vykonať zmeny plánu projektu, budete ich musieť urobiť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a zverejniť ich ako aktualizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Upraviť projekt, ktorý ste importovali  
 Na zmenu plánu projektu naimportovaného v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] máte dve možnosti:  

- Otvorte hlavný súbor a upravte ho v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Zrušte prepojenie súboru a upravte ho priamo v Project Service. V predvolenom nastavení je projekt, ktorý sa odovzdáva z aplikácie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], zamknutý a možno ho upravovať len v projekte. Na úpravu súboru v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] musí byť zrušené jeho prepojenie.  

### <a name="edit-in-pn_microsoft_project"></a>Upraviť v aplikácii [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. V hlavnej ponuke prejdite na **Project Service** > **Projekty**.  

2. Pre zoznam projektov otvorte projekt, ktorý ste vytvorili v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Vyberte **Otvoriť v MS Project** z pása s nástrojmi. Týmto sa otvorí prepojený hlavný súbor v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Zrušte prepojenie súboru a upravte ho v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. V hlavnej ponuke prejdite na **Project Service** > **Projekty**.  

2. Pre zoznam projektov otvorte projekt, ktorý ste vytvorili v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Vyberte **Zrušiť prepojenie z MS Project** z pása s nástrojmi.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Odovzdanie súboru Projekt do SharePoint alebo Office Groups  
 Môžete odovzdať súbor Projekt SharePoint a nájsť ho pod Súvisiace dokumenty pre váš [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  Váš správca vám musí nastaviť správu dokumentov SharePoint a tiež povoliť entitu Project. 

 Môžete tiež nahrať súbor projektu do [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], ak máte nastavené Office skupiny.

### <a name="upload-a-file-for-sharepoint"></a>Nahrajte súbor pre SharePoint  

1. V hlavnej ponuke prejdite na **Project Service** > **Odovzdať**.  

2. Zvoľte možnosť **Do projektových dokumentov Project Service Automation**.  

3. V dialógovom okne **Povoliť otvorenie v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** vyberte možnosť **Áno** alebo **Nie**.  

   - Ak vyberiete **Áno**, budete môcť vybrať **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v Project Service Automation, spustiť [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načítať súbor projektu zo SharePoint knižnice dokumentov.  

   - Ak vyberiete **Nie**, odkaz na **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovať.  

4. Súbor programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] nájdete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod položkou **Dokumenty** pre konkrétny projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Nahrajte súbor pre skupiny Office  

1. V hlavnej ponuke prejdite na **Project Service** > **Odovzdať**.  

2. Zvoľte možnosť **Do projektových dokumentov Project Service Automation**.  

3. V dialógovom okne **Povoliť otvorenie v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** vyberte možnosť **Áno** alebo **Nie**.  

   - Ak vyberiete **Áno**, budete môcť vybrať **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v Project Service Automation, spustiť [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načítať súbor projektu zo SharePoint knižnice dokumentov.  

   - Ak vyberiete **Nie**, odkaz na **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovať.  

4. Súbor programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] nájdete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod položkou **Dokumenty** pre konkrétny projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publikovať svoj projekt ako šablónu  
 Môžete uložiť projekt a znova ho uložíte ako šablónu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Projektové šablóny sú opakovane projektové plány v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Viac informácií nájdete na [Vytvorenie šablóny projektu (Project Service Automation)](../psa/create-project-template.md). 

1. Na karte **Project Service** prejdite na možnosť **Publikovať** > **Nová šablóna projektu Project Service Automation**.  

2. V dialógovom okne **Publikovanie v novom projekte v rámci šablóny Project Service** zadajte **názov šablóny projektu**.  

3. Môžete tiež vybrať **Prepojiť plán projektu so systémom Project Service Automation** na prepojenie súboru projektu s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Stlačte možnosť **Publikovať**.  

Prepojenie súboru projektu na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] robí projekt súboru kapitána a nastaví štruktúry rozdelenia práce v šablóne[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iba na čítanie.  S cieľom vykonať zmeny plánu projektu, budete ich musieť urobiť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a zverejniť ich ako aktualizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

## <a name="read-a-resource-loaded-schedule"></a>Prečítajte si plán načítaný zdrojom

Pri čítaní projektu z Project Service Automation sa kalendár zdroja nesynchronizuje s počítačovým klientom. Ak existujú rozdiely v trvaní úlohy, jej úsilí alebo konci, je to pravdepodobne preto, lebo zdroje a klient pre počítač nemajú pre projekt rovnaký kalendár šablón pracovnej doby.


## <a name="data-synchronization"></a>Synchronizácia údajov
Tabuľky v tejto časti poskytujú informácie o synchronizácii údajov entít medzi Project Service Automation a doplnkom Microsoft Project pre počítač.

### <a name="project-task-entity-table"></a>Tabuľka entít projektových úloh
V nasledujúcej tabuľke je uvedené, ako sa synchronizujú údaje entity projektovej úlohy medzi Project Service Automation a doplnkom Microsoft Project pre počítač.

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Projektová úloha | Termín | Synchronizované | Nesynchronizované |
| Projektová úloha | Odhadované úsilie | Synchronizované | Nesynchronizované |
| Projektová úloha | ID klienta MS Project | Synchronizované | Nesynchronizované |
| Projektová úloha | Nadradená úloha | Synchronizované | Nesynchronizované |
| Projektová úloha | Project | Synchronizované | Nesynchronizované |
| Projektová úloha | Projektová úloha | Synchronizované | Nesynchronizované |
| Projektová úloha | Názov projektovej úlohy | Synchronizované | Nesynchronizované |
| Projektová úloha | Zdrojová jednotka (zastarané vo verzii 3.0) | Synchronizované | Nesynchronizované |
| Projektová úloha | Plánované trvanie | Synchronizované | Nesynchronizované |
| Projektová úloha | Počiatočný dátum | Synchronizované | Nesynchronizované |
| Projektová úloha | ID štruktúry WBS | Synchronizované | Nesynchronizované |

### <a name="team-member-entity-table"></a>Tabuľka entít člena tímu
V nasledujúcej tabuľke je uvedené, ako sa synchronizujú údaje entity člena tímu medzi Project Service Automation a doplnkom Micros

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Člen tímu | ID klienta MS Project | Synchronizované | Nesynchronizované |
| Člen tímu | Názov pozície | Synchronizované | Nesynchronizované |
| Člen tímu | projekt | Synchronizované | Synchronizované |
| Člen tímu | Projektový tím | Synchronizované | Synchronizované |
| Člen tímu | Zdrojová jednotka | Nesynchronizované | Synchronizované |
| Člen tímu | Rola | Nesynchronizované | Synchronizované |
| Člen tímu | Pracovná doba | Nesynchronizované | Nesynchronizované |

### <a name="resource-assignment-entity-table"></a>Tabuľka entít priradenia zdrojov
V nasledujúcej tabuľke je uvedené, ako sa synchronizujú údaje entity priradenia zdroja medzi Project Service Automation a doplnkom Micros

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Priradenie zdroja | Dátum Od | Synchronizované | Nesynchronizované |
| Priradenie zdroja | Hod. | Synchronizované | Nesynchronizované |
| Priradenie zdroja | ID klienta MS Project | Synchronizované | Nesynchronizované |
| Priradenie zdroja | Plánovaná práca | Synchronizované | Nesynchronizované |
| Priradenie zdroja | Project | Synchronizované | Nesynchronizované |
| Priradenie zdroja | Projektový tím | Synchronizované | Nesynchronizované |
| Priradenie zdroja | Priradenie zdroja | Synchronizované | Nesynchronizované |
| Priradenie zdroja | Úloha | Synchronizované | Nesynchronizované |
| Priradenie zdroja | Dátum Do | Synchronizované | Nesynchronizované |

### <a name="project-task-dependencies-entity-table"></a>Tabuľka entít závislostí projektových úloh
V nasledujúcej tabuľke je uvedené, ako sa synchronizujú údaje entity závislostí projektových úloh medzi Project Service Automation a doplnkom Micros

| **Entita** | **Pole** | **Microsoft Project do Project Service Automation** | **Project Service Automation do Microsoft Project** |
| --- | --- | --- | --- |
| Závislosti projektovej úlohy | Závislosť projektovej úlohy | Synchronizované | Nesynchronizované |
| Závislosti projektovej úlohy | Typ prepojenia | Synchronizované | Nesynchronizované |
| Závislosti projektovej úlohy | Úloha predchodcu | Synchronizované | Nesynchronizované |
| Závislosti projektovej úlohy | Project | Synchronizované | Nesynchronizované |
| Závislosti projektovej úlohy | Úloha následníka | Synchronizované | Nesynchronizované |

### <a name="additional-resources"></a>Ďalšie zdroje
 [Príručka projektového manažéra](../psa/project-manager-guide.md)
