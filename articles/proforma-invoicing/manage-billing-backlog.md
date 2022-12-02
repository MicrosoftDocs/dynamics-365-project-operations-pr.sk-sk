---
title: Správa backlogu pre fakturáciu
description: Tento článok poskytuje informácie o tom, ako zobraziť a pracovať s backlogom pre fakturáciu v Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5be05639650bb5b9d646067e8d83bada60824081
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929397"
---
# <a name="manage-billing-backlog"></a>Správa backlogu pre fakturáciu

**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

Dynamics 365 Project Operations má vyhradené zobrazenia, ktoré pomáhajú spravovať backlog pre fakturáciu. Ak chcete spravovať backlog pre fakturáciu, vyberte odkazy v časti **Fakturácia** v rámci oblasti **Predaj**. 

Dostupné sú nasledujúce zobrazenia:

- Preddavky a zálohy
- Dostupné preddavky a zálohy
- Medzníky pevných cien
- Backlog pre fakturáciu času a materiálu

## <a name="retainers-and-advances"></a>Preddavky a zálohy

Zobrazenie **Preddavky a zálohy** obsahuje zoznam preddavkov a záloh vo všetkých zmluvách o projekte. Po zaúčtovaní preddavku alebo zálohy bude suma zálohy k dispozícii na použitie.

## <a name="available-retainers-and-advances"></a>Dostupné preddavky a zálohy

Zobrazenie **Dostupné preddavky a zálohy** obsahuje zoznam všetkých dostupných preddavkov a záloh vo všetkých zmluvách o projekte. Po zaúčtovaní preddavku alebo zálohy bude suma zálohy k dispozícii na použitie a pridá sa do zoznamu. Keď sa množstvo použitých preddavkov alebo záloh úplne vyčerpá, odstráni sa zo zoznamu.

## <a name="fixed-price-milestones"></a>Medzníky pevných cien

Zobrazenie **Medzníky pevných cien** obsahuje zoznam všetkých medzníkov pevných cien vo všetkých riadkoch zmlúv o projekte. Z tohto zobrazenia je možné označiť jeden alebo viac medzníkov ako **Pripravené na fakturáciu** alebo **Nepripravené na fakturáciu**. Označenie medzníka ako **Pripravené na fakturáciu** ho sprístupní na zaradenie na koncept faktúry.

Keď majú riadky zmluvy pre viacerých zákazníkov metódu fakturácie s pevnou cenou, vytvorí sa medzník pre každého zákazníka na riadku zmluvy. Medzník je možné vytvoriť a potom rozdeliť na jednotlivé záznamy medzníkov špecifické pre zákazníkov. Toto rozdelenie je interné a v súlade s rozdelením fakturačných percentuálnych podielov definovaných pre každého zákazníka na riadku zmluvy. V zobrazení **Medzníky pevných cien** uvidíte jednotlivé záznamy medzníkov špecifické pre zákazníkov. Každý z týchto medzníkových záznamov možno označiť ako **Pripravené na fakturáciu** osobitne od tohto zobrazenia. Keď je jeden alebo viac súvisiacich medzníkov označí ako **Pripravené na faktúru**, stav hlavičky sa aktualizuje na **Prebieha** z **Nezačaté**. Keď sú fakturované všetky medzníky, stav hlavičky medzníka sa aktualizuje na **Dokončené**.

Medzník v koncepte faktúry sa zobrazuje v tomto zobrazení so stavom fakturácie **Bola vytvorená faktúra pre zákazníka**. Po potvrdení konceptu faktúry sa stav fakturácie v zázname aktualizuje na **Bola uverejnená faktúra pre zákazníka**. 

> [!NOTE] 
> Neaktualizujte túto hodnotu stavu pomocou vlastného kódu. Aplikácia Project Operations nefunguje správne, keď sa tieto hodnoty stavu aktualizujú pomocou vlastného kódu.

## <a name="time-and-material-billing-backlog"></a>Backlog pre fakturáciu času a materiálu

Zobrazenie **Backlog pre fakturáciu času a materiálu** obsahuje zoznam všetkých nevyfakturovaných skutočných predajov vo všetkých projektových zmluvách v systéme, ktoré neboli fakturované. V tomto zobrazení možno označiť jeden alebo viacero nevyfakturovaných predajných skutočných hodnôt ako **Pripravené na fakturáciu** alebo **Nepripravené na fakturáciu**. Označenie nevyfakturovanej predajnej skutočnej hodnoty ako **Pripravené na fakturáciu** ju sprístupní na vloženie do konceptu faktúry.

Nevyfakturované skutočné predaje so stavom **Nesmie sa prekročiť** ako **Neúspešné** nemožno označiť ako **Pripravené na fakturáciu**. Ak je potrebné skutočné hodnoty označiť ako **Pripravené na fakturáciu**, resetujte stav ďalších skutočných hodnôt na riadku zmluvy, ktoré sú potvrdené, a potom prehodnoťte stav **Nesmie sa prekročiť**.

Ak riadky zmluvy pre viacerých zákazníkov majú časovú a materiálovú metódu fakturácie, po schválení času a výdavkov sa vytvorí jeden nefakturovaný skutočný predaj pre každého zákazníka na riadku zmluvy podľa percentuálneho podielu fakturácie definovaného pre každého zo zákazníkov. V zobrazení **Backlog pre fakturáciu času a materiálu** uvidíte tieto jednotlivé nefakturované skutočné predaje špecifické pre zákazníkov. Každý z týchto záznamov nevyfakturovaných predajných skutočných hodnôt možno označiť ako **Pripravené na fakturáciu** osobitne od tohto zobrazenia.

Skutočný fakturovaný predaj, ktorý je na koncepte faktúry, sa zobrazuje v tomto zobrazení so stavom fakturácie **Bola vytvorená faktúra pre zákazníka**. Po potvrdení konceptu faktúry sa stav fakturácie v tomto zázname aktualizuje na **Bola uverejnená faktúra pre zákazníka**. 

> [!NOTE] 
> Neaktualizujte túto hodnotu stavu pomocou vlastného kódu. Aplikácia Project Operations nefunguje správne, keď sa tieto hodnoty stavu aktualizujú pomocou vlastného kódu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
