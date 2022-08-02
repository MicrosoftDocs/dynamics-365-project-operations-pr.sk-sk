---
title: Čo je nové júni 2022 – nasadenie Project Operations Lite
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft z júna 2022 Dynamics 365 Project Operations lite nasadenie.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 8313288ecf7ff1350cd82c62d3d0c291d8a3ded4
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031212"
---
# <a name="whats-new-june-2022---project-operations-lite-deployment"></a>Čo je nové júni 2022 – nasadenie Project Operations Lite

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.43.0.77 alebo 4.43.0.119

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Subdodávky | 2708885 | Opravené chybové hlásenie, ktoré sa zobrazuje, keď používateľ vytvorí záznam hlavičky rezervácie rezervovateľného zdroja, kde nie je vyplnený žiadny rezervovateľný zdroj. |
| Plánovanie a sledovanie projektu | 2629441 | Opravená logika spúšťania pracovného toku, aby sa zabránilo nekonečnej slučke pri aktualizácii projektových úloh. |
| Čas a výdavky | 2641209 | Import časových záznamov z úloh/rezervácií si musí zachovať referenciu na rezervovateľný zdroj. |
| Plánovanie a sledovanie projektu | 2651148 | Hlavička projektového dokumentu musí byť strážená.|
| Plánovanie a sledovanie projektu | 2653145 | Pridané overenia, aby sa zabezpečilo, že nie je možné vytvoriť záznam projektu, ktorý má v názve neplatné znaky. |
| Čas a výdavky | 2654710 | Opravené filtrovanie na **Schválenia** stránku. |
| Fakturácia a tvorba cien | 2667805 | Pridané overenia, ktoré pomôžu zabrániť vytváraniu skutočných fakturovaných predajov, ak neexistujú podporné nevyúčtované skutočné predaje. |
| Fakturácia a tvorba cien | 2668378 | Pridané overenia, ktoré pomôžu zabrániť pridaniu vlastnej cenovej dimenzie, pokiaľ nie je vyplnený logický názov a názov poľa. |
| Čas a výdavky | 2700428 | Vylepšená logika schvaľovania, aby sa zabezpečilo, že ostatné sady schvaľovania pre projekt môžu byť spracované, aj keď jedna zo sád schvaľovania uviazla v systémových úlohách. |
