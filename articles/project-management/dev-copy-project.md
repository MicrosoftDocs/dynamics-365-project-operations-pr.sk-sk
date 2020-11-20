---
title: Vytváranie šablóny projektu pomocou funkcie kopírovania projektu
description: Táto téma poskytuje informácie o tom, ako vytvoriť šablóny projektu pomocou vlastnej akcie kopírovania projektu.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131632"
---
# <a name="develop-project-templates-with-copy-project"></a>Vytváranie šablóny projektu pomocou funkcie kopírovania projektu

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations podporuje schopnosť kopírovať projekt a vrátiť všetky priradenia späť k všeobecným zdrojom, ktoré predstavujú rolu. Zákazníci môžu pomocou tejto funkcie zostaviť základné šablóny projektu.

Keď vyberiete **Kopírovať projekt**, aktualizuje sa stav cieľového projektu. Použite **Dôvod stavu** na určenie, kedy je akcia kopírovania dokončená. Výberom možnosti **Kopírovať projekt** sa aktualizuje aj počiatočný dátum projektu na aktuálny počiatočný dátum, ak sa v entite cieľového projektu nezistí žiadny cieľový dátum.

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


- **{"clearTeamsAndAssignments":true}**: Predvolené správanie pre Project for Web, ktoré odstráni všetky priradenia a členov tímu.
- **{"removeNamedResources": true}** Predvolené správanie pre Project Operations, ktoré vráti priradenia k všeobecným zdrojom.

Ďalšie predvolené hodnoty akcií nájdete v časti [Použitie akcií Web API](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>Zadajte polia, ktoré chcete kopírovať 
Po vyvolaní akcie bude funkcia **Kopírovať projekt** prehľadávať zobrazenie projektu **Kopírovať stĺpce projektu** na určenie, ktoré polia sa majú kopírovať pri kopírovaní projektu.
