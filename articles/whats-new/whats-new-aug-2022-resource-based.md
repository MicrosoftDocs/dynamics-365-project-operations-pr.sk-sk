---
title: Novinky v auguste 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft z augusta 2022 Dynamics 365 Project Operations pre scenáre založené na zdrojoch/nezásobách.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403876"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novinky v auguste 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.45.0.53
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili mapu predpripravenej tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak pri spustení mapy narazíte na problém, postupujte podľa pokynov v časti [Problém chýbajúcich stĺpcov tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Správa príležitostí | 2762089 | Ošetrenie chýb pri uzatváraní zmluvy ako stratenej, ak je v organizácii vypnuté automatické ukladanie.|
|Plánovanie a sledovanie projektu | 2767841 | Aktualizácie telemetrie Entita projektu Vytvorenie alebo aktualizácia scenárov.|
|Fakturácia a tvorba cien | 2771072 | Spracovanie výnimiek z nulovej referencie pri vyhrávaní cenovej ponuky.|
|Fakturácia a tvorba cien | 2844181 |Nepodarilo sa získať ID korelácie a zablokovať vytvorenie faktúry.|
|Fakturácia a tvorba cien | 2852836 | Medzipodnikové skutočné údaje chýbajú pre medzipodnikové výdavky vytvorené a schválené v CE.|


### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo vo financiách

Ak chcete získať informácie o opravách chýb, ktoré sú súčasťou tejto aktualizácie, prihláste sa na Microsoft Dynamics Služby životného cyklu (LCS) a pozrite si [článok KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
