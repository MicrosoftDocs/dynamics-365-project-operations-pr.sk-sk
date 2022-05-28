---
title: Čo je nové v marci 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú dostupné vo vydaní Project Operations z marca 2022 pre scenáre založené na zdrojoch/nezásobách.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: afd5149cda909b5367e7f12382423179d7e19267
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600761"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v marci 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

*Platí pre: Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch*

Táto téma sa týka nasledujúcich komponentov a verzií Microsoftu Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.30.0.99
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.25

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

Denné diéty sú teraz podporované v novom a prepracovanom modernom pracovnom priestore. Spoločnosti, ktoré používajú denné diéty, môžu povoliť túto funkciu, aby používateľom poskytli jednoduchý spôsob, ako podať žiadosť o diéty a nechať im preplatiť ich výdavky. Viac informácií nájdete v časti [Denné výdavky](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúci zoznam zobrazuje mapy s duálnym zápisom, ktoré boli upravené alebo pridané vo vydaní Project Operations z marca 2022.

| **Mapa entity** | **Aktualizovaná verzia** | **Vytvoril** |
| --- | --- | --- |
| Projektové operácie integrácia projekt dodávateľ faktúra riadok export entity msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Mapovania boli aktualizované tak, aby boli v súlade s entitou riadku faktúry dodávateľa v Dataverse. <br>Neaktivujte verziu mapovania 1.0.0.4. V ďalšej mesačnej aktualizácii bude pripravený na použitie v kombinácii s finančným prostredím verzie 10.0.26. |

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste si prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spustení mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Čas a výdavky | 2388011 | Počas hromadného schvaľovania zobrazte predkladateľom zadania času komentáre o odmietnutí. |
| Plánovanie a sledovanie projektu | 2495294 | Podrobnosti projektu nesmú byť upraviteľné na **Podrobnosti úlohy** stránku. |
| Fakturácia a tvorba cien | 2499605 | Zmluvné míľniky, ktoré sú vytvorené z cenových míľnikov, sú nesprávne označené ako len na čítanie. |
| Plánovanie a sledovanie projektu | 2506050 | Ak nedôjde k žiadnej zmene na uloženie, sada operácií zostane nevybavená jednu hodinu. Súprava je potom falošne označená ako **Nepodarilo sa**, pričom by mala byť dokončená okamžite. |
| Fakturácia a tvorba cien | 2507401 | Predvolené zmluvné jednotky sú v projektoch nesprávne zadané z dôvodu nesprávneho ukladania do vyrovnávacej pamäte. |
| Fakturácia a tvorba cien | 2541660 | **Overenie vytvorenia zákazky odberateľa** v duálnom zápise by malo byť iba pre zákazky založené na projekte. |
| Fakturácia a tvorba cien | 2552745 | Daň sa nerozdeľuje medzi zákazníkov, ktorí si nastavili pravidlá rozdelenej fakturácie. |
| Fakturácia a tvorba cien | 2558859 | Vylepšené chybové hlásenia pri nastavovaní dimenzií cien. |
| Fakturácia a tvorba cien | 2558933 | **Importovať z odhadov projektu** zlyhá, keď **msdyn\_ projektu** sa pridáva ako cenová dimenzia. |
| Fakturácia a tvorba cien | 2559101 | Odstránenie parametrov projektu nie je blokované a spôsobuje problémy. |
| Správa príležitostí | 2570390 | Zásuvný modul s dvojitým zápisom núti typ účtu na cenové ponuky, objednávky a príležitosti **Zákazník**, aj keď tento typ účtu nie je správny. |
| Fakturácia a tvorba cien | 2586097 | Skutočné rozdelené fakturované náklady nie sú stornované, keď je projekt odstránený z riadku projektovej zmluvy. |
| Fakturácia a tvorba cien | 2589619 | Daň zo zapísaného materiálu sa prenáša do skutočných nevyfakturovaných predajov a faktúry. |
| Správa príležitostí | 2594015 | Cenovú ponuku nemožno uzavrieť ako vyhratú pre zákazníkov, ktorí tak urobili **Net60** platobné podmienky. |
| Plánovanie a sledovanie projektu | 2595841 | V Project for the Web sa používateľom zobrazí chybové hlásenie o chýbajúcom **msdyn\_ skutočný štart** keď vytvoria novú požiadavku na zdroj. |
| Čas a výdavky | 2602511 | The **Odmietnuté používateľom** pole pre časové záznamy zobrazuje **systém** namiesto menovaného používateľa ako odmietajúceho. |
| Čas a výdavky | 2602528 | Schvaľovateľ projektu môže schváliť čas na projektoch, kde nie je uvedený ako schvaľovateľ. |
| Fakturácia a tvorba cien | 2608550 | Opravnú faktúru je možné potvrdiť aj vtedy, ak nedošlo k žiadnym zmenám oproti originálu. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektový manažment a účtovníctvo na Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Medzi finančnými a projektovými operáciami je nesúlad v povolenej dĺžke **ID kategórie** lúka. |
| Projektový manažment a účtovníctvo | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Projekty s pevnou cenou nemožno eliminovať, keď **Fakturácia na účet** pole je nastavené na **Zisk a strata** a **Dokončené percento** používa sa princíp. |
| Projektový manažment a účtovníctvo | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Nesprávna predvolená skupina dane z obratu je zadaná z nastavenia projektu na riadkoch výdavkov v denníku integrácie projektových operácií. |
| Projektový manažment a účtovníctvo | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | V integrovanom nasadení s projektovými operáciami nemôžete upravovať dimenzie hlavičky návrhu faktúry za projekt. |
| Projektový manažment a účtovníctvo | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Medzipodnikové faktúry dodávateľov nesmú byť integrované s Dataverse. |
| Projektový manažment a účtovníctvo | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Vyskytuje sa nesúlad v mene zostatkov zákazníkov a mene vykazovania. |
| Projektový manažment a účtovníctvo | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projektovú faktúru môžete zaúčtovať aj vtedy, ak má zákazník pozastavené všetky faktúry. |
| Projektový manažment a účtovníctvo | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | The **Odstráňte všetky riadky** tlačidlo chýba v návrhoch projektových faktúr, ktoré majú **Hlavička** a **Čiary** názory. |
| Projektový manažment a účtovníctvo | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Keď zaúčtujete faktúru dodávateľa, vyskytne sa nasledujúca chyba: „Účtovný dátum faktúry musí byť v rovnakom účtovnom roku ako súvisiaca nákupná objednávka. Spustite proces na konci roka nákupnej objednávky alebo zmeňte dátum na aktuálny účtovný rok." |
| Cestovanie a výdavky | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Záväzné náklady na projekt nie sú uvoľnené po uvoľnení viazaných nákladov cestovnej požiadavky. |
| Cestovanie a výdavky | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Pri odoslaní správy o výdavkoch sa vyskytne nasledujúca chyba: "Sledovanie zásobníka: Spoločnosť neexistuje." |
| Cestovanie a výdavky | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Predvolená hodnota **ID projektu** sa neuvádza vo výkazoch výdavkov, keď **Vyžadovať aktivitu pre denník** parameter je vybraný v projekte. |
| Cestovanie a výdavky | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | The **Zaúčtovať výdavky** tlačidlo nefunguje správne v projektových operáciách pre scenáre so zdrojmi/bez zásob. |
| Cestovanie a výdavky | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Vyskytol sa problém s **Sadzba za míľu** pre správu o nákladoch na kilometre, ktorá zahŕňa cestujúcich. |
| Cestovanie a výdavky | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Sadzby najazdených kilometrov pre zamestnancov nie sú správne spočítané, keď sa v systéme používajú dva rôzne typy vozidiel **Stupne počtu najazdených kilometrov** výdavková kategória. |
| Cestovanie a výdavky | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Hľadanie pre **Projekt** pole na riadku cestovnej požiadavky nevracia správny zoznam projektov. |
| Cestovanie a výdavky | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Prehľad najazdených kilometrov** zobrazuje varovanie vo výkazoch výdavkov. |
| Cestovanie a výdavky | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Služba optického rozpoznávania znakov (OCR) potvrdenia nefunguje pre problém s adresou URL výdavkovej služby OCR. |
| Cestovanie a výdavky | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Keď **Schopnosť rýchlo rozpísať opakujúce sa výdavky** Ak je aktivovaná funkcia, sumy v riadkoch položiek vo výkazoch výdavkov sa menia sumy zakaždým, keď **Itemize** stránka sa otvorí. |
| Cestovanie a výdavky | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Výkaz výdavkov nemôžete odstrániť, ak má priebežný zoznam viac ako jedného schvaľovateľa. |

## <a name="removed-and-deprecated-features"></a>Odstránené a zastarané funkcie

The [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) téma popisuje funkcie, ktoré boli odstránené alebo zastarané Dynamics 365 Project Operations.

- Odstránená funkcia už v produkte nie je k dispozícii.
- Zastaraná funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Oznámenie o ukončení podpory sa zobrazí v [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) tému 12 mesiacov pred odstránením akejkoľvek funkcie z produktu.

Pre prerušenie zmien, ktoré ovplyvňujú iba čas kompilácie, ale sú binárne kompatibilné so sandboxom a produkčným prostredím, bude čas ukončenia podpory kratší ako 12 mesiacov. Tieto zmeny sú zvyčajne funkčné aktualizácie, ktoré je potrebné vykonať v kompilátore.
