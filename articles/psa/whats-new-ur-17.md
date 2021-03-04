---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 17, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 17, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: f9fb941a95b0610dc546b1c12a87aa7faef4d676
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143775"
---
# <a name="project-service-automation-update-release-17-v3"></a>Aktualizácia pre Project Service Automation, vydanie 17, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.  Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 17. Táto verzia má číslo zostavy V3.10.6.34 a je všeobecne dostupná prostredníctvom samoaktualizácie v marci 2020.


## <a name="update-release-17"></a>Aktualizácia vydania 17

### <a name="bug-fixes"></a>Opravy chýb

**Všeobecné**

- Oprava: Aktualizácia Project Service Automation na vynútenie licencií členov tímu (Centrum projektových zdrojov bude obsahovať metaúdaje plánu Team Member Service 3.x)
 
**Čas a výdavky**

- Oprava: Nie je možné zmeniť odhad výdavkov z nenulovej ceny na nulu (0). Zmena sa ignoruje.

**Riadenie projektov**

- Oprava: Do názvu pozície člena tímu bola pridaná kontrola nulových hodnôt.
- Opravené: pole **msdyn_userresourceid** v entite **msdyn_resourceassignment** bolo zastarané.
- Oprava: Aktualizácia z 2.x na 3.x teraz spracováva prázdne kontúry úsilia pri prideľovaní úloh.

**Sales**

- Opravené: **Invoice.PreValidateInvoiceUpdate** teraz rieši scenár správneho priradenia vlastníkov záznamov.
- Oprava: Keď je trieda transakcie **Čas**, **UnitGroup** nie je možné upravovať pre všetky entity vrátane **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** a **ContractLineDetails**. Avšak **Jednotka** nie je upraviteľná len pre **JournalLine** a **InvoiceLineDetails**.


