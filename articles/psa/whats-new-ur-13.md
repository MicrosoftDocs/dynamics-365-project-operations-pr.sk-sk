---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 13, V3
description: Tento článok poskytuje informácie o tom, čo je nové v Project Service Automation Update Release 13, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: f4898391922f5ecbc99d78e49358ea749fe27b3f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930705"
---
# <a name="project-service-automation-update-release-13-v3"></a>Aktualizácia pre Project Service Automation, vydanie 13, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA). Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation V3, vydanie aktualizácie 13. Táto verzia má číslo zostavenia V3.10.3.18 a je k dispozícii v nasledujúcom harmonograme:

- **Všeobecná dostupnosť (samoaktualizácia):** November 2019
- **Automatická Aktualizácia** December 2019


## <a name="update-release-13"></a>Aktualizácia vydania 13 

### <a name="bug-fixes"></a>Opravy chýb

- Čas a výdavky

     - Oprava: Funkcie vyhľadávania na stránke **Schválenie výdavkov** nefungujú pri vyhľadávaní podľa účelu výdavkov.

- Správa zdrojov

     - Oprava: Čísla v odsúhlasení boli aktualizované, aby boli správne zarovnané.
     - Oprava: Pomenované zdroje nemôžu byť priradené k úlohám prostredníctvom karty **Plán**.

- Riadenie projektov

     - Oprava: Nulová referenčná výnimka pri prideľovaní člena tímu, keď typu **TransactionType** chýbajú informácie o nastavení pre **Jednotka** a **DefaultGroup**.

- Sales

     - Oprava: Duplicitné záznamy typu transakcie vracajú chybu pri vytváraní záznamov o cenách rolí.
     - Opravené: Extra tlačidlá pre **Nová príležitosť**, **Cenová ponuka**, **Riadok objednávky** a **Pridať produkt** sú viditeľné v príkazoch pre Príležitosti, Cenové ponuky, Produkty objednávky a vedľajšiu mriežku riadkov založených na projektoch.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
