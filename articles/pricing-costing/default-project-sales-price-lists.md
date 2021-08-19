---
title: Predvolené cenníky
description: Táto téma poskytuje informácie o predvolených predajných a obstarávacích cenníkoch v Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a5e38e2f0b553b789956c6d73d481ab0ed2ce3a77815e7cf8c058a0b4666c558
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6989885"
---
# <a name="default-price-lists"></a>Predvolené cenníky

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

## <a name="sales-price-lists"></a>Predajné cenníky

Každá cenová ponuka a zmluva projektu v aplikácii Dynamics 365 Project Operations obsahuje predvolený predajný cenník. 

### <a name="price-list-default-on-project-quotes"></a>Predvolený cenník pre projektové cenové ponuky
Systém dokončí nasledujúci proces, aby určil, ktorý cenník je predvolený pre cenovú ponuku projektu:

1. Systém sleduje cenníky, ktoré sú pripojené k cenníkom projektov projektu pre obchodný vzťah. 
2. Ak sú k záznamu obchodného vzťahu pripojené cenníky projektu, systém prehľadá predajné cenníky pripojené k parametrom projektu, ktoré sa zhodujú s menou cenovej ponuky projektu.
3. Potom systém skontroluje účinnosť cenníkov podľa dátumu, ktorý zodpovedá rozsahu dátumov cenovej ponuky projektu. Konkrétne dátum vytvorenia cenovej ponuky.
4. Ak existuje viac cenníkov s účinnosťou cenovej ponuky projektu k dátumu, všetky cenníky sú predvolene nastavené pre cenovú ponuku projektu.
5. Ak k dátumu cenovej ponuky projektu nie sú v platnosti žiadne cenníky, v ponuke projektu nie je nastavený žiadny predvolený cenník projektu. V cenovej ponuke projektu sa zobrazí varovné hlásenie. V hlásení sa uvádza, že skutočné údaje a odhady týkajúce sa projektu nebudú ocenené, pretože k nim nie sú priložené žiadne cenníky projektu.

### <a name="price-list-default-on-project-contracts"></a>Predvolený cenník pre projektové zmluvy 
Systém dokončí nasledujúci proces, aby určil, ktorý cenník je predvolený pre zmluvu projektu:

1. Ak je zmluva vytvorená z cenovej ponuky, cenníky projektu z cenovej ponuky sa prekopírujú osobitne a priložia sa k projektovej zmluve.
2. Ak je zmluva vytvorená úplne od začiatku, systém prehľadá cenníky, ktoré sú pripojené k cenníkom projektu pre obchodný vzťah. Ak k záznamu obchodného vzťahu nie sú pripojené cenníky projektu, systém prehľadá predajné cenníky pripojené k parametrom projektu, ktoré sa zhodujú s menou zmluvy projektu.
4. Potom systém skontroluje účinnosť cenníkov podľa dátumu, ktorý zodpovedá rozsahu dátumov zmluvy projektu. Konkrétne dátum vytvorenia zmluvy.
5. Ak existuje viac cenníkov s účinnosťou zmluvy k dátumu, všetky cenníky sú predvolene nastavené pre zmluvu.
6. Ak k dátumu uzavretia zmluvy nie sú platné žiadne cenníky, pre zmluvu nebudú predvolené žiadne cenníky projektu. V zmluve projektu sa zobrazí varovné hlásenie. V hlásení sa uvádza, že skutočné údaje a odhady týkajúce sa projektu nebudú ocenené, pretože k nim nie sú priložené žiadne cenníky projektu.

## <a name="cost-price-lists"></a>Cenníky obstarávacích cien

Obstarávacie cenníky nie sú predvolene nastavené na žiadnu entitu v rámci Project Operations. Stanovenie obstarávacieho cenníka, ktorý sa má použiť ako náklad projektu, sa vykonáva vždy v danom okamihu. Systém dokončí nasledujúci proces, aby určil, ktorý cenník sa má použiť pre náklady na projekt:

1. Systém najskôr prehľadá cenníky, ktoré sú pripojené k zmluvnej organizačnej jednotke projektu.
2. Systém potom prehľadá účinnosť cenníkov podľa dátumu, ktoré sa zhodujú s dátumom prichádzajúceho riadku s odhadom alebo skutočnou hodnotou. V tejto situácii *riadok s odhadom* označuje všetky tri kontexty odhadu v Project Operations:

    - Riadok s odhadom projektu
    - Podrobnosti o riadku cenovej ponuky
    - Podrobnosti o riadku zmluvy
  
3. Ak existuje viac cenníkov s účinnosťou k dátumu pri prichádzajúcom odhade alebo skutočnej hodnote, vyberie sa naposledy vytvorený cenník.
4. Ak k zmluvnej organizačnej jednotke projektu nie sú pripojené žiadne cenníky, systém prehľadá obstarávacie cenníky pripojené k parametrom projektu, ktoré zodpovedajú mene projektu.
5. Potom systém prehľadá účinnosť cenníkov podľa dátumu, ktoré sa zhodujú s dátumom prichádzajúceho riadku s odhadom alebo skutočnou hodnotou. 
6. Ak existuje viac cenníkov s účinnosťou k dátumu pri prichádzajúcom odhade alebo skutočnej hodnote, vyberie sa naposledy vytvorený cenník.
7. Ak k parametrom projektu nie sú pripojené žiadne obstarávacie cenníky, ktoré sa zhodujú s menou a dátumom účinnosti, systém predvolene nastaví nákladovú sadzbu na nulu (0) v prichádzajúcom riadku s odhadom alebo skutočnom hodnotou.


[!INCLUDE[footer-include](../includes/footer-banner.md)]