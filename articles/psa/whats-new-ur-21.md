---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 21, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 21, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: dd894f27baac70238d0bd9e9b1a21a9a499e1ea7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002346"
---
# <a name="project-service-automation-update-release-21-v3"></a>Aktualizácia pre Project Service Automation, vydanie 21, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 21. Táto verzia má číslo V 3.10.32.50 a v júni 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

## <a name="update-release-21"></a>Aktualizácia vydania 21

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Pri hosťovaní **Ovládacieho prvku mriežky so zadaniami času** v tabuliach táto mriežka nevyužíva celú šírku kontajnera mriežky tabule.
- Pokiaľ ide o konkrétne časové pásma, ovládací prvok mriežky **Zadanie času** nezobrazuje záznamy.
- Zadania času, ktoré sú po 21:00, sa zobrazujú v nesprávny deň.
- Používatelia nemôžu odosielať výdavky, ak kategória výdavkov **Vyžaduje sa potvrdenie o výdavkoch** nemá žiadnu hodnotu.

**Správa zdrojov**

Vyriešili sa tieto problémy:

- Neaktívne rezervácie sa zobrazujú v zobrazení **Vyrovnanie**.
- Pri plnení všeobecných požiadaviek na zdroje chýbalo overenie, ktoré by zabezpečilo, že existuje platný stav rezervácie.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Mriežky formulára **Projekt** (**Priradenie zdroja**, **Úloha**, **Vyrovnanie**, **Odhady výdavkov**) sa dajú upravovať, aj keď projekt nie je aktívny.
- Duplicitní zákazníci sa nemôžu zlúčiť so zákazníkmi, ktorí sú spojení s potvrdenými projektovými zmluvami.
- Po pridaní zdroja, ktorý nemá platný kalendár, systém nevráti používateľsky prístupné chybové hlásenie.
- Tlačidlo **Pridať úlohu** na mriežke úloh je povolené, keď je projekt prepojený s **doplnkom Microsoft Project**.
- Úsilie rastie nekontrolovateľne, keď je úloha s kategóriou priradená k zdroju, pre ktorý je definovaná obstarávacia cena.

**Sales**

Vykonali sme nasledovné vylepšenia:

- **Frekvencia fakturácie** a **Začiatok fakturácie** boli presunuté na kartu **Plán fakturácie**.

Vyriešili sa tieto problémy:

- **Celková predajná cena** je nula (0) pre položku **Kategória**, aj keď má **Rola** celkovú predajnú cenu, ktorá nie je nula.
- Zákazníci nemôžu zmeniť hodnotu poľa **Stav faktúry** na **Pripravené na fakturáciu**, keď iný prispôsobený proces aktualizuje ďalšie pole.
- Tlačidlo **Obnoviť riadky faktúry** môže vytvoriť viac duplicitných riadkov, ak je opakovane vybrané.
- Tlačidlo **Aktualizovať ceny** nefunguje na vedľajšej mriežke **Ceny rolí** vo formulári **Rýchle zobrazenie**.
- Logika **Vyriešenie predajného cenníka** nesprávne spracúva časové pásma, čo vedie k nesprávnemu výberu cenníkov.
- **Celkové skutočné náklady** projektu môžu byť nepresné o zlomkovú sumu po schválení jedného zadania času.
- Logika **Vyriešenie ceny** neposkytuje používateľsky prístupné chybové hlásenie, ak **Získaná cena roly** nemá hodnoty v poli **„Primárna jednotka“** a **„Cena v primárnej jednotke“**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]