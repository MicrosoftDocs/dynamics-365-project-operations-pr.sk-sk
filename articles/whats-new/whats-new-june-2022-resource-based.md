---
title: Novinky v júni 2022 – Project Operations pre scenáre založené na zdrojoch/nenaskladnení
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft z júna 2022 Dynamics 365 Project Operations pre scenáre založené na zdrojoch/nezásobách.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031350"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novinky v júni 2022 – Project Operations pre scenáre založené na zdrojoch/nenaskladnení

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.43.0.77 alebo 4.43.0.119
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.27

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúca tabuľka zobrazuje mapy s duálnym zápisom, ktoré boli upravené alebo pridané vo vydaní Project Operations z júna 2022.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| --- | --- | --- |
| Entita exportu faktúr dodávateľa integrácie Project Operations (msdyn_projectvendorinvoices) | 1.0.0.1 | Zastarané pole bolo zastarané a namapované na nové pole na sledovanie stavu faktúry dodávateľa. |

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili mapu predpripravenej tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak pri spustení mapy narazíte na problém, postupujte podľa pokynov v časti [Problém chýbajúcich stĺpcov tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Subdodávky | 2708885 | Opravené chybové hlásenie, ktoré sa zobrazuje, keď používateľ vytvorí záznam hlavičky rezervácie rezervovateľného zdroja, kde nie je vyplnený žiadny rezervovateľný zdroj. |
| Plánovanie a sledovanie projektu | 2629441 | Opravená logika spúšťania pracovného toku, aby sa zabránilo nekonečnej slučke pri aktualizácii projektových úloh. |
| Čas a výdavky | 2641209 | Import časových záznamov z úloh/rezervácií si musí zachovať referenciu na rezervovateľný zdroj. |
| Plánovanie a sledovanie projektu | 2651148 | Hlavička projektového dokumentu musí byť strážená.|
| Plánovanie a sledovanie projektu | 2653145 | Pridané overenia, aby sa zabezpečilo, že nie je možné vytvoriť záznam projektu, ktorý má v názve neplatné znaky. |
| Čas a výdavky | 2654710 | Opravené filtrovanie na **Schválenia** stránku. |
| Fakturácia a tvorba cien | 2667805 | Pridané overenia, ktoré pomôžu zabrániť vytváraniu skutočných fakturovaných predajov, ak neexistujú podporné nevyúčtované skutočné predaje. |
| Fakturácia a tvorba cien | 2668378 | Pridané overenia, ktoré pomôžu zabrániť pridaniu vlastnej cenovej dimenzie, pokiaľ nie je vyplnený logický názov a názov poľa. |
| Subdodávky | 2677485 | Aktualizovaná cieľová verzia mapy dvojitého zápisu riadkov faktúry dodávateľa. |
| Čas a výdavky | 2700428 | Vylepšená logika schvaľovania, aby sa zabezpečilo, že ostatné sady schvaľovania pre projekt môžu byť spracované, aj keď jedna zo sád schvaľovania uviazla v systémových úlohách. |

### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo v oblasti financií

Ak chcete získať informácie o opravách chýb, ktoré sú súčasťou tejto aktualizácie, prihláste sa na Microsoft Dynamics Služby životného cyklu (LCS) a pozrite si [článok KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
