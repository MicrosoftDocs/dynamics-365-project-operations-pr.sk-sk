---
title: Čo je nové vo februári 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú dostupné vo vydaní Project Operations z februára 2022 pre scenáre založené na zdrojoch/nezásobách.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 76ae00517c857415c89d7a03f421686dad28da93
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600853"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové vo februári 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

*Platí pre: Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch*

Táto téma sa týka nasledujúcich komponentov a verzií Microsoftu Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.28.0.120
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.24

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

- Od tohto vydania môžete do jedného projektu pridať až 300 členov tímu. Predtým bol limit na počet členov tímu 150. Viac informácií nájdete v časti [Limity projektu](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>Aktualizácie máp s dvojitým zápisom Project Operations

Nasledujúci zoznam zobrazuje mapy s dvojitým zápisom, ktoré boli upravené alebo pridané vo vydaní Project Operations z februára 2022.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| --- | --- | --- |
| Integrácia projektových operácií Výdavky na projekt exportný subjekt (msdyn\_ výdavky) | 1.0.0.3 | Rozšírené o synchronizáciu projektových aktivít na Dataverse. |

Aktuálny zoznam a verzie máp s dvojitým zápisom Project Operations nájdete na [Verzie máp s dvojitým zápisom Project Operations](../environment/resource-dual-write-maps.md).

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste si prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spustení mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2415109 | Predvolená hodnota v **Platobné podmienky operácií** pole musí byť zákaznícky záznam projektovej zmluvy a záznam proforma faktúry. |
| Fakturácia a tvorba cien | 2497369 | Oprava materiálu musí nasledovať hodnotu dátumu v **Oprava** parametre. |
| Fakturácia a tvorba cien | 2498697 | Vylepšená konfigurácia zabezpečenia pre **Vyvolanie vstupu času**. |
| Fakturácia a tvorba cien | 2513824 | Pre scenáre založené na zdrojoch nesmie ID kategórie transakcie presiahnuť 28 znakov v Project Operations. |
| Fakturácia a tvorba cien | 2517455 | The **Obnoviť transakcie riadkov faktúr** akcia nesmie byť spustená viackrát súčasne pre tú istú faktúru. |
| Fakturácia a tvorba cien | 2517465 | The **Deaktivujte podrobnosti o riadku faktúry** akcia je zablokovaná, pretože nie je podporovaná. |
| Fakturácia a tvorba cien | 2556660 | Opravená kontrola účinnosti dátumu, ktorá sa vykonáva v cenníku, ktorý je priložený k záznamu parametrov projektu. |
| Správa príležitostí | 2369202 | Opravená obchodná logika, ktorá overuje, že cenníky, ktoré majú prekrývajúce sa dátumy účinnosti, možno pripojiť k tej istej zmluve o projekte. |
| Správa príležitostí | 2385965 | Opravené správanie na **zákazníkov** záložku **Projektová zmluva** pri výbere **Uložiť a zavrieť**. |
| Čas a výdavky | 2538503 | Projektová úloha musí byť dostupná v **Skutočnosti projektu** účtovnej jednotke po zaúčtovaní výkazu výdavkov. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektový manažment a účtovníctvo na Dynamics 365 Finance

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Počas importu dobropisov dodávateľa sa vyskytne chyba. V chybovom hlásení sa uvádza: "Zadržaná suma nemôže byť väčšia ako zostávajúca čistá suma." |
| Projektový manažment a účtovníctvo | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Ak návrh faktúry obsahuje akékoľvek transakcie s nulovým poplatkom, ktoré sú skutočnými nevyfakturovanými predajmi, fakturácia nemôže prebehnúť. |
| Projektový manažment a účtovníctvo | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Zaúčtovaná cena nie je správna po aktualizácii kúpnej ceny a **Aktivujte riadenie zmien** je umožnené.|
| Projektový manažment a účtovníctvo | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Odhad účtovania pre projekt s pevnou cenou používa nesprávnu menu a sumu v doklade odhadu, aj keď **Povoliť menu projektovej zmluvy pre výpočet odhadu** funkcia je povolená. |
| Projektový manažment a účtovníctvo | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Rozšírenie** by nemali volať na povolenie sledovania zmien bez zachytenia výnimiek pre entity, ktoré majú konfiguračné kľúče, ktoré nie sú povolené. |
| Projektový manažment a účtovníctvo | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Dávková úloha je opravená, keď sa zaúčtuje viacero rozšírených žurnálov a vyskytne sa chyba. |
| Cestovanie a výdavky | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Z dôvodu problému s vysporiadaním, ktorý súvisí s preddavkami v hotovosti vo výkazoch výdavkov, suma dane nie je súčasťou preddavku v hotovosti. |
| Cestovanie a výdavky | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | Informácie o dani z predaja nie sú zahrnuté na **Výdavok - Zaúčtované transakcie** správa. |
| Cestovanie a výdavky | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | The **Požadujú sa potvrdenky** porušenie politiky výdavkov nesprávne zobrazuje varovanie vo výkazoch výdavkov. |
| Cestovanie a výdavky | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Transakcia projektu nezahŕňa nenávratnú daň z obratu v celkovej sume predaja, ak je transakcia výsledkom nákladov na najazdené kilometre. |
| Cestovanie a výdavky | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Keď riadok s položkami obsahuje daň, nemôžete zmeniť dátum riadka položky a vyskytne sa chyba stavu zdrojového dokumentu. |

## <a name="removed-and-deprecated-features"></a>Odstránené a zastarané funkcie

The [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) téma popisuje funkcie, ktoré boli odstránené alebo zastarané Dynamics 365 Project Operations.

- Odstránená funkcia už v produkte nie je k dispozícii.
- Zastaraná funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Oznámenie o ukončení podpory sa zobrazí v [Odstránené alebo zastarané funkcie v Project Operations](removed-depreciated-features-project.md) tému 12 mesiacov pred odstránením akejkoľvek funkcie z produktu.

Pre prerušenie zmien, ktoré ovplyvňujú iba čas kompilácie, ale sú binárne kompatibilné so sandboxom a produkčným prostredím, bude čas ukončenia podpory kratší ako 12 mesiacov. Tieto zmeny sú zvyčajne funkčné aktualizácie, ktoré je potrebné vykonať v kompilátore.
