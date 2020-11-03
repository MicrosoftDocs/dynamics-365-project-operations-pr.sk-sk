---
title: Pracovný postup riadenia výdavkov
description: Táto téma vysvetľuje, ako môžete používať systém pracovných tokov v aplikácii Microsoft Dynamics 365 Finance na nastavenie procesu kontroly výkazov výdavkov v správe výdavkov.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084519"
---
# <a name="expense-management-workflow"></a>Pracovný postup riadenia výdavkov

[!include [banner](../includes/banner.md)]

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
