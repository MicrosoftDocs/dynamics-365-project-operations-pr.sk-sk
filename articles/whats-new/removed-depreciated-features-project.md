---
title: Odstránené alebo zastarané funkcie v Dynamics 365 Project Operations
description: Tento článok popisuje funkcie, ktoré boli odstránené alebo ktoré sú plánované na odstránenie z Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028348"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Odstránené alebo zastarané funkcie v Dynamics 365 Project Operations

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma a Project Operations pre scenáre založené na zdrojoch/výrobe_

Tento článok popisuje funkcie, ktoré boli odstránené alebo ktoré sú plánované na odstránenie z Dynamics 365 Project Operations.

- *Odstránená* funkcia už v produkte nie je k dispozícii.
- *Zastaraná* funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Tento zoznam vám pomôže zvážiť tieto odstránenia a ukončenia podpory pre vaše vlastné plánovanie.

> [!NOTE]
> Podrobné informácie o objektoch v aplikáciách na riadenie financií a prevádzok nájdete v [**Správach o technických referenciách**](/dynamics/s-e/global/axtechrefrep_61). Môžete porovnať rôzne verzie týchto prehľadov, aby ste sa dozvedeli o objektoch, ktoré sa zmenili alebo boli odstránené v jednotlivých verziách aplikácií na riadenie financií a prevádzok.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Odstránené alebo zastarané funkcie v aplikácii Project Operations, vydanie z marca 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Riadenie projektu a účtovníctvo – parameter „Vždy vytvárať transakciu úpravy“

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Na účely auditu sú potrebné transakcie úprav. Po ukončení podpory bude tento parameter skrytý. Systém vždy vytvorí transakcie úprav, rovnako ako to robí v súčasnosti, keď je parameter nastavený na **Áno**. |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Project Operations pre scenáre založené na výrobe/zdrojoch |
| **Status** | Zastarané: Do 1. marca 2023 skryjeme parameter a zmeníme správanie systému tak, aby sa vždy vytvárali transakcie úprav. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Riadenie a účtovníctvo projektu – parameter „Použiť dátum úpravy ako nový dátum projektu“

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Tento parameter sa pôvodne používal na umožnenie úprav pri zatvorení fiškálneho obdobia. Už to však nie je potrebné, pretože účtovný dátum transakcie je možné zmeniť na prvý dátum otvoreného obdobia, ak je nakonfigurovaný. Dátum projektu sa nesmie meniť, pretože predstavuje dátum, kedy došlo k transakcii. |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Project Operations pre scenáre založené na výrobe/zdrojoch |
| **Status** | Zastarané: Do 1. marca 2023 skryjeme parameter a zmeníme správanie systému tak, aby sa dátum projektu v úpravách nikdy nemenil. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Pracovný postup týkajúci sa požiadaviek na zdroje v Project Operations pre scenáre založené na zdrojoch/výrobe

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Zastarané z dôvodu nízkeho využitia a obmedzení objemu transakcií. |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Project Operations pre scenáre založené na výrobe/zdrojoch |
| **Status** | Zastarané: Do 1. marca 2023 zakážeme možnosť žiadať zdroje pre projekt pomocou pracovného postupu. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stránka návrhu faktúry projektu bez zobrazení hlavičky a riadkov

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Zastarané z dôvodu vylepšení stránky, ktorá bola predstavená spolu s kľúčom funkcie **Použitie návrhu faktúry projektu a formulárov denníka faktúr so zobrazením hlavičky a riadkov**. |
| **Nahradené inou funkciou?** | Áno |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Project Operations pre scenáre založené na výrobe/zdrojoch; Project Operation spre scenáre založené na zdrojoch/neskladovaných položkách |
| **Status** | Zastarané: Do 1. marca 2023 vypneme staršiu (klasickú) stránku a zapneme predvolene kľúč funkcie **Použitie návrhu faktúry projektu a formulárov denníka faktúr so zobrazením hlavičky a riadkov**. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Odstránené alebo zastarané funkcie v aplikácii Project Operations, vydanie z decembra 2021

### <a name="collaboration-workspaces"></a>Pracovné priestory na spoluprácu

[Vytvorenie alebo prepojenie na pracovný priestor spolupráce (projekt)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Zastarané z dôvodu nízkeho používania. Zákazníci, ktorí používajú Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek, môžu využiť [Spoluprácu pomocou skupín v Office](../project-management/collaboration-groups.md). |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia  |
| **Možnosť nasadenia** | Project Operations pre scenáre založené na výrobe/zdrojoch |
| **Status** | Zastarané: Do 1. decembra 2022 plánujeme ukončiť podporu pracovných priestorov na spoluprácu. |
