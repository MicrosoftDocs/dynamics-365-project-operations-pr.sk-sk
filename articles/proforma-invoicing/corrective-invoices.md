---
title: Opravené faktúry
description: Táto téma poskytuje informácie o opravených faktúrach.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1ebfec053a59bbadd261d4333f6737cf16292e81
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122407"
---
# <a name="corrected-invoices"></a>Opravené faktúry

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Potvrdené faktúry môžu byť editované. Keď upravíte potvrdenú faktúru, vytvorí sa koncept opravenej faktúry. Pretože predpoklad je, že chcete zvrátiť všetky transakcie a množstvá z pôvodnej faktúry, opravená faktúra obsahuje všetky transakcie z pôvodnej faktúry a všetky množstvá na nej sú 0 (nula).

Keď niektoré transakcie nevyžadujú opravu, môžete ich odstrániť z konceptu opravnej faktúry. Ak chcete zvrátiť alebo vrátiť iba čiastočné množstvo, môžete upraviť pole Množstvo v detaile riadka. Ak otvoríte detail riadka faktúry, môžete vidieť pôvodné množstvo faktúry. Potom môžete upraviť aktuálne množstvo faktúr tak, aby bolo menšie ako alebo väčšie ako pôvodné množstvo faktúry.

Po potvrdení opravnej faktúry, sú stornované pôvodné fakturované skutočné hodnoty a sú vytvorené nové fakturované skutočné hodnoty predaja. Ak bolo množstvo znížené, rozdiel spôsobí nové vytvorenie ďalších nefakturovaných skutočných hodnôt predaja. Ak bol napríklad pôvodný fakturovaný predaj osem hodín a detail riadka opravenej faktúry má znížené množstvo šiestich hodín, pôvodný fakturovaný predajný riadok sa vráti späť a vytvoria dve nové skutočné hodnoty:

- Skutočná hodnota fakturovaného predaja je šesť hodín.
- Skutočná hodnota nefakturovaného predaja sú dve hodiny. Táto transakcia môže byť fakturovaná neskôr alebo označená ako nefakturovateľná v závislosti od rokovaní so zákazníkom.


[!INCLUDE[footer-include](../includes/footer-banner.md)]