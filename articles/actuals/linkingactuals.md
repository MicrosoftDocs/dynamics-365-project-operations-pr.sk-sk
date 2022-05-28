---
title: Pôvod transakcie – prepojte aktuálne informácie s ich zdrojom
description: Táto téma vysvetľuje, ako sa koncept pôvodu transakcií používa na prepojenie skutočných údajov s pôvodnými zdrojovými záznamami, ako sú časové záznamy, záznamy o výdavkoch alebo protokoly použitia materiálu.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 908f78f7d58ec4b18f37d03b6fa7c4e2295491fa
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584845"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Pôvod transakcie – prepojte aktuálne informácie s ich zdrojom

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Záznamy o pôvode transakcie sa vytvárajú na prepojenie skutočností s ich zdrojom, ako sú časové záznamy, výdavkové záznamy, protokoly spotreby materiálu a projektové faktúry.

Nasledujúci príklad znázorňuje typické spracovanie časových záznamov v životnom cykle projektu Project Operations.

> ![Spracovanie celkov v projektových operáciách.](media/basic-guide-17.png)
 
1. Odoslanie časového záznamu spôsobí, že sa vytvoria dva riadky denníka: jeden pre náklady a jeden pre nevyfakturovaný predaj.
2. Prípadné schválenie časového záznamu spôsobí, že sa vytvoria dva skutočné údaje: jeden pre náklady a jeden pre nevyfakturovaný predaj.
3. Keď používateľ vytvorí fakturačný projekt, vytvorí sa fakturačný riadok transakcie zo skutočného nefakturovaného predaja.
4. Po potvrdení faktúry sa vytvoria dve nové skutočné hodnoty: nefakturovaný obrat predaja a skutočný fakturovaný predaj.

Každá udalosť v tomto pracovnom postupe spracovania spúšťa vytváranie záznamov v entite pôvodu transakcie, čo pomáha vytvoriť stopu vzťahov medzi týmito záznamami, ktoré sa vytvárajú cez časový záznam, riadok denníka, skutočné údaje a podrobnosti riadku faktúry.

Nasledujúca tabuľka zobrazuje záznamy v pôvode transakcie entity pre predchádzajúci pracovný postup.

| Udalosť                        | Pôvod                   | Typ pôvodu                       | Transakcia                       | Typ transakcie         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Podanie časového záznamu        | Record GUID časový záznam   | Zadanie času                        | Záznam v účtovnom denníku Record GUID (náklady)   | Záznam v účtovnom denníku             |
| Record GUID časový záznam       | Zadanie času               | Záznam v účtovnom denníku Record GUID (predaje)  | Záznam v účtovnom denníku                      |                          |
| Schválený čas                | Záznam v účtovnom denníku Record GUID | Záznam v účtovnom denníku                      | Nefakturovaný predaj Record GUID        | Skutočná hodnota                   |
| Record GUID časový záznam       | Zadanie času               | Nefakturovaný predaj Record GUID        | Skutočná hodnota                            |                          |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Skutočné údaje nákladov Record GUID           | Skutočná hodnota                            |                          |
| Record GUID časový záznam       | Zadanie času               | Skutočné údaje nákladov Record GUID           | Skutočná hodnota                            |                          |
| Vytváranie faktúr             | Record GUID časový záznam   | Zadanie času                        | Riadok faktúry Transaction GUID     | Transakcia riadka faktúry |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Riadok faktúry Transaction GUID     | Transakcia riadka faktúry          |                          |
| Potvrdenie faktúry         | Riadok faktúry GUID        | Riadok faktúry                      | Fakturovaný predaj Record GUID          | Skutočná hodnota                   |
| Faktúra GUID                 | Faktúra                  | Fakturovaný predaj Record GUID          | Skutočná hodnota                            |                          |
| Podrobnosti o riadku faktúry GUID     | Podrobnosti o riadku faktúry      | Fakturovaný predaj Record GUID          | Skutočná hodnota                            |                          |
| Record GUID časový záznam       | Zadanie času               | Fakturovaný predaj Record GUID          | Skutočná hodnota                            |                          |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Fakturovaný predaj Record GUID          | Skutočná hodnota                            |                          |
| Record GUID časový záznam       | Zadanie času               | Storno nefakturovaného predaja GUID      | Skutočná hodnota                            |                          |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Storno nefakturovaného predaja GUID      | Skutočná hodnota                            |                          |
| Koncept opravy faktúry     | Staré ILD GUID             | Transakcia riadka faktúry          | Oprava ILD GUID               | Transakcia riadka faktúry |
| Staré IL GUID                  | Riadok faktúry             | Oprava ILD GUID               | Transakcia riadka faktúry          |                          |
| Stará faktúra GUID             | Faktúra                  | Oprava ILD GUID               | Transakcia riadka faktúry          |                          |
| Record GUID časový záznam       | Zadanie času               | Oprava ILD GUID               | Transakcia riadka faktúry          |                          |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Oprava ILD GUID               | Transakcia riadka faktúry          |                          |
| Potvrdená oprava faktúry | Staré ILD GUID             | Transakcia riadka faktúry          | Storno skutočného fakturovaného predaja GUID | Skutočná hodnota                   |
| Staré IL GUID                  | Riadok faktúry             | Storno skutočného fakturovaného predaja GUID | Skutočná hodnota                            |                          |
| Stará faktúra GUID             | Faktúra                  | Storno skutočného fakturovaného predaja GUID | Skutočná hodnota                            |                          |
| Record GUID časový záznam       | Zadanie času               | Storno skutočného fakturovaného predaja GUID | Skutočná hodnota                            |                          |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Storno skutočného fakturovaného predaja GUID | Skutočná hodnota                            |                          |
| Staré ILD GUID                 | Transakcia riadka faktúry | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |
| Staré IL GUID                  | Riadok faktúry             | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |
| Stará faktúra GUID             | Faktúra                  | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |
| Record GUID časový záznam       | Zadanie času               | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |
| Oprava ILD GUID          | Transakcia riadka faktúry | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |
| Oprava IL GUID           | Riadok faktúry             | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |
| Oprava faktúry GUID      | Faktúra                  | Nové nefakturované skutočné predaje GUID    | Skutočnosť                            |                          |


Nasledujúca ilustrácia zobrazuje prepojenia, ktoré sa vytvárajú medzi skutočnými hodnotami a ich zdrojmi pri rôznych udalostiach, na príklade časových záznamov v Project Operations.

> ![Ako sú skutočné údaje prepojené so zdrojovými záznamami v projektových operáciách.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
