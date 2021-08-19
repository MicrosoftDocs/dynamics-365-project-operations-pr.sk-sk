---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 33, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 33, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: a72202905fc0464577bb126aa5890a8f952dc3a8aff505416e535b42b53df7db
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006535"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 33, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 33. Táto verzia má číslo zostavenia V3.10.54.98 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie z júla 2021.

## <a name="update-release-33"></a>Aktualizácia vydania 33

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Dve zamknuté polia, **msdyn_description** a **msdyn_externaldescription** sú editovateľné po odoslaní.
- Chybové hlásenie sa objaví, ak sa vytvorí výdaj, ktorý nesúvisí s projektom.
- Keď je vytvorený časový záznam, predvolená rola prostriedku je neaktívna.
- Riadky denníka spojené s odvolaným a odstráneným výdavkom sa neodstránia.
- V rámci položky **Formulár rýchleho vytvorenia zadania času** aktualizujte zobrazenie **Zoznam projektových úloh** a zmeňte predvolene zobrazený dátum na dátum začatia úlohy.
- Keď vytvoríte časový záznam na karte **Súvisiace**, na záložke rezervovateľného zdroja je pre prihláseného používateľa nesprávne vytvorený časový údaj namiesto nadradeného rezervovateľného prostriedku.
- Do dialógového okna **Hromadné schválenie MDD** sú pridané ďalšie polia.

**Plánovanie projektu**

Vyriešili sa tieto problémy:
- K pomalému výkonu pri vytváraní projektu dochádza, keď sa šablóny pracovných hodín projektu používajú so zložitými kalendármi.
- Keď je počiatočný dátum väčší ako konečný dátum, na šablóne projektu kopírovania sa zobrazí chyba z dôvodu rozdielov v časovej zložke každého poľa.

**Správa zdrojov**

Vyriešili sa tieto problémy:
- V dotaze na využitie prostriedkov sa používa nesprávny parameter a XML vedie k nesprávnym výsledkom filtra v mriežke **Využitie zdrojov**.
- Potvrdenie **Rozšíriť rezervácie** zobrazí nesprávny dátum ukončenia rezervácie.

**Predaj**

Vyriešili sa tieto problémy:
- Ak sa vytvorí cena kategórie s chýbajúcimi hodnotami, zobrazí sa chybové hlásenie.
- Chybové hlásenie sa objaví, ak sa míľnik riadka zmluvy vytvorí bez riadku objednávky.
