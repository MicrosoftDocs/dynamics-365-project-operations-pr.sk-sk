---
title: Skutočné údaje
description: Tento článok poskytuje informácie o tom, ako pracovať so skutočnými údajmi v aplikácii Microsoft Dynamics 365 Project Operations.
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
ms.openlocfilehash: 2551b7d6d20df170c913e302e734583135265529
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924817"
---
# <a name="actuals"></a>Skutočné hodnoty

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Skutočné hodnoty predstavujú skontrolované a schválené finančné údaje a naplánovaný postup projektu. Vytvárajú sa po schválení zadaní času, výdavkov, položiek použitia materiálu, účtovných záznamov a faktúr.

> [!IMPORTANT]
> Skutočné hodnoty by sa nemali upravovať ani odstraňovať zo systému. V opačnom prípade môže byť nepriaznivo ovplyvnená finančná integrita a akákoľvek integrácia s inými finančnými a účtovnými systémami. Microsoft Dynamics 365 Project Operations umožňuje použiť storno a nahradenie skutočných hodnôt na úpravu skutočných hodnôt v rôznych bodoch životného cyklu obchodného procesu vašich projektov.

## <a name="recording-actuals-based-on-project-events"></a>Zaznamenávanie skutočných údajov na základe projektových podujatí

Project Operations zaznamenáva finančné transakcie, ktoré sa vyskytnú počas životného cyklu interakcie s projektom ako skutočné hodnoty. Vytváranie skutočných hodnôt pri rôznych udalostiach v životnom cykle sa líši v závislosti od toho, či interakcia s projektom používa model účtovania času a materiálu alebo model účtovania s pevnou cenou a či je vo fáze predpredaja alebo ide o interný projekt.

Nasledujúce články vysvetľujú vplyv na tabuľku Skutočné hodnoty pri rôznych udalostiach pre rôzne variácie:

- [Vplyv skutočných hodnôt v rámci interakcie s časom a materiálmi](ActualsonTM.md)
- [Vplyv skutočných hodnôt v rámci interakcie s pevnou cenou](ActualonFP.md)
- [Vplyv skutočných hodnôt počas štádia predpredaja v rámci interakcie](ActualonPreSales.md)
- [Vplyv skutočných hodnôt pre interný projekt](ActualonInternal.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
