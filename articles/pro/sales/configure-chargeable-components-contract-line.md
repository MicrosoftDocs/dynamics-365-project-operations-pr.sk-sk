---
title: Konfigurácia fakturovateľných súčastí riadka zmluvy založenej na projekte – čiastočné
description: Táto téma poskytuje informácie o tom, ako pridávať účtovateľné zložky do riadkov zmluvy v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cf3f2a28fc992d6444b35d6ffa0c3f6cadcf16ea
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273937"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Konfigurácia fakturovateľných súčastí riadka zmluvy založenej na projekte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadok zmluvy na základe projektu obsahuje *zahrnuté* zložky a *účtovateľné* zložky.

Zahrnuté zložky sú zložky, ktoré sa vzťahujú na:

  - Spôsob fakturácie a rozdelenie zákazníkov
  - Limity, ktoré sa nesmú prekročiť 
  - Nastavenia frekvencie faktúr definované v riadku zmluvy na základe projektu

Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú pomocou poľa **Typ fakturácie**. Pole **Typ fakturácie** je súpravou volieb, ktoré môžu obsahovať nasledujúce hodnoty v kontexte riadka zmluvy:

  - Účtovateľné
  - Neúčtovateľné

Účtovateľné zložky možno definovať pre úlohy, roly a kategórie transakcií.

Účtovateľnosť je definovaná na úlohách pre riadok zmluvy projektu a vzťahuje sa na všetky triedy transakcií zahrnuté v riadku. Ak je pole **Zahrnúť úlohy** v riadku zmluvy prázdne alebo nastavené na **Celý projekt**, karta **Účtovateľné úlohy** nebude k dispozícii.

Účtovateľnosť definovaná pre roly pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Čas**. Ak je pole **Zahrnúť čas** v riadku zmluvy nastavené na **Nie**, karta **Účtovateľné roly** nebude k dispozícii.

Účtovateľnosť definovaná pre kategórie transakcií pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Výdavok**. Ak je pole **Zahrnúť výdavky** nastavené na **Nie**, karta **Účtovateľné kategórie** nebude k dispozícii.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Aktualizácia úlohy projektu ako účtovateľnej alebo neúčtovateľnej

Projektová úloha môže byť účtovateľná alebo neúčtovateľná v konkrétnom riadku zmluvy, čo umožňuje nasledujúce nastavenie:

Ak zahŕňa riadok zmluvy založený na projekte **Čas** a určitú úlohu, **T1** je k nej pridružená ako účtovateľná. Ak existuje druhý riadok zmluvy, ktorý obsahuje **Výdavky**, môžete úlohu T1 v riadku zmluvy priradiť ako neúčtovateľnú. Výsledkom je, že všetok čas zaznamenaný pri úlohe je účtovateľný a všetky výdavky nie sú neúčtovateľné.

Typ fakturácie úlohy je možné nakonfigurovať na karte **Fakturovateľné úlohy** riadka zmluvy aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke úlohy riadkov zmluvy. Prípadne môžete aktualizovať pole **Typ fakturácie** vo vedľajšej mriežke nastavenia fakturácie úloh projektu, ktoré zobrazuje riadky zmluvy spojené s úlohou.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Aktualizácia roly ako účtovateľnej alebo neúčtovateľnej

Rola môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy.

Typ fakturácie role je možné nakonfigurovať na karte **Účtovateľné role** v riadku zmluvy. Ak to chcete urobiť, aktualizujte pole **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné roly**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Aktualizácia kategórie transakcie ako účtovateľnej alebo neúčtovateľnej

Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy.

Typ fakturácie transakcie je možné nakonfigurovať na karte **Účtovateľné kategórie** v riadku zmluvy na základe projektu. Ak to chcete urobiť, aktualizujte pole **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné kategórie**.

### <a name="resolve-chargeability"></a>Vyriešenie účtovateľnosti

Odhad alebo skutočná hodnota vytvorená pre čas sa bude považovať za účtovateľnú, iba ak je **Čas** zahrnutý v riadku zmluvy, a ak sú kategórie **Úloha** a **Rola** nakonfigurované ako účtovateľné v riadku zmluvy.

Odhad alebo skutočná hodnota vytvorená pre výdavok sa považuje za účtovateľnú, iba ak je **Výdavok** zahrnutý v riadku zmluvy, a ak sú kategórie **Úloha** a **Transakcia** nakonfigurované ako účtovateľné v riadku zmluvy.


| Zahrnie čas | Zahrnie výdavok | Zahrnie úlohy | Rola           | Kategória       | Úloha                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Áno           | Áno              | Celý projekt | Účtovateľné     | Účtovateľné     | Fakturácia skutočnej hodnoty času: **Účtovateľné** </br> Typ fakturácie skutočnej hodnoty výdavku: **Účtovateľné**           |
| Áno           | Áno              | Vybraté úlohy | Účtovateľné     | Účtovateľné     | Fakturácia skutočnej hodnoty času: **Účtovateľné** </br> Typ fakturácie skutočnej hodnoty výdavku: **Účtovateľné**           |
| Áno           | Áno              | Vybraté úlohy | Neúčtovateľné | Účtovateľné     | Fakturácia skutočnej hodnoty času: **Neúčtovateľné** </br> Typ fakturácie skutočnej hodnoty výdavku: **Účtovateľné**       |
| Áno           | Áno              | Vybraté úlohy | Účtovateľné     | Účtovateľné     | Fakturácia skutočnej hodnoty času: **Neúčtovateľné** </br> Typ fakturácie skutočnej hodnoty výdavku:   **Neúčtovateľné** |
| Áno           | Áno              | Vybraté úlohy | Neúčtovateľné | Účtovateľné     | Fakturácia skutočnej hodnoty času: **Neúčtovateľné** </br> Typ fakturácie skutočnej hodnoty výdavku:   **Neúčtovateľné** |
| Áno           | Áno              | Vybraté úlohy | Neúčtovateľné | Neúčtovateľné | Fakturácia skutočnej hodnoty času: **Neúčtovateľné** </br> Typ fakturácie skutočnej hodnoty výdavku:   **Neúčtovateľné** |
| No            | Áno              | Celý projekt | Nie je možné nastaviť   | Účtovateľné     | Fakturácia skutočnej hodnoty času: **Nedostupné**</br>Typ fakturácie skutočnej hodnoty výdavku: **Účtovateľné**          |
| No            | Áno              | Celý projekt | Nie je možné nastaviť   | Neúčtovateľné | Fakturácia skutočnej hodnoty času: **Nedostupné**</br> Typ fakturácie skutočnej hodnoty výdavku: **Neúčtovateľné**     |
| Áno           | No               | Celý projekt | Účtovateľné     | Nie je možné nastaviť   | Fakturácia skutočnej hodnoty času: **Účtovateľné** </br> Typ fakturácie skutočnej hodnoty výdavku: **Nedostupné**        |
| Áno           | No               | Celý projekt | Neúčtovateľné | Nie je možné nastaviť   | Fakturácia skutočnej hodnoty času: **Neúčtovateľné** </br>Typ fakturácie skutočnej hodnoty výdavku: **Nedostupné**   |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]