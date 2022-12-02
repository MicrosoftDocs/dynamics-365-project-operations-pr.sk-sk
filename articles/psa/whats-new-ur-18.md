---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 18, V3
description: Tento článok obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 18, V3
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: e8d423c550d9aa09c9cbb7d4f7c277c43bbe10ae
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918883"
---
# <a name="project-service-automation-update-release-18-v3"></a>Aktualizácia pre Project Service Automation, vydanie 18, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 18. Táto verzia má číslo V3.10.8.12 a v apríli 2020 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.

## <a name="update-release-18"></a>Aktualizácia vydania 18

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

- Opravené: Toky **Odvolať**, **Vyžiadať** a **Zrušiť schválenie** vyvolávajú výnimky s nejasnými chybovými hláseniami.
- Opravené: Ak zlyhá tok **Zrušiť schválenie** pre výdavok, nevyvolá sa príslušná výnimka.
- Opravené: Mriežka so zadaniami času po prepnutí letného času (DST) v októbri nesprávne spracováva dni pracovného pokoja v Austrálii.
- Opravené: Nesprávna predvolená logika bráni zadávaniu výdavkov.
- Opravené: Ak zlyhá schválenie zadania, toto schválenie zostáva v stave **Nevybavené**.
- Opravené: Chyby SQL pri hromadných schváleniach (zablokovanie/časový limit).
- Opravené: Závažné problémy s výkonom v používateľskom rozhraní spôsobené aktualizáciou členov tímu počas schvaľovania zadaní času.

**Riadenie projektov**

- Opravené: Oznámenie o časovom pásme bolo presunuté zo zobrazenia **Vyrovnanie** na hlavný formulár **Projekt**.
- Opravené: Šablóna kalendára nie je správne predvolená po otvorení nového formulára projektu.
- Opravené: Pri prehliadačoch založených na technológii Chromium nemôžu používatelia jednoducho vybrať predchádzajúce úlohy na odstránenie.
- Opravené: Vytvorením alebo skopírovaním **Projektu z prázdnej šablóny** sa načítajú nesúvisiace priradenia.
- Opravené: V konkrétnych okrajových prípadoch povedie vytvorenie nového priradenia z mriežky úloh k vytvoreniu duplicitných záznamov.
- Opravené: V manuálnom režime nemôžu používatelia aktualizovať dátum začatia úlohy na neskorší dátum ako ten, ktorý je aktuálne uložený.

**Správa zdrojov**

- Opravené: V riadku medzisúčtu v zobrazení **Vyrovnanie** sa nesprávne vypočíta odchýlka v rezerváciách po rozšírení rezervácií.
- Opravené: V zobrazení **Vyrovnanie** sa nesprávne zobrazia priradenia zdrojov, ak rezervovateľný zdroj obsahuje kalendár, ktorý sa nezhoduje s kalendárom projektu.

**Sales**

- Opravené: Pri opätovnom schválení zadaní času (**Schváliť > Zrušiť >** Opätovne schváliť) sa vytvorí duplikát skutočnej neúčtovanej sumy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
