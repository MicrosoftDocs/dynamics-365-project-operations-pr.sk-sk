---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 37, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v Microsoft Dynamics 365 Project Service Automation Aktualizácia vydanie 37, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: bdbb125b4f41bb9970f5bd8a01cf0bb863c34738
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922517"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 37, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation Update Release 37, V3. Táto verzia má číslo zostavy V3.10.58.120 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie z novembra 2021.

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
