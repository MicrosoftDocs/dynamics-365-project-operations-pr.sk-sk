---
title: Denné výdavky
description: Táto téma poskytuje informácie o tom, ako pracovať s výdavkami na diéty.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596069"
---
# <a name="per-diem-expenses"></a>Denné výdavky

> [!IMPORTANT] 
> Funkcia, ktorá je popísaná v tejto téme, je dostupná pre cieľových používateľov ako súčasť predbežnej verzie.

Diem platba je pevná, vopred určená denná dávka, ktorú spoločnosť vypláca svojim zamestnancom za ubytovanie (hotely), stravu a vedľajšie výdavky, ktoré títo zamestnanci vynaložia počas cesty za prácou. Spoločnosť vypláca tento príspevok zamestnancom namiesto úhrady skutočných cestovných nákladov. Zamestnanci môžu využiť ich **Príležitostné/Iné** denný príspevok na pokrytie sprepitného, izbovej služby, práčovne alebo čistiarne pre dôležité obchodné stretnutia. Denná sadzba sa môže líšiť v závislosti od toho, či sa zamestnávateľ rozhodne preplatiť kombinované náklady na ubytovanie a stravu, alebo len náklady na stravu a vedľajšie výdavky.

Sadzby za diéty môžu byť založené na ročnom období, mieste cesty alebo oboch. Keď vytvoríte pravidlo pre denné diéty, môžete určiť, že určité percento dennej sadzby bude zadržané, ak zamestnanec dostane bezplatné jedlá alebo služby. Môžete tiež nastaviť minimálny počet hodín a maximálny počet hodín, počas ktorých je možné uplatniť diétnu sadzbu na cestu zamestnanca.

Denné diéty sa vypočítajú ako celková dávka, ktorá sa ponúka za deň, znížená o zníženie stravy (náklady na bezplatné stravovanie), ktoré sa poskytuje zamestnancovi.

## <a name="configure-per-diems"></a>Konfigurovať podľa diét

Ak chcete nakonfigurovať výdavky na diéty, postupujte podľa týchto krokov.

1. Ísť do **Riadenie výdavkov** \> **Nastaviť** \> **generál** \> **Parametre riadenia výdavkov**.
2. Na **Denne** kartu, v **Vypočítajte zníženie jedla o** vyberte spôsob výpočtu diét:

    - **Druh jedla na cestu** – Vypočítajte diéty na základe zadaného druhu jedla (raňajky, obed alebo večera) a krátenia stravy, ktoré je uvedené pre každý druh stravy pre diétu počas trvania cesty.
    - **Druh jedla za deň** – Vypočítajte diétu na základe typu zadaného jedla a zníženia stravy, ktoré je špecifikované pre každý druh stravy pre diétu na deň.
    - **Počet jedál za deň** – Vypočítajte diéty na základe počtu zadaných jedál za deň a zníženia stravy za počet jedál, ktoré sa poskytujú každý deň.

3. Ísť do **Riadenie výdavkov** \> **Nastaviť** \> **Výpočty a kódy** \> **Miesta na denné**.
4. Pridajte miesta, kde je možné použiť diéty.
5. Pre každé miesto, ktoré pridáte, na **Na diéty** vyberte dennú sadzbu a menu, ktoré sú platné medzi konkrétnymi dátumami začiatku a konca pre ubytovanie, stravu a iné výdavky. Ak chcete nakonfigurovať denné sadzby a meny, prejdite na **Riadenie výdavkov** \> **Nastaviť** \> **Výpočty a kódy** \> **Na diéty**.

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Denné diéty v prepracovanom rozhraní výdavkov

Funkcia denného príjmu je podporovaná v reimagined **Riadenie nákladov** pracovný priestor v Microsoft Dynamics 365 Finance verzia 10.0.25 a novšia.

Ak chcete povoliť diéty, postupujte podľa týchto krokov.

1. V **Správa funkcií** pracovný priestor, nájdite a vyberte **Prepracované výkazy výdavkov** v zozname a potom vyberte **Povoliť teraz**.
2. Nájdite a vyberte **Prepracované rozhranie pre denné pre výkaz výdavkov** v zozname a potom vyberte **Povoliť teraz**.

## <a name="how-the-feature-works"></a>Ako funkcia funguje

Táto časť obsahuje príklady troch scenárov konfigurácie. Pre každý príklad, **Vypočítajte zníženie jedla o** pole je nastavené na inú hodnotu. Pre všetky tri príklady je celková suma, ktorá je splatná, rovnaká, kým sa neuplatní zníženie stravného. Po tomto bode sa celková splatná suma pre každý príklad líši.

Ak chcete vytvoriť výdavky na diéty, ktoré sa používajú pre všetky tri príklady, postupujte podľa týchto krokov.

1. Ísť do **Pracovné priestory** \> **Riadenie nákladov**.
2. Vyberte **Nová správa o výdavkoch** alebo vyberte existujúci výkaz výdavkov.
3. Pridajte nový výdavok. V **Kategória** pole, vyberte **Denne**. Vyberte miesto a dátum začiatku a konca vašej cesty. Diéty za ubytovanie, stravu a vedľajšie (iné výdavky) sa vypočítavajú na základe dennej dávky, ktorá je stanovená pre vybrané miesto.

    Napríklad si vyberiete **Redmond (USA)** ako umiestnenie. Denný príspevok pre túto lokalitu je 150 amerických dolárov (150 USD) na ubytovanie, USD 75 na jedlo a USD 5 na vedľajšie výdavky. Počiatočný dátum je 10. januára a dátum ukončenia je 14. januára. Preto je vybraté trvanie päť dní, keď je zvolená konfigurácia kalendárnych dní s časom a vybratý čas začína a končí o 00:00 v dátumoch začiatku a konca. Tu sú výpočty:

    - Celková splatná suma = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Strava a vedľajšia časť z celkovej sumy = 5 × (75 + 5) = USD 400

