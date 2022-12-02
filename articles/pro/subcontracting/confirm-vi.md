---
title: Potvrdenie projektovej faktúry dodávateľa
description: Tento článok vysvetľuje, ako potvrdiť faktúru dodávateľa projektu v Microsoft Dynamics 365 Project Operations a finančný dopad potvrdenia faktúry dodávateľa projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261532"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potvrdenie projektovej faktúry dodávateľa

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Po overení všetkých riadkov na faktúre dodávateľa v Microsoft Dynamics 365 Project Operations môžete použiť akciu Potvrdiť na potvrdenie faktúry dodávateľa.

Keď vyberiete **Potvrdiť** na faktúre dodávateľa, dochádza k nasledujúcemu správaniu:

1. Stav faktúry dodávateľa sa aktualizuje na **Potvrdené**.
2. Potvrdená faktúra dodávateľa a súvisiace záznamy sa zmenia iba na čítanie a nie je možné ich upravovať ani mazať.
3. Ak niektoré skutočné náklady odkazujú na riadok faktúry dodávateľa ako súčasť procesu párovania, všetky skutočné náklady, ktoré sú priradené k riadku faktúry dodávateľa s odkazom, sa stornujú.
4. Nové skutočné náklady sa vytvárajú pomocou informácií v riadku faktúry dodávateľa.
5. Po potvrdení stornovaní faktúry dodávateľa už nemôžete vytvárať denníky opráv, spracovávať odvolania časových vstupov alebo zrušiť schválenie pôvodných skutočných časov, výdavkov alebo materiálu, ktoré boli stornované.

> [!NOTE]
> Ak má niektorý riadok na faktúre dodávateľa stav overenia iný ako **Dokončiť**, faktúru dodávateľa nie je možné potvrdiť.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
