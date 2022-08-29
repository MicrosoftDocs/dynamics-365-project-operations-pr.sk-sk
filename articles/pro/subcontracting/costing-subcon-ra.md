---
title: Odhad nákladov v prípade priradení zdrojov v rámci subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako Microsoft Dynamics 365 Project Operations vypočítava odhad nákladov na subdodávateľské priradenia zdrojov.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 5a4d0707f8373b5083272eacb7dc1318e82a23ac
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262079"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Odhad nákladov v prípade priradení zdrojov v rámci subdodávateľskej zmluvy

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Zadania úloh subdodávateľských členov projektového tímu sú kalkulované pomocou **Nákup** cenník priložený k subdodávke na príslušnom zázname člena tímu. Toto sa líši od toho, ako sa kalkulujú priradenia zdrojov zamestnancov, kde sa priradenia úloh zamestnancov počítajú pomocou **náklady** cenník, ktorý je priložený k zmluvnej jednotke projektu. 

Pre členov generického projektového tímu, ktorí sú zadávaní subdodávateľom, sú úlohy ocenené pomocou nastavenia ceny na základe roly v nákupnom cenníku priloženom k subdodávke. Nákupné ceny môžu byť tiež nastavené špeciálne pre každý zdroj. Tieto ceny špecifické pre zdroj budú uprednostňované pri zadaní nákladových úloh menovaných členov projektového tímu, ktorí sú zmluvnými pracovníkmi. 

Priorita použitia nákupnej ceny špecifickej pre rolu oproti špecifickej pre zdroj je riadená nastavením priority cenovej dimenzie v **Parametre > Dimenzie určovania cien na základe sumy**.

Táto funkcionalita dynamického odvodzovania cien na základe nastavenia rozmerov pre nákupné ceny subdodávateľov je podobná tomu, ako sa odvodzujú nákladové a fakturačné sadzby pre zamestnancov na plný úväzok. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Vytváranie zadaní úloh na získanie odhadov nákladov na zdroje subdodávateľov

Zadania úloh pre subdodávateľov možno vytvoriť dvoma spôsobmi: 
- Pomocou **Úlohy** tab.
- Pomocou **Tím** tab.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Vytváranie priradení zdrojov pomocou karty Úlohy
Pomocou **Zdroje** zoznam v **Úlohy** pre konkrétnu úlohu, môžete vytvoriť priradenie úlohy pre pomenovaný zdroj alebo všeobecný zdroj. Ak vyberiete pomenovaný zdroj z **Pridelené zdroje** v rozbaľovacej ponuke úlohy a tento zdroj je zmluvným pracovníkom, k úlohe sa priradí pomenovaný zdroj a vytvorí sa zodpovedajúci záznam člena projektového tímu s typom pracovníka nastaveným na **Pracovník na dohodu** a **Platnosť** nastavený na **Neplatné**. Ako ďalší krok budete musieť otvoriť záznam člena projektového tímu a vybrať subdodávku a subdodávku. Týmto sa aktualizuje zadanie úlohy tak, aby obsahovalo odkaz na subdodávku a subdodávateľskú líniu, a tiež sa aktualizuje stav člena tímu na **Platné**.

Ak sa rozhodnete vytvoriť všeobecného člena tímu z **Pridelené zdroje** rozbaľovacia ponuka na úlohu, **Generické vytváranie členov tímu** dialógové okno vám umožní vybrať subdodávku a linku subdodávky. Keď sa k úlohe priradí všeobecný zdroj a vytvorí sa zodpovedajúci záznam člena projektového tímu, všimnete si, že záznam člena projektového tímu sa vytvorí s typom pracovníka nastaveným na **Pracovník na dohodu** a **Platnosť** nastavený na **Platné**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Vytváranie členov projektového tímu pomocou karty Tím
Pomocou karty Tím v projekte môžete vytvoriť všeobecného alebo pomenovaného člena tímu. Pri vytváraní člena tímu môžete vybrať subdodávku a riadok subdodávky. Po vytvorení člena tímu budete musieť člena tímu priradiť k úlohe pomocou **Pridelené zdroje** rozbaľovací zoznam úlohy. 

## <a name="updating-estimates"></a>Aktualizácia odhadov
Po priradení členov projektového tímu k úlohám budete musieť prejsť na **Odhady** na projekte a vyberte **Aktualizujte ceny** zabezpečiť, aby sa nákladové sadzby prideľovania zdrojov subdodávateľov aktualizovali na základe nákupného cenníka priloženého k subdodávke. Pre nepriradené úlohy v Microsofte sa negenerujú odhady Dynamics 365 Project Operations. V dôsledku toho budete musieť vytvoriť priradenia úloh na stanovenie ceny a nákladov rôznych úloh na vašom projekte. 

> [POZNÁMKA!] Členovia projektového tímu, ktorí majú **Typ pracovníka** ako **Pracovník na dohodu** ale nemajú referenciu na subdodávku sú označené ako **Neplatné** na **Členovia projektového tímu** mriežka. Ak existujú členovia projektového tímu s týmto stavom, otvorte záznam člena projektového tímu a manuálne aktualizujte polia subdodávok a riadkov subdodávok tak, aby odhad finančných nákladov presne odrážal náklady subdodávateľa na **Odhady** tab. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
