---
title: Nákupné objednávky pre projekt
description: Tento článok popisuje rôzne metódy, ktoré môžete použiť na vytvorenie nákupných objednávok pre projekt. Metóda, ktorú použijete, závisí od účelu nákupnej objednávky a od toho, kedy sa zakúpené položky spotrebujú a zaúčtujú v rámci projektu.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289208"
---
# <a name="purchase-orders-for-a-project"></a>Nákupné objednávky pre projekt

[!include [banner](../includes/banner.md)]

Tento článok popisuje rôzne metódy, ktoré môžete použiť na vytvorenie nákupných objednávok pre projekt. Metóda, ktorú použijete, závisí od účelu nákupnej objednávky a od toho, kedy sa zakúpené položky spotrebujú a zaúčtujú v rámci projektu.

### <a name="methods-for-creating-a-purchase-order"></a>Metódy vytvárania nákupnej objednávky

Môžete použiť jednu z nasledujúcich metód na vytvorenie nákupnej objednávky v časti Projektové riadenie a účtovníctvo. Účel nákupnej objednávky určuje, kedy sa nákupná objednávka spotrebuje, a tým pádom kedy sa položky zaúčtujú v rámci projektu.

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Spôsob</th>
<th>Účel</th>
<th>Spotreba položiek</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Vytvorte nákupnú objednávku priamo z projektu.</td>
<td>Použite túto metóda na nákup položiek od externého dodávateľa na spotrebu v projekte. Nákupnú objednávku môžete vytvoriť dvoma spôsobmi:
<ul>
<li>Zo samotného projektu. V takom prípade je projekt už pre nákupnú objednávku definovaný.</li>
<li>Navigáciou k nákupnej objednávke projektu. Musíte vybrať dodávateľa aj projekt, pre ktorý chcete vytvoriť nákupnú objednávku.</li>
</ul></td>
<td>Položky sa spotrebujú, keď sa aktualizuje faktúra dodávateľa.</td>
</tr>
<tr class="even">
<td>Vytvorte nákupnú objednávku z predajnej objednávky.</td>
<td>Táto metóda sa používa na nákup položiek, keď vytvárate predajnú objednávku z projektu.</td>
<td>Položky sa spotrebujú, keď sa predajná objednávka fakturuje zákazníkovi.</td>
</tr>
<tr class="odd">
<td>Vytvorte nákupnú objednávku z požiadavky na položku.</td>
<td>Táto metóda sa používa na nákup položiek, keď vytvárate požiadavku na položku z projektu.</td>
<td>Položky sa spotrebujú, keď sa aktualizuje dodací list s požiadavkou na položku.</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> Pri aktualizácii faktúry dodávateľa alebo dodacieho listu sa zobrazí výzva na aktualizáciu dodacieho listu podľa požiadavky na položku.

Viac informácií sa dozviete v časti [Príjem položiek z nákupnej objednávky z požiadaviek na položku](tasks/receive-items-purchase-order-item-requirement.md).



[!INCLUDE[footer-include](../includes/footer-banner.md)]