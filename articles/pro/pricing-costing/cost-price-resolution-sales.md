---
title: Riešenie obstarávacích cien v odhadoch a skutočných hodnotách projektov
description: Táto téma poskytuje informácie o tom, ako sa riešia obstarávacie ceny pri odhadoch a skutočných hodnotách projektu.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a2a2df7672118a4a4d7748795174e8e8238dd7618a48437185879e06a253a381
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6997580"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Riešenie obstarávacích cien v odhadoch a skutočných hodnotách projektov 

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Na riešenie obstarávacích cien a cenníka obstarávacích cien pre odhady a skutočné hodnoty systém používa informácie v poliach **Dátum**, **Mena** a **Zmluvná jednotka** súvisiaceho projektu. Po vyriešení cenníka obstarávacích cien aplikácia vyrieši nákladovú sadzbu.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Riešenie nákladových sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre čas

Riadky s odhadmi pre čas sa týkajú riadkov s podrobnosťami o cenovej ponuke a zmluve pre pridelenie času a zdroja pre projekt.

Po vyriešení cenníka obstarávacích cien sa polia **Rola** a **Zdrojová jednotka** v riadku odhadu pre Čas zhodujú s riadkami cenových rolí v cenníku. Táto zhoda predpokladá, že používate štandardné cenové dimenzie pre náklady na prácu. Ak ste nakonfigurovali systém tak, aby zodpovedal poliam namiesto, alebo okrem položiek **Rola** a **Zdrojová jednotka**, tak sa na získanie zodpovedajúceho riadka s cenou roly použije iná kombinácia. Ak aplikácia nájde riadok s cenou roly s nákladovou sadzbou pre kombináciu **Rola** a **Zdrojová jednotka**, bude to predvolená nákladová sadzba. Ak sa aplikácia nemôže zhodovať s hodnotami **Rola** a **Zdrojová jednotka**, tak načíta riadky s cenami rolí so zodpovedajúcou rolou, ale s nulovými hodnotami parametra **Zdrojová jednotka**. Keď obsahuje zodpovedajúci záznam o cene roly, bude predvolená nákladová sadzba z tohto záznamu. 

> [!NOTE]
> Ak nakonfigurujete inú prioritu pre položky **Rola** a **Zdrojová jednotka**, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, toto správanie sa zodpovedajúcim spôsobom zmení. Systém načítava záznamy cien rolí s hodnotami, ktoré sa zhodujú s každou z hodnôt dimenzií ceny, v poradí podľa priority s riadkami, ktoré majú nulové hodnoty pre tieto dimenzie prichádzajúce ako posledné.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Riešenie nákladových sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre náklad

Riadky s odhadmi pre náklad sa týkajú riadkov s podrobnosťami o cenovej ponuke a zmluve pre náklady a riadky odhadov výdavkov pre projekt.

Po vyriešení cenníka obstarávacích cien systém použije kombináciu polí **Kategória** a **Jednotka** v riadku odhadu výdavkov, aby sa zhodovali s riadkami **Cena kategórie** na vyriešenom cenníku. Ak systém nájde riadok s cenou kategórie, ktorá má nákladovú sadzbu pre kombináciu polí **Kategória** a **Jednotka**, nákladová sadzba bude predvolená. Ak systém nedokáže zosúladiť hodnoty **Kategória** a **Jednotka**, alebo ak dokáže nájsť cenovú linku zodpovedajúcej kategórie, ale metóda určovania cien nie je **Cena za jednotku**, sadzba nákladov je predvolene nastavená na nulu (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Riešenie nákladových sadzieb v riadkoch skutočných a odhadovaných hodnôt pre materiál

Odhadované riadky pre materiál sa týkajú detailov cenovej ponuky a riadka zmluvy pre materiály a odhadované riadky materiálu v projekte.

Po vyriešení cenníka nákladových cien systém použije kombináciu polí **Produkt** a **Jednotka** na riadku odhadu pre odhad materiálu, na spárovanie odhadu materiálu s riadkami **Položky v cenníku** vo vyriešenom cenníku. Ak systém nájde riadok ceny produktu, ktorý má nákladovú sadzbu pre kombináciu polí **Produkt** a **Jednotka**, nákladová sadzba sa nastaví na predvolenú hodnotu. Ak sa systém nedokáže spárovať hodnoty **Produkt** a **Jednotka**, alebo ak dokáže nájsť zodpovedajúci riadok položky v cenníku, ale metóda určovania cien je založená na štandardných cenách alebo aktuálnych cenách a ani jedna z nich nie je na produkte definovaná, jednotkové náklady sa predvolene nastavia na nulu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
