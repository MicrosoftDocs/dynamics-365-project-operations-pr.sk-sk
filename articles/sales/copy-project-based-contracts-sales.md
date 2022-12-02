---
title: Kopírovanie zmlúv založených na projekte
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
# <a name="copy-project-based-contracts"></a>Kopírovanie zmlúv založených na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Nové projektové zmluvy môžete vytvoriť ľahko skopírovaním existujúcich zmlúv jedným z dvoch spôsobov:

- Na stránke zoznamu **Projektové zmluvy** vyberte projektovú zmluvu a potom vyberte položku **Kopírovať**.
- Na stránke s podrobnosťami **Projektová zmluva** vyberte **Kopírovať**.

V oboch prípadoch sa otvorí sa dialógové okno, kde môžete nastaviť parametre kopírovanej zmluvy. V dialógovom okne sa nachádzajú nasledujúce polia. V závislosti od zvolených hodnôt sa môže proces kopírovania zmeniť.

| Pole | Description | Nadväzujúci vplyv |
| --- | --- | --- |
| Téma | Zadajte tému cieľovej zmluvy. Keď sa otvorí dialógové okno, systém nastaví pole na názov zdrojovej zmluvy, ale doplní slovo „kópia“. | Toto pole nemá žiadny následný dopad. |
| zákazník | Referencia na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. Po otvorení dialógového okna systém nastaví toto pole na obchodný vzťah uvedený v zdrojovej zmluve. | Toto pole je primárnym zákazníkom v zmluve. |
| Vlastniaca spoločnosť | Spoločnosť, ktorá je zodpovedná za realizáciu projektov spojených s týmto obchodom. Po otvorení dialógového okna systém nastaví toto pole na vlastnícku spoločnosť zdrojovej zmluvy. | Vlastníckou spoločnosťou je právnická osoba, ktorá bude realizovať projekt po uzavretí obchodu. Mena vlastníckej spoločnosti sa musí zhodovať s menou zmluvnej jednotky. |
| Zmluvná jednotka | Organizačná jednotka, ktorá je zodpovedná za realizáciu projektov spojených s týmto obchodom. Po otvorení dialógového okna systém nastaví toto pole na zmluvnú jednotku zdrojovej zmluvy. | Zmluvnou jednotkou je divízia spoločnosti, ktorá bude po uzatvorení obchodu realizovať projekty. Každá zmluvná jednotka má menu. Táto mena sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas projektu. |
| Mena | Mena, v ktorej sa obchoduje transakcia. Po otvorení dialógového okna systém nastaví toto pole na menu zdrojovej zmluvy. Mena sa môže zmeniť. V takom prípade je pole **Kopírovať ceny** vždy nastavené na **Nie**, pretože cenníky na zdrojovej zmluve už nie sú relevantné. | Táto mena sa používa pre predvolené cenníky, na generovanie finančných odhadov zmluvy a na fakturáciu zákazníkovi, keď dôjde k získaniu obchodu. |
| Požadovaný dátum doručenia | Dodací termín požadovaný zákazníkom. | Dátum sa používa ako konečný dátum pri vytváraní fakturačných dátumov podľa konkrétnej frekvencie. |
| Kopírovať cenu | Hodnota, ktorá označuje, či sa má cena v zmluve kopírovať zo zdrojovej zmluvy. | Ak je pole nastavené na **Áno**, cenník projektu a referencie cenníka produktu sa skopírujú zo zdrojovej zmluvy do cieľovej zmluvy. Ak nastavené na **Nie**, použijú sa predvolené cenníky na základe najnovších cenníkov v parametroch účtu alebo projektu. |

Keď na stránke dialógového okna vyberiete **OK**, systém vytvorí kópiu zmluvy na základe hodnôt parametrov, ktoré ste nastavili. Potom sa otvorí nová zmluva.

Nasledujúca informácia sa **neskopíruje** zo zdrojovej zmluvy do cieľovej zmluvy, pretože je špecifická pre každú zmluvu:

- Plány faktúry
- Zákazníci v zmluve a v riadku zmluvy
- Odkaz na projekt v riadkoch zmlúv založených na projekte
- Informácie o rozpočte zákazníka

Skopírujú sa riadky zmluvy pre projekty a produkty, odhady v podrobnostiach riadku zmluvy a hodnoty na úrovni zmluvy, ktoré sa nemajú prekročiť. Zadanie predvolených cien a nákladových sadzieb závisí od výberu v poli **Kopírovať ceny** v dialógovom okne **Kopírovať parametre**.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
