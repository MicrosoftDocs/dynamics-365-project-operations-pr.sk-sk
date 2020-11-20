---
title: Odhady predaja a projekty
description: Táto téma poskytuje informácie o tom, ako využiť plán a odhady v procese predaja.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120697"
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
