---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 29, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 29, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499690"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 29, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 29. Táto verzia má číslo zostavenia V3.10.45.98 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie vo februári 2021.

## <a name="update-release-29"></a>Aktualizácia vydania 29

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Používateľom sa v mriežke na zadanie času nezobrazí pracovný čas zaznamenaný počas nepracovných dní.
- Schválené záznamy výdavkov je možné upravovať v mriežke.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Chýba logika overenia, aby sa zabezpečilo, že hodiny úsilia priraďovania zdrojov nemôžu byť záporné.
- Vlastná akcia **AssignResourcesForTask** aktualizuje všetky polia namiesto výhradne zmenených polí.
- Pri kopírovaní projektu v prostredí s doplnkami alebo pracovnými postupmi, ktoré sú registrované v udalosti **CreateProject**, atribút **msdyn_bulkgenerationstatus** sa neaktualizuje, ak **CopyWBSToProject** zlyhá.
- Pri rozbalení kalendára projektu nie sú pracovné dni zoradené vzostupne, čo spôsobí zlyhanie niektorých aktualizácií úloh projektu.
- Zmena manažéra projektu pri existujúcom projekte spustí predvolenú logiku organizačnej jednotky.

**Predaj**

Vyriešili sa tieto problémy:

- Karta **Plnenie zmluvy** na stránke **Zmluva** počas inicializácie zlyhá, ak nie sú k dispozícii žiadne riadky zmluvy.