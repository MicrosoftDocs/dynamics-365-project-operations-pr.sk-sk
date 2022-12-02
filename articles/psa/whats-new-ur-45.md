---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 45, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v aktualizácii Microsoft Dynamics 365 Project Service Automation, vydanie 45, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169188"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 45, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 45, V3. Táto verzia má číslo zostavenia V3.10.76.168 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie z júla 2022.

## <a name="update-release-45"></a>Aktualizácia vydania 45

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Predaj**

- Používatelia nemôžu úspešne vytvárať faktúry po tom, čo sa pokúsia vytvoriť faktúru bez nevyúčtovaných predajov, ak si tiež prezerajú rovnakú inštanciu stránky a neobnovia ju.

**Čas a výdavky**

- Keď sú povolené moderné schválenia a je schválené schválenie odvolaného projektu, etapa záznamu sa nesprávne aktualizuje na **Žiadosť o odvolanie bola schválená**.
- Keď sú povolené moderné schválenia a postupy v cloude sú neaktívne, proces schvaľovania nie je úspešný a odosielajúci alebo schvaľujúci používatelia nie sú upozornení.
