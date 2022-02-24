---
title: URčiť náklady na projekt a odhady výnosov
description: Ako na určenie nákladov na projekt a odhady príjmov v Project Service
author: ruhercul
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a91e988632d2b2cdebfe7fd17516c5d6886728fc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148842"
---
# <a name="determine-project-cost-and-revenue-estimates"></a>URčiť náklady na projekt a odhady výnosov 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Odhady projektu poskytujú finančné náhľady pre odhadovanú prácu a plánovanie v štruktúre rozdelenia prác projektu. Zobrazené odhady informuje vás o nákladoch a príjmoch vplyvu plánovaných prác. Zobrazenie odhadov poskytuje nástroj na zobrazenie informácií o celom rade preddefinovaných rozmerov, aby vás čo najlepšie informovali o finančnom vplyve projektu.  
  
## <a name="cost-and-sales-value-of-the-project"></a>Náklady a hodnota predaja projektu  
Cenníky [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] stanovujú cenu a sadzby fakturácie pre použité roly projektu. Na základe úlohy priradenej k úlohe v štruktúre rozdelenia práce v projekte môžete určiť vplyv nákladov a príjmov príslušnej práce.  
  
## <a name="cost-price-defaulting"></a>Predvolená suma obstarávacej ceny  
Každý projekt patrí k organizácii (určenej v poli projektu **vlastniaca jednotka**). Cenník prepojený s vlastniacou organizačnou jednotkou určuje obstarávaciu cenu jednotky. Možnosti [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] určujú obstarávacie ceny pre roly vyhľadávaním kombinácie roly, jednotky a organizačnej jednotky v cenníku obstarávacej ceny, čím sa zistí správna obstarávacia cena k efektívnemu dátumu na požadovaných riadkoch.  
  
Ak kombinácia roly, jednotky a organizačnej jednotky nemá za následok obstarávaciu cenu z cenníka vlastniacej jednotky, jednotka sa neberie do úvahy v prospech kombinácie roly a organizačnej jednotky. Ak tu je obstarávacia cena, táto cena sa prevedie na jednotku, ktorú ste si vybrali v riadku odhadu.  
  
Ak kombinácia roly a organizačnej jednotky nemá za následok obstarávaciu cenu, organizačná jednotka sa neberie do úvahy v prospech kombinácie jednotky a roly a cena sa v prípade potreby predvolene určí po použití prevodu.  
  
 Ak nie je stanovená cena za rolu, obstarávacia cena sa predvolene určí na hodnotu 0.00 riadku odhadu.  
  
 Všetky čiastky riadkov odhadov nákladov na projekt sú v mene vlastniacej organizačnej jednotky.  
  
## <a name="sales-price-defaulting"></a>Predvolená suma predajnej ceny  
Predajný cenník vychádza z entity predaja priradeného k projektu. Prepojení predajný cenník s cenovou ponukou alebo zmluvou určuje jednotkovú predajnú cenu. Ak ponuka alebo zmluva má vlastný cenník, tak sa pre odhady projektu použije predvolený predajný cenník. Ak neexistuje žiadne priradenie do predajných entít, predvolené predajné cenník nakonfigurované v parametroch nastavení bude predvolený zoznam predajných cien pre projekt. Každý riadok odhadu má zdroj organizačnej jednotky priradenej na uvádzanie organizačnej jednotky, z ktorej sa zdroje budú rezervovať na dokončenie úlohy. Predajná cena priradenej roly sa určuje podľa vyhľadávania pre kombináciu roly, jednotky a zdrojovej organizačnej jednotky v predajnom cenníku, čím sa získa správna predajná cena k efektívnemu dátumu v riadkoch odhadu.  
  
Ak kombinácia úlohu, jednotka a zdroj organizačná jednotka nemá mať za následok predajná cena zo zoznamu predajné ceny, systém nebude braný jednotky a hľadajte kombinácie zdrojov a úloha organizačnú jednotku. Ak sa nájde predajná cena, skonvertuje sa na jednotku zvolenú v riadku odhadu predaja.  
  
Ak systém nenájde cenu pre rolu, potom bude predajná cena nastavená na predvolenú hodnotu 0.00 riadku odhadu.  
  
Zobrazenie odhadov má mriežkové zobrazenie ukazujúce riadky odhadov s jednotkami a celkovými nákladmi a predajnou cenou.  
  
