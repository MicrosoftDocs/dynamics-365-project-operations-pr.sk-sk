---
title: Verzie máp duálneho zápisu v aplikácii Project Operations
description: Táto téma poskytuje zoznam máp duálneho zápisu potrebných pre Dynamics 365 Project Operations.
author: sigitac
ms.date: 04/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 452f9f16bfbae2d547afb9fcf4fc51595ea49890
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547128"
---
# <a name="project-operations-dual-write-map-versions"></a>Verzie máp duálneho zápisu v aplikácii Project Operations

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Použitím Dynamics 365 Project Operations pre scenáre zdrojov/tovary, ktoré nie sú na sklade vyžaduje spustenie množiny máp duálneho zápisu v prostredí. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Nevyhnutné mapy: Riešenie orchestrácie duálneho zápisu

Nasledujúce mapy sú povinnými predpokladmi pre riešenie Project Operations. Uistite sa, že ste vo svojom prostredí spustili mapy uvedené v nasledujúcej tabuľke a všetky súvisiace mapové tabuľky.

| Mapa tabuľky | Počiatočná synchronizácia |
| --- | --- |
| Účtovná kniha (msdyn_ledgers) | Vyžaduje sa počiatočná synchronizácia pre mapu tabuľky a všetky predpoklady. Hlavné pre úvodnú synchronizáciu sú aplikácie Finance and Operations. |
| Právnické entity (cdm_companies) | Nevyžaduje sa. Systém vyplní túto entitu automaticky, keď sú prostredia prepojené pomocou duálneho zápisu. |
| Customers V3 (účty) | Na zabezpečenie nie je potrebné. |
| Vendors V2 (msdyn_vendors) | Na zabezpečenie nie je potrebné. |

1. V zozname máp vyberte mapu Účtovná kniha **(msdyn\_ledgers)** so všetkými predpokladmi a začiarknite políčko **Počiatočná synchronizácia**. V poli **Predloha pre počiatočnú synchronizáciu** stlačte možnosť **Aplikácie Finance and Operations** pre mapu hlavnej knihy aj všetky mapy nevyhnutných podmienok. Vyberte položku **Spustiť**.

![Synchronizácia máp účtovnej knihy.](media/DW6.png)

2. Rovnakým spôsobom postupujte pre všetky zostávajúce mapové tabuľky uvedené v tabuľke vyššie. Neoznačujte pole **Počiatočná synchronizácia** pri spustení týchto máp.

## <a name="project-operations-dual-write-maps"></a>Duálny zápis máp Project Operations

Nasledujúce mapy sú povinnými pre riešenie Project Operations. Verzie máp duálneho zápisu sú uvedené počnúc aktualizáciou Project Operations z mája 2021, verzia 4.10.0.186.

| **Mapa entity** | **Najnovšia verzia** | **Počiatočná synchronizácia** |
| --- | --- | --- |
| Integračná entita pre transakčné vzťahy projektu (msdyn\_transactionconnections) | 1.0.0.0 | Na zabezpečenie nie je potrebné. |
| Hlavičky kontraktov projektu (zákazky odberateľa) | 1.0.0.1 | Na zabezpečenie nie je potrebné. |
| Riadky zmlúv projektu (salesorderdetails) | 1.0.0.0 | Na zabezpečenie nie je potrebné. |
| Zdroj financovania projektu (msdyn_projectcontractsplitbillingrules) | 1.0.0.2 | Na zabezpečenie nie je potrebné. |
| Tabuľka integrácie Project Operations pre materiálové odhady (msdyn\_estimatelines) | 1.0.0.0 | Na zabezpečenie nie je potrebné. |
| Návrhy projektovej faktúry V2 (faktúry) | 1.0.0.3 | Na zabezpečenie nie je potrebné. |
| Skutočné hodnoty integrácie Project Operations (msdyn_actuals) | 1.0.0.14 | Na zabezpečenie nie je potrebné. |
| Míľniky riadka zmluvy integrácie Project Operations (msdyn_contractlinescheduleofvalues) | 1.0.0.4 | Na zabezpečenie nie je potrebné. |
| Integrácia entity Project Operations pre odhady nákladov (msdyn_estimatelines) | 1.0.0.2 | Na zabezpečenie nie je potrebné. |
| Entita integrácie Project Operations pre odhady hodín (msdyn_resourceassignments) | 1.0.0.5 | Na zabezpečenie nie je potrebné. |
| Entita exportu kategórií výdavkov integrácie projektu Project Operations (msdyn_expensecategories) | 1.0.0.1 | Na zabezpečenie nie je potrebné. |
| Entita exportu výdavkov projektu integrácie Project Operations (msdyn_expenses) | 1.0.0.2 | Na zabezpečenie nie je potrebné. |
| Entita exportu faktúr dodávateľa integrácie Project Operations (msdyn_projectvendorinvoices) | 1.0.0.0 | Na zabezpečenie nie je potrebné. |
| Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.1 | Na zabezpečenie nie je potrebné. |
| Roly projektových zdrojov pre všetky spoločnosti (bookableresourcecategories) | 1.0.0.1 | Vyžaduje počiatočnú synchronizáciu pre mapu tabuľky na synchronizáciu rolí prostriedkov projektového manažéra a člena tímu, ktoré sú vyplnené v prostredí Dynamics 365 Dataverse počas vytvárania opravných položiek. Dataverse je hlavným zdrojom počiatočnej synchronizácie. |
| Projektové úlohy (msdyn_projecttasks) | 1.0.0.4 | Na zabezpečenie nie je potrebné. |
| Kategórie projektových transakcií (msdyn_transactioncategories) | 1.0.0.0 | Na zabezpečenie nie je potrebné. |
| Projekty V2 (msdyn_projects) | 1.0.0.2 | Na zabezpečenie nie je potrebné. |

Uvedené mapy spustíte vykonaním nasledujúcich krokov.

1. Povoľte role prostriedkov projektu pre tabuľkovú mapu **všetky spoločnosti (bookableresourcecategories)**, pretože táto mapa vyžaduje počiatočnú synchronizáciu. V poli **Predloha pre počiatočnú synchronizáciu** stlačte možnosť **Common Data Service**. 

 ![Synchronizácia mapy tabuliek rolí zdrojov.](media/6ResourceInitialSync.jpg)

 Počkajte, kým nebude stav mapy **Spustené** a až potom prejdite na ďalší krok.

2. Vyberte všetky zostávajúce požadované mapy. Môžete ich filtrovať v zozname máp duálneho zápisu pomocou kľúčového slova **Projekt** pri hľadaní v pravom hornom rohu. Môžete vybrať všetky mapy a potom ich spustiť. Viac informácií nájdete v časti [Správa viacerých mapových tabuliek](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Nezabudnite tiež povoliť a spustiť súvisiace mapy entít.

### <a name="project-operations-dual-write-map-versions"></a>Verzie máp duálneho zápisu v aplikácii Project Operations

Vždy používajte najnovšiu verziu mapy vo vašom prostredí. Niektoré funkcie a možnosti nemusia fungovať správne, ak existuje niektorá z nasledujúcich podmienok:

- Mapa nie je aktivovaná.
- Najnovšia verzia mapy nie je aktivovaná. 
- Súvisiace tabuľkové mapy nie sú aktivované.

Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy môžete aktivovať výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, musíte znova použiť zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).
