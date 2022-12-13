---
title: Náklady v riadkoch cenových ponúk založených na produkte
description: Tento článok téma poskytuje informácie o uplatnení obstarávacej ceny na riadok cenovej ponuky založený na produkte.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: a8b3569ff217f6fc62606dae4292be14f9d3358c
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825631"
---
# <a name="costing-product-based-quote-lines"></a>Náklady v riadkoch cenových ponúk založených na produkte

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_


Produktové riadky ponúk v rámci Dynamics 365 Project Operations majú aj pole **Obstarávacia cena**. Toto pole sa používa na sledovanie obstarávacej ceny produktu v riadku cenovej ponuky a na následné výpočty ziskovosti.

Keď sa pre katalógový produkt vytvorí riadok cenovej ponuky založenej na produkte, náklad v riadku cenovej ponuky založenej na produkte sa predvolene nastaví podľa poľa **Štandardné náklady** v katalógu produktov. Pole štandardných nákladov v katalógu produktov je nastavené v základnej mene organizácie. Predvolené jednotkové náklady v riadku cenovej ponuky založenej na produkte sa prevedú na predajnú menu v cenovej ponuke.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Jednotkový náklad v riadku cenovej ponuky založenej na produkte

Účelom jednotkových nákladov v riadku cenovej ponuky založenej na produkte je umožniť rozdielne náklady na produkt pri každom predaji. Toto nie je typický scenár, ale niekedy môže dodávateľ znížiť cenu produktu v závislosti od zákazníka konečného predaja.

Napríklad:

Spoločnosť Fabrikam Robotics inštaluje robotické ramená na montážnych linkách spoločnosti A Datum Corporation. Fabrikam poskytuje inštalačné služby, ale robotické ramená sú získavané od spoločnosti Trey robotics. Ak inštalácia robotických ramien v spoločnosti A Datum Corporation otvorí novú priemyselnú vertikálu pre robotické ramená od spoločnosti Trey, spoločnosť Trey môže poskytnúť spoločnosti Fabrikam špeciálnu zľavu za tento obchod.

V takom prípade spoločnosť Fabrikam vytvorí riadok cenovej ponuky založenej na produkte pre spoločnosť Robotic Arms a pre túto cenovú ponuku zadá špeciálne jednotkové náklady. Tieto náklady sa líšia od štandardných nákladov spoločnosti Trey Robotic Arms.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
