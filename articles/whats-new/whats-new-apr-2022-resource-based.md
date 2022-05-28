---
title: Čo je nové v apríli 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft z apríla 2022 Dynamics 365 Project Operations pre scenáre založené na zdrojoch/nezásobách.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc713e7a0dd6993e38ce3e3b2ba19f796a6f4773
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/18/2022
ms.locfileid: "8613351"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v apríli 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma sa týka nasledujúcich komponentov a verzií Microsoftu Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.41.0.45
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.26

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

Kategórie obstarávania možno použiť v projektových nákupných objednávkach a čakajúcich faktúrach dodávateľa. Ďalšie informácie nájdete v časti [Použite kategórie obstarávania s projektovými nákupnými objednávkami a čakajúcimi faktúrami dodávateľa](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúca tabuľka zobrazuje mapy s duálnym zápisom, ktoré boli upravené alebo pridané vo vydaní Project Operations z marca 2022.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| -------------- | ------------------- | ------------|
| Projektové operácie integrácia projekt dodávateľ faktúra riadok export entity msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Táto mapa podporuje použitie kategórií obstarávania s nákupnými objednávkami a čakajúcimi faktúrami dodávateľa. |

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste si prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spustení mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| ------------ | ---------------- | -------------- |
| Čas a výdavky | 2573900 | The **Moderné schválenie** funkcia musí byť predvolene povolená. |
| Fakturácia a tvorba cien | 2603313 | Opravená chyba duplicitného záznamu, ktorá znemožňovala pridanie cenových ponúk a riadkov zmlúv s produktom. |
| Nasadenie a konfigurácia | 2611368 | Zákazníci musia mať možnosť pridať do riešenia až päť vlastných entít pomocou moderného návrhára aplikácií. |
| Čas a výdavky | 2628285 | Opravený problém, ktorý ovplyvňoval možnosť nastaviť správnu kategóriu zdrojov počas importu časového záznamu. |
| Správa príležitostí| 2628815 | Aktualizujte limit počtu znakov v popise podrobností riadka citácie tak, aby zodpovedal limitu počtu znakov predmetu úlohy, aby bol import úspešný pre úlohy, ktorých predmet je dlhší ako 100 znakov. |
| Čas a výdavky| 2629547 | The **Predloženej** pole schválenia projektov musí smerovať na používateľa, ktorý záznam predložil. |
| Čas a výdavky| 2629865 | The **Kopírovať kategóriu** pri kopírovaní projektov. |
| Čas a výdavky| 2636463 | Opravené filtre na schváleniach v moderných schvaľovacích formulároch. |
| Plánovanie a sledovanie projektu | 2648300 | Opravený problém, ktorý bráni zmene vlastníka projektu. |
| Fakturácia a tvorba cien | 2563000 | Riadky denníka pre nevyfakturovaný predaj, kde sa mena líši od meny kontraktu, nesmú byť povolené. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

Ak chcete získať informácie o opravách chýb, ktoré sú súčasťou tejto aktualizácie, prihláste sa na Microsoft Dynamics Lifecycle Services (LCS) a pozrite si [článok KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
