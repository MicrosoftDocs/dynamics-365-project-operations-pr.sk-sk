---
title: Zrušenie projektovej faktúry dodávateľa
description: Tento článok vysvetľuje, ako zrušiť faktúru dodávateľa projektu v spoločnosti Microsoft Dynamics 365 Project Operations a finančný dopad zrušenia faktúry dodávateľa projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261110"
---
# <a name="cancel-a-project-vendor-invoice"></a>Zrušenie projektovej faktúry dodávateľa

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Po potvrdení faktúry dodávateľa ju nie je možné upraviť ani odstrániť. Ak sa na faktúre dodávateľa vyskytla chyba, ktorá bola potvrdená, môžete pomocou akcie Zrušiť zvrátiť vplyv faktúry dodávateľa a vytvoriť novú faktúru dodávateľa.

Keď vyberiete **Zrušiť** na faktúre dodávateľa dochádza k nasledujúcemu správaniu:

1. Stav faktúry dodávateľa sa aktualizuje na **Zrušené**.
2. Zrušená faktúra dodávateľa a súvisiace záznamy sa stanú iba na čítanie a nie je možné ich upravovať ani mazať.
3. Všetky skutočné náklady, ktoré boli vytvorené na základe riadkov faktúry dodávateľa ako súčasť potvrdenia faktúry dodávateľa, sa stornujú.
4. Ak boli nejaké skutočné náklady spojené s riadkami faktúry dodávateľa ako súčasť procesu párovania, pôvodné potvrdenie faktúry dodávateľa ich zrušilo. Počas zrušenia faktúry dodávateľa sa tieto skutočné náklady znova vytvoria. Pôvod poukazujú na položky času, nákladov alebo spotreby materiálu.
5. Po stornovaní faktúry dodávateľa môžete znova vytvárať denníky opráv, spracovávať odvolania časových vstupov a zrušiť schválenie pôvodných skutočných časov, nákladov alebo materiálu.

> [!NOTE]
> Stornovať možno iba potvrdené faktúry dodávateľa projektu. Faktúry dodávateľa v iných štátoch nie je možné zrušiť.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
