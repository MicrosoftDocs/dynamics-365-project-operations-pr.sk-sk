---
title: Čo je nové v apríli 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Microsoft Dynamics 365 Project Operations Project Operations v apríli 2022 pre scenáre založené na zdrojoch/neskladovaných položkách.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110903"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v apríli 2022 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.41.0.45
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.26

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

Kategórie obstarávania je možné použiť v nákupných objednávkach a čakajúcich faktúrach dodávateľa. Ďalšie informácie sú uvedené v časti [Použitie kategórií obstarávania s nákupnými objednávkami projektu a čakajúcimi faktúrami dodávateľa](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúca tabuľka zobrazuje mapy duálneho zápisu, ktoré boli upravené alebo pridané vo vydaní Project Operations z marca 2022.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| -------------- | ------------------- | ------------|
| Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.4 | Táto mapa podporuje použitie kategórií obstarávania s nákupnými objednávkami a čakajúcimi faktúrami dodávateľa. |

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| ------------ | ---------------- | -------------- |
| Čas a výdavky | 2573900 | Funkcia **Moderné schválenia** musí byť predvolene povolená. |
| Fakturácia a tvorba cien | 2603313 | Opravená chyba duplicitného záznamu, ktorá zabránila pridaniu riadkov cenových ponúk a zmlúv s produktom. |
| Nasadenie a konfigurácia | 2611368 | Zákazníci musia mať možnosť pridať do riešenia až päť vlastných entít pomocou moderného návrhára aplikácií. |
| Čas a výdavky | 2628285 | Opravený problém, ktorý ovplyvňoval možnosť nastaviť správnu kategóriu zdrojov počas importu zadania času. |
| Správa príležitostí| 2628815 | Aktualizácia limitu počtu znakov v riadku popisu podrobností cenovej ponuky tak, aby zodpovedal limitu počtu znakov predmetu úlohy, aby bol import úspešný pre úlohy, ktorých predmet je dlhší ako 100 znakov. |
| Čas a výdavky| 2629547 | Pole **Odoslal používateľ** schválenia projektov musí smerovať na používateľa, ktorý záznam odoslal. |
| Čas a výdavky| 2629865 | Pole **Kopírovať kategóriu** pri úlohách, kde sa kopírujú projekty. |
| Čas a výdavky| 2636463 | Opravené filtre schválení vo formulároch moderných schválení. |
| Plánovanie a sledovanie projektu | 2648300 | Opravený problém, ktorý bráni zmene vlastníka projektu. |
| Fakturácia a tvorba cien | 2563000 | Záznamy v účtovnom denníku pre nevyfakturovaný predaj, kde sa mena líši od meny kontraktu, nesmú byť povolené. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

Informácie o opravách zahrnutých v tejto aktualizácii nájdete po prihlásení do Microsoft Dynamics Lifecycle Services (LCS) a zobrazení [článku vedomostnej databázy](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
