---
title: Množiny schválení
description: Táto téma poskytuje informácie o množine schválení, žiadostiach a podmnožinách týchto operácií.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116890"
---
# <a name="approval-sets"></a>Množiny schválení

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Množiny schválení zoskupujú žiadosti o schválenie do menších podmnožín operácií. Toto zoskupenie umožňuje, aby projekt spracovával schválenia v správnom poradí, a umožňuje ich opakovanie a radenie. Zoskupenie zvyšuje spoľahlivosť a sledovateľnosť spracovania schválení pri veľkom objeme schválení.

Množiny schválení označujú celkový stav spracovania ich súvisiacich záznamov. Keď sa záznam o schválení spracuje pomocou množiny schválení, presunie sa zo stavu **Odoslané** do stavu **Schválené** a odpojí sa z množiny schválení. Ak záznam po odoslaní na schválenie zlyhá, zostane v stave **Odoslané** a množina schválení sa označí za neúspešnú. Množina schválení zaznamená chybové hlásenie o neúspechu.

## <a name="processing-approvals-and-approval-sets"></a>Spracúvanie schválení a množín schválení
Schválenia, ktoré sú zaradené do frontu na spracovanie, možno vidieť v zobrazení **Spracúvanie schválení**. Systém sa pokúsi niekoľkokrát asynchrónne spracovať všetky záznamy vrátane opakovaného pokusu o schválenie, ak predchádzajúce pokusy zlyhali.

Pole **Životnosť množiny schválení** zaznamenáva počet pokusov, ktoré zostávajú na spracovanie množiny, kým bude označená ako neúspešná.

## <a name="failed-approvals-and-approval-sets"></a>Neúspešné schválenia a množiny schválení
Zobrazenie **Neúspešné schválenia** obsahuje zoznam všetkých schválení, ktoré si vyžadujú zásah používateľa. Otvorte príslušné protokoly o množinách schválení, aby ste určili príčinu zlyhania.
Výberom možnosti **Skúsiť znova** zvýšite životnosť množiny schválení, presuniete množinu schválení späť do stavu **Spracováva sa** a pokúsite sa o spracovanie zostávajúcich záznamov.

## <a name="configure-approval-sets"></a>Konfigurácia množín schválení

###  <a name="enable-the-approval-sets-feature"></a>Povolenie funkcie Množiny schválení
Skôr než povolíte funkciu Množiny schválení, skontrolujte, či sa v súčasnosti nespracovávajú žiadne schválenia.

- Prejdite na stránku **Parametre projektu** a vyberte možnosť **Ovládací prvok funkcie** > **Povoliť moderné schválenia**.

### <a name="turn-off-the-approval-sets-feature"></a>Vypnutie funkcie Množiny schválení
Skôr než vypnete funkciu Množiny schválení, skontrolujte, či sa v súčasnosti nespracovávajú žiadne schválenia.

- Prejdite na stránku **Parametre projektu** a vyberte možnosť **Ovládací prvok funkcie** > **Zakázať moderné schválenia**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurácia asynchrónnej hranice 
Keď sa vytvoria množiny schválení, spracovanie sa presunie do pozadia, keď zvolený počet záznamov na schválenie prekročí stanovenú hranicu. Pomocou poľa **Asynchrónna hranica** nakonfigurujte, kedy sa má spracovanie schválenia spustiť synchrónne alebo asynchrónne.
Platné hodnoty sú:

  - Nula: Všetky žiadosti by sa mali spracovávať asynchrónne. 
  - Čísla väčšie ako nula: Schválenia sa spracovávajú asynchrónne iba v prípade, že zadaný počet schválení prekročí túto hodnotu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
