---
title: Vytváranie šablóny projektu pomocou funkcie kopírovania projektu
description: Táto téma poskytuje informácie o tom, ako vytvoriť šablóny projektu pomocou vlastnej akcie kopírovania projektu.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb49109e8c199bc4569702ae844a19985534294d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084304"
---
# <a name="develop-project-templates-with-copy-project"></a>Vytváranie šablóny projektu pomocou funkcie kopírovania projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations podporuje schopnosť kopírovať projekt a vrátiť všetky priradenia späť k všeobecným zdrojom, ktoré predstavujú rolu. Zákazníci môžu pomocou tejto funkcie zostaviť základné šablóny projektu.

Keď vyberiete **Kopírovať projekt** , aktualizuje sa stav cieľového projektu. Použite **Dôvod stavu** na určenie, kedy je akcia kopírovania dokončená. Výberom možnosti **Kopírovať projekt** sa aktualizuje aj počiatočný dátum projektu na aktuálny počiatočný dátum, ak sa v entite cieľového projektu nezistí žiadny cieľový dátum.

## <a name="copy-project-custom-action"></a>Vlastná akcia kopírovania projektu 

### <a name="name"></a>Meno 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Vstupné parametre
Existujú tri vstupné parametre:

| Parameter          | Zadať   | Hodnoty                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** alebo **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Odkaz na entitu | Zdrojový projekt |
| Cieľ             | Odkaz na entitu | Cieľový projekt |


- **{"clearTeamsAndAssignments":true}** : Predvolené správanie pre Project for Web, ktoré odstráni všetky priradenia a členov tímu.
- **{"removeNamedResources": true}** Predvolené správanie pre Project Operations, ktoré vráti priradenia k všeobecným zdrojom.

Ďalšie predvolené hodnoty akcií nájdete v časti [Použitie akcií Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Zadajte polia, ktoré chcete kopírovať 
Po vyvolaní akcie bude funkcia **Kopírovať projekt** prehľadávať zobrazenie projektu **Kopírovať stĺpce projektu** na určenie, ktoré polia sa majú kopírovať pri kopírovaní projektu.
