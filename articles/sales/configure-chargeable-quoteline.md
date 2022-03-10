---
title: Konfigurácia fakturovateľných súčastí riadka projektovej cenovej ponuky
description: Táto téma poskytuje informácie o zahrnutých, fakturovateľných a nefakturovateľných komponentoch v riadkoch projektovej cenovej ponuky.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 251d0013b445d2f7d17fbe1908f0db2e05cfc2670ac667deb363c98f608a2aef
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004015"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Konfigurácia fakturovateľných súčastí riadka projektovej cenovej ponuky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Riadok projektovej cenovej ponuky môže obsahovať komponenty a fakturovateľné komponenty.

Zahrnuté komponenty podliehajú metóde fakturácie, rozdeleniu zákazníkov, limitom, ktoré sa nesmú prekročiť a nastaveniam frekvencie fakturácie definovaným v riadku projektovej cenovej ponuky.
Podskupinu zahrnutých komponentov možno označiť ako fakturovateľnú použitím položky **Typ fakturácie**. V poli **Typ fakturácie** môžete zvoliť jednu z nasledujúcich možností v kontexte riadka cenovej ponuky:

   - Účtovateľné
   - Neúčtovateľné

Fakturovateľné komponenty možno definovať pre roly a kategórie transakcií.

Fakturovateľnosť, ktorá je definovaná pre roly pre riadok projektovej cenovej ponuky, sa vzťahuje iba na triedu transakcie **Čas**. Ak má riadok projektovej cenovej ponuky nastavené **Zahrnúť čas** = **Nie**, karta **Fakturovateľné roly** nie je k dispozícii.

Fakturovateľnosť, ktorá je definovaná pre kategórie transakcií pre riadok projektovej cenovej ponuky, sa vzťahuje iba na triedu transakcie **Výdavok**. Ak má riadok projektovej cenovej ponuky nastavené **Zahrnúť výdavky** = **Nie**, karta **Fakturovateľné kategórie** nie je k dispozícii.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizácia roly, ktorá má byť účtovateľná alebo neúčtovateľná
Rola môže byť fakturovateľná alebo nefakturovateľná na riadku projektovej cenovej ponuky. Typ fakturácie pre rolu je možné nakonfigurovať na karte **Fakturovateľné roly** riadka projektovej cenovej ponuky. Ak to chcete urobiť, aktualizujte **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné roly**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizácia kategórie transakcie, ktorá má byť účtovateľná alebo neúčtovateľná
Kategória transakcie môže byť fakturovateľná alebo nefakturovateľná na riadku projektovej cenovej ponuky. Typ fakturácie pre transakciu je možné nakonfigurovať na karte **Fakturovateľné kategórie** riadka projektovej cenovej ponuky. Ak to chcete urobiť, aktualizujte pole **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné kategórie**. 

## <a name="resolve-chargeability"></a>Vyriešenie účtovateľnosti

Odhad alebo skutočná hodnota vytvorená pre čas sa bude považovať za fakturovateľnú, iba ak je čas uvedený v riadku cenovej ponuky a ak je rola nakonfigurovaná ako fakturovateľná.
Odhad alebo skutočná hodnota vytvorená pre výdavok sa bude považovať za fakturovateľnú, iba ak je výdavok uvedený v riadku cenovej ponuky a ak je kategória transakcie nakonfigurovaná ako fakturovateľná v riadku cenovej ponuky. Nasledujúca tabuľka ukazuje, aká je predvolená hodnota fakturovateľnosti pri každej skutočnej hodnote. Predvolené hodnoty sú založené na zahrnutých komponentoch a type fakturácie nastavenom na riadku cenovej ponuky.

| Zahrnie čas | Zahrnie výdavok | Rola | Kategória | Úloha |
| --- | --- | --- | --- | --- |
| Áno | Áno | Účtovateľné | Účtovateľné | Fakturácia skutočnej hodnoty času: Účtovateľné </br>Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné |
| Áno | Áno | Neúčtovateľné | Účtovateľné | Fakturácia skutočnej hodnoty času: Neúčtovateľné </br>Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné |
| Áno | Áno | Neúčtovateľné | Neúčtovateľné | Fakturácia skutočnej hodnoty času: Neúčtovateľné </br>Typ fakturácie skutočnej hodnoty výdavku: Neúčtovateľné |
| No | Áno | Nie je možné nastaviť | Účtovateľné | Fakturácia skutočnej hodnoty času: Nedostupné </br>Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné |
| No | Áno | Nie je možné nastaviť | Neúčtovateľné | Fakturácia skutočnej hodnoty času: Nedostupné </br>Typ fakturácie skutočnej hodnoty výdavku: Neúčtovateľné |
| Áno | No | Účtovateľné | Nie je možné nastaviť | Fakturácia skutočnej hodnoty času: Účtovateľné </br>Typ fakturácie skutočnej hodnoty výdavku: Nedostupné |
| Áno | No | Neúčtovateľné | Nie je možné nastaviť | Fakturácia skutočnej hodnoty času: Neúčtovateľné </br> Typ fakturácie skutočnej hodnoty výdavku: Nedostupné |


[!INCLUDE[footer-include](../includes/footer-banner.md)]