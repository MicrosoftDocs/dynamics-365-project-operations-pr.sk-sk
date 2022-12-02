---
title: Typy období
description: Tento článok obsahuje informácie o tom, ako nastaviť typy období pre odhad výnosov.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5bbf2dcb4758611aa9d0591ddfec42869f4438c0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930981"
---
# <a name="period-types"></a>Typy období

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Typ obdobia definuje, ako často sa odhadujú výnosy v projekte. Tento článok obsahuje informácie o tom, ako nastaviť typy období pre odhad výnosov. 

## <a name="create-and-work-with-period-types"></a>Vytvorenie a práca s typmi období
Ak chcete vytvárať a pracovať s typmi období, postupujte takto:

1. Vo vašom prostredí Dynamics 365 Finance prejdite do **Projektový manažment a účtovníctvo** > **Nastavenie** > **Odhady** > **Typy období**.
2. Ak chcete vytvoriť nový typ obdobia, vyberte **Nové**. Zadajte názov a popis.
3. V poli **Frekvencia** vyberte hodnotu:

    - Ak vyberiete **Týždenne**, **Dvojtýždenne**, **Polmesačne**, **Mesačne**, **Denne**, **Štvrťročne** alebo **Ročne**, kalendár sa použije na generovanie období. 
    - Ak vyberiete **Obdobie účtovnej knihy**, na generovanie období sa použijú obdobia hlavnej účtovnej knihy z konfigurácie hlavnej účtovnej knihy.
    - Ak vyberiete **Neobmedzene**, môžete určiť vlastné obdobia.
4. Vyberte záznam typu obdobia a potom vyberte **Generovať obdobia** na vytvorenie období pre typ obdobia. Na základe zvolenej frekvencie období môžete mať možnosť určiť dátum začatia alebo počet období, ktoré sa majú vygenerovať.
5. Vyberte **Obdobia** na kontrolu generovaných období.



[!INCLUDE[footer-include](../includes/footer-banner.md)]