---
title: Novinky v auguste 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní nasadenia Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch z augusta 2021.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 26861472d3af20c58b3d01142b834d535cf99715
ms.sourcegitcommit: 083e3d219cd5126eecb74debb1b70b361680b1f6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/18/2021
ms.locfileid: "7501390"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novinky v auguste 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

*Platí pre: Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch*

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

   - Project Operations v prostredí Microsoft Dataverse verzie 4.13.0.152.
   - Projektový manažment a účtovanie v prostredí Dynamics 365 Finance verzie 10.0.20.

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

V tomto vydaní sú zahrnuté nasledujúce funkcie:

- **Množiny schválení**: Schválenie nastavuje skupinový čas, výdavky alebo schválenie použitia materiálu spoločne do menších podskupín operácií. Toto zoskupenie umožňuje spracovanie schválení v konkrétnej objednávke podľa projektu a umožňuje opakovanie a sekvenovanie. Zoskupenie žiadostí zvyšuje spoľahlivosť a vysledovateľnosť spracovania schválenia pre veľké objemy schválení. Ďalšie informácie nájdete v článku [Množiny schválení](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations.

Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť na stránke **Duálny zápis** v stĺpci **Verzia**. Novú verziu mapy aktivujete stlačením možnosti **Verzie mapových tabuliek**, výberom najnovšej verzie a následným uložením vybranej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spustení mapy, postupujte podľa pokynov v časti [Problém s chýbajúcou tabuľkou na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Riešenie problémov s funkciou duálneho zápisu.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2295625 | Názov medzníka je potrebné skopírovať z plánu faktúr do detailu riadka faktúry. |
| Fakturácia a tvorba cien | 2316323 | Zľavu nie je možné upravovať na proforma faktúre v Project Operations pre scenáre založené na zdrojoch. |
| Správa príležitostí | 2338619 | Obchodné pravidlá **Príležitosť** a **Cenová ponuka** je možné použiť iba na stránkach. |
| Správa zdrojov | 2316523 | Pri použití možnosti **Poslať žiadosť** z požiadavky na zdroj, ku ktorej je priradená rola, by sa nemala zobrazovať chyba. |
| Správa zdrojov | 2326885 | Pri vytváraní požiadavky na zdroj prostredníctvom projektu by sa nemala zobrazovať chyba. |
| Čas a výdavky | 2335584 | Toky úloh v zadaní času už nie sú podporované. |
| Čas a výdavky | 2336884 | Tlačidlo časovej položky **Kopírovať týždeň** musí fungovať nielen pre aktuálneho používateľa. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v rámci Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Cestovanie a výdavky | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nesprávne sumy transakcií dodávateľa a dane z predaja sa zaúčtujú pri vytvorení výdavku z transakcie kreditnou kartou. |
| Cestovanie a výdavky | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Nesprávne vyrovnanie sú riadky vytvorené pri generovaní denníka platieb. |
| Cestovanie a výdavky | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Nesprávne sumy transakcie dane z predaja sa zaúčtujú pri vytvorení výdavku z transakcie kreditnou kartou. |
| Cestovanie a výdavky | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Odstránenie výdavkového riadka môže trvať dlho. |
| Projektové účtovníctvo | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Keď zaúčtujete odhad po použití KB 4619395, systém nepodporuje nastavenie postupného sekvenovania čísel. |
| Projektové účtovníctvo | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Účtovanie faktúry dodávateľa môže zlyhať s chybovým hlásením „Transakcie s poukážkou nie sú zostatkové podľa dátumu 17.5.2021. (účtovná mena: 0,00 – mena vykazovania: 0,01) “ |
