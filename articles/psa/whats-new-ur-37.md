---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 37, V3
description: Táto téma obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v aktualizácii Microsoft Dynamics 365 Project Service Automation, vydanie 37, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: 7bd00ccbb09fb43f7d7c3e0fef888a4e9dfcc752
ms.sourcegitcommit: f888e9c6e0290608abb915aa599ae9629b0efd3e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727624"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 37, V3. Táto verzia má číslo zostavy V3.10.58.120 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie z novembra 2021.

## <a name="update-release-37"></a>Aktualizácia vydania 37

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Čas a výdavky**
- Používatelia nemôžu vymazať záznam času vymazaním bunky.
- Zobrazenie **Moje neúspešné schválenia** obsahuje iba schválenia projektov so stavom **Odoslané**.

**Projektový manažment**
- Ak je názov pozície člena projektového tímu prázdny, používatelia dostanú pri otváraní projektu v doplnku pracovnej plochy spoločnosti Microsoft chybu o nulovej referencii.
- Nenájdete žiadne tlačidlo **Uložiť** na stránke **Projektová úloha**, aby používatelia nemohli ukladať zmeny v záznamoch úloh.
- Používatelia nemôžu odstrániť projekt, ktorý má úlohu priradenú k cenovej ponuke so stavom **Využité**.

**Predaj**
- Pole **Mena** na stránke **Projekt** sa aktualizuje tak, aby zodpovedala mene použitej šablóny.
- Náklady sú vypočítané nesprávne pri úlohách, ktoré majú viacero mien.
