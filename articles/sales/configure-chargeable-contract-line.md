---
title: Konfigurácia účtovateľných zložiek riadka zmluvy na základe projektu
description: Táto téma poskytuje informácie o zahrnutých, účtovateľných a neúčtovateľných zložkách v riadkoch zmluvy.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084301"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Konfigurácia účtovateľných zložiek riadka zmluvy na základe projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Riadok zmluvy na základe projektu má koncept zahrnutej, účtovateľnej a neúčtovateľnej zložky.

Zahrnuté zložky sa vzťahujú na metódu fakturácie, rozdelenie zákazníkov, limit neprekročenia a nastavenia frekvencie fakturácie definované v riadku zmluvy na základe projektu.

Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú aktualizáciou poľa **Typ fakturácie**.

Účtovateľné zložky možno definovať pre roly a kategórie transakcií.

Pre riadok zmluvy projektu sa účtovateľnosť definovaná pre roly vzťahuje iba na triedu transakcie **Čas**. Ak je možnosť **Zahrnúť čas** nastavená na **Nie** v riadku zmluvy projektu, karta **Účtovateľné roly** nebude k dispozícii.

Účtovateľnosť definovaná pre kategórie transakcií pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Výdavok**. Ak je možnosť **Zahrnúť výdavky** nastavená na **Nie** v riadku zmluvy projektu, karta **Účtovateľné kategórie** nebude k dispozícii.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizácia roly, ktorá má byť účtovateľná alebo neúčtovateľná

Rola môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy založenej na projekte.

Na karte **Účtovateľné roly** pre riadok zmluvy založenej na projekte, na vedľajšej mriežke **Účtovateľné kategórie** v poli **Typ fakturácie** , aktualizujte typ fakturácie pre rolu.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizácia kategórie transakcie, ktorá má byť účtovateľná alebo neúčtovateľná

Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy založenej na projekte.

Na karte **Účtovateľné kategórie** pre riadok zmluvy založenej na projekte, na vedľajšej mriežke **Účtovateľné kategórie** v poli **Typ fakturácie** , aktualizujte typ fakturácie pre transakciu.

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
