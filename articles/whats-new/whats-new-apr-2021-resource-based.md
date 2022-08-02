---
title: Čo je nové v apríli 2021 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Project Operations z apríla 2021 pre scenáre založené na zdrojoch alebo bez zásob.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 490b7aa38bfdfbcdce21a21e582296e4ce15aeeb
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029273"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v apríli 2021 – Project Operations pre scenáre založené na zdrojoch/neskladovaných položkách

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa vzťahuje na nasledujúce Dynamics 365 Project Operations komponenty a verzie:

- Project Operations v prostredí Dataverse verzie 4.9.0.221
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.17

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

V tomto vydaní sú zahrnuté nasledujúce funkcie:

- Neskladované materiály pre projekty. Medzi kľúčové schopnosti patrí:
  - Odhad a naceňovanie neskladovaných materiálov počas predajného cyklu projektu. Viac informácií sa dozviete v článku [Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sledovanie použitia neskladovaných materiálov počas dodania projektu. Viac informácií sa dozviete v článku [Zaznamenanie využitia materiálu na projektoch a projektových úlohách](../material/material-usage-log.md).
  - Fakturácia nákladov na použité neskladované materiály. Ďalšie informácie nájdete v článku [Správa backlogu pre fakturáciu](../proforma-invoicing/manage-billing-backlog.md).
  - Informácie o konfigurácii tejto funkcie nájdete v časti [Konfigurovať neskladované materiály a čakajúce faktúry dodávateľov](../procurement/configure-materials-nonstocked.md)
- Fakturácia na základe úloh: Pridaná možnosť priradiť projektové úlohy k riadkom zmluvy projektu, čím ich vystavuje rovnakému spôsobu fakturácie, frekvencii fakturácie a zákazníkom ako sú na riadku zmluvy. Toto priradenie zaisťuje presnú fakturáciu, účtovníctvo, odhad výnosov a rozpoznávanie tak, aby fungovalo v súlade s týmto nastavením na projektových úlohách.
- Nové rozhrania API v Dynamics 365 Dataverse umožňuje vytvárať, aktualizovať a mazať operácie s **Entitami plánovania**. Viac informácií sa dozviete v časti [Používanie rozhraní API na vykonávanie operácií s entitami plánovania](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúci zoznam zobrazuje mapy duálneho zapisovania, ktoré boli upravené alebo pridané vo vydaní Project Operations z apríla 2021.

| **Mapa entity** | **Aktualizovaná verzia** | **Vytvoril** |
| --- | --- | --- |
| Skutočné hodnoty integrácie Project Operations (msdyn\_actuals) | 1.0.0.14 | Mapa bola upravená na synchronizáciu skutočných hodnôt projektu. |
| Entita integrácie Project Operations pre odhady výdavkov (msdyn\_estimateslines) | 1.0.0.2 | Pridaná synchronizácia riadku projektovej zmluvy do finančných a prevádzkových aplikácií pre podporu fakturácie na základe úloh. |
| Entita integrácie Project Operations pre odhady hodín (msdyn\_resourceassignments) | 1.0.0.5 | Pridaná synchronizácia riadku projektovej zmluvy do finančných a prevádzkových aplikácií pre podporu fakturácie na základe úloh. |
| Tabuľka integrácie Project Operations pre materiálové odhady (msdyn\_estimatelines) | 1.0.0.0 | Nová tabuľková mapa na synchronizáciu odhadov materiálu Dataverse na finančné a prevádzkové aplikácie. |
| Entita exportu faktúr projektu dodávateľa projektu Project Operations (msdyn\_projectvendorinvoices) | 1.0.0.0 | Nová tabuľková mapa na synchronizáciu hlavičiek faktúr dodávateľov z finančných a prevádzkových aplikácií do Dataverse. |
| Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations (msdyn\_projectvendorinvoicelines) | 1.0.0.0 | Nová tabuľková mapa na synchronizáciu riadkov faktúr dodávateľa z finančných a prevádzkových aplikácií do Dataverse. |

Pri aktualizácii operácií projektu by ste mali vždy spustiť najnovšiu verziu mapy vo svojom prostredí a povoliť všetky súvisiace mapy tabuliek Dataverse verzia riešenia a financií a prevádzky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy môžete aktivovať výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém so spustením mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-in-dynamics-365-dataverse"></a>Project Operations v Dynamics 365 Dataverse

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2124532 | Tlačidlo **Správna faktúra** sa zobrazí na proforma faktúre, keď sa na pôvodnej faktúre nachádza suma preddavku alebo použitá suma preddavku. Tlačidlo sa zobrazuje iba pre prostredia Finance verzie 10.0.19 alebo vyššej. |
| Fakturácia a tvorba cien | 2224568 | Pridaná logika na povolenie prispôsobení, ktoré zahŕňajú vyvolanie doplnku na potvrdenie faktúry. |
| Fakturácia a tvorba cien | 2101098 | Vylepšená logika predvolených polí faktúry pro forma: **Zasielacia adresa**, **Fakturačné meno** a **Platobné podmienky** teraz získavajú predvolené údaje z príslušného záznamu zákazníka projektovej zmluvy. |
| Fakturácia a tvorba cien | 2021413 | Aktualizované polia **Skutočné náklady** a **Predaj** v entite **Úloha** zahŕňajú hodnoty predaja z nefakturovaných a fakturovaných výdavkov za úlohy. |
| Fakturácia a tvorba cien | 2182110 | Pri kopírovaní projektovej zmluvy sa ID riadku zmluvy regeneruje v cieľovej projektovej zmluve, aby sa zabezpečilo, že je jedinečné. |
| Správa príležitostí | 2186741 | Pridané overovania na zabezpečenie, že pole **Pôvod** a **Typ transakcie** nie je možné aktualizovať o podrobnosti riadka existujúcej cenovej ponuky. |
| Správa príležitostí | 2191353 | Medzníky sa nesmú vytvárať na riadku zmluvy s časom a materiálom. |
| Správa príležitostí | 2216956 | Opravené problémy s **aktualizáciou cien**. |
| Plánovanie a sledovanie | 2182979 | Vylepšená funkcia kopírovania projektu, aby sa zabezpečilo kopírovanie riadkov odhadu výdavkov z pôvodného projektu. |
| Plánovanie a sledovanie | 2184144 | Vylepšená funkcia kopírovania projektu, aby sa zabezpečilo kopírovanie názvu pozície zdroja z pôvodného projektu. |
| Plánovanie a sledovanie | 2184799 | Kópia projektu: Sprísnená kontrola, ktorá zabezpečí, že odhadovaný dátum začatia nebude možné zmeniť, keď prebieha kopírovanie. |
| Plánovanie a sledovanie | 2185134 | Kópia projektu: Odhadovaný dátum začatia cieľového projektu je nastavený na dnešný dátum. |
| Plánovanie a sledovanie | 2196373 | Kópia projektu: Zaistí, aby sa v projektovom tíme neduplikovali záznamy projektového manažéra a člena tímu. |
| Plánovanie a sledovanie | 2211833 | Kópia projektu: Priradenia zdrojov sa skopírujú z úlohy zdrojového projektu do cieľového projektu. |
| Plánovanie a sledovanie | 2186541 | Opravené problémy v mriežke **Odhady** pri zoskupovaní podľa zdrojov. |
| Plánovanie a sledovanie | 2166906 | Kategória transakcie z úlohy musí byť skopírovaná do entity **Priradenie zdroja**. |
| Správa zdrojov | 2125362 | Opravené problémy s vytváraním všeobecného člena tímu pomocou metódy prideľovania podľa hodín. |
| Čas a výdavky | 2113603 | Opravený problém súvisiaci s prispôsobením pri odstraňovaní atribútov zo stránky **Zadanie času**. Systém teraz pred prístupom pomocou skriptu skontroluje, či atribút na stránke existuje. |
| Čas a výdavky | 2204377 | Po výbere **Kopírovať týždeň** počas zadávania času sa musia skopírované časové rozvrhy zobraziť automaticky. |
| Čas a výdavky | 2209059 | Pole **Stav** je možné upraviť pre časové rozvrhy Dynamics 365 Field Service. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Eliminácia reverzného odhadu nefunguje v sekcii **Pravidelné**.  |
| Projektový manažment a účtovníctvo | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Funkcia **Úprava účtovníctva** vytvára problém s účtami hlavnej účtovnej knihy, ktoré majú vybranú možnosť **Nepovoliť ručné zadávanie**. |
| Projektový manažment a účtovníctvo | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Pridaná obchodná logika na spracovanie opravných faktúr vrátane sumy preddavku alebo použitej sumy preddavku. |
| Projektový manažment a účtovníctvo | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | Zaúčtovanie hodnoty predaja z nedokončenej výroby v rámci medzipodnikovej fakturácie projektu vyberie neočakávaný účet. |
| Projektový manažment a účtovníctvo | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Pri práci s preddavkami v Project Operations zmena pôvodného projektu na základe zmluvy po fakturácii preddavkov spôsobí problémy s prichádzajúcimi odpočtami. |
| Projektový manažment a účtovníctvo | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | V Project Operations by odstránenie projektu zo zmluvy malo v prípade potreby resetovať predvolený projekt zmluvy. |
| Projektový manažment a účtovníctvo | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | V Project Operations sa v medzipodnikovej faktúre v zozname **Pridať riadok** zobrazujú nesprávne riadky výdavkov. |
| Projektový manažment a účtovníctvo | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | V rámci Project Operations nie je stránka **Kúpna zmluva** viditeľná v právnych entitách zameraných na financie, ktoré sú integrované do Project Operations. |
| Projektový manažment a účtovníctvo | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Z dôvodu chyby integrácie Dataverse nemôžete previesť cenovú ponuku na získanú v Project Operations. |
| Projektový manažment a účtovníctvo | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** môže nastaviť fakturačnú adresu zdroja financovania od iného zákazníka.  |
| Projektový manažment a účtovníctvo | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | V Project Operations sa pri vytváraní účtovacej faktúry za transakciu nevyberú žiadne dimenzie. |
| Čas a výdavky | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Zostatok peňažnej zálohy sa neaktualizuje pre výkaz výdavkov, ak je schválený a zaúčtovaný riadok po riadku. |
| Cestovanie a výdavky | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Dane za jednotlivé položky zostáv medzipodnikových výdavkov nie sú vypočítané správne. |
| Cestovanie a výdavky | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Ďalšie polia súvisiace s projektmi sa zobrazia na prepracovanej stránke **Výkazy medzipodnikových výdavkov**. |
| Cestovanie a výdavky | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Nesprávne chybové hlásenie sa vyskytuje na hlavičkových dokladoch výkazov výdavkov. |
| Cestovanie a výdavky | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Výkaz výdavkov sa nesprávne zaúčtuje v medzipodnikovom scenári, ak sa daň z obratu zaúčtuje cieľovej právnickej osobe. |
| Cestovanie a výdavky | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Dátumy odoslania výkazov sa nevytlačia na schválených výkazoch výdavkov. |
| Cestovanie a výdavky | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Polia **Dátum schválený** a **Dátum zamietnutý** sa nevyplnia po schválení výdavkov. |
| Cestovanie a výdavky | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Cestovná žiadanka vytvorená pre jedného pracovníka sa môže použiť pre výkaz výdavkov iného pracovníka. |
| Cestovanie a výdavky | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Pri pridávaní nového riadku výdavkov sú kategórie výdavkov uzamknuté. |
| Cestovanie a výdavky | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Položkovanie už rozdelených riadkov výkazu výdavkov vedie k neúplnému zaúčtovaniu dokladu Záväzky\Hlavná účtovná kniha a rozdelí Prieskumníka zdrojov účtovníctva, pretože **TRVEXPTRANS.SOURCEDOCUMENTLINE** je duplikovaný. |
| Cestovanie a výdavky | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Pravidlá týkajúce sa cestovných žiadaniek nepracujú podľa očakávaní. |
| Cestovanie a výdavky | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Názov účtu dodávateľa sa nezobrazuje v zaúčtovaných projektových transakciách pre výkazy výdavkov. |
| Cestovanie a výdavky | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | V časti Project Operations nemôžete schváliť čas s úlohou pre medzipodnikový projekt. |
| Cestovanie a výdavky | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Kategória vrátenia platby vopred v hotovosti neaktualizuje zostatky platieb vopred v hotovosti po zaúčtovaní. |
| Cestovanie a výdavky | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Predajná cena sa nesprávne počíta vo výkazoch výdavkov, ktoré boli vytvorené v cudzej mene pomocou importovaných transakcií kreditnou kartou a sú spojené s projektom. |
| Cestovanie a výdavky | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Vrátenie späť dátovej entity **TrvRequisitionLine** a súvisiaceho jedinečného indexu. |
| Cestovanie a výdavky | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Pridané vybavenie do generovania **SOURCEDOCUMENTLINE**. |
| Cestovanie a výdavky | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Zobrazuje sa nesprávny výkaz vedľajšej účtovnej knihy v medzipodnikovom scenári, ak sa daň z obratu zaúčtuje cieľovej právnickej osobe. |
| Cestovanie a výdavky | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | V Project Operations sa odhady výdavkov neodstránia z aplikácie Finance, keď sa odstránia z Dataverse. |
| Cestovanie a výdavky | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Ak je kategóriou výdavkov neprojektová kategória, finančné dimenzie vybrané na stránke **Výdavky** sa neskopírujú do výkazu výdavkov. |
