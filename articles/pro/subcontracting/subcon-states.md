---
title: Prechody stavov v rámci subdodávateľskej zmluvy
description: Tento článok vysvetľuje prechody stavu v subdodávateľskej zmluve v Microsoft Dynamics 365 Project Operations pri vytvorení, vykonaní a zatvorení subdodávateľskej zmluvy.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522954"
---
# <a name="state-transitions-on-a-subcontract"></a>Prechody stavov v rámci subdodávateľskej zmluvy 

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok vysvetľuje prechody stavu v subdodávateľskej zmluve v Microsoft Dynamics 365 Project Operations. Každý sta je reprezentovaný ako koncept, potvrdený, uzavretý alebo zrušený. Nasledujúci obrázok zobrazuje prechody stavov.

![Model stavu subdodávateľskej zmluvy](../media/SubconStates.png)  

Nasledujúca tabuľka poskytuje opis, čo každý stav predstavuje v životnom cykle subdodávateľskej zmluvy v Project Operations.

| State | Description | Povolené prechody |
| --- | --- | --- |
| Koncept | Predstavuje počiatočný stav subdodávateľskej zmluvy. Prebiehajú rokovania s dodávateľom. Riadky a ceny podliehajú zmenám. Subdodávateľská zmluva v tomto stave môže byť použitá na odhad a personálne požiadavky projektu na zdroje a materiály. Môže sa tiež vzťahovať na čas, výdavky a spotrebu materiálu v projekte. Subdodávateľská zmluva v tomto stave sa nedá upravovať a odstrániť. | Potvrdené |
| Potvrdené | Toto predstavuje etapu subdodávateľskej zmluvy po dokončení rokovaní s dodávateľom o cenách a nakupovaných riadkových položkách. Samotné dodávanie materiálov a/alebo prác subdodávateľskými zdrojmi však stále prebieha. Subdodávateľská zmluva v tomto stave môže byť použitá na odhad a personálne požiadavky projektu na zdroje a materiály. Môže sa tiež vzťahovať na čas, výdavky a spotrebu materiálu v projekte. Subdodávateľská zmluva v tomto stave sa nedá upravovať ani odstrániť. Tlačidlo **Zrušiť** umožňuje zrušiť potvrdenú subdodávateľskú zmluvu. Tlačidlo **Znova otvoriť** vám umožní znova otvoriť subdodávateľskú zmluvu a vrátiť ju späť do stavu **Koncept**. Použite tlačidlo **Zavrieť** na zatvorenie potvrdenej subdodávateľskej zmluvy. | Zatvorené <br> Zrušená <br> Koncept |
| Zatvorené | Tento stav predstavuje etapu subdodávateľskej zmluvy, kedy už je dokončená dodávka materiálu a/alebo práce zo subdodávateľských zdrojov. Subdodávateľská zmluva v tomto stave už nemôže byť použitá na odhad a personálne požiadavky projektu na zdroje a materiály. Už sa tiež nemôže vzťahovať na čas, výdavky a spotrebu materiálu v projekte. Subdodávateľská zmluva v tomto stave sa nedá upravovať ani odstrániť. | None |
| Zrušená | Tento stav predstavuje etapu subdodávateľskej zmluvy, kedy už nie je viac potrebná dodávka materiálu a/alebo práce zo subdodávateľských zdrojov. Subdodávateľská zmluva v tomto stave sa nedá použiť na odhad a personálne projektové požiadavky na zdroje a materiály, ani sa na ňu nedá odkazovať na čas, náklady a spotrebu materiálu v projekte. Subdodávateľská zmluva v tomto stave sa nedá upravovať ani odstrániť. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
