---
title: Odstránené alebo zastarané funkcie v Dynamics 365 Project Operations
description: Tento článok popisuje funkcie, ktoré boli odstránené alebo ktoré sa plánujú odstrániť z Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921505"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Odstránené alebo zastarané funkcie v Dynamics 365 Project Operations

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma a Project Operations pre scenáre založené na zdrojoch/výrobe_

Tento článok popisuje funkcie, ktoré boli odstránené alebo ktoré sa plánujú odstrániť z Dynamics 365 Project Operations.

- *Odstránená* funkcia už v produkte nie je k dispozícii.
- *Zastaraná* funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Tento zoznam vám pomôže zvážiť tieto odstránenia a ukončenia podpory pre vaše vlastné plánovanie.

> [!NOTE]
> Podrobné informácie o objektoch v aplikáciách Finance and Operations nájdete v [**Správy o technických referenciách**](/dynamics/s-e/global/axtechrefrep_61). Môžete porovnať rôzne verzie týchto prehľadov, aby ste sa dozvedeli o objektoch, ktoré boli zmenené alebo odstránené v jednotlivých verziách aplikácií Finance and Operations.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkcie odstránené alebo zastarané vo vydaní Project Operations z marca 2022

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Riadenie projektu a účtovníctvo Parameter "Vždy vytvárať transakciu úpravy".

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Na účely auditu sú potrebné transakcie úprav. Po ukončení podpory bude tento parameter skrytý. Systém vždy vytvorí transakcie úprav, rovnako ako to robí v súčasnosti, keď je parameter nastavený na **Áno**. |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Projektové operácie pre scenáre výroby/skladu |
| **Status** | Zastarané: Do 1. marca 2023 skryjeme parameter a zmeníme správanie systému tak, aby sa vždy vytvárali transakcie úprav. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Riadenie a účtovníctvo projektu Parameter „Použiť dátum úpravy ako nový dátum projektu“.

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Tento parameter bol pôvodne použitý na umožnenie úprav, keď bol fiškálne obdobie zatvorený. Už to však nie je potrebné, pretože účtovný dátum transakcie je možné zmeniť na prvý dátum otvoreného obdobia, ak je nakonfigurovaný. Dátum projektu sa nesmie meniť, pretože predstavuje dátum, kedy došlo k transakcii. |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Projektové operácie pre scenáre výroby/skladu |
| **Status** | Zastarané: Do 1. marca 2023 skryjeme parameter a zmeníme správanie systému tak, aby sa dátum projektu pri úpravách nikdy nezmenil. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Pracovný postup požiadaviek na zdroje v projektových operáciách pre scenáre na sklade/výrobe

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Zastarané z dôvodu nízkeho využitia a obmedzení objemu transakcií. |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Projektové operácie pre scenáre výroby/skladu |
| **Status** | Zastarané: Do 1. marca 2023 zakážeme možnosť žiadať zdroje pre projekt pomocou pracovného postupu. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Stránka návrhu faktúry projektu bez zobrazení hlavičky a riadkov

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Zastarané z dôvodu vylepšení stránky, ktorá bola predstavená spolu s **Použite návrh faktúry projektu a formuláre denníka faktúr so zobrazením Hlavička a riadky** funkčný kľúč. |
| **Nahradené inou funkciou?** | Áno |
| **Ovplyvnené oblasti výrobkov** | Aplikácia |
| **Možnosť nasadenia** | Projektové operácie pre scenáre výroby/skladu; Projektové operácie pre scenáre zdrojov/nezásobených zdrojov |
| **Status** | Zastarané: Do 1. marca 2023 vypneme staršiu (staršiu) stránku a zapneme **Použite návrh faktúry projektu a formuláre denníka faktúr so zobrazením Hlavička a riadky** funkčný kľúč štandardne. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcie odstránené alebo zastarané vo vydaní Project Operations z decembra 2021

### <a name="collaboration-workspaces"></a>Pracovné priestory pre spoluprácu

[Vytvorenie pracovného priestoru spolupráce (projekt) alebo prepojenie naň](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Dôvod ukončenia podpory/odstránenia** | Zastarané pre nízke využitie. Zákazníci, ktorí používajú projektové operácie pre scenáre so zdrojmi/nezásobené, môžu využiť [Spolupráca s Office Groups](../project-management/collaboration-groups.md). |
| **Nahradené inou funkciou?** | No |
| **Ovplyvnené oblasti výrobkov** | Aplikácia  |
| **Možnosť nasadenia** | Projektové operácie pre scenáre výroby/skladu |
| **Status** | Zastarané: Do 1. decembra 2022 plánujeme ukončiť podporu pracovných priestorov Collaboration. |
