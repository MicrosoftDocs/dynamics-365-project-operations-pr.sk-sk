---
title: Kopírovanie cenových ponúk založených na projekte
description: Táto téma poskytuje informácie o tom, ako kopírovať cenové ponuky založené na projekte v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1ce6c2b644319f2d822010a34c57c591f82edc9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278167"
---
# <a name="copy-project-based-quotes"></a>Kopírovanie cenových ponúk založených na projekte

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Novú cenovú ponuku projektu môžete ľahko vytvoriť skopírovaním existujúcej ponuky. 

- Ak chcete skopírovať ponuku projektu na stránke zoznamu **Cenové ponuky projektu** alebo na stránke s podrobnosťami **Cenová ponuka projektu** vyberte ponuku projektu, ktorú chcete skopírovať, a potom vyberte možnosť **Kopírovať**.

Otvorí sa dialógové okno, na ktorom môžete zadať parametre kópie. V nasledujúcej tabuľke je uvedený zoznam polí, ktoré sú obsiahnuté na dialógovej stránke. V závislosti od zvolených hodnôt sa môže proces kopírovania zmeniť.

| **Pole** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- |
| Predmet | Zadajte príslušnú tému alebo názov cieľovej cenovej ponuky. Keď sa otvorí dialógové okno, systém ho nastaví na tému zdrojovej ponuky s doplnkom **-kópia**. | |
| Potenciálny zákazník | Odkaz na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. Po otvorení dialógového okna ho systém nastaví na účet uvedený v zdrojovej cenovej ponuke. | Toto pole je primárnym zákazníkom v cenovej ponuke. |
| Zmluvná jednotka | Organizačná jednotka, ktorá je zodpovedná za realizáciu projektov spojených s týmto obchodom.
Po otvorení dialógového okna ho systém nastaví na zmluvnú jednotku cenovej ponuky. | Zmluvnou jednotkou je divízia spoločnosti, ktorá bude po uzatvorení obchodu realizovať projekty. Každá zmluvná jednotka má menu. Mena sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas realizácie projektu. |
| Mena | Je to mena, v ktorej sa obchoduje transakcia. Po otvorení dialógového okna ho systém nastaví na menu cenovej ponuky. Môže sa upravovať a ak ide o zmenu, pole **Kopírovať ceny** je vždy nastavené na **Nie**. Je to tak preto, lebo cenníky pri zdrojovej ponuke už nie sú relevantné. | Mena sa používa na predvolenie cenníka, na zostavenie finančného odhadu cenovej ponuky a prípadne na fakturáciu zákazníkovi, keď dôjde k získaniu obchodu. |
| Požadovaný dátum doručenia | Toto je dátum doručenia požadovaný zákazníkom. | Používa sa ako konečný dátum pri vytváraní fakturačných dátumov podľa konkrétnej frekvencie. |
| Kopírovať cenu | Hodnota Áno/Nie označuje, či sa má cena v cenovej ponuke kopírovať zo zdrojovej cenovej ponuky. | Ak je vybraná možnosť **Áno**, cenník projektu a referencie cenníka produktu sa skopírujú zo zdrojovej cenovej ponuky do cieľovej cenovej ponuky. Ak je vybraná možnosť **Nie**, cenníky sa predvolene nastavujú na základe najnovších cenníkov, ktoré boli nastavené v parametroch účtu alebo projektu. |

Keď vyberiete **OK** na dialógovej stránke, systém vytvorí kópiu ponuky projektu na základe parametrov vybratých v dialógovom okne. Otvorí sa nová ponuka projektu. 

> [!NOTE]
> Nasledujúce informácie sa nekopírujú zo zdrojovej ponuky do cieľovej ponuky:
>
> - Plány faktúry
> - Zákazníci v cenovej ponuke a v riadkoch cenovej ponuky
> - Odkaz na projekt v riadkoch založených na cenovej ponuke založených na projekte – Informácie o rozpočte zákazníka
>
>Pretože sú tieto informácie veľmi špecifické pre každú cenovú ponuku, tieto polia a záznamy sa nekopírujú. Skopírujú sa riadky cenovej ponuky pre projekty a produkty, odhady podrobností ponuky a hodnoty neprekročenia na úrovni ponuky. Predvolené ceny a sadzby nákladov závisia od možnosti **Kopírovať ceny** vybranej na dialógovej stránke **Kopírovať parametre**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]