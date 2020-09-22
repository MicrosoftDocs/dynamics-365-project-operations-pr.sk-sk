---
title: Prognózy a rozpočty projektov
description: Microsoft Dynamics 365 Finance poskytuje predpovede projektu a rozpočty projektu na spravovanie a riadenie vašich projektov.
author: KimANelson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 85a5577968024bf42449c50d72a11414f9207eec
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755611"
---
# <a name="project-forecasts-and-budgets"></a>Prognózy a rozpočty projektov

[!include [banner](../includes/banner.md)]

Existujú dva spôsoby, ako spravovať a riadiť vaše projekty: prognózy projektov a rozpočty projektov. 

Použite prognózy projektov, ak má vaša organizácia prevádzkové hľadisko a ak sa zameriava na výnosy a náklady, ktoré sú odvodené z konkrétnych transakcií. Ak sa vaša organizácia zameriava viac na finančné sumy, použite rozpočty projektov. 

Prognózy projektov aj rozpočty projektov používajú prognózové modely na udržanie predpokladaných súm transakcií. 

Každá metóda má svoje výhody. Pred výberom metódy pre vašu organizáciu by ste mali zvážiť nasledujúce body.

|                           |                                          |                                                    |
|---------------------------|------------------------------------------|----------------------------------------------------|
|                           | **Prognózy projektov**                  | **Rozpočty projektov**                              |
| **Pridelenie obdobia**     | Transakcie nemôžete výslovne alokovať cez fiškálne obdobie. Prognóza a kontrola prognózy naopak vychádzajú zo životnosti projektu. Pretože prognózy sú založené na konkrétnom dátume, musíte odvodiť obdobie od tohto dátumu. | Transakcie môžete alokovať cez celý projekt alebo fiškálne obdobie. Ak vykonáte alokáciu na určité obdobie, môžete nevyužité sumy preniesť do nasledujúceho fiškálneho obdobia. |
| **Prezeranie transakcií**  | Transakcie môžete zobraziť vo formulároch prognóz, kde vidíte prognózy pre celú spoločnosť a pre všetky projekty bez ohľadu na hierarchiu. Ak sa chcete zamerať na konkrétny projekt, musíte filtrovať údaje.                                       | Môžete zobraziť rozpočtované transakcie pre jednu hierarchiu projektu. Preto si môžete pozrieť podrobnosti transakcie nadradeného projektu alebo jeho podprojektov.                 |
| **Transakčné premenné** | Pri zadávaní prognózovaných transakcií môžete pre skutočnú transakciu použiť všetky atribúty, ktoré existujú. To umožňuje v prognóze získať viac detailov. Môžete napríklad zadať podrobnosti o množstvách, pracovníkoch, položkách alebo vlastnostiach riadkov.         | Po zadaní podrobností o rozpočte môžete použiť iba sumy, kategórie a aktivity.                    |
| **Zabezpečenie**              | Prognózovanie je založené na transakciách, ktoré zadáte do formulárov prognózy, a nezahŕňa žiadny mechanizmus riadenia procesu. Každý pracovník, ktorý má povolenia na formulár prognózy, môže informácie upravovať bez schválenia.                                        | Rozpočtovanie využíva systém pracovných postupov, ktorý umožňuje správu zmien a udržiavať históriu revízií.         |
| **Typy vstupov**           | Transakčné položky prognózy sú založené na počte jednotiek a na nákladoch a predajných jednotkových cenách.  | Podrobnosti rozpočtu sú založené na sumách, ktoré sú rozdelené medzi náklady a výnosy.                                          |
| **Modely prognóz**       | Pretože každá prognóza musí byť spojená s modelom, môžete vytvoriť viac modelov prognózy a tiež nastaviť vedľajšie modely.           | Rozpočtovanie projektov obmedzuje prognózované modely, ktoré sa používajú pri zostavovaní rozpočtu. Menej modelov prognóz môže pomôcť zvýšiť konzistenciu projekcií.                           |
| **Prekročenie nákladov**         | Môžete povoliť alebo zakázať iba zadávanie transakcií, ktoré spôsobia prekročenie nákladov.   | Rozpočty projektu poskytujú používateľom ďalšie možnosti kontroly. Môžete povoliť varovania a prekročenia.                    |
| **Ovládací prvok**               | Kontrola prognózy sa vykonáva pomocou redukcie prognózy. Skutočné sumy sa odpočítajú od zostatkov prognózovaných transakcií bez akýchkoľvek záznamov o audite. To môže sťažiť sledovanie, kde k skutočným transakciám došlo.                   | Pri kontrole rozpočtu projektu sa skutočné sumy odpočítajú od súm vo zvyšnom rozpočte. To umožňuje vytvoriť jasnejší auditovací záznam.                                   |

## <a name="project-forecasts"></a>Prognózy projektov
Keď použijete prognózu projektu, môžete zadať prognózované transakcie do formulárov prognózy pre každý typ transakcie. Pre prognózovanú transakciu je možné použiť každý atribút, ktorý je k dispozícii pre skutočnú transakciu – napríklad ziskovosť riadku, atribúty riadku, pracovníci alebo popisy. Môžete tiež navrhnúť, ako dlho potom, čo vám vzniknú náklady, budete zákazníkovi fakturovať. 

