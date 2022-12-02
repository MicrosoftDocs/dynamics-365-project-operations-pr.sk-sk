---
title: Čo je nové alebo zmenené v Project Operations z júla 2021 pre scenáre založené na zdrojoch/výrobe
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní nasadenia Project Operations pre scenáre založené na zdrojoch/výrobe z júla 2021.
author: andchoi
ms.date: 07/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: andchoi
ms.openlocfilehash: c04d0465f5f7dd43ba50d4c0d2937b45fed6df86
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028859"
---
# <a name="whats-new-or-changed-in-project-operations-july-2021-for-stockedproduction-based-scenarios"></a>Čo je nové alebo zmenené v Project Operations z júla 2021 pre scenáre založené na zdrojoch/výrobe

_**Vzťahuje sa na:** Project Operations pre scenáre založené na zdrojoch/výrobe_

Tento článok sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.20
 
### <a name="quality-updates"></a>Aktualizácie kvality
                                                                                                                                                                                  
| Oblasť funkcií                      | Číslo odkazu| Aktualizácia kvality                                                                                                                                                                          |
|-----------------------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektový manažment a účtovníctvo | [485394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485394) | Záznamy o nákladových záväzkoch z požiadavky na objednávku sa vymažú, akonáhle sa objednávka uvoľní z problému požiadavky na objednávku.                                                                           |
| Projektový manažment a účtovníctvo | [529602](https://fix.lcs.dynamics.com/Issue/Details/?bugId=529602) | Potvrdenie rozpočtu sa na požiadavke na nákup vyskytuje dvakrát. Toto duplikovanie znamená, že požiadavku nemožno uzavrieť a príslušná objednávka sa nevytvorí.                                                                                                                        |
| Projektový manažment a účtovníctvo | [539439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539439) | Pravidlo fakturácie **Percento, ktoré sa má fakturovať** nebolo možné dokončiť kvôli problému so zaokrúhľovaním.                                                                              |
| Projektový manažment a účtovníctvo | [540023](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540023) | Keď upravíte transakciu a percento bude obsahovať desatinné miesta, náklady a predajná cena nebudú správne upravené.                                      |
| Projektový manažment a účtovníctvo | [540927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=540927) | Prieskumník zdrojov účtovníctva zobrazuje hodiny pre jeden riadok časového rozvrhu pre viac riadkov časového rozvrhu s rôznymi aktivitami.                                      |
| Projektový manažment a účtovníctvo | [541471](https://fix.lcs.dynamics.com/Issue/Details/?bugId=541471) | Uložené zobrazenia a prispôsobenie detailov riadkov časového rozvrhu spôsobujú, že systém pri pokuse o otvorenie časového rozvrhu vždy otvorí podrobnosti prvého časového rozvrhu v zozname.  |
| Projektový manažment a účtovníctvo | [548677](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548677) | Koreňový uzol projektu zmizne a záznamy štruktúry rozdelenia práce sa po importe odstránia.                                                                                             |
| Projektový manažment a účtovníctvo | [548999](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548999) | Keď sú položky prijímané a vydávané čiastočne z požiadavky na položku, systém aktualizuje nesprávny zostatok spotreby rozpočtu. |
| Projektový manažment a účtovníctvo | [550959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550959) | Objednávky na zadržanie projektu nezobrazujú správne súčty v table **Súčty** alebo mriežke **Čakajúca fakturácia**.                                                                  |
| Projektový manažment a účtovníctvo | [554593](https://fix.lcs.dynamics.com/Issue/Details/?bugId=554593) | Pri uzávierke zásob sa úpravy nákladov na položky projektu zaúčtujú na účet súvahy namiesto na účet ziskov a strát.                                                            |
| Projektový manažment a účtovníctvo | [557394](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557394) | Poukaz na transakciu zaúčtovaný na projekt a poukaz na odhad používajú ako účtovnú menu USD, ale suma ukazuje, aký by bol ekvivalent CAD.              |
| Projektový manažment a účtovníctvo | [560140](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560140) | Viazané náklady s požiadavkou na položku a objednávkou sú nesprávne v procese fakturácie objednávky s príjmom produktu a fakturáciou dielu.       |
| Projektový manažment a účtovníctvo | [560567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=560567) | Úprava projektu nesprávne aktualizuje sumu predaja s nepriamymi nákladmi.                                                                                    |
| Projektový manažment a účtovníctvo | [561137](https://fix.lcs.dynamics.com/Issue/Details/?bugId=561137) | Tabuľke **Časový rozvrh** chýba definovaný vzťah so zobrazením **Pracovník/Zdroj**.                                                                                   |
| Projektový manažment a účtovníctvo | [563330](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563330) | Nedá sa vyplniť pole **Číslo aktivity**, keď ho vyberiete z rozbaľovacej ponuky medzipodnikového časového rozvrhu.                                                                 |
| Projektový manažment a účtovníctvo | [563840](https://fix.lcs.dynamics.com/Issue/Details/?bugId=563840) | Nemôžete pridať prispôsobené pole **Účel** ani **Popis činnosti** na nasledujúce stránky: **Transakcia zaúčtovaná v rámci projektu**, **Vytvorenie návrhu faktúry** alebo **Návrh faktúry**.  |
| Projektový manažment a účtovníctvo | [566348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566348) | Nesprávna kontrola dátumu dodania sa poskytuje, keď vytvárate požiadavky na položku pomocou správy údajov (**ProjSalesItemRequirementEntity**).                                              |
| Projektový manažment a účtovníctvo | [566544](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566544) | Keď vyberiete ID zmluvy projektu v službe Finance, integrované prostredie Project Operations otvorí stránku na vytvorenie nového záznamu namiesto otvorenia existujúcej zmluvy o projekte.                                                                                                                 |
| Projektový manažment a účtovníctvo | [567300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567300) |  Štítok „@SYS4083080„ („Nie je možné nájsť jedinečný záznam pracovníka zodpovedajúci zadaným hodnotám“) nie je preložený do dánčiny.                                |
| Projektový manažment a účtovníctvo | [569901](https://fix.lcs.dynamics.com/Issue/Details/?bugId=569901) | Pole **Skupina dane z predaja položiek** nemožno upraviť v návrhu faktúry.                                                                               |
| Projektový manažment a účtovníctvo | [557049](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557049) | Zaviazané náklady sú nadhodnotené neodpočítateľnými čiastkami dane.                                                                                                    |
| Projektový manažment a účtovníctvo | [565080](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565080) | Uverejnenie medzipodnikového časového rozvrhu s viacerými projektmi a rôznymi finančnými dimenziami generuje neočakávané hodnoty v hlavnej knihe.                             |
| Projektový manažment a účtovníctvo | [567962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=567962) | Riadky ponuky faktúr sú duplikované z dôvodu viacerých prípadov pravidelného procesu, súčasne beží aj **Import z prípravy**.                                      |
| Projektový manažment a účtovníctvo | [571339](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571339) | V zaúčtovaní návrhu faktúry na dobropis sa vyskytla chyba, takže transakcie na poukaze sa nevyrovnávajú.    |
| Projektový manažment a účtovníctvo | [573567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573567) | Po uvoľnení pozastavených čakajúcich faktúr sa náklady spojené s projektom stanú nesprávnymi.                                                                             |
| Projektový manažment a účtovníctvo | [573886](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573886) | Nie je možné vytvoriť dobropis pre zákazku odberateľa projektu, keď je daň v inej mene ako mena spoločnosti.                                      |
| Projektový manažment a účtovníctvo | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Vymazanie zmluvy zároveň vymaže adresu priradenú k zákazníkovi.                                                                                     |
| Projektový manažment a účtovníctvo | [585811](https://fix.lcs.dynamics.com/Issue/Details/?bugId=585811) | Návrh faktúry, ktorý je výsledkom opravy zápornej časovej transakcie, nemožno zaúčtovať.                                                                    |
| Cestovanie a výdavky                  | [532075](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532075) | Daň sa v prehľadoch výdavkov počíta rôzne.                                                                                                                  |
| Cestovanie a výdavky                  | [546450](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546450) | Vydanie aktualizácie **DB72_Expense.updateTrvExpTransProjTransId()** neumožňuje, aby **trvExpTrans.ReferenceDataAreaId** vytvorilo novú číselnú postupnosť.                    |
| Cestovanie a výdavky                  | [568805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568805) | Zadaná suma sa nezobrazuje s povinným poľom.                                                                                                             |
| Cestovanie a výdavky                  | [568831](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568831) | Vylepšenia vo výkonnosti pripájania výdavkov k výkazu výdavkov pomocou používateľského rozhrania Prepracované náklady.                                                            |
| Cestovanie a výdavky                  | [570790](https://fix.lcs.dynamics.com/Issue/Details/?bugId=570790) | Môžete vymazať zaúčtované výkazy výdavkov.                                                                                           |
| Cestovanie a výdavky                  | [571317](https://fix.lcs.dynamics.com/Issue/Details/?bugId=571317) | Hlásenie zásad výdavkoch sa zobrazuje viackrát.                                                                                                       |
| Cestovanie a výdavky                  | [573969](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573969) | Pole **Spôsob platby** je zahrnuté na table **Nový výdaj**.                                                                                                      |
| Cestovanie a výdavky                  | [523557](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523557) | Nástroj **Obnoviť stav dokumentu výdavkov** by mal obnoviť stav výkazu výdavkov na **Koncept**, ak nebol nájdený pracovný postup. 

### <a name="regulatory-updates"></a>Regulačné aktualizácie
Informácie o regulačných aktualizáciách pre aplikácie na riadenie financií a prevádzok nájdete v časti [Regulačné aktualizácie](/dynamics365/finance/localizations/regulatory-updates). Môžete sa tiež prihlásiť do služby Lifecycle Services (LCS) a pozrieť si plánované aktualizácie právnych predpisov pomocou vyhľadávacieho nástroja problémov. Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny, typu funkcie a vydania.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
