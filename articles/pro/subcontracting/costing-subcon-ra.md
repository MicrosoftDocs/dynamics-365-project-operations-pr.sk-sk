---
title: Odhad nákladov v prípade priradení zdrojov v rámci subdodávateľskej zmluvy
description: Tento článok vysvetľuje, ako Microsoft Dynamics 365 Project Operations vypočítava odhad nákladov na priradenia zdrojov v rámci subdodávateľskej zmluvy.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 9fded1baa63d2defc134994c858dfc6c09f75082
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522675"
---
# <a name="cost-estimation-of-subcontracted-resource-assignments"></a>Odhad nákladov v prípade priradení zdrojov v rámci subdodávateľskej zmluvy

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Priradenia úloh členom projektového tímu v rámci subdodávateľskej zmluvy sú kalkulované pomocou cenníka **Nákup** priloženého k subdodávke na príslušnom zázname člena tímu. Toto sa líši od toho, ako sa kalkulujú priradenia zdrojov zamestnancov, kde sa priradenia úloh zamestnancov počítajú pomocou cenníka **Náklady**, ktorý je priložený k zmluvnej jednotke projektu. 

V prípade všeobecných členov projektového tímu, ktorí sú subdodávateľmi, sa priradenia naceňujú pomocou nastavenia cien na základe rolí v nákupnom cenníku pripojenom k subdodávateľskej zmluve. Nákupné ceny môžu byť tiež nastavené špeciálne pre každý zdroj. Tieto ceny špecifické pre zdroj budú uprednostňované pri oceňovaní priradenia úloh menovaných členov projektového tímu, ktorí sú zmluvnými pracovníkmi. 

Priorita použitia nákupnej ceny špecifickej pre rolu oproti špecifickej pre zdroj je riadená nastavením priority cenovej dimenzie v ponuke **Parametre > Dimenzie určovania cien na základe sumy**.

Táto funkcia dynamického odvodzovania cien na základe nastavenia dimenzie pre nákupné ceny subdodávateľov je podobná tomu, ako sa odvodzujú nákladové a fakturačné sadzby pre zamestnancov na plný úväzok. 

## <a name="creating-task-assignments-for-getting-cost-estimates-of-subcontractor-resources"></a>Vytváranie priradení úloh na získanie odhadov nákladov na zdroje subdodávateľov

Priradenia úloh pre subdodávateľov možno vytvoriť dvoma spôsobmi: 
- Pomocou karty **Úlohy**.
- Pomocou karty **Tím**.

### <a name="creating-resources-assignments-using-the-tasks-tab"></a>Vytváranie priradení zdrojov pomocou karty Úlohy
Pomocou zoznamu **Zdroje** na karte **Úlohy** pre konkrétnu úlohu môžete vytvoriť priradenie úlohy pre menovaný zdroj alebo všeobecný zdroj. Ak vyberiete menovaný zdroj z rozbaľovacej ponuky **Priradené zdroje** v úlohe a tento zdroj je zmluvným pracovníkom, k úlohe sa priradí menovaný zdroj a vytvorí sa zodpovedajúci záznam člena projektového tímu s typom pracovníka nastaveným na **Zmluvný pracovník** a položkou **Platnosť** nastavenou na **Neplatné**. Ako ďalší krok budete musieť otvoriť záznam člena projektového tímu a vybrať subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy. Týmto sa aktualizuje priradenie úlohy tak, aby obsahovalo odkaz na subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy, a tiež sa aktualizuje stav člena tímu na **Platný**.

Ak sa rozhodnete vytvoriť všeobecného člena tímu z rozbaľovacej ponuky **Priradené zdroje** v úlohe, dialógové okno **Vytvorenie všeobecného člena tímu** vám umožní vybrať subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy. Keď sa k úlohe priradí všeobecný zdroj a vytvorí sa zodpovedajúci záznam člena projektového tímu, všimnete si, že záznam člena projektového tímu sa vytvorí s typom pracovníka nastaveným na **Zmluvný pracovník** a poľom **Platnosť** nastaveným na **Platné**.

### <a name="creating-project-team-members-using-the-team-tab"></a>Vytváranie členov projektového tímu pomocou karty Tím
Pomocou karty Tím v projekte môžete vytvoriť všeobecného alebo menovaného člena tímu. Pri vytváraní člena tímu môžete vybrať subdodávateľskú zmluvu a riadok subdodávateľskej zmluvy. Po vytvorení člena tímu budete musieť člena tímu priradiť k úlohe pomocou rozbaľovacej ponuky úlohy **Priradené zdroje**. 

## <a name="updating-estimates"></a>Aktualizácia odhadov
Po priradení členov projektového tímu k úlohám budete musieť prejsť na kartu **Odhady** na projekte a vybrať **Aktualizovať ceny**, čo zabezpečí, aby sa nákladové sadzby prideľovania zdrojov subdodávateľov aktualizovali na základe nákupného cenníka priloženého k subdodávateľskej zmluve. Pre nepriradené úlohy v Microsoft Dynamics 365 Project Operations sa negenerujú odhady. V dôsledku toho budete musieť vytvoriť priradenia úloh na stanovenie ceny a nákladov rôznych úloh na vašom projekte. 

> [POZNÁMKA!] Členovia projektového tímu, ktorí majú **Typ pracovníka** nastavený ako **Zmluvný pracovník**, ale nemajú referenciu na subdodávateľskú zmluvu označenú ako **Neplatné** na mriežke **Členovia projektového tímu**. Ak existujú členovia projektového tímu s týmto stavom, otvorte záznam člena projektového tímu a ručne aktualizujte polia subdodávateľská zmluva a riadok subdodávateľskej zmluvy tak, aby finančný odhad nákladov presne odrážal náklady subdodávateľa na karte **Odhady**. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
