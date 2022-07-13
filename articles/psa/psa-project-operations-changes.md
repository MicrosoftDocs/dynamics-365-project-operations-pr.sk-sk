---
title: Zmeny funkcií medzi aplikáciami Project Service Automation a Project Operations
description: Tento článok poskytuje prehľad zmien funkcií z Project Service Automation na Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925369"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Zmeny funkcií medzi aplikáciami Project Service Automation a Project Operations

Aktualizácia z Dynamics 365 Project Service Automation do Dynamics 365 Project Operations Lite bude dodaný v troch fázach. Tento článok poskytuje informácie o hlavných zmenách, ktoré môžete očakávať po dokončení inovácie.

| Inovovať doručenie | Fáza 1 <br>(január 2022) | 2. fáza <br>(Vlna apríla 2022) | 3. fáza  |
|------------------|------------------------|---------------------------|---------------------------|
| Žiadna závislosť od štruktúry rozpisu prác (WBS) pre projekty. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS je súčasťou aktuálne podporovaných limitov projektových operácií. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS mimo aktuálne podporovaných limitov Project Operations, vrátane podpory pre desktopového klienta Project. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektový manažment

Najvýraznejšie zmeny v používateľskej skúsenosti budú v oblasti plánovania projektov. Project Operations prijíma novú modernú skúsenosť so správou štruktúry rozpisu práce (WBS) využitím možností plánovania, ktoré poskytuje [Projekt pre web](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Rozdiely v plánovaní

Nasledujúca tabuľka sumarizuje rozdiely v plánovaní medzi Project Service Automation a Project Operations.

|  Plánuje sa     |   Project Operations   |   PSA   |
|-----------------|------------------------|---------|
| Projektové šablóny – Schopnosť definovať a aplikovať projektové šablóny pri vytváraní projektu  |  &nbsp;    | :heavy_check_mark: |
| Integrácia štruktúry rozdelenia práce na projekte (WBS) s klientom na pracovnej ploche   |    &nbsp;  | :heavy_check_mark: |
| Obmedzenia – Začať najskôr, skončiť najneskôr  | :heavy_check_mark: |   &nbsp;  |
| Míľniky – Úlohy s nulovým trvaním   | :heavy_check_mark:  |  &nbsp;  |
| Úlohy riadené zdrojmi budú rešpektovať dostupnosť pridelených zdrojov   | :heavy_check_mark: |  &nbsp;    |
| Úpravy v časovom rozvrhu – Upravujte plány a pracujte každý deň   |   &nbsp;  | :heavy_check_mark: |
| Automatické/manuálne plánovanie – použite nástroj na plánovanie projektu na automatické alebo manuálne plánovanie úloh |  &nbsp; | :heavy_check_mark:  |
| Upravujte veľké projekty priamo v používateľskom rozhraní: Veľkosť plánov, ktoré je možné upravovať, nie je obmedzená  | Limit 500 úloh  | :heavy_check_mark:       |
| Percento dokončenia – Označte priebeh úlohy   | :heavy_check_mark:  |  &nbsp;  |
| [Režimy plánovania projektu](../project-management/scheduling-modes.md) - Definujte projekt ako fixné jednotky, fixné úsilie alebo fixné trvanie | :heavy_check_mark: | &nbsp; |
| Časová os – vytvorte a prispôsobte zobrazenie časovej osi na vizualizáciu podrobností plánu a komunikáciu so zainteresovanými stranami. | :heavy_check_mark:  | &nbsp; |
| Úlohy riadené úsilím – Podpora nástroja na plánovanie pre plánovanie úlohy podľa úsilia  | :heavy_check_mark:  | &nbsp; |
| **Informácie o úlohe** dialógové okno – uložte podrobnosti o úlohe pomocou dialógového okna | :heavy_check_mark:  |  &nbsp;  |
| Drag and drop – Úlohy vyberte viackrát a upravte ich pozíciu na WBS | :heavy_check_mark: | &nbsp;  |
| Flexibilné trvalé zobrazenia – Definujte podrobnejšie zobrazenia atribútov úloh   | :heavy_check_mark:  | &nbsp; |
| Triediť a filtrovať WBS  | :heavy_check_mark:  | &nbsp; |
| Zobrazenie tabúľ pre dodanie projektu bez vodopádu  | :heavy_check_mark:   | &nbsp; |
| Zobrazenie časovej osi – Interaktívny Ganttov diagram používaný na vizualizáciu a úpravu WBS   | :heavy_check_mark:  | &nbsp; |
| Klávesové skratky – použite klávesové skratky na bežné operácie, ako je odsadenie alebo vloženie  | :heavy_check_mark:  |  &nbsp; |
| Viacúrovňové vrátenie – vykonajte analýzu typu „čo keby“, aby ste plne porozumeli dopadu zmien, a to zvrátením a opätovným použitím celej skupiny operácií | :heavy_check_mark: | &nbsp; |
| Vystrihnúť/Kopírovať/Vložiť – Spolupracujte na vývoji plánu kopírovaním a vkladaním podrobností plánu medzi aplikáciami  | :heavy_check_mark: | &nbsp; |
| Kontrolné zoznamy úloh – Pridajte k úlohe až 20 položiek kontrolného zoznamu   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Plánovanie projektu

The **Projekt** Stránka Project Operations má značný počet rozdielov v porovnaní s **Projekt** na stránke Project Service Automation.

Nasledujúce akcie boli odstránené z **projekty** stránku v rámci inovácie fázy 1:

  - **Otvoriť v programe MS Project**
  - **Vytvoriť šablónu**
  - **Zrušiť prepojenie s programom MS Project**

The **Projekt** Stránka Project Operations obsahuje nasledujúce nové karty.

- **Odhady materiálov**
- **Nastavenie fakturácie úloh**

The **Postavenie** karta bola odstránená a **Postavenie** pole je teraz na **Zhrnutie** s režimom plánovania projektu.

   ![Aktualizácie na stránke projektu.](media/projectform.png)

The **Rozvrh** karta bola premenovaná na **Úloha** a obsahuje nové možnosti plánovania projektov s Project for the Web.

   ![Nová karta Projektové úlohy.](media/tasktab.png)

## <a name="scheduling-modes"></a>Režimy plánovania

Projektové operácie zaviedli novú funkciu, [Režimy plánovania](../project-management/scheduling-modes.md). Všetky existujúce projekty Project Service Automation budú predvolene nastavené **Pevné trvanie** v projektových operáciách. Predvolenú hodnotu pre nové projekty však môžete spravovať tak, že prejdete na **nastavenie** > **Parametre** > **Parameter** > **Režim plánovania**.

   ![Nastavenia parametrov projektu pre režim plánovania.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Limity plánovania projektu

Project Operations sa spolieha na Project for the Web pre všetky operácie plánovania projektu. Project for the Web spravuje štruktúru rozpisu práce pomocou limitov v nasledujúcej tabuľke.

| **Pole**                                          | **Limit**             |
|----------------------------------------------------|-----------------------|
| Maximálny celkový počet úloh pre projekt                  | 500                   |
| Maximálne celkové trvanie pre projekt               | 3650 dní (10 rokov)  |
| Maximálny celkový počet zdrojov pre projekt              | 300                   |
| Maximálny celkový počet odkazov (len nasledovník) pre projekt | 600                   |
| Maximálny celkový počet vlastných polí pre projekt          | 10                    |
| Maximálna úroveň hierarchie                            | 10 úrovní             |
| Maximálny počet odkazov (nástupca + predchodca)            | 20                    |
| Maximálne trvanie listovej úlohy                      | 1250 dní             |
| Maximálne trvanie súhrnnej úlohy                 | 3650 dní (10 rokov)  |
| Maximálny počet zdrojov priradených k úlohe               | 20 zdrojov          |
| Podporovaný rozsah dátumov pre úlohu                    | 1/1/2000 – 12/31/2149 |
| Položky kontrolného zoznamu                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Rozšíriteľnosť a rozvoj projektového plánovania

Po inovácii na Project Operations musíte použiť Project Scheduling API na vykonávanie operácií vytvárania, aktualizácie a odstraňovania na nasledujúcich entitách:

|   Názov entity           |   Logický názov entity       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projektová úloha            | msdyn_projecttask           |
| Závislosť projektovej úlohy | msdyn_projecttaskdependency |
| Priradenie zdroja     | msdyn_resourceassignment    |
| Projektový kontajner          | msdyn_projectbucket         |
| Člen projektového tímu     | msdyn_projectteam           |

Ak v súčasnosti máte prispôsobenia, ktoré zahŕňajú tieto entity, pozrite si časť [Použite rozhrania API plánovania projektu na vykonávanie operácií s entitami plánovania](../project-management/schedule-api-preview.md) za usmernenie k implementácii.

## <a name="data-model-changes"></a>Zmeny dátového modelu

V rámci fázy inovácie 1 dochádza k zmenám dátového modelu. Tieto zmeny sú primárne terénne zmeny existujúcich subjektov. Vo fáze 1 entity, **msydn_project** a **msdyn_projectteam** sú refaktoring prispôsobení. 

> [!IMPORTANT]
> Po dokončení budúcich fáz inovácie sa táto časť aktualizuje o ďalšie entity.

Nasledujúce polia boli nahradené novými poliami.

|   Entity          |   Starý logický názov   |   Nový logický názov    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Boli pridané nasledujúce polia.

|   Entity          |   Logický názov                               |   Description |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Zobrazuje súhrn skutočných predajov poplatkov za projekt. Len na použitie v Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialcost                     | Zobrazuje súhrn skutočných nákladov na materiál v projekte. Len na použitie v Project Service Automation. |
| msdyn_project     | msdyn_actualmaterialsales                    | Zobrazuje súhrn skutočného predaja materiálu na projekte. Len na použitie v Project Service Automation. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Zmluvná linka spojená s týmto projektom. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Toto je interné systémové pole, ktoré sa používa **Kopírovať projekt** súvisiace s identifikátorom korelácie. Len na použitie v Project Service Automation. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Toto je interné systémové pole, ktoré sa používa na **Kopírovať projekt** súvisiace s Identifikátorom relácie. Len na použitie v Project Service Automation. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Posledná synchronizácia xRM Global Revision Token zo služby plánovania projektu. |
| msdyn_project     | msdyn_msprojectdocument                      | Dokument Microsoft Project, ktorý patrí k projektu. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Súhrn plánovaných nákladov na materiál na projekte. Len na použitie v Project Service Automation. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Súhrn plánovaného predaja materiálu na projekte. Len na použitie v Project Service Automation. |
| msdyn_project     | msdyn_program                                | Program, s ktorým súvisí tento projekt. |
| msdyn_project     | msdyn_quotelineproject                       | Riadok ponuky súvisiaci s týmto projektom. |
| msdyn_project     | msdyn_replaylogheader                        | Hlavička denníkov opakovania. |
| msdyn_project     | msdyn_schedulemode                           | Predvolený režim plánovania používaný pre všetky úlohy v projekte.  |
| msdyn_project     | msdyn_taskearlieststart                      | Najskorší dátum začatia akejkoľvek úlohy v projekte.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfrom projectteammember            | Člen projektového tímu, z ktorého bol tento člen projektového tímu skopírovaný. |
| msdyn_projectteam | msdyn_creategenericteammember withrequirement | Označuje, či sa má vytvoriť požiadavka na zdroj pre novovytvoreného všeobecného člena tímu.  |
| msdyn_projectteam | msdyn_deletestatus                           | Stav odstránenia člena tímu, ktorý sa má sledovať, či je službe plánovania projektu odoslaná žiadosť o vymazanie a či úspešne odošle odpoveď späť v rámci očakávaného časového okna. |
| msdyn_projectteam | msdyn_effortcompleted                        | Sleduje úsilie, ktoré člen tímu dosiahol na svojich úlohách. |
| msdyn_projectteam | msdyn_effortremaining                        | Sleduje úsilie, ktoré má člen tímu ešte dokončiť na svojich úlohách. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Čakacia doba od odoslania žiadosti o vymazanie do plánovacej služby projektu až do skutočného vymazania člena tímu dňa Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Časová pečiatka, ktorá sa má zaznamenať, keď sa žiadosť o vymazanie člena tímu odošle službe plánovania projektu. |
| msdyn_projectteam | msdyn_copiedfrom projectteammember            | Zobrazuje člena projektového tímu, z ktorého bol tento člen projektového tímu skopírovaný.  |

## <a name="project-templates"></a>Projektové šablóny

Project Operations neposkytuje podporu pre projektové šablóny. Väčšinu základných funkcií však môžete replikovať pomocou [Project Copy API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Podpora desktop add-in

Podpora pre doplnok Microsoft Project Desktop nebude k dispozícii v prvých 2 fázach inovácie. Vo fáze 3 budú môcť zákazníci, ktorí majú projekty väčšie ako aktuálne podporované limity Project for the Web, používať doplnok pre stolné počítače.

## <a name="editing-resource-assignment-contours"></a>Úprava obrysov priradenia zdrojov

Možnosť upravovať obrysy priradenia zdrojov bude k dispozícii, keď bude k dispozícii 2. fáza inovácie.

## <a name="billing-and-pricing"></a>Fakturácia a tvorba cien

V prevádzke projektu boli pridané nasledujúce nové funkcie. Tieto funkcie majú aditívny charakter a nemajú vplyv na dátový model Project Service Automation.

- [Evidovanie spotreby materiálu na projektoch a projektových úlohách](../material/material-usage-log.md)
- [Manažment subdodávok](../pro/subcontracting/managing-subcontracts-overview.md)
- [Zálohy a zmluvy založené na preddavkoch](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Stav neprekročenia zmluvy a overenia](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Účtovanie podľa úloh](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Zastarané komponenty

Nasledujúce tabuľky dokumentujú všetky zastarané polia, ktoré sa po inovácii presunú do riešenia zastaraných komponentov. Viac informácií a odkaz na riešenie nájdete na [Dynamics 365 Project Service Automation 3x do Project Operations 4x zastarané komponenty](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>Fakturačný údaj

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
|fakturadetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amount method                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionklasifikácia

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatioid.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionklasifikácia

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_agregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedčlenovia tímu                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourtocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicants k dispozícii                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>Registrácia člena msdyn_projectteam

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembership.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>Detail predajnej objednávky

| Polia                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |
