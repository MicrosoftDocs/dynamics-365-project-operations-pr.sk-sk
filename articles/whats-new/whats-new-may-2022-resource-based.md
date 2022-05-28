---
title: Čo je nové v máji 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft z mája 2022 Dynamics 365 Project Operations pre scenáre založené na zdrojoch/nezásobách.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710167"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v máji 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma sa týka nasledujúcich komponentov a verzií Microsoftu Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.42.0.70
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste si prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spustení mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality
### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Správa zdrojov | 2634019 | Vylepšené chybové hlásenia pre obchodné overenia pri pridávaní generických členov tímu ako zdrojov. |
| Plánovanie a sledovanie projektu | 2648515 | Obmedzené aktualizácie z **vlastníka**, **a** **postavenie** v plánovaní subjektov. |
| Fakturácia a tvorba cien | 2653167 | The **Odhady** mriežkový oddeľovač desatinných miest musí zodpovedať nastaveniam formátu v **Osobné možnosti**. |
| Fakturácia a tvorba cien| 2662251 | Hodnoty v **Opravená jednotka** a **Skupina jednotiek** polia predvolené pri vytváraní záznamov v odhadoch materiálu. |
| Fakturácia a tvorba cien| 2571408 | Skutočné nevyfakturované tržby sú pri vytváraní návrhu faktúry opečiatkované ID proforma faktúry. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

Ak chcete získať informácie o opravách chýb, ktoré sú súčasťou tejto aktualizácie, prihláste sa na Microsoft Dynamics Lifecycle Services (LCS) a pozrite si [článok KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
