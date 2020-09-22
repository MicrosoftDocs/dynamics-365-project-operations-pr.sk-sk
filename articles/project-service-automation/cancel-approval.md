---
title: Zrušenie predtým schváleného času a položiek výdavkov
description: Táto téma poskytuje informácie o zrušení schváleného času projektu a nákladov transakcie.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755500"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Zrušenie predtým schváleného času a položiek výdavkov

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V najnovšej verzii Dynamics 365 Project Service Automation môžu schvaľovatelia zrušiť položky času alebo výdavkov, ktoré predtým schválili.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Zrušenie predtým schváleného času a výdavkových položiek

Ak chcete zrušiť položku času alebo výdavkov, ktoré ste predtým schválili, postupujte podľa týchto krokov.

1. Prejdite na **projekty** \> **moja práca** \> **schválenia**.
2. Na stránke zoznam **schválení** zmeňte zobrazenie na **moje predchádzajúce schválenia**. Zobrazí sa zoznam položiek času a výdavkov, ktoré ste predtým schválili.
3. Vyberte jednu alebo viac položiek a potom vyberte položku **zrušiť schválenie**. Zobrazí sa upozorňujúce hlásenie.
4. Ak chcete zrušiť schválenie, stlačte tlačidlo **OK**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Pochopte vplyv zrušenia schválenia času alebo výdavkov

Ak sa schválenie zruší, existuje prevádzkový dopad aj finančný dopad.

### <a name="operational-impact"></a>Prevádzkový dopad

Na strane operácie pri zrušení schválenia sa stav záznamu obnoví na **draft**a schválenie sa už nezobrazí v zobrazení **moje minulé schválenia**. Namiesto zrušených schválení sa zobrazí **Časové položky na schválenie** alebo **výdavkové položky na schválenie**, v závislosti od toho, či to bola časová položka alebo výdavková položka. Okrem toho stav súvisiacich časových alebo výdavkových položiek sa zmení na **odoslané**, takže súvisiaca položka je v súlade so schváleniami, ktoré majú štatút **Draftu**.

Ako schvaľovateľ môžete upraviť niektoré polia schválenia, ktoré majú stav **Draftu**. Tieto polia zahŕňajú **typ fakturácie** a **Fakturovateľné hodiny pre položky času**. Po zmene môžete záznam znova schváliť. Prípadne môžete položku zamietnuť. Ak odmietnete schválenie časovej položky, stav položky sa zmení na **vrátený**. Ak odmietnete schválenie výdavkovej položky, stav položky sa zmení na **zamietnutý**. Funkčne, sa vrátené a odmietnuté položky správajú rovnako ako položka, ktorá má stav **Draftu**. Člen projektového tímu môže buď vykonať požadované zmeny v položke a potom ho znova odoslať na schválenie, alebo úplne odstrániť položku.

### <a name="financial-impact"></a>Finančný vplyv

Projekt je tiež ovplyvnený finančne, ak je schválenie zrušené. Po prvé, zodpovedajúce skutočné hodnoty nákladov a predaja sa aktualizujú nasledujúcim spôsobom:

- Stav úpravy je nastavený na **upravené**.
- Stav fakturácie je nastavený na **zrušené**.

Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje. Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt. Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva. Tieto hodnoty sa namiesto toho obrátili. Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**. Pole **Stav nastavenia** v obrátenom stave je nastavené na **nenastaviteľné**a stav fakturácie je nastavený na **zrušené**.

Po týchto zmenách, množstvo, ktoré je zaznamenané ako vynaložené na projekt a nevybavené príjmy projektu predĺžia obchodný vzťah pre hodnoty, ktoré tieto skutočné údaje predstavujú.
