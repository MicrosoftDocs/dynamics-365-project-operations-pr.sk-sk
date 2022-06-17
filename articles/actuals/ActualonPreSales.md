---
title: Skutočný vplyv počas predpredajnej fázy zákazky
description: Tento článok poskytuje informácie o vplyve na tabuľku Aktuálny stav pri rôznych udalostiach, kým je zákazka v štádiu predpredaja v Microsofte Dynamics 365 Project Operations.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922379"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Skutočný vplyv počas predpredajnej fázy zákazky

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Nasledujúca tabuľka uvádza skutočné údaje o rôznych typoch transakcií, ktoré sa vytvárajú pri rôznych udalostiach počas predpredajnej fázy projektového zapojenia.

| Udalosť | Skutočné údaje nákladov | Príklad |
|---|---|---|
| Čas je vytvorený. | Nevzťahuje sa | <p>Bob Kozack z organizačnej jednotky Fabrikam US, ktorá má cenu 100 USD (100 USD) za hodinu, pracuje na projekte s názvom „Inštalácia ramena v Adatum“. Tento projekt je namapovaný na spôsob fakturácie s pevnou cenou na riadku zmluvy. Tu je ukážkový časový záznam od Boba Kozaka:</p><p>Bob Kozack - 8 hodín</p> |
| Čas je predložený. | Nevzťahuje sa | Pre časový záznam sa vytvorí riadok nákladového denníka. Predvolená nákladová sadzba sa zadá do účtovného zápisu. |
| Časový záznam sa pred schválením vyvolá. | Nevzťahuje sa | |
| Čas je schválený. | Vytvorí sa skutočný náklad. | <p>Nová skutočnosť, ktorá sa vytvorí:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800</li></ul> |
| Schválenie času je zrušené. | <p>Stav úpravy pôvodných skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvorí sa skutočná obstarávacia cena, ktorá má stav úpravy **Nenastaviteľné**.</p> | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul> |
| Časový záznam sa po schválení odvolá. | <p>Stav úpravy pôvodných skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvorí sa skutočná obstarávacia cena, ktorá má stav úpravy **Nenastaviteľné**.</p> | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul> |
| Vyhrá sa ponuka a vytvorí sa zmluva. | <p>Stav úpravy starých skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvárajú sa skutočné náklady na stornovanie, ktoré majú stav úpravy **Nenastaviteľné**.</p><p>Nové skutočné náklady sa vytvárajú po prehodnotení zmluvných pravidiel.</p> | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul><p>Nové skutočnosti, ktoré sa vytvoria pre prehodnotený finančný vplyv, keď sa získa ponuka a vznikne zmluva:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800</li><li>**Skutočný nevyfakturovaný predaj:** Bob Kozack, 8 hodín, USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
