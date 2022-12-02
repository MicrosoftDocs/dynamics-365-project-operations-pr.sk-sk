---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 25, V3
description: Tento článok obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 25, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 2330c7dc5d2dfb148d5c7fb9a5ce643fded84dde
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922563"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 25, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation V3, aktualizované vydanie 25. Táto verzia má číslo zostavenia V 3.10.43.76 a je všeobecne dostupná prostredníctvom automatickej aktualizácie v októbri 2020.

## <a name="update-release-25"></a>Aktualizácia vydania 25

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Nasledujúci problém bol opravený:

- Graf zadávania času zobrazujúci ďalšie údaje na základe príliš veľkého intervalu, ktorý sa načítava.

**Správa zdrojov**

Nasledujúci problém bol opravený:

- Pridaný kód pre Package Deployer na preskočenie importu opravy Universal Resource Scheduling, ak už existuje opravná aktualizácia vyššej verzie.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Opravené nezrovnalosti pri zaokrúhľovaní a výmennom kurze, ktoré majú za následok nesprávne plánované náklady v mriežke sledovania projektu.
- Podpora možnosti zobrazenia dvoch alebo viacerých reagujúcich mriežok vo formulári **Projekt**.
- Poskytnuté overenie na riešenie schopnosti priradiť úlohu po dátume ukončenia kalendára, čo má za následok neúspešné priradenie zdroja.
- Vylepšené spracovanie chýb pri riešení výnimky Null Reference vygenerovanej z nasledujúcich:

    - doplnok **PreValidateProjectTeamMemberCreate**
    - **PreValidateProjectTaskCreate** keď je projektová úloha vytvorená bez pridruženého projektu
    - doplnok **PreProjectTeamMemberCreate**
    - doplnok **PostProjectTeamMemberDelete**
    - doplnok **PreValidateProjectTaskDelete**

**Sales**

Vyriešili sa tieto problémy:

- Vylepšené spracovanie chýb pri riešení výnimiek Null Reference vygenerovaných z **Kopírovať projekt: Odhady správy HelperResource**.
- **Nepripravené na fakturáciu** a **Backlog pre fakturáciu času a materiálu** nevymaže stav fakturácie.
- Opravené nesprávne označené tlačidlá **Ceny** na karte **Cena roly** a **Katalógové položky**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
