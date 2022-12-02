---
title: Prechody stavov v rámci faktúry dodávateľa
description: Tento článok vysvetľuje prechody stavu na faktúre dodávateľa v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261063"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Prechody stavov v rámci faktúry dodávateľa

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok vysvetľuje prechody stavu na faktúre dodávateľa v Microsoft Dynamics 365 Project Operations. Používajú sa tieto stavy: **Koncept**, **Prebieha kontrola**, **Potvrdené**, **Podržané** a **Zrušené**.

Nasledujúce obrázky zobrazujú prechody stavov.

![Model prechodu stavu subdodávateľskej zmluvy.](../media/VI_State_Model.jpg)

Nasledujúca tabuľka vysvetľuje, čo každý stav predstavuje v životnom cykle faktúry dodávateľa v Project Operations.

| State | Description | Povolené prechody |
| --- | --- | --- |
| Koncept | Tento stav je počiatočným stavom faktúry dodávateľa. Riadky a ceny podliehajú zmenám. Faktúra dodávateľa v tomto stave sa dá upravovať a odstrániť. | Prebiehajúce |
| Prebieha kontrola | Tento stav predstavuje stav spracovania faktúry dodávateľa. Aspoň jeden riadok faktúry dodávateľa má stav overenia **Prebieha**. | Potvrdené, pozastavené |
| Potvrdené | Tento stav predstavuje etapu faktúry dodávateľa, kde aplikácia vytvorila skutočné náklady pre každý riadok faktúry dodávateľa. Všetky prepojené skutočné náklady, ktoré boli priradené k riadkom faktúry dodávateľa, boli stornované a nahradené skutočnými nákladmi z týchto riadkov faktúry dodávateľa. Faktúra dodávateľa v tomto stave sa nedá upravovať ani odstrániť. Môžete použiť tlačidlo **Zrušiť** na zrušenie potvrdenej faktúry dodávateľa. Akcia Zrušiť zruší účinok akcie Potvrdiť. | Zrušená |
| Pozastavené | <p>Tento stav predstavuje etapu faktúry dodávateľa, kde sa faktúra dodávateľa nemôže posunúť z dôvodu problému s faktúrou alebo stavom dodávateľa. Faktúru dodávateľa v tomto stave nemožno potvrdiť, zrušiť, upraviť ani vymazať.</p><p>Akciu Opätovné otvorenie môžete použiť na presun faktúry dodávateľa do stavu **Koncept** alebo **Prebieha kontrola**. Ak má aspoň jeden riadok na faktúre dodávateľa stav overenia **Prebieha** alebo **Dokončené**, faktúra dodávateľa bude znovu otvorená v stave **Prebieha kontrola**. Ak majú všetky riadky na faktúre dodávateľa stav overenia **Nespustené**, faktúra dodávateľa bude znovu otvorená v stave **Koncept**.</p> | Koncept, Prebieha kontrola |
| Zrušená | Tento stav predstavuje etapu subdodávateľskej zmluvy, kde už nie je potrebná skutočná dodávka materiálu a/alebo práce zo subdodávateľských zdrojov. Subdodávateľská zmluva v tomto stave sa nedá použiť na odhad a personálne projektové požiadavky na zdroje a materiály a tiež sa na ňu nedá odkazovať na čas, náklady a spotrebu materiálu v projekte. Subdodávateľská zmluva v tomto stave sa nedá upravovať ani odstrániť. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
