---
title: Počiatky transakcií – prepojenie skutočných hodnôt s ich zdrojom
description: Tento článok vysvetľuje, ako sa koncept pôvodu transakcií používa na prepojenie skutočných hodnôt s pôvodnými zdrojovými záznamami, ako je napríklad záznam času, záznam výdavkov alebo denníky použitia materiálu.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921321"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Počiatky transakcií – prepojenie skutočných hodnôt s ich zdrojom

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Záznamy o pôvode transakcie sa vytvárajú na prepojenie skutočných hodnôt s ich zdrojom, ako sú zadania času, zadania výdavkov, denníky o použití materiálu a projektové faktúry.

Nasledujúci príklad znázorňuje typické spracovanie časových záznamov v životnom cykle projektu Project Operations.

> ![Spracovanie zadaní času v Project Operations.](media/basic-guide-17.png)
 
1. Odoslanie zadania času spôsobí vytvorenie dvoch záznamov v účtovnom denníku: jeden pre náklad a jeden pre nevyfakturované predaje.
2. Prípadné schválenie zadania času spôsobuje vytvorenie dvoch skutočných hodnôt: jedna pre náklad a jedna pre nevyfakturované predaje.
3. Keď používateľ vytvorí fakturačný projekt, vytvorí sa fakturačný riadok transakcie zo skutočného nefakturovaného predaja.
4. Po potvrdení faktúry sa vytvoria dve nové skutočné hodnoty: nefakturovaný obrat predaja a skutočný fakturovaný predaj.

Každá udalosť v tomto pracovnom postupe spracovania spúšťa vytváranie záznamov v entite pôvodu transakcie, aby pomohli vytvoriť stopy vzťahov medzi týmito záznamami, ktoré sú vytvorené naprieč zadaním času, záznamu v účtovnom denníku, skutočnej hodnote a detailom fakturačných riadkov.

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


Nasledujúca ilustrácia zobrazuje prepojenia, ktoré sa vytvárajú medzi skutočnými hodnotami a ich zdrojmi pri rôznych udalostiach, na príklade zadaní času v Project Operations.

> ![Ako sú skutočné hodnoty prepojené so zdrojovými záznamami v Project Operations.](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
