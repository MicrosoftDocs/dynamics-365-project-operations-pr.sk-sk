---
title: Správa backlogu pre fakturáciu
description: Táto téma poskytuje informácie o tom, ako zobraziť a pracovať s backlogom pre fakturáciu v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/20/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c3752abd26e760d27320d2b86079d84a967d53cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287752"
---
# <a name="manage-the-billing-backlog"></a>Správa backlogu pre fakturáciu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations má dve vyhradené zobrazenia, ktoré pomáhajú využívať a spravovať backlog pre fakturáciu. K dispozícii sú možnosti **Medzníky pevnej ceny** a **Backlog pre fakturáciu podľa času a materiálu**. Ak chcete zvoliť zobrazenie, v oblasti **Predaj** aplikácie Project Operations, na ľavej navigačnej stránke, zvoľte **Fakturácia**. Sú tu uložené odkazy na backlogy pre fakturáciu.

## <a name="fixed-price-milestones"></a>Medzníky pevných cien

Toto zobrazenie zobrazuje všetky medzníky pevných cien vo všetkých riadkoch projektových zmlúv v systéme. V tomto zobrazení možno označiť jeden alebo viac medzníkov ako **Pripravené na fakturáciu** alebo **Nepripravené na fakturáciu**. Keď označíte medzník ako **Pripravené na fakturáciu**, medzník bude k dispozícii pre koncept faktúry.

Keď majú riadky zmluvy pre viacerých zákazníkov metódu fakturácie s pevnou cenou, vytvorí sa pre každého zákazníka v riadku zmluvy jeden medzník. Používateľ vytvorí medzník a tento medzník sa interne rozdelí na záznamy o zákazníkoch = špecifické medzníky podľa rozdelenia fakturačného percenta definovaného pre každého zákazníka v riadku zmluvy. V zobrazení **Medzníky s pevnou cenou** môžete vidieť jednotlivé medzníkové záznamy špecifické pre zákazníka. Každý z týchto medzníkových záznamov možno označiť ako **Pripravené na fakturáciu** osobitne od tohto zobrazenia. Keď je jeden alebo viac súvisiacich rozdelených medzníkov označených ako **Pripravené na fakturáciu**, stav v hlavičke sa zmení na **Prebieha** z **Nezačaté**. Po vyfakturovaní všetkých rozdelení medzníkov, stav v hlavičke medzníka sa zmení na **Dokončené**.

Medzník v koncepte faktúry sa zobrazuje v tomto zobrazení so stavom fakturácie **Bola vytvorená faktúra pre zákazníka**. Po potvrdení konceptu faktúry sa stav fakturácie v tomto zázname aktualizuje na **Bola uverejnená faktúra**. Aktualizácia tejto hodnoty stavu pomocou vlastného kódu sa neodporúča. Ak sa tieto hodnoty stavu aktualizujú pomocou vlastného kódu, aplikácia Project Operations nebude fungovať správne.

## <a name="time-and-material-billing-backlog"></a>Backlog pre fakturáciu času a materiálu

Toto zobrazenie obsahuje zoznam všetkých nevyfakturovaných predajných skutočných hodnôt, ktoré neboli vyfakturované vo všetkých projektových zmluvách v systéme. V tomto zobrazení možno označiť jeden alebo viacero nevyfakturovaných predajných skutočných hodnôt ako **Pripravené na fakturáciu** alebo **Nepripravené na fakturáciu**. Označenie nevyfakturovanej predajnej skutočnej hodnoty ako **Pripravené na fakturáciu** ju sprístupní na vloženie do konceptu faktúry.

Nevyfakturované predajné skutočné hodnoty, ktoré majú stav **Nesmie sa prekročiť** nastavený na **Neúspešné** nemožno označiť ako **Pripravené na fakturáciu**. Ak je potrebné tieto skutočné hodnoty ako také označiť, vynulujte stav ostatných skutočných hodnôt v riadku zmluvy, ktoré sú potvrdené, a potom vyhodnoťte stav **Nesmie sa prekročiť**.

V prípade riadkov zmluvy pre viacerých zákazníkov, ktoré majú metódu fakturácie času a materiálu, sa po schválení času a výdavkov vytvorí nevyfakturovaná predajná skutočná hodnota pre každého zákazníka v riadku zmluvy podľa percentuálneho rozdelenia fakturácie definovaného pre každého zákazníka v riadku zmluvy. V zobrazení **Backlog pre fakturáciu času a materiálu** uvidíte tieto jednotlivé nevyfakturované predajné skutočné hodnoty špecifické pre zákazníka. Každý z týchto záznamov nevyfakturovaných predajných skutočných hodnôt možno označiť ako **Pripravené na fakturáciu** osobitne od tohto zobrazenia.

Nevyfakturovaná predajná skutočná hodnota v koncepte faktúry sa zobrazuje v tomto zobrazení so **stavom fakturácie** **Bola vytvorená faktúra pre zákazníka**. Po potvrdení konceptu faktúry sa stav fakturácie v tomto zázname aktualizuje na **Bola uverejnená faktúra pre zákazníka**. Aktualizácia tejto hodnoty stavu, keď je v tomto stave, pomocou vlastného kódu sa neodporúča. Ak sa tieto hodnoty stavu aktualizujú pomocou vlastného kódu, aplikácia Project Operations nebude fungovať správne.


[!INCLUDE[footer-include](../includes/footer-banner.md)]