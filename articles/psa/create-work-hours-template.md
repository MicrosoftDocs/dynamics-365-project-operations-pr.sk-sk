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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997215"
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
3. Stlačte kartu **Pracovný čas** na karte zdroja a vykonajte pokyny v priečinku v časti [Nastavenie pracovnej doby zdroja](/dynamics365/field-service/set-work-hours-resource.md) a nakonfigurujte pravidlá kalendára.

**Vytvorí novú šablónu kalendára**

1. Prejdite do ponuky **Nastavenia** \> **Šablóna kalendára**.
2. Stlačte možnosť **Nový** a zadajte názov, popis a prostriedok šablóny.


> [!NOTE]
> Keď sa na prostriedok odkazuje v šablóne kalendára, kópia kalendára prostriedku je spojená so šablónou kalendára. Ak dôjde k zmene pracovného času skopírovanej šablóny, tieto zmeny sa nezanesú do šablóny kalendára.


### <a name="see-also"></a>Pozrite si tiež  
 [Nastavenie zdrojov](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
