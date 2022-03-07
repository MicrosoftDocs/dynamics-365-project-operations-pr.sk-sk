---
title: Synchronizácia kapacity zdroja
description: Táto téma poskytuje informácie o tom, ako synchronizovať kapacitu zdroja v rámci kalendárov a projektov.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f2e9b8e189be0594569e14ebc41c6ed452afd10aba34ea1397b3e3f66cd2e96
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005635"
---
# <a name="synchronize-resource-capacity"></a>Synchronizácia kapacity zdroja

[!include [banner](../includes/banner.md)]

Procesy synchronizácie zdrojov pomáhajú zaručiť, že informácie pre kalendár a základný kalendár sa prenášajú až do plánovania zdrojov projektu. Ak dôjde k zmene kalendára, procesy vykonajú požadované aktualizácie plánovania zdrojov projektu. Procesy tiež pomáhajú zvýšiť výkon, pretože informácie o zdrojoch z kalendára sú synchronizované vopred. Preto sa aktualizácie informácií o plánovaní zdrojov vyskytujú rýchlejšie. Odporúčame naplánovať procesy ako dávkové, nie po jednom. V opačnom prípade existuje riziko, že niekto zabudne na zahrnuté dátumy pri poslednej synchronizácie informácií. Ak sa nepoužívajú zahrnuté dátumy, počas synchronizácie dátumov môžu nastať medzery.

![Synchronizácia kalendára.](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizácia súhrnov kapacity zdroja

Proces synchronizácie je navrhnutý tak, aby synchronizoval všetky informácie z kalendára zdrojov. Tieto informácie zahŕňajú informácie základného kalendára o akýchkoľvek zmenách v tabuľke kapacity kalendára zdrojov projektu. Ak sú do projektu pridané nové zdroje, synchronizácia pomáha zaručiť, že sú k dispozícii aktualizované informácie z kalendára. Túto synchronizáciu je možné vykonať kedykoľvek.

Odporúčame používať dávku. Možnosti sú k dispozícii počas synchronizácie rezervácií kapacity.

1. Vyberte **Projektové riadenie a účtovníctvo** &gt; **Pravidelne** &gt; **Synchronizácia kapacity** &gt; **Synchronizácia súhrnov kapacity zdroja**.
2. Nastavte možnosti v nasledujúcej tabuľke.

    | Možnosť      | Popis |
    |-------------|-------------|
    | Kód obdobia | Voliteľne vyberte kód intervalu dátumu hlavnej účtovnej knihy, aby ste nastavili dátumy začiatku a konca procesu synchronizácie pre súhrn kapacity zdrojov. |
    | Počiatočný dátum  | Zadajte dátum začatia procesu synchronizácie pre súhrn kapacity zdrojov. |
    | Dátum skončenia    | Zadajte dátum ukončenia procesu synchronizácie pre súhrn kapacity zdrojov. |

[![Proces synchronizácie.](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]