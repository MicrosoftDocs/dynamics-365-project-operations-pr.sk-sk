---
title: Synchronizácia projektových úloh priamo z Project Service Automation do Finance and Operations
description: Táto téma popisuje šablónu a základnú úlohu, ktoré sa používajú na synchronizáciu projektových úloh priamo z Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 45846d7a6dd7b84fe28f0a78ccc103679236917ea506180c5b383fd2828624eb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992810"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizácia projektových úloh priamo z Project Service Automation do Finance and Operations

[!include[banner](../includes/banner.md)]

Táto téma popisuje šablónu a základnú úlohu, ktoré sa používajú na synchronizáciu projektových úloh priamo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

> [!NOTE]
> - Integrácia projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií sú k dispozícii vo verzii 8.0.
> - Ak používate Enterprise Edition 7.3.0, po inštalácii KB 4132657 a KB 4132660 budete môcť tieto šablóny použiť na integráciu projektových úloh, kategórií transakcií výdavkov, odhadov hodín, odhadov výdavkov a skutočných údajov a na nakonfigurovať blokovanie funkcií. Ak musíte resetovať účtovné prerozdelenie, odporúčame vám nainštalovať si aj KB 4131710.
> - Integrácia skutočných hodnôt je k dispozícii vo verzii 8.0.1 alebo novšej.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok údajov pre Project Service Automation do Finance

Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance. Šablóna integrácie, ktorá je k dispozícii s funkciou integrácie údajov, umožňuje tok údajov o projektových úlohách z Project Service Automation do Finance.

Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.

[![Tok údajov pre integráciu Project Service Automation s Finance.](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Šablóna a úloha

Šablónu nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt**, kde si vyberiete verejné šablóny.

Nasledujúca šablóna a základná úlohu sa používajú na synchronizáciu projektových úloh Project Service Automation do Finance:

- **Názov šablóny v časti Integrácia údajov:** Projektové úlohy (PSA do Fin a Ops)
- **Názov úlohy v projekte:** Projektové úlohy

Predtým, ako môže dôjsť k synchronizácii projektových úloh, musíte synchronizovať projektové zmluvy a projekty.

## <a name="entity-set"></a>Nastavenie entity

| Project Service Automation | Finance                             |
|----------------------------|-------------------------------------|
| Projektové úlohy              | Integračná entita pre projektovú úlohu |

## <a name="entity-flow"></a>Tok entity

Projektové úlohy sa spravujú v Project Service Automation a synchronizujú s Finance ako projektové aktivity.

## <a name="prerequisites-and-mapping-setup"></a>Nevyhnutné predpoklady a nastavenie mapovania

Predtým, ako môže dôjsť k synchronizácii projektových úloh, musíte synchronizovať projektové zmluvy a projekty.

## <a name="power-query"></a>Power Query

Ak je táto podmienka splnená, na filtrovanie údajov musíte použiť Microsoft Power Query for Excel:

- V projektovej úlohe máte záznamy týkajúce sa konkrétnych zdrojov.

Ak musíte použiť Power Query, postupujte podľa tohto pokynu:

- Šablóna Projektové úlohy (PSA do Fin a Ops) má predvolený filter, ktorý vylučuje záznamy špecifické pre daný zdroj z projektovej úlohy nastavením filtra na **IsLineTask** na **False**. Ak vytvárate vlastnú šablónu, musíte pridať tento filter.

## <a name="template-mapping-in-data-integration"></a>Mapovanie šablón v integrácii údajov

Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov. Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.

[![Mapovanie šablón.](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]