Ak boli počas cesty poskytnuté raňajky, obedy a večere, tieto jedlá je potrebné zaúčtovať ako krátenie stravy.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>Príklad 1: Diéty, kde sú zníženia stravy založené na druhu jedla na cestu

V tomto príklade je zníženie jedla o 30 percent na raňajky, 30 percent na obed a 40 percent na večeru. Na **Parametre riadenia výdavkov** stránka, **Vypočítajte zníženie jedla o** pole je nastavené na **Druh jedla na cestu**. Tu sú výpočty, ak boli zamestnancovi poskytnuté tri raňajky, dva obedy a nula večerí:

- Zníženie jedla = (3 ×\[ 75 × 30 %\]) + (2 ×\[ 75 × 30 %\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Jedlá a vedľajšie jedlá = 400 – 112,50 = USD 287.50
- Celková splatná suma = celkový príspevok – zníženie stravy = 1 150 – 112,50 = USD 1,037.50

![Výdavky na diéty, kde je zníženie stravy založené na druhu jedla na cestu.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>Príklad 2: Denné diéty, kde redukcia jedla je založená na druhu jedla za deň

V tomto príklade je zníženie jedla o 30 percent na raňajky, 30 percent na obed a 40 percent na večeru. Na **Parametre riadenia výdavkov** stránka, **Vypočítajte zníženie jedla o** pole je nastavené na **Druh jedla za deň**. V tomto prípade v **Jedlá** mriežka v **Upraviť výdavok** dialógovom okne zrušíte začiarknutie políčok, aby ste označili, ktoré jedlá vám boli poskytnuté počas vašej cesty.

Tu sú napríklad výpočty, ak boli raňajky poskytnuté počas prvých troch dní cesty:

- Denné zníženie jedla za každý z prvých troch dní = 75 × 30 % = USD 22.50
- Celkové zníženie jedla = 3 × 22,50 = USD 67.50
- Jedlá a vedľajšie jedlá za 1. až 3. deň = 75 – 22,50 = USD 57.50
- Celkové jedlá a vedľajšie jedlá = súčet jedál a vedľajších výdavkov za päť dní = 400 – 67,50 = USD 332.50
- Celková splatná suma = Celková suma – Zníženie stravy = 1 150 – 67,50 = USD 1,082.50

![Výdavky na diéty, kde zníženie jedla je založené na druhu jedla za deň.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>Príklad 3: Denné diéty, kde zníženie stravy je založené na počte jedál za deň

V tomto príklade sa krátenie jedla vypočíta na základe počtu jedál, ktoré boli poskytnuté za deň (t.j **Vypočítajte zníženie jedla o** pole na **Parametre riadenia výdavkov** stránka je nastavená na **Počet jedál za deň**). V **Jedlá** mriežka v **Upraviť výdavok** dialógovom okne zrušíte začiarknutie políčok, aby ste označili, ktoré jedlá boli poskytnuté.
V tomto prípade je krátenie stravy založené len na počte poskytnutých jedál a nie na druhu poskytnutej stravy (Raňajky/obed/večera).

Tu sú výpočty denných diét, keď je denná dávka USD 150 na ubytovanie, USD 75 na jedlo a USD 5 na vedľajšie výdavky:

- **Celková splatná suma** = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Jedno jedlo:** Zníženie jedla = 20 % = USD 15
- **Dve jedlá:** Zníženie jedla = 50 % = USD 37.50
- **Tri jedlá:** Zníženie jedla = 100 % = USD 75

Tu sú výpočty pre **príspevok na stravovanie a vedľajšie výdavky**, ktorý obsahuje USD 5 pre vedľajšie:

- Deň 1 – dve jedlá zabezpečené = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- Deň 2 – dve jedlá zabezpečené = (75 – 37,50) + 5 = 37,50 + 5 = USD 42.50
- Deň 3 – jedno jedlo poskytnuté = (75 – 15) + 5 = 60 + 5 = USD 65
- Deň 4 – nula poskytnutých jedál = (75-0) + 5 = 75 + 5 = USD 80
- 5. deň – poskytnuté tri jedlá = (75 – 75) + 5 = 0 + 5 = USD 5

- Celkový počet jedál a vedľajších jedál = jedlá a vedľajšie jedlá za deň 1+ deň 2 + deň 3 + deň 4+ deň 5 = USD 235
- Celkové zníženie jedla = Zníženie jedla za deň 1+ deň 2 +deň 3+deň 4+ deň 5= 37,5+ 37,5+ 15 + 0+ 75 = USD 165
- Celková splatná suma = Celkový príspevok – Celkové zníženie stravy = USD 1,150 - USD 165 = USD 985

![Výdavky na diéty, kde zníženie stravy je založené na počte jedál za deň.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Od verzie Financie 10.0.23, ak používate prepracované rozhranie výdavkov, nemôžete vytvárať výdavky na diéty, ktoré majú prekrývajúce sa dátumy. Ak sa pokúsite, dostanete chybové hlásenie.
