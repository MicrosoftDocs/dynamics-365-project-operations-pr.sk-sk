---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 38, V3
description: Táto téma obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v aktualizácii Microsoft Dynamics 365 Project Service Automation, vydanie 38, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 12/06/2021
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
ms.openlocfilehash: 1e5175b12c9e06962888bf09c8e07119b9505dda
ms.sourcegitcommit: 2aba2082d50b20b596ee86735045644cd647c2b0
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/08/2021
ms.locfileid: "7901519"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 38, V3. Táto verzia má číslo zostavenia V3.10.59.117 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie v decembri 2021.

## <a name="update-release-38"></a>Aktualizácia vydania 38

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Čas a výdavky**

- Výnimka nastane, keď dĺžka protokolov sady schválení prekročí 100 000 záznamov.
- Používatelia nemajú prístup k **Vstup času** mriežka od The **Vstup času** Hlavná stránka.
- The **Import vstupu času** dialógové okno nezobrazuje žiadny text, keď žiadne položky nie sú vhodné na import.
- Používatelia môžu vytvárať sady schvaľovania, kde **Cieľový stav** pole je nastavené na **Neznámy**.

**Riadenie projektov**

- Obrysy sa nezobrazujú správne v priradení zdrojov pre UTC (+09:30) a UTC (+10:00), keď sa začína letný čas.
- The **Doplnkový stĺpec** pole pre štruktúry rozpadu prác je v niektorých lokalitách skryté.
- Výber dátumu pre ovládací prvok kalendára v **Projektová úloha** mriežka nie je správne lokalizovaná pre čínštinu.

**Predaj**

- **Plnenie zmluvy** a **Skutočné náklady projektu** hodnoty sa nezhodujú, keď rezervovateľné zdroje, ktoré majú rôzne zmluvné jednotky a meny, odosielajú časové záznamy.
- Vlastný pracovný postup na automatické potvrdenie faktúr zlyhá, keď sa faktúry importujú ako spravované riešenie. Zobrazí sa nasledujúca správa: "Microsoft.Xrm.Sdk.InvalidPluginExecutionException Message: Neplatný stav faktúry."
- Kedy **Root** je vybratá ako možnosť sumarizácie a projekt má odhady zo zmesi tried transakcií (napríklad kombinácia odhadov času, nákladov a materiálu), systém sumarizuje medzi triedami transakcií ako jeden riadok poplatkov.
- V scenároch, v ktorých sa výdavkový riadok pridá pred priradením zmluvného riadku k projektu, nie je zadaná správna cena ako predvolená hodnota v poli **Aktualizovať cenu** lúka.
- Záporné sumy predaja nie sú povolené **Projekt** a **Úloha** subjektov.
