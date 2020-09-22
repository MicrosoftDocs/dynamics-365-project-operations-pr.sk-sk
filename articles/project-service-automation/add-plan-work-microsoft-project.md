---
title: Použite doplnok Project Service na plánovanie práce v Microsoft Project | MicrosoftDocs
description: Táto téma poskytuje informácie o tom ako pridávať, konfigurovať a používať doplnok Microsoft Project add-in pre službu Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: Dynamics 365 Project Service Automation
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: efd589e0-8233-4abf-bf7e-5c1e83c4daea
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0ad503ff0c27f1543d15b60714c2be46b8487d18
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755549"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a>Použite doplnok Project Service Automation na plánovanie práce v Microsoft Project

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] vám zjednodušuje plánovanie projektov vrátane odhadov. Môžete si definovať prácu tak, aby náklady, úsilie a predajná hodnota boli jasné pri odoslaní finálneho návrhu.  

 Teraz môžete nainštalovať [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] a naplánovať si svoju prácu v známom prostredí [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]. Použite robustné možnosti plánovania a správy [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a následne si aktualizujte svoj plán projektu v Project Service Automation.  

> [!IMPORTANT]
> - Na použitie správy dokumentov SharePoint na ukladanie vašich súborov [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pre projekty [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], váš správca [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vám bude musieť zapnúť funkciu správy dokumentov. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Povolenie správy dokumentov lokality SharePoint pre konkrétne entity](../admin/enable-sharepoint-document-management-specific-entities.md)  
> - [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je kompatibilné len s [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.  

## <a name="download-and-install-the-add-in"></a>Stiahnite a nainštalujte si doplnok  
 Pripravte si svoje prihlasovacie informácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Tieto informácie budete potrebovať na pripojenie z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

1.  V stredisku pre prevzatie softvéru si prevezmite doplnok pre vašu podporovanú verziu programu Project Service buď [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) alebo [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).  

2.  Kliknite na odkaz na stiahnutie.  

3.  Po dokončení sťahovania kliknite na možnosť **Áno**, čím doplnok nainštalujete.  

## <a name="configure-the-add-in"></a>Nakonfigurujte prídavok  

1. Otvorte program [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a kliknite na kartu **Project Service**.  

2. Kliknite na tlačidlo **Pripojiť**.  

3. Zadajte vaše prihlasovacie údaje a kliknite na tlačidlo **prihlásiť**.  

   Teraz môžete začať s používaním prídavku.  

## <a name="read-from-a-template"></a>Čítanie zo šablóny  
 Čítanie zo šablóny, ktorú ste si vytvorili v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a skopírovali ich do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] na začatie projektového plánovania. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Vytvorenie šablóny projektu (Project Service Automation)](../project-service/create-project-template.md)  

1.  Na karte **Project Service** kliknite na možnosť **Čítať** > **Šablóna Project Service Automation**.  

2.  Zo zoznamu si vyberte šablónu a potom kliknite na možnosť **Otvoriť**.  

    > [!NOTE]
    >  Predvolene sa úlohy skopírované zo šablóny do projektu nastavia ako manuálne plánované.  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a>Priradiť [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] role k projektovým zdrojom  

1.  Otvorte projekt a kliknite na stuhu **Úloha**.  

2.  Kliknite na ponuku **Ganttovho grafu** a potom vyberte **Hárok zdrojov**.  

3.  V hárku zdrojov kliknite na rozbaľovaciu ponuku **Rola prostriedku Project Service** a vyberte rolu Project Service Automation.  

## <a name="staff-your-project-with-resources"></a>Zaplňte svoj projekt zdrojmi  

1.  Na karte Project Service vyberte riadok a kliknite na tlačidlo **Vyhľadať zdroje**.  

2.  Na obrazovke **Rezervovať zdroj** vyberte zdroj, ktorý chcete použiť pre projekt.  

3.  Kliknite na tlačidlo **Rezervovať** a potom kliknite na položku **OK**.  

## <a name="publish-your-project"></a>Zverejnite svoj projekt  
Pri plánovaní projektu je ďalším krokom importovanie a zverejnenie projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

Projekt sa naimportuje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. Použije sa projekt oceňovania a vytvárania tímov. Otvorte projekt v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a zistite, že tím, projektové odhady a štruktúra rozdelenia práce boli vytvorené, Nasledujúca tabuľka ukazuje, kde nájsť výsledky:


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Ganttov graf**   | Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Štruktúra rozdelenia práce**. |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Hárok zdrojov** |   Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Členovia projektového tímu**.   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] **Použiť využitie**    |    Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Odhady projektu**.     |

**Importovať a publikovať svoj projekt**  
1. Na karte **Project Service** kliknite na možnosť **Publikovať** > **Nový projekt Project Service Automation**.  

2. V dialógovom okne **Publikovanie v novom projekte v rámci služby Project Service** zadajte **názov projektu** a vyberte **zákazník**.  

3. Môžete tiež označiť **Prepojiť plán projektu so systémom Project Service Automation** ne prepojenie súboru projektu s automatizáciou Project Service.  

4. Kliknite na položku **Publikovať**.  

   Prepojenie súboru projektu na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] urobí súbor projektu hlavným a nastaví štruktúru rozdelenia práce v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iba na čítanie.  S cieľom vykonať zmeny plánu projektu, budete ich musieť urobiť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a zverejniť ich ako aktualizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="edit-a-project-thats-been-imported"></a>Upraviť projekt, ktorý ste importovali  
 Na zmenu plánu projektu naimportovaného v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] máte dve možnosti:  