Transakcie prognózovania projektov sú založené na jednotkách a sumách. 

Každú prognózu projektu musíte spojiť s modelom prognózy. Po zadaní transakcie prognózy sa automaticky navrhne model prognózy. Model prognózy funguje ako kontajner pre transakcie prognózy. 

Modely prognózy môžete určiť ako podmodely modelu. Takto môžete prognózovať podľa regiónu, časového obdobia alebo oddelenia. Transakcie prognózy môžete skopírovať do modelu a vytvoriť tak nový model. Transakcie môžete tiež preniesť do hlavnej účtovnej knihy. Pretože medzi prognózou a modelom existuje vzájomný vzťah jeden k jednému, každý model prognózy tvorí pre projekt samostatný rozpočet. 

Modely prognóz môžu využívať redukciu prognózy ako kontrolný mechanizmus pre projekty. Pri redukcii prognózy skutočné transakcie znižujú zostatky prognózovaných transakcií. Pretože sa však redukcia prognózy uplatňuje na najvyšší projekt v hierarchii, poskytuje obmedzený pohľad na zmeny v prognóze. Napríklad, ak je pracovník spojený s podprojektom, skutočné transakcie pre pracovníka sa zaúčtujú do nadradeného projektu. To môže sťažiť sledovanie zmien, pretože nemôžete ľahko určiť, ktorá transakcia, v ktorom podprojekte spôsobila zníženie prognózovanej sumy. Preto je dobré vytvoriť si kópiu modelu prognózy na použitie s redukciou prognózy. Potom môžete pomocou prehľadov zobraziť pôvodné prognózy. 

Môžete revidovať, kopírovať, mazať alebo prenášať prognózy projektu do rozpočtu hlavnej účtovnej knihy. Kontrola procesu však neexistuje. Každý pracovník, ktorý má povolenie na formulár prognózy, môže uskutočniť revízie bez schválenia.

-   **Revidovať** – Prognózovanú transakciu môžete revidovať v rovnakých formulároch, v ktorých boli vykonané pôvodné záznamy.
-   **Kopírovať alebo odstrániť** – Pri kopírovaní prognózovaných transakcií kopírujete riadky transakcií jedného modelu prognózy do iného modelu prognózy. Keď odstránite prognózu, odstránite transakcie prognózy z modelu prognózy. Ak chcete obmedziť transakcie prognózy, ktoré sa kopírujú alebo odstraňujú, vyberte konkrétne typy transakcií a dátumy. Takto môžete kopírovať alebo odstraňovať iba konkrétne časti prognózy.
-   **Prenos** – Pri prenose prognózy projektu do rozpočtu hlavnej účtovnej knihy prenesiete transakcie prognózy modelu prognózy do rozpočtu hlavnej účtovnej knihy. Všetky predtým prevedené transakcie môžete prepísať v rozpočte hlavnej účtovnej knihy, do ktorej prenesiete prognózu projektu.

## <a name="project-budgets"></a>Rozpočty projektov
Rozpočty projektov je jednoduchšia metóda ako prognózovanie, aj keď sa integruje do modelov prognózy. Pre pôvodné podrobnosti a revízie rozpočtu používa jediný vstupný formulár a umožňuje projekcie, ktoré sú založené iba na sume, kategórii alebo aktivite. 

V rámci rozpočtov projektov musia byť všetky pôvodné rozpočty a revízie odoslané do pracovného postupu projektu na schválenie. Pracovné postupy vám poskytujú väčšiu kontrolu nad procesom a vytvárajú záznam histórie zmien. 

Rozpočtovanie projektov sa podobá rozpočtu hlavnej účtovnej knihy, ale je rýchlejšie a ľahšie sa nastavuje. Mnoho možností v rozpočte hlavnej knihy, ako napríklad postupnosť čísel alebo mena, sa nemusí pre projekty nastavovať osobitne.

Rozpočty projektov sú automaticky spojené s dvoma modelmi prognóz, jedným pre pôvodný rozpočet a druhým pre zostávajúci rozpočet. Preto môžu prehľady založené na modeloch prognóz využívať údaje o rozpočte. Keď je pridelený rozpočet projektu, systém vytvorí transakcie prognóz na základe súvisiacich modelov, ktoré sa používajú na účely vykazovania a kontroly.

## <a name="forecast-models"></a>Modely prognóz
Modely prognóz majú jednovrstvovú hierarchiu. To znamená, že jedna prognóza projektu musí byť spojená s jedným modelom prognózy.

Ak používate prognózy projektov, môžete identifikovať modely ako podmodely. Potom môžete vytvárať prognózy podľa oddelenia, časového obdobia alebo regiónu. Môžete napríklad vytvoriť model prognózy na jeden rok a potom vytvoriť podmodely pre regionálne predpovede severovýchod, juhovýchod, severozápad a juhozápad, ktoré predložia regionálni vedúci. Výberom rôznych možností v dostupných prehľadoch môžete zobraziť informácie podľa celkovej prognózy alebo podľa podmodelu.



