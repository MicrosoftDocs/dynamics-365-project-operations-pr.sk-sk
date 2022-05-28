---
title: Skutočné hodnoty
description: Táto téma poskytuje informácie o tom, ako pracovať so skutočnými údajmi v aplikácii Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3f0cb8c478e2ce6fba589d51d95649f53f62e883
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581303"
---
# <a name="actuals"></a>Skutočné hodnoty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Skutočné hodnoty predstavujú skontrolované a schválené finančné údaje a naplánovaný postup projektu. Vytvárajú sa, keď sú schválené položky času, nákladov a spotreby materiálu, účtovné zápisy a faktúry.

> [!IMPORTANT]
> Skutočné hodnoty by sa nemali upravovať ani odstraňovať zo systému. V opačnom prípade môže byť nepriaznivo ovplyvnená finančná integrita a akákoľvek integrácia s inými finančnými a účtovnými systémami. Microsoft Dynamics 365 Project Operations umožňuje použiť obrátenie a nahradenie skutočných hodnôt na úpravu skutočných hodnôt v rôznych bodoch životného cyklu obchodného procesu vašich projektov.

## <a name="recording-actuals-based-on-project-events"></a>Zaznamenávanie skutočných údajov na základe projektových podujatí

Operácie projektu zaznamenávajú finančné transakcie, ktoré sa vyskytnú počas životného cyklu projektovej zákazky, ako skutočné. Vytváranie skutočných udalostí pri rôznych udalostiach v životnom cykle sa líši v závislosti od toho, či projektové zapojenie používa model fakturácie času a materiálu alebo model fakturácie s pevnou cenou a či je vo fáze predpredaja alebo ide o interný projekt.

Nasledujúce témy vysvetľujú vplyv na tabuľku Skutočnosti pri rôznych udalostiach pre rôzne variácie:

- [Skutočný vplyv na čas a materiál](ActualsonTM.md)
- [Skutočný vplyv na interakciu s pevnou cenou](ActualonFP.md)
- [Skutočný vplyv počas predpredajnej fázy zákazky](ActualonPreSales.md)
- [Skutočný vplyv na interný projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
