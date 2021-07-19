---
title: Novinky v júni 2021 – Project Operations pre scenáre založené na zdrojoch/nenaskladnení
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní nasadenia Project Operations pre scenáre založené na zdrojoch/nenaskladnení z júna 2021.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 28890238f9debb96786a31f66dd9a219f88a5338
ms.sourcegitcommit: 2f16c2bc7c8350676a6a380c61fffa9958db6a0b
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6293156"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novinky v júni 2021 – Project Operations pre scenáre založené na zdrojoch/nenaskladnení

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

- Project Operations v prostredí Dynamics 365 Dataverse verzie 4.11.0.156 alebo 4.11.0.164.
- Projektový manažment a účtovníctvo v aplikáciách Finance and Operations, verzie prostredia 10.0.19.

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

V tomto vydaní sú zahrnuté nasledujúce funkcie:

- Možnosť mazania [Riadkov návrhu faktúry projektu pre scenáre úprav](../invoicing/correct-project-invoice-proposals.md).
- Rozdelené riadky výdavkov odrážajú názvy podkategórií v prehľade výdavkov [Prepracované zostavy o nákladoch – nové funkcie](../expense/expense-reports-reimagined.md#new-features).
- Spôsob platby je k dispozícii na paneli nových výdavkov pri vytváraní nových výdavkov.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. 

Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácií verzie svojho riešenia Project Operations Dataverse a riešenia aplikácií Finance and Operations vždy spustite najnovšiu verziu mapy svojho prostredia a aktivovať všetky súvisiace tabuľkové mapy. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť na stránke **Duálny zápis** v stĺpci **Verzia**. Novú verziu mapy aktivujete stlačením možnosti **Verzie mapových tabuliek**, výberom najnovšej verzie a následným uložením vybranej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spustení mapy, postupujte podľa pokynov v časti [Problém s chýbajúcou tabuľkou na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Riešenie problémov s funkciou duálneho zápisu.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2281417 | Opravený problém týkajúci sa zlyhania akcie automatického vytvárania faktúr prostredníctvom plánu faktúr. |
| Fakturácia a tvorba cien | 2287835 | Vylepšený výkon potvrdenia faktúry. |
| Správa príležitostí | 2222555 | Materiálne odhady spoplatnenosti sa musia správne skopírovať podrobností riadka cenovej ponuky pri použití **Import z Project Estimation**. |
| Správa príležitostí | 2223427 | Prispôsobenia sú teraz povolené pre akciu, **GenerateRetainersFromRetainerScheduleOptions**. |
| Správa príležitostí | 2277528 | Opravený výpočet hodnoty míľnika fakturácie pre riadky zmlúv s viacerými zákazníkmi. |
| Plánovanie a sledovanie projektu | 2226110 | Opravený prerušovaný problém s funkciou **Generovať požiadavku** v mriežke **Projektový tím**. |
| Plánovanie a sledovanie projektu | 2208109 | Používatelia nemôžu vytvoriť projekt v jednej mene so súvisiacimi úlohami v inej mene. |
| Plánovanie a sledovanie projektu | 2258228 | Zoznam polí, ktoré je možné meniť pomocou entít **Plánovanie** pomocou API Plán, bol aktualizovaný. |
| Plánovanie a sledovanie projektu | 2293989 | Správne jazykové a regionálne nastavenia musia byť odovzdané do mriežky **Projektové úlohy**. |
| Správa zdrojov | 2220493 | Opravená používateľská skúsenosť v mriežke **Úloha**, keď rýchlo označíte požiadavku na zdroj ako dokončenú. |
| Správa zdrojov | 2330496 | Opravený problém s načítaním **Tabule plánovania**. (Aktualizácia kvality je k dispozícii vo verzii 4.11.0.164) |
| Čas a výdavky | 2194431 | Mriežka **Zadanie času** musí dodržiavať začiatok týždňa, ako je stanovené v **Nastaveniach systému**. |
| Čas a výdavky | 2277311 | Po odstránení hodnoty z bunky v mriežke **Zadanie času**, kurzor zostane v mriežke. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v rámci Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Poznámky formulára** a **Nastavenie formulára** sa nezobrazuje v rámci **nastavenia riadenia projektu** v právnych entitách Finance, keď sú integrované do Project Operations. |
| Projektový manažment a účtovníctvo | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Predvolený popis je pre DPH prázdny, keď sa **typ účtovania** = **dani z predaja** pri poukážkach na faktúry projektu. |
| Projektový manažment a účtovníctvo | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Dvojité transakcie sa účtujú, ak sa používa v integrácii Dataverse s Project Operations fakturácia na základe úloh. |
| Projektový manažment a účtovníctvo | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Percentuálna hodnota dokončenosti na rozpoznávanie výnosov je nesprávne pri použití integrácie Project Operations. |
| Projektový manažment a účtovníctvo | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | Ak použijete nespracovanú faktúru dodávateľa v integrovanom scenári projektu Project Operations, výnosy sa zdvojnásobia. |
| Projektový manažment a účtovníctvo | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Nemožno zaúčtovať účtovný denník integrácie, ak je pravidlo profilu výnosu nastavené na **Skupina**. |
| Projektový manažment a účtovníctvo | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Nákupnú faktúru nemožno zaúčtovať pre nákupné objednávky projektu, ktoré obsahujú riadky s viacerými mernými jednotkami. |
| Projektový manažment a účtovníctvo | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Predvolenú finančnú dimenziu projektu nemožno aktualizovať pomocou entity údajov projektov **V2**. |
| Projektový manažment a účtovníctvo | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Dokončenie hromadného procesu vytvárania odhadov projektu trvá príliš dlho. |
| Projektový manažment a účtovníctvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Vymazanie zmluvy zároveň vymaže adresu priradenú k zákazníkovi. |
| Cestovanie a výdavky | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Podmienka pracovného postupu schválenia výkazu výdavkov nie je vyhodnotená správne. |
| Cestovanie a výdavky | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Pravidlá výkazu výdavkov nesprávne vyhodnocujú ID projektu. |
| Cestovanie a výdavky | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Akcia **Rozdeliť na osobné pre medzipodnikové nákladové transakcie** nefunguje správne. |
| Cestovanie a výdavky | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Oprávnenia riadka výkazu výdavkov sa náhodne vymazali pri vymazaní určitých požiadaviek na cestovanie. K tomu dôjde, keď sú odpočet správy o výdavkoch a cestovná požiadavka rovnaké. |
| Cestovanie a výdavky | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | S mobilnou aplikáciou Expense je problém, keď pole **ID projektu** je vyžadované zásadami výkazu výdavkov. |
| Cestovanie a výdavky | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Medzipodnikové výdavky spojené s projektom nemožno upraviť. Namiesto toho sa zobrazí nasledujúce chybové hlásenie „Odkaz na objekt nie je nastavený na inštanciu objektu“. |
| Cestovanie a výdavky | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Po zaúčtovaní výkazov výdavkov sa vo vedľajšej účtovnej knihe banky uvedie nesprávne mena a suma. |
| Cestovanie a výdavky | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Vylepšená bola funkcia *Vymazať transakcie kreditnej karty*.  |
| Cestovanie a výdavky | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Daň z obratu, ktorá je zahrnutá v prehľade výdavkov, sa nevypočíta konzistentne, ak je v právnickej osobe zadaná iná mena vykazovania. |
| Cestovanie a výdavky | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Výkon je ovplyvnený pridaním nových cestovných výdavkov v hotovosti. |
| Cestovanie a výdavky | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Pravidlá zásad výdavkov nie sú spustené na výkaze o výdavkoch. |
| Cestovanie a výdavky | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Nahraním novej zdieľanej kategórie pomocou Data Management Framework sa odstránia všetky podkategórie pre všetky zdieľané kategórie. |
| Cestovanie a výdavky | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Keď vytvoríte výdavkový riadok a vyberiete kategóriu, vyskytne sa nasledujúca chyba: „Kombinácia skupiny DPH z predaja DOM a skupiny dane z obratu položky STD je neplatná.“ |
| Cestovanie a výdavky | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | S mobilnou aplikáciou Expense sú problémy so synchronizáciou. |
