---
title: Čo je nové v novembri 2020 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Project Operations z novembra 2020, pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 9eda9d75f5a4d71e6e4b8bd22dce973270639db3f927ac6a76be5b3c4303fc31
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007975"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v novembri 2020 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

- Project Operations v prostredí CDS environment verzie 4.4.0.70
- Projektový manažment a účtovanie v prostredí Dynamics 365 Finance verzie 10.0.14

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a>Aktualizácie aplikácie Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

### <a name="project-operations-on-cds"></a>Project Operations v prostredí CDS

| Oblasť funkcií                 | Číslo odkazu | Aktualizácia kvality                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|  Správa príležitostí       | 2036993          | Riadok odhadu a riadky zmlúv priradenia zdroja sa aktualizujú v získaných cenových ponukách, keď je typ riadku cenovej ponuky **Všetky úlohy**.                                                 |
| Fakturácia a tvorba cien          | 2070392          | Riadky projektovej zmluvy na faktúre sa zvyšujú vždy po výbere možnosti **Obnovenie fakturačných transakcií**.                                                                         |
| Plánovanie projektu             | 2043336          | Nie je možné odstrániť záznam člena projektového tímu.                                                                                                                                  |
| Plánovanie projektu             | 2046013          | Nekonzistentné správanie pre stĺpce značky Odhady počas načítania a pri zmene typu časovej fázy.                                                                                   |
| Plánovanie projektu             | 2046647          | Počiatočný a konečný čas sú o hodinu vypnuté, keď sa požiadavky na zdroje generujú od členov projektového tímu.                                                                      |
| Plánovanie projektu             | 2053879          | (Podľa pripravovaného zavádzania CDS) PublishUnassignedAssignments zruší pokus o uloženie úlohy pri chybe „Hodnota odovzdaná pre ConditionOperator.In je prázdna.“                       |
| Plánovanie projektu             | 2055501          | Odchod s prázdnou hodnotou **Dátum začatia projektu** spôsobí zlyhanie plánu.                                                                                                      |
| Plánovanie projektu             | 2066817          | Nie je možné vytvoriť všeobecný zdroj pomocou nástroja na výber ľudí na karte **Úlohy**.                                                                                                   |
| Plánovanie projektu             | 2067034          | Tlačidlo **Zobraziť podrobnosti** nie je k dispozícii na stránke **Podrobnosti úlohy**.                                                                                                       |
| Správa zdrojov          | 2046667          | Všeobecní členovia tímu sa neodstránia ani po splnení všetkých zdrojov.                                                                                                    |
| Položka času a rýchleho výdavku | 2047499          | Tlačidlo **Nový** na stránke Časový vstup otvorí stránku **Nový e-mailový podpis**.                                                                                               |
| Položka času a rýchleho výdavku | 2059859          | Pri vytváraní položky výdavkov sa otvorí neočakávané vyskakovacie okno.                                                                                                                         |
| Ostatné                        | 2044181          | (Odinštalovanie nákupnej objednávky) Pri pokuse o odinštalovanie základných riešení aplikácie Project Service msdyn_ProjectServiceCore_Patch a msdyn sa vyskytne chyba „Záznam nie je k dispozícii“.  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v Dynamics 365 Finance

| Oblasť funkcií        | Číslo odkazu | Aktualizácia kvality                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Priznanie výnosov | [451662](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | Percento dokončenia odhadu projektu je nesprávne, keď zmluva používa cudziu menu a percento postupu práce pre metódu dokončenia.                     |
| Priznanie výnosov | [469894](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | Odhady nie je možné odoslať s metódou dokončenia **Skutočné náklady**.                                                                                                    |
| Priznanie výnosov | [485439](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | Vylúčenie zlyhá z dôvodu chyby nerovnováhy poukazu, keď sa mena spoločnosti a mena transakcie líšia.                                              |
| Správa výdavkov  | [456882](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | Pre používateľov, ktorí nie sú správcami, sa hodnoty vyhľadávania pre stĺpce riadkov výdavkov, ako napr. **ID projektu** a **Kategória výdavkov** v ráme dátového konektora nezobrazujú správne. |
| Správa výdavkov  | [469300](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | Predvolená vlastnosť riadku sa nezobrazuje pre kategórie výdavkov.                                                                                                         |
| Správa výdavkov  | [469302](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | Integrácia výdavkov musí obsahovať vlastnosť riadka z výkazu výdavkov.                                                                                             |
| Účtovanie           | [462499](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | Nie je možné zaúčtovať návrhy projektových faktúr kvôli chybovej správe, ktorá hovorí, že kombinácia FD nebola overená.                                                    |
| Účtovanie           | [470614](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | Nie je možné zobraziť transakcie zo stránky s podrobnosťami **faktúra**.                                                                                                              |
| Účtovanie           | [480070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | Riadky s návrhom faktúry je možné odstrániť.                                                                                                                                  |
| Účtovníctvo v rámci projektu  | [470293](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | Položky ponuky **Predpoveď** nie sú viditeľné na stránke so zoznamom **Projekty**.                                                                                                   |
| Účtovníctvo v rámci projektu  | [475873](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | Nedá sa otvoriť **Vyhlásenie o projekte**   > **Transakcie a predpoveď**.                                                                                                       |
| Účtovníctvo v rámci projektu  | [475879](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | **Upraviť účtovníctvo** nie je povolené pre fakturované projektové transakcie.                                                                                                  |
| Účtovníctvo v rámci projektu  | [480962](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | Podrobnosti účtovníctva nie sú zahrnuté v tabuľke **ProjCDSActualsImport**, keď je uverejnený denník **Integrácia**.                                                  |
| Účtovníctvo v rámci projektu  | [482558](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | Položka prognózy projektu sa zdvojnásobí, keď odstránite a znovu pridáte priradenie zdrojov.                                                                            |
| Účtovníctvo v rámci projektu  | [502019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | Výber odkazu na ID projektu neotvorí adresu URL priameho odkazu do CDS.                                                                                                         |
| Účtovníctvo v rámci projektu  | [505458](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | Nie je možné aktualizovať dátum začatia úlohy v službe CDS.                                                                                                                           |
| Účtovníctvo v rámci projektu  | [510041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | Po povolení tejto funkcie nie sú možné viaceré riadky zmluvy bez integrácie CDS.                                                                                   |

### <a name="regulatory-updates"></a>Regulačné aktualizácie
Informácie o regulačných aktualizáciách pre aplikácie Finance and Operations sú uvedené v časti [Regulačné aktualizácie](/dynamics365/finance/localizations/regulatory-updates). Môžete sa tiež prihlásiť do LCS a pozrieť si plánované regulačné aktualizácie pomocou nástroja na vyhľadanie problému. Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny, typu funkcie a vydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]