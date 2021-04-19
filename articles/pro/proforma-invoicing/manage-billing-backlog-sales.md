---
title: Správa backlogu pre fakturáciu projektu
description: Táto téma poskytuje informácie o rôznych zobrazeniach, ktoré je možné použiť pri správe backlogu pre fakturáciu na projektoch.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25dc9cff6aeb6daed9a27ba843a74b892ca4751c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867015"
---
# <a name="manage-project-billing-backlog"></a>Správa backlogu pre fakturáciu projektu 

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations má vyhradené zobrazenia, ktoré pomáhajú spravovať backlog pre fakturáciu. Ak chcete spravovať backlog pre fakturáciu, vyberte odkazy v časti **Fakturácia** v rámci oblasti **Predaj**. 

Dostupné sú nasledujúce zobrazenia:

- Preddavky a zálohy
- Dostupné preddavky a zálohy
- Medzníky pevných cien
- Backlog pre fakturáciu produktov
- Backlog pre fakturáciu času a materiálu

## <a name="retainers-and-advances"></a>Preddavky a zálohy

Zobrazenie **Preddavky a zálohy** obsahuje všetky preddavky a zálohy vo všetkých projektových zmluvách v systéme. Po zaúčtovaní preddavku alebo zálohy bude suma zálohy k dispozícii na použitie.

## <a name="available-retainers-and-advances"></a>Dostupné preddavky a zálohy

Zobrazenie **Dostupné preddavky a zálohy** obsahuje všetky dostupné preddavky a zálohy vo všetkých projektových zmluvách v systéme. Po zaúčtovaní preddavku alebo zálohy bude suma zálohy k dispozícii na použitie a pridá sa do zoznamu. Po úplnom vyčerpaní preddavku alebo zálohy dôjde k ich odstráneniu zo zoznamu.

## <a name="fixed-price-milestones"></a>Medzníky pevných cien

Zobrazenie **Medzníky pevných cien** uvádza všetky medzníky pevných cien vo všetkých riadkoch projektových zmlúv v systéme. V tomto zobrazení možno označiť jeden alebo viac medzníkov ako **Pripravené na fakturáciu** alebo **Nepripravené na fakturáciu**. Označenie medzníka ako **Pripravené na fakturáciu** ho sprístupní na zaradenie na koncept faktúry.

Keď majú riadky zmluvy pre viacerých zákazníkov metódu fakturácie s pevnou cenou, vytvorí sa medzník pre každého zákazníka na riadku zmluvy. Medzník je možné vytvoriť a potom rozdeliť na jednotlivé záznamy medzníkov špecifické pre zákazníkov. Toto rozdelenie je interné a v súlade s rozdelením fakturačných percentuálnych podielov definovaných pre každého zákazníka na riadku zmluvy. V zobrazení **Medzníky pevných cien** uvidíte jednotlivé záznamy medzníkov špecifické pre zákazníkov. Každý z týchto medzníkových záznamov možno označiť ako **Pripravené na fakturáciu** osobitne od tohto zobrazenia. Keď sú jeden alebo viac súvisiacich rozdelení medzníkov označené ako **Pripravené na fakturáciu**, stav hlavičky sa aktualizuje na **Prebieha** z **Nezačaté**. Keď sú fakturované všetky rozdelenia medzníkov, stav hlavičky medzníka sa aktualizuje na **Dokončené**.

Medzník v koncepte faktúry sa zobrazuje v tomto zobrazení so stavom fakturácie **Bola vytvorená faktúra pre zákazníka**. Po potvrdení konceptu faktúry sa stav fakturácie v zázname aktualizuje na **Bola uverejnená faktúra pre zákazníka**. Neaktualizujte túto hodnotu stavu pomocou vlastného kódu. Aplikácia Project Operations nefunguje správne, keď sa tieto hodnoty stavu aktualizujú pomocou vlastného kódu.

## <a name="product-billing-backlog"></a>Backlog pre fakturáciu produktov

Zobrazenie **Backlog pre fakturáciu produktov** obsahuje všetky riadky zmlúv založených na produktoch vo všetkých projektových zmluvách v systéme. V tomto zobrazení možno označiť jeden alebo viac riadkov zmlúv založených na produktoch ako **Pripravené na fakturáciu** alebo **Nepripravené na fakturáciu**. Označenie riadka zmluvy založenej na produkte ako **Pripravené na fakturáciu** ho sprístupní na zaradenie na koncept faktúry.

Riadok zmluvy založenej na produkte, ktorý je na koncepte faktúry, je v tomto zobrazení zobrazený so stavom fakturácie **Bola vytvorená faktúra pre zákazníka**. Po potvrdení konceptu faktúry sa stav fakturácie v tomto zázname aktualizuje na **Bola uverejnená faktúra pre zákazníka**. Neaktualizujte túto hodnotu stavu pomocou vlastného kódu. Aplikácia Project Operations nefunguje správne, keď sa tieto hodnoty stavu aktualizujú pomocou vlastného kódu.

## <a name="time-and-material-billing-backlog"></a>Backlog pre fakturáciu času a materiálu

Zobrazenie **Backlog pre fakturáciu času a materiálu** obsahuje zoznam všetkých nevyfakturovaných skutočných predajov vo všetkých projektových zmluvách v systéme, ktoré neboli fakturované. V tomto zobrazení možno označiť jeden alebo viacero nevyfakturovaných predajných skutočných hodnôt ako **Pripravené na fakturáciu** alebo **Nepripravené na fakturáciu**. Označenie nevyfakturovanej predajnej skutočnej hodnoty ako **Pripravené na fakturáciu** ju sprístupní na vloženie do konceptu faktúry.

Nevyfakturované skutočné predaje so stavom **Nesmie sa prekročiť** ako **Neúspešné** nemožno označiť ako **Pripravené na fakturáciu**. Ak je potrebné skutočné hodnoty označiť ako **Pripravené na fakturáciu**, obnovte stav ostatných skutočných hodnôt na riadku zmluvy, ktoré sú potvrdené. a potom prehodnoťte stav **Nesmie sa prekročiť**.

Ak riadky zmluvy pre viacerých zákazníkov majú časovú a materiálovú metódu fakturácie, po schválení času a výdavkov sa vytvorí jeden nefakturovaný skutočný predaj pre každého zákazníka na riadku zmluvy podľa percentuálneho podielu fakturácie definovaného pre každého zo zákazníkov. V zobrazení **Backlog pre fakturáciu času a materiálu** uvidíte tieto jednotlivé nefakturované skutočné predaje špecifické pre zákazníkov. Každý z týchto záznamov nevyfakturovaných predajných skutočných hodnôt možno označiť ako **Pripravené na fakturáciu** osobitne od tohto zobrazenia.

Skutočný nefakturovaný predaj, ktorý je na koncepte faktúry, je v tomto zobrazení zobrazený so stavom fakturácie **Bola vytvorená faktúra pre zákazníka**. Po potvrdení konceptu faktúry sa stav fakturácie v tomto zázname aktualizuje na **Bola uverejnená faktúra pre zákazníka**. Neaktualizujte túto hodnotu stavu pomocou vlastného kódu. Aplikácia Project Operations nefunguje správne, keď sa tieto hodnoty stavu aktualizujú pomocou vlastného kódu.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
