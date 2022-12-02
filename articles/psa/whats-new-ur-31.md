---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 31, V3
description: Tento článok obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 31, V3
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 8d62b12a5363637e46b29c2e9edf4e1f17da729f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925047"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 31, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 31. Táto verzia má číslo V3.10.52.77 a v máji 2021 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

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







