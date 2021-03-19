---
title: Čo je nové v marci 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Project Operations z marca 2021, pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
manager: tfehr
ms.date: 03/03/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 95a9251707de3699322471535aa93070ba4fb2ae
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500041"
---
# <a name="whats-new-march-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové v marci 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.8.0.91 
- Projektový manažment a účtovanie v prostredí Dynamics 365 Finance verzie 10.0.16 

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse


| **Oblasť funkcií** | **Číslo odkazu** | **Aktualizácia kvality** |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2133873 | Opravilo sa zobrazenie symbolu meny **Jednotková predajná cena** na mriežke **Odhady výdavkov**. |
| Fakturácia a tvorba cien | 2174616 | Keď získate cenovú ponuku, na vlastný cenník zmluvy sa odkazuje v podrobnostiach riadku zmluvy, ktoré sa skopírujú z cenovej ponuky. |
| Správa príležitostí | 2167475 | Pevná suma dane v opravnej faktúre, z ktorej vzišiel nevyfakturovaný skutočný záznam. |
| Správa príležitostí | 2176285 | Suma dane sa nesmie kopírovať z podrobností v predajnom riadku zmluvy/cenovej ponuky do podrobností v nákladovom riadku zmluvy/cenovej ponuky. |
| Správa príležitostí | 2188079 | Pravidlo rozdelenej fakturácie sa nesmie vytvoriť pre zmluvy, ktoré nie sú založené na práci. |
| Plánovanie a sledovanie | 2125274 | Atribút **Mapa duálneho zápisu projektu** pre **Mapovanie dátumu začatia projektu** sa aktualizovala z **msdyn\_taskearlieststart** na **msdyn\_actualstart**. |
| Plánovanie a sledovanie | 2138853 | Funkcia kopírovania projektu bola aktualizovaná, aby sa zabezpečilo, že riadky odhadu výdavkov, ktoré odkazujú na úlohy, sa skopírujú do cieľového projektu. |
| Plánovanie a sledovanie | 2154306 | Opravili sa problémy s odstránením odhadov výdavkov v aplikácii Project Operations pre scenáre založené na zdrojoch. |
| Plánovanie a sledovanie | 2173259 | Funkcia kopírovania projektu bola aktualizovaná, aby sa zabezpečilo, že v určitých scenároch nezobrazuje chybové hlásenie **Kopíruje sa štruktúra WBS**. |
| Čas a výdavky | 2148910 | Opravil sa problém so stránkou **Upraviť záznam** na mriežke **Zadanie času**. |
| Čas a výdavky | 2159798 | Sprísnili sa kontroly, aby sa zabezpečilo, že schválené záznamy výdavkov nebude možné upravovať. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektový manažment a účtovníctvo v rámci Dynamics 365 Finance

Ďalšie informácie nájdete v sekcii [Čo je nové v januári 2021 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch](whats-new-jan-2021-resource-based.md).

## <a name="regulatory-updates"></a>Regulačné aktualizácie

Informácie o regulačných aktualizáciách pre aplikácie Finance and Operations sú uvedené v časti [Regulačné aktualizácie](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates). Ďalším spôsobom, ako sa dozvedieť o regulačných aktualizáciách, je prihlásiť sa do služby LCS a pozrieť si plánované aktualizácie právnych predpisov pomocou nástroja na vyhľadávanie problémov. Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny, typu funkcie a vydania.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
