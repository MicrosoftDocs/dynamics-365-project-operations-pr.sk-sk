---
title: Čo je nové v aktualizácii Project Service Automation, vydanie 12, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 12, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: af8dbfe3-7ce9-4374-9c03-17b2e1d6ac32
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 758717562c12a72848f1a874fa8b1171139ebb0c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755586"
---
# <a name="project-service-automation-v3-update-release-12"></a>Aktualizácia Project Service Automation V3, vydanie 12
S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA). Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 12. Táto verzia má číslo zostavy V3.10.2.34 a je všeobecne dostupná prostredníctvom samoaktualizácie v októbri 2019.

## <a name="update-release-12"></a>Aktualizácia vydania 12

### <a name="bug-fixes"></a>Opravy chýb

- Čas a výdavky

    - Oprava: Chybové správy o zadaní času boli aktualizované s relevantnejším kontextom.
    - Oprava: Mriežka zadávania času a harmonogram správne zobrazujú vertikálny posúvač, ak je to potrebné.
    - Oprava: Odoslané výdavky a zadania času môžu byť schválené.
    - Oprava: Dialogové okno s potvrdením o zrušení schválenia bolo opravené, aby odrážalo stav schválenia pri zmene zo **Schválený** na **Predložený**.
    - Oprava: Polia **Cena**, **Jednotka** a **Množstvo** sú teraz uzamknuté v zázname Výdavok po ich schválení.

- Riadenie projektov

    - Oprava: Akcia **Nový** v hlavnom formulári **Člen tímu** bola odstránená.
    - Oprava: Priradenia zdrojov boli aktualizované pre obchodný vzťah, aby sa zohľadnili chyby nepresného zaokrúhľovania, ktoré vedú k posunu dátumu ukončenia úlohy.
    - Oprava: V mriežke úloh sa používateľovi zobrazia príslušné chyby na strane servera.
    - Oprava: Meno člena tímu sa teraz v názve úlohy vykreslí namiesto názvu pozície.

- Správa zdrojov

    - Oprava: Podrobnosti o požiadavkách na zdroje pre projekty vytvorené zo šablóny teraz používajú kalendár projektu.
    - Oprava: Zručnosti a kompetencie sú predvolené od kmeňových dát role po požiadavku na zdroje vytvorenú pre túto rolu.

- Sales

    - Oprava: Duplicitné ID objektov nájdené vo formulári **Hlavná zmluva**.
    - Oprava: Logika bola aktualizovaná, aby vytvorila viditeľnú kartu **Analýza ponuky**, aby zobrazovala nastavenie metadát karty.
    - Oprava: Účtovný dátum v skutočnom zázname teraz prichádza od dátumu vloženia času/výdavkov a nie od dátumu schválenia.
