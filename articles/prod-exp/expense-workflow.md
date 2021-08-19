---
title: Pracovný postup riadenia výdavkov
description: Táto téma vysvetľuje, ako môžete používať systém pracovných tokov v aplikácii Microsoft Dynamics 365 Finance na nastavenie procesu kontroly výkazov výdavkov v správe výdavkov.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c2a2cae435342139f32d1bb5d38d68acd920453f5e6f6551e1f6d57967d8053
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001315"
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