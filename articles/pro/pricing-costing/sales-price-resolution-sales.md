---
title: Riešenie predajných cien pre odhady a skutočné hodnoty – čiastočné
description: Táto téma poskytuje informácie o tom, ako vyriešiť predajné ceny pre odhady a skutočné hodnoty.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 92cebbe851c3cface86d0580e7e060134295e8c2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176765"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals---lite"></a>Riešenie predajných cien pre odhady a skutočné hodnoty – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Keď sa predajné ceny na základe odhadov a skutočností vyriešia v rámci Dynamics 365 Project Operations, systém najskôr použije dátum a menu príslušnej ponuky alebo kontraktu na vyriešenie cenníka predajných cien. Po vyriešení predajného cenníka systém vyrieši predajnú alebo fakturačnú sadzbu.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]