---
title: Nastavenie automatického vytvárania faktúr
description: Tento článok poskytuje informácie o nastavení a konfigurácii automatického vytvárania faktúr pro forma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c5160b22bd0d8a738c31a5105d83bd15cf136fab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911753"
---
# <a name="set-up-automatic-invoice-creation"></a>Nastavenie automatického vytvárania faktúr 
 
_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

V rámci Dynamics 365 Project Operations môžete konfigurovať automatické vytváranie faktúr. Systém vytvorí koncept zálohovej faktúry na základe plánu faktúr pre každú projektovú zmluvu a riadok zmluvy. Plány faktúr sa konfigurujú na úrovni riadka zmluvy. Každý riadok zmluvy môže mať samostatný plán faktúr alebo môže byť v každom riadku zmluvy uvedený rovnaký plán faktúr.

Pri vytváraní faktúry systém vždy vytvorí minimálne jednu faktúru pre každú projektovú zmluvu. V niektorých prípadoch môže byť vytvorených viac faktúr. Napríklad, ak má zmluva viac zákazníkov, vytvorí sa rovnaký počet faktúr ako počet zákazníkov, ktorí majú fakturovateľné transakcie, ktoré sa majú fakturovať na základe tejto projektovej zmluvy.

## <a name="understand-how-transactions-are-included-on-an-invoice"></a>Pochopte, ako sú transakcie zahrnuté vo faktúre 

Niekedy každý riadok zmluvy na základe projektu určuje osobitný plán faktúr. Napríklad, realizačné služby pre zmluvu Adatum majú nasledujúce riadky zmluvy:

- Prototypová práca, ktorá predstavuje pevnú cenu s dvoma manuálne vytvorenými medzníkmi.
- Realizačné práce, ktoré zahŕňajú čas, a budú sa účtovať každé dva týždne v pondelok.
- Výdavky, ktoré je potrebné fakturovať každý prvý pondelok v mesiaci.

Plány faktúr definované pre každú z týchto dvoch riadkových položiek vyzerajú podobne ako v nasledujúcej tabuľke:

| Riadok zmluvy | Dátum spustenia faktúry | Dátum uzávierky transakcie | Dátum medzníka | Suma medzníka |
| --- | --- | --- | --- | --- |
| Prototypová práca | 5. októbra, pondelok | - | 5. októbra, pondelok | 5000 USD |
| - | 3. novembra, utorok | - | 3. novembra, utorok | 12,000 USD |
| Realizačné práce | 5. októbra, pondelok | 4. októbra, nedeľa | - | - |
| - | 19. októbra, pondelok | 18. októbra, nedeľa | - | - |
| - | 2. novembra, pondelok | 1. novembra, nedeľa | - | - |
| - | 16. novembra, pondelok | 15. novembra, nedeľa | - | - |
| Vzniknuté výdavky | 5. októbra, pondelok | 4. októbra, nedeľa | - | - |
| - | 2. novembra, pondelok | 1. novembra, nedeľa | - | - |

V tomto príklade, keď je v prevádzke automatická fakturácia:

- **4. októbra alebo akýkoľvek predchádzajúci deň**: Pre túto zmluvu sa negeneruje žiadna faktúra, pretože tabuľka **Plán faktúry** pre každý z týchto riadkov zmluvy nevyvoláva 4. október v nedeľu ako dátum spustenia faktúry.
- **5. októbra pondelok** : Jedna faktúra sa vygeneruje pre:

    - Prototypovú prácu, ktorá obsahuje medzník, ak je označená ako **Pripravená na fakturáciu**.
    - Realizačné práce, ktoré zahŕňajú všetky časové transakcie vytvorené pred dátumom ukončenia transakcie 4. októbra v nedeľu, ktoré sú označené ako **Pripravené na fakturáciu**.
    - Realizačné práce, ktoré zahŕňajú všetky časové transakcie vytvorené pred dátumom ukončenia transakcie 4. októbra v nedeľu, ktoré sú označené ako **Pripravené na fakturáciu**.
  
