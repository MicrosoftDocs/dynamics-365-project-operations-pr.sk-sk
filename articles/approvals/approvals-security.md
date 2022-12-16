---
title: Zabezpečenie a schválenia
description: Tento článok poskytuje informácie o nastavení zabezpečenia pre prácu so schváleniami v Microsoft Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841943"
---
# <a name="security-and-approvals"></a>Zabezpečenie a schválenia

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Microsoft Dynamics 365 Project Operations používa dve roly zabezpečenia, ktoré umožňujú schvaľovanie záznamov času, výdavkov a materiálu:

- Schvaľovateľ projektu
- Správca schvaľovateľa projektu

## <a name="project-approver"></a>Schvaľovateľ projektu

Musíte mať rolu zabezpečenia **Schvaľovateľ projektu** na schválenie zadaní času, výdavkov a materiálov pre projekt. Musíte mať aj prístup aj k príslušným súvisiacim entitám, ako je napr **Projekt**. Tento prístup môže prideliť niekto, kto má rolu **Projektový manažér**. Okrem toho musíte byť členom tímu projektu a označený ako schvaľovateľ.

Ak chcete schvaľovať neprojektové zadania, musíte byť manažérom odosielateľa.

## <a name="project-approver-admin"></a>Správca schvaľovateľa projektu

> [!NOTE]
> Pred použitím funkcie Správca schvaľovateľa projektu musí byť povolená funkcia [Množiny schválení](approval-sets.md).

Rola zabezpečenia **Správca schvaľovateľa projektu** umožňuje používateľom obísť pravidlá a umožňuje schvaľovanie zadaní vo všetkých projektoch. Priradenie tejto roly obíde logiku overovania, ktorá vyžaduje členstvo v tíme a označenie ako schvaľovateľa. Musíte mať prístup k príslušným súvisiacim tabuľkám, ako napr. **Projekt**, prostredníctvom rolí zabezpečenia, ktoré vám boli pridelené.

Používateľský kontext SYSTEM obchádza overenia rovnakým spôsobom ako rola zabezpečenia Správca schvaľovateľa projektu.
