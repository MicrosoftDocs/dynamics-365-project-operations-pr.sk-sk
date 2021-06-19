---
title: Náklady v riadkoch zmlúv založených na produkte – čiastočné
description: Táto téma poskytuje informácie o vytváraní
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003560"
---
# <a name="cost-product-based-contract-lines---lite"></a>Náklady v riadkoch zmlúv založených na produkte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Riadky zmlúv založené na produkte Dynamics 365 Project Operations zahŕňajú pole **Obstarávacia cena**, v ktorom sa ukladá obstarávacia cena produktu pre následné výpočty ziskovosti.

Keď sa pre katalógový produkt vytvorí riadok zmluvy založený na produkte, náklady v tomto riadku sa štandardne nastavia podľa poľa **Štandardné náklady** v katalógu produktov. Pole **Štandardné náklady** v katalógu produktov je nastavené v základnej mene organizácie. Keď sú jednotkové náklady predvolené pre riadok zmluvy, prevedú sa na menu predaja v zmluve.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Jednotkový náklad v riadku zmluvy založenej na produkte

Jednotkové náklady v riadku zmluvy založenej na produkte umožňujú rôzne produktové náklady pre každý predaj jednotky. Aj keď to nie je vždy potrebné, existujú určité scenáre, pri ktorých môže dodávateľovi zákazníkovi odpočítať náklady na produkt. Posúďte nasledujúci scenár:

Spoločnosť Fabrikam Robotics inštaluje robotické ramená na montážnych linkách spoločnosti Adatum Corporation. Spoločnosť Fabrikam poskytuje inštalačné služby, ale robotické ramená pochádzajú od spoločnosti Trey Research. Ak inštalácia robotických ramien v spoločnosti Adatum Corporation otvorí novú priemyselnú vertikálu pre robotické ramená od spoločnosti Trey Research, môže poskytnúť spoločnosti Fabrikam špeciálnu zľavu za tento obchod. V takom prípade vytvorí spoločnosť Fabrikam pre spoločnosť Robotic Arms riadok zmluvy založený na produkte. Pri tejto zmluve sa zadáva jednotkový náklad. Náklad sa líši od nákladu na robotické ramená od spoločnosti Trey Research.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]