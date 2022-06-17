---
title: Skutočný vplyv na interakciu s pevnou cenou
description: Tento článok poskytuje informácie o vplyve na tabuľku Skutočné údaje pri rôznych udalostiach počas životného cyklu zapojenia s pevnou cenou v spoločnosti Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918147"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Skutočný vplyv na interakciu s pevnou cenou

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Nasledujúca tabuľka uvádza skutočné hodnoty rôznych typov transakcií, ktoré sa vytvárajú pri rôznych udalostiach v rámci zapojenia s pevnou cenou.

| Udalosť | Skutočné údaje nákladov | Nevyfakturované skutočné hodnoty predajov | Fakturovaný predaj | Príklad |
|---|---|---|---|---|
| Čas je vytvorený. | Nevzťahuje sa | Nevzťahuje sa | Nevzťahuje sa | <p>Bob Kozack z organizačnej jednotky Fabrikam US, ktorá má cenu 100 USD (100 USD) za hodinu, pracuje na projekte s názvom „Inštalácia ramena v Adatum“. Tento projekt je namapovaný na spôsob fakturácie s pevnou cenou na riadku zmluvy. Tu je ukážkový časový záznam od Boba Kozaka:</p><p>Bob Kozack - 8 hodín</p> |
| Čas je predložený. | Nevzťahuje sa | Nevzťahuje sa | Nevzťahuje sa | Pre časový záznam sa vytvorí riadok nákladového denníka. Predvolená nákladová sadzba sa zadá do účtovného zápisu. |
| Časový záznam sa pred schválením vyvolá. | Nevzťahuje sa | Nevzťahuje sa | Nevzťahuje sa | |
| Čas je schválený. | Vytvorí sa skutočný náklad. | Nevzťahuje sa | Nevzťahuje sa | <p>Nová skutočnosť, ktorá sa vytvorí:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800</li></ul> |
| Schválenie času je zrušené. | <p>Stav úpravy pôvodných skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvorí sa skutočná obstarávacia cena, ktorá má stav úpravy **Nenastaviteľné**.</p> | Nevzťahuje sa | Nevzťahuje sa | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul> |
| Časový záznam sa po schválení odvolá. | <p>Stav úpravy pôvodných skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvorí sa skutočná obstarávacia cena, ktorá má stav úpravy **Nenastaviteľné**.</p> | Nevzťahuje sa | Nevzťahuje sa | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul> |
| Zmluva je potvrdená. | <p>Stav úpravy starých skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvárajú sa skutočné náklady na stornovanie, ktoré majú stav úpravy **Nenastaviteľné**.</p><p>Nové skutočné náklady sa vytvárajú po prehodnotení zmluvných pravidiel.</p> | Nevzťahuje sa | Nevzťahuje sa | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí pre prehodnotený finančný dopad:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800</li></ul> |
| Vytvorí sa faktúra. | Nevzťahuje sa | Nevzťahuje sa | Nevzťahuje sa | |
| Faktúra je potvrdená míľnikom. | Nevzťahuje sa | Nevzťahuje sa | Vytvoria sa nové skutočné fakturované predaje založené na míľnikoch. | <p>Existujúce skutočné, ktoré zostávajú nezmenené:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zaznamenanie hodnôt fakturovaného predaja:</p><ul><li>**Fakturovaný predaj:** Míľnik, USD 5,000</li></ul> |
| Faktúra je opravená na pripísanie míľnika. | Nevzťahuje sa | Nevzťahuje sa | Vytvoria sa reverzne účtované skutočné tržby. | <p>Existujúce skutočné, ktoré zostávajú nezmenené:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, 800 USD</li></ul><p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Fakturovaný predaj:** Míľnik, USD 5,000, *Upravená*</li></ul><p>Nová skutočná hodnota, ktorá sa vytvorí na zvrátenie predchádzajúcich fakturovaných predajných hodnôt:</p><ul><li>**Fakturovaný predaj:** míľnik, (5 000 USD), *Nenastaviteľné*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
