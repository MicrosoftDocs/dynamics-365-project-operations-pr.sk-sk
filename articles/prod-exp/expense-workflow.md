---
title: Pracovný postup riadenia výdavkov
description: Táto téma vysvetľuje, ako môžete použiť systém pracovného toku v Microsoft Dynamics 365 Financie, aby ste nastavili proces kontroly pre výkazy výdavkov v riadení výdavkov.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: johnmichalak
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3eb4d57194ce2dd7f80d75c2c765f1cfa48b0348
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684293"
---
# <a name="expense-management-workflow"></a>Pracovný postup riadenia výdavkov

Systém pracovného toku môžete použiť na nastavenie procesu kontroly výkazov výdavkov v správe výdavkov. Môžete nastaviť pracovný tok, ktorý pomocou nasledujúcich kritérií určuje, kto schvaľuje výkazy výdavkov:

- Hierarchia vykazovania zamestnancov a preddefinované limity schválenia
- Viacúrovňové schválenie, ktoré podporuje dočasných schvaľovateľov a konečného schvaľovateľa
- Finančné rozmery a zodpovednosť za projekt
- Priradenie konkrétnym používateľom alebo skupinám používateľov

Je možné vytvoriť schválenia pracovných postupov pre výkazy výdavkov, cestovné požiadavky, zálohy v hotovosti a vrátenie dane z pridanej hodnoty (DPH).

**Príklad**

Nasledujúci proces je príkladom pracovného toku správy výdavkov pre výkaz výdavkov.

1. Zamestnanec vytvorí a uloží výkaz výdavkov.
2. Zamestnanec predloží výkaz výdavkov na schválenie. Schvaľovateľ je identifikovaný na základe pravidiel, ktoré boli definované pri nastavovaní pracovného toku.
3. Schvaľovateľ dostane oznámenie, že výkaz výdavkov je pripravený na schválenie. Schvaľovateľ skontroluje výkaz výdavkov a overí, či sú splnené nasledujúce podmienky:

    - Výdavky neporušujú žiadne zásady týkajúce sa výdavkov. Ak výdavok porušuje zásady, schvaľovateľ overí, či správa o výdavkoch obsahuje platné obchodné odôvodnenie.
    - Elektronické potvrdenky sú pripojené k výkazu výdavkov.

4. Schvaľovateľ schvaľuje výkaz výdavkov.
5. Výkaz výdavkov je priradený koordinátorovi záväzkov na zverejnenie.
6. Podľa toho, či je nakonfigurované automatické zverejňovanie, dôjde k jednému z nasledujúcich krokov:

    - Ak je nakonfigurované automatické zverejňovanie, výkaz výdavkov sa spracuje na platbu a aktualizuje sa stav výkazu výdavkov.
    - Ak automatické zverejňovanie nie je nakonfigurované, koordinátor záväzkov overí, či boli odoslané všetky pôvodné potvrdenky a či sú potvrdenia zarovnané s výdavkami v prehľade výdavkov. Rovnako musia byť overené všetky daňové kódy, ktoré sú zadané vo výkaze výdavkov.

Po overení týchto požiadaviek sa zverejní výkaz výdavkov.

Po zverejnení výkazu výdavkov sa platba za výkaz výdavkov autorizuje a zamestnancovi preplatená suma.


[!INCLUDE[footer-include](../includes/footer-banner.md)]