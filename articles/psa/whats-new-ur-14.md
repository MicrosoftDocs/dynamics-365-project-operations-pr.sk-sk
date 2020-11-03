---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 14, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 14, V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084322"
---
# <a name="project-service-automation-update-release-14-v3"></a>Aktualizácia pre Project Service Automation, vydanie 14, V3
S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA). Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 14. Táto verzia má číslo zostavenia V3.10.4.21 a je k dispozícii v nasledujúcom harmonograme:

- **Všeobecná dostupnosť (samoaktualizácia):** Január 2020
- **Automatická aktualizácia:** Február 2020

## <a name="update-release-14"></a>Aktualizácia vydania 14

### <a name="enhancements"></a>Vylepšenia

- Sales

     - Vlastné hodnoty poľa z **Podrobnosti o riadku cenovej ponuky** sú skopírované do **Podrobnosti o riadku projektovej zmluvy** pri aktualizácii ponuky na **Uzavreté ako využité**.
     - Potvrdené projekty môžu byť **Uzavreté ako nevyužité**.

- Správa zdrojov

     - Pri rozširovaní rezervácií budú používatelia vyzvaní dialógovým oknom s potvrdením, aby zhrnuli výsledky rezervácie a poskytli odkaz na zachovanie rezervácií.


### <a name="bug-fixes"></a>Opravy chýb

- Čas a výdavky

     - Oprava: Vylepšené používateľské rozhranie, keď používateľ nevybral žiadne položky, ktoré sa majú opraviť.

- Správa zdrojov

     - Oprava: Pri rezervácii zdroja viackrát pretečie názov rezervovateľného zdroja.

- Sales

     - Oprava: Celková predajná cena sa nevypočítava, kým používateľ nevloží obstarávaciu cenu pre odhady výdavkov na projekt.
     - Oprava: Zatvorenie cenovej ponuky ako **Využitá** zlyhá, ak súvisiaca projektová zmluva nie je v stave **Koncept**.

