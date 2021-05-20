---
title: Synchronizácia projektových zmlúv a projektov priamo z Project Service Automation do Finance
description: Táto téma popisuje šablónu a základnú úlohy, ktoré sa používajú na synchronizáciu projektových zmlúv a projektov priamo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
manager: AnnBe
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85722f61a672cc55cd2b511dc80ebfbe4807b957
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950418"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance"></a>Synchronizácia projektových zmlúv a projektov priamo z Project Service Automation do Finance 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Táto téma popisuje šablónu a základnú úlohy, ktoré sa používajú na synchronizáciu projektových zmlúv a projektov priamo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE] 
> Ak používate Enterprise edition 7.3.0, musíte nainštalovať KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok údajov pre Project Service Automation do Finance

> [!NOTE]
> Predtým, ako budete môcť použiť riešenie integrácie Project Service Automation do Finance, mali by ste byť oboznámení s funkciou integrácie údajov Dynamics 365.

Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance. Integračná šablóna, ktorá je k dispozícii s funkciou Integrácia údajov, umožňuje tok údajov projektových zmlúv, projektov, riadkov projektových zmlúv, medzníkov riadkov projektových zmlúv, projektových úloh, kategórií transakcií výdavkov, odhadov hodín a odhadov výdavkov z Project Service Automation do Finance.

Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.

