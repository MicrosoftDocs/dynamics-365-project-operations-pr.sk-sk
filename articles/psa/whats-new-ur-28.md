---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 28, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 28, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: b3afeaf131c8bab25e1ed3a9eb3b41cb3059f711
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586823"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 28, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation V3, aktualizované vydanie 28. Táto verzia má číslo zostavenia V3.10.46.32 a je všeobecne dostupná prostredníctvom automatickej aktualizácie v januári 2021.

## <a name="update-release-28"></a>Aktualizácia vydania 28

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Používatelia môžu používať **Hromadné úpravy** na aktualizovanie časových zadaní, ktoré boli schválené a odoslané.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- V prípadoch, keď sa identifikátor GUID úlohy interpretuje ako číslo, úlohy nemožno otvoriť na úpravu pomocou možnosti **Upraviť úlohu** v páse s nástrojmi na stránke **Štruktúra rozdelenia práce**.

**Sales**

Vyriešili sa tieto problémy:

- Nulová referenčná výnimka sa vygeneruje, keď je vyvolaný doplnok **GetEstimatesForProject**.
- **Značka je pripravená na fakturáciu** v mriežke medzníkov aktualizuje atribúty iba čiastočne, s výnimkou atribútu **InvoiceStatus**, ktorý sa aktualizuje.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
