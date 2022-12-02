---
title: Čo je nové v marci 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Project Operations z marca 2022, pre scenáre založené na zdrojoch/neskladovaných zdrojoch.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910925"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v marci 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

*Platí pre: Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch*

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.30.0.99
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.25

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

Diéty sú teraz podporované v novom a prepracovanom modernom pracovnom priestore výdavkov. Spoločnosti, ktoré používajú diéty, môžu povoliť túto funkciu, aby používateľom poskytli jednoduchý spôsob, ako podať žiadosť o diéty a preplatiť im ich výdavky. Ďalšie informácie nájdete v téme [Výdavky na diéty](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúci zoznam zobrazuje mapy duálneho zapisovania, ktoré boli upravené alebo pridané vo vydaní Project Operations z marca 2022.

| **Mapa entity** | **Aktualizovaná verzia** | **Vytvoril** |
| --- | --- | --- |
| Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations msdyn\_projectvendorinvoicelines | 1.0.0.3 | Mapovania boli aktualizované, aby boli v súlade s entitou riadku faktúry dodávateľa v Dataverse. <br>Neaktivujte verziu mapovania 1.0.0.4. V ďalšej mesačnej aktualizácii bude pripravené na použitie v kombinácii s prostredím Finance verzie 10.0.26. |

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Čas a výdavky | 2388011 | Počas hromadného schvaľovania sa zobrazujú predkladateľom časových položiek komentáre o odmietnutí. |
| Plánovanie a sledovanie projektu | 2495294 | Podrobnosti projektu sa nesmú dať upravovať na stránke **Podrobnosti úlohy**. |
| Fakturácia a tvorba cien | 2499605 | Zmluvné míľniky, ktoré sú vytvorené z míľnikov cenových ponúk, sú nesprávne označené ako len na čítanie. |
| Plánovanie a sledovanie projektu | 2506050 | Ak nedôjde k žiadnej zmene na uloženie, množina operácií zostane nevybavená jednu hodinu. Množina je potom falošne označená ako **Nepodarilo sa**, pričom by mala byť dokončená okamžite. |
| Fakturácia a tvorba cien | 2507401 | Predvolené zmluvné jednotky sú v projektoch nesprávne zadané z dôvodu nesprávneho ukladania do vyrovnávacej pamäte. |
| Fakturácia a tvorba cien | 2541660 | **Overenie vytvorenia predajnej objednávky** v duálnom zápise by malo byť iba pre zákazky založené na projekte. |
| Fakturácia a tvorba cien | 2552745 | Daň sa nerozdeľuje medzi zákazníkov, ktorí si nastavili pravidlá rozdelenej fakturácie. |
| Fakturácia a tvorba cien | 2558859 | Vylepšené chybové hlásenia pri nastavovaní cenových dimenzií. |
| Fakturácia a tvorba cien | 2558933 | **Import z odhadov projektu** zlyhá, keď sa **msdyn\_project** pridá ako cenová dimenzia. |
| Fakturácia a tvorba cien | 2559101 | Odstránenie parametrov projektu nie je blokované a spôsobuje problémy. |
| Správa príležitostí | 2570390 | Doplnok s duálnym zápisom vynucuje typ obchodného vzťahu pre cenové ponuky, objednávky a príležitosti **Zákazník**, aj keď tento typ obchodného vzťahu nie je správny. |
| Fakturácia a tvorba cien | 2586097 | Skutočné rozdelené fakturované náklady sa nestornujú, keď je projekt odstránený z riadku projektovej zmluvy. |
| Fakturácia a tvorba cien | 2589619 | Daň zo zapísaného materiálu sa prenáša do skutočných nevyfakturovaných predajov a faktúry. |
| Správa príležitostí | 2594015 | Cenovú ponuku nemožno uzavrieť ako získanú pre zákazníkov, ktorí majú platobné podmienky **Net60** . |
| Plánovanie a sledovanie projektu | 2595841 | V Project for the Web sa používateľom zobrazí chybové hlásenie o chýbajúcom **msdyn\_actualstart** keď vytvoria novú požiadavku na zdroj. |
| Čas a výdavky | 2602511 | Pole **Odmietnuté používateľom** pre časové záznamy zobrazuje **Systém** namiesto menovaného používateľa ako odmietajúceho. |
| Čas a výdavky | 2602528 | Schvaľovateľ projektu môže schváliť čas na projektoch, kde nie je uvedený ako schvaľovateľ. |
| Fakturácia a tvorba cien | 2608550 | Opravnú faktúru je možné potvrdiť aj vtedy, ak nedošlo k žiadnym zmenám oproti originálu. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Medzi Finance a Project Operations je nesúlad v povolenej dĺžke poľa **ID kategórie**. |
| Projektový manažment a účtovníctvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekty s pevnou cenou nemožno eliminovať, keď je pole **Fakturácia na účet** nastavené na **Zisk a strata** a používa sa princíp **Dokončené percento**. |
| Projektový manažment a účtovníctvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nesprávna predvolená skupina dane z obratu je zadaná z nastavenia projektu na riadkoch výdavkov v denníku integrácie Project Operations. |
| Projektový manažment a účtovníctvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | V integrovanom nasadení s Project Operations nemôžete upravovať dimenzie hlavičky návrhu faktúry za projekt. |
| Projektový manažment a účtovníctvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Medzipodnikové faktúry dodávateľov nesmú byť integrované s Dataverse. |
| Projektový manažment a účtovníctvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Existuje nesúlad v mene zostatkov zákazníka a v mene vykazovania. |
| Projektový manažment a účtovníctvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektovú faktúru môžete zaúčtovať aj vtedy, ak má zákazník pozastavené všetky faktúry. |
| Projektový manažment a účtovníctvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Tlačidlo **Odstrániť všetky riadky** chýba v návrhoch projektových faktúr, ktoré majú zobrazenia **Hlavička** a **Riadky**. |
| Projektový manažment a účtovníctvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Keď zaúčtujete faktúru dodávateľa, vyskytne sa nasledujúca chyba: „Účtovný dátum faktúry musí byť v rovnakom účtovnom roku ako súvisiaca nákupná objednávka. Spustite proces na konci roka nákupnej objednávky alebo zmeňte dátum na aktuálny účtovný rok.“ |
| Cestovanie a výdavky | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Viazané náklady na projekt sa neuvoľnia po uvoľnení viazaných nákladov cestovného príkazu. |
| Cestovanie a výdavky | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Pri odoslaní správy o výdavkoch sa vyskytne nasledujúca chyba: „Sledovanie zásobníka: Spoločnosť neexistuje.“ |
| Cestovanie a výdavky | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Predvolená hodnota **ID projektu** sa neuvádza vo výkazoch výdavkov, keď je v projekte vybraný parameter **Vyžadovať aktivitu pre denník**. |
| Cestovanie a výdavky | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Tlačidlo **Zaúčtovať výdavky** nefunguje správne v Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách. |
| Cestovanie a výdavky | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Vyskytol sa problém so **Sadzba za míľu** pre správu o výdavkoch na najazdené kilometre, ktorá zahŕňa cestujúcich. |
| Cestovanie a výdavky | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Sadzby najazdených kilometrov pre zamestnancov nie sú správne spočítané, keď sa používajú dva rôzne typy vozidiel v kategórii výdavkov **Úrovne najazdených kilometrov**. |
| Cestovanie a výdavky | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Vyhľadávanie pre pole **Projekt** na riadku cestovnej žiadanky nevracia správny zoznam projektov. |
| Cestovanie a výdavky | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Prehľad najazdených kilometrov** zobrazuje varovanie vo výkazoch výdavkov. |
| Cestovanie a výdavky | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Služba optického rozpoznávania znakov na účtenke (OCR) nefunguje z dôvodu problému s adresou URL výdavkovej služby OCR. |
| Cestovanie a výdavky | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Keď je povolená funkcia **Schopnosť rýchlo rozpísať opakujúce sa výdavky**, sumy v riadkoch položiek vo výkazoch výdavkov sa menia sumy zakaždým, keď sa otvorí stránka **Rozpísať**. |
| Cestovanie a výdavky | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Výkaz výdavkov nemôžete odstrániť, ak má priebežný zoznam viac ako jedného schvaľovateľa. |

## <a name="removed-and-deprecated-features"></a>Odstránené a zastarané funkcie

Článok [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) popisuje funkcie, ktoré boli odstránené alebo ktorých podpora bola ukončená pre Dynamics 365 Project Operations.

- Odstránená funkcia už v produkte nie je k dispozícii.
- Zastaraná funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Oznámenie o ukončení podpory sa zobrazí v článku [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) 12 mesiacov pred odstránením akejkoľvek funkcie z produktu.

Pre zásadné zmeny, ktoré ovplyvňujú iba čas kompilácie, ale sú binárne kompatibilné s izolovaným prostredím a produkčným prostredím, bude čas ukončenia podpory kratší ako 12 mesiacov. Tieto zmeny sú zvyčajne funkčné aktualizácie, ktoré je potrebné vykonať v kompilátore.
