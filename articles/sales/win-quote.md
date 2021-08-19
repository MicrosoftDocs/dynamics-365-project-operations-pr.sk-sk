---
title: Uzavretie cenovej ponuky
description: Táto téma poskytuje informácie o uzatváraní cenových ponúk v Project Operations.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2314444dfdbd4d1a2f38c7de55e2070011e51a86f1e074dd6667d54393c641fe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6993440"
---
# <a name="close-a-quote"></a>Uzavretie cenovej ponuky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Cenovú ponuku projektu je možné uzavrieť ako Získaná alebo Nevyužitá. Keďže funkcie Aktivovať a Upraviť pre cenové ponuky nie sú v aplikácii Microsoft Dynamics 365 Project Operations podporované, môžete koncept cenovej ponuky zatvoriť.

## <a name="close-a-quote-as-won"></a>Uzavretie cenovej ponuky ako Získaná

Uzatvorením ponuky projektu ako Získaná nastavíte stav cenovej ponuky na **Uzavretá** s dôvodom stavu **Získaná**. Po uzavretí budú cenové ponuky iba na čítanie a vytvorí sa koncept projektovej zmluvy so všetkými informáciami o cenovej ponuke. Keďže uzavretú cenovú ponuku nie je možné znovu otvoriť, pred zatvorením cenovej ponuky musíte svoje zmeny potvrdiť v dialógovom okne.

Projektová zmluva vytvorená z cenovej ponuky projektu je sprístupnená aj v module Projektové riadenie a účtovníctvo v Project Operations. Ak projektová zmluva nie je priradená k projektu na žiadnom z jej riadkov, táto projektová zmluva je sprístupnená ako neaktívna projektová zmluva a stáva sa aktívnou, akonáhle je projekt priradený k aspoň jednej z jej riadkov zmluvy.

Ak je cenová ponuka pripojená k príležitosti, akékoľvek ďalšie projektové ponuky týkajúce sa príležitosti sa automaticky uzavrú ako nezískané.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančný dopad uzavretia cenovej ponuky nastavenej ako Získaná

Ak na projekte boli zaznamenané nejaké skutočnosti v čase, keď je ešte pripojený ku konceptu cenovej ponuky, zaznamenajú sa iba náklady na čas alebo výdavky. Po uzavretí cenovej ponuky ako získanej bude aplikácia refaktorovať náklady obrátením starších skutočných nákladov a opätovným vytvorením nových skutočných nákladov. Aplikácia spracuje tieto skutočné náklady na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu. Ak sa skutočné náklady vzťahujú na riadok zmluvy pre čas a materiál, systém automaticky vytvorí zodpovedajúce nevyfakturované predajné skutočné hodnoty, keď je cenová ponuka uzavretá a vytvorí sa projektová zmluva. Ak sa skutočné náklady vzťahujú na riadku zmluvy s pevnou cenou, aplikácia zastaví spracovanie skutočných nákladov na základe pravidiel rozdeleného fakturovania pre zmluvných zákazníkov pre projekt.

Všetky prepracované skutočné hodnoty sú k dispozícii v module Projektové riadenie a účtovníctvo, aby ich mohol účtovník projektu skontrolovať, aktualizovať a zaúčtovať do hlavnej knihy. 

## <a name="close-a-quote-as-lost"></a>Uzavretie cenovej ponuky ako Nevyužitá

Uzatvorením ponuky projektu ako Nevyužitá nastavíte stav na **Uzavretá** s dôvodom stavu **Nevyužitá**. Uzavretie cenovej ponuky spôsobí, že bude iba na čítanie. Keďže uzavretú cenovú ponuku nie je možné znovu otvoriť, tak pred zatvorením cenovej ponuky musíte svoje zmeny potvrdiť v dialógovom okne.

Ak je v cenovej ponuke projektu, ktorá je uzavretá ako Nezískaná, uvedený projekt na ktoromkoľvek z jeho riadkov, tento projekt bude tiež označený ako Uzavretý a všetky rezervácie zdrojov od tohto dňa budú zrušené.

> [!NOTE]
> V rámci Project Operations uzavretie ponuky ako Získaná or Nevyužitá nebude mať vplyv na tento stav príležitosti, ktorá zostane otvorená, kým sa manuálne neuzavrie.


[!INCLUDE[footer-include](../includes/footer-banner.md)]