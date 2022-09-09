---
title: Skopírujte zmluvy založené na projekte
description: Tento článok poskytuje informácie o kopírovaní projektových zmlúv v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 21994ef6d8f6e6cdf321599d107cc80368c96ecc
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410387"
---
# <a name="copy-project-based-contracts"></a>Skopírujte zmluvy založené na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Nové projektové zmluvy môžete jednoducho vytvoriť skopírovaním existujúcich zmlúv jedným z dvoch spôsobov:

- Na **Projektové zmluvy** stránku so zoznamom, vyberte zmluvu o projekte a potom vyberte **Kopírovať**.
- Na stránke s podrobnosťami **Projektová zmluva** vyberte **Kopírovať**.

V oboch prípadoch sa zobrazí dialógové okno, kde môžete nastaviť parametre kopírovanej zmluvy. Dialógové okno obsahuje nasledujúce polia. V závislosti od hodnôt, ktoré vyberiete, sa proces kopírovania môže zmeniť.

| Pole | Description | Nadväzujúci vplyv |
| --- | --- | --- |
| Téma | Zadajte tému cieľovej zmluvy. Po otvorení dialógového okna systém nastaví pole na názov zdrojovej zmluvy, ale pripojí sa k nemu slovo „kopírovať“. | Toto pole nemá žiadny následný dopad. |
| zákazník | Referencia na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. Po otvorení dialógového okna systém nastaví pole na účet v zdrojovej zmluve. | Toto pole je primárnym zákazníkom v zmluve. |
| Vlastniaca spoločnosť | Spoločnosť, ktorá je zodpovedná za dodávku projektov spojených s touto transakciou. Po otvorení dialógového okna systém nastaví pole na spoločnosť, ktorá vlastní zdrojovú zmluvu. | Vlastníkom je právnická osoba, ktorá bude realizovať projekt po uzavretí obchodu. Mena vlastnej spoločnosti sa musí zhodovať s menou zmluvnej jednotky. |
| Zmluvná jednotka | Organizačná jednotka, ktorá je zodpovedná za dodanie projektov, ktoré sú spojené s touto dohodou. Po otvorení dialógového okna systém nastaví pole na zmluvnú jednotku zdroja zmluvy. | Zmluvnou jednotkou je divízia spoločnosti, ktorá bude po uzatvorení obchodu realizovať projekty. Každá zmluvná jednotka má menu. Táto mena sa používa na vykazovanie odhadovaných a skutočných nákladov, ktoré vzniknú počas projektu. |
| Mena | Mena, v ktorej sa obchoduje transakcia. Po otvorení dialógového okna systém nastaví pole na menu zdroja kontraktu. Mena sa môže zmeniť. Ak je, **Kopírovať ceny** pole je vždy nastavené na **Nie**, pretože cenníky na zmluve o zdroji už nie sú relevantné. | Táto mena sa používa pre predvolené cenníky, na generovanie finančných odhadov na zmluve a na fakturáciu zákazníkovi v prípade získania obchodu. |
| Požadovaný dátum doručenia | Zákazníkom požadovaný termín dodania. | Tento dátum sa používa ako dátum ukončenia, keď vytvárate dátumy fakturácie s určitou frekvenciou. |
| Kopírovať cenu | Hodnota, ktorá označuje, či sa má cena na zmluve skopírovať zo zdrojovej zmluvy. | Ak je pole nastavené na **Áno**, referencie na projekt a cenník produktov sa skopírujú zo zdrojovej zmluvy do cieľovej zmluvy. Ak je nastavená na **Nie**, používajú sa predvolené cenníky na základe najnovších cenníkov v parametroch účtu alebo projektu. |

Keď vyberiete **OK** v dialógovom okne systém vytvorí kópiu zmluvy na základe hodnôt parametrov, ktoré nastavíte. Potom sa otvorí nová zmluva.

Nasledujúce informácie sú **nie** skopírované zo zdrojovej zmluvy do cieľovej zmluvy, pretože je špecifická pre každú zmluvu:

- Plány faktúry
- Zákazníci v zmluve a v riadku zmluvy
- Odkaz na projekt v riadkoch zmlúv založených na projekte
- Informácie o rozpočte zákazníka

Skopírujú sa zmluvné riadky pre projekty a produkty, odhady v detailoch zmluvných riadkov a neprekročené hodnoty na zmluvnej úrovni. Zadanie predvolených cien a nákladových sadzieb závisí od výberu v **Kopírovať ceny** poli v **Kopírovať parametre** dialógové okno.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