[![Tok údajov pre integráciu Project Service Automation s Finance](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Šablóny a úlohy

Dostupné šablóny nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt**, kde si vyberiete verejné šablóny.

Nasledujúca šablóny a základné úlohy sa používajú na synchronizáciu projektový zmlúv a projektov z Project Service Automation do Finance:

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integrácia s Dynamics 365 Project Service Automation v2.x
- **Názov šablóny v integrácii údajov:** Projekty a zmluvy (Project Service Automation do Finance)
- **Názov úloh v projekte:**

    - Projektové zmluvy Project Service Automation do Finance
    - Projekty Project Service Automation do Finance
    - Riadky projektových zmlúv Project Service Automation do Finance
    - Riadky medzníkov projektových zmlúv Project Service Automation do Finance
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integrácia s Dynamics 365 Project Service Automation v3.x
V Project Service Automation nastala zmena schémy, ktorá ovplyvní šablónu medzníka riadku zmluvy s projektom a na integráciu Project Service Automation v3.x s Dynamics 365 je potrebné použitie verzie šablóny v2.

- **Názov šablóny v integrácii údajov:** Projekty a zmluvy (Project Service Automation 3.x do Finance) – v2
- **Názov úloh v projekte:**

    - Projektové zmluvy Project Service Automation do Finance
    - Projekty Project Service Automation do Finance
    - Riadky projektových zmlúv Project Service Automation do Finance
    - Riadky medzníkov projektových zmlúv Project Service Automation do Finance

Predtým, ako môže dôjsť k synchronizácii zmlúv a projektov, musíte synchronizovať účty.

## <a name="entity-set"></a>Nastavenie entity

| Project Service Automation       | Finance                                                |
|----------------------------------|--------------------------------------------------------|
| Objednávky                           | Integračná entita pre projektovú zmluvu                |
| Projekty                         | Integračná entita pre projekt                         |
| Riadky objednávok                      | Integračná entita pre riadok projektovej zmluvy           |
| Medzníky v riadkoch projektovej zmluvy | Integračná entita pre medzník riadka projektovej zmluvy |

## <a name="entity-flow"></a>Tok entity

Projektové zmluvy sa spravujú v Project Service Automation a synchronizujú s Finance ako projektové zmluvy. Ako súčasť šablóny integrácie môžete nastaviť zdroj integrácie v časti Finance pre zmluvu o projekte.

Časové a materiálne projekty a projekty s pevnou cenou sa spravujú v Project Service Automation a synchronizujú sa s Finance ako projekty. V rámci integrácie šablón môžete nastaviť zdroj integrácie pre projekt v aplikácii Finance. V súčasnosti sú podporované iba časové a vecné projekty a projekty s pevnou cenou.


Projektové riadky zmlúv sa spravujú v Project Service Automation a synchronizujú s Finance ako projektové zmluvné pravidlá fakturácie. Ak sa spôsob fakturácie líši od predvoleného typu projektu, synchronizácia aktualizuje typ projektu pre riadok zmluvy projektu a projektovú skupinu.

Projektové medzníky riadka zmlúv sa spravujú v Project Service Automation a synchronizujú sa s Finance ako projektové medzníky zmluvných pravidiel fakturácie.

## <a name="project-service-automation-to-finance-integration-solution"></a>Integrácia riešenia Project Service Automation do Finance

Pole **ID projektovej zmluvy** je k dispozícii na stránke **Zmluvy o projekte**. Táto oblasť sa stala prirodzeným a jedinečným kľúčom na podporu integrácie.

Pri vzniku novej zmluvy o projekte, ak hodnota **ID projektovej zmluvy** ešte neexistuje, automaticky sa generuje pomocou číselnej postupnosti. Hodnota sa skladá z **ORD** a nasleduje prírastková číselná sekvencia a potom prípona šiestich znakov. Príklad: **ORD-01022-Z4M9Q0**.

Pole **Číslo projektu** je k dispozícii na stránke **Projekty**. Táto oblasť sa stala prirodzeným a jedinečným kľúčom na podporu integrácie.

Pri vzniku nového projektu, ak hodnota **Číslo projektu** ešte neexistuje, automaticky sa generuje pomocou číselnej postupnosti. Hodnota sa skladá z **PRJ** a nasleduje prírastková číselná sekvencia a potom prípona šiestich znakov. Príklad: **PRJ-01049-CCNID0**.

Keď sa použije integračné riešenie Project Service Automation to Finance, inovačný skript nastaví hodnotu poľa **ID projektovej zmluvy** pre existujúce projektové zmluvy a pole **Číslo projektu** pre existujúce projekty v Project Service Automation.

## <a name="prerequisites-and-mapping-setup"></a>Nevyhnutné predpoklady a nastavenie mapovania

- Predtým, ako môže dôjsť k synchronizácii zmlúv a projektov, musíte synchronizovať účty.
- Do svojej skupiny pripojení pridajte mapovanie poľa integračného kľúča pre **msdyn\_organizationalunits** na **msdyn\_name\[Name\]**. Možno bude najskôr potrebné pridať projekt do súpravy pripojení. Ďalšie informácie nájdete v časti [Integrácia údajov do Common Data Service pre aplikácie](/powerapps/administrator/data-integrator).
- Do svojej skupiny pripojení pridajte mapovanie poľa integračného kľúča pre **msdyn\_projects** na **msdynce\_projectnumber\[Project Number\]**. Možno bude najskôr potrebné pridať projekt do súpravy pripojení. Ďalšie informácie nájdete v časti [Integrácia údajov do Common Data Service pre aplikácie](/powerapps/administrator/data-integrator).
- **SourceDataID** pre projektové zmluvy a projekty je možné aktualizovať na inú hodnotu alebo odstrániť z mapovania. Predvolená hodnota šablóny je **Project Service Automation**.
- Mapovanie **PaymentTerms** musí byť aktualizované tak, aby odrážalo platné platobné podmienky v službe Finance. Môžete tiež odstrániť mapovanie z projektovej úlohy. Mapa predvolených hodnôt má predvolené hodnoty pre ukážkové údaje. Nasledujúca tabuľka zobrazuje hodnoty v Project Service Automation.

    | Hodnota | Popis   |
    |-------|---------------|
    | 1     | 30 dní netto        |
    | 2     | 10 dní so zľavou 2 %, inak 30 dní netto |
    | 3     | 45 dní netto        |
    | 4     | 60 dní netto        |

## <a name="power-query"></a>Power Query

Na filtrovanie údajov použite program Microsoft Power Query for Excel, ak sú splnené nasledujúce podmienky:

- Predajné objednávky nájdete v Dynamics 365 Sales.
- V službe Project Service Automation máte viac organizačných jednotiek a tieto organizačné jednotky budú namapované na viaceré právnické osoby v službe Finance.

Ak musíte použiť Power Query, postupujte podľa týchto pokynov:

- Šablóna Projekty a zmluvy (PSA pre Fin a Ops) má predvolený filter, ktorý obsahuje iba predajné objednávky **Pracovná položka typu (msdyn\_ordertype = 192350001)**. Tento filter pomáha zaručiť, že sa pre zákazky odberateľa v službe Finance nevytvoria projektové zmluvy. Ak vytvárate vlastnú šablónu, musíte pridať tento filter.
- Vytvorte filter Power Query, ktorý obsahuje iba zmluvné organizácie, ktoré by sa mali synchronizovať s právnickou osobou súpravy integračného pripojenia. Napríklad projektové zmluvy, ktoré máte s organizačnou jednotkou zmluvy Contoso USA by mali byť synchronizované s právnickou osobou USSI, ale projektové zmluvy, ktoré máte s organizačnou jednotkou zmluvy Contoso Global by sa mali synchronizovať s právnickou osobou USMF. Ak tento filter nepridáte do svojho mapovania úloh, všetky kontrakty projektu sa synchronizujú s právnickou osobou, ktorá je definovaná pre množinu pripojení, bez ohľadu na organizačnú jednotku kontraktu.

## <a name="template-mapping-in-data-integration"></a>Mapovanie šablón v integrácii údajov

> [!NOTE] 
> Polia **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** a **AddressZipCode** nie sú súčasťou predvoleného mapovania pre projektové zmluvy. Ak chcete, aby sa tieto údaje synchronizovali pre zmluvy o projekte, môžete pridať priradenia.
>
> Polia **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** a **ProjectType** nie sú zahrnuté v predvolenom mapovaní pre projekty. Ak chcete, aby sa tieto údaje synchronizovali pre zmluvy o projekte, môžete synchronizovať pre projekty.

Nasledujúca ilustrácia ukazuje príklady mapovania úlohy šablóny v Integrácii údajov. Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.

[![Mapovanie šablón projektovej zmluvy](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Mapovanie šablón projektu](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Mapovanie šablón riadkov zmluvy projektu](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Mapovanie šablón míľnika riadku zmluvy projektu](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Mapovanie medzníkov linky kontraktov v projektoch a kontraktoch (PSA 3.x až Dynamics) - šablóna v2:

[![Mapovanie míľnika riadka zmluvy projektu so šablónou verzie dva](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]