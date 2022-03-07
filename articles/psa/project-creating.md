---
title: Plány projektov
description: Táto téma poskytuje informácie o tom, ako vytvoriť plán.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 3/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 192fbe7f26a2bd060ffe9bc0b1eea50b9431bca4696e3da1d94bf53158e026a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6998435"
---
# <a name="project-schedules"></a>Plány projektov 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Plán projektu komunikuje, aká práca sa musí dokončiť, ktoré zdroje budú vykonávať prácu, a časový rámec v ktorom práca musí byť dokončená. To odráža všetku prácu spojenú s dodaním projektu na čas. V Dynamics 365 Project Service Automation, môžete vytvoriť plán projektu tým, že rodelíte prácu na zvládnuteľné úlohy, odhad času, ktorý je potrebný na vykonanie každej úlohy, nastavenie závislostí úloh, nastavenie trvania úlohy, a odhad všeobecných zdrojov, ktoré budú robiť úlohy. Plán projektu sa vytvorí na karte **plán** na stránke projektu.
 
## <a name="tasks"></a>Úlohy

Prvým krokom pri vytváraní plánu projektu je rozdelenie na zvládnuteľné porcie. Plán v PSA podporuje nasledujúce funkcie:

- Koreňový uzol projektu
- Súhrn alebo zásobník úloh
- Úlohy listového uzla

### <a name="project-root-node"></a>Koreňový uzol projektu

Koreňový uzol projektu je súhrnná úloha najvyššej úrovne projektu. Všetky ostatné úlohy projektu sú vytvorené pod ním. Názov koreňového uzla je vždy nastavený na názov projektu. Úsilie, dátumy a trvanie koreňového uzla sú zosumarizované na základe hodnôt v hierarchii pod ním. Vlastnosti koreňového uzla nemôžete upraviť. Koreňový uzol tiež nemôžete odstrániť.

### <a name="summary-or-container-tasks"></a>Súhrn alebo zásobník úloh 

Súhrnné úlohy majú čiastkové úlohy alebo kontajnerové úlohy v rámci nich. Nemajú na seba žiadne pracovné úsilie alebo náklady. Namiesto toho ich pracovné úsilie a náklady sú súhrnom úsilia a nákladov na ich kontajnerové úlohy. Počiatočný dátum súhrnnej úlohy je dátum začatia kontajnerovej úlohy a koncový dátum je dátum ukončenia kontajnerovej úlohy. Názov súhrnnej úlohy je možné upraviť, ale nie je možné upraviť vlastnosti plánovania (úsilie, dátumy a trvanie). Ak odstránite súhrnnú úlohu, odstránite aj všetky jej kontajnerové úlohy.

### <a name="leaf-node-tasks"></a>Úlohy listového uzla

Úloha listového uzla predstavuje najpodrobnejšiu prácu na projekte. Majú odhadnuté úsilie, zdroje, plánovaný dátum začatia a ukončenia a celkové trvanie.
 
## <a name="creating-a-task-hierarchy"></a>Vytvorenie hierarchie úloh

Môžte vytvoriť heirarchiu úloh pomocou nasledujúcich možností:

- Tlačidlo **pridať úlohu**
- Tlačidlo **znížiť úroveň úlohy**
- Tlačidlo **zvýšiť úroveň úlohy**
- Tlačidlá **posunúť nahor** a **posunúť nadol**
- Klávesové skratky a zjednodušenie ovládania

### <a name="add-task"></a>Pridať úlohu

Tlačidlo **pridať úlohu** umožňuje vytvoriť novú úlohu v hierarchii. Ak nevyberiete pozíciu, úloha je vložená na koniec. 

Pre každú úlohu je priradené ID plánu. ID plánu predstavuje hĺbku a pozíciu úlohy v hierarchii. Používa prehľad číslovania. Pre úlohy v prvej úrovni v rámci projektu koreňového uzla, sa požíva schéma číslovania 1, 2, 3, a tak ďalej. Pre úlohy pod prvou úrovňou v rámci projektu koreňového uzla, sa požíva schéma číslovania 1.1, 1.2, 1.3, a tak ďalej.

