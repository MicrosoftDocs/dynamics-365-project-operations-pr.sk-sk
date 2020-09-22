---
title: Obchodné transakcie
description: Táto téma poskytuje informácie o obchodných transakciách.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: f059d9ec-878d-40c1-bd00-a8966bdf4e29
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe93ec07e9eed0af02c62d08f18a0b2aaeff7996
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755684"
---
# <a name="business-transactions"></a>Obchodné transakcie

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

V Dynamics 365 Project Service Automation, *business transaction* je abstraktný koncept, ktorý nie je zastúpený žiadnou entitou. Avšak, niektoré bežné polia a procesy na entitách sú navrhnuté tak, aby používali koncept obchodných transakcií. Nasledujúce entity používajú túto abstrakciu:

- Podrobnosti o riadku cenovej ponuky
- Podrobnosti o riadku zmluvy
- Riadky odhadov
- Záznamy v účtovnom denníku
- Skutočné hodnoty

Podľa týchto entít, podrobností riadka cenovej ponuky, podrobnosti riadka zmluvy a riadkov odhadu sú priradené k fáze odhadu v životnom cykle projektu. Riadky účtovného denníka a správne údaje entít sú priradené k fáze vykonania v životnom cykle projektu.

PSA zaobchádza so záznamami v týchto piatich entitách ako s obchodnými transakciami. Jediným rozdielom je, že záznamy v entitách, ktoré sú priradené do fázy odhadu, sa považujú za finančné prognózy, zatiaľ čo záznamy v entitách, ktoré sú priradené k fáze vykonania, sa považujú za finančné skutočnosti, ktoré sa už vyskytli.

Ďalšie informácie nájdete v časti [Estimates](estimates.md) a [Actuals](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepty, ktoré sú jedinečné pre obchodné transakcie
Tieto pojmy sú jedinečné pre koncept obchodných transakcií:

- Typ transakcie
- Trieda transakcie
- Počiatok transakcie
- Kontaktná osoba transakcie

### <a name="transaction-type"></a>Typ transakcie

Typ transakcie predstavuje načasovanie a kontext finančného vplyvu na projekt. Je zastúpená množinou možností, ktorá má nasledujúce podporované hodnoty v PSA:
- Náklady
- Projektová zmluva
- Nefakturovaný predaj
- Fakturovaný predaj
- Predaj medzi organizáciami
- Náklady zdrojovej jednotky

### <a name="transaction-class"></a>Trieda transakcie

Trieda transakcie predstavuje rôzne typy nákladov, ktoré vznikli na projektoch. Je zastúpená množinou možností, ktorá má nasledujúce podporované hodnoty v PSA:

- Time
- Výdavok
- Materiál
- Poplatok
- Medzník
- Daň

Hodnota **Milestone** sa zvyčajne používa v obchodnej logike pre fakturáciu s pevnou cenou v PSA.

### <a name="transaction-origin"></a>Počiatok transakcie

Pôvod transakcie je entita, ktorá ukladá pôvod každej obchodnej transakcie. Keď sa realizácia projektu začína, každá obchodná transakcia bude viesť k ďalšej obchodnej transakcii, ktorá následne vytvorí ďalšiu a tak ďalej. Entita pôvodu transakcie bola navrhnutá tak, aby ukladala údaje o pôvode každej transakcie, aby sa uľahčilo vykazovanie a sledovateľnosť. 

### <a name="transaction-connection"></a>Kontaktná osoba transakcie

Kontaktná osoba transakcie je entita, ktorá uchováva vzťah medzi dvoma podobnými obchodnými transakciami, ako sú náklady a súvisiace skutočné údaje predaja alebo storno vyvolané fakturačnými aktivitami ako potvrdenie faktúry alebo opravy faktúry.

Počiatok transakcie a kontaktná osoba transakcie vám spolu pomáhajú sledovať vzťahy medzi obchodnými transakciami a akciami, ktoré spôsobujú vytvorenie konkrétnej obchodnej transakcie.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Príklad: Ako kontaktná osoba transakcie pracuje s transakcie pripojenia

Nasledujúci príklad znázorňuje typické spracovanie časových záznamov v životnom cykle projektu PSA.

> ![Čas spracovania sa oprávňuje na životný cyklus Project Service](media/basic-guide-17.png)
 
1. Podanie časovej položky spôsobuje vytvorenie dvoch riadkov v účtovnom denníku: jeden pre náklad a jeden pre nevyfakturované predaje.
2. Prípadné schválenie časového záznamu spôsobuje vytvorenie dvoch pravdivých údajov: jeden pre náklad a jeden pre nevyfakturované predaje.
3. Keď používateľ vytvorí fakturačný projekt, vytvorí sa fakturačný riadok transakcie zo skutočného nefakturovaného predaja. 
4. Po potvrdení faktúry sa vytvoria dve nové skutočné hodnoty: nefakturovaný obrat predaja a skutočný fakturovaný predaj.

Každá z týchto udalostí spúšťa vytváranie záznamov transakcie pôvodu a transakcie pripojení entít, aby pomohli vytvoriť stopy vzťahov medzi týmito záznamami, ktoré sú vytvorené časovom zázname, účtovnom zázname, skutočných údajoch a detailoch fakturačných riadkov.

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
| Oprava faktúry GUID      | Faktúra                  | Nové nefakturované skutočné predaje GUID    | Skutočná hodnota                            |                          |

Nasledujúca tabuľka zobrazuje záznamy v pripojení transakčnej entity pre predchádzajúci pracovný postup.

| Udalosť                          | Transakcia 1                 | Rola transakcie 1 | Typ transakcie 1           | Transakcia 2                | Rola transakcie 2 | Typ transakcie 2 |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Podanie časového záznamu          | Záznam v účtovnom denníku GUID (Predaje)     | Nefakturovaný predaj     | msdyn_journalline            | Záznam v účtovnom denníku GUID (náklady)     | Náklady               | msdyn_journalline  |
| Schválený čas                  | Skutočné náklady (základné)  | Nefakturovaný predaj     | msdyn_actual                 | Skutočné náklady (náklady) GUID       | Náklady               | msdyn_actual       |
| Vytváranie faktúr               | Podrobnosti o riadku faktúry GUID      | Fakturovaný predaj       | msdyn_invoicelinetransaction | Nové nefakturované skutočné údaje predaja GUID   | Nefakturovaný predaj     | msdyn_actual       |
| Potvrdenie faktúry           | Storno skutočných údajov GUID         | Storno          | msdyn_actual                 | Pôvodné nefakturované predaje GUID | Pôvodné           | msdyn_actual       |
| Fakturovaný predaj GUID              | Fakturovaný predaj                  | msdyn_actual       | Nové nefakturované skutočné údaje predaja GUID   | Nefakturovaný predaj               | msdyn_actual       |                    |
| Koncept opravy faktúry       | Riadok faktúry Transaction GUID | Nahradenie          | msdyn_invoicelinetransaction | Fakturovaný predaj GUID            | Pôvodné           | msdyn_actual       |
| Potvrdená oprava faktúry     | Storno fakturovaného predaja GUID    | Storno          | msdyn_actual                 | Fakturovaný predaj GUID            | Pôvodné           | msdyn_actual       |
| Nové nefakturované skutočné predaje GUID | Nahradenie                     | msdyn_actual       | Fakturovaný predaj GUID            | Pôvodné                     | msdyn_actual       |                    |
