---
title: Skutočný vplyv na interný projekt
description: Tento článok poskytuje informácie o vplyve na tabuľku Skutočné údaje pri rôznych udalostiach interného projektu v spoločnosti Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921367"
---
# <a name="actuals-impact-for-an-internal-project"></a>Skutočný vplyv na interný projekt

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Nasledujúca tabuľka uvádza skutočné hodnoty rôznych typov transakcií, ktoré sa vytvárajú pri rôznych udalostiach v rámci internej projektovej zákazky.

| Udalosť | Skutočné údaje nákladov | Príklad |
|---|---|---|
| Čas je vytvorený. | Nevzťahuje sa | <p>Bob Kozack z organizačnej jednotky Fabrikam US, ktorá má cenu 100 USD (100 USD) za hodinu, pracuje na projekte s názvom „Inštalácia ramena v Adatum“. Tento projekt je namapovaný na spôsob fakturácie s pevnou cenou na riadku zmluvy. Tu je ukážkový časový záznam od Boba Kozaka:</p><p>Bob Kozack - 8 hodín</p> |
| Čas je predložený. | Nevzťahuje sa | Pre časový záznam sa vytvorí riadok nákladového denníka. Predvolená nákladová sadzba sa zadá do účtovného zápisu. |
| Časový záznam sa pred schválením vyvolá. | Nevzťahuje sa | |
| Čas je schválený. | Vytvorí sa skutočný náklad. | <p>Nová skutočnosť, ktorá sa vytvorí:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800</li></ul> |
| Schválenie času je zrušené. | <p>Stav úpravy pôvodných skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvorí sa skutočná obstarávacia cena, ktorá má stav úpravy **Nenastaviteľné**.</p> | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul> |
| Časový záznam sa po schválení odvolá. | <p>Stav úpravy pôvodných skutočných nákladov sa aktualizuje na **Upravená**.</p><p>Vytvorí sa skutočná obstarávacia cena, ktorá má stav úpravy **Nenastaviteľné**.</p> | <p>Existujúce skutočné, ktoré sa aktualizujú:</p><ul><li>**Skutočné náklady:** Bob Kozack, 8 hodín, USD 800, *Upravená*</li></ul><p>Nová skutočnosť, ktorá sa vytvorí na zvrátenie predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočné náklady:** Bob Kozack, (8 hodín), (800 USD), *Nenastaviteľné*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