### <a name="indent-task"></a>Znížiť úroveň úlohy.

Keď je úroveň úlohy znížená, stane sa podradenou úlohou úlohe, ktorá je priamo nad ňou. ID plánu úlohy sa potom prepočíta tak, že je založené na ID plánu svojho nového nadradeného a sleduje prehľad schémy číslovania. Nadradená úloha je teraz súhrnná úloha alebo kontajnerová úlohu. Preto sa stáva súhrnom jej podradených úloh.

### <a name="outdent-task"></a>Znížiť úroveň úlohy. 

Keď je úroveň úlohy znížená, táto už nie je podradená úloha úlohe, ktorá bola jej nadradenou úlohou. Potom sa prepočítajú ID plánu tak, aby odrážal aktualizovanú hĺbku a pozíciu úlohy v hierarchii. Úsilie, náklady a dátumy predchádzajúcej nadradenej úlohy sa prepočítajú tak, aby nezahŕňali túto úlohu.

### <a name="move-up-and-move-down"></a>Posun nahor a posun nadol. 

Tlačidlá **posunúť nahor** a **posunúť nadol** zmenia pozíciu úlohy v nadradenej hierarchii. Zmeny tohto typu neovplyvnia úsilie, náklady, dátumy alebo trvanie úlohy. Len ID plánu úlohy je ovplyvnené. Potom sa prepočíta ID plánu tak, aby odrážal novú pozíciu úlohy v zozname nadradených a podradených úloh.

### <a name="accessibility-and-keyboard-shortcuts"></a>Klávesové skratky a zjednodušenie ovládania

Mriežka **plánu** je plne prístupná a môže sa používať s čítačkami obrazovky, ako sú napríklad Narrator, JAWS alebo NVDA. Môžete prechádzať oblasti mriežky pomocou šípok (ako v Microsoft Excel), môžete použiť klávesu Tab na postúp cez interaktívne prvky UI, a môžete použiť šípku nadol, klávesu ENTER, alebo medzerník pre výber a vyvolanie rozbaľovacích ponúk. Hlavičky stĺpcov sú tiež interaktívne. Môžete skryť a zobraziť stĺpce, pomocou klávesy Tab a kláves so šípkami prechádzať hlavičkami stĺpcov a použiť tlačidlá akcie na paneli s nástrojmi. Okrem toho môžete použiť nasledujúce klávesové skratky:

- **Obnoviť**: ALT+SHIFT+F5
- **Pridať**: ALT+SHIFT+Insert
- **Odstrániť**: ALT+SHIFT+DELETE
- **Posunúť nahor/nadol**: ALT+SHIFT+šípky nahor/nadol
- **Znížiť/Zvýšiť úroveň**: ALT_SHIFT+šípky vľavo/vpravo
- **Rozbaliť/Zbaliť hierarchie**: ALT+SHIFT+plus/mínus tlačidlá

## <a name="task-attributes"></a>Atribúty úlohy

Názov úlohy popisuje prácu, ktorá sa musí dokončiť. V PSA, atribúty, ktoré sú priradené k úlohe opísať plán úlohy a jeho personálne požiadavky.

> ![Atribúty úlohy.](media/project-2.png)
 
### <a name="schedule-attributes"></a>Naplánovať atribúty

Atribúty **Úsilie**, **dátum začiatku**, **dátum konca** a **trvanie** určujú plán úlohy.

Ďalšie atribúty plánu zahŕňajú:

- **Hodiny úsilia**: zadajte odhad hodín, ktoré sú potrebné na dokončenie úlohy. 
- **Trvanie**: zadajte počet pracovných dní, ktoré sú potrebné na dokončenie úlohy.
- **ID plánu**: toto automaticky generované ID sa používa na objednávku úloh v hierarchii. Závislosti medzi úlohami riadia skutočné poradie, v ktorom sú úlohy spracované.
 
### <a name="staffing-attributes"></a>Personálne atribúty

