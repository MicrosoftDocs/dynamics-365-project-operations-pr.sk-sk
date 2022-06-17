---
title: Čo je nové v novembri 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú dostupné vo vydaní Project Operations z novembra 2021 pre scenáre založené na zdrojoch/nezásobách.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932913"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v novembri 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

*Platí pre: Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch*

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.22

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

V tomto vydaní sú zahrnuté nasledujúce funkcie:

- Aplikačné programové rozhrania (API) plánovania projektu teraz podporujú možnosť vytvárať a odstraňovať segmenty Project.

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](/dynamics365/project-operations/environment/resource-dual-write-maps).

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste si prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spustení mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-in-dataverse"></a>Projektové operácie v Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2240080 | The **Platobné podmienky** pole nesmie byť duplikované na proforma faktúre. |
| Fakturácia a tvorba cien | 2358236 | Oprava faktúry musí umožňovať opravy, ktoré majú riadky s nulovou cenou. |
| Správa zdrojov | 2410072 | Povoliť nastavenie zdroja, ktorý je priradený k úlohe ako projektový manažér. |
| Fakturácia a tvorba cien | 2430234 | Opravte problém s výpočtom nákladov a výkonnosti. |
| Čas a výdavky | 2436978 | Povoliť zadanie času vo formáte hh:mm. |
| Fakturácia a tvorba cien | 2448623 | Povoliť aktualizáciu cenníkov po ich priradení k organizačnej jednotke. |
| Čas a výdavky | 2460396 | Umožnite vymazanie časového záznamu vymazaním bunky. |
| Fakturácia a tvorba cien | 2467386 | Povoliť odstránenie projektu, ktorý má úlohu, aj keď je úloha priradená k vyhranej cenovej ponuke. |
| Čas a výdavky | 2461744 | The **Moje neúspešné schválenie** pohľad obsahuje iba schválenia projektov v **Predložené** etapa. |
| Čas a výdavky | 2464082 | Keď sa zhoduje cieľový stav, odstráňte prepojenie zo schvaľovania projektov na množinu schválení. |
| Čas a výdavky | 2468108 | Úloha Schedule by nemala nastaviť a **Spracovanie** stav schvaľovacej sady. |
| Čas a výdavky | 2471503 | Odstráňte skupiny schválenia staré sedem dní. |
| Fakturácia a tvorba cien | 2480687 | Odkaz na riadok cenovej ponuky sa nesmie odstrániť, keď sa vytvorí míľnik riadka cenovej ponuky. |

### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo vo financiách

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Projektový manažment a účtovníctvo | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Ponechané sumy dodávateľa v transakciách výdavkov projektu sa nezobrazujú v zozname transakcií. |
| Projektový manažment a účtovníctvo | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Medzipodniková faktúra dodávateľa je poškodená, keď je zapnutá integrácia faktúry dodávateľa. |
| Projektový manažment a účtovníctvo | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Platobné podmienky na projektových faktúrach nefungujú podľa očakávania. |
| Projektový manažment a účtovníctvo | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Keď sa uvoľní zadržanie dodávateľa, zaúčtovanie kupónu obsahuje ďalšie riadky, ktoré sú nesprávne. |
| Projektový manažment a účtovníctvo | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Po zaúčtovaní denníka integrácie projektových operácií zlyhá z dôvodu chýbajúcich dimenzií pre účet, do ktorého sa neodosiela. |
| Projektový manažment a účtovníctvo | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | The **Projekt** kartu nie je možné upravovať na čakajúcej faktúre dodávateľa, keď je k položke priradená kategória obstarávania. |
| Projektový manažment a účtovníctvo | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Navigačná tabla chýba, ak nie ste prihlásení do Project Operations Dataverse. |
| Projektový manažment a účtovníctvo | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Keď zaúčtujete výnos z projektovej faktúry v použitom zálohovom prípade, vyskytne sa problém, pretože transakcie na doklade nie sú vyrovnané. |
| Projektový manažment a účtovníctvo | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Vytvorenie odhadu po zaúčtovaní návrhu faktúry blokuje opravné riadky z importu. |
| Projektový manažment a účtovníctvo | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Úprava plne fakturovaného medzníka by nemala byť možná. |
| Cestovanie a výdavky | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Všetky prehľady výdavkov sú viditeľné pri hľadaní kategórie v mobilnej aplikácii Výdavky. |
| Cestovanie a výdavky | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Nesprávne sumy transakcií predajcu a transakcií dane z obratu sa účtujú z nákladu, ktorý je vytvorený z transakcie kreditnou kartou. |
| Cestovanie a výdavky | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Irelevantné varovanie sa zobrazí, keď obnovíte súbor **Správa o výdajoch** stránku. |
| Cestovanie a výdavky | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Nesprávny dočasný schvaľovateľ sa použije, keď odstránite dočasného schvaľovateľa a potom znova odošlete výkaz výdavkov prostredníctvom pracovného toku. |
| Cestovanie a výdavky | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Vyskytla sa chyba účtovania, ktorá súvisí s nastavením najazdených kilometrov. |
