---
title: Nakonfigurujte tabuľu plánovania tak, aby zobrazovala zmluvných pracovníkov a subdodávateľskú kapacitu
description: Táto téma popisuje, ako nakonfigurovať plánovaciu tabuľu v spoločnosti Microsoft Dynamics 365 Project Operations ukázať kapacitu subdodávateľských zdrojov pri personálnom zabezpečení požiadaviek na zdroje projektu.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903095"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Nakonfigurujte tabuľu plánovania tak, aby zobrazovala zmluvných pracovníkov a subdodávateľskú kapacitu 

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Schedule Board v Microsofte Dynamics 365 Project Operations možno použiť na vyhľadávanie zdrojov dvoma spôsobmi:

- Všeobecné vyhľadávanie zdrojov bez kontextu akýchkoľvek špecifických požiadaviek na zdroje založené na projekte.
- Vyhľadávanie zdrojov špecifických pre požiadavku, kde požiadavka projektu poskytne kontext pre navrhované zdroje.

Ak chcete upozorniť tabuľu plánovania na kapacitu subdodávateľských zdrojov a zmluvných pracovníkov, musíte vykonať aktualizácie nastavení tabule plánovania. Tieto aktualizácie zahŕňajú: 
- Aktualizujte nastavenia tabule plánovania pre všeobecné vyhľadávanie zdrojov.
- Aktualizujte nastavenia plánovacej tabule pre vyhľadávanie zdrojov na základe požiadaviek.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Aktualizujte nastavenia tabule plánovania pre všeobecné vyhľadávanie zdrojov
### <a name="update-filters-for-general-resource-search"></a>Aktualizujte filtre pre všeobecné vyhľadávanie zdrojov
Keď hľadáte zdroj, filtre dostupné na tabuli plánovania by sa mali aktualizovať, aby ste mohli vyhľadávať aj externé zdroje zadaním niektorého alebo všetkých nasledujúcich údajov:
  - Typ pracovníka, či by uvedené zdroje mali byť zmluvnými pracovníkmi alebo zamestnancami.
  - Spoločnosť dodávateľa, ktorej by mal zdroj patriť.
  - Zdroje, ktoré patria ku konkrétnej subdodávke alebo subdodávke.
    
### <a name="update-retrieve-resource-query"></a>Aktualizovať dotaz na získanie zdroja
Dotaz používaný na vyhľadávanie by sa mal tiež aktualizovať, aby používal tieto dodatočné atribúty filtra. Pomocou nasledujúcich krokov aktualizujte konfiguráciu plánovacej tabule pre všeobecné vyhľadávanie zdrojov:  
1. Otvorené **Nastavenia tabule plánovania** pre konkrétnu plánovaciu radu.
2. Otvor **Všeobecné nastavenia** kartu a prejdite na **Iné nastavenia**.
3. V zozname nastavení v tejto časti aktualizujte **Rozloženie filtra** do **Predvolené rozloženie filtra pre Project Operations Lite**.
4. Aktualizovať **Dopyt na získanie zdrojov** do **Predvolený dotaz na zdroje na získanie pre Project Operations Lite**.

![Aktualizujte nastavenia tabule plánovania pre všeobecné vyhľadávanie zdrojov](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Aktualizujte nastavenia plánovacej tabule pre vyhľadávanie zdrojov na základe požiadaviek
### <a name="update-filters-for-requirement-specific-resource-search"></a>Aktualizujte filtre na vyhľadávanie zdrojov podľa požiadaviek 
Keď hľadáte zdroj, filtre dostupné na tabuli plánovania by sa mali aktualizovať, aby ste mohli vyhľadávať aj externé zdroje zadaním niektorého alebo všetkých nasledujúcich údajov:
 - Typ pracovníka, či by uvedené zdroje mali byť zmluvnými pracovníkmi alebo zamestnancami.
 - Spoločnosť dodávateľa, ktorej by mal zdroj patriť.
 - Zdroje, ktoré patria ku konkrétnej subdodávke alebo subdodávke.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Aktualizujte dotaz na získanie zdroja pre vyhľadávanie zdroja špecifického pre požiadavku 
Dotaz používaný na vyhľadávanie by sa mal tiež aktualizovať, aby používal tieto dodatočné atribúty filtra. Pomocou nasledujúcich krokov aktualizujte konfiguráciu plánovacej tabule pre vyhľadávanie zdrojov na základe požiadaviek:

1. Otvorené **Nastavenia tabule plánovania** pre konkrétnu plánovaciu tabuľu a potom vyberte **Otvorte Predvolené nastavenia** otvorte nastavenia pre vyhľadávanie podľa požiadaviek.
2. Otvor **Všeobecné nastavenia** kartu a prejdite na **Iné nastavenia**.
3. V zozname nastavení v tejto časti aktualizujte **Rozloženie filtra** do **Predvolené rozloženie filtra pre Project Operations Lite**.
4. Aktualizovať **Dopyt na získanie zdrojov** do **Predvolený dotaz na zdroje na získanie pre Project Operations Lite**.
5. Otvor **Typy rozvrhu** kartu a prejdite na **Projekt**.
6. V nastaveniach pre **Projekt**, aktualizovať **Dotaz na získanie zdrojov Asistenta plánovania** do **Predvolený dotaz na zdroje na získanie pre Project Operations Lite** a aktualizovať **Dotaz na získanie obmedzení asistenta plánovania** do **Predvolený dotaz na obmedzenia načítania pre Project Operations Lite**.

![Aktualizujte nastavenia plánovacej tabule pre vyhľadávanie zdrojov na základe požiadaviek](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
