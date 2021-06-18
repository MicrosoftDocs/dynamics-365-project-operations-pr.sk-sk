---
title: Prepojenie skutočných hodnôt s pôvodnými záznamami
description: Táto téma vysvetľuje, ako prepojiť skutočné údaje s pôvodnými záznamami, ako sú napríklad časové údaje, záznamy o výdavkoch alebo denníky použitia materiálu.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9fc49211f3c2c79e18f6dd18e9a687091793cad0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996765"
---
# <a name="link-actuals-to-original-records"></a>Prepojenie skutočných hodnôt s pôvodnými záznamami

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_


V Dynamics 365 Project Operations je *obchodná transakcia* abstraktný koncept, ktorý nie je zastúpený žiadnou entitou. Avšak, niektoré bežné polia a procesy na entitách sú navrhnuté tak, aby používali koncept obchodných transakcií. Nasledujúce entity používajú tento koncept:

- Podrobnosti o riadku cenovej ponuky
- Podrobnosti o riadku zmluvy
- Riadky odhadov
- Záznamy v účtovnom denníku
- Skutočné hodnoty

Z týchto entít **Podrobnosti o riadku cenovej ponuky**, **Podrobnosti o riadku zmluvy** a **Riadky odhadov** sú priradené k fáze odhadu v životnom cykle projektu. **Záznamy v účtovnom denníku** a **Entity skutočných hodnôt** sú priradené k fáze vykonania v životnom cykle projektu.

Project Operations rozpoznáva záznamy v týchto piatich entitách ako obchodné transakcie. Jediným rozdielom je, že záznamy v entitách, ktoré sú priradené do fázy odhadu, sa považujú za finančné prognózy, zatiaľ čo záznamy v entitách, ktoré sú priradené k fáze vykonania, sa považujú za finančné skutočnosti, ktoré sa už vyskytli.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepty, ktoré sú jedinečné pre obchodné transakcie
Tieto pojmy sú jedinečné pre koncept obchodných transakcií:

- Typ transakcie
- Trieda transakcie
- Počiatok transakcie
- Kontaktná osoba transakcie

### <a name="transaction-type"></a>Typ transakcie

Typ transakcie predstavuje načasovanie a kontext finančného vplyvu na projekt. Toto je zastúpené množinou možností, ktorá má nasledujúce podporované hodnoty v Project Operations:

  - Náklady
  - Projektová zmluva
  - Nefakturovaný predaj
  - Fakturovaný predaj
  - Predaj medzi organizáciami
  - Náklady zdrojovej jednotky

### <a name="transaction-class"></a>Trieda transakcie

Trieda transakcie predstavuje rôzne typy nákladov, ktoré vznikli na projektoch. Toto je zastúpené množinou možností, ktorá má nasledujúce podporované hodnoty v Project Operations:

  - Čas
  - Výdavok
  - Materiál
  - Poplatok
  - Medzník
  - Daň

**Medzník** sa zvyčajne používa v obchodnej logike pre fakturáciu s pevnou cenou v Project Operations.

### <a name="transaction-origin"></a>Počiatok transakcie

**Pôvod transakcie** je entita, ktorá ukladá pôvod každej obchodnej transakcie. V priebehu realizácie projektu bude každá obchodná transakcia viesť k ďalšej obchodnej transakcii, ktorá následne vytvorí ďalšiu atď. Entita pôvodu transakcie je navrhnutá na ukladanie údajov o pôvode každej transakcie, aby pomohla s vykazovaním a sledovateľnosťou. 

### <a name="transaction-connection"></a>Kontaktná osoba transakcie

**Kontaktná osoba pre transakciu** je entita, ktorá uchováva vzťah medzi dvoma podobnými obchodnými transakciami, ako sú náklady a súvisiace skutočné údaje predaja alebo storno transakcie vyvolané fakturačnými aktivitami ako potvrdenie faktúry alebo opravy faktúry.

**Počiatok transakcie** a **Kontaktná osoba pre transakciu** vám spolu pomáhajú sledovať vzťahy medzi obchodnými transakciami a akciami, ktoré spôsobujú vytvorenie konkrétnej obchodnej transakcie.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Príklad: Ako kontaktná osoba transakcie pracuje s transakcie pripojenia

Nasledujúci príklad znázorňuje typické spracovanie časových záznamov v životnom cykle projektu Project Operations.

> ![Čas spracovania sa oprávňuje na životný cyklus Project Service](media/basic-guide-17.png)
 
1. Podanie časovej položky vytvorí dva záznamy v účtovnom denníku: jeden pre náklad a jeden pre nevyfakturované predaje.
2. Prípadné schválenie časového záznamu vytvorí dva skutočné údaje: jeden pre náklad a jeden pre nevyfakturované predaje.
3. Keď sa vytvorí nový fakturačný projekt, vytvorí sa fakturačný riadok transakcie zo skutočného nefakturovaného predaja. 
4. Po potvrdení faktúry sa vytvoria dve nové skutočné hodnoty: skutočné storno nefakturovaného predaja a skutočný fakturovaný predaj.

Každá z týchto udalostí vytvára záznam v entitách **Počiatok transakcie** a **Kontaktná osoba pre transakciu**. Tieto nové záznamy pomáhajú vytvárať históriu vzťahov medzi záznamami, ktoré sa vytvárajú v detailoch záznamu času, zázname v účtovnom denníku, skutočných údajoch a faktúrach.

Nasledujúca tabuľka zobrazuje záznamy v entite **Počiatok transakcie** pre pracovný postup.

| Udalosť                        | Počiatok                   | Typ pôvodu                       | Transakcia                       | Typ transakcie         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Podanie časového záznamu        | GUID záznamu zadania času   | Zadanie času                        | Záznam v účtovnom denníku Record GUID (náklady)   | Záznam v účtovnom denníku             |
| Record GUID časový záznam       | Zadanie času               | Záznam v účtovnom denníku Record GUID (predaje)  | Záznam v účtovnom denníku                      |                          |
| Schválený čas                | Záznam v účtovnom denníku Record GUID | Záznam v účtovnom denníku                      | Nefakturovaný predaj Record GUID        | Skutočná hodnota                   |
| Record GUID časový záznam       | Zadanie času               | Nefakturovaný predaj Record GUID        | Skutočná hodnota                            |                          |
| Záznam v účtovnom denníku Record GUID     | Záznam v účtovnom denníku             | Skutočné údaje nákladov Record GUID           | Skutočná hodnota                            |                          |
| Record GUID časový záznam       | Zadanie času               | Skutočné údaje nákladov Record GUID           | Skutočnosť                            |                          |
| Vytváranie faktúr             | GUID záznamu zadania času   | Zadanie času                        | Riadok faktúry Transaction GUID     | Transakcia riadka faktúry |
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

Nasledujúca tabuľka zobrazuje záznamy v entite **Kontaktná osoba pre transakciu** pre pracovný postup.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
