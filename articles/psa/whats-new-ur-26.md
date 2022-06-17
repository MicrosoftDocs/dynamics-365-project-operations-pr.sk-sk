---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 26, V3
description: Tento článok obsahuje zoznam funkcií a opráv, ktoré sú k dispozícii v Project Service Automation Update Release 26, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 11f722c1f31c0e8aa08192cc955aabbe97018225
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928819"
---
# <a name="project-service-automation-update-release-26-v3"></a>Aktualizácia pre Project Service Automation, vydanie 26, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation Update Release 26, V3. Táto verzia má číslo zostavenia V3.10.44.59 a je všeobecne dostupná prostredníctvom vlastnej aktualizácie v decembri 2020.

## <a name="update-release-26"></a>Aktualizácia vydania 26

### <a name="bug-fixes"></a>Opravy chýb

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Používatelia môžu zmeniť úlohu pri zadaní času, ktorý bol schválený/odoslaný.
- Chyba „Referencia objektu nie je nastavená“ pri ukladaní zadania času.
- Importom časovej položky z priradení zdrojov sa vytvárajú časové položky s nesprávnymi hodnotami DateTime.
- Keď sú nainštalované aplikácie Project Service Automation a Field Service, tlačidlo **Nový** sa dvakrát zobrazuje na paneli príkazov pre zadávanie času v aplikácii Field Service.
- Aktualizácie buniek **Povoliť jednotky** a **Jednotková skupina** v mriežke **Odhady výdavkov** teraz fungujú.
- Formulár **Aktualizovať Úpravu zadania času** obsahuje **Časovú os**.
- Schválenie času pre časové údaje nesúvisiace s projektom blokuje systém pri hľadaní roly schvaľovateľa projektu.

**Správa zdrojov**

Vyriešili sa tieto problémy:

- Pridaná validácia v doplnku **PostProjectCreate** na kontrolu primárnej požiadavky pred jej vytvorením.
- Formulár rýchleho vytvorenia **člena projektového tímu** vyvolá výnimku odkazu na hodnotu null, ak sú polia odstránené z formulára.
- Generovanie požiadaviek na 12 hodín v priebehu 1 roka zlyhá.
- Vylepšené chybové hlásenie pri výnimke odkazu na hodnotu null počas vytvárania požiadavky na zdroj.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Vylepšené overovanie adresy s cieľom vylúčiť výnimku odkazu na hodnotu null vygenerovanú v doplnku **PreProjectUpdate**.
- Projekty zverejnené doplnkom Microsoft Project pre počítač odstránia nepriradené priradenia.
- Pridané nové overenie, keď je odkaz na úlohu projektu neplatný z dôvodu výnimky odkazu na hodnotu null v doplnku **PreValidateProjectTaskUpdate**.
- Mriežka člena tímu nezobrazuje odlišné priradenia v zázname člena tímu.
- Pridané nové overovacie a chybové správy z dôvodu výnimky odkazu na hodnotu null v doplnku **PreProjectTaskDelete**.

**Sales**

Vyriešili sa tieto problémy:

- Pri výbere projektovej riadka v cenovej ponuke alebo zmluve by malo byť tlačidlo **Návrh** viditeľné iba pri výbere produktového riadka priradeného k existujúcemu produktu.
- Rozdeľte oprávnenie **Vytvoriť_Produkt** z oprávnenia **Vytvoriť_ProjektováZmluva**.
- Vymazanie riadka faktúry spôsobí, že dôjde k zlyhaniu odkazu na hodnotu null v **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
