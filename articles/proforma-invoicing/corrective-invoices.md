---
title: Opravené faktúry
description: Táto téma poskytuje informácie o opravených faktúrach.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: e14da1c07d5b697de6caf1b9041c30581ecff102
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898100"
---
# <a name="corrected-invoices"></a>Opravené faktúry

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Potvrdené faktúry môžu byť editované. Keď upravíte potvrdenú faktúru, vytvorí sa koncept opravenej faktúry. Pretože predpoklad je, že chcete zvrátiť všetky transakcie a množstvá z pôvodnej faktúry, opravená faktúra obsahuje všetky transakcie z pôvodnej faktúry a všetky množstvá na nej sú 0 (nula).

Keď niektoré transakcie nevyžadujú opravu, môžete ich odstrániť z konceptu opravnej faktúry. Ak chcete zvrátiť alebo vrátiť iba čiastočné množstvo, môžete upraviť pole Množstvo v detaile riadka. Ak otvoríte detail riadka faktúry, môžete vidieť pôvodné množstvo faktúry. Potom môžete upraviť aktuálne množstvo faktúr tak, aby bolo menšie ako alebo väčšie ako pôvodné množstvo faktúry.

Po potvrdení opravnej faktúry, sú stornované pôvodné fakturované skutočné hodnoty a sú vytvorené nové fakturované skutočné hodnoty predaja. Ak bolo množstvo znížené, rozdiel spôsobí nové vytvorenie ďalších nefakturovaných skutočných hodnôt predaja. Ak bol napríklad pôvodný fakturovaný predaj osem hodín a detail riadka opravenej faktúry má znížené množstvo šiestich hodín, pôvodný fakturovaný predajný riadok sa vráti späť a vytvoria dve nové skutočné hodnoty:

- Skutočná hodnota fakturovaného predaja je šesť hodín.
- Skutočná hodnota nefakturovaného predaja sú dve hodiny. Táto transakcia môže byť fakturovaná neskôr alebo označená ako nefakturovateľná v závislosti od rokovaní so zákazníkom.
