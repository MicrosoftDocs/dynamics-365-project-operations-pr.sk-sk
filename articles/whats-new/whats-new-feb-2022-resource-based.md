---
title: Čo je nové vo februári 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Project Operations z februára 2022, pre scenáre založené na zdrojoch/neskladovaných položkách.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8933005"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové vo februári 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

*Platí pre: Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch*

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.28.0.120
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.24

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

- Od tohto vydania môžete do jedného projektu pridať až 300 členov tímu. Predtým bol limit na počet členov tímu 150. Ďalšie informácie nájdete v dokumente [Limity projektu](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Aktualizácie mapy duálneho zapisovania v aplikácii Project Operations

Nasledujúci zoznam zobrazuje mapy duálneho zapisovania, ktoré boli upravené alebo pridané vo vydaní Project Operations z februára 2022.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| --- | --- | --- |
| Entita exportu výdavkov projektu integrácie Project Operations (msdyn\_expenses) | 1.0.0.3 | Rozšírené na synchronizáciu projektových aktivít do Dataverse. |

Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2415109 | Predvolená hodnota v poli **Platobné podmienky operácií** musí byť zákaznícky záznam projektovej zmluvy a záznam proforma faktúry. |
| Fakturácia a tvorba cien | 2497369 | Oprava materiálu musí nasledovať hodnotu dátumu v parametroch **Oprava**. |
| Fakturácia a tvorba cien | 2498697 | Vylepšená konfigurácia zabezpečenia pre **Odvolanie zadania času**. |
| Fakturácia a tvorba cien | 2513824 | Pre scenáre založené na zdrojoch nesmie ID kategórie transakcie presiahnuť 28 znakov v Project Operations. |
| Fakturácia a tvorba cien | 2517455 | Akcia **Obnoviť transakcie v riadku faktúry** nesmie byť povolené spustenie akcie viackrát súčasne pre tú istú faktúru. |
| Fakturácia a tvorba cien | 2517465 | Akcia **Deaktivácia podrobností o riadku faktúry** je zablokovaná, pretože nie je podporovaná. |
| Fakturácia a tvorba cien | 2556660 | Opravená kontrola dátumu účinnosti, ktorá sa vykonáva v cenníku, ktorý je priložený k záznamu parametrov projektu. |
| Správa príležitostí | 2369202 | Opravená obchodná logika, ktorá overuje, že cenníky, ktoré majú prekrývajúce sa dátumy účinnosti, možno pripojiť k tej istej zmluve o projekte. |
| Správa príležitostí | 2385965 | Opravené správanie na karte **Zákazníci** na stránke **Projektová zmluva** pri výbere možnosti **Uložiť a zavrieť**. |
| Čas a výdavky | 2538503 | Projektová úloha musí byť dostupná v entite **Skutočné hodnoty projektu** po zaúčtovaní výkazu výdavkov. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Počas importu dobropisov dodávateľa sa vyskytne chyba. V chybovom hlásení sa uvádza: „Zadržaná suma nemôže byť väčšia ako zostávajúca čistá suma.“ |
| Projektový manažment a účtovníctvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ak návrh faktúry obsahuje akékoľvek transakcie s nulovým poplatkom, ktoré sú skutočnými nevyfakturovanými predajmi, fakturácia sa nemôže uskutočniť. |
| Projektový manažment a účtovníctvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Zaúčtovaná cena nie je správna po aktualizácii nákupnej ceny, keď je povolené **Aktivovať riadenie zmien**.|
| Projektový manažment a účtovníctvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Odhad účtovania pre projekt s pevnou cenou používa nesprávnu menu a sumu v poukaze na odhad, aj keď funkcia **Povoliť menu projektovej zmluvy na výpočet odhadu** je povolená. |
| Projektový manažment a účtovníctvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_Extension** by nemali uskutočňovať volania na povolenie sledovania zmien bez zachytenia výnimiek pre entity, ktoré majú konfiguračné kľúče, ktoré nie sú povolené. |
| Projektový manažment a účtovníctvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Dávková úloha je opravená, keď sa zaúčtuje viacero rozšírených denníkov a vyskytne sa chyba. |
| Cestovanie a výdavky | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Z dôvodu problému s vyrovnaním, ktorý súvisí s peňažnými preddavkami na výkazoch výdavkov, suma dane nie je zahrnutá ako súčasť peňažného preddavku. |
| Cestovanie a výdavky | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informácie o dani z predaja nie sú zahrnuté v zostave **Výdavok – Zaúčtované transakcie**. |
| Cestovanie a výdavky | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Porušenie politiky výdavkov **Požadujú sa potvrdenky** nesprávne zobrazuje varovanie vo výkazoch výdavkov. |
| Cestovanie a výdavky | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transakcia projektu nezahŕňa nenávratnú daň z obratu v celkovej sume predaja, ak je transakcia výsledkom výdavkov na najazdené kilometre. |
| Cestovanie a výdavky | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Keď rozpísaný riadok obsahuje daň, nemôžete zmeniť dátum rozpísania riadka a vyskytne sa chyba stavu zdrojového dokumentu. |

## <a name="removed-and-deprecated-features"></a>Odstránené a zastarané funkcie

Článok [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) popisuje funkcie, ktoré boli odstránené alebo ktorých podpora bola ukončená pre Dynamics 365 Project Operations.

- Odstránená funkcia už v produkte nie je k dispozícii.
- Zastaraná funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Oznámenie o ukončení podpory sa zobrazí v článku [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) 12 mesiacov pred odstránením akejkoľvek funkcie z produktu.

Pre zásadné zmeny, ktoré ovplyvňujú iba čas kompilácie, ale sú binárne kompatibilné s izolovaným prostredím a produkčným prostredím, bude čas ukončenia podpory kratší ako 12 mesiacov. Tieto zmeny sú zvyčajne funkčné aktualizácie, ktoré je potrebné vykonať v kompilátore.
