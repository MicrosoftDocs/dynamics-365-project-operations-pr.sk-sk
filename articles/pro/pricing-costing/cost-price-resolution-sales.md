---
title: Riešenie obstarávacích cien pre odhady a skutočné hodnoty
description: Táto téma poskytuje informácie o tom, ako vyriešiť obstarávacie ceny pre odhady a skutočné hodnoty.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bad8f4b95ac5803d3f334e1b306d2a9d27a6645d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084274"
---
# <a name="resolving-cost-prices-on-estimates-and-actuals"></a>Riešenie obstarávacích cien pre odhady a skutočné hodnoty

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Na riešenie obstarávacích cien a cenníka obstarávacích cien pre odhady a skutočné hodnoty systém používa informácie v poliach **Dátum** , **Mena** a **Zmluvná jednotka** súvisiaceho projektu. Po vyriešení cenníka obstarávacích cien aplikácia vyrieši nákladovú sadzbu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Riešenie nákladových sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre čas

Riadky s odhadmi pre čas sa týkajú riadkov s podrobnosťami o cenovej ponuke a zmluve pre pridelenie času a zdroja pre projekt.

Po vyriešení cenníka obstarávacích cien systém používa polia **Rola** a **Zdrojová jednotka** v riadku odhadu času, aby sa zhodovali s riadkami cenníka roly v cenníku. Táto zhoda predpokladá, že používate cenové dimenzie dostupné pri zakúpení pre náklady na prácu. Ak ste nakonfigurovali systém tak, aby zodpovedal poliam namiesto, alebo okrem položiek **Rola** a **Zdrojová jednotka** , tak sa na získanie zodpovedajúceho riadka s cenou roly použije iná kombinácia. Ak aplikácia nájde riadok s cenou roly s nákladovou sadzbou pre kombináciu **Rola** a **Zdrojová jednotka** , bude to predvolená nákladová sadzba. Ak sa aplikácia nemôže zhodovať s hodnotami **Rola** a **Zdrojová jednotka** , tak načíta riadky s cenami rolí so zodpovedajúcou rolou, ale s nulovými hodnotami parametra **Zdrojová jednotka**. Keď obsahuje zodpovedajúci záznam o cene roly, bude predvolená nákladová sadzba z tohto záznamu. 

> [!NOTE]
> Ak nakonfigurujete inú prioritu pre položky **Rola** a **Zdrojová jednotka** , alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, toto správanie sa zodpovedajúcim spôsobom zmení. Systém načítava záznamy cien rolí s hodnotami, ktoré sa zhodujú s každou z hodnôt dimenzií ceny, v poradí podľa priority s riadkami, ktoré majú nulové hodnoty pre tieto dimenzie prichádzajúce ako posledné.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Riešenie nákladových sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre náklad

Riadky s odhadmi pre náklad sa týkajú riadkov s podrobnosťami o cenovej ponuke a zmluve pre náklady a riadky odhadov výdavkov pre projekt.

Po vyriešení cenníka nákladov systém použije kombináciu polí **Kategória** a **Jednotka** pre riadok odhadu nákladov, ktorý sa zhoduje s riadkami **Cena kategórie** vo vyriešenom cenníku. Ak systém nájde riadok s cenou kategórie, ktorá má nákladovú sadzbu pre kombináciu polí **Kategória** a **Jednotka** , nákladová sadzba bude predvolená. Ak systém nedokáže zosúladiť hodnoty **Kategória** a **Jednotka** , alebo ak je schopný nájsť zodpovedajúci riadok s cenou kategórie, ale metóda oceňovania nie je **Cena za jednotku** , nákladová sadzba je predvolene nastavená na nulu (0).
