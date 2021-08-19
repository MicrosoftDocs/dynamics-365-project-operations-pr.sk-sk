---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 23, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 23, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: ec27d2344f14e61a50be2771ee3d7952f16abd736927de7c3c5a019351a3e067
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6996635"
---
# <a name="project-service-automation-update-release-23-v3"></a>Aktualizácia pre Project Service Automation, vydanie 23, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 23. Táto verzia má číslo V 3.10.34.30 a vo všeobecnosti je k dispozícii prostredníctvom samostatnej aktualizácie z augusta 2020.

## <a name="update-release-23"></a>Aktualizácia vydania 23

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:
- Spracúvajte hraničné prípady v časti **Odstránenie člena projektového tímu** na poskytnutie zmysluplnej výnimky.
- Výsledkom importu priradenia je prázdna obrazovka odstránenia.

**Správa zdrojov**

Vyriešili sa tieto problémy:

- **Karta zdrojov mriežky využitia zdrojov** ukazuje nesprávne údaje, ak je časová škála dlhšia ako päť dní.
- Keď zákazníci vytvoria rezervovateľný zdroj, doplnok občas zlyhá pri automatickom pridávaní zdroja do skupiny Microsoft Office 365.
- Zobrazenie **Vyrovnanie** ukazuje nesprávne manuálne kontúry v zobrazení **Týždeň** alebo **Mesiac**.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Nadmerný počet entít **RetrieveMultiple for usersettings** spôsobuje zhoršenú výkonnosť pri schvaľovaní projektov a iných operáciách.
- Vyhľadávanie zdrojov na mriežke **Plánovanie úloh** je obmedzené na zobrazenie iba piatich členov tímu z projektového tímu. 
- Vyhľadávanie zdrojov na mriežke **Plánovanie úloh** nefiltruje neaktívne zdroje.
- Manuálny režim nefunguje podľa očakávania v štruktúre rozdelenia práce pri plánovaní projektu.
- Mriežka **Plánovanie úloh** ukazuje **Kategórie neaktívnych transakcií**.
- Mriežka **Priradenie zdrojov** sa zaokrúhľuje nesprávne, keď má úloha viac priradení.
- Hodnoty zaokrúhľovania sa líšia medzi plánovanými a skutočnými nákladmi na jednu úlohu.

**Sales**

Vyriešili sa tieto problémy:

- Dvojité kliknutie na položku **Načítať všetky kategórie transakcií** vytvorí viac riadkov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]