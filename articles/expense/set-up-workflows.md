---
title: Nastavte pracovné postupy pre správu výdavkov
description: Môžete nastaviť proces pracovného postupu, ktorý sa používa na kontrolu a schválenie cestovných a výdavkových dokladov.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: e54fca67427e8f3d0e7050563a751b5be354356c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276052"
---
# <a name="set-up-workflows-for-expense-management"></a>Nastavte pracovné postupy pre správu výdavkov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Môžete nastaviť proces pracovného postupu na kontrolu a schválenie cestovných a výdavkových dokladov. Môžete definovať pracovné postupy pre výkazy výdavkov, cestovné požiadavky a žiadosti o hotovostné zálohy.

Pracovný postup predstavuje obchodný proces a definuje, ako dokument prechádza systémom. Pracovný postup tiež označuje, kto musí dokončiť úlohu alebo schváliť dokument. Používanie systému pracovných postupov vo vašej organizácii má niekoľko výhod:

- **Konzistentné procesy**: Môžete definovať proces schvaľovania pre konkrétne dokumenty, ako sú napríklad požiadavky na nákup a výkazy výdavkov. Používanie systému pracovných postupov pomáha zabezpečiť, aby boli dokumenty spracovávané a schvaľované konzistentne a efektívne.
- **Viditeľnosť procesu**: Môžete sledovať stav, históriu a metriky výkonu konkrétnej inštancie pracovného postupu. To vám pomôže určiť, či je potrebné vykonať zmeny v pracovnom postupe s cieľom zvýšiť efektivitu.
- **Centralizovaný pracovný zoznam**: Používatelia môžu zobraziť centralizovaný pracovný zoznam a zobraziť úlohy a schválenia pracovných postupov, ktoré sú im pridelené. 

## <a name="workflow-types"></a>Typy pracovných postupov

V nasledujúcej tabuľke sú uvedené typy pracovných postupov, ktoré môžete vytvoriť v **Správe výdavkov**.


|              <strong>Typ</strong>              |                   <strong>Tento typ použite na</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <strong>Automatické schválenie výkazu výdavkov</strong> |            Vytvorenie pracovných postupov schválenia pre výkazy výdavkov.             |
|  <strong>Automatické zaúčtovanie výkazov výdavkov</strong>   |        Vytvorenie pracovných postupov automatického zaúčtovania pre výkazy výdavkov.        |
|       <strong>Položka riadka výdavku</strong>        |     Vytvorenie pracovných postupov schválenia pre riadkové položky vo výkaze výdavkov.      |
| <strong>Automatické zaúčtovanie položky riadka výdavku</strong> | Vytvorenie pracovných postupov automatického zaúčtovania pre riadkové položky vo výkaze výdavkov. |
|       <strong>Cestovná žiadanka</strong>       |          Vytvorenie pracovných postupov schvaľovania pre cestovné požiadavky.           |
|      <strong>Požiadavka o platbu vopred</strong>      |         Vytvorte pracovné postupy schvaľovania pre žiadosti o hotovostné zálohy.          |
|        <strong>Vrátenie dane z pridanej hodnoty</strong>        | Vytvorte schvaľovacie pracovné postupy pre vrátenie dane z pridanej hodnoty (DPH).  |


[!INCLUDE[footer-include](../includes/footer-banner.md)]