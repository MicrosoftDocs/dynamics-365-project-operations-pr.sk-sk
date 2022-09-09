---
title: Stanovte predajné ceny pre odhady projektu a skutočné skutočnosti
description: Tento článok poskytuje informácie o tom, ako sa určujú predajné ceny pre odhady a skutočné hodnoty projektu.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410138"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Stanovte predajné ceny pre odhady projektu a skutočné skutočnosti

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Určenie predajných cien na základe odhadov a skutočností v spoločnosti Microsoft Dynamics 365 Project Operations, systém najprv použije dátum a menu v prichádzajúcom odhade alebo skutočnom kontexte na určenie predajného cenníka. V skutočnom kontexte konkrétne systém používa **Dátum transakcie** na určenie, ktorý cenník je platný. Po určení predajného cenníka systém určí predajnú alebo fakturačnú sadzbu.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Určenie predajných sadzieb na skutočných a odhadovaných riadkoch pre čas

Odhadnúť kontext pre **Čas** odkazuje na:

- Podrobnosti o riadku cenovej ponuky pre **Čas**.
- Podrobnosti zmluvnej linky pre **Čas**.
- Priradenia zdrojov k projektu.

Skutočný kontext pre **Čas** odkazuje na:

- Riadky denníka zápisov a opráv pre **Čas**.
- Riadky denníka, ktoré sa vytvoria pri odoslaní časového záznamu.
- Podrobnosti o riadku faktúry za **Čas**. 

Po určení cenníka predaja systém vykoná nasledujúce kroky na zadanie predvolenej fakturačnej sadzby.

1. Systém zodpovedá kombinácii **Role** a **Jednotka zdrojov** polia v odhadovanom alebo skutočnom kontexte pre **Čas** oproti cenovým líniám rol v cenníku. Táto zhoda predpokladá, že pre fakturačné sadzby používate preddefinované cenové dimenzie. Ak ste ceny nakonfigurovali tak, aby boli založené na iných poliach ako alebo naviac **Role** a **Jednotka zdrojov**, táto kombinácia polí sa používa na získanie zodpovedajúcej cenovej línie role.
1. Ak systém nájde cenovú líniu role, ktorá má účtovanú sadzbu pre **Role** a **Jednotka zdrojov** táto účtovná sadzba sa použije ako predvolená účtovná sadzba.
1. Ak sa systém nezhoduje s **Role** a **Jednotka zdrojov** hodnoty, načíta cenové línie rolí, ktoré majú zhodné hodnoty pre **Role** pole, ale hodnoty null pre **Jednotka zdrojov** lúka. Keď systém nájde zodpovedajúci cenový záznam roly, fakturovaná sadzba z tohto záznamu sa použije ako predvolená fakturačná sadzba. Toto párovanie predpokladá predpripravenú konfiguráciu pre relatívnu prioritu **Role** proti **Jednotka zdrojov** ako rozmer predajnej ceny.

> [!NOTE]
> Ak nakonfigurujete inú prioritu **Role** a **Jednotka zdrojov** polia, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, predchádzajúce správanie sa zodpovedajúcim spôsobom zmení. Systém načítava cenové záznamy rolí, ktoré majú hodnoty, ktoré zodpovedajú každej hodnote cenovej dimenzie v poradí podľa priority. Riadky, ktoré majú pre tieto dimenzie nulové hodnoty, sú posledné.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Určenie predajných sadzieb na skutočných a odhadovaných riadkoch pre náklady

Odhadnúť kontext pre **Výdavok** odkazuje na:

- Podrobnosti o riadku cenovej ponuky pre **Výdavok**.
- Podrobnosti zmluvnej linky pre **Výdavok**.
- Riadky odhadu výdavkov na projekte.

Skutočný kontext pre **Výdavok** odkazuje na:

- Riadky denníka zápisov a opráv pre **Výdavok**.
- Riadky denníka, ktoré sa vytvoria pri odoslaní nákladového záznamu.
- Podrobnosti o riadku faktúry za **Výdavok**. 

Po určení cenníka predaja systém vykoná nasledujúce kroky na zadanie predvolenej jednotkovej predajnej ceny.

1. Systém zodpovedá kombinácii **Kategória** a **Jednotka** polia na riadku odhadu pre **Výdavok** oproti cenovým radom kategórie v cenníku.
1. Ak systém nájde cenovú líniu kategórie, ktorá má predajnú sadzbu pre **Kategória** a **Jednotka** že predajná sadzba sa použije ako predvolená predajná sadzba.
1. Ak systém nájde zodpovedajúcu cenovú líniu kategórie, na zadanie predvolenej predajnej ceny sa môže použiť metóda tvorby cien. Nasledujúca tabuľka zobrazuje predvolené správanie nákladových cien v projektových operáciách.

    | Kontext | Spôsob oceňovania | Predvolená cena |
    | --- | --- | --- |
    | Odhadované | Jednotková cena | Na základe cenovej línie kategórie. |
    |        | V rámci nákladov | 0.00 |
    |        | Prirážka nad rámec nákladov | 0.00 |
    | Skutočnosť | Jednotková cena | Na základe cenovej línie kategórie. |
    |        | V rámci nákladov | Na základe súvisiacich skutočných nákladov. |
    |        | Prirážka nad rámec nákladov | Prirážka sa aplikuje, ako je definovaná líniou ceny kategórie, na sadzbu jednotkových nákladov súvisiacich skutočných nákladov. |

1. Ak sa systém nezhoduje s **Kategória** a **Jednotka** hodnoty, je nastavený predajný kurz **0** štandardne (nula).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Stanovenie predajných sadzieb na skutočných a odhadovaných riadkoch pre materiál

Odhadnúť kontext pre **Materiál** odkazuje na:

- Podrobnosti o riadku cenovej ponuky pre **Materiál**.
- Podrobnosti zmluvnej linky pre **Materiál**.
- Riadky odhadu materiálu na projekte.

Skutočný kontext pre **Materiál** odkazuje na:

- Riadky denníka zápisov a opráv pre **Materiál**.
- Riadky denníka, ktoré sa vytvoria pri odoslaní denníka použitia materiálu.
- Podrobnosti o riadku faktúry za **Materiál**. 

Po určení cenníka predaja systém vykoná nasledujúce kroky na zadanie predvolenej jednotkovej predajnej ceny.

1. Systém zodpovedá kombinácii **Produkt** a **Jednotka** polia na riadku odhadu pre **Materiál** oproti riadkom cenníkovej položky na cenníku.
1. Ak systém nájde riadok položky cenníka, ktorý má predajnú sadzbu pre **Produkt** a **Jednotka** kombinácia, a ak je to spôsob oceňovania **Suma meny**, použije sa predajná cena, ktorá je uvedená na riadku cenníka. 
1. Ak **Produkt** a **Jednotka** hodnoty polí sa nezhodujú, alebo ak je metóda určovania cien iná ako **Suma meny**, predajná sadzba je nastavená na **0** štandardne (nula). Toto správanie sa vyskytuje, pretože Project Operations podporuje iba **Suma meny** spôsob oceňovania materiálov, ktoré sa používajú na projekte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
