---
title: Riadky príležitostí založených na projekte
description: Táto téma poskytuje informácie o práci s riadkami príležitostí založených na projekte.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7b255d607ac8180c249a9b9831db6f8d0cd3937b
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898415"
---
# <a name="project-based-opportunity-lines"></a>Riadky príležitostí založených na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Riadky príležitostí založené na projekte sú k dispozícii iba v prípade príležitostí založených na projekte. Záznamy príležitostí založených na projekte majú hodnoty poľa **Typ** nastavenú na **Založené na práci**.

Riadky príležitostí založené na projekte sú riadkové položky, ktoré sa zákazníkovi doručia pomocou projektu. Projekt však nemožno spojiť s riadkom príležitosti založenej na projekte. Projekty je možné naviazať ďalej na riadkové položky v etape **Cenová ponuka**, pretože príležitosť sa zvyčajne vyskytuje v počiatočnej etape obchodu. Rozhodnutie, koľko projektov sa použije na dodanie diela pre zákazníka, je rozhodnutím, ktoré sa urobí neskôr vo fáze predaja. Využite fázu príležitosti na identifikáciu jednotlivých komponentov dodávky pre zákazníka. Rozhodnutia týkajúce sa skutočného počtu projektov použitých na dodanie týchto komponentov je možné vytlačiť, kým nebudú známe ďalšie informácie o samotnej práci.

Nižšie sú uvedené polia na riadku príležitostí založených na projekte:

| **Pole** | **Miesto** | **Relevantnosť, účel a pokyny** | **Nadväzujúci vplyv** |
| --- | --- | --- | --- |
| Typ produktu | Karta Všeobecné (skrytá) | Toto je pole množiny možností. Ak máte nainštalované Dynamics 365 Operations, jednou z dostupných možností je **Služba založená na projekte**.  | Hodnota tohto poľa sa nastaví na **Služba založená na projekte**, keď vytvoríte riadok príležitosti založenej na projekte z mriežky riadkov na základe projektu v príležitosti. <br> Ak túto hodnotu zmeníte alebo prepíšete, vo vašich riadkových položkách založených na projekte nebude povolená funkčnosť projektu. |
| Príležitosť | Karta Všeobecné | Toto pole je iba na čítanie a odkazuje na nadradený záznam príležitosti, ku ktorému patrí táto riadková položka. | Toto pole nemá žiadny následný dopad. |
| Meno | Karta Všeobecné | Toto je upraviteľné textové pole, ktoré možno použiť na zabezpečenie krátkej identity tejto riadkovej položky | Táto hodnota sa prenesie do riadka cenovej ponuky, keď vytvoríte cenovú ponuku z tejto príležitosti |
| Rozpočet zákazníka | Karta Všeobecné | Toto editovateľné pole meny možno použiť na sledovanie sumy, ktorú je zákazník ochotný zaplatiť za túto riadkovú položku. | Táto hodnota sa prenesie do príslušného poľa pre riadok cenovej ponuky, keď vytvoríte cenovú ponuku z tejto príležitosti |
| Spôsob fakturácie | Karta Všeobecné | Toto upraviteľné pole má nasledujúce hodnoty:</br>- Čas a materiál</br>- Pevná cena | Táto hodnota sa prenesie do príslušného poľa pre riadok cenovej ponuky, keď vytvoríte cenovú ponuku z tejto príležitosti. Po vytvorení riadka cenovej ponuky je pole uzamknuté a nemožno ho zmeniť. Priraďte túto hodnotu poľa čo najpresnejšie. Ak potrebujete zmeniť hodnotu tohto poľa v riadku cenovej ponuky, riadok cenovej ponuky vymažte a znova vytvorte. |
