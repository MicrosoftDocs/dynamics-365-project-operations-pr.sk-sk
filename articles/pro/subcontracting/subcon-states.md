---
title: Prechody štátov na subdodávku
description: Táto téma vysvetľuje prechody stavu na subdodávke v spoločnosti Microsoft Dynamics 365 Project Operations ako je subdodávka vytvorená, vykonaná a uzavretá.
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d67f4a3cd834c25462304c2d75c824427fcbd034
ms.sourcegitcommit: 04dc8d952e6da3ab3eb2a20131c6f7cee6040876
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/10/2021
ms.locfileid: "7903778"
---
# <a name="state-transitions-on-a-subcontract"></a>Prechody štátov na subdodávku 

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Táto téma vysvetľuje prechody stavu na subdodávke v Microsofte Dynamics 365 Project Operations. Každý štát je reprezentovaný ako koncept, potvrdený, uzavretý alebo zrušený. Nasledujúci obrázok znázorňuje prechody stavov.

![Model subdodávateľského štátu](../media/SubconStates.png)  

Nasledujúca tabuľka poskytuje popis toho, čo jednotlivé štáty predstavujú v životnom cykle subdodávky v prevádzke projektu.

| State | Description | Povolené prechody |
| --- | --- | --- |
| Koncept | Toto predstavuje počiatočný stav subdodávky. Prebiehajú rokovania s dodávateľom. Línie a ceny podliehajú zmenám. Subdodávka v tomto stave môže byť použitá na odhad a personálne požiadavky projektu na zdroje a materiály. Môže sa tiež vzťahovať na čas, náklady a spotrebu materiálu v projekte. Subdodávku v tomto stave je možné upravovať a mazať. | Potvrdené |
| Potvrdené | Toto predstavuje štádium subdodávky po dokončení rokovaní s dodávateľom o cenách a nakupovaných riadkových položkách. Samotné dodávanie materiálov a/alebo prác subdodávateľskými zdrojmi však stále prebieha. Subdodávka v tomto stave môže byť použitá na odhad a personálne požiadavky projektu na zdroje a materiály. Môže sa tiež vzťahovať na čas, náklady a spotrebu materiálu v projekte. Subdodávateľskú zmluvu v tomto stave nie je možné upravovať ani mazať. The **Zrušiť** umožňuje zrušiť potvrdenú subdodávku. The **Znovu otvorte** vám umožní znovu otvoriť subdodávku a vrátiť ju späť **Návrh** postavenie. Použi **Zavrieť** tlačidlo na zatvorenie potvrdenej subdodávky. | Zatvorené <br> Zrušená <br> Koncept |
| Zatvorené | Toto predstavuje štádium subdodávky, keď je dokončená skutočná dodávka materiálov a/alebo práce prostredníctvom subdodávateľských zdrojov. Subdodávka v tomto stave sa už nedá použiť na odhad a personálne projektové požiadavky na zdroje a materiály. Tiež sa už nemôže odvolávať na čas, náklady a spotrebu materiálu v projekte. Subdodávateľskú zmluvu v tomto stave nie je možné upravovať ani mazať. | None |
| Zrušená | Toto predstavuje štádium subdodávky, keď už nie je potrebná skutočná dodávka materiálov a/alebo práca zo subdodávateľských zdrojov. Subdodávateľská zmluva v tomto stave nemôže byť použitá na odhad a personálne projektové požiadavky na zdroje a materiály, ani sa nemôže odvolávať na čas, náklady a spotrebu materiálu v projekte. Subdodávateľskú zmluvu v tomto stave nie je možné upravovať ani mazať. | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
