---
title: Integrácia duálneho zápisu Project Operations
description: Tento článok poskytuje prehľad integrácie duálneho zápisu Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927991"
---
# <a name="project-operations-dual-write-integration-overview"></a>Prehľad integrácie duálneho zápisu Project Operations

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Project Operations využíva [možnosti duálneho zápisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) na synchronizáciu údajov naprieč Microsoft Dataverse a Dynamics 365 Finance.

Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje ako súčasť tejto integrácie medzi Dataverse a Finance.

![Prehľad tokov údajov Project Operations.](./media/ProjectOperationsFlows.jpg)

Project Operations v Dataverse poskytujú moderné používateľské rozhranie (UI) a ľahkú rozšíriteľnosť bez kódu/s nízkym kódom pomocou možností Power Platform. Projektoví manažéri, manažéri zdrojov, členovia projektového tímu a ďalšie osobnosti front-office vykonávajú svoje činnosti v rámci Project Operations v Dataverse.

Project Operations vo Finance poskytuje podporu projektového účtovníctva a uznávania výnosov. Project Operations sa pripájajú k finančnému rámcu v Finance pre výpočet dane z obratu, výmenné kurzy, vykazovanie finančnej dimenzie a ďalšie. Skúsenosti účtovníka projektu sú väčšinou založené v nástroji Finance.

Integrácia Project Operations pozostáva z nasledujúcej integrácie komponentov:


- [Integrácia nastavenia a konfiguračných údajov aplikácie Project Operations](resource-dual-write-setup-integration.md) 
- [Odhady a skutočné hodnoty projektu](resource-dual-write-estimates-actuals.md)
- [Projektové faktúry](resource-dual-write-project-invoice.md)
- [Správa výdavkov](resource-dual-write-expense.md)
- [Faktúra dodávateľa](resource-dual-write-vendor-invoice.md)
