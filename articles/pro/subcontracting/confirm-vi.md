---
title: Potvrdenie projektovej faktúry dodávateľa
description: Tento článok vysvetľuje, ako potvrdiť faktúru dodávateľa projektu v spoločnosti Microsoft Dynamics 365 Project Operations a finančný dosah potvrdenia faktúry dodávateľa projektu.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932453"
---
# <a name="confirm-a-project-vendor-invoice"></a>Potvrdenie projektovej faktúry dodávateľa

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Po overení všetkých riadkov na faktúre dodávateľa v Microsofte Dynamics 365 Project Operations, môžete použiť akciu Potvrdiť na potvrdenie faktúry dodávateľa.

Keď vyberiete **Potvrďte** na faktúre dodávateľa dochádza k nasledujúcemu správaniu:

1. Stav faktúry dodávateľa sa aktualizuje na **Potvrdené**.
2. Potvrdená faktúra dodávateľa a súvisiace záznamy sa stanú iba na čítanie a nie je možné ich upravovať ani mazať.
3. Ak niektoré skutočné náklady odkazujú na riadok faktúry dodávateľa ako súčasť procesu párovania, všetky skutočné náklady, ktoré sú priradené k riadku faktúry dodávateľa s odkazom, sa stornujú.
4. Nové skutočné náklady sa vytvárajú pomocou informácií v riadku faktúry dodávateľa.
5. Po potvrdení faktúry dodávateľa už nemôžete vytvárať denníky opráv, spracovávať odvolania záznamu času alebo zrušiť schválenie pôvodných skutočných časov, nákladov alebo materiálu, ktoré boli stornované.

> [!NOTE]
> Ak má niektorý riadok na faktúre dodávateľa stav overenia iný ako **Dokončiť**, faktúru dodávateľa nie je možné potvrdiť.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
