---
title: Rozpis výdavkov
description: Tento článok vysvetľuje, ako rozpísať výdavky pomocou prepracovaného pracovného priestoru Výdavky.
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

Organizácie často vyžadujú od zamestnancov, aby poskytli podrobný rozpis výdavkov vynaložených počas cestovania. Napríklad hotelové zoznam môže obsahovať niekoľko riadkov s jednotlivými položkami pre cenu za izbu, daň, parkovanie a iné rôzne výdavky, ktoré vzniknú každý deň počas trvania pobytu. Alebo výdavky na jedlo môžu vyžadovať, aby ste poskytli podrobnejšie rozpis pre raňajky, obed alebo večeru. Bez ohľadu na potreby organizácie je možné každú kategóriu výdavkov nastaviť tak, aby odrážala podkategórie alebo riadkové položky, ktoré tvoria výdavky. Kým rozpis bol vždy podporovaný vo funkcii **Správa výdavkov**, pracovný priestor **Prepracované výdavky** umožňuje efektívnejší rozpis, keď je povolená funkcia **Schopnosť rýchlo rozpísať opakujúce sa výdavky**.  

## <a name="enable-quick-itemization"></a>Povolenie rýchleho rozpisu 

Môžete použiť funkciu **Schopnosť rýchlo rozpísať opakujúce sa výdavky** na rýchly rozpis opakujúcich sa výdavkov, pričom sa vyhnete potrebe zadávať denné výdavky zakaždým počas trvania pobytu. Vykonaním nasledujúcich krokov povolíte rýchly rozpis.

1. Prejdite do pracovného priestoru **Správa funkcií** a v zozname funkcií vyhľadajte a vyberte položku **Prepracované výkazy výdavkov**. 
2. Vyberte položku **Povoliť teraz**. 
3. V zozname funkcií vyhľadajte a vyberte **Schopnosť rýchlo rozpísať opakujúce sa výdavky**.
4. Vyberte položku **Povoliť teraz**. 

## <a name="itemization-grid"></a>Mriežka rozpisu 

Ak má kategória výdavkov podkategórie alebo rôzne súčasti, ktoré tvoria tieto výdavky, možno ju rozčleniť na jednotlivé položky. Ak chcete rozpísať výdavok, vyberte riadok výdavkov vo výkaze výdavkov a na table **Podrobnosti o výdavkoch** vyberte **Akcie** > **Rozpísať**. Jazdec **Rozpis** odhaľuje mriežku s poľami. Nasledujúca tabuľka poskytuje príklad každého poľa v mriežke a spôsob vykreslenia poľa vo výkaze výdavkov. 

|     Pole          |     Description                                                                                  |     Príklad              |
|--------------------|--------------------------------------------------------------------------------------------------|--------------------------|
|     Podkategória    |     Zoznam podkategórií nakonfigurovaných pod typom kategórie výdavkov **Hotel**.             |     Dennú sadzba za izbu      |
|     Počiatočný dátum     |     Dátum prvého vzniku položky výdavku.                                           |     13. 9. 2021           |
|     Denná sadzba     |     Suma vynaložená na položku výdavku.                                                    |     200                  |
|     Množstvo       |     Počet opakovaní poplatku počas súvislého obdobia.                       |     3                    |

![Rozpíšte výdavok.](media/Itemization%20screen%201.png)

Keď uložíte rozpis, uvidíte samostatný riadok s rozpísanými položkami pre množstvo zadané v tabuľke Rozpis. Každý riadok začína dátumom, ktorý je uvedený v mriežke.

![Rozpísaná zostava.](media/Itemization%20screen%202.png)