Personálne atribúty sú prístupné prostredníctvom poľa **zdroje** v pláne. Môžete vyhľadať existujúci zdroj alebo kliknúť na **vytvoriť** a na paneli **rýchle vytvorenie** pridať člena projektového tímu ako nový zdroj.

Polia **rola**, **zdrojová jednotka** a **názov pozície** sa používajú na popis personálnych požiadaviek na úlohu. Tieto personálne atribúty spolu s plánom úloh sa používajú na vyhľadanie dostupných zdrojov na vykonanie tejto úlohy.

**Rola** - zadajte typ zdroja, ktorý je potrebný na vykonanie úlohy.

**Zdrojová jednotka** - zadajte jednotku, z ktorej by mali byť pridelené zdroje pre úlohu. Tento atribút ovplyvňuje odhady nákladov a predaja na úlohy, ak sú náklady a fakturačná sadzba zdroja nastavené na zdrojové jednotky.

**Názov pozície** – zadajte popisný názov pre všeobecný zdroj, ktorý slúži ako zástupný symbol pre zdroj, ktorý bude v konečnom dôsledku vykonávať prácu.

Pole **zdroje** obsahuje názov pozície všeobecného zdroja alebo pomenovaného zdroja, keď sa našiel.

Pole **Kategória** obsahuje hodnoty, ktoré označujú širší typ práce, do ktorej môže byť úloha zoskupená. Toto pole neovplyvňuje plánovanie ani personálne obsadenie. Používa sa len na vykazovanie.

### <a name="task-dependencies"></a>Závislosti úloh 

Môžete použiť plán v PSA na vytvorenie predchodcu vzťahov medzi úlohami. Pole **predchodcu** v časti **úlohy** preberá jednu alebo viacero hodnôt na označenie úloh, na ktorých je úloha závislá. Keď sú hodnoty predchodcu priradené k úlohe, úloha môže začať iba ak sa dokončili všetky predchádzajúce úlohy. Z dôvodu závislosti, plánovaný počiatočný dátum úlohy sa obnoví na dátum po dokončení predchádzajúcich úloh.

Režim úlohy nemá žiadny vplyv na aktualizácie, ktoré sú vykonané na počiatočných a koncových dátumoch predchádzajúcich/závislých úloh.

## <a name="task-mode"></a>Režim úlohy 

Režim úlohy určuje plánovanie úloh listového uzla. PSA podporuje dva režimy pre každú úlohu: režim automatického plánovania a režim manuálneho plánovania.

### <a name="auto-scheduling"></a>Automatické plánovanie 
 
Keď nastavíte režim úlohy na **automatické plánovanie**, systém plánovania úloh použije pravidlá plánovania na nasledovné atribúty úloh, čím sa určí plán úlohy.

#### <a name="scheduling-rules"></a>Pravidlá plánovania

Ak nemá úloha listového uzla predchodcov, jej dátum začiatku je prednastavený na dátum plánovaného začiatku projektu. Trvanie úlohy listového uzla sa vždy vypočítava ako počet pracovných dní medzi dátumom začatia a skončenia. Po automatickom naplánovaní úlohy bude systém plánovania sledovať tieto pravidlá:

- Počiatočný a koncový dátum úlohy musí byť vždy pracovný deň v súlade s plánovacím kalendárom projektu 
- Pre každú úlohu, ktorá má predchádzajúce úlohy, sa dátum začatia úlohy automaticky nastaví na dátum posledného ukončenia svojich predchodcov.
- Úsilie sa vypočíta pomocou tohto vzorca: počet ľudí × trvanie × hodiny v štandardnom pracovnom dni v kalendári projektu.

### <a name="manual-scheduling"></a>Ručné plánovanie

Ak pravidlá automatického plánovania nespĺňajú vaše požiadavky, môžete nastaviť režim úloh pre úlohu na **manuálne naplánované.** Tým plánovací systém prestane vypočítavať hodnoty ostatných atribútov plánovania. Bez ohľadu na režim úloh, ak nastavíte predchodcov úloh, vždy ovplyvníte dátum začatia závislej úlohy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]