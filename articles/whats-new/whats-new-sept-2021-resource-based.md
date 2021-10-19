---
title: Čo je nové September 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Project Operations lite v septembri 2021 pre scenáre na základe zdroja/neskladovania.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547173"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové September 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

*Platí pre: Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch*

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

   - Project Operations v prostredí Microsoft Dataverse verzie 4.14.0.99.
   - Projektový manažment a účtovanie v prostredí Dynamics 365 Finance verzie 10.0.20.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť na stránke **Duálny zápis** v stĺpci **Verzia**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém so spustením mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) sprievodcu riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Čas a výdavky | 1811407 | Upravená rola zabezpečenia Schvaľovateľ projektu na schválenie vstupu do výdavkov. |
| Čas a výdavky | 1811438 | Upravená rola zabezpečenia Schvaľovateľ projektu na rušenie schválenia zadávania času. |
| Čas a výdavky | 2370126 | Aktualizované ikony **Úloha projektu** a **Rola** pre entitu **Zadanie času**. |
| Čas a výdavky | 2379879 | Opravená funkcia **Kopírovať týždeň** pri zadávaní času pri použití systému Dynamics 365 pre telefón. |
| Fakturácia a tvorba cien | 2371906 | Celková čiastka faktúry Proforma nesmie byť nastaviteľná v Project Operations pre nasadenia založené na zdrojoch. |
| Fakturácia a tvorba cien | 2385802 | Opravená chyba, ktorá sa vyskytuje pri záporných skutočných hodinách pri obnove súčtov projektov. |
| Fakturácia a tvorba cien | 2389675 | Vylepšené správanie pri potvrdzovaní faktúry proforma. Entita pre dlhodobé úlohy musí vziať do úvahy činnosť potrebnú na zapísanie výsledkov potvrdenia pre účtovníctvo. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Cestovanie a výdavky | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Sumy transakcií s daňou z predaja a z predaja, ktoré sú zaúčtované z výdavku vytvoreného z transakcie kreditnou kartou, sú nesprávne. |
| Cestovanie a výdavky | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Pri generovaní denníka platieb sa vytvoria nesprávne zúčtovacie riadky. |
| Cestovanie a výdavky | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Sumy transakcií s daňou z predaja, ktoré sú zaúčtované z výdavku vytvoreného z transakcie kreditnou kartou, sú nesprávne. |
| Cestovanie a výdavky | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Odstránenie výdavkového riadka môže trvať dlho. |
| Projektové účtovníctvo | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Po použití KB 4619395 nie je zmena postupnosti čísel na **Nepretržité** podporovaná a keď zaúčtujete odhad, vyskytne sa nasledujúca chyba „Systém nepodporuje nastavenie „nepretržitého “ poradia čísel Proj_X.“ |
| Projektové účtovníctvo | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Zaúčtovanie faktúry dodávateľa môže zlyhať s nasledujúcim chybovým hlásením „Transakcie s poukážkou nie sú zostatkové ku dňu 17. 5. 2021. (účtovná mena: 0,00 – mena vykazovania: 0,01).“ |
