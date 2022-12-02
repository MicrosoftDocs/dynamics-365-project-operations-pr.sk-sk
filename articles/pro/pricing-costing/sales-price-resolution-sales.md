---
title: Určenie predajných cien pre odhady a skutočné hodnoty projektu
description: Tento článok poskytuje informácie o tom, ako sa určujú predajné ceny pre odhady a aktuálne hodnoty na základe projektu.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475204"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Určenie predajných cien pre odhady a skutočné hodnoty projektu

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Na určenie predajných cien na základe odhadov a skutočných hodnôt v Microsoft Dynamics 365 Project Operations systém najprv použije dátum a menu v kontexte prichádzajúceho odhadu alebo skutočnej hodnoty na určenie predajného cenníka. V kontexte skutočnej hodnoty systém používa pole **Dátum transakcie** na určenie, ktorý cenník je platný. Hodnota **Dátum transakcie** vstupného odhadu alebo skutočnej hodnoty sa porovnáva s hodnotami **Začiatok účinnosti (nezávislý od časového pásma)** a **Koniec účinnosti (nezávislý od časového pásma)** v cenníku. Po určení predajného cenníka systém určí predajnú alebo fakturačnú sadzbu.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Určenie predajných sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre čas

Kontext odhadu pre **Čas** odkazuje na:

- Podrobnosti riadka cenovej ponuky pre **Čas**.
- Podrobnosti riadka zmluvy pre **Čas**.
- Priradenie strojov v projekte.

Kontext skutočnej hodnoty pre **Čas** odkazuje na:

- Záznamy v účtovnom denníku Zadanie a Oprava pre **Čas**.
- Záznamy v účtovnom denníku, ktoré sa vytvoria pri odoslaní zadania času.
- Podrobnosti o riadku faktúry pre **Čas**. 

Po určení cenníka predaja systém dokončí nasledujúce kroky a zadá predvolenú fakturačnú sadzbu.

1. Systém spáruje kombináciu polí **Rola** a **Zdrojová jednotka** v kontexte odhadu alebo skutočnej hodnoty pre **Čas** oproti riadkom s cenami rolí v cenníku. Toto zosúladenie predpokladá, že používate predvolené cenové dimenzie pre sadzby fakturácie. Ak ste konfigurovali cenu na základe iných polí ako **Rola** a **Zdrojová jednotka** alebo nad ich rámec, tak sa na získanie zodpovedajúceho riadka s cenou roly použije táto kombinácia polí.
1. Ak systém nájde riadok s cenou roly s fakturačnou sadzbou pre kombináciu **Rola** a **Zdrojová jednotka**, bude daná fakturačná sadzba použitá ako predvolená.
1. Ak systém nemôže spárovať hodnoty **Rola** a **Zdrojová jednotka**, vyhľadá riadky s cenami rolí, ktoré majú spárované hodnoty pre pole **Rola**, ale nulové hodnoty pre pole **Zdrojová jednotka**. Keď systém nájde spárovaný záznam o cene roly, fakturačná sadzba z tohto záznamu sa použije ako predvolená fakturačná sadzba. Toto priradenie predpokladá predpripravenú konfiguráciu relatívnej priority **Rola** vs **Zdrojová jednotka** ako dimenzia predajných cien.

> [!NOTE]
> Ak nakonfigurujete inú prioritu pre polia **Rola** a **Zdrojová jednotka**, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, predchádzajúce správanie sa zodpovedajúcim spôsobom zmení. Systém načítava cenové záznamy rolí, ktoré majú hodnoty, ktoré zodpovedajú každej hodnote cenovej dimenzie v poradí podľa priority. Riadky, ktoré majú pre tieto dimenzie nulové hodnoty, sú posledné.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Určenie predajných sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre Výdavok

Kontext odhadu pre **Výdavok** odkazuje na:

- Podrobnosti riadka cenovej ponuky pre **Výdavok**.
- Podrobnosti riadka zmluvy pre **Výdavok**.
- Riadky odhadu výdavkov pre projekt.

Kontext skutočnej hodnoty pre **Výdavok** odkazuje na:

- Záznamy v účtovnom denníku Zadanie a Oprava pre **Výdavok**.
- Záznamy v účtovnom denníku, ktoré sa vytvoria pri odoslaní zadania výdavku.
- Podrobnosti riadka faktúry pre **Výdavok**. 

Po určení cenníka predaja systém dokončí nasledujúce kroky na zadanie predvolenej predajnej jednotkovej ceny.

1. Systém spáruje kombináciu polí **Kategória** a **Jednotka** na riadku odhadu pre **Výdavok** s cenovými riadkami kategórie v cenníku.
1. Ak systém nájde riadok s cenou kategórie, ktorá má predajnú sadzbu pre kombináciu polí **Kategória** a **Jednotka**, predajná sadzba sa použije ako predvolená.
1. Ak systém nájde cenový riadok zodpovedajúcej kategórie, môže sa na metóda nacenenia použiť na zadanie predvolenej predajnej ceny. Nasledujúca tabuľka nižšie zobrazuje predvolené správanie pre ceny výdavkov v Project Operations.

    | Kontext | Spôsob oceňovania | Predvolená cena |
    | --- | --- | --- |
    | Odhadované | Jednotková cena | Na základe riadka kategórie ceny. |
    |        | V rámci nákladov | 0.00 |
    |        | Prirážka nad rámec nákladov | 0.00 |
    | Skutočnosť | Jednotková cena | Na základe riadka kategórie ceny. |
    |        | V rámci nákladov | Na základe súvisiacej skutočnej ceny. |
    |        | Prirážka nad rámec nákladov | Je uplatnená prirážka, ako je definované v riadku kategórie ceny na sadzbu jednotkových nákladov súvisiacej skutočnej ceny. |

1. Ak systém nedokáže spárovať hodnoty polí **Kategória** a **Jednotka**, sadzba predaja je predvolene nastavená na **0** (nulu).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Určenie predajných sadzieb v riadkoch skutočných a odhadovaných hodnôt pre materiál

Kontext odhadu pre **Materiál** odkazuje na:

- Podrobnosti riadka cenovej ponuky pre **Materiál**.
- Podrobnosti riadka zmluvy pre **Materiál**.
- Riadky odhadu materiálu pre projekt.

Kontext skutočnej hodnoty pre **Materiál** odkazuje na:

- Záznamy v účtovnom denníku Zadanie a Oprava pre **Materiál**.
- Záznamy v účtovnom denníku, ktoré sa vytvoria pri odoslaní denníka použitia materiálu.
- Podrobnosti riadka faktúry pre **Materiál**. 

Po určení cenníka predaja systém dokončí nasledujúce kroky na zadanie predvolenej predajnej jednotkovej ceny.

1. Systém spáruje kombináciu polí **Produkt** a **Jednotka** na riadku odhadu pre **Materiál** s riadkami položiek v cenníku.
1. Ak systém nájde riadok položky v cenníku, ktorý má predajnú sadzbu pre kombináciu **Produkt** a **Jednotka** a metóda určovania cien je **Čiastka v mene**, použije sa predajná cena uvedená v riadku cenníka. 
1. Ak sa hodnoty polí **Produkt** a **Jednotka** nezhodujú, alebo ak je metóda určovania cien iná ako **Čiastka v mene**, predajná sadzba je nastavená štandardne na **0** (nula). Toto správanie sa vyskytuje, pretože Project Operations podporuje iba spôsob oceňovania **Čiastka v mene** materiálov, ktoré sa používajú na projekte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
