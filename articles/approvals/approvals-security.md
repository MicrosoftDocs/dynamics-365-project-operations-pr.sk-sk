---
title: Zabezpečenie a schválenia
description: Tento článok poskytuje informácie o nastavení zabezpečenia pre prácu so schváleniami v Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709417"
---
# <a name="security-and-approvals"></a>Zabezpečenie a schválenia

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Microsoft Dynamics 365 Project Operations používa dve roly zabezpečenia, ktoré umožňujú schvaľovanie záznamov času, nákladov a materiálu:

- Schvaľovateľ projektu
- Administrátor schvaľovateľa projektu

## <a name="project-approver"></a>Schvaľovateľ projektu

Musíte mať **Schvaľovateľ projektu** rola zabezpečenia na schválenie projektového času, výdavkov a materiálových vstupov. Musíte mať prístup aj k príslušným spriazneným subjektom, ako napr **Projekt**. Tento prístup môže prideliť niekto, kto má **Projektový manažér** úlohu. Okrem toho musíte byť členom tímu projektu a označený ako schvaľovateľ.

Ak chcete schvaľovať neprojektové príspevky, musíte byť manažérom zadávateľa.

## <a name="project-approver-admin"></a>Administrátor schvaľovateľa projektu

> [!NOTE]
> The [Sady schvaľovania](approval-sets.md) Funkcia správcu projektu musí byť povolená.

The **Administrátor schvaľovateľa projektu** rola zabezpečenia umožňuje používateľom obísť pravidlá a umožňuje schvaľovanie záznamov vo všetkých projektoch. Priradenie tejto roly obíde logiku overovania, ktorá vyžaduje členstvo v tíme a označenie ako schvaľovateľa. Musíte mať prístup k príslušným súvisiacim tabuľkám, ako napr **Projekt**, prostredníctvom rolí zabezpečenia, ktoré vám boli pridelené.

Používateľský kontext SYSTEM obchádza overenia rovnakým spôsobom ako správca schvaľovateľa projektu rola zabezpečenia.
