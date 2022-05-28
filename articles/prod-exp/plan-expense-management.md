---
title: Konfigurácia správy výdavkov
description: Tento článok popisuje úvahy a rozhodnutia, ktoré musíte urobiť počas procesu plánovania pred konfiguráciou správy výdavkov Microsoft Dynamics 365 Financie.
author: KimANelson
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d919a26000b127dd6fb2fd8a49d79e3087f1c403
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710157"
---
# <a name="configure-expense-management"></a>Konfigurácia správy výdavkov

Táto téma popisuje úvahy a rozhodnutia, ktoré musíte urobiť počas procesu plánovania pred konfiguráciou správy výdavkov. V správe výdavkov môžete ukladať informácie o spôsoboch platby, cestovných požiadavkách, správach o výdavkoch, pravidlách atď.

Pretože veľa rozhodnutí, ktoré urobíte pri plánovaní svojej konfigurácie pre správu výdavkov, je založených na hierarchii a finančnej štruktúre vašej organizácie, musíte si prečítať plánovacie dokumenty pre tieto oblasti.

## <a name="intercompany-expenses"></a>Medzipodnikové výdavky

Ak povolíte medzipodnikové výdavky, umožníte právnickým osobám a zamestnancom znášať výdavky v mene inej právnickej osoby a vyberať platby od právnických osôb, ktoré sú zamestnancami vo vašej organizácii. Napríklad zamestnanec v právnickej osobe A dokončí projekt pre právnickú osobu B a v rámci projektu vzniknú cestovné náklady. Ak sú povolené medzipodnikové výdavky, zamestnanec môže potom podať výkaz výdavkov, ktorý zaúčtuje náklady právnickej osobe B, a výdavok musí potom zaplatiť právnická osoba A. Ak vaša organizácia nemá viac právnických osôb, nemusíte povoliť medzipodnikové výdavky.

**Rozhodnutie:** Chcete povoliť medzipodnikové výdavky?

## <a name="financial-management"></a>Finančný manažment

Správa výdavkov je úzko prepojená s finančným riadením vašej organizácie. Mnoho konfigurácie pre správu výdavkov bude závisieť od vašich rozhodnutí o financiách vašej organizácie. Nasledujúce časti popisujú rôzne oblasti, ktoré si vyžadujú plánovanie a rozhodovanie na základe finančných rozhodnutí vašej organizácie a na vedení vášho vodcovského tímu.

### <a name="per-diems"></a>Za každý deň

Musíte definovať diéty zamestnancov, ktoré poskytuje vaša organizácia. Pretože diéty sa zvyčajne používajú na pokrytie výdavkov, ako je strava, ubytovanie a ďalšie vedľajšie výdavky, môžete vytvoriť pravidlá pre denné diéty, ktoré vaša organizácia ponúka. Sadzby za diéty môžu byť založené na ročnom období, mieste cesty alebo oboch. Keď definujete pravidlo týkajúce sa diéty, môžete určiť, že bude zadržané percento z diéty, ak pracovník dostane bezplatné stravovanie alebo služby. Môžete tiež definovať triedy sadzieb diét na stanovenie minimálneho a maximálneho počtu hodín, pre ktoré môže platiť diéta pre cestu pracovníka.

**Rozhodnutia:**

- Predvolené pravidlá diéty pre prvý a posledný deň:

    - Aký je minimálny počet hodín, ktoré si zamestnanec môže nárokovať za deň a stále dostávať diéty?
    - Dochádza k zníženiu sumy, ktorá sa ponúka za jedlo prvý a posledný deň? Ak dôjde k zníženiu, aké je percento zníženia?
    - Dochádza k zníženiu sumy, ktorá sa ponúka za hotel prvý a posledný deň? Ak dôjde k zníženiu, aké je percento zníženia?
    - Dochádza k zníženiu sumy, ktorá sa ponúka za iné náklady vzniknuté prvý a posledný deň? Ak dôjde k zníženiu, aké je percento zníženia?

- Predvolené pravidlá diét:

    - Dochádza k percentuálnemu zníženiu diét za každé jedlo, ak je napríklad jedlo bezplatné? Ak dôjde k zníženiu, aké je percento zníženia pre každé jedlo?
    - Počíta sa zníženie na jedlo vypočítané za deň, na cestu alebo podľa počtu jedál za deň?
    - Mali by byť sumy za diéty zaokrúhlené bežným spôsobom alebo zaokrúhlené nahor?
    - Počítajú sa diéty za 24 hodín alebo za kalendárny deň?

- Pravidlá diéty založené na umiestnení:

    - Líšia sa sadzby diéty podľa miesta? Aké miesta sú zahrnuté?
    - Ak sa sadzby za diéty líšia v závislosti od lokality, pre každú lokalitu sa uvádza percentuálna suma pri nasledujúcich druhoch výdavkov:

        - Jedlá
        - Hotel
        - Iné výdavky

### <a name="expense-management-journals-and-accounts"></a>Denníky a účty riadenia výdavkov

Správa výdavkov vyžaduje, aby ste používali viac denníkov a účtov. Musíte sa napríklad rozhodnúť, či sa ten istý účet používa na hotovostné zálohy a spory o kreditné karty.

**Rozhodnutia:**

- Do ktorého denníka hlavnej knihy sa zaúčtujú schválené výkazy výdavkov?
- Aký účet sa používa na hotovostné zálohy?
- Mali by sa peňažné zálohy zaúčtovať okamžite?

### <a name="payment-methods"></a>Spôsoby platby

