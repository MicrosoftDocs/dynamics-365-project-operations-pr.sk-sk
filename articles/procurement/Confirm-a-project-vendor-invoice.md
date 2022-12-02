---
title: Potvrdenie projektových faktúr dodávateľov
description: Tento článok vysvetľuje, ako potvrdiť faktúru dodávateľa projektu v Microsoft Dynamics 365 Project Operations a popisuje finančný dopad potvrdenia faktúry dodávateľa projektu.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475491"
---
# <a name="confirm-project-vendor-invoices"></a>Potvrdenie projektových faktúr dodávateľov

**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

Keď je povolený parameter **Vyžaduje sa manuálne potvrdenie zo strany PM**, faktúry dodávateľa, ktoré sú vytvorené v Microsoft Dataverse, majú stav **Koncept**. Faktúry dodávateľa, ktoré sú vytvorené týmto spôsobom, musia byť skontrolované a manuálne potvrdené. Keď je zakázaný parameter **Vyžaduje sa manuálne potvrdenie zo strany PM**, faktúry dodávateľa, ktoré sú vytvorené v Dataverse, sa potvrdia automaticky. Nevyžadujú sa žiadne ďalšie akcie. 

Po overení všetkých riadkov na faktúre dodávateľa v Dynamics 365 Project Operations vyberte **Potvrdiť** na potvrdenie faktúry dodávateľa.

Keď vyberiete **Potvrdiť** na faktúre dodávateľa, dochádza k nasledujúcemu správaniu:

1. Stav faktúry dodávateľa sa aktualizuje na **Potvrdené**.
1. Potvrdená faktúra dodávateľa a súvisiace záznamy sa zmenia iba na čítanie a nie je možné ich upravovať ani mazať.
1. Ak niektoré skutočné náklady odkazujú na riadok faktúry dodávateľa ako súčasť procesu párovania, všetky skutočné náklady, ktoré sú priradené k riadku faktúry dodávateľa s odkazom, sa stornujú.
1. Nové skutočné náklady sa vytvárajú pomocou informácií v riadku faktúry dodávateľa.
1. Nemôžete viac vytvárať denníky opráv, spracúvať storná zadaní času alebo zrušiť schválenie pôvodných skutočných časov, výdavkov alebo materiálu, ktoré boli stornované.
1. V Dynamics 365 Finance sa hodnota **Náklady na projekt** aktualizuje pomocou Denníka integrácie projektu a Účet integrácie obstarávania je *vrátený späť* po zverejnení Denníka integrácie projektu.

> [!NOTE]
> Ak má niektorý riadok na faktúre dodávateľa stav overenia iný ako **Dokončiť**, faktúru dodávateľa nie je možné potvrdiť.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
