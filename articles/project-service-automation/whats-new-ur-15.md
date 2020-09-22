---
title: Čo je nové v aktualizácii Project Service Automation, vydanie 15, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 15, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: 75117934-8042-448b-91dc-b43f1f677e4f
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 68e0faa4c1afdb0d1520388253671330f9b7d334
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755583"
---
# <a name="project-service-automation-v3-update-release-15"></a>Aktualizácia Project Service Automation V3, vydanie 15

S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA). Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 15. Táto verzia má číslo zostavy V3.10.5.28 a je všeobecne dostupná prostredníctvom samoaktualizácie v januári 2020.

## <a name="update-release-15"></a>Aktualizácia vydania 15 

### <a name="enhancements"></a>Vylepšenia

- Riadenie projektov

### <a name="bug-fixes"></a>Opravy chýb

- Čas a výdavky

  - Oprava: Pridanie spracovania chýb pri načítaní v zobrazení odsúhlasenia.
  - Oprava: Centrum projektových zdrojov: Premenovanie **množstva** na zníženie nejednoznačnosti.
  - Oprava: Úprava zobrazenia **Kopírovať stĺpce zadaní času** na zahrnutie typu.
  - Oprava: Úprava trvania zadania času v zobrazení mriežky pomocou desatinných čísel má za následok neznámu chybu pre niektoré čísla.

- Riadenie projektov

  - Oprava: Rozbaľovacia ponuka pre **Použiť v zobrazení sledovania** sa teraz rozširuje na základe šírky možností.
  - Oprava: Pri riadení projektov v časovom pásme +13 môžu výpočty úloh zobraziť nepresné výsledky.
  - Oprava: **Čas ukončenia člena tímu** bol opravený pri použití 24-hodinového kalendára.
  - Oprava: Opätovná aktivácia **BPF** v hlavnom formulári **msdyn_project**.
  - Oprava: Výpočet priradení už neignoruje jeden deň.
  - Oprava: Do formulára projektu bol pridaný nový oznamovací pruh, keď sa časové pásmo medzi používateľom a projektom líši.

- Sales

  - Oprava: Vyhľadávanie kategórie odhadu výdavkov sa môže použiť na filtrovanie duplikátov.
  - Oprava: Kód v **PluginDomain.ExecuteInTryCatchBlock (..)** už neskrýva pôvod výnimky.
  - Oprava: Už sa nezobrazí chybové hlásenie vo formulári **Vyhľadávanie projektu** v **Riadku ponuky**, ak existuje viac ako 1000 projektov.
  - Oprava: Mriežka **Odhady** pre odhady práce a odhady výdavkov teraz zobrazuje správny symbol meny.
  - Oprava: Keď organizácia aktualizuje PSA z vydania aktualizácie 14 na vydanie aktualizácie 15, karta **Plán** sa už nezobrazuje ako prázdna karta vo formulári **Projekt**.
