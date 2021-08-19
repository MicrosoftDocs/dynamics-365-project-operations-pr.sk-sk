---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 31, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 31, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: 2e5fce003c25f9c5911e5a01fb4ec3e19c06c078e00b054472699a522b9cd070
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002170"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 31. Táto verzia má číslo V3.10.52.77 a v máji 2021 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

## <a name="update-release-31"></a>Aktualizácia vydania 31

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Ovládacie tlačidlá príkazu na zadanie času na stránke **Rezervovateľný zdroj** bola neprehľadná.
- V systéme bola vygenerovaná nulová referenčná výnimka **Project.SetTrackingFields** pri schvaľovaní časového záznamu.

**Správa zdrojov**

Vyriešili sa tieto problémy:

- **Vytvoriť člena tímu** nezobrazuje správne nastavenie metadát nastavenia rezervácie pre server **Predvolený stav potvrdenia rezervácie**.
- Pri aktualizácii z PSA 1.X na 3.X proces aktualizácie zlyhá pri **UpgradeResourceRequirements**.


**Predaj**

Vyriešili sa tieto problémy:

- Skutočný príjem prevádza sumy v sledovacej mriežke na menu projektu.
- Predvolené meny sú nejasné pri vytváraní riadkov denníka, riadkov ponúk a kontraktov v scenároch, kde sa základná mena organizácie líši od meny projektu.
- **Čaká sa na overenie denníka opráv** dopyt nefiltruje podľa projektu.
- Zvyšný predaj sa v projekte počíta nesprávne.
- Cenové ponuky založené na kontakte zlyhajú, keď sú vytvorené bez cenníka.
- Po výbere možnosti **Potvrdiť faktúru** sa nezobrazí žiadny číselník spracovania.
- Po výbere možnosti **Vytvoriť faktúru** sa nezobrazí žiadny číselník spracovania.
- Uzatvorenie cenovej ponuky za stratené nezruší rezervácie.