## <a name="time-phased-view-of-project-estimates"></a>Odhady času postupne zobrazenie projektu  
V časovom zobrazení odhadov projektu sa údaje projektu z mriežkového zobrazenia otáčajú predvolene podľa role a zobrazujú rozšírenie odhadovaných údajov naprieč časovou osou zvolenej časovej škály.  
  
## <a name="effort-estimate-allocation-based-on-task-mode"></a>Odhad pridelené na základe režimu úloh  
V zobrazení rozloženia na časové fázy je distribuovaný celkové úsilie odhadnúť úlohy pridelením určitého počtu hodín úsilie na jednotku počas zvoleného časového harmonogramu. V project service úloha režimu určuje, ako sa úsilie rozdeľovať medzi trvanie úlohy. Dva druhy pridelenia sú rovnomerné pridelenie a pridelenie podľa pracovnej doby. 
  
## <a name="work-hours-based-allocation"></a>Pridelenie založené na pracovnej dobe  
Režim automatického plánovania úloh pre úlohy upravuje, že počet zdrojov odhadovaných na úlohu, sa odhadujú na využitie pre plný pracovných hodín za deň. To platí pri prideľovaní úsilie rozdelením naprieč trvaním úloh aj v časovom zobrazení. Napríklad v "Deň" časový rámec úlohy odhaduje na dokončenie jeden zdroj, snaha pridelené za deň nepresiahne počet pracovných hodín za deň stanovený v kalendári projektu. Preto pridelené vždy zabezpečí, že zdroje sa odhadujú využívať počas celého dňa.  
  
## <a name="even-distribution"></a>Vyrovnaná distribúcia  
Režim manuálneho plánovania úloh nemusí brať zreteľ na pracovné hodiny, kalendár projektu ani počet zdrojov zadefinovaných v úlohe. Plán úlohy sa zakladá na vstupoch používateľa. Pre také úlohy pridelené na jednotku počas zvoleného časového harmonogramu nemá žiadne limitujúcim faktorom. Celkové úsilie na úlohu je rovnaké rozdelenie a pridelenie pre každú jednotku časové obdobie na zvolenej časovej osi.  
  
Týmto spôsobom režimu úlohy definované úlohy určuje rozdelenie úsilia alebo rozdelenie úsilia na jednotku časové obdobie v čase postupne odhady.  
  
## <a name="grouping-and-time-phasing-options"></a>Zoskupenie a možnosti fázovania času  
Toto zobrazenie vám pomôže pochopiť rozdelenie úsilia, cena a predaj odhady na základe deň, týždeň, mesiac alebo rok. Zoskupiť podľa možností umožní posun odhadov údajov na dvoch iných rozmerov: Kategória a zdroj. Na zobrazenie mriežky a časové usporiadanie zobrazenie si môžete vybrať polia, ktoré chcete zobraziť. Súčty pre každý z časových blokov sa zobrazia v dolnej časti s uvedením celkového odhadovaného úsilia, nákladov a predaja za deň, týždeň, mesiac alebo rok..  
  
Náklady a predajná cena je určená dňom účinnosti. Keď miera zmeny úlohy bude transparentnejšie časovým usporiadaním zobrazenia pri zobrazení údajov na odhad posunutý na zdroje a časovo fázovaný podľa týždňa.  
  
## <a name="expense-estimates"></a>Odhady nákladov  
Akékoľvek náklady, ktoré vzniknú v rámci projektu, ktoré sa priamo netýkajú práce sa rozšíria možno zaznamenať v projekte odhadov zobrazenie mriežky. Pomocou možnosti **Pridať odhad nákladov** v zobrazení mriežky, môžete to urobiť. Odhady výdavkov môžete zaznamenať pre konkrétnu úlohu alebo pre celý projekt. V týchto riadkoch môžete zvoliť kategórie výdavkov a zvoliť predbežný dátum, kedy sa očakáva vznik výdavkov. Ak súvisiace náklady a predajná cena zoznam predvolené ceny, alebo percentá značiek definovaných kategórií výdavkov, bude splácať odhad riadku združenia.  
  
### <a name="see-also"></a>Pozrite si tiež:  
 [Príručka projektového manažéra](../psa/project-manager-guide.md)
