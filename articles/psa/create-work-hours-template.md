---
title: Vytvorenie šablóny pracovnej doby
description: Táto téma opisuje postup vytvorenia šablóny pracovných hodín v Project Service.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 5788378c7e015c4b11182aaf427aca7d1da48b40
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598967"
---
# <a name="create-a-work-hours-template-project-service"></a>Vytvorenie šablóny pracovných hodín (Project Service)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

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
3. Stlačte kartu **Pracovný čas** na karte zdroja a vykonajte pokyny v priečinku v časti [Nastavenie pracovnej doby zdroja](/dynamics365/field-service/set-work-hours-resource) a nakonfigurujte pravidlá kalendára.

**Vytvorí novú šablónu kalendára**

1. Prejdite do ponuky **Nastavenia** \> **Šablóna kalendára**.
2. Stlačte možnosť **Nový** a zadajte názov, popis a prostriedok šablóny.


> [!NOTE]
> Keď sa na prostriedok odkazuje v šablóne kalendára, kópia kalendára prostriedku je spojená so šablónou kalendára. Ak dôjde k zmene pracovného času skopírovanej šablóny, tieto zmeny sa nezanesú do šablóny kalendára.


### <a name="see-also"></a>Pozrite si tiež  
 [Nastavenie zdrojov](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
