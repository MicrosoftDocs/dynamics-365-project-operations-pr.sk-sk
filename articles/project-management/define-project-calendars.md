---
title: Definovanie kalendárov projektu
description: Táto téma poskytuje informácie o tom, ako použiť šablónu kalendára na projekt na sledovanie harmonogramu projektu.
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981319"
---
# <a name="define-project-calendars"></a>Definovanie kalendárov projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Ak chcete vytvoriť a spravovať projekt, musíte na projekt použiť šablónu kalendára. Šablóna kalendára definuje nasledujúce atribúty projektu:

- Pracovná doba vrátane času začiatku a konca
- Pracovné dni
- Výnimky z kalendára, napríklad dni pracovného pokoja

Šablóna kalendára, ktorá sa použije na projekt, je kópiou šablóny kalendára definovanej v nastaveniach vašej organizácie.

> [!NOTE]
> Ak zmeníte šablónu kalendára, tieto zmeny sa neprenesú na pracovnú dobu projektu. Pre zmenu pracovnej doby projektu je potrebné použiť novú šablónu.

Na vytvorenie šablóny kalendára pre vašu organizáciu existujú dve kľúčové požiadavky:

- Definujte požadovaný pracovný čas šablóny pomocou nového alebo existujúceho rezervovateľného zdroja.
- Vytvorte novú šablónu kalendára a priraďte ju k rezervovateľnému prostriedku.

**Definovať pracovný čas šablóny**

1. Prejdite do **Zdroje** \> **Zdroje**.
2. Vytvorte nový zdroj, ktorý bude odkazovať v šablóne kalendára, alebo vyberte existujúci zdroj.
3. Stlačte kartu **Pracovný čas** na karte zdroja a vykonajte pokyny v priečinku v časti [Nastavenie pracovnej doby zdroja](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) a nakonfigurujte pravidlá kalendára.

**Vytvorí novú šablónu kalendára**

1. Prejdite do ponuky **Nastavenia** \> **Šablóna kalendára**.
2. Stlačte možnosť **Nový** a zadajte názov, popis a prostriedok šablóny.

> [!NOTE]
> Keď sa na prostriedok odkazuje v šablóne kalendára, kópia kalendára prostriedku je spojená so šablónou kalendára. Ak dôjde k zmene pracovného času skopírovanej šablóny, tieto zmeny sa nezanesú do šablóny kalendára.

Šablónu práce teraz môžete priradiť k šablóne kalendára projektu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

