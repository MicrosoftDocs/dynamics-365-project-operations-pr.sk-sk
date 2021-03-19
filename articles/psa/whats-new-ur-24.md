---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 24, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 24, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c789a65f1996d082410b3d8dd9e76e5065e708a2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280507"
---
# <a name="project-service-automation-update-release-24-v3"></a>Aktualizácia pre Project Service Automation, vydanie 24, V3

[!include [banner](../includes/psa-now-project-operations.md)]

S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365. Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti. Toto vydanie je kompatibilné s Dynamics 365 9.x. Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu. Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 24. Táto verzia má číslo V 3.10.42.43 a vo všeobecnosti je k dispozícii prostredníctvom samostatnej aktualizácie z októbra 2020.

## <a name="update-release-24"></a>Aktualizácia vydania 24

### <a name="bug-fixes"></a>Opravy chýb

**Sales**

Vyriešili sa tieto problémy:

- Problém pri nastavovaní predvoleného cenníka produktov.
- Výkon využitia cenovej ponuky je pomalý kvôli kopírovaniu vložených cenníkov a záznamov cien rolí.
- **Projektová zmluva/Centrum predaja** > **Položka skupiny produktov/Počet riadkov objednávky** sa automaticky zaokrúhľuje na najbližšie celé číslo.
- Povýšenie na systémové oprávnenia pri čítaní denníkov.
- Skopírujte polia adresy zákazníka **address1_freighttermscode** a **address1_shippingmethodcode** na cenovú ponuku/objednávku. 


**Čas a výdavky**

Vyriešili sa tieto problémy:

- **Mriežka časového vstupu** nepodporuje správanie času položky **Iba dátum**.
- **Časový vstup** sa automaticky neobnovuje. Vyžaduje sa manuálne obnovenie.
- Nie je možné importovať časové vstupy z priradenia, keď je v priradeniach zdroja prestávka (0 hodín).
- Pri vytváraní časového záznamu nastavte začiatok na rovnakú hodnotu ako **msdyn_date**.
- Znova povoľte hromadné úpravy časového vstupu.

**Správa zdrojov**

Vyriešili sa tieto problémy:

- Pokus o aktualizáciu stavu rezervácie počas dňa bez požiadavky vyvolá výnimku s nulovými referenčnými hodnotami.
- Chyba pri načítavaní súboru **Zobrazenie vyrovnania**.


**Riadenie projektov**

Vyriešili sa tieto problémy:

- V časti **Plán projektu** sa pri zmene z položky **Manuálny** na **Automatický** nedokončuje automatické ukladanie.
- Náklady by sa nemali počítať smerom k odchýlke v **mriežke sledovania projektu**.
- Nekonzistentné správanie pre stĺpce **Značka odhadov** počas načítavania v porovnaní so zmenou typu **Časová fáza**.
- Skutočné náklady na projekt nemusia reflektovať celkové hodnoty z časti **Skutočné hodnoty**.
- **Odhadovaný dátum dokončenia** na karte **Zhrnutie** sa nezhoduje s položkou **Plán WBS**.
- **Aktualizácia skutočných hodín** pri odsadení nefunguje správne.
- Projektový manažér mimo koreňovej **BU** nemôže vytvoriť projekt.
- Zmeny úlohy alebo kategórie v časti **Odhady výdavkov** sa nezachovávajú.
- **Kópia zmluvy** skopíruje plány faktúr a stav priebehu.
- Tlačidlo **Obnoviť skutočné hodnoty** nesprávne vypočítava súhrnné úlohy.
- Doplnok Microsoft Project: Oprava nulovej referenčnej chyby v prípade, ak má ktorýkoľvek člen tímu prázdnu zdrojovú jednotku.



[!INCLUDE[footer-include](../includes/footer-banner.md)]