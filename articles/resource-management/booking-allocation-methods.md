---
title: Metódy prideľovania rezervácií
description: Táto téma poskytuje informácie o tom, ako metódy prideľovania rezervácií fungujú v Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: c2a964c18c7eae61c5a0239da3b18da31b6ad574
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084314"
---
# <a name="booking-allocation-methods"></a>Metódy prideľovania rezervácií

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Či už pridáte člena tímu priamo k projektu na karte **tím** alebo zarezervujete zdroj k projektu alebo požiadavke na tabule plánu, existuje niekoľko rôznych spôsobov priradenia rezervácie, ktoré možno využiť. Tento nadpis vysvetľuje, ako každá metóda funguje, a aké metódy by mohli viesť k nadmernej rezervácii zdrojov.

## <a name="booking-allocation-methods"></a>Metódy prideľovania rezervácií

Môžete použiť šesť spôsobov prideľovania rezervácií:

- [Plná kapacita](#full)
- [Zostávajúca kapacita](#remaining)
- [Kapacita v percentách](#percentage)
- [Rovnomerne distribuovať hodiny](#evenly)
- [Hodiny počiatočného vyťaženia](#front)
- [Žiadne](#none)

### <a name="full-capacity"></a><a name="full"></a>Plná kapacita 
Metóda plnej kapacity zarezervuje úplnú kapacitu zdrojov pre stanovené dátumy od a do. Napríklad, ak má zdroj kalendár nastavte pracovať 8 hodín denne, 5 dní týždenne, nastavte dátum začatia a ukončenia, ktorý pokrýva 5 pracovných dní zarezervuje zdroj na 40 hodín. Rezervácia prebieha bez ohľadu na zdroje a zostávajúcu kapacitu. Ak je zdroj počas daného obdobia už zarezervovaný pre iné projekty, 40 hodín sa zarezervuje ako hodiny naviac, čo môže viesť k nadmerným rezerváciám.

### <a name="remaining-capacity"></a><a name="remaining"></a>Zostávajúca kapacita
Metóda zostávajúcej kapacity je dostupná len pri rezervácii priamo do projektu pomocou plánovacej tabule. Táto metóda zarezervuje dostupnú kapacitu zdroja v rámci stanoveného rozsahu dátumov. Napríklad, ak zdroj má kapacitu 40 hodín týždenne a už rezervovaných 10 hodín týždenne, rezervácia metódou zostávajúcej kapacity, zarezervuje s rovnakými týždennými výsledkami zvyšných 30 hodín kapacity pre tento týždeň.

### <a name="percentage-capacity"></a><a name="percentage"></a>Kapacita v percentách
Metóda percentuálnej kapacity zarezervuje zdroj pre percento kapacity pre stanovené dátumy od a do. Napríklad, ak má zdrojový kalendár nastavené pracovať 8 hodín denne, 5 dní týždenne, nastavte dátum začatia a ukončenia, ktorý pokrýva 5 pracovných dní na 50% kapacity, čo zarezervuje zdroj na 20 hodín. Individuálne rezervácie na deň sú rozložené rovnomerne naprieč obdobím, napríklad v tomto prípade ide o 4 hodiny denne. Rezervácia prebieha bez ohľadu na zdroje a zostávajúcu kapacitu. Ak je zdroj počas daného obdobia už zarezervovaný pre iné projekty, 20 hodín sa zarezervuje ako hodiny naviac, čo môže viesť k nadmerným rezerváciám.

### <a name="evenly-distribute-hours"></a><a name="evenly"></a>Rovnomerne distribuovať hodiny
Metóda rovnomerného rozdelenia hodín zarezervuje zdroj pre stanovený počet hodín, ktoré rovnomerne rozdelí na dni v rámci stanovených dátumov od a do. Napríklad, ak ste rezervovali zdroj na 20 hodín počas 5-dňového obdobia, táto metóda distribuuje 20 hodín rovnomerne na 4 hodiny denne. Rezervácia prebieha bez ohľadu na zdroje a zostávajúcu kapacitu. Ak je zdroj počas daného obdobia už zarezervovaný pre iné projekty, 20 hodín sa zarezervuje ako hodiny naviac, čo môže viesť k nadmerným rezerváciám.

### <a name="front-load-hours"></a><a name="front"></a>Hodiny počiatočného vyťaženia
Metóda počiatočného vyťaženia hodín zarezervuje zdroj pre stanovený počet hodín, v rámci počiatočného vyťaženia denných hodín v rámci stanovených dátumov od a do. Počiatočné vyťaženie spotrebuje dostupnú kapacitu zdroja v poradí postupného spotrebovania. Napríklad ak pracovný plán zdroja je 8 hodín denne, 5 dní v týždni, a nemajú žiadne aktuálne rezervácie, rezervácia zdroja na 20 hodín po dobu 5 pracovných dní má za následok nasledujúci vzor denných rezervácií: 

|                           |    Deň 1    |    Deň 2    |    Deň 3    |    Deň 4    |    Deň 5    |    Spolu    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    **Existujúce rezervácie**    |    0        |    0        |    0        |    0        |    0        |    0        |
|    **Nová rezervácia**          |    8        |    8        |    4        |    0        |    0        |    20       |

Metóda počiatočného vyťaženia zohľadňuje existujúce rezervácie a dostupnú kapacitu. Napríklad ak má rovnaký zdroj už 20 hodín rezervácií v pracovnom týždni, nová rezervácia spotrebuje zostávajúcu kapacitu nasledovne:

|                     | Deň 1 | Deň 2 | Deň 3 | Deň 4 | Deň 5 | Spolu |
|---------------------|-------|-------|-------|-------|-------|-------|
| **Existujúce rezervácie** | 8     | 8     | 4     | 0     | 0     | 20    |
| **Nová rezervácia**       | 0     | 0     | 4     | 8     | 8     | 20    |

Pretože sa zohľadňuje dostupná kapacita, môže sa vám zobraziť chybové hlásenie v prípade, že zdroj už nemá zostávajúcu kapacitu, ktorú možno spotrebovať rezerváciou. Použitím tejto metódy nie je možná nadmerná rezervácia.

### <a name="none"></a><a name="none"></a>Žiadne
Nulová metóda je dostupná len v prípade rezervácie z karty **tímu** v rámci projektu. Táto metóda pridá zdroj ako člena tímu v projekte, no nevytvorí žiadne rezervácie, ktoré využívajú kapacitu zdroja. Táto metóda sa používa, keď predvolený člen tímu projektového manažéra sa pridá pri vytváraní projektu. Používateľ manažéra projektu, ktorý vytvoriť projekt, sa predvolene pridá k projektu, vďaka čomu má záznam entity projektu vlastníka a projekt bude mať jedného schvaľovateľa. Pretože tento používateľ nemá žiadne rezervácie, ak si chcete rezervovať prostriedok môžete buď odstrániť a znova pridať metódu rozdielneho pridelenia, alebo pridať prostriedok k úlohám a potom použiť **rozšírená rezervácia** , na karte **odsúhlasenie** na vytvorenie rezervácie úlohy.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Rozdelenie metód, ktoré vedú k nadmernej rezervácii
Aby sme to zhrnuli, nasledujúce metódy prideľovania vedú k nadmernej rezervácii v prípade, že zdroj už je pridelený iným projektom (alebo na iné objednávky prác alebo plánovateľné entity):

- Plná kapacita
- Kapacita v percentách
- Rovnomerne distribuovať hodiny

Keď používate jednu z týchto troch metód rozdelenia, nedostanete upozornenie na nadmernú rezerváciu zdroja. Na nápravu nadmerného počtu rezervácií, budete musieť použiť tabuľu plánovania.
