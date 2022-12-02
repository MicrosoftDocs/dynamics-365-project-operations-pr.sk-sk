---
title: Čo je nové v máji 2021 – Project Operations, čiastočné nasadenie
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Project Operations Lite, z mája 2021.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: a5d67159b732e0309e03c64fb6dadcc7b8cbff51
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934201"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Čo je nové v máji 2021 – Project Operations, čiastočné nasadenie

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

   - Project Operations v prostredí Dataverse verzie 4.10.0.186.

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

V tomto vydaní sú zahrnuté nasledujúce funkcie:

- [Režimy plánovania](../../project-management/scheduling-modes.md): Projektoví manažéri teraz môžu definovať, či sa má projekt riadiť pomocou režimu plánovania s fixným trvaním, fixnou prácou alebo fixnými jednotkami.

## <a name="quality-updates"></a>Aktualizácie kvality

| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2224568 | Pridaná logika na povolenie prispôsobení, ktoré zahŕňajú vyvolanie doplnku na potvrdenie faktúry. |
| Fakturácia a tvorba cien | 2101098 | Vylepšili sme logiku predvolených polí faktúry pro forma. Patria sem polia **Zasielacia adresa**, **Fakturovať na meno** a **Platobné podmienky**. Polia sú teraz predvolene vybraté z príslušného záznamu zákazníka o projektovej zmluve. |
| Fakturácia a tvorba cien | 2021413 | Aktualizované polia **Skutočné náklady** a **Predaj** v entite **Úloha** zahŕňajú hodnoty predaja z nefakturovaných a fakturovaných výdavkov za úlohy. |
| Fakturácia a tvorba cien | 2182110 | Pri kopírovaní projektovej zmluvy sa ID riadku zmluvy regeneruje v cieľovej projektovej zmluve, aby sa zabezpečilo, že je jedinečné. |
| Správa príležitostí | 2186741 | Pridané overovania na zabezpečenie, že pole **Pôvod** a typ transakcie nie je možné aktualizovať o podrobnosti riadka existujúcej cenovej ponuky. |
| Správa príležitostí | 2191353 | Tvorba medzníkov sa nesmie povoliť na riadku zmluvy s časom a materiálom. |
| Správa príležitostí | 2216956 | Opravené problémy s **aktualizáciou cien**. |
| Plánovanie a sledovanie | 2182979 | Vylepšená funkcia kopírovania projektu, aby sa zabezpečilo kopírovanie riadkov odhadu výdavkov z pôvodného projektu. |
| Plánovanie a sledovanie | 2184144 | Vylepšená funkcia kopírovania projektu, aby sa zabezpečilo kopírovanie názvu pozície zdroja z pôvodného projektu. |
| Plánovanie a sledovanie | 2184799 | Sprísnená kontrola pri kopírovaní projektu, ktorá zabezpečí, že odhadovaný dátum začatia nebude možné zmeniť, keď prebieha kopírovanie. |
| Plánovanie a sledovanie | 2185134 | Počas kopírovania projektu je odhadovaný dátum začatia cieľového projektu nastavený na dnešný dátum. |
| Plánovanie a sledovanie | 2196373 | Zaistí, aby sa pri kopírovaní projektu v rámci projektového tímu neduplikovali záznamy projektového manažéra a člena tímu. |
| Plánovanie a sledovanie | 2211833 | Priradenia zdrojov sa skopírujú z úlohy zdrojového projektu do cieľového projektu. |
| Plánovanie a sledovanie | 2186541 | Opravené problémy v mriežke **Odhady** pri zoskupovaní podľa **zdrojov**. |
| Plánovanie a sledovanie | 2166906 | Kategória transakcie z úlohy musí byť skopírovaná do entity **Priradenie zdroja**. |
| Správa zdrojov | 2125362 | Opravené problémy s vytváraním všeobecného člena tímu pomocou metódy prideľovania podľa hodín. |
| Čas a výdavky | 2113603 | Opravený problém súvisiaci s prispôsobením pri odstraňovaní atribútov zo stránky **Časový záznam**. Systém teraz pred prístupom k atribútu pomocou skriptu skontroluje, či atribút na stránke existuje. |
| Čas a výdavky | 2204377 | Po výbere **Kopírovať týždeň** sa musia skopírované časové rozvrhy zobraziť automaticky. |
| Čas a výdavky | 2209059 | Pole **Stav** je možné upraviť pre časové rozvrhy Dynamics 365 Field Service. |
