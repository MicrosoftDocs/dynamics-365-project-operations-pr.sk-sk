---
title: Čo je nové v novembri 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Microsoftu Dynamics 365 Project Operations  z novembra 2022 pre scenáre založené na zdrojoch alebo bez zásob.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831149"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v novembri 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.58.0.119
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.30

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2781818 | Chyba kľúča sa nenašla pri predvolenej cene pre denník použitia materiálu. |
| Fakturácia a tvorba cien | 2922373 | Nie je možné prepojiť riadok ponuky s projektom, ktorý sa uzavrel ako stratená ponuka. |
| Fakturácia a tvorba cien | 2943206 | **Pole Riadok zmluvy**  v entite projektu by malo byť voliteľné. |
| Fakturácia a tvorba cien | 2953182 | Vylepšite chybové hlásenie pre opravné faktúry.|
| Fakturácia a tvorba cien | 2959500 | Nie je možné prepojiť riadok ponuky s projektovou úlohou, ktorá je už priradená k stratenej ponuke.|
| Fakturácia a tvorba cien | 2959560 | Správa „Tento zákazník už má zmluvu o projekte“ prijatá pri uzatváraní cenovej ponuky, ktorá bola získaná v určitých lokalitách. |
| Fakturácia a tvorba cien | 3031727 | Priradenia zdrojov zlyhajú, pretože v poli Povinné pole „msdyn_Company“ chýba chyba. |
| Fakturácia a tvorba cien | 3036905 | Vlastniť spoločnosť nikdy nie je inicializovaná členom ProjectTeam. |
| Správa príležitostí | 2763519 | Chyba Null Reference v SecureProjectContractAlowsUpdates. |
| Správa príležitostí | 2783798 | Pri importovaní odhadov projektu na riadok ponuky chýbajú popisy úloh pre odhady nákladov a materiálu.|
| Správa príležitostí | 2988635 | Vylepšite popis chybovej správy pri odstraňovaní zákazníka z ponuky. |
| Správa príležitostí | 3001191 | Nie je možné vytvoriť cenovú ponuku z príležitosti, kde je spôsob fakturácie zadaný ako null. |
| Inovácia | 3012324 | Konverzia projektu zlyhala v projekte s riadiacimi znakmi ako Tab v názve. || Plánovanie a sledovanie projektu | 2790384 | Časový limit Pending OperationSet je príliš krátky. |
| Plánovanie a sledovanie projektu | 3044275 | Chýba lokalizácia pre: missingProjectSchedulerErrorMessage. |
| Plánovanie a sledovanie projektu | 3044277 | Mriežka Project Recon sa nenačíta, keď nie je nastavený plánovač.|
| Správa zdrojov | 2943153 | Aktualizujte kartu Sledovanie, aby sa pre Trvanie zobrazovali dve desatinné miesta.|
| Subdodávateľské zmluvy | 2932774 | Chyba iba na čítanie riadku faktúry dodávateľa vyvoláva chybu. |
| Subdodávateľské zmluvy | 2939556 | Stav hlavičky faktúry dodávateľa by nemal byť nastavený na možnosť Vymazať online koncept, ak nie je aktívny. |
| Čas a výdavky | 2939998 | Získajte novú verziu TESA v ProjOps. |


### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo vo Finance

Informácie o opravách zahrnutých v tejto aktualizácii nájdete po prihlásení do Microsoft Dynamics Lifecycle Services a zobrazení [článku vedomostnej databázy](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
