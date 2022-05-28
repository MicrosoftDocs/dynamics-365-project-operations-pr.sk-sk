---
title: Zrušte faktúru dodávateľa projektu
description: Táto téma vysvetľuje, ako zrušiť faktúru dodávateľa projektu v spoločnosti Microsoft Dynamics 365 Project Operations a finančný dopad zrušenia faktúry dodávateľa projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580659"
---
# <a name="cancel-a-project-vendor-invoice"></a>Zrušte faktúru dodávateľa projektu

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Po potvrdení faktúry dodávateľa ju nie je možné upraviť ani odstrániť. Ak sa na faktúre dodávateľa vyskytla chyba, ktorá bola potvrdená, môžete pomocou akcie Zrušiť zvrátiť vplyv faktúry dodávateľa a vytvoriť novú faktúru dodávateľa.

Keď vyberiete **Zrušiť** na faktúre dodávateľa dochádza k nasledujúcemu správaniu:

1. Stav faktúry dodávateľa sa aktualizuje na **Zrušené**.
2. Zrušená faktúra dodávateľa a súvisiace záznamy sa stanú iba na čítanie a nie je možné ich upravovať ani mazať.
3. Všetky skutočné náklady, ktoré boli vytvorené na základe riadkov faktúry dodávateľa ako súčasť potvrdenia faktúry dodávateľa, sa stornujú.
4. Ak boli nejaké skutočné náklady spojené s riadkami faktúry dodávateľa ako súčasť procesu párovania, pôvodné potvrdenie faktúry dodávateľa ich zrušilo. Počas zrušenia faktúry dodávateľa sa tieto skutočné náklady znova vytvoria. Pôvod poukazujú na položky času, nákladov alebo spotreby materiálu.
5. Po zrušení faktúry dodávateľa môžete znova vytvárať denníky opráv, spracovávať odvolania časových vstupov a zrušiť schválenie pôvodných skutočných časov, nákladov alebo materiálu.

> [!NOTE]
> Stornovať možno len potvrdené faktúry dodávateľa projektu. Faktúry dodávateľa v iných štátoch nie je možné zrušiť.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