Ak zamestnancom umožníte, aby v mene vašej firmy znášali výdavky, musíte definovať spôsoby platby, ktoré môžu zamestnanci používať. Môžete napríklad povoliť zamestnancom používať hotovosť alebo firemnú kreditnú kartu. Môžete tiež umožniť zamestnancom používať osobné kreditné karty a potom zamestnancom refundovať náklady. Pre každý povolený spôsob platby musíte urobiť nasledujúce rozhodnutia.

**Rozhodnutia:**

- Aké spôsoby platby sú povolené?
- Kto vlastní výdavky na spôsob platby?
- Existuje typ offsetového účtu? Ak existuje typ offsetového účtu, čo to je?
- Ak existuje typ offsetového účtu, aký je účet?
- Ak je platobnou metódou kreditná karta, mala by sa platobná metóda použiť iba pri importovaných transakciách?

### <a name="expense-categories-and-shared-categories"></a>Kategórie výdavkov a zdieľané kategórie

Keď zamestnanci vytvárajú výkaz výdavkov, každý výdavok, ktorý zaznamenajú, musí byť priradený ku kategórii výdavkov. Kategórie výdavkov sú odvodené od zdieľaných kategórií, ktoré je možné zdieľať medzi právnymi entitami vo vašej organizácii. Tieto kategórie možno zdieľať aj v rámci riadenia projektu a účtovníctva v závislosti od toho, ako je definovaná vaša organizácia. Na základe definície vašej organizácie a pokynov implementačného tímu musíte určiť, či sa kategórie, ktoré sa používajú v správe výdavkov, použijú iba v správe výdavkov, alebo či sa majú zdieľať medzi správou projektu a účtovania a správou výdavkov. Upozorňujeme, že tieto kategórie možno zdieľať medzi projektom a výdavkami alebo projektom a výrobou, no nie medzi výdavkami a výrobou. Pre každú kategóriu výdavkov musíte urobiť nasledujúce rozhodnutia.

**Rozhodnutia:**

- Čo je kategória výdavku? Príklady zahŕňajú kategórie letov, hotelov alebo najazdených kilometrov.
- Dá sa kategória výdavkov použiť aj v projektovom manažmente a účtovníctve?
- Čo je typ výdavku?
- Aký je predvolený spôsob platby pre kategóriu výdavkov?
- Musia byť výdavky v kategórii výdavkov rozpísané na jednotlivé položky?
- Aký je hlavný predvolený obchodný vzťah pre kategóriu výdavkov?
- Aká je predvolená skupina dane z predaja položky pre kategóriu výdavkov?
- Sú pre kategóriu výdavkov povolené ďalšie spôsoby platby? Ak sú povolené ďalšie spôsoby platby, aké sú?
- Existujú v tejto kategórii výdavkov podkategórie? Ak existujú podkategórie, musíte uskutočniť aj nasledujúce rozhodnutia:

    - Je niektorá z podkategórií vylúčená z vrátenia dane?
    - Čo je skupina dane z predaja položky v podkategóriách?

Ak sa kategória výdavkov používa aj v projektovom manažmente a účtovníctve, odpovedzte na zostávajúce otázky. V opačnom prípade prejdite na ďalšiu časť.

- Ktoré nákladové účty sa použijú na nasledujúce výdavky?

    - Náklady
    - Alokácia miezd
    - Hodnota nákladov WIP
    - Nákladová položka
    - WIP – nákladová hodnota – položka
    - Akumulovaná strata
    - WIP – akumulovaná strata

- Ktoré výnosové účty sa použijú na nasledujúce?

    - Fakturovaný príjem
    - Akumulované výnosy – hodnota predaja
    - WIP – hodnota predaja
    - Akumulované výnosy – produkcia
    - WIP – produkcia
    - Akumulované výnosy – zisk
    - WIP – zisk
    - Akumulované výnosy – predplatné
    - WIP – predplatné

### <a name="taxes"></a>Dane

Pri daniach súvisiacich s výdavkami musíte určiť, čo je zahrnuté alebo povolené v prehľadoch výdavkov.

**Rozhodnutia:**

- Je daň z obratu zahrnutá do výšky výdavkov?
- Malo by sa povoliť vrátenie dane z výdavkov?

    > [!NOTE]
    > Ak ste sa pri plánovaní hlavnej knihy rozhodli uplatniť daň z obratu v USA a použiť pravidlá dane, nemôžete povoliť vrátenie daní z výdavkov. (Ak chcete použiť daň z obratu v USA a použiť daňové pravidlá, nastavte možnosť **Použiť pravidlá zdaňovania dane z obratu** na **Áno**.)

## <a name="policies"></a>Politiky

Vytvorením politík výkazov výdavkov môžete pomôcť svojej organizácii ušetriť čas a peniaze, keď zamestnancom vzniknú v jej mene výdavky. Pravidlá pomáhajú zaručiť, že zamestnanci zostanú v rozpočte, poskytnú všetky požadované informácie a míňajú peniaze len tak, ako to požadujú. Pre každú politiku výkazov výdavkov a každú politiku schvaľovania výkazov výdavkov, ktorú vytvoríte, musíte urobiť nasledujúce rozhodnutia.

**Rozhodnutia:**

- Aký je názov politiky?
- Na čo slúži výdavková politika?
- Ak ste sa predtým rozhodli povoliť medzipodnikové výdavky, na ktoré spoločnosti vo vašej organizácii sa tieto pravidlá budú vzťahovať?
- Kedy politika nadobudne účinnosť?
- Kedy vyprší platnosť politiky?
- Aké je pravidlo politiky?
- Aký je výsledok pravidla politiky?


[!INCLUDE[footer-include](../includes/footer-banner.md)]