---
title: Čo je nové júni 2022 – nasadenie Project Operations Lite
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft z júna 2022 Dynamics 365 Project Operations lite nasadenie.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 2d773603abef7ab45d4d1c298e5553e57893294d
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959657"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Čo je nové júni 2022 – nasadenie Project Operations Lite

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.43.0.77

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Subdodávky | 2708885 | Opravené chybové hlásenie, ktoré sa zobrazuje, keď používateľ vytvorí záznam hlavičky rezervácie rezervovateľného zdroja, kde nie je vyplnený žiadny rezervovateľný zdroj. |
| Plánovanie a sledovanie projektu | 2629441 | Opravená logika spúšťania pracovného toku, aby sa zabránilo nekonečnej slučke pri aktualizácii projektových úloh. |
| Čas a výdavky | 2641209 | Import časových záznamov z úloh/rezervácií si musí zachovať referenciu na rezervovateľný zdroj. |
| Plánovanie a sledovanie projektu | 2651148 | Hlavička projektového dokumentu musí byť strážená.|
| Plánovanie a sledovanie projektu | 2653145 | Pridané overenia, aby sa zabezpečilo, že nie je možné vytvoriť záznam projektu, ktorý má v názve neplatné znaky. |
| Čas a výdavky | 2654710 | Opravené filtrovanie na **Schválenia** stránku. |
| Fakturácia a tvorba cien | 2667805 | Pridané overenia, ktoré pomáhajú zabrániť vytváraniu skutočných fakturovaných predajov, ak neexistujú podporné nevyúčtované skutočné predaje. |
| Fakturácia a tvorba cien | 2668378 | Pridané overenia, ktoré pomôžu zabrániť pridaniu vlastnej cenovej dimenzie, pokiaľ nie je vyplnený logický názov a názov poľa. |
| Čas a výdavky | 2700428 | Vylepšená logika schvaľovania, aby sa zabezpečilo, že ostatné sady schvaľovania pre projekt môžu byť spracované, aj keď jedna zo sád schvaľovania uviazne v systémových úlohách. |
