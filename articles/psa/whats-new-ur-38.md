---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 38, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v aktualizácii Microsoft Dynamics 365 Project Service Automation, vydanie 38, V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ccc08cd0bc365bd4761424a4c0ceac91985e7c89
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915204"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-38-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 38, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením oznamujeme najnovšiu aktualizáciu pre aplikáciu Microsoft Dynamics 365 Project Service Automation. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Je kompatibilná s verziou Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku Centra spravovania pre online riešenia služby Dynamics 365 a nainštalujte si aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation, vydanie 38, V3. Táto verzia má číslo zostavenia V3.10.59.117 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie v decembri 2021.

## <a name="update-release-38"></a>Aktualizácia vydania 38

### <a name="bug-fixes"></a>Opravy chýb

Vyriešili sa tieto problémy.

**Čas a výdavky**

- Výnimka nastane, keď dĺžka protokolov o množine schválení prekročí 100 000 záznamov.
- Používatelia nemajú prístup k mriežke **Zadanie času** z hlavnej stránky **Zadanie času**.
- Dialógové okno **Import zadania času** nezobrazuje žiadny text, keď žiadne položky nie sú vhodné na import.
- Používatelia môžu vytvárať množiny schvaľovania, kde je pole **Cieľový stav** nastavené na **Neznámy**.

**Riadenie projektov**

- Kontúry sa nezobrazujú správne v priradení zdrojov pre UTC (+09:30) a UTC (+10:00), keď sa začína letný čas.
- Pole **Doplnkový stĺpec** pre štruktúry rozdelenia práce je v niektorých lokalitách skryté.
- Výber dátumu pre ovládací prvok kalendára v mriežke **Projektová úloha** nie je správne lokalizovaný pre čínštinu.

**Predaj**

- Hodnoty **Plnenie zmluvy** a **Skutočné náklady projektu** sa nezhodujú, keď rezervovateľné zdroje, ktoré majú rôzne zmluvné jednotky a meny, odosielajú časové záznamy.
- Vlastný pracovný postup na automatické potvrdenie faktúr zlyhá, keď sa faktúry importujú ako spravované riešenie. Zobrazí sa nasledujúca správa: „Správa Microsoft.Xrm.Sdk.InvalidPluginExecutionException: Neplatný stav faktúry.“
- Keď je ako možnosť súhrnu vybrané **Koreň** a projekt má odhady zo zmesi tried transakcií (napríklad kombinácia odhadov času, nákladov a materiálu), systém sumarizuje triedy medzi transakciami ako jeden riadok poplatkov.
- V scenároch, v ktorých sa výdavkový riadok pridá pred priradením riadku zmluvy k projektu, nie je zadaná správna cena ako predvolená hodnota v poli **Aktualizovať cenu**.
- Záporné sumy predaja nie sú povolené v entitách **Projekt** a **Úloha**.
