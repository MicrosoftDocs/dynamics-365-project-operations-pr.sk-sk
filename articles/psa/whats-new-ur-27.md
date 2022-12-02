---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 27, V3
description: Tento článok obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 27, V3
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
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912949"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 27, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).

Tento článok obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 27. Táto verzia má číslo zostavy V3.10.45.98 a je všeobecne dostupná prostredníctvom samoaktualizácie v januári 2021.

## <a name="update-release-27"></a>Aktualizácia vydania 27

### <a name="bug-fixes"></a>Opravy chýb

**Všeobecné**

Vyriešili sa tieto problémy:

- Protokoly generované doplnkami v Project Service Automation neboli nastavené na automatické odstraňovanie.
- Automatická aktualizácia zlyhá, pretože riešenie Project Service Automation obsahuje starší nulový prvok NavBarArea a názov.

**Čas a výdavky**

Vyriešili sa tieto problémy:

- Mriežka **Zadanie času** zobrazuje nesprávne údaje pre správanie pri dátume **Nezávislé od časového pásma**.
- Mriežka **Zadanie času** vytvorí nesprávny čas pre správanie pri dátume **Nezávislé od časového pásma**.
- Vyhľadanie úlohy sa neobmedzuje iba na vybraný projekt na stránke **Upraviť zadanie času**.
- Schválenie času pre časové údaje nesúvisiace s projektom je zablokované, pretože systém vyhľadáva schvaľovateľa projektu.
- Správne zadanie skutočných údajov zobrazuje nesprávne chybové hlásenie.
- Keď úloha obsahuje nulovú hodnotu skutočných nákladov a súčty projektu sa obnovia, dôjde k nasledujúcej chybe „Daný kľúč nie je v slovníku“.
- V konkrétnych prípadoch filtre **Zoskupiť podľa** na karte **Odhad projektu** nezobrazuje odhady výdavkov.
- Interval **Letný čas** nie je správny pre zadanie času.

**Riadenie projektov**

Vyriešili sa tieto problémy:

- Vylepšenia v ukladaní do vyrovnávacej pamäte, ktoré zvyšujú výkon súvisiaci s načítaním stránky **Projekt**.
- Zastarané obchodné pravidlo zabraňujúce dokončeniu projektových úloh.
- Obrysy doplnku Microsoft Project nerešpektujú kalendár doplnku, čo má za následok nesprávne požiadavky na zdroje.
- Vytváranie projektov zo šablón nesprávne nastavuje dátumy priradenia a zabraňuje schopnosti generovať požiadavky na zdroje.
- Používateľ nemá prístup k možnostiam **Kategória**, **Popis**, **Stav** pomocou klávesnice.
- Skutočné hodnoty predaja projektu nezahŕňajú predajné hodnoty poplatkov a materiálov.
- K agregácii skutočných predajov a skutočných nákladov dochádza nesprávne pri rôznych výmenných kurzoch.
- Popis v časti **Predvolená šablóna pracovného času** je zavádzajúci.
- Odsadenie úlohy neodstráni položku **Kategória** v používateľskom rozhraní, kým sa neobnoví.
- Chýbajúce overenie na zabezpečenie, že sa projekt presunie za nepovolený dátum ukončenia.

**Sales**

Vyriešili sa tieto problémy:

- V riadku ponuky projektu sa generuje nulová referenčná výnimka, pretože možnosť **Importovať z odhadu projektu** je viditeľná, keď nebol vybraný projekt.
- Pri uzatváraní ponuky ako **Získaná** sa zobrazuje nasledujúca chyba „Referencia objektu nie je nastavená na inštanciu objektu“.
- Stav úprav nie je nastavený počas skutočného storna pri odpájaní projektu od riadka zmluvy.
- Keď sú nainštalované Dynamics 365 Field Service a Project Service Automation, možnosti **Zablokovať ceny** a **Použiť aktuálne ceny** sa nezobrazujú súčasne na stránke **Faktúra**.
- Pre japonský jazyk existuje nekonzistentný preklad s inými stránkami založenými na kalendári.
- Možnosti **Aktivovať** a **Deaktivovať** boli odstránené z entít **Priradenie cenníka** v Project Service Automation.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
