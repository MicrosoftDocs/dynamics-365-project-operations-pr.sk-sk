---
title: Stanovte nákladové sadzby pre odhady a skutočné skutočnosti založené na projekte
description: Tento článok poskytuje informácie o tom, ako sa určujú nákladové sadzby pre odhady a skutočné hodnoty založené na projekte.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475298"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Stanovte nákladové sadzby pre odhady a skutočné skutočnosti založené na projekte

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Na určenie nákladových cien na základe odhadov a skutočností v spoločnosti Microsoft Dynamics 365 Project Operations, systém najprv použije dátum a menu v prichádzajúcom odhade alebo skutočnom kontexte na určenie predajného cenníka. V skutočnom kontexte konkrétne systém používa **Dátum transakcie** na určenie, ktorý cenník je platný. The **Dátum transakcie** hodnota vstupného odhadu alebo skutočnej hodnoty sa porovnáva s **Efektívny štart (nezávislý od časového pásma)** a **Efektívny koniec (nezávislý od časového pásma)** hodnoty v cenníku. Po určení cenníka nákladov systém určí nákladovú sadzbu.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Stanovenie nákladových sadzieb v odhadovaných a skutočných kontextoch pre čas

Odhadnúť kontext pre **Čas** odkazuje na:

- Podrobnosti o riadku cenovej ponuky pre **Čas**.
- Podrobnosti zmluvnej linky pre **Čas**.
- Priradenia zdrojov k projektu.

Skutočný kontext pre **Čas** odkazuje na:

- Riadky denníka zápisov a opráv pre **Čas**.
- Riadky denníka, ktoré sa vytvoria pri odoslaní časového záznamu.

Po určení cenníka nákladov systém vykoná nasledujúce kroky na zadanie predvolenej nákladovej sadzby.

1. Systém zodpovedá kombinácii **Role**, **poskytujúca zdroje**, a **Jednotka zdrojov** polia v odhadovanom alebo skutočnom kontexte pre **Čas** oproti cenovým líniám rol v cenníku. Toto párovanie predpokladá, že pre cenu práce používate štandardné cenové dimenzie. Ak ste systém nakonfigurovali tak, aby zodpovedal iným poliam alebo iným poliam **Role**, **poskytujúca zdroje** a **Jednotka zdrojov**, na získanie zodpovedajúcej cenovej línie roly sa používa iná kombinácia.
1. Ak systém nájde cenovú líniu role, ktorá má nákladovú sadzbu pre **Role**, **poskytujúca zdroje**, a **Jednotka zdrojov** kombinácia, táto nákladová sadzba sa použije ako predvolená nákladová sadzba.
1. Ak sa systém nezhoduje s **Role**, **poskytujúca zdroje**, a **Jednotka zdrojov** hodnoty, zruší dimenziu, ktorá má najnižšiu prioritu, vyhľadá riadky cien rolí, ktoré sa zhodujú s ďalšími dvoma hodnotami dimenzie, a pokračuje v postupnom znižovaní dimenzií, kým sa nenájde zodpovedajúci riadok ceny role. Sadzba nákladov z tohto záznamu sa použije ako predvolená sadzba nákladov. Ak systém nenájde zodpovedajúci riadok s cenou roly, cena sa nastaví na **0** štandardne (nula).

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

[!INCLUDE[footer-include](../includes/footer-banner.md)]
