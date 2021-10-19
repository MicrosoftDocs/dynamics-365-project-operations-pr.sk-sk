---
title: Prehľad udržania dodávateľov
description: Táto téma poskytuje prehľad možností zachovania dodávateľov.
author: sigitac
ms.date: 10/01/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5f89904af5fb00eac46de834a438f412b371e74e
ms.sourcegitcommit: 098ea345ecfaf4445520094c32f5511b67e7953c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2021
ms.locfileid: "7594627"
---
# <a name="vendor-retention-overview"></a>Prehľad udržania dodávateľov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Vaša organizácia môže chcieť ponechať časť platieb dodávateľom, ktorí pracujú na projektoch pre vašu organizáciu. Pred zaplatením predajcovi sa napríklad budete chcieť uistiť, že položky a služby, ktoré poskytoval, spĺňajú vaše očakávania.

Keď vyjednávate o nákupoch projektov s dodávateľmi, môžete zadať podmienky uchovávania dodávateľa, ktoré obsahujú percento alebo sumu, ktorá sa má zadržať. Keď dodávateľ dodáva položky a služby, odpočítate uvedené percento alebo čiastku zadržania z vašej platby dodávateľovi. Keď je projekt dokončený alebo dosiahne predbežnú fázu, ako je uvedené v zmluve s dodávateľom, uvoľníte zadržanú čiastku a vytvoríte platbu predajcovi.

## <a name="vendor-retention-example"></a>Príklad zadržania platby dodávateľovi

Nasledujúci príklad ukazuje, ako sa zadrží percento sumy faktúry dodávateľa na základe percenta, ktoré je dokončené pre projekt.

Spoločnosť Contoso Robotics USA uzavrela s dodávateľom Fabrikam zmluvu na dodanie 100 hodín školenia na projekt obnovy zariadenia. Celková hodnota zmluvy je USD 30 000 s dohodnutou kúpnou cenou USD 300 za hodinu.

Školenie bude prebiehať v troch fázach s týmto harmonogramom:

- Fáza 1: 50 hodín alebo 50 percent projektu
- Fáza 2: 30 hodín alebo celkovo 80 percent projektu
- Fáza 3: 20 hodín alebo 100 percent projektu

Nasledujúca tabuľka uvádza podmienky zadržania.

| **Percento dodaných jednotiek** | **Percento zadržania** | **Percento uvoľnenia** |
| --- | --- | --- |
| 50 % | 20 % | 0 % |
| 80 % | 10 % | 10 % |
| 100 % | 0 % | 100 % |

Výsledkom transakcií sú nasledujúce sumy:

- Fáza 1:
  - Splatná čiastka je 50 x 300 alebo 15 000.
  - 20 percent zo sumy, čiže 3 000, je zadržaných a budú uvoľnené v neskoršej fáze.
  - Suma, ktorá je zaplatená predajcovi, je 12 000.
- Fáza 2:
  - Splatná čiastka je 30 x 300 alebo 9 000.
  - 10 percent zo sumy, alebo 900, je zachovaných.
  - Uvoľňuje sa 10 percent z 3 000, ktoré boli zadržané vo fáze 1 alebo 300.
  - Suma, ktorá je zaplatená predajcovi, je 8 400. Táto čiastka je 9 000 mínus 900 zadržaných plus 300, ktoré boli uvoľnené zo zadržania v rámci fázy 1.
- Fáza 3:
  - Splatná čiastka je 20 x 300 alebo 6 000.
  - Nezadržiava sa žiadna čiastka.
  - Suma, ktorá je uvoľnená, je 3 600. Toto množstvo pozostáva z 3 000, ktoré boli zadržané vo fáze 1, mínus 300 z fázy 1, ktoré bola uvoľnené vo fáze 2, plus 900, ktoré boli zadržané vo fáze 2.
  - Suma, ktorá je zaplatená predajcovi, je 9 600. Táto suma pozostáva zo zadržanej sumy 3 600 plus 6 000 za dokončenie fázy 3.

Celková čiastka zaplatená dodávateľovi po dokončení troch fáz je 30 000, čo je celková čiastka objednávky (15 000 + 9 000 + 6 000).
