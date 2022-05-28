---
title: Čo je nové v marci 2022 – nasadenie aplikácie Project Operations Lite
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú dostupné vo vydaní zjednodušeného nasadenia Project Operations z marca 2022.
author: sigitac
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8a83491da1d312406dfb36f5ad214c307c15cfbf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583769"
---
# <a name="whats-new-march-2022---project-operations-lite-deployment"></a>Čo je nové v marci 2022 – nasadenie aplikácie Project Operations Lite

_Platí pre: Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma sa týka nasledujúcich komponentov a verzií Microsoftu Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.30.0.99

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

- Subdodávky: Vytváranie faktúr dodávateľa a porovnávanie skúseností

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Čas a výdavky | 2388011 | Počas hromadného schvaľovania zobrazte predkladateľom zadania času komentáre o odmietnutí. |
| Plánovanie a sledovanie projektu | 2495294 | Podrobnosti projektu nesmú byť upraviteľné na **Podrobnosti úlohy** stránku. |
| Fakturácia a tvorba cien | 2499605 | Zmluvné míľniky, ktoré sú vytvorené z cenových míľnikov, sú nesprávne označené ako len na čítanie. |
| Plánovanie a sledovanie projektu | 2506050 | Ak nedôjde k žiadnej zmene na uloženie, sada operácií zostane nevybavená jednu hodinu. Súprava je potom falošne označená ako **Nepodarilo sa**, pričom by mala byť dokončená okamžite. |
| Fakturácia a tvorba cien | 2507401 | Predvolené zmluvné jednotky sú v projektoch nesprávne zadané z dôvodu nesprávneho ukladania do vyrovnávacej pamäte. |
| Fakturácia a tvorba cien | 2541660 | **Overenie vytvorenia zákazky odberateľa** v duálnom zápise by malo byť iba pre zákazky založené na projekte. |
| Fakturácia a tvorba cien | 2552745 | Daň sa nerozdeľuje medzi zákazníkov, ktorí si nastavili pravidlá rozdelenej fakturácie. |
| Fakturácia a tvorba cien | 2558859 | Vylepšené chybové hlásenia pri nastavovaní dimenzií cien. |
| Fakturácia a tvorba cien | 2558933 | **Importovať z odhadov projektu** zlyhá, keď **msdyn\_ projektu** sa pridáva ako cenová dimenzia. |
| Fakturácia a tvorba cien | 2559101 | Odstránenie parametrov projektu nie je blokované a spôsobuje problémy. |
| Správa príležitostí | 2570390 | Zásuvný modul s dvojitým zápisom núti typ účtu na cenové ponuky, objednávky a príležitosti **Zákazník**, aj keď tento typ účtu nie je správny. |
| Fakturácia a tvorba cien | 2586097 | Skutočné rozdelené fakturované náklady nie sú stornované, keď je projekt odstránený z riadku projektovej zmluvy. |
| Fakturácia a tvorba cien | 2589619 | Daň zo zapísaného materiálu sa prenáša do skutočných nevyfakturovaných predajov a faktúry. |
| Správa príležitostí | 2594015 | Cenovú ponuku nemožno uzavrieť ako vyhratú pre zákazníkov, ktorí tak urobili **Net60** platobné podmienky. |
| Plánovanie a sledovanie projektu | 2595841 | V Project for the Web sa používateľom zobrazí chybové hlásenie o chýbajúcom **msdyn\_ skutočný štart** keď vytvoria novú požiadavku na zdroj. |
| Čas a výdavky | 2602511 | The **Odmietnuté používateľom** pole pre časové záznamy zobrazuje **systém** namiesto menovaného používateľa ako odmietajúceho. |
| Čas a výdavky | 2602528 | Schvaľovateľ projektu môže schváliť čas na projektoch, kde nie je uvedený ako schvaľovateľ. |
| Fakturácia a tvorba cien | 2608550 | Opravnú faktúru je možné potvrdiť aj vtedy, ak nedošlo k žiadnym zmenám oproti originálu. |

## <a name="removed-and-deprecated-features"></a>Odstránené a zastarané funkcie

The [Odstránené alebo zastarané funkcie v Project Operations](../../whats-new/removed-depreciated-features-project.md) téma popisuje funkcie, ktoré boli odstránené alebo zastarané Dynamics 365 Project Operations.

- Odstránená funkcia už v produkte nie je k dispozícii.
- Zastaraná funkcia nie je v aktívnom vývoji a môže byť odstránená v budúcej aktualizácii.

Oznámenie o ukončení podpory sa zobrazí v [Odstránené alebo zastarané funkcie v Project Operations](../../whats-new/removed-depreciated-features-project.md) tému 12 mesiacov pred odstránením akejkoľvek funkcie z produktu.
