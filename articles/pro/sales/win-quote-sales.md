---
title: Uzavretie cenových ponúk
description: Táto téma poskytuje informácie o uzatváraní cenovej ponuky v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084285"
---
# <a name="close-quotes"></a>Uzavretie cenových ponúk 

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Cenovú ponuku projektu je možné uzavrieť ako Získaná alebo Nevyužitá. Operácie Aktivovať a Skontrolovať nie sú v Microsoft Dynamics 365 Project Operations podporované pre cenové ponuky, takže môžete uzavrieť koncept cenovej ponuky.

## <a name="close-a-quote-as-won"></a>Uzavretie cenovej ponuky ako Získaná

Uzatvorením ponuky projektu ako Získaná uzavriete cenovú ponuku so stavom nastaveným na Uzavretá s dôvodom stavu nastaveným na Získaná. Po uzavretí budú cenové ponuky projektu iba na čítanie a vytvorí sa koncept projektovej zmluvy so všetkými informáciami o cenovej ponuke. Pretože uzavretú ponuku nie je možné znovu otvoriť, pred vykonaním zmien sa zobrazí potvrdzovacie dialógové okno a zmeny budú nezvratné.

Ak je cenová ponuka pripojená k príležitosti, akékoľvek ďalšie projektové ponuky týkajúce sa príležitosti sa automaticky uzavrú ako nezískané.

### <a name="financial-impact-of-closing-a-quote-as-won"></a>Finančný dopad uzavretia cenovej ponuky nastavenej ako Získaná

Ak na projekte boli zaznamenané nejaké skutočnosti v čase, keď je ešte pripojený ku konceptu cenovej ponuky, zaznamenajú sa iba náklady na čas alebo výdavky. Po uzavretí cenovej ponuky ako získanej bude aplikácia refaktorovať náklady obrátením starších skutočných nákladov a opätovným vytvorením nových skutočných nákladov. Aplikácia spracuje tieto skutočné náklady na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu. Ak sa skutočné náklady vzťahujú na riadok zmluvy pre čas a materiál, systém automaticky vytvorí zodpovedajúce nevyfakturované predajné skutočné hodnoty, keď je cenová ponuka uzavretá a vytvorí sa projektová zmluva. Ak sa skutočné náklady vzťahujú na riadku zmluvy s pevnou cenou, aplikácia zastaví spracovanie skutočných nákladov na základe pravidiel rozdeleného fakturovania pre zmluvných zákazníkov pre projekt.

## <a name="closing-a-quote-as-lost"></a>Uzavretie cenovej ponuky ako nevyužitej:

Uzatvorením ponuky projektu ako Nevyužitá nastavíte stav na Uzavretá s dôvodom stavu Nevyužitá. Uzavretie cenovej ponuky spôsobí, že ponuka projektu bude iba na čítanie. Keďže uzavretú cenovú ponuku nie je možné znovu otvoriť, tak pred zatvorením cenovej ponuky musíte svoje zmeny potvrdiť v dialógovom okne.

Ak je v cenovej ponuke projektu, ktorá je uzavretá ako Nezískaná, uvedený projekt na ktoromkoľvek z jeho riadkov, tento projekt bude tiež označený ako Uzavretý a všetky rezervácie zdrojov od tohto dňa budú zrušené.

> [!NOTE]
> V rámci Project Operations uzavretie ponuky ako Získaná or Nevyužitá nebude mať vplyv na tento stav príležitosti, ktorá zostane otvorená, kým sa manuálne neuzavrie.