- Otvorte hlavný súbor a upravte ho v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

- Zrušte prepojenie súboru a upravte ho priamo v Project Service. V predvolenom nastavení je projekt, ktorý sa odovzdáva z aplikácie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], zamknutý a možno ho upravovať len v projekte. Na úpravu súboru v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] musí byť zrušené jeho prepojenie.  

### <a name="edit-in-pn_microsoft_project"></a>Upraviť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]  

1. Z hlavného menu kliknite na tlačidlo **Project Service** > **Projekty**.  

2. Pre zoznam projektov otvorte projekt vytvorený v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Kliknite na **Otvoriť v MS Project** z pása s nástrojmi. Týmto sa otvorí prepojený hlavný súbor v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a>Zrušte prepojenie súboru a upravte ho v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service  

1. Z hlavného menu kliknite na tlačidlo **Project Service** > **Projekty**.  

2. Pre zoznam projektov otvorte projekt vytvorený v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].  

3. Kliknite na **Zrušiť prepojenie z MS Project** z pása s nástrojmi.  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a>Odovzdanie súboru Projekt do SharePoint alebo Office Groups  
 Môžete odovzdať súbor Projekt SharePoint a nájsť ho pod Súvisiace dokumenty pre váš [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.  Váš správca vám musí nastaviť správu dokumentov SharePoint a tiež povoliť entitu Project. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Nastavenie integrácie služby SharePoint](../admin/set-up-sharepoint-integration.md)  

 Môžete tiež nahrať súbor projektu do [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], ak máte nastavené Office skupiny. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Spolupracujte s kolegami pomocou skupín Office 365 Groups](../basics/collaborate-with-colleagues-using-office-365-groups.md)  

### <a name="upload-a-file-for-sharepoint"></a>Nahrajte súbor pre SharePoint  

1. Z hlavného menu kliknite na tlačidlo **Project Service** > **Nahrať**.  

2. Zvoľte možnosť **Do projektových dokumentov Project Service Automation**.  

3. V dialógovom okne **Povoliť otvorenie v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** zvoľte možnosť **Áno** alebo **Nie**.  

   - Keď kliknete na **Áno**, budete môcť vybrať tlačidlo **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v Project Service Automation, spustiť [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načítať súbor projektu zo SharePoint knižnice dokumentov.  

   - Keď kliknete na **Nie**, prepojenie na tlačidlo **Otvoriť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovať.  

4. Súbor programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] nájdete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod položkou **Dokumenty** pre konkrétny projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

### <a name="upload-a-file-for-office-groups"></a>Nahrajte súbor pre skupiny Office  

1. Z hlavného menu kliknite na tlačidlo **Project Service** > **Nahrať**.  

2. Zvoľte možnosť **Do projektových dokumentov Project Service Automation**.  

3. V dialógovom okne **Povoliť otvorenie v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** zvoľte možnosť **Áno** alebo **Nie**.  

   - Keď kliknete na **Áno**, budete môcť vybrať tlačidlo **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v Project Service Automation, spustiť [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načítať súbor projektu z knižnice dokumentov SharePoint.  

   - Keď kliknete na **Nie**, prepojenie na tlačidlo **Otvoriť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovať.  

4. Súbor programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] nájdete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod položkou **Dokumenty** pre konkrétny projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

## <a name="publish--your-project-as-a-template"></a>Publikovať svoj projekt ako šablónu  
 Môžete uložiť projekt a znova ho uložíte ako šablónu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  Projektové šablóny sú opakovane projektové plány v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]. [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] [Vytvorenie šablóny projektu (Project Service Automation)](../project-service/create-project-template.md)  

1. Na karte **Project Service** kliknite na možnosť **Publikovať** > **Nový projekt šablóny Project Service Automation**.  

2. V dialógovom okne **Publikovanie v novom projekte v rámci šablóny Project Service** zadajte **názov šablóny projektu**.  

3. Môžete tiež označiť **Prepojiť plán projektu so systémom Project Service Automation** na prepojenie súboru projektu s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].  

4. Kliknite na položku **Publikovať**.  

Prepojenie súboru projektu na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] robí projekt súboru kapitána a nastaví štruktúry rozdelenia práce v šablóne[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iba na čítanie.  S cieľom vykonať zmeny plánu projektu, budete ich musieť urobiť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a zverejniť ich ako aktualizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].

### <a name="see-also"></a>Pozrite si tiež:  
 [Príručka projektového manažéra](../project-service/project-manager-guide.md)
