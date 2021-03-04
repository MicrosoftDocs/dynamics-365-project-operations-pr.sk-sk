---
title: Riešenie predajných cien pre odhady a skutočné hodnoty
description: Táto téma poskytuje informácie o tom, ako vyriešiť predajné sadzby pre odhady a skutočnosti.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119572"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Riešenie predajných cien pre odhady a skutočné hodnoty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keď sa predajné ceny na základe odhadov a skutočností vyriešia v rámci Dynamics 365 Project Operations, systém najskôr použije dátum a menu príslušnej ponuky alebo kontraktu na vyriešenie cenníka predajných cien. Po vyriešení predajného cenníka systém vyrieši predajnú alebo fakturačnú sadzbu.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Riešenie predajných sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre čas

V rámci Project Operations sa riadky odhadu času používajú na označenie riadku ponuky a podrobností riadku kontraktu pre čas a priradenia zdrojov v projekte.

Po vyriešení cenníka predaja systém dokončí nasledujúce kroky a predvolí fakturačnú sadzbu.

1. Systém používa polia **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka** na riadku odhadu času, aby sa zhodovali s riadkami cenníka roly vo vyriešenom cenníku. Táto zhoda predpokladá, že používate cenové dimenzie dostupné pre využívané sadzby fakturácie. Ak ste konfigurovali cenu na základe akýchkoľvek iných polí namiesto, alebo okrem položiek **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**,  tak sa na získanie zodpovedajúceho riadka s cenou roly použije iná kombinácia.
2. Ak systém nájde riadok s cenou roly s fakturačnou sadzbou pre kombináciu polí **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, bude daná fakturačná sadzba predvolená.
3. Ak sa systém nemôže zhodovať s hodnotami polí **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, tak načíta riadky s cenami rolí so zodpovedajúcou rolou, ale s nulovými hodnotami parametra **Zdrojová jednotka**. Keď systém nájde záznam ceny zodpovedajúcej role, predvolene nastaví fakturačnú sadzbu z tohto záznamu. Toto priradenie predpokladá predpripravenú konfiguráciu relatívnej priority **Rola** vs **Zdrojová jednotka** ako dimenzia predajných cien.

> [!NOTE]
> Ak nakonfigurujete inú prioritu pre položky **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, toto správanie sa zodpovedajúcim spôsobom zmení. Systém načítava záznamy cien rolí s hodnotami, ktoré sa zhodujú s každou z hodnôt dimenzií ceny, v poradí podľa priority s riadkami, ktoré majú nulové hodnoty pre tieto dimenzie prichádzajúce ako posledné.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]