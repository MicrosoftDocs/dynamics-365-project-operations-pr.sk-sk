---
title: Konfigurácia tabule plánovania s cieľom zobraziť zmluvných pracovníkov a kapacitu na základe subdodávateľskej zmluvy
description: Tento článok popisuje, ako nakonfigurovať tabuľu plánovania v Microsoft Dynamics 365 Project Operations, aby zobrazovala kapacitu subdodávateľských zdrojov pri personálnom zabezpečení požiadaviek na zdroje projektu.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262236"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigurácia tabule plánovania s cieľom zobraziť zmluvných pracovníkov a kapacitu na základe subdodávateľskej zmluvy 

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tabuľu plánovania v Microsoft Dynamics 365 Project Operations možno použiť na vyhľadávanie zdrojov dvoma spôsobmi:

- Všeobecné vyhľadávanie zdrojov bez kontextu akýchkoľvek špecifických požiadaviek na zdroje založených na projekte.
- Vyhľadávanie zdrojov špecifických pre požiadavku, kde požiadavka projektu poskytne kontext pre navrhované zdroje.

Ak chcete upozorniť tabuľu plánovania na kapacitu subdodávateľských zdrojov a zmluvných pracovníkov, musíte vykonať aktualizácie nastavení tabule plánovania. Tieto metriky aktualizácie zahŕňajú: 
- Aktualizujte nastavenia tabule plánovania pre všeobecné vyhľadávanie zdrojov.
- Aktualizujte nastavenia tabule plánovania pre vyhľadávanie zdrojov na základe požiadaviek.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Aktualizácia nastavenia tabule plánovania pre všeobecné vyhľadávanie zdrojov
### <a name="update-filters-for-general-resource-search"></a>Aktualizácia filtrov pre všeobecné vyhľadávanie zdrojov
Keď hľadáte zdroj, filtre dostupné na tabuli plánovania by sa mali aktualizovať, aby ste mohli vyhľadávať aj externé zdroje zadaním niektorého alebo všetkých nasledujúcich údajov:
  - Typ pracovníka, či by uvedené zdroje mali byť zmluvnými pracovníkmi alebo zamestnancami.
  - Dodávateľská spoločnosť, do ktorej by mal zdroj patriť.
  - Zdroje, ktoré patria ku konkrétnej subdodávateľskej zmluve alebo riadku subdodávateľskej zmluvy.
    
### <a name="update-retrieve-resource-query"></a>Aktualizácia dotazu na načítanie zdrojov
Dotaz používaný na vyhľadávanie by sa mal tiež aktualizovať, aby používal tieto dodatočné atribúty filtra. Pomocou nasledujúcich krokov aktualizujte konfiguráciu tabule plánovania pre všeobecné vyhľadávanie zdrojov:  
1. Otvorte **Nastavenia tabule plánovania** pre konkrétnu tabuľu plánovania.
2. Otvorte kartu **Všeobecné nastavenia** a prejdite na **Iné nastavenia**.
3. V zozname nastavení v tejto sekcii aktualizujte **Rozloženie filtra** na **Predvolené rozloženie filtra pre Project Operations Lite**.
4. Aktualizujte **Dotaz na načítanie zdrojov** na **Predvolený dotaz na načítanie zdrojov pre Project Operations Lite**.

![Aktualizácia nastavenia tabule plánovania pre všeobecné vyhľadávanie zdrojov](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Aktualizácia nastavenia tabule plánovania pre vyhľadávanie zdrojov na základe požiadaviek
### <a name="update-filters-for-requirement-specific-resource-search"></a>Aktualizácia filtrov pre vyhľadávanie zdrojov špecifického pre požiadavku 
Keď hľadáte zdroj, filtre dostupné na tabuli plánovania by sa mali aktualizovať, aby ste mohli vyhľadávať aj externé zdroje zadaním niektorého alebo všetkých nasledujúcich údajov:
 - Typ pracovníka, či by uvedené zdroje mali byť zmluvnými pracovníkmi alebo zamestnancami.
 - Dodávateľská spoločnosť, do ktorej by mal zdroj patriť.
 - Zdroje, ktoré patria ku konkrétnej subdodávateľskej zmluve alebo riadku subdodávateľskej zmluvy.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Aktualizácia dotazu na získanie zdroja pre vyhľadávanie zdroja špecifického pre požiadavku 
Dotaz používaný na vyhľadávanie by sa mal tiež aktualizovať, aby používal tieto dodatočné atribúty filtra. Pomocou nasledujúcich krokov aktualizujte konfiguráciu tabule plánovania pre vyhľadávanie zdroja špecifického pre požiadavku:

1. Otvorte **Nastavenia tabule plánovania** pre konkrétnu tabuľu plánovania a potom vyberte **Otvoriť predvolené nastavenia** na otvorenie nastavení na vyhľadávanie podľa požiadaviek.
2. Otvorte kartu **Všeobecné nastavenia** a prejdite na **Iné nastavenia**.
3. V zozname nastavení v tejto sekcii aktualizujte **Rozloženie filtra** na **Predvolené rozloženie filtra pre Project Operations Lite**.
4. Aktualizujte **Dotaz na načítanie zdrojov** na **Predvolený dotaz na načítanie zdrojov pre Project Operations Lite**.
5. Otvorte kartu **Typy plánov** a prejdite na **Projekt**.
6. V nastaveniach pre **Projekt** aktualizujte **Dotaz na načítanie zdrojov asistenta plánovania** na **Predvolený dotaz na načítanie zdrojov pre Project Operations Lite** a aktualizujte **Dotaz na načítanie obmedzení asistenta plánovania** na **Predvolený dotaz na načítanie obmedzení pre Project Operations**.

![Aktualizácia nastavenia tabule plánovania pre vyhľadávanie zdrojov na základe požiadaviek](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
