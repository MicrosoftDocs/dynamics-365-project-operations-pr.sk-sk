---
title: Čo je nové v aktualizácii Project Service Automation, vydanie 14, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 14, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c69eab3b-0bb9-4b52-b606-e8a96e893471
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 31134756a5f4bff3022fca7df8364c49217b9b55
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755584"
---
# <a name="project-service-automation-v3-update-release-14"></a>Aktualizácia Project Service Automation V3, vydanie 14
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

