---
title: Konfigurácia fakturovateľných súčastí v riadku projektovej zmluvy
description: Táto téma poskytuje informácie o zahrnutých, účtovateľných a neúčtovateľných zložkách v riadkoch zmluvy.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bd419e189cd063f1cb2a1f0ecd3cd6450de0996b
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586639"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Konfigurácia fakturovateľných súčastí v riadku projektovej zmluvy

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Riadok zmluvy na základe projektu má koncept zahrnutej, účtovateľnej a neúčtovateľnej zložky.

Zahrnuté zložky sa vzťahujú na metódu fakturácie, rozdelenie zákazníkov, limit neprekročenia a nastavenia frekvencie fakturácie definované v riadku zmluvy na základe projektu.

Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú aktualizáciou poľa **Typ fakturácie**.

Účtovateľné zložky možno definovať pre roly a kategórie transakcií.

Pre riadok zmluvy projektu sa účtovateľnosť definovaná pre roly vzťahuje iba na triedu transakcie **Čas**. Ak je možnosť **Zahrnúť čas** nastavená na **Nie** v riadku zmluvy projektu, karta **Účtovateľné roly** nebude k dispozícii.

Účtovateľnosť definovaná pre kategórie transakcií pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Výdavok**. Ak je možnosť **Zahrnúť výdavky** nastavená na **Nie** v riadku zmluvy projektu, karta **Účtovateľné kategórie** nebude k dispozícii.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizácia roly, ktorá má byť účtovateľná alebo neúčtovateľná

Rola môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy založenej na projekte.

Na karte **Fakturovateľné roly** riadka zmluvy založenej na projekte, na vedľajšej mriežke **Fakturovateľné kategórie** v poli **Typ fakturácie** aktualizujte typ fakturácie pre rolu.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizácia kategórie transakcie, ktorá má byť účtovateľná alebo neúčtovateľná

Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy založenej na projekte.

Na karte **Fakturovateľné kategórie** riadka zmluvy založenej na projekte, na vedľajšej mriežke **Fakturovateľné kategórie** v poli **Typ fakturácie** aktualizujte typ fakturácie pre transakciu.

### <a name="resolve-chargeability"></a>Vyriešenie účtovateľnosti

Odhad alebo skutočná hodnota vytvorená pre čas sa bude považovať za účtovateľnú, iba ak je čas zahrnutý v riadku zmluvy, a ak je rola nakonfigurovaná ako účtovateľná v riadku zmluvy.

Odhad alebo skutočná hodnota vytvorená pre výdavok sa považuje za účtovateľnú, iba ak je výdavok zahrnutý v riadku zmluvy, a ak je sú kategória transakcie nakonfigurovaná ako účtovateľná v riadku zmluvy.

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
