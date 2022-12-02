---
title: Čo je nové v marci 2022 – nasadenie aplikácie Project Operations Lite
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní nasadenia Project Operations lite z marca 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 321d59568bfd33bb00a1500afe514fbecf9a0250
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934247"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Čo je nové v marci 2022 – nasadenie aplikácie Project Operations Lite

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.30.0.99

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

- Subdodávateľské zmluvy Vytváranie faktúr dodávateľa a skúsenosti s párovaním

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Čas a výdavky | 2388011 | Počas hromadného schvaľovania sa zobrazujú predkladateľom časových položiek komentáre o odmietnutí. |
| Plánovanie a sledovanie projektu | 2495294 | Podrobnosti projektu sa nesmú dať upravovať na stránke **Podrobnosti úlohy**. |
| Fakturácia a tvorba cien | 2499605 | Zmluvné míľniky, ktoré sú vytvorené z míľnikov cenových ponúk, sú nesprávne označené ako len na čítanie. |
| Plánovanie a sledovanie projektu | 2506050 | Ak nedôjde k žiadnej zmene na uloženie, množina operácií zostane nevybavená jednu hodinu. Množina je potom falošne označená ako **Nepodarilo sa**, pričom by mala byť dokončená okamžite. |
| Fakturácia a tvorba cien | 2507401 | Predvolené zmluvné jednotky sú v projektoch nesprávne zadané z dôvodu nesprávneho ukladania do vyrovnávacej pamäte. |
| Fakturácia a tvorba cien | 2541660 | **Overenie vytvorenia predajnej objednávky** v duálnom zápise by malo byť iba pre zákazky založené na projekte. |
| Fakturácia a tvorba cien | 2552745 | Daň sa nerozdeľuje medzi zákazníkov, ktorí si nastavili pravidlá rozdelenej fakturácie. |
| Fakturácia a tvorba cien | 2558859 | Vylepšené chybové hlásenia pri nastavovaní cenových dimenzií. |
| Fakturácia a tvorba cien | 2558933 | **Import z odhadov projektu** zlyhá, keď sa **msdyn\_project** pridá ako cenová dimenzia. |
| Fakturácia a tvorba cien | 2559101 | Odstránenie parametrov projektu nie je blokované a spôsobuje problémy. |
| Správa príležitostí | 2570390 | Doplnok s duálnym zápisom vynucuje typ obchodného vzťahu pre cenové ponuky, objednávky a príležitosti **Zákazník**, aj keď tento typ obchodného vzťahu nie je správny. |
| Fakturácia a tvorba cien | 2586097 | Skutočné rozdelené fakturované náklady sa nestornujú, keď je projekt odstránený z riadku projektovej zmluvy. |
| Fakturácia a tvorba cien | 2589619 | Daň zo zapísaného materiálu sa prenáša do skutočných nevyfakturovaných predajov a faktúry. |
| Správa príležitostí | 2594015 | Cenovú ponuku nemožno uzavrieť ako získanú pre zákazníkov, ktorí majú platobné podmienky **Net60** . |
| Plánovanie a sledovanie projektu | 2595841 | V Project for the Web sa používateľom zobrazí chybové hlásenie o chýbajúcom **msdyn\_actualstart** keď vytvoria novú požiadavku na zdroj. |
| Čas a výdavky | 2602511 | Pole **Odmietnuté používateľom** pre časové záznamy zobrazuje **Systém** namiesto menovaného používateľa ako odmietajúceho. |
| Čas a výdavky | 2602528 | Schvaľovateľ projektu môže schváliť čas na projektoch, kde nie je uvedený ako schvaľovateľ. |
| Fakturácia a tvorba cien | 2608550 | Opravnú faktúru je možné potvrdiť aj vtedy, ak nedošlo k žiadnym zmenám oproti originálu. |

## <a name="removed-and-deprecated-features"></a>Odstránené a zastarané funkcie

Článok [Odstránené alebo zastarané funkcie v Project Operations](../../whats-new/removed-depreciated-features-project.md) popisuje funkcie, ktoré boli odstránené alebo ktorých podpora bola ukončená pre Dynamics 365 Project Operations.

- Odstránená funkcia už v produkte nie je k dispozícii.
- Zastaraná funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Oznámenie o ukončení podpory sa zobrazí v článku [Odstránené alebo zastarané funkcie v Project Operations](../../whats-new/removed-depreciated-features-project.md) 12 mesiacov pred odstránením akejkoľvek funkcie z produktu.
