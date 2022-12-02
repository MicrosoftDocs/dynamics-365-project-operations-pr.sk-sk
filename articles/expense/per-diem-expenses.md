---
title: Denné výdavky
description: Tento článok poskytuje informácie o tom, ako pracovať s výdavkami na diéty.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923207"
---
# <a name="per-diem-expenses"></a>Denné výdavky

> [!IMPORTANT] 
> Funkcie opísané v tomto článku sú k dispozícii cieľovým používateľom ako súčasť verzie Preview.

Platba diét je pevná, vopred stanovená denná dávka, ktorú spoločnosť vypláca svojim zamestnancom za ubytovanie (hotely), stravu a vedľajšie výdavky, ktoré títo zamestnanci vynaložia počas cesty za prácou. Spoločnosť vypláca tento príspevok zamestnancom namiesto úhrady skutočných cestovných nákladov. Zamestnanci môžu využiť svoj limit na diéty **Príležitostné/Iné** na pokrytie sprepitného, izbovej služby, práčovne alebo čistiarne pre dôležité obchodné stretnutia. Úroveň diét sa môže líšiť v závislosti od toho, či sa zamestnávateľ rozhodne preplatiť náklady spojené s ubytovaním a stravou alebo len náklady na stravu a vedľajšie výdavky.

Sadzby za diéty môžu byť založené na ročnom období, mieste cesty alebo oboch. Keď vytvoríte pravidlo týkajúce sa diéty, môžete určiť, že bude zadržané percento z diéty, ak zamestnanec dostane bezplatné stravovanie alebo služby. Môžete tiež nastaviť minimálny a maximálny počet hodín, pre ktoré môže platiť diéta pre cestu zamestnanca.

Diéty sa vypočítajú ako celková dávka, ktorá sa ponúka za deň, znížená o cenu stravy (náklady na bezplatné stravovanie), ktoré sa poskytuje zamestnancovi.

## <a name="configure-per-diems"></a>Konfigurácia diét

Ak chcete nakonfigurovať výdavky na diéty, postupujte podľa týchto krokov.

1. Prejdite do **Správa výdavkov** \> **Nastaviť** \> **Všeobecné** \> **Parametre správy výdavkov**.
2. Na karte **Diéty** v poli **Vypočítať zníženie stravného o** vyberte spôsob výpočtu diét:

    - **Druh stravovania na ceste** – Vypočítajte diéty na základe zadaného druhu stravovania (raňajky, obed alebo večera) a zníženia stravného, ktoré je uvedené pre každý druh stravy pre diétu počas trvania cesty.
    - **Druh stravovania na deň** – Vypočítajte diéty na základe zadaného druhu stravovania a zníženia stravného, ktoré je uvedené pre každý druh stravy pre diétu na deň.
    - **Počet jedál za deň** – Vypočítajte diéty na základe počtu zadaných jedál za deň a zníženia stravného za počet jedál, ktoré sa poskytujú každý deň.

3. Prejdite do **Správa výdavkov** \> **Nastavenie** \> **Výpočty a kódy** \> **Miesta diét**.
4. Pridajte miesta, kde je možné použiť diéty.
5. Pre každé miesto, ktoré pridáte, vyberte na karte **Diéty** sadzbu diét a menu, ktorá je platná medzi konkrétnym dátumom začatia a ukončenia ubytovania, stravovania a ďalších výdavkov. Ak chcete nakonfigurovať sadzby diét a meny, prejdite do **Správa výdavkov** \> **Nastavenie** \> **Výpočty a kódy** \> **Diéty**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Diéty v prepracovanom rozhraní výdavkov

Funkcia diét je podporovaná v prepracovanom pracovnom priestore **Správa výdavkov** v Microsoft Dynamics 365 Finance verzia 10.0.25 a novšia.

Ak chcete povoliť diéty, postupujte takto.

1. V pracovnom priestore **Správa funkcií** nájdite a vyberte v zozname funkciu **Prepracované výkazy výdavkov** a potom vyberte **Povoliť teraz**.
2. V zozname nájdite a vyberte funkciu **Prepracované rozhranie diét pre výkaz výdavkov** a potom vyberte **Povoliť teraz**.

## <a name="how-the-feature-works"></a>Ako funguje funkcia

Táto časť obsahuje príklady troch scenárov konfigurácie. Pre každý príklad je pole **Vypočítať zníženie stravného o** nastavené na inú hodnotu. Pre všetky tri príklady je celková suma, ktorá je splatná, rovnaká, kým sa neuplatní zníženie stravného. Po tomto bode sa celková splatná suma pre každý príklad líši.

Ak chcete vytvoriť výdavky na diéty, ktoré sa používajú pre všetky tri príklady, postupujte podľa týchto krokov.

1. Prejdite do časti **Pracovné priestory** \> **Správa výdavkov**.
2. Vyberte **Nový výkaz výdavkov** alebo vyberte existujúci výkaz výdavkov.
3. Pridať nový výdavok. V poli **Kategória** vyberte **Diéty**. Vyberte miesto a dátumy začiatku a konca vašej cesty. Diéty na ubytovanie, stravu a vedľajšie (iné výdavky) sa vypočítavajú na základe dennej dávky, ktorá je nastavená pre vybrané miesto.

    Napríklad si vyberiete ako miesto **Redmond (USA)**. Denný príspevok pre túto lokalitu je 150 amerických dolárov (150 USD) na ubytovanie, 75 USD na jedlo a 5 USD na vedľajšie výdavky. Dátum začiatku je 10. januára a dátum ukončenia je 14. januára. Preto je vybraté trvanie päť dní, keď je zvolená konfigurácia kalendárnych dní s časom a vybratý čas začína a končí o 00:00 v dátumoch začiatku a konca. Tu sú výpočty:

    - Celková splatná suma = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
    - Strava a vedľajšia časť z celkovej sumy = 5 × (75 + 5) = USD 400

