---
title: Množiny schválení
description: Táto téma vysvetľuje, ako pracovať s množinami schválení, požiadavkami a podmnožinami týchto operácií.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323255"
---
# <a name="approval-sets"></a>Množiny schválení

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Množiny schválení zoskupujú žiadosti o schválenie do menších podmnožín operácií. Toto zoskupenie umožňuje spracovanie schválení v konkrétnej objednávke podľa projektu a umožňuje opakovanie a sekvenovanie. Zoskupenie žiadostí o schválenie zvyšuje spoľahlivosť a vysledovateľnosť spracovania schválenia pre veľké objemy schválení.

Množiny schválení označujú celkový stav spracovania ich súvisiacich záznamov. Keď sa záznam schválenia spracuje pomocou množiny schválení, záznam sa presunie z **Predložené** do **Schválené** a už nie je prepojený s množinou schválení. Ak záznam po odoslaní na schválenie zlyhá, zostane v stave **Odoslané** a množina schválení sa označí za neúspešnú. Množina schválení zaznamená chybové hlásenie o neúspechu.

## <a name="processing-approvals-and-approval-sets"></a>Spracúvanie schválení a množín schválení
Schválenia, ktoré sú zaradené do frontu na spracovanie, možno vidieť v zobrazení **Spracúvanie schválení**. Systém spracuje všetky položky viackrát asynchrónne vrátane opätovného pokusu o schválenie, ak predchádzajúce pokusy zlyhali.

Pole **Životnosť množiny schválení** zaznamenáva počet pokusov, ktoré zostávajú na spracovanie množiny, kým bude označená ako neúspešná.

## <a name="failed-approvals-and-approval-sets"></a>Neúspešné schválenia a množiny schválení
Zobrazenie **Neúspešné schválenia** uvádza všetky schválenia, ktoré vyžadujú zásah používateľa. Otvorte príslušné protokoly o množinách schválení, aby ste určili príčinu zlyhania.
Výberom možnosti **Skúsiť znova** zvýšite životnosť množiny schválení, presuniete množinu schválení späť do stavu **Spracováva sa** a pokúsite sa o spracovanie zostávajúcich záznamov.

## <a name="configure-approval-sets"></a>Konfigurácia množín schválení

### <a name="enable-the-approval-sets-feature"></a>Povolenie funkcie Množiny schválení
Skôr než povolíte funkciu Množiny schválení, skontrolujte, či sa v súčasnosti nespracovávajú žiadne schválenia.

- Prejdite na stránku **Parametre projektu** a vyberte možnosť **Ovládací prvok funkcie** > **Povoliť moderné schválenia**.

### <a name="turn-off-the-approval-sets-feature"></a>Vypnutie funkcie Množiny schválení
Skôr než vypnete funkciu Množiny schválení, skontrolujte, či sa v súčasnosti nespracovávajú žiadne schválenia.

- Prejdite na stránku **Parametre projektu** a vyberte možnosť **Ovládací prvok funkcie** > **Zakázať moderné schválenia**.

### <a name="configuring-the-asynchronous-threshold"></a>Konfigurácia asynchrónnej hranice 
Keď sa vytvoria množiny schválení, spracovanie sa presunie do pozadia, keď zvolený počet záznamov na schválenie prekročí stanovenú hranicu. Pomocou poľa **Asynchrónna hranica** nakonfigurujte, kedy sa má spracovanie schválenia spustiť synchrónne alebo asynchrónne. Vyberte jednu z nasledujúcich hodnôt:

  - Nula: Všetky žiadosti by sa mali spracovávať asynchrónne. 
  - Čísla väčšie ako nula: Schválenia sa spracovávajú asynchrónne iba v prípade, že zadaný počet schválení prekročí túto hodnotu.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
