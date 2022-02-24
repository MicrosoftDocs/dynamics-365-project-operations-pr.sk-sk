---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 19, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 19, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 8a73a6acd4ce4c9559cdf4591ede735a613f4d52
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143670"
---
# <a name="project-service-automation-update-release-19-v3"></a>Aktualizácia pre Project Service Automation, vydanie 19, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 19. Táto verzia má číslo V3.10.30.41 a v máji 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

## <a name="update-release-19"></a>Aktualizácia vydania 19

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy: 

- Chyby odvodené z importov zadania času sa nezobrazujú správne.
- Mriežka zadania času nepodporuje správanie poľa **Iba dátum**.
- Zdroje projektu nedokážu vytvoriť výdavok v rámci projektu.

**Riadenie projektov**

Vyriešili sa tieto problémy: 

-  Podriadená úloha druhej úrovne spôsobuje nesprávny odhad úsilia počas odhadu pri dokončení (EAC).

**Sales**

Vyriešili sa tieto problémy: 

- Akcia **Prepočítať** nefunguje s podrobnosťami v riadku zmluvy pre výdavok alebo s podrobnosťami v riadku pre cenovú ponuku.
- Pred odhad výdavkov chýba pole **Aktualizovať ceny**.
-  Zákazníci si na stránke **Projektová zmluva** nemôžu vybrať vlastné dôvody stavu zmluvy.
- Pri vytváraní vlastného cenníka z cenovej ponuky zaznamenávajú zákazníci zhoršený výkon.
- Zákazníci sa stretávajú s nekonzistentnosťou pri predvolených nastaveniach **jednotky** na stránke **Podrobnosti o riadku cenovej ponuky** a **Podrobnosti o riadku zmluvy**.
- Pridávanie položiek z kategórie nefakturovateľných transakcií do fakturovateľného riadku zmluvy nerešpektuje typ fakturácie **Nefakturovateľné** v rámci kategórie transakcií.
- Novo pridané roly a kategórie nemôžu zákazníci použiť v rámci starších vytvorených zmlúv.
- Zákazníci zaznamenávajú zhoršený výkon pri zbytočnom načítaní v PreValidateProjectTeamMemberUpdate.cs
- Roly nastavené v zozname **Kategórie zdrojov** ako nefakturovateľné by sa mali pridať na kartu **Fakturovateľné roly** v riadku zmluvy projektu ako **Nefakturovateľné**.
- Pri vytváraní projektu môžu zákazníci zaznamenať zhoršený výkon, pretože **GetBookableResourceIdFromUser** načíta všetky stĺpce rezervovateľných zdrojov namiesto výhradne primárneho ID.
- Entita **TransactionType** nemá doplnok aktualizácie pred overením, ktorý zabraňuje vstupu používateľov do **Jednotiek** a **Jednotkových skupín**, ktoré nie sú platné pre typy transakcií.
- Krok **Odstrániť** nefunguje pri importe zadania času.