- **6. októbra alebo akýkoľvek deň pred 19. októbrom**: Pre túto zmluvu sa negeneruje žiadna faktúra, pretože tabuľka **Plán faktúry** pre každý z týchto riadkov zmluvy nevyvoláva 6. október ani akýkoľvek deň pred 19. októbrom ako dátum spustenia faktúry.
- **19. októbra, pondelok**: Jedna faktúra sa vygeneruje pre realizačné práce, ktoré zahŕňajú všetky časové transakcie vytvorené pred dátumom ukončenia transakcie 18. októbra v nedeľu, ktoré sú označené ako **Pripravené na fakturáciu**.
- **2. novembra, pondelok** : Jedna faktúra sa vygeneruje pre:

    - Realizačné práce, ktoré zahŕňajú všetky časové transakcie vytvorené pred dátumom ukončenia transakcie 1. novembra v nedeľu, ktoré sú označené ako **Pripravené na fakturáciu**.
    - Realizačné práce, ktoré zahŕňajú všetky časové transakcie vytvorené pred dátumom ukončenia transakcie 1. novembra v nedeľu, ktoré sú označené ako **Pripravené na fakturáciu**.

- **3. novembra, utorok** : Vygeneruje sa jedna faktúra na realizačné práce, ktorá obsahuje medzník na 12000 USD, ak je označená ako **Pripravená na fakturáciu**.

## <a name="configure-automatic-invoicing"></a>Konfigurovať automatické fakturovanie

Ak chcete nakonfigurovať automatické vytváranie faktúr, vykonajte nasledujúci postup.

1. V časti **Project Operations** prejdite na **Nastavenia** > **Nastavenie opakovanej faktúry**.
2. Vytvorte dávkovú úlohu a pomenujte ju **Vytvorenie faktúr Project Operations**. Názov dávkovej úlohy musí obsahovať slová „vytvorenie faktúr“.
3. V poli **Typ úlohy** vyberte položku **Žiadne**. Štandardne sú polia **Frekvencia denne** a **Je aktívne** nastavené na **Áno**.
4. Vyberte **spustiť pracovný postup**. V dialógovom okne **vyhľadať záznam** sa zobrazia tri pracovné postupy:

- ProcessRunCaller
- ProcessRunner
- UpdateRoleUtilization

5. Vyberte **ProcessRunCaller** a potom **pridať**.
6. V ďalšom dialógovom okne kliknite na **OK**. Pracovný postup **spánok** je nasledovaný pracovným postupom **proces**. 

> [!NOTE]
> Môžete tiež vybrať **processrunner** v kroku 5. Potom, keď vyberiete **OK**, pracovný postup **proces** je nasledovaný pracovným postupom **spánok**.

Pracovné postupy **processruncaller** a **processrunner** vytvárajú faktúry. **ProcessRunCaller** volá **processrunner**. **ProcessRunner** je pracovný postup, ktorý skutočne vytvára faktúry. Pracovný postup prechádza všetky riadky zmluvy, pre ktoré musia byť vytvorené faktúry, a vytvára faktúry pre tieto riadky. Ak chcete určiť riadky zmluvy, pre ktoré musia byť vytvorené faktúry, úloha sa pozerá na dátumy spustenia faktúry pre riadky zmluvy. Ak riadky zmluvy patriace do jednej zmluvy majú rovnaký dátum spustenia faktúry, transakcie sa skombinujú do jednej faktúry, ktorá má dva riadky faktúry. Ak neexistujú žiadne transakcie na vytvorenie faktúr, úloha vynechá vytvorenie faktúry.

Po dokončení **procesrunnera**, sa volá **processruncaller**, ktorý poskytuje čas ukončenia a je uzavretý. **ProcessRunCaller** potom spustí časovač, ktorý beží 24 hodín od zadaného času ukončenia. Na konci časovača, je **processruncaller** uzavretý.

Dávková úloha pre vytváranie faktúr je opakujúca sa úloha. Ak je táto dávková úloha spustená mnohokrát, sú vytvorené viaceré inštancie úlohy a spôsobujú chyby. Preto by ste mali spustiť dávkový proces len raz, a potom ho reštartovať iba v prípade, že prestane fungovať.

> [!NOTE]
> Hromadná fakturácia v aplikácii Project Operations sa spustí iba pre riadky zmlúv projektu, ktoré sú konfigurované podľa plánov faktúr. Riadok zmluvy s metódou fakturácie podľa fixnej ceny musí mať nakonfigurované medzníky. V riadku zmluvy projektu s metódou fakturácie podľa času a materiálu bude potrebné zostaviť plán fakturácie založený na dátume.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
