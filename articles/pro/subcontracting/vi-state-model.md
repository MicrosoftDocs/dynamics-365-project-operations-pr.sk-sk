---
title: Prechody stavu na faktúre dodávateľa
description: Táto téma vysvetľuje prechody stavu na faktúre dodávateľa v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7efb52621ee325d5025dfad0b45218d1fe20a063
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584707"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Prechody stavu na faktúre dodávateľa

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma vysvetľuje prechody stavu na faktúre dodávateľa v Microsoft Dynamics 365 Project Operations. Používajú sa tieto stavy: **Návrh**, **recenzii**, **·**, **a** **Zrušené**.

Nasledujúce obrázky zobrazujú prechody stavov.

![Model prechodu stavu subdodávok.](../media/VI_State_Model.jpg)

Nasledujúca tabuľka vysvetľuje, čo každý stav predstavuje v životnom cykle faktúry dodávateľa v Project Operations.

| State | Description | Povolené prechody |
| --- | --- | --- |
| Koncept | Tento stav je počiatočným stavom faktúry dodávateľa. Línie a ceny podliehajú zmenám. Faktúru dodávateľa v tomto stave je možné upravovať a mazať. | V procese |
| Prebieha kontrola | Tento stav predstavuje stav spracovania faktúry dodávateľa. Aspoň jeden riadok faktúry dodávateľa má stav overenia **Prebieha**. | Potvrdené, Podržané |
| Potvrdené | Tento stav predstavuje fázu faktúry dodávateľa, kde aplikácia vytvorila skutočné náklady pre každý riadok faktúry dodávateľa. Všetky prepojené skutočné náklady, ktoré boli priradené k riadkom faktúry dodávateľa, boli stornované a nahradené skutočnými nákladmi z týchto riadkov faktúry dodávateľa. Faktúru dodávateľa v tomto stave nie je možné upraviť ani odstrániť. Môžete použiť **Zrušiť** tlačidlo na zrušenie potvrdenej faktúry dodávateľa. Akcia Zrušiť zruší účinok akcie Potvrdiť. | Zrušená |
| Pozastavené | <p>Tento stav predstavuje štádium faktúry dodávateľa, kde sa faktúra dodávateľa nemôže posunúť z dôvodu problému s faktúrou alebo stavu dodávateľa. Faktúru dodávateľa v tomto stave nie je možné potvrdiť, zrušiť, upraviť ani odstrániť.</p><p>Akciu Opätovné otvorenie môžete použiť na presun faktúry dodávateľa do **Návrh** alebo **V recenzii** štát. Ak má aspoň jeden riadok na faktúre dodávateľa stav overenia **Prebieha** alebo **Dokončiť**, faktúra dodávateľa bude znovu otvorená v **V recenzii** štát. Ak majú všetky riadky na faktúre dodávateľa stav overenia **Nezačal**, faktúra dodávateľa bude znovu otvorená v **Návrh** štát.</p> | Koncept, Prebieha kontrola |
| Zrušená | Tento stav predstavuje štádium subdodávky, kde už nie je potrebná skutočná dodávka materiálu a/alebo práce zo subdodávateľských zdrojov. Subdodávateľská zmluva v tomto stave sa nedá použiť na odhad a personálne projektové požiadavky na zdroje a materiály a tiež sa na ňu nedá odkázať čas, náklady a spotreba materiálu v projekte. Subdodávateľskú zmluvu v tomto stave nie je možné upraviť ani odstrániť. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
