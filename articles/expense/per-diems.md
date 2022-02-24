---
title: Za každý deň
description: Táto téma poskytuje informácie o pravidlách diét, ktoré sa používajú v správe výdavkov.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 8d723b49e9556401c364b323cf58eaaf44906275
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128527"
---
# <a name="per-diems"></a>Za každý deň

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_


Diéta je príspevok, ktorý sa vypláca pracovníkovi, ktorý cestuje za prácou. V správe výdavkov môžete vytvoriť pravidlá diét pre rôzne cestovné situácie. Sadzby za diéty môžu byť založené na ročnom období, mieste cesty alebo oboch. Keď vytvoríte pravidlo týkajúce sa diéty, môžete určiť, že bude zadržané percento z diéty, ak pracovník dostane bezplatné stravovanie alebo služby. Môžete tiež nastaviť minimálny a maximálny počet hodín, pre ktoré môže platiť diéta pre cestu pracovníka.

## <a name="configuration"></a>Konfigurácia 

1. Ak chcete pridať miesta diét, prejdite na **Nastaviť** > **Výpočty a kódy** > **Miesta diét**.
2. Pre každé z miest pridaných vyššie vyberte sadzbu diét a menu, ktorá je platná medzi konkrétnym dátumom začatia a ukončenia hotela, stravovania a ďalších výdavkov. Sadzby a meny diét sú nakonfigurované v časti **Nastaviť** > **Výpočty a kódy** > **Diéty**.
3. Na stránke **Miesta diét** stránka, nakonfigurujte úrovne denných diét. Úrovne denných diét vám umožňujú definovať percentuálne rozdelenie denného príspevku na hotel, stravu a ďalšie výdavky. 
4. Ak chcete určiť zníženie percento jedla pri raňajkách, obede alebo večeri, aktualizujte polia na stránke **Parametre správy výdavkov** na karte **Diéty**. 
    
## <a name="submit-expenses-using-per-diem"></a>Predloženie výdavkov pri použití diét
Na predloženie výdavkov s použitím diét pri vytváraní výkazu výdavkov použite kategóriu výdavkov **Diéty**. Prejdite do **Diéty od dátumu**, **Diéta k dátumu** a **Miesto diét**. Suma sa vypočíta na základe sadzieb diét pre vybrané miesto a zníženie jedál sa vypočíta na základe úrovní denných diét.
