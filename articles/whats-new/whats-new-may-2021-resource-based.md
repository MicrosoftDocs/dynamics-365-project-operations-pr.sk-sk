---
title: Čo je nové v máji 2021 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Project Operations z mája 2021 pre scenáre založené na zdrojoch/neskladovaných položkách.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: cc5e8104702951fd787d02407d26671e46d44f0c
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9030008"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v máji 2021 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

- Project Operations v službe Dynamics 365 Dataverse, verzia prostredia 4.10.0.186
- Projektový manažment a účtovníctvo v prostrediach aplikácií na riadenie financií a prevádzok verzie 10.0.18

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

V tomto vydaní sú zahrnuté nasledujúce funkcie:

- [Režimy plánovania](../project-management/scheduling-modes.md): Projektoví manažéri môžu definovať, či sa má projekt riadiť pomocou režimu plánovania s fixným trvaním, fixnou prácou alebo fixnými jednotkami.
- [Nastavte počet najazdených kilometrov pomocou úrovní hodnotenia počtu najazdených kilometrov](../expense/set-up-mileage.md) : Aktualizujte úrovne počtu najazdených kilometrov podľa výkazov zamestnancov o výdavkoch.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúci zoznam zobrazuje mapy duálneho zapisovania, ktoré boli upravené alebo pridané vo vydaní Project Operations z mája 2021.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| --- | --- | --- |
| Zdroj financovania projektu (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Synchronizácia platobných podmienok zákazníka v projektovej zmluve. |
| Návrh projektovej faktúry V2 (faktúry) | 1.0.0.3 | Synchronizácia platobných podmienok faktúry pro forma. |
| Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Aktualizácie kvality |
| Projekty V2 (msdyn\_projects) | 1.0.0.2 | Aktualizácie kvality |

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia aplikácií na riadenie financií a prevádzok vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém so spustením mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2227635 | Hodnoty v poli **Jednotková skupina** a **Jednotka** sú predvolené na základe produktu v mriežke **Odhady materiálov**. |
| Fakturácia a tvorba cien | 2234127 | Pole **ID úlohy** sa teraz správne integruje do skutočných hodnôt projektu Dataverse, keď sa zaúčtuje faktúra dodávateľa. |
| Fakturácia a tvorba cien | 2235564 | Uloženie záznamu v účtovnom denníku zabezpečí, že mena zobrazená v účtovnom zázname sa po uložení bude zhodovať s predvolenou menou v zázname. |
| Fakturácia a tvorba cien | 2246671 | Ak transakciu nebude možné zúčtovať počas fakturácie, zvráti sa pôvodný nevyfakturovaný záznam predaja a vytvorí sa nový nevyfakturovaný záznam predaja, ktorý bude nezúčtovateľný. |
| Fakturácia a tvorba cien | 2264042 | Platná oprava faktúry nesmie byť zablokovaná, ak existujú podrobnosti o oprave faktúry, ktoré nie sú v danom prostredí platné. |
| Fakturácia a tvorba cien | 2146367 | Priradenie duálneho zápisu v hlavičke faktúry projektu je rozšírené o platobné podmienky. |
| Správa príležitostí | 2086888 | Nepridávajte roly a kategórie, ktoré sú deaktivované, skôr než skopírujete cenovú ponuku do zúčtovateľných rolí a kategórií v rámci novoskopírovanej ponuky. |
| Správa príležitostí | 2234376 | Polia určené iba na čítanie sú v mriežke **Odhady materiálov** sivé. |
| Správa príležitostí | 2238337 | Cenovú ponuku založenú na kontakte je možné uložiť, aj keď nie je spojená s cenníkom projektu. |
| Správa príležitostí | 2239810 | Po uzatvorení cenovej ponuky ako stratenej sa uzavrie aj súvisiaci projekt a zrušia sa všetky rezervácie. |
| Plánovanie a sledovanie projektu | 2099559 | Pridali sa ďalšie overenia stavu systému pred otvorením mriežky **Projektové úlohy**. |
| Plánovanie a sledovanie projektu | 2178987 | Opravila sa prechodná chyba, ktorá sa vyskytla pri výbere možnosti **Ďalšia etapa** na stránke **Projekt**. |
| Správa zdrojov | 2224817 | Funkcia na rozšírenie rezervácií má predvolene vybratý správny stav rezervácie. |
| Zadanie času | 2202476 | Stránka **Zadanie času** teraz používa reaktívne ovládanie mriežky a opravuje problémy, ako je nesprávne zarovnanie mriežky. |
| Zadanie času | 2223377 | Zadanie času je skryté v sekcii **Súvisiace** na stránke **Rezervovateľný zdroj**, aby pri používaní nedošlo k zmätkom. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | V scenároch Project Operations na základe zdrojov: nemôžete konvertovať cenovú ponuku na využitú v dôsledku chyby integrácie. |
| Projektový manažment a účtovníctvo | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | Project Operations: pri pokuse o priradenie riadku zmluvy k ID projektu sa zobrazí chybové hlásenie z dôvodu kontroly prekrývania riadkov zmluvy a typov transakcií. |
| Projektový manažment a účtovníctvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** nastaví fakturačnú adresu zdroja financovania od iného zákazníka. |
| Cestovanie a výdavky | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Môže sa vyskytnúť chyba zverejnenia súvisiaca s nastavením najazdených kilometrov. |
| Cestovanie a výdavky | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Funkcia **Rozdeliť na osobné** nefunguje pri transakciách s výdavkami v cudzej mene. |
| Cestovanie a výdavky | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | V rozbaľovacej ponuke hodnôt kategórií výdavkov sa delegátom zobrazujú nesprávne kategórie bez ohľadu na to, sú nastavení ako zdroj. |
| Cestovanie a výdavky | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Výkaz medzipodnikových výdavkov nemôžete uložiť z dôvodu chyby **overenia zdroja/kategórie**. |
| Cestovanie a výdavky | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Chybný výpočet počtu najazdených kilometrov v zaúčtovaní výkazu výdavkov má rozdelené riadky. |
| Cestovanie a výdavky | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Keď je zahrnutá daň z obratu a typ ofsetového účtu pri spôsobe platby, nemôžete zaúčtovať výkaz medzipodnikových výdavkov **Pracovník**. |
| Cestovanie a výdavky | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Vrátila sa späť dátová entita **TrvRequisitionLine** a s ňou súvisiaci jedinečný index. |
| Cestovanie a výdavky | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Výkaz o výdavkoch podporuje tvorbu a aktualizáciu riadkov zdrojových dokumentov. |
| Cestovanie a výdavky | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | V medzipodnikovom scenári sa zobrazuje nesprávny výkaz vedľajšej účtovnej knihy, ak sa daň z obratu zaúčtuje cieľovej právnickej osobe. |
| Cestovanie a výdavky | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | Project Operations: odhady výdavkov sa neodstránia z aplikácie Finance, keď sa odstránia z Dataverse. |
| Cestovanie a výdavky | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Ak je kategóriou výdavkov neprojektová kategória, finančné dimenzie, ktoré sú vybrané na stránke **Výdavky**, sa neskopírujú do výkazu výdavkov. |
