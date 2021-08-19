---
title: Zálohy a zmluvy založené na preddavkoch
description: Táto téma poskytuje informácie o preddavkových zmluvných modeloch a zálohách v Project Operations.
author: rumant
ms.date: 10/20/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 87e275cb72f1edc5a2a9913b4aa47d461d1f3d3d9bf177bf0ffba8b463f4ce01
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994430"
---
# <a name="advances-and-retainer-based-contracts"></a>Zálohy a zmluvy založené na preddavkoch


_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations podporuje zmluvy založené na preddavkoch. Zmluva na základe preddavku je dohodnutá množina rovnako rozdelených platieb, za ktoré bude zákazníkovi fakturovaná počas celého trvania projektu. Tento typ zmluvy sa zvyčajne používa pre fakturačné modely založené na čase a materiáli alebo spotrebe, kde je potrebné poskytnúť zákazníkovi predvídateľnú faktúru a časový plán platieb. Skutočné výnosy nahromadené v každom období sa porovnajú s platbami prijatými od zákazníka na začiatku obdobia. V súlade s koncepciou modelu fakturácie za čas a materiál sa hodnoty výnosov nahromadené v každom období môžu líšiť v závislosti od vzniknutých nákladov. Ak nazhromaždený príjem presahuje sumu prijatú na začiatku obdobia, spoločnosť poskytujúca projekt by mohla:

- Zákazníkovi fakturovať iba prebytok 
- Odložiť odsúhlasenie výnosov na ďalšie fakturačné obdobie a na konci projektu urobiť jeden konečný účet za všetky zostávajúce nevyrovnané príjmy

Hlavný rozdiel medzi modelom kontraktu založeného na preddavku a modelom zmluvy s pevnou cenou v Project Operations je ten, že v modeli zmluvy s pevnou cenou nie je výška faktúry spojená alebo viazaná na vzniknuté náklady. Fakturácia sa riadi míľnikovým prístupom, ktorý je zosúladený s nákladmi vzniknutými v danom období. V zmluve na základe preddavkov sa výnosy, ktoré je možné fakturovať, zaznamenávajú na základe spôsobu fakturácie na riadku zmluvy. Ak je spôsob fakturácie časovo a vecne relevantný, fakturovateľný príjem sa viaže na náklady vzniknuté v danom období a môže sa v jednotlivých obdobiach líšiť. Zákazníkovi sa však fakturuje iba čiastka na periodickom preddavku. Systém používa inú faktúru na konci obdobia na porovnanie fakturovateľných výnosov zaznamenaných počas obdobia s čiastkou, za ktorú bol zákazníkovi fakturovaný na začiatku obdobia.

Výhodou tejto metódy je, že náklady zákazníka sa stávajú predvídateľnými v časovom rozvrhu, na rozdiel od typického časového a materiálového modelu. Organizácia poskytujúca projekt má tiež určitý priestor na pokrytie rizika úhrady vzniknutých nákladov v dôsledku zvýšenia rozsahu, ktoré by im model pevnej ceny neumožnil.

Okrem pravidelného harmonogramu založeného na preddavkovom mechanizme môže Project Operations zaznamenať jednorazový preddavok od zákazníka a zosúladiť ho s rôznymi nákladovými komponentmi projektu.

Preddavok v Project Operations nie je k dispozícii na použitie, kým nebude fakturovaný zákazníkovi. Toto je označené nasledujúcimi poľami v podskupine záloh a preddavkov.

| Pole | Popis | Nadväzujúci vplyv |
| --- | --- | --- |
| Dostupná suma | Suma, ktorá je k dispozícii na použitie v zázname preddavku či zálohy. | Kým nebude fakturovaná záloha alebo preddavok, nebude možné ju použiť, čo znamená, že dostupná suma bude nulová. |
| Využitá suma | Suma, ktorá už je k dispozícii na použitie v preddavku či zálohe. | Zálohu alebo preddavok je možné čiastočne vyrovnať na faktúre so skutočnými nákladmi, ktoré budú mať časť označenú ako už použitú alebo spotrebovanú. Zvyšok zálohy alebo preddavku je k dispozícii na vyrovnanie na budúcej faktúre so skutočnými nákladmi. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]