Ak boli počas cesty poskytnuté raňajky, obedy a večere, tieto jedlá sa musia zaúčtovať ako krátenie stravného.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Príklad 1: Denné diéty, kde je krátenie stravného založené na druhu jedla na cestu

V tomto príklade je zníženie stravného o 30 percent pre raňajky, 30 percent pre obed a 40 percent pre večeru. Na stránke **Parametre správy výdavkov** je pole **Vypočítať zníženie stravného o** nastavené na **Druh stravovania na ceste**. Tu sú výpočty, ak boli zamestnancovi poskytnuté troje raňajky, dva obedy a nula večerí:

- Zníženie stravného = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112,50
- Jedlá a vedľajšie výdavky = 400 – 112,50 = USD 287,50
- Celková splatná suma = Celkový príspevok – Zníženie stravného = 1150 – 112,50 = USD 1037,50

![Diéty, kde je zníženie stravného založené na druhu jedla na cestu.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Príklad 2: Diéty, kde je zníženie stravného založené na druhu jedla na deň

V tomto príklade je zníženie stravného o 30 percent pre raňajky, 30 percent pre obed a 40 percent pre večeru. Na stránke **Parametre správy výdavkov** je pole **Vypočítať zníženie stravného o** nastavené na **Druh stravovania na deň**. V tomto prípade v mriežke **Jedlá** v dialógovom okne **Upraviť výdavok** zrušíte začiarknutie políčok, aby ste označili, ktoré jedlá vám boli poskytnuté počas vašej cesty.

Tu sú napríklad výpočty, ak boli raňajky poskytnuté počas prvých troch dní cesty:

- Denné zníženie stravného za každý z prvých troch dní = 75 × 30 % = USD 22,50
- Celkové zníženie stravného = 3 × 22,50 = USD 67,50
- Jedlá a vedľajšie výdavky za 1. až 3. deň = 75 – 22,50 = USD 57,50
- Celkové jedlá a vedľajšie výdavky = Súčet jedál a vedľajších výdavkov za päť dní = 400 – 67,50 = USD 332,50
- Celková splatná suma = Celková suma – Zníženie stravného = 1150 – 67,50 = USD 1082,50

![Diéty, kde je zníženie stravného založené na druhu jedla na deň.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Príklad 3: Diéty, kde je zníženie stravného založené na počte jedál na deň

V tomto príklade sa zníženie stravného vypočíta na základe počtu jedál, ktoré boli poskytnuté za deň (t. j. pole **Vypočítajte zníženie stravného o** na stránke **Parametre správy výdavkov** je nastavené na **Počet jedál za deň**). V mriežke **Jedlá** v dialógovom okne **Upraviť výdavok** zrušíte začiarknutie políčok, aby ste označili, ktoré jedlá vám boli poskytnuté.
V tomto prípade je zníženie stravného založené len na počte poskytnutých jedál a nie na druhu poskytnutej stravy (raňajky/obed/večera).

Tu sú výpočty diét, keď je denná dávka USD 150 na ubytovanie, USD 75 na jedlo a USD 5 na vedľajšie výdavky:

- **Celková splatná suma** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1150
- **Jedno jedlo:** Zníženie stravného = 20 % = USD 15
- **Dve jedlá:** Zníženie stravného = 50 % = USD 37,50
- **Tri jedlá:** Zníženie stravného = 100 % = USD 75

Tu sú výpočty pre **príspevok na stravovanie a vedľajšie výdavky**, ktorý obsahuje USD 5 pre vedľajšie výdavky:

- Deň 1 – Dve jedlá zabezpečené = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Deň 2 – Dve jedlá zabezpečené = (75 – 37,50) + 5 = 37,50 + 5 = USD 42,50
- Deň 3 – Jedno jedlo zabezpečené = (75 – 15) + 5 = 60 + 5 = USD 65
- Deň 4 – Nula jedál zabezpečených = (75 – 0) + 5 = 75 + 5 = USD 80
- Deň 5 – Tri jedlá zabezpečené = (75 – 75) + 5 = 0 + 5 = USD 5

- Celkový počet jedál a vedľajších výdavkov = Jedlá a vedľajšie výdavky za deň 1+ deň 2 + deň 3 + deň 4+ deň 5 = USD 235
- Celkové zníženie stravného = Zníženie stravného za deň 1+ deň 2 +deň 3+deň 4+ deň 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Celková splatná suma = Celkový príspevok – Celkové zníženie stravného = USD 1150 – USD 165 = USD 985

![Diéty, kde je zníženie stravného založené na počte jedál na deň.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od verzie Financie 10.0.23, ak používate prepracované rozhranie výdavkov, nemôžete vytvárať výdavky na diéty, ktoré majú prekrývajúce sa dátumy. Ak to skúsite, zobrazí sa chybové hlásenie.
