---
title: Predvolené cenníky
description: Tento článok poskytuje informácie o predvolených predajných a obstarávacích cenníkoch v Project Operations.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410282"
---
# <a name="default-price-lists"></a>Predvolené cenníky

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

## <a name="sales-price-lists"></a>Predajné cenníky

Každá cenová ponuka a zmluva projektu v aplikácii Dynamics 365 Project Operations obsahuje predvolený predajný cenník. 

### <a name="price-list-default-on-project-quotes"></a>Predvolený cenník pre projektové cenové ponuky
Systém dokončí nasledujúci proces, aby určil, ktorý cenník je predvolený pre cenovú ponuku projektu:

1. Systém sleduje cenníky, ktoré sú pripojené k cenníkom projektov projektu pre obchodný vzťah. 
1. Ak k záznamu obchodného vzťahu nie sú pripojené cenníky projektu, systém prehľadá predajné cenníky pripojené k parametrom projektu, ktoré sú spárované s menou cenovej ponuky projektu.
1. Potom systém skontroluje účinnosť cenníkov podľa dátumu, ktorý zodpovedá rozsahu dátumov cenovej ponuky projektu. Konkrétne dátum vytvorenia cenovej ponuky.
1. Ak existuje viac cenníkov s účinnosťou cenovej ponuky projektu k dátumu, všetky cenníky sú predvolene nastavené pre cenovú ponuku projektu.
1. Ak k dátumu cenovej ponuky projektu nie sú v platnosti žiadne cenníky, v ponuke projektu nie je nastavený žiadny predvolený cenník projektu. V cenovej ponuke projektu sa zobrazí varovné hlásenie. V hlásení sa uvádza, že skutočné údaje a odhady týkajúce sa projektu nebudú ocenené, pretože k nim nie sú priložené žiadne cenníky projektu.

### <a name="price-list-default-on-project-contracts"></a>Predvolený cenník pre projektové zmluvy 
Systém dokončí nasledujúci proces, aby určil, ktorý cenník je predvolený pre zmluvu projektu:

1. Ak je zmluva vytvorená z cenovej ponuky, cenníky projektu z cenovej ponuky sa prekopírujú osobitne a priložia sa k projektovej zmluve.
1. Ak je zmluva vytvorená úplne od začiatku, systém prehľadá cenníky, ktoré sú pripojené k cenníkom projektu pre obchodný vzťah. Ak k záznamu obchodného vzťahu nie sú pripojené cenníky projektu, systém prehľadá predajné cenníky pripojené k parametrom projektu, ktoré sa zhodujú s menou zmluvy projektu.
1. Potom systém skontroluje účinnosť cenníkov podľa dátumu, ktorý zodpovedá rozsahu dátumov zmluvy projektu. Konkrétne dátum vytvorenia zmluvy.
1. Ak existuje viac cenníkov s účinnosťou zmluvy k dátumu, všetky cenníky sú predvolene nastavené pre zmluvu.
1. Ak k dátumu uzavretia zmluvy nie sú platné žiadne cenníky, pre zmluvu nebudú predvolené žiadne cenníky projektu. V zmluve projektu sa zobrazí varovné hlásenie. V hlásení sa uvádza, že skutočné údaje a odhady týkajúce sa projektu nebudú ocenené, pretože k nim nie sú priložené žiadne cenníky projektu.

## <a name="cost-price-lists"></a>Cenníky obstarávacích cien

Obstarávacie cenníky nie sú predvolene nastavené na žiadnu entitu v rámci Project Operations. Stanovenie obstarávacieho cenníka, ktorý sa má použiť pre náklady projektu, prebieha vždy na báze transakcie. Systém dokončí nasledujúci proces, aby určil, ktorý cenník sa má použiť pre náklady na projekt:

1. Systém prehľadá cenníky, ktoré sú pripojené k zmluvnej organizačnej jednotke projektu.
1. Potom systém prehľadá účinnosť cenníkov podľa dátumu, ktoré sú spárované s dátumom s kontextom prichádzajúceho odhadu alebo skutočným kontextom.

    - *Kontext odhadu* označuje ktorýkoľvek z troch kontextov odhadu v Project Operations:

        - Riadok s odhadom projektu
        - Podrobnosti o riadku cenovej ponuky
        - Podrobnosti o riadku zmluvy

    - *Kontext skutočnej hodnoty* označuje ktorýkoľvek z troch zdrojov skutočných hodnôt v Project Operations:

       - Záznamy v účtovnom denníku vstupov, ktoré sú vytvorené manuálne, alebo opravné záznamy v účtovnom denníku, ktoré sú vytvorené v denníku opráv
       - Záznamy v účtovnom denníku, ktoré sa vytvárajú počas odosielania denníkov času, výdavkov alebo použitia materiálu
       - Podrobnosti o riadku faktúry

    Keď Project Operations páruje dátum účinnosti prichádzajúceho záznamu v účtovnom denníku alebo detailu riadka faktúry v *kontexte skutočných hodnôt*, používa pole **Dátum transakcie**.

    - Ak pre dátum kontextu prichádzajúceho odhadu alebo skutočného kontextu platí viac cenníkov, vyberie sa naposledy vytvorený cenník.
    - Ak k zmluvnej organizačnej jednotke projektu nie sú pripojené žiadne cenníky, systém prehľadá obstarávacie cenníky, ktoré sú pripojené k parametrom projektu, ktoré zodpovedajú mene projektu.

## <a name="enable-multi-currency-cost-price-list"></a>Povoliť cenník obstarávacích cien vo viacerých menách

Toto nastavenie nájdete v časti **Nastavenia** \> **Parametre**. Predvolená hodnota je **Nie**.

Keď je toto nastavenie povolené (to znamená, že hodnota je nastavená na **Áno**), systém sa správa takto:

- Umožňuje priradiť k organizačnej jednotke cenníky obstarávacích cien v ľubovoľnej mene. Napríklad cenník obstarávacích cien v mene EUR môže byť pripojený k organizačnej jednotke v mene USD. Systém bude naďalej overovať, že cenníky obstarávacích cien, ktoré sú pripojené k organizačnej jednotke, nemajú prekrývajúcu sa dátumovú účinnosť.
- Overuje, že cenníky obstarávacích cien, ktoré sú pripojené k parametrom projektu, nemajú prekrývajúcu sa dátumovú účinnosť, aj keď majú rôzne meny. Toto správanie sa líši od predvoleného správania (t. j. správania, keď je hodnota nastavená na **Nie**). V predvolenom správaní sa používajú iba cenníky obstarávacích cien, ktoré majú **rovnakú** menu a sú overené, že v nich nedochádza k prekrývaniu dátumov účinnosti.
- Pre kontext prichádzajúcej transakcie určuje cenník obstarávacích cien len na základe dátumu účinnosti. Toto správanie sa líši od predvoleného správania, kde systém vyberie cenník obstarávacích cien, ktorý sa zhoduje s menou projektu a dátumom účinnosti.

Z dôvodu týchto zmien v správaní budú zákazníci Project Operations schopní udržiavať globálny cenník obstarávacích cien, ktorý bude relevantný pre celú spoločnosť. Nebudú musieť mať cenníky v každej mene prevádzky. Globálny cenník bude mať dátumovú účinnosť a umožní nastavenie nákladových sadzieb v akejkoľvek mene pre konkrétnu kombináciu hodnôt cenovej dimenzie. Mena cenníka obstarávacích cien sa používa iba na zadanie predvolených hodnôt, keď sa vytvárajú záznamy položiek **Ceny rolí**, **Ceny kategórií** a **Cenník**. Nepoužije sa na stanovenie cenníka.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
