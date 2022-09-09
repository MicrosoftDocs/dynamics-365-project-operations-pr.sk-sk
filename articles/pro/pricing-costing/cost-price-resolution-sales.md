---
title: Určite nákladové sadzby pre odhady projektu a skutočné skutočnosti
description: Tento článok poskytuje informácie o tom, ako sa určujú nákladové sadzby pre odhady a skutočné hodnoty projektu.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410178"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Určite nákladové sadzby pre odhady projektu a skutočné skutočnosti

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Na určenie cenníka nákladov a sadzieb nákladov v odhadovanom a skutočnom kontexte systém používa informácie v **Dátum**, **·**, a **zmluvná jednotka** oblasti súvisiaceho projektu.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Stanovenie nákladových sadzieb v odhadovaných a skutočných kontextoch pre čas

Odhadnúť kontext pre **Čas** odkazuje na:

- Podrobnosti o riadku cenovej ponuky pre **Čas**.
- Podrobnosti zmluvnej linky pre **Čas**.
- Priradenia zdrojov k projektu.

Skutočný kontext pre **Čas** odkazuje na:

- Riadky denníka zápisov a opráv pre **Čas**.
- Riadky denníka, ktoré sa vytvoria pri odoslaní časového záznamu.

Po určení cenníka nákladov systém vykoná nasledujúce kroky na zadanie predvolenej nákladovej sadzby.

1. Systém zodpovedá kombinácii **Role** a **Jednotka zdrojov** polia v odhadovanom alebo skutočnom kontexte pre **Čas** oproti cenovým líniám rol v cenníku. Toto párovanie predpokladá, že pre cenu práce používate štandardné cenové dimenzie. Ak ste systém nakonfigurovali tak, aby zodpovedal iným poliam alebo iným poliam **Role** a **Jednotka zdrojov**, na získanie zodpovedajúcej cenovej línie roly sa používa iná kombinácia.
1. Ak systém nájde cenovú líniu role, ktorá má nákladovú sadzbu pre **Role** a **Jednotka zdrojov** kombinácia, táto nákladová sadzba sa použije ako predvolená nákladová sadzba.
1. Ak sa systém nezhoduje s **Role** a **Jednotka zdrojov** hodnoty, načíta cenové línie rolí, ktoré majú zhodné hodnoty pre **Role** pole, ale hodnoty null pre **Jednotka zdrojov** lúka. Keď má systém zodpovedajúci cenový záznam roly, ako predvolená nákladová sadzba sa použije nákladová sadzba z tohto záznamu.

> [!NOTE]
> Ak nakonfigurujete inú prioritu **Role** a **Jednotka zdrojov** polia, alebo ak máte iné dimenzie, ktoré majú vyššiu prioritu, predchádzajúce správanie sa zodpovedajúcim spôsobom zmení. Systém načítava cenové záznamy rolí, ktoré majú hodnoty, ktoré zodpovedajú každej hodnote cenovej dimenzie v poradí podľa priority. Riadky, ktoré majú pre tieto dimenzie nulové hodnoty, sú posledné.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Stanovenie nákladových sadzieb na skutočných a odhadovaných riadkoch pre Výdavky

Odhadnúť kontext pre **Výdavok** odkazuje na:

- Podrobnosti o riadku cenovej ponuky pre **Výdavok**.
- Podrobnosti zmluvnej linky pre **Výdavok**.
- Odhady nákladov na projekt.

Skutočný kontext pre **Výdavok** odkazuje na:

- Riadky denníka zápisov a opráv pre **Výdavok**.
- Riadky denníka, ktoré sa vytvoria pri odoslaní nákladového záznamu.

Po určení cenníka nákladov systém vykoná nasledujúce kroky na zadanie predvolenej nákladovej sadzby.

1. Systém zodpovedá kombinácii **Kategória** a **Jednotka** polia v odhadovanom alebo skutočnom kontexte pre **Výdavok** oproti cenovým radom kategórie v cenníku.
1. Ak systém nájde cenovú líniu kategórie, ktorá má nákladovú sadzbu pre **Kategória** a **Jednotka** kombinácia, táto nákladová sadzba sa použije ako predvolená nákladová sadzba.
1. Ak sa systém nezhoduje s **Kategória** a **Jednotka** hodnoty, cena je nastavená na **0** štandardne (nula).
1. V kontexte odhadu, ak systém dokáže nájsť cenovú líniu zodpovedajúcej kategórie, ale metóda oceňovania je niečo iné ako **Cena za jednotku**, sadzba nákladov je nastavená na **0** štandardne (nula).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Stanovenie nákladových sadzieb na skutočných a odhadovaných riadkoch pre materiál

Odhadnúť kontext pre **Materiál** odkazuje na:

- Podrobnosti o riadku cenovej ponuky pre **Materiál**.
- Podrobnosti zmluvnej linky pre **Materiál**.
- Materiálové odhady na projekte.

Skutočný kontext pre **Materiál** odkazuje na:

- Riadky denníka zápisov a opráv pre **Materiál**.
- Riadky denníka, ktoré sa vytvoria pri odoslaní denníka použitia materiálu.

Po určení cenníka nákladov systém vykoná nasledujúce kroky na zadanie predvolenej nákladovej sadzby.

1. Systém využíva kombináciu **Produkt** a **Jednotka** polia v odhadovanom alebo skutočnom kontexte pre **Materiál** oproti riadkom cenníkovej položky na cenníku.
1. Ak systém nájde riadok položky cenníka, ktorý má nákladovú sadzbu pre **Produkt** a **Jednotka** kombinácia, táto nákladová sadzba sa použije ako predvolená nákladová sadzba.
1. Ak sa systém nezhoduje s **Produkt** a **Jednotka** hodnoty sa nastavia jednotkové náklady **0** štandardne (nula).
1. V odhadovanom alebo skutočnom kontexte, ak systém dokáže nájsť zodpovedajúci riadok cenníka, ale metóda oceňovania je iná ako **Suma meny**, jednotkové náklady sú nastavené na **0** predvolene. Toto správanie sa vyskytuje, pretože Project Operations podporuje iba **Suma meny** spôsob oceňovania materiálov, ktoré sa používajú na projekte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
