---
title: Nastavenie kategórií výdavkov
description: Táto téma poskytuje informácie o tom, ako nastaviť kategórie výdavkov a zdieľané kategórie pre výkazy výdavkov.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896705"
---
# <a name="set-up-expense-categories"></a>Nastavenie kategórií výdavkov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Keď zamestnanci vytvárajú výkazy výdavkov, každý výdavok, ktorý zaznamenajú, musí byť priradený ku kategórii výdavkov. Kategórie výdavkov sú odvodené od zdieľaných kategórií, ktoré je možné zdieľať medzi právnymi entitami vo vašej organizácii. V závislosti od toho, ako je definovaná vaša organizácia, je možné tieto kategórie výdavkov zdieľať aj v iných oblastiach. Na základe definície vašej organizácie a pokynov implementačného tímu musíte určiť, či sa kategórie, ktoré sa používajú v správe výdavkov, použijú iba v správe výdavkov, alebo či sa majú zdieľať v iných oblastiach.

> [!NOTE]
> Tieto kategórie možno zdieľať medzi projektovým manažmentom a účtovníctvom a riadením výdavkov alebo medzi projektovým riadením a účtovníctvom a produkciou. Nemôžu sa však zdieľať medzi správou výdavkov a produkciou.

Predtým, ako začnete s procesom nastavenia, musíte urobiť nasledujúce rozhodnutia pre každú kategóriu výdavkov:

- Čo je kategória výdavku? Príklady zahŕňajú kategórie letov, hotelov alebo najazdených kilometrov.
- Dá sa kategória výdavkov použiť aj v projektovom manažmente a účtovníctve? Ak je to možné, musíte uskutočniť aj tieto rozhodnutia:

    - Ktoré nákladové účty sa použijú na nasledujúce výdavky?

        - Náklady
        - Alokácia miezd
        - Hodnota nákladov WIP
        - Nákladová položka
        - WIP – nákladová hodnota – položka
        - Akumulovaná strata
        - WIP – akumulovaná strata

    - Ktoré obchodné vzťahy s výnosmi sa použijú pre nasledujúce zdroje výnosov?

        - Fakturovaný príjem
        - Akumulované výnosy – hodnota predaja
        - WIP – hodnota predaja
        - Akumulované výnosy – produkcia
        - WIP – produkcia
        - Akumulované výnosy – zisk
        - WIP – zisk
        - Akumulované výnosy – predplatné
        - WIP – predplatné

- Čo je typ výdavku?
- Aký je predvolený spôsob platby pre kategóriu výdavkov?
- Musia byť výdavky v kategórii výdavkov rozpísané na jednotlivé položky?
- Aký je hlavný predvolený obchodný vzťah pre kategóriu výdavkov?
- Aká je predvolená skupina dane z predaja položky pre kategóriu výdavkov?
- Sú pre kategóriu výdavkov povolené ďalšie spôsoby platby? Ak áno, ktoré to sú?
- Existujú v tejto kategórii výdavkov podkategórie? Ak existujú podkategórie, musíte uskutočniť aj nasledujúce rozhodnutia:

    - Je niektorá z podkategórií vylúčená z vrátenia dane?
    - Čo je skupina dane z predaja položky v podkategóriách?
