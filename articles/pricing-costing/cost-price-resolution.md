---
title: Určenie nákladových sadzieb pre odhady a skutočné hodnoty založené na projektoch
description: Tento článok poskytuje informácie o tom, ako sa určujú nákladové sadzby pre odhady a skutočné hodnoty založené na projektoch.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475298"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Určenie nákladových sadzieb pre odhady a skutočné hodnoty založené na projektoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Na určenie obstarávacích cien na základe odhadov a skutočných hodnôt v Microsoft Dynamics 365 Project Operations systém najprv použije dátum a menu v kontexte prichádzajúceho odhadu alebo skutočnej hodnoty na určenie predajného cenníka. V kontexte skutočnej hodnoty systém používa pole **Dátum transakcie** na určenie, ktorý cenník je platný. Hodnota **Dátum transakcie** vstupného odhadu alebo skutočnej hodnoty sa porovnáva s hodnotami **Začiatok účinnosti (nezávislý od časového pásma)** a **Koniec účinnosti (nezávislý od časového pásma)** v cenníku. Po určení cenníka obstarávacích cien systém určí nákladovú sadzbu.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Určenie nákladových sadzieb v kontexte odhadov a skutočných hodnôt pre čas

Kontext odhadu pre **Čas** odkazuje na:

- Podrobnosti riadka cenovej ponuky pre **Čas**.
- Podrobnosti riadka zmluvy pre **Čas**.
- Priradenie strojov v projekte.

Kontext skutočnej hodnoty pre **Čas** odkazuje na:

- Záznamy v účtovnom denníku Zadanie a Oprava pre **Čas**.
- Záznamy v účtovnom denníku, ktoré sa vytvoria pri odoslaní zadania času.

Po určení cenníka obstarávacích cien systém dokončí nasledujúce kroky a zadá predvolenú nákladovú sadzbu.

1. Systém zosúladí kombináciu polí **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka** v kontexte odhadu alebo skutočnej hodnoty pre **Čas** oproti riadkom s cenami rolí v cenníku. Toto spárovanie predpokladá, že používate štandardné cenové dimenzie pre náklady na prácu. Ak ste nakonfigurovali systém tak, aby spároval polia iné ako **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, alebo polia nad ich rámec, tak sa na získanie zodpovedajúceho riadka s cenou roly použije iná kombinácia.
1. Ak systém nájde riadok s cenou roly s nákladovou sadzbou pre kombináciu **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, táto nákladová sadzba sa použije ako predvolená nákladová sadzba.
1. Ak systém nedokáže spárovať hodnoty **Rola**, **Spoločnosť zaisťujúca zdroje** a **Zdrojová jednotka**, zruší dimenziu, ktorá má najnižšiu prioritu, vyhľadá riadky cien rol, ktoré sa zhodujú s ďalšími dvoma hodnotami dimenzie, a pokračuje v postupnom znižovaní dimenzií, kým sa nenájde zodpovedajúci riadok ceny roly. Sadzba nákladov z tohto záznamu sa použije ako predvolená sadzba nákladov. Ak systém nenájde zodpovedajúci riadok s cenou roly, cena sa nastaví štandardne na **0** (nula).

> [!NOTE]
> Ak nakonfigurujete inú prioritu pre polia **Rola** a **Zdrojová jednotka**, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, predchádzajúce správanie sa zodpovedajúcim spôsobom zmení. Systém načítava cenové záznamy rolí, ktoré majú hodnoty, ktoré zodpovedajú každej hodnote cenovej dimenzie v poradí podľa priority. Riadky, ktoré majú pre tieto dimenzie nulové hodnoty, sú posledné.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Určenie nákladových sadzieb v riadkoch so skutočnými hodnotami a odhadmi pre Výdavok

Kontext odhadu pre **Výdavok** odkazuje na:

- Podrobnosti riadka cenovej ponuky pre **Výdavok**.
- Podrobnosti riadka zmluvy pre **Výdavok**.
- Odhady výdavkov na projekt.

Kontext skutočnej hodnoty pre **Výdavok** odkazuje na:

- Záznamy v účtovnom denníku Zadanie a Oprava pre **Výdavok**.
- Záznamy v účtovnom denníku, ktoré sa vytvoria pri odoslaní zadania výdavku.

Po určení cenníka obstarávacích cien systém dokončí nasledujúce kroky a zadá predvolenú nákladovú sadzbu.

1. Systém spáruje kombináciu polí **Kategória** a **Jednotka** v kontexte odhadu alebo skutočnej hodnoty pre **Výdavok** oproti riadkom s cenami kategórií v cenníku.
1. Ak systém nájde riadok s cenou kategórie, ktorá má nákladovú sadzbu pre kombináciu polí **Kategória** a **Jednotka**, Táto nákladové sadzba sa použije ako predvolená.
1. Ak systém nedokáže spárovať hodnoty polí **Kategória** a **Jednotka**, cena je predvolene nastavená na **0** (nulu).
1. V kontexte odhadu, ak systém dokáže nájsť zodpovedajúci riadok s cenou kategórie, ale metóda oceňovania je iná ako **Cena za jednotku**, nákladová sadzba je štandardne nastavená na **0** (nula).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Určenie nákladových sadzieb v riadkoch skutočných a odhadovaných hodnôt pre materiál

Kontext odhadu pre **Materiál** odkazuje na:

- Podrobnosti riadka cenovej ponuky pre **Materiál**.
- Podrobnosti riadka zmluvy pre **Materiál**.
- Odhady materiálov v projekte.

Kontext skutočnej hodnoty pre **Materiál** odkazuje na:

- Záznamy v účtovnom denníku Zadanie a Oprava pre **Materiál**.
- Záznamy v účtovnom denníku, ktoré sa vytvoria pri odoslaní denníka použitia materiálu.

Po určení cenníka obstarávacích cien systém dokončí nasledujúce kroky a zadá predvolenú nákladovú sadzbu.

1. Systém používa kombináciu polí **Kategória** a **Jednotka** v kontexte odhadu alebo skutočnej hodnoty pre **Materiál** oproti riadkom položiek v cenníku.
1. Ak systém nájde riadok položky v cenníku, ktorá má nákladovú sadzbu pre kombináciu polí **Produkt** a **Jednotka**, táto nákladová sadzba sa použije ako predvolená.
1. Ak sa systém nedokáže spárovať hodnoty **Produkt** a **Jednotka**, jednotkové náklady sa predvolene nastavia na **0** (nula).
1. V kontexte odhadu alebo skutočnej hodnoty, ak systém dokáže nájsť zodpovedajúci riadok položky v cenníku, ale spôsob oceňovania je iný ako **Čiastka v mene**, jednotková cena je predvolene nastavená na **0**. Toto správanie sa vyskytuje, pretože Project Operations podporuje iba spôsob oceňovania **Čiastka v mene** materiálov, ktoré sa používajú na projekte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
