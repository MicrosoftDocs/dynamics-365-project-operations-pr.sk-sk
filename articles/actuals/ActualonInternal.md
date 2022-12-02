---
title: Vplyv skutočných hodnôt pre interný projekt
description: Tento článok poskytuje informácie o vplyve na tabuľku Skutočné hodnoty pri rôznych udalostiach pre interný projekt v Microsoft Dynamics 365 Project Operations.
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
# <a name="actuals-impact-for-an-internal-project"></a>Vplyv skutočných hodnôt pre interný projekt

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Nasledujúca tabuľka uvádza skutočné hodnoty o rôznych typoch transakcií, ktoré sa vytvoria pri rôznych udalostiach v rámci interakcie s interným projektom.

| Udalosť | Skutočné údaje nákladov | Príklad |
|---|---|---|
| Čas je vytvorený. | Nevzťahuje sa | <p>Bob Kozack z organizačnej jednotky Fabrikam US, ktorá má nákladovú sadzbu 100 USD za hodinu, pracuje na projekte s názvom „Inštalácia ramena v Adatum“. Tento projekt je priradený k spôsobu fakturácie s pevnou cenou na riadku zmluvy. Tu je ukážkový časový záznam od Boba Kozaka:</p><p>Bob Kozack – 8 hodín</p> |
| Čas je odoslaný. | Nevzťahuje sa | Pre každú časovú položku sa vytvorí záznam v účtovnom denníku nákladov. Predvolená nákladová sadzba sa zadá do účtovného záznamu. |
| Zadanie času sa vyvolá pred schválením. | Nevzťahuje sa | |
| Čas je schválený. | Vytvorí sa skutočný náklad. | <p>Nová skutočná hodnota, ktorá sa vytvorí:</p><ul><li>**Skutočný náklad:** Bob Kozack, 8 hodín, USD 800</li></ul> |
| Schválenie času je zrušené. | <p>Stav úpravy pôvodnej skutočnej hodnoty nákladov sa aktualizuje na **Upravené**.</p><p>Vytvorí storno skutočnej hodnoty nákladov, ktoré má stav úpravy **Neupraviteľné**.</p> | <p>Existujúca skutočná hodnota, ktorá je aktualizovaná:</p><ul><li>**Skutočný hodnota nákladov:** Bob Kozack, 8 hodín, USD 800, *Upravené*</li></ul><p>Nová skutočná hodnota, ktorá je vytvorená na storno predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočná hodnota nákladov:** Bob Kozack, (8 hodín), (USD 800), *Neupraviteľné*</li></ul> |
| Zadanie času sa vyvolá po schválení. | <p>Stav úpravy pôvodnej skutočnej hodnoty nákladov sa aktualizuje na **Upravené**.</p><p>Vytvorí storno skutočnej hodnoty nákladov, ktoré má stav úpravy **Neupraviteľné**.</p> | <p>Existujúca skutočná hodnota, ktorá je aktualizovaná:</p><ul><li>**Skutočný hodnota nákladov:** Bob Kozack, 8 hodín, USD 800, *Upravené*</li></ul><p>Nová skutočná hodnota, ktorá je vytvorená na storno predchádzajúceho finančného vplyvu:</p><ul><li>**Skutočná hodnota nákladov:** Bob Kozack, (8 hodín), (USD 800), *Neupraviteľné*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
