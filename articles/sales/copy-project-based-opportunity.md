---
title: Kopírovanie príležitostí založených na projekte
description: Táto téma poskytuje informácie o tom, ako kopírovať príležitosti založené na projekte v Project Operations.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ca48125d90ee50c5621780be19bd4ceb2130d2d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577807"
---
# <a name="copy-project-based-opportunities"></a>Kopírovanie príležitostí založených na projekte

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


Projektové príležitosti možno ľahko kopírovať a vytvoriť tak nové príležitosti projektu. 

1. Prejdite na stránku so zoznamom **Projektové príležitosti** vyberte príležitosť zo zoznamu. Prípadne otvorte stránku s podrobnosťami o konkrétnej príležitosti. 
2. Na ktorejkoľvek stránke vyberte **Kopírovať**. Otvorí sa dialógové okno, ktoré obsahuje nasledujúce informácie o poli. V závislosti od hodnôt zvolených v tomto dialógovom okne sa môže proces kopírovania zmeniť.

    | **Pole** | **Opis** | **Nadväzujúci vplyv** |
    | --- | --- | --- |
    | Predmet | Zadajte príslušnú tému cieľovej príležitosti. Keď sa otvorí dialógové okno, systém ho nastaví na tému zdrojovej príležitosti s doplnkom **-kópia**. | Toto pole nemá žiadny následný dopad. |
    | Konto | Odkazy na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. Po otvorení dialógového okna ho systém nastaví na účet uvedený v zdrojovej príležitosti. | Toto pole je primárnym zákazníkom v príležitosti. |
    | Zmluvná jednotka | Organizačná jednotka zodpovedná za realizáciu projektov spojených s týmto obchodom. Po otvorení dialógového okna ho systém nastaví na zmluvnú jednotku zdrojovej príležitosti. | Zmluvnou jednotkou je divízia spoločnosti, ktorá po uzatvorení obchodu realizuje projekty. Každá zmluvná jednotka má menu, ktorá sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas projektu. |
    | Mena | Mena, v ktorej sa obchoduje transakcia. Po otvorení stránky dialógového okna ho systém nastaví na menu zdrojovej príležitosti. | Mena sa používa pre predvolený cenník a na zostavenie finančných odhadov cenovej ponuky. Mena sa prípadne použije na fakturáciu zákazníkovi po získaní obchodu. |
    | Kopírovať cenu | Hodnota Áno/Nie, ktorá označuje, či sa má cena z príležitosti kopírovať zo zdrojovej príležitosti. | Ak je vybraná možnosť **Áno**, cenníky sa skopírujú zo zdroja do cieľovej príležitosti. Ak je vybraná možnosť **Nie**, cenníky sa znova predvolene nastavujú na základe najnovších cenníkov, ktoré boli nastavené. |

3. Vyberte položku **OK**. Systém vytvorí kópiu projektovej príležitosti na základe zvolených parametrov a otvorí sa nová projektová príležitosť.


[!INCLUDE[footer-include](../includes/footer-banner.md)]