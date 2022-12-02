---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 41, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v aktualizácii Microsoft Dynamics 365 Project Service Automation, vydanie 41, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 03/07/2022
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
ms.openlocfilehash: 8625ae16e45da30614b3a3eec44193bee0c0b36f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930567"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-41-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 41, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 41, V3. Táto verzia má číslo zostavy V3.10.62.162 a je všeobecne dostupná prostredníctvom samoaktualizácie v marci 2022.

## <a name="update-release-41"></a>Aktualizácia vydania 41

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Riadenie projektov**
- Keď sa pokúsite vytvoriť projekt zo šablóny, ktorá je založená na projekte vytvorenom z doplnku pre stolné zariadenia, zobrazí sa nasledujúca chyba: „Overenie poľa plánovanej práce priradenia zdrojov: Dátum ukončenia každého časového úseku priradenia zdrojov nesmie byť skorší ako jeho dátum začiatku“.

**Čas a výdavky**
- Keď sa pokúsite odstrániť časový údaj, zobrazí sa nasledujúce chybové hlásenie „Vyskytla sa neočakávaná chyba z kódu ISV“.

**Predaj**
- Keď vytvoríte faktúru za medzník s pevnou cenou, polia **Popis** a **Vonkajší popis** nie sú vyplnené. 
