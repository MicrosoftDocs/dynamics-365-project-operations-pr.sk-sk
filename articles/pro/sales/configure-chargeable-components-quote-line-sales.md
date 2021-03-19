---
title: Konfigurácia fakturovateľných súčastí riadka cenovej ponuky – čiastočné
description: Táto téma poskytuje informácie o nastavení účtovateľných a neúčtovateľných zložiek v riadku cenovej ponuky založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e293587adf15d0523bef6b7e688fdc883aba0fa
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273892"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Konfigurácia fakturovateľných súčastí riadka cenovej ponuky – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Riadok cenovej ponuky na základe projektu má koncept *zahrnutej* zložky a *účtovateľnej* zložky.

Zahrnuté komponenty sa vzťahujú na:

  - Spôsob fakturácie a rozdelenie zákazníkov
  - Limity, ktoré sa nesmú prekročiť 
  - Nastavenia frekvencie faktúr definované v riadku cenovej ponuky na základe projektu

Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú pomocou poľa **Typ fakturácie**. Pole **Typ fakturácie** je súpravou volieb, ktoré môžu obsahovať nasledujúce hodnoty v kontexte riadka cenovej ponuky:

  - Účtovateľné
  - Neúčtovateľné

Účtovateľné zložky možno definovať pre úlohy, roly a kategórie transakcií.

Účtovateľnosť je definovaná na úlohách pre riadok cenovej ponuky a vzťahuje sa na všetky triedy transakcií zahrnuté v tomto riadku. Ak je pole **Zahrnúť úlohy** nastavené na **Celý projekt** alebo je ponechané prázdne, karta **Účtovateľné úlohy** nebude k dispozícii.

Účtovateľnosť je definovaná pre riadok cenovej ponuky a vzťahuje sa iba na triedu transakcie **Čas**. Ak je pole **Zahrnúť čas** nastavené na **Nie** v riadku cenovej ponuky projektu, karta **Účtovateľné roly** nebude k dispozícii.

Účtovateľnosť je definovaná pre kategórie transakcií pre riadok cenovej ponuky sa vzťahuje iba na triedu transakcie **Výdavok**. Ak je pole **Zahrnúť výdavky** nastavené na **Nie** v riadku cenovej ponuky projektu, karta **Účtovateľné kategórie** nebude k dispozícii.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Aktualizácia úlohy projektu, ktorá má byť účtovateľná alebo neúčtovateľná

Projektová úloha môže byť účtovateľná alebo neúčtovateľná v kontexte špecifického riadku cenovej ponuky na základe projektu, čo umožňuje nasledujúce nastavenie:

Ak riadok cenovej ponuky založený na projekte obsahuje **Čas** a úlohu **T1**, úloha je priradená k riadku cenovej ponuky ako účtovateľná. Ak existuje druhý riadok cenovej ponuky, ktorý obsahuje **Výdavky**, môžete úlohu **T1** v riadku cenovej ponuky priradiť ako neúčtovateľnú. Výsledkom je, že všetok čas zaznamenaný pri úlohe je účtovateľný a všetky výdavky zaznamenané pre úlohu nie sú neúčtovateľné.

Typ fakturácie úlohy je možné nakonfigurovať na karte **Fakturovateľné úlohy** riadku cenovej ponuky založenej na projekte aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Úlohy riadkov cenovej ponuky**. Prípadne môžete aktualizovať typ fakturácie pre projektovú úlohu v poli **Typ fakturácie** vo vedľajšej mriežke v nastavení fakturácie úloh projektu, ktoré zobrazuje riadky cenovej ponuky spojené s úlohou.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Aktualizácia roly, ktorá má byť účtovateľná alebo neúčtovateľná

Rola môže byť účtovateľná alebo neúčtovateľná v kontexte konkrétneho riadka cenovej ponuky založenej na projekte.

Typ fakturácie roly je možné nakonfigurovať na karte **Fakturovateľné roly** riadku cenovej ponuky aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné roly**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Aktualizácia kategórie transakcie, ktorá má byť účtovateľná alebo neúčtovateľná

Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku cenovej ponuky.

Typ fakturácie transakcie je možné nakonfigurovať na karte **Fakturovateľné kategórie** riadku cenovej ponuky aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné kategórie**.

### <a name="resolve-chargeability"></a>Vyriešenie účtovateľnosti
Odhad alebo skutočná hodnota vytvorená pre čas sa bude považovať za účtovateľnú, iba ak je **Čas** zahrnutý v riadku cenovej ponuky, a ak sú kategórie **Úloha** a **Rola** nakonfigurované ako účtovateľné v riadku cenovej ponuky.

Odhad alebo skutočná hodnota vytvorená pre výdavok sa bude považovať za účtovateľnú, iba ak je **Výdavok** zahrnutý v riadku cenovej ponuky, a ak sú kategórie **Úloha** a **Transakcia** nakonfigurované ako účtovateľné v riadku cenovej ponuky.

| Zahrnie čas | Zahrnie výdavok | Zahrnuté úlohy | Rola | Kategória | Úloha | Fakturácia |
| --- | --- | --- | --- | --- | --- | --- |
| Áno | Áno | Celý projekt | Účtovateľné | Účtovateľné | Nie je možné nastaviť | Fakturácia skutočnej hodnoty času: Účtovateľné </br>Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné |
| Áno | Áno | Iba vybraté úlohy | Účtovateľné | Účtovateľné | Účtovateľné | Fakturácia skutočnej hodnoty času: Účtovateľné</br>Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné |
| Áno | Áno | Iba vybraté úlohy | Neúčtovateľné | Účtovateľné | Účtovateľné | Fakturácia skutočnej hodnoty času: Neúčtovateľné</br>Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné |
| Áno | Áno | Iba vybraté úlohy | Účtovateľné | Účtovateľné | Neúčtovateľné | Fakturácia skutočnej hodnoty času: Neúčtovateľné</br> Typ fakturácie skutočnej hodnoty výdavku: Neúčtovateľné |
| Áno | Áno | Iba vybraté úlohy | Neúčtovateľné | Účtovateľné | Neúčtovateľné | Fakturácia skutočnej hodnoty času: Neúčtovateľné</br> Typ fakturácie skutočnej hodnoty výdavku: Neúčtovateľné |
| Áno | Áno | Iba vybraté úlohy | Neúčtovateľné | Neúčtovateľné | Účtovateľné | Fakturácia skutočnej hodnoty času: Neúčtovateľné</br> Typ fakturácie skutočnej hodnoty výdavku: Neúčtovateľné |
| No | Áno | Celý projekt | Nie je možné nastaviť | Účtovateľné | Nie je možné nastaviť | Fakturácia skutočnej hodnoty času: Nedostupné </br>Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné |
| No | Áno | Celý projekt | Nie je možné nastaviť | Neúčtovateľné | Nie je možné nastaviť | Fakturácia skutočnej hodnoty času: Nedostupné </br>Typ fakturácie skutočnej hodnoty výdavku: Neúčtovateľné |
| Áno | No | Celý projekt | Účtovateľné | Nie je možné nastaviť | Nie je možné nastaviť | Fakturácia skutočnej hodnoty času: Účtovateľné</br>Typ fakturácie skutočnej hodnoty výdavku: Nedostupné |
| Áno | No | Celý projekt | Neúčtovateľné | Nie je možné nastaviť | Nie je možné nastaviť | Fakturácia skutočnej hodnoty času: Neúčtovateľné </br>Typ fakturácie skutočnej hodnoty výdavku: Nedostupné |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]