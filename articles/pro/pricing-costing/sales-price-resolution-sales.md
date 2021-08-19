---
title: Riešenie predajných cien pre odhady projektov a skutočné hodnoty
description: Táto téma poskytuje informácie o riešení predajných cien pri odhadoch a skutočných hodnotách.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2152b3f59050482cab0d1c5940d6743f420206bfc90e034dc2d754df8bd513a5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996095"
---
# <a name="resolve-sales-prices-for-project-estimates-and-actuals"></a>Riešenie predajných cien pre odhady projektov a skutočné hodnoty

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Keď sa predajné ceny na základe odhadov a skutočností vyriešia v rámci Dynamics 365 Project Operations, systém najskôr použije dátum a menu príslušnej ponuky alebo zmluvy na vyriešenie cenníka predaja. Po vyriešení predajného cenníka systém vyrieši predajnú alebo fakturačnú sadzbu.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Riešenie predajných sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre čas

V rámci Project Operations sa riadky odhadu času používajú na označenie riadku ponuky a podrobností riadku kontraktu pre čas a priradenia zdrojov v projekte.

Po vyriešení cenníka predaja systém dokončí nasledujúce kroky a predvolí fakturačnú sadzbu.

1. Systém používa polia **Rola**, **Zdrojová jednotka** a na riadku odhadu času, aby sa zhodovali s riadkami cenníka roly vo vyriešenom cenníku. Táto zhoda predpokladá, že používate cenové dimenzie dostupné pre využívané sadzby fakturácie. Ak ste konfigurovali cenu na základe akýchkoľvek iných polí namiesto, alebo okrem položiek **Rola** a **Zdrojová jednotka**, tak sa na získanie zodpovedajúceho riadka s cenou roly použije iná kombinácia.
2. Ak systém nájde riadok s cenou roly s fakturačnou sadzbou pre kombináciu polí **Rola** a **Zdrojová jednotka**, bude daná fakturačná sadzba predvolená.
3. Ak sa systém nemôže zhodovať s hodnotami polí **Rola** a **Zdrojová jednotka**, tak načíta riadky s cenami rolí so zodpovedajúcou rolou, ale s nulovými hodnotami parametra **Zdrojová jednotka**. Keď systém nájde záznam ceny zodpovedajúcej role, predvolene nastaví fakturačnú sadzbu z tohto záznamu. Toto priradenie predpokladá predpripravenú konfiguráciu relatívnej priority **Rola** vs **Zdrojová jednotka** ako dimenzia predajných cien.

> [!NOTE]
> Ak nakonfigurujete inú prioritu pre položky **Rola** a **Zdrojová jednotka**, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, toto správanie sa zodpovedajúcim spôsobom zmení. Systém načítava záznamy cien rolí s hodnotami, ktoré sa zhodujú s každou z hodnôt dimenzií ceny, v poradí podľa priority s riadkami, ktoré majú nulové hodnoty pre tieto dimenzie prichádzajúce ako posledné.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Riešenie predajných sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre výdavky

V rámci Project Operations sa riadky odhadu výdavkov používajú na označenie riadku ponuky a podrobností riadku kontraktu pre výdavky a riadok s odhadom výdavkov v projekte.

Po vyriešení cenníka predaja systém dokončí nasledujúce kroky a predvolí fakturačnú predajnú jednotkovú sadzbu.

1. Po vyriešení cenníka nákladov systém použije kombináciu polí **Kategória** a **Jednotka** pre kombináciu poľa a odhadu nákladov, ktorý sa zhoduje s riadkami ceny kategórie vo vyriešenom cenníku.
2. Ak systém nájde riadok s cenou kategórie, ktorá má predajnú sadzbu pre kombináciu polí **Kategória** a **Jednotka**, predajná sadzba bude predvolená.
3. Ak systém nájde cenový riadok zodpovedajúcej kategórie, môže sa na predvolenie predajnej ceny použiť metóda určovania cien. Nasledujúca tabuľka nižšie zobrazuje predvolené správanie ceny výdavkov v Project Operations.

    | Kontext | Spôsob oceňovania | Predvolená cena |
    | --- | --- | --- |
    | Odhadované | Cena za jednotku | Na základe riadka kategórie ceny |
    | &nbsp; | V rámci nákladov | 0.00 |
    | &nbsp; | Prirážka nad rámec nákladov | 0.00 |
    | Skutočnosť | Cena za jednotku | Na základe riadka kategórie ceny |
    | &nbsp; | V rámci nákladov | Na základe súvisiacej skutočnej ceny |
    | &nbsp; | Prirážka nad rámec nákladov | Uplatnením prirážky definovanej v riadku ceny kategórie na sadzbu jednotkových nákladov súvisiacej skutočnej ceny |

4. Ak systém nedokáže priradiť hodnoty polí **Kategória** a **Jednotka**, sadzba predaja je predvolene nastavená na nulu (0).

## <a name="resolving-sales-rates-on-actual-and-estimate-lines-for-material"></a>Riešenie predajných sadzieb v riadkoch skutočných a odhadovaných hodnôt pre materiál

V Project Operations sa odhadované riadky pre materiál používajú na zaznamenanie detailov riadka cenovej ponuky a riadka zmluvy pre materiály a odhadované riadky materiálu v projekte.

Po vyriešení cenníka predaja systém dokončí nasledujúce kroky a predvolí fakturačnú predajnú jednotkovú sadzbu.

1. Systém používa kombináciu polí **Produkt** a **Jednotka** na riadku odhadu pre materiál na spárovanie s riadkami položiek v cenníku v cenníku, ktorý boli vyriešený.
2. Ak systém nájde riadok položky v cenníku, ktorý má predajnú sadzbu pre kombináciu polí **Produkt** a **Jednotka** a metóda určovania cien je **Čiastka v mene**, použije sa predajná cena uvedená v riadku cenníka.
3. Ak hodnoty polí **Produkt** a **Jednotka** nesúhlasia, predajná sadzba sa predvolene nastaví na nulu.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
