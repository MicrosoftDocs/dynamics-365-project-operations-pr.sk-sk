---
title: Kopírovanie projektových zmlúv – čiastočné
description: Táto téma poskytuje informácie o kopírovaní projektových zmlúv v Project Operations.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5c45c6f1631d9e20bd0416410c7fe24a11623da425c8e2a633b085fbfabdd79
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006040"
---
# <a name="copy-project-contracts---lite"></a>Kopírovanie projektových zmlúv – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Nové projektové zmluvy môžete vytvoriť ľahko vytvorením kópií existujúcich zmlúv jedným z dvoch spôsobov: 

  - Na stránke zoznamu **Projektové zmluvy** vyberte projektovú zmluvu a potom vyberte položku **Kopírovať**.
  - Na stránke s podrobnosťami **Projektová zmluva** vyberte **Kopírovať**.

Otvorí sa dialógové okno, kde môžete zvoliť parametre kopírovanej zmluvy. V dialógovom okne sa nachádzajú nasledujúce polia. V závislosti od hodnôt, ktoré ste vybrali v tomto dialógovom okne sa môže proces kopírovania zmeniť.

| **Pole** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- |
| Predmet | Zadajte tému cieľovej zmluvy. Keď sa otvorí stránka dialógového okna, systém nastaví toto pole na názov zdrojovej zmluvy s doplnkom **kópia**. | Toto pole nemá žiadny následný dopad. |
| Zákazník | Odkaz na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu. Po otvorení dialógového okna systém nastaví toto pole na účet uvedený v zdrojovej zmluve. | Toto pole je primárnym zákazníkom v zmluve. |
| Zmluvná jednotka | Organizačná jednotka, ktorá je zodpovedná za realizáciu projektov spojených s týmto obchodom. Po otvorení stránky dialógového okna ho systém nastaví na zmluvnú jednotku zdrojovej zmluvy. | Zmluvnou jednotkou je divízia spoločnosti, ktorá bude po uzatvorení obchodu realizovať projekty. Každá zmluvná jednotka má menu. Táto mena sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas projektu. |
| Mena | Mena, v ktorej sa obchoduje transakcia. Po otvorení stránky dialógového okna systém nastaví toto pole na menu zdrojovej zmluvy. Mena sa môže zmeniť. V takom prípade je pole **Kopírovať ceny** vždy nastavené na **Nie**, pretože cenníky na zdrojovej zmluve už nie sú relevantné. | Mena sa používa pre predvolené cenníky, na zostavenie finančných odhadov zmluvy a na fakturáciu zákazníkovi, keď dôjde k získaniu obchodu. |
| Požadovaný dátum doručenia | Dodací termín požadovaný zákazníkom. | Dátum sa používa ako konečný dátum pri vytváraní fakturačných dátumov podľa konkrétnej frekvencie. |
| Kopírovať cenu | Označuje, či sa má cena v zmluve kopírovať zo zdrojovej zmluvy. | Ak je pole nastavené na **Áno**, cenník projektu a referencie cenníka produktu sa skopírujú zo zdrojovej do cieľovej zmluvy. Ak je vybraná možnosť **Nie**, cenníky sa predvolene nastavujú na základe najnovších cenníkov v parametroch účtu alebo projektu. |

Keď stránke dialógového okna vyberiete **OK**, systém vytvorí kópiu zmluvy na základe vybratých parametrov. Otvorí sa nová zmluva.

Nasledujúce informácie sa nekopírujú zo **zdrojovej** do **cieľovej zmluvy**:

  - Plány faktúry
  - Zákazníci v zmluve a v riadku zmluvy
  - Odkaz na projekt v riadkoch zmlúv založených na projekte
  - Informácie o rozpočte zákazníka

Pretože sú tieto informácie veľmi špecifické pre každú zmluvy, tieto polia a záznamy sa nekopírujú. Skopírujú sa riadky zmluvy pre projekty a produkty, odhady podrobností v riadku zmluvy a hodnoty na úrovni zmluvy, ktoré sa nemajú prekročiť. Predvolené ceny a sadzby nákladov závisia od výberu v poli **Kopírovať ceny** na stránke dialógového okna **Kopírovať parametre**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]