---
title: Odhady nákladov
description: Táto téma poskytuje informácie o definovaní alebo odhade výdavkov na základe projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908582"
---
# <a name="expense-estimates"></a>Odhady nákladov
_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Spolu s definovaním odhadov založených na zdrojoch umožňuje Dynamics 365 Project Operations projektovým manažérom definovať výdavky na základe projektu pre každý projekt. Každú položku výdavkov je možné priradiť ku konkrétnej projektovej úlohe alebo kategórii výdavkov. Kategórie výdavkov sú zvyčajne definované na úrovni organizácie. Cena pre každú kategóriu výdavkov je zvyčajne definovaná v nasledujúcej hierarchii:

- Organizácia
- Zákazník
- Cenová ponuka/zmluva

Ak chcete zobraziť, pridať alebo odstrániť projektové výdavky, postupujte podľa nasledujúcich krokov.

1. Prejdite do časti **Projekty** a vyberte projekt, na ktorom chcete pracovať.
2. Vyberte kartu **Odhady projektu** a prezrite si zoznam projektových výdavkov.
3. Vyberte **Nový výdavok** na pridanie výdavku. Alebo vyberte výdavok, ktorý chcete odstrániť, a potom vyberte **Odstrániť výdavok**.

Pre každú položku riadka výdavku sú definované nasledujúce atribúty:

- **Kategória** :Bežné zoskupenia používané na popis všetkých výdavkov vzniknutých v súvislosti s projektom.
- **Dátum začiatku**: Dátum, kedy sa predpokladá vznik výdavkov.
- **Množstvo**: Odhadovaný počet položiek výdavkov pre konkrétnu kategóriu.
- **Jednotková obstarávacia cena**: Jednotková cena použitá na náklady výdavkov.
- **Jednotková predajná cena**: Jednotková cena použitá na výpočet predajných cien výdavkov.

