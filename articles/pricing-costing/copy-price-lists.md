---
title: Kopírovanie cenníkov
description: Táto téma poskytuje informácie o spôsobe kopírovania cenníkov v Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ad09bdce563a48843b3ed96e7aaabd9c0d5960336b9e1c74fddb9b61f760f4cd
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003745"
---
# <a name="copy-price-lists"></a>Kopírovanie cenníkov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V rámci Dynamics 365 Project Operations môžete vytvárať kópie cenníkov. Môžete napríklad vytvoriť cenníky pre nadchádzajúci rok pomocou cenníka z aktuálneho roka.  Prípadne môžete skopírovať cenník fakturačných sadzieb a predajných cien z cenníkov pre náklady. 

Ak chcete vytvoriť kópiu cenníka, postupujte nasledovne.

1. Otvorte cenník, z ktorého chcete vytvoriť kópiu, a vyberte možnosť **Kopírovať**.
2. Zadajte potrebné informácie na kopírovanie cenníka. V nasledujúcej tabuľke sú uvedené úvahy, na ktoré treba pamätať pri zadávaní informácií.

| Pole | Popis | Nadväzujúci vplyv |
| --- | --- | --- |
| Meno | Názov zdrojového cenníka s doplneným **-kópia**. | Cenník obsahuje túto hodnotu na všetkých stránkach so zoznamami a v rozbaľovacích možnostiach. |
| Kontext | Zadajte požadovaný kontext pre cieľový cenník. | Cenník s kontextom nastaveným na **Náklady** sa používa na vyhľadanie ceny odhadov nákladov a skutočných nákladov. Cenník s kontextom nastaveným na **Predaje** sa používa na vyhľadanie ceny odhadov predajov a skutočných predajov. Iba cenníky, ktoré majú nastavený kontext na **Predaj** môžu byť pripojené k cenníku projektu pre zákazníka, cenovej ponuke alebo zmluve. |
| Počiatočný dátum | Počiatočný dátum obdobia, v ktorom je cenník platný. | Toto pole sa spolu s **Dátum ukončenia** používa na určenie, ktorý cenník je použiteľný pre určitý odhad alebo riadok skutočnej hodnoty. |
| Konečný dátum | Konečný dátum obdobia, v ktorom je cenník platný. | Toto pole sa spolu s **Dátum začiatku** používa na určenie, ktorý cenník je použiteľný pre určitý odhad alebo riadok skutočnej hodnoty. |
| Mena | Mena zdrojového cenníka. Toto nastavenie je možné zmeniť. | Po zmene sa všetky výsledné riadky cien za prácu, náklady a položky katalógu produktov počas kopírovania prevedú na cieľovú menu cenníka. |
| Jednotka času | Mena zdrojového cenníka. Toto nastavenie je možné zmeniť. | Po zmene sa všetky výsledné riadky cien za prácu počas kopírovania prevedú na cieľovú menu cenníka. Používa sa prevod z nastavenia jednotky pre časovú jednotku zdrojového cenníka a časovú jednotku cieľového cenníka. |
| Popis | Popis zdrojového cenníka s doplneným **-kópia**. Toto je textové pole a umožňuje použiť viacriadkový popis cenníka. | Toto pole sa zobrazuje v zobrazeniach **Priradené** pre cenník v rôznych entitách, ktoré majú súvisiace cenníky. |

3. Uložte cenník. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Aktualizujte cenník použitím prirážky na všetky ceny

1. Na kartách **Rola**, **Kategória** a **Položka cenníka** cenníka môžete si vybrať **Aktualizovať ceny** a použiť prirážku pre všetky ceny vo vedľajšej mriežke. 
2. Na dialógovej stránke, ktorá sa otvorí, zadajte prirážku. Môžete zadať aj percento zápornej prirážky a znížiť ceny o určité percento. 
3. Vyberte **OK** na dialógovej stránke a potom overte, či ceny vo vedľajšej mriežke odrážajú vykonané zmeny.


[!INCLUDE[footer-include](../includes/footer-banner.md)]