---
title: Náklady v riadkoch zmlúv založených na produkte
description: Táto téma poskytuje informácie o vytváraní
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084595"
---
# <a name="costing-product-based-contract-lines"></a>Náklady v riadkoch zmlúv založených na produkte

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Riadky zmlúv založené na produkte v Dynamics 365 Project Operations obsahujú pole **Obstarávacia cena** , v ktorom je uložená obstarávacia cena produktu pre následné výpočty ziskovosti.

Keď sa pre katalógový produkt vytvorí riadok zmluvy založenej na produkte, náklad v riadku zmluvy založenej na produkte sa predvolene nastaví podľa poľa **Štandardné náklady** v katalógu produktov. Pole **Štandardné náklady** v katalógu produktov je nastavené v základnej mene organizácie. Keď sú jednotkové náklady predvolené pre riadok zmluvy, prevedú sa na menu predaja v zmluve.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jednotkový náklad v riadku zmluvy založenej na produkte

Jednotkové náklady v riadku zmluvy založenej na produkte umožňujú rôzne produktové náklady pre každý predaj jednotky. Aj keď to nie je vždy potrebné, existujú určité scenáre, pri ktorých môže dodávateľovi zákazníkovi odpočítať náklady na produkt. Posúďte nasledujúci scenár:

Spoločnosť Fabrikam Robotics inštaluje robotické ramená na montážnych linkách spoločnosti Adatum Corporation. Fabrikam poskytuje inštalačné služby, ale robotické ramená sú získavané od spoločnosti Trey Research. Ak inštalácia robotických ramien v spoločnosti Adatum Corporation otvorí novú priemyselnú vertikálu pre robotické ramená od spoločnosti Trey Research, môže poskytnúť spoločnosti Fabrikam špeciálnu zľavu za tento obchod. V takom prípade spoločnosť Fabrikam vytvorí riadok zmluvy založený na produkte pre spoločnosť Robotic Arms a zadá jednotkové náklady pre túto zmluvu, ktoré sa líšia od štandardných nákladov na robotické ramená od spoločnosti Trey Research.
