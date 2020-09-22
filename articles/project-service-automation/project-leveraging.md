---
title: Odhady predaja a projekty
description: Táto téma poskytuje informácie o tom, ako využiť plán a odhady v procese predaja.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755564"
---
# <a name="sales-estimates-and-projects"></a>Odhady predaja a projekty

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Počas procesu predaja môžete vytvoriť odhady predaja prepojením projektu s predajnou cenovou ponukou. Týmto spôsobom sa môže vyskytnúť definovaný odhad počas predajného procesu, aby sa využili výhody možnosti plánovania a odhadu projektu. Ak predaj prekročí, plán, ktorý bol použitý na účely odhadu predaja, môže byť použitý ako základ pre ďalšie upresnenie projektového plánu.

## <a name="linking-a-project-to-a-quote-line"></a>Prepojenie projektu s riadkom cenovej ponuky

Keď vytvoríte riadok cenovej ponuky založený na projekte, môžete vytvoriť nový projekt alebo priradiť existujúci projekt na stránke **riadok cenovej ponuky**. 

> ![Formulár riadka cenovej ponuky](media/project-8.png)
 
Keď vytvoríte nový projekt z podrobností riadka cenovej ponuky, môžete využiť šablóny projektu. Šablóny projektu sú modelové projekty, ktoré predstavujú štandardné projektové plány a finančné odhady, ktoré sú typické pre organizáciu. Môžu tiež reprezentovať kópie projektových plánov a odhadov z minulých projektov.

> ![Podrobnosti o riadku cenovej ponuky](media/project-9.png)
  
Keď vytvoríte projekt z cenovej ponuky, projekt sa automaticky priradí k riadku cenovej ponuky.

## <a name="components-of-estimates-in-a-project"></a>Zložky odhadov v projekte

Plán vám umožňuje rozdeliť prácu na úlohy, udržiavať hierarchiu úloh, určiť, aké zdroje sú potrebné na dokončenie úlohy a priradiť odhad úsilia, ktoré je potrebné na dokončenie úlohy.

Pracovné úsilie a odhady plánu môžete definovať pomocou polí na karte **plán** na stránke **projekt**. Keďže je v projekte priradený cenník, finančné odhady sa vypočítavajú pomocou nákladov a predajných cien definovaných v ceníku.

## <a name="importing-estimates-from-a-project-into-a-quote"></a>Import odhadov z projektu do cenovej ponuky

Po definovaní odhadov projektu ich môžete importovať do riadka cenovej ponuky. Na stránke **Podrobnosti riadka cenovej** vyberte položku **importovať z odhadov** na páse s nástrojmi a zhrňte odhady projektov podľa typu transakcie, roly alebo úlohy.
