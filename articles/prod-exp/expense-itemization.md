---
title: Rozpis výdavkov
description: Tento článok vysvetľuje, ako rozčleniť výdavky pomocou prepracovaného pracovného priestoru Výdavky.
author: suvaidya
ms.date: 12/16/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 71bfbe83259804fc0b0355c81d430805da23dd45
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920953"
---
# <a name="expense-itemization"></a>Rozpis výdavkov

[!include [banner](../includes/banner.md)]

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Organizácie často vyžadujú od zamestnancov, aby poskytli podrobný rozpis nákladov vynaložených počas cestovania. Napríklad hotelové folio môže obsahovať niekoľko riadkov s jednotlivými položkami pre cenu za izbu, daň, parkovanie a iné rôzne výdavky, ktoré vzniknú každý deň počas trvania pobytu. Alebo výdavky na jedlo môžu vyžadovať, aby ste poskytli podrobnejšie rozpis na raňajky, obed alebo večeru. Bez ohľadu na potreby organizácie je možné každú kategóriu výdavkov nastaviť tak, aby odrážala podkategórie alebo riadkové položky, ktoré tvoria výdavky. Kým položka bola vždy podporovaná v **Riadenie výdavkov**, **náklady** pracovný priestor umožňuje efektívnejšiu tvorbu položiek, keď funkcia, **Schopnosť rýchlo rozpísať opakujúce sa výdavky** je umožnené.  

## <a name="enable-quick-itemization"></a>Povoliť rýchlu tvorbu položiek 

Môžete použiť **Schopnosť rýchlo rozpísať opakujúce sa výdavky** funkcia na rýchle rozloženie opakujúcich sa výdavkov, pričom nie je potrebné zadávať denné výdavky zakaždým počas trvania pobytu. Ak chcete povoliť rýchlu tvorbu položiek, vykonajte nasledujúce kroky.

1. Choďte na **Správa funkcií** pracovný priestor a v zozname funkcií nájdite a vyberte, **Prepracované výkazy výdavkov**. 
2. Vyberte položku **Povoliť teraz**. 
3. V zozname funkcií vyhľadajte a vyberte **Schopnosť rýchlo rozpísať opakujúce sa výdavky**.
4. Vyberte položku **Povoliť teraz**. 

## <a name="itemization-grid"></a>Mriežka položiek 

Ak má kategória výdavkov podkategórie alebo rôzne zložky, ktoré tvoria tieto výdavky, možno ju rozčleniť na jednotlivé položky. Ak chcete rozpísať výdavok, vyberte riadok výdavkov vo výkaze výdavkov a v **Podrobnosti o výdavkoch** panel, vyberte **Akcie** > **Itemize**. The **Rozpis položiek** posúvač odhaľuje mriežku s poľami. Nasledujúca tabuľka poskytuje príklad každého poľa v mriežke a spôsob vykreslenia poľa vo výkaze výdavkov. 

|     Pole          |     Description                                                                                  |     Príklad              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Podkategória    |     Zoznam podkategórií nakonfigurovaných pod typom kategórie výdavkov, **Hotel**.             |     Cena za dennú izbu      |
|     Počiatočný dátum     |     Dátum prvého vzniku nákladovej položky.                                           |     13.09.2021           |
|     Denná sadzba     |     Suma vynaložená na nákladovú položku.                                                    |     200                  |
|     Množstvo       |     Počet opakovaní nabíjania počas súvislého obdobia.                       |     3                    |

![Rozpísať výdavky.](media/Itemization%20screen%201.png)

Keď uložíte rozpis položiek, uvidíte samostatný riadok s položkami pre množstvo zadané v tabuľke Rozpis položiek. Každý riadok začína dátumom, ktorý je uvedený v mriežke.

![Rozpísaný prehľad.](media/Itemization%20screen%202.png)

