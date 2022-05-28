---
title: Čo je nové v apríli 2021 – Project Operations, čiastočné nasadenie
description: Táto téma poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Project Operations, čiastočné nasadenie, z apríla 2021.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 10d9498636d8c5f72b7544be4ec30f399d5e0311
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598139"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Čo je nové v apríli 2021 – Project Operations, čiastočné nasadenie

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

  - Project Operations v prostredí Dataverse verzie 4.9.0.221 

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

V tomto vydaní sú zahrnuté nasledujúce funkcie:

- Neskladované materiály pre projekty. Medzi kľúčové schopnosti patrí:
  - Odhad a naceňovanie neskladovaných materiálov počas predajného cyklu projektu. Viac informácií sa dozviete v článku [Nastavenie nákladových a predajných sadzieb pre katalógové produkty – čiastočné nasadenie](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Sledovanie použitia neskladovaných materiálov počas dodania projektu. Viac informácií sa dozviete v článku [Zaznamenanie využitia materiálu na projektoch a projektových úlohách](../../material/material-usage-log.md).
  - Fakturácia nákladov na použité neskladované materiály. Ďalšie informácie nájdete v článku [Správa backlogu pre fakturáciu – čiastočné nasadenie](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Nové rozhrania API v Dynamics 365 Dataverse umožňuje vytvárať, aktualizovať a mazať operácie s **Entitami plánovania**. Viac informácií sa dozviete v časti [Používanie rozhraní API na vykonávanie operácií s entitami plánovania](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Aktualizácie kvality

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2224568 | Pridaná logika na povolenie prispôsobení, ktoré zahŕňajú vyvolanie doplnku na potvrdenie faktúry. |
| Fakturácia a tvorba cien | 2101098 | Vylepšená logika predvolených polí faktúry pro forma: **Zasielacia adresa**, **Fakturačné meno** a **Platobné podmienky** teraz získavajú predvolené údaje z príslušného záznamu zákazníka projektovej zmluvy. |
| Fakturácia a tvorba cien | 2021413 | Aktualizované polia **Skutočné náklady** a **Predaj** v entite **Úloha** zahŕňajú hodnoty predaja z nefakturovaných a fakturovaných výdavkov za úlohy. |
| Fakturácia a tvorba cien | 2182110 | Pri kopírovaní projektovej zmluvy sa ID riadku zmluvy regeneruje v cieľovej projektovej zmluve, aby sa zabezpečilo, že je jedinečné. |
| Správa príležitostí | 2186741 | Pridané overovania na zabezpečenie, že pole **Pôvod** a **Typ transakcie** nie je možné aktualizovať o podrobnosti riadka existujúcej cenovej ponuky. |
| Správa príležitostí | 2191353 | Medzníky sa nesmú vytvárať na riadku zmluvy s časom a materiálom. |
| Správa príležitostí | 2216956 | Opravené problémy s **aktualizáciou cien**. |
| Plánovanie a sledovanie | 2182979 | Vylepšená funkcia kopírovania projektu, aby sa zabezpečilo kopírovanie riadkov odhadu výdavkov z pôvodného projektu. |
| Plánovanie a sledovanie | 2184144 | Vylepšená funkcia kopírovania projektu, aby sa zabezpečilo kopírovanie názvu pozície zdroja z pôvodného projektu. |
| Plánovanie a sledovanie | 2184799 | Kópia projektu: Sprísnená kontrola, ktorá zabezpečí, že odhadovaný dátum začatia nebude možné zmeniť, keď prebieha kopírovanie. |
| Plánovanie a sledovanie | 2185134 | Kópia projektu: Odhadovaný dátum začatia cieľového projektu je nastavený na dnešný dátum. |
| Plánovanie a sledovanie | 2196373 | Kópia projektu: Zaistí, aby sa v projektovom tíme neduplikovali záznamy projektového manažéra a člena tímu. |
| Plánovanie a sledovanie | 2211833 | Kópia projektu: Priradenia zdrojov sa skopírujú z úlohy zdrojového projektu do cieľového projektu. |
| Plánovanie a sledovanie | 2186541 | Opravené problémy v mriežke **Odhady** pri zoskupovaní podľa zdrojov. |
| Plánovanie a sledovanie | 2166906 | Kategória transakcie z úlohy musí byť skopírovaná do entity **Priradenie zdroja**. |
| Správa zdrojov | 2125362 | Opravené problémy s vytváraním všeobecného člena tímu pomocou metódy prideľovania podľa hodín. |
| Čas a výdavky | 2113603 | Opravený problém súvisiaci s prispôsobením pri odstraňovaní atribútov zo stránky **Zadanie času**. Systém teraz pred prístupom pomocou skriptu skontroluje, či atribút na stránke existuje. |
| Čas a výdavky | 2204377 | Po výbere **Kopírovať týždeň** počas zadávania času sa musia skopírované časové rozvrhy zobraziť automaticky. |
| Čas a výdavky | 2209059 | Pole **Stav** je možné upraviť pre časové rozvrhy Dynamics 365 Field Service. |
