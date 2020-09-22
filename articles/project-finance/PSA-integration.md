---
title: Project Service Automation – prehľad
description: Táto téma obsahuje informácie o riešení integrácie Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 897e1a1c-d31c-42b8-bb59-6b67202d8d61
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 080a545d8713e52d9778367aec1969b815d683e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755608"
---
# <a name="project-service-automation-overview"></a>Project Service Automation – prehľad

[!include[banner](../includes/banner.md)]

Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Dynamics 365 Finance a Dynamics 365 Project Service Automation cez Common Data Service. Integračné šablóny, ktoré sú k dispozícii s funkciou Integrácia údajov, umožňujú tok projektov, projektových zmlúv, riadkov projektových zmlúv, medzníkov riadkov projektových zmlúv, projektových úloh, kategórií transakcií výdavkov, odhadov hodín a odhadov výdavkov z Project Service Automation do Finance.

> [!NOTE]
> - Ak používate verziu 7.3.0, musíte nainštalovať KB 4074835. Potom budete môcť integrovať projekty s pevnou cenou.
> - Ak používate verziu 7.3.0 a prenášate transakcie poplatkov z Project Service Automation, musíte nainštalovať KB 4345320, aby ste mohli zahrnúť tieto poplatky do faktúry za projekt.
> - Ak používate verziu 8.0, budete môcť používať integráciu projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií.
> - Ak používate verziu 8.0.1 alebo novšiu, budete môcť synchronizovať skutočné údaje.

Predtým, ako budete môcť integrovať Project Service Automation Finance, musíte nakonfigurovať parametre integrácie Project Service Automation. Pre ďalšie informácie si pozrite [Parametre integrácie Project Service Automation](PSA-parameters.md).

Toto integračné riešenie umožňuje priamu synchronizáciu v nasledujúcich scenároch:

- Udržiavanie projektových zmlúv v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.
- Vytváranie projektov v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.
- Udržiavanie riadkov projektových zmlúv v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.
- Udržiavanie medzníkov riadkov projektových zmlúv v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.
- Udržiavanie projektových úloh v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.
- Udržiavanie kategórií výdavkov na transakciu vo Finance a ich priama synchronizácia z Finance do Project Service Automation.
- Vytváranie odhadov hodín projektov v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.
- Vytváranie odhadov výdavkov na projekty v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.
- Vytváranie skutočných údajov o projektov, výdavkoch a poplatkoch v Project Service Automation a vytvorenie transakcií projektov v integračnom žurnále Project Service Automation, aby ich bolo možné zverejniť v službe Finance.

## <a name="data-synchronization"></a>Synchronizácia údajov

Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje ako súčasť integrácie medzi Project Service Automation a Finance.

> [!NOTE]
> Nie všetky šablóny sú momentálne k dispozícii. Šablóny budú vydané hneď po dokončení.

[![Integrácia Project Service Automation s Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systémové požiadavky na Finance

Ak chcete použiť riešenie integrácie Project Service Automation do Finance, musíte si nainštalovať Enterprise edition 7.3 s aktualizáciou platformy 12 alebo novšou.

## <a name="system-requirements-for-project-service-automation"></a>Systémové požiadavky na Project Service Automation

Ak chcete použiť riešenie integrácie Project Service Automation do Finance, musíte si nainštalovať nasledujúce komponenty:

- Dynamics 365 Project Service Automation verzia 9.0.0.0 alebo novšia
- Riešenie Od záujemcu po platbu pre Dynamics 365 Sales, verzia 1.14.0.0 (v14) alebo novšia
- Riešenie Project Service Automation do Finance pre Dynamics 365 Project Service Automation, verzia 1.0.0.0 alebo novšia

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Nainštalujte si do svojej inštancie Project Service Automation integračné riešenie Project Service Automation do Finance

Stiahnite si integračné riešenie Project Service Automation do Finance z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) a postupujte podľa pokynov, ktoré sú súčasťou riešenia.
