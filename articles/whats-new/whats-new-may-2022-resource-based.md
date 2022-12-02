---
title: Čo je nové v máji 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Microsoft Dynamics 365 Project Operations Project Operations v máji 2022 pre scenáre založené na zdrojoch/neskladovaných položkách.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921413"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v máji 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.42.0.70
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.26

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality
### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Správa zdrojov | 2634019 | Vylepšené chybové hlásenia pre obchodné overenia pri pridávaní všeobecných členov tímu ako zdrojov. |
| Plánovanie a sledovanie projektu | 2648515 | Obmedzené aktualizácie **id vlastníka**, **stav** a **postavenie** v plánovaní entít. |
| Fakturácia a tvorba cien | 2653167 | Oddeľovač desatinných miest v mriežke **Odhady** musí zodpovedať nastaveniam formátu v ponuke **Osobné možnosti**. |
| Fakturácia a tvorba cien| 2662251 | Hodnoty v poliach **Upravená jednotka** a **Jednotková skupina** sú pri vytváraní záznamov v odhadoch materiálu predvolené. |
| Fakturácia a tvorba cien| 2571408 | Nevyfakturované skutočné hodnoty predaja sú pri vytváraní konceptu faktúry opečiatkované ID proforma faktúry. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

Informácie o opravách zahrnutých v tejto aktualizácii nájdete po prihlásení do Microsoft Dynamics Lifecycle Services (LCS) a zobrazení [článku vedomostnej databázy](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
