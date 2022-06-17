---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 34, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v Project Service Automation Update Release 34, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/05/2021
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
ms.openlocfilehash: e47a5442f285952c165a2d30e337a362a6b065dd
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928681"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-34-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 34, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

V tomto článku sú uvedené funkcie a opravy, ktoré sú nové alebo zmenené pre Project Service Automation V3, vydanie aktualizácie 34. Táto verzia má číslo zostavenia V3.10.55.38 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie z júla 2021.

## <a name="update-release-34"></a>Aktualizácia vydania 34

### <a name="bug-fixes"></a>Opravy chýb
Vyriešili sa tieto problémy.

**Všeobecné**

- Aktualizácie riadené vydavateľom neaktivujú nový moderný pracovný postup schvaľovania.
- Atribúty **Cieľový stav** a **Typ akcie** chýbajú na hlavnej stránke **Množina schválení**.

**Čas a výdavky**

- Nie je možné schváliť žiadosť o stiahnutie pomocou moderného postupu schválenia.
- Pri kopírovaní záznamov, ktoré nesúvisia s prihláseným používateľom, nefunguje kopírovanie týždenných záznamov.

**Plánovanie projektu**

- Pri importovaní z doplnku pracovnej plochy programu Microsoft Project sú poškodené kontúry priradenia zdrojov.

**Správa zdrojov**

- Keď publikujete projekt z doplnku klienta Microsoft Desktop pre počítače, dátum ukončenia existujúcich požiadaviek sa zmení.
- Presnosť na desatinné miesta presahuje dve desatinné miesta v dialógovom okne potvrdenia rozšírených rezervácií.

**Predaj**

- Keď do projektovej zmluvy pridáte riadok založený na produkte s existujúcim produktom, zobrazí sa výnimka **kľúč sa nenašiel v slovníku**.
- Potenciálnych zákazníkov nemožno kvalifikovať, ak je typ objednávky mapovaný z potenciálneho zákazníka na príležitosť.
