---
title: Riešenie obstarávacích cien pre odhady a skutočné hodnoty
description: Táto téma poskytuje informácie o tom, ako vyriešiť obstarávacie ceny pre odhady a skutočné hodnoty.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7395a1845f4a895efbabda36ba3b2a2f3c1eea52
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587927"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Riešenie obstarávacích cien pre odhady a skutočné hodnoty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Na riešenie obstarávacích cien a cenníka obstarávacích cien pre odhady a skutočné hodnoty systém používa informácie v poliach **Dátum**, **Mena** a **Zmluvná jednotka** súvisiaceho projektu. Po vyriešení cenníka obstarávacích cien aplikácia vyrieši nákladovú sadzbu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Riešenie nákladových sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre čas

Riadky s odhadmi pre čas sa týkajú riadkov s podrobnosťami o cenovej ponuke a zmluve pre pridelenie času a zdroja pre projekt.

Po vyriešení cenníka obstarávacích cien systém používa polia **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka** na riadku odhadu času, aby sa zhodovali s riadkami cenníka roly v cenníku. Táto zhoda predpokladá, že používate cenové dimenzie dostupné pri zakúpení pre náklady na prácu. Ak ste nakonfigurovali systém tak, aby zodpovedal poliam namiesto, alebo okrem položiek **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, tak sa na získanie zodpovedajúceho riadka s cenou roly použije iná kombinácia. Ak aplikácia nájde riadok s cenou roly s nákladovou sadzbou pre kombináciu **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, bude to predvolená nákladová sadzba. Ak sa aplikácia nemôže presne zosúladiť kombináciu hodnôt **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, načíta riadky cien rolí so zodpovedajúcou hodnotou roly, ale bude mať nulové hodnoty pre položky **Zdrojová jednotka** a **Spoločnosť zaisťujúca zdroje**. Po nájdení cenového záznamu zodpovedajúcej roly s hodnotou ceny zodpovedajúcej roly sa sadzba nákladov predvolene nastaví z tohto záznamu. 

> [!NOTE]
> Ak nakonfigurujete inú prioritu pre položky **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, toto správanie sa zodpovedajúcim spôsobom zmení. Systém načítava záznamy cien rolí s hodnotami, ktoré sa zhodujú s každou z hodnôt cenových dimenzií v poradí podľa priority, s riadkami, ktoré majú nulové hodnoty pre tie dimenzie, ktoré prichádzajú ako posledné v poradí priority.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Riešenie nákladových sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre náklad

Riadky s odhadmi pre náklad sa týkajú riadkov s podrobnosťami o cenovej ponuke a zmluve pre náklady a riadky odhadov výdavkov pre projekt.

Po vyriešení cenníka nákladov systém použije kombináciu polí **Kategória** a **Jednotka** pre riadok odhadu nákladov, ktorý sa zhoduje s riadkami **Cena kategórie** vo vyriešenom cenníku. Ak systém nájde riadok s cenou kategórie, ktorá má nákladovú sadzbu pre kombináciu polí **Kategória** a **Jednotka**, nákladová sadzba bude predvolená. Ak systém nedokáže zosúladiť hodnoty **Kategória** a **Jednotka**, alebo ak je schopný nájsť zodpovedajúci riadok s cenou kategórie, ale metóda oceňovania nie je **Cena za jednotku**, nákladová sadzba je predvolene nastavená na nulu (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Riešenie nákladových sadzieb v riadkoch skutočných a odhadovaných hodnôt pre materiál

Odhadované riadky pre materiál sa týkajú detailov cenovej ponuky a riadka zmluvy pre materiály a odhadované riadky materiálu v projekte.

Po vyriešení cenníka nákladových cien systém použije kombináciu polí **Produkt** a **Jednotka** na riadku odhadu pre odhad materiálu, na spárovanie odhadu materiálu s riadkami **Položky v cenníku** vo vyriešenom cenníku. Ak systém nájde riadok ceny produktu, ktorý má nákladovú sadzbu pre kombináciu polí **Produkt** a **Jednotka**, nákladová sadzba sa nastaví na predvolenú hodnotu. Ak sa systém nedokáže zosúladiť hodnoty **Produkt** a **Jednotka**, jednotkové náklady sa predvolene nastavia na nulu. Toto predvolené nastavenie nastane aj v prípade, že existuje zodpovedajúci riadok položky v cenníku, ale metóda určovania cien je založená na štandardných nákladoch alebo aktuálnych nákladoch, ktoré nie sú definované v produkte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
