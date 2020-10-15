---
title: Odhady zdrojov
description: Táto téma poskytuje informácie o tom, ako sa počítajú odhady zdrojov v Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: f255b2cbf290973ce62fe2c1c121bd1df15a7392
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3928606"
---
# <a name="resource-estimates"></a>Odhady zdrojov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Odhady zdrojov pochádzajú z časovo odstupňovaného úsilia, ktoré je definované v štruktúre rozdelenia práce spolu s príslušnými cenovými dimenziami. Typický výpočet je **rýchlosť/hod. pre každú rolu x hodiny.** Časovo odstupňované úsilie pre každý zdroj je uložené v zázname o priradení zdroja. Cena je uložená v preddefinovanom cenníku. Prevod jednotiek sa uplatňuje na základe príslušného cenníka.

![Odhady zdrojov](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Predvolená obstarávacia cena a mena nákladov

Obstarávacie ceny sú predvolené od organizačnej jednotky.

## <a name="default-bill-rate-and-sales-currency"></a>Predvolené sadzby fakturácie a meny predaja

Predajné ceny sa uplatňujú raz pre každú dohodu. Hierarchia predvolených predajných cenníkov je nasledovná:

1. Organizácia
2. Zákazník
3. Cenová ponuka/zmluva
