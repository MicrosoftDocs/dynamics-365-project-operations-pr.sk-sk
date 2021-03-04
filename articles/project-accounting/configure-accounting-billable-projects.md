---
title: Konfigurácia účtovníctva pre fakturovateľné projekty
description: Táto téma poskytuje informácie o možnostiach účtovníctva pre fakturovateľné projekty.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 47bb5671c7b80c0e96f3f65e9c4d25f6da8184a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131992"
---
# <a name="configure-accounting-for-billable-projects"></a>Konfigurácia účtovníctva pre fakturovateľné projekty

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations podporuje rôzne možnosti účtovníctva pre fakturovateľné projekty, ktoré zahŕňajú časové a materiálne transakcie a transakcie s pevnou cenou.

- **Transakcie času a materiálu** : Tieto transakcie sú fakturované podľa postupu práce na základe spotreby hodín, výdavkov, položiek alebo poplatkov za projekt. Tieto transakčné náklady je možné porovnať s výnosmi z každej transakcie a projekt je fakturovaný podľa postupu prác. Výnosy z projektu je možné akumulovať aj v čase, keď dôjde k transakcii. Počas fakturácie sú výnosy vykázané a akumulované výnosy sú prípadne vrátené.
- **Transakcie s pevnou cenou**: Tieto transakcie sa fakturujú podľa plánu fakturácie, ktorý je založený na zmluve o projekte. Výnosy z transakcií s pevnou cenou je možné vykázať pri fakturácii alebo vypočítať a pravidelne účtovať podľa metódy **Dokončená zmluva** alebo **Dokončené percento**.

Projekt sa považuje za zúčtovateľný, ak je spojený s jednou alebo viacerými riadkami zmluvy. Riadok zmluvy projektu sám definuje, ktoré spôsoby účtovania a typy transakcií sú povolené.

Napríklad spoločnosť Fabrikam Robotics získala zmluvu na projekt so spoločnosťou Adatum corporation na optimalizáciu vybavenia. Adatum zaplatí pevnú sumu 10 000 USD na pokrytie vzniknutých výdavkov na projekt. Toto je metóda fakturácie s pevnou cenou. Čas projektu a poplatky budú účtované za každé použitie. Toto je spôsob fakturácie času a materiálu. Všetky práce budú sledované v rámci jedného projektu s názvom Optimalizácia vybavenia Adatum.

Člen projektového tímu predloží osem hodín práce na projekte optimalizácie vybavenia Adatum. Keď projektový manažér schváli tento čas, systém použije metódu fakturácie času a materiálu na vytvorenie transakcií skutočných hodnôt, faktúry a účtu. Táto transakcia nebude zahrnutá do výpočtu odhadu výnosov z pevnej ceny.

Ďalší člen projektového tímu predkladá cestovné náklady za 2000,00 USD na projekt optimalizácie vybavenia Adatum. Keď projektový manažér schváli toto predloženie, systém použije metódu fakturácie s pevnou cenou na vytvorenie transakcií skutočných hodnôt, faktúry a účtu pre výdavky za tento projekt. Na základe tejto transakcie nebude zákazníkovi fakturovaná žiadna čiastka. Namiesto toho sa budú fakturovať pomocou osobitne nakonfigurovaných medzníkov fakturácie. Táto transakcia výdavkov bude spolu s odhadmi výdavkov zahrnutá do výpočtu odhadu výnosov z pevnej ceny.

Účtovné zásady pre projektové transakcie sú definované v profiloch nákladov a výnosov projektu. Pre každú projektovú transakciu systém určuje vhodný profil nákladov a výnosov projektu pomocou pravidiel profilu nákladov a výnosov projektu, ktoré boli nakonfigurované.

## <a name="define-project-cost-and-revenue-profiles"></a>Definovanie profilov projektových nákladov a výnosov 

Profily nákladov a výnosov projektu určujú účtovné pravidlá pre transakcie projektu. Tieto profily sú konfigurované v časti Riadenie projektu a účtovníctvo. 

Vykonaním nasledujúcich krokov vytvoríte nový profil nákladov a výnosov projektu. 

1. Prejdite do **Riadenie projektu a účtovníctvo** > **Nastavenie** > **Zaúčtovanie** > **Profily nákladov a výnosov projektu**. 
2. Vyberte **Nový** na vytvorenie nového profilu nákladov a výnosov projektu.
3. V poli **Názov** zadajte názov a stručný popis profilu.
4. V poli **Spôsob fakturácie** vyberte **Čas a materiál** alebo **Pevná cena**.
5. Rozbaľte rýchlu kartu **Hlavná kniha**. Polia na tejto karte definujú účtovné zásady, ktoré sa používajú, keď sa transakcie projektu zaznamenávajú do účtovného denníka pomocou denníka integrácie Project Operations a potom sa fakturujú prostredníctvom návrhu projektovej faktúry.
6. Vyberte príslušné informácie v nasledujúcich poliach na rýchlej karte **Hlavná kniha**:

    - **Náklady na príspevok – hodina**:

       - *Žiadna hlavná kniha*: Náklady za časové transakcie sa nebudú účtovať do hlavnej knihy, keď sa zaúčtuje integračný denník Project Operations. Účtovník však môže zaúčtovať náklady na príspevok neskôr pomocou funkcie Náklady na príspevok.
       - **Zostatok**: Cena za časové transakcie sa zaúčtuje na typ účtu Hlavná kniha, *WIP – hodnota nákladov* a pripísané na *Účet alokácie miezd* v časti Nastavenia zverejňovania v hlavnej knihe. Účtovník bude pomocou funkcie Náklady na príspevok pravidelne prevádzať tieto náklady z účtu zostatku na účet ziskov a strát.
       - **Zisk a strata**: Pri zverejňovaní integračného denníka Project Operations sa náklady časovej transakcie zaúčtujú na typ účtu *Náklady* hlavnej knihy a pripísané na *Účet alokácie miezd* definovaný na karte **Náklady** na stránke **Nastavenia zverejňovania v hlavnej knihe** (**Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Zaúčtovanie** \> **Nastavenia zverejňovania v hlavnej knihe**). Toto je najbežnejšie nastavenie pre transakcie času a materiálu.
        - *Nikdy nepoužívať hlavnú knihu*: Náklad za časové transakcie sa nikdy nezaúčtuje do hlavnej knihy.

    - **Náklady na príspevok – výdavok**:

         - **Zostatok**: Pri zverejňovaní integračného denníka Project Operations sa náklady nákladovej transakcie zaúčtujú na typ účtu Účtovná kniha *WIP – hodnota nákladov* podľa definície na karte **Náklady** na stránke **Nastavenia zverejňovania v hlavnej knihe** a pripísaná na účet s odchýlkou v zázname v účtovnom denníku. Predvolené účty s odchýlkou pre výdavky sú definované v časti **Projektové riadenie a účtovníctvo** > **Nastaviť** \> **Zaúčtovanie** \> **Predvolený účet s odchýlkami pre výdavky**. Účtovník bude pomocou funkcie **Náklady na príspevok** pravidelne prevádzať tieto náklady z účtu zostatku na účet ziskov a strát.
        - **Zisk a strata**: Pri zverejňovaní integračného denníka Project Operations sa náklady nákladovej transakcie zaúčtujú na typ účtu Účtovná kniha *Náklady* podľa definície na karte **Náklady** na stránke **Nastavenia zverejňovania v hlavnej knihe** a pripísaná na účet s odchýlkou v zázname v účtovnom denníku. Predvolené účty s odchýlkou pre výdavky sú definované v časti **Projektové riadenie a účtovníctvo** \> **Nastaviť** \> **Zaúčtovanie** \> **Predvolený účet s odchýlkami pre výdavky**.
       
    - **Fakturácia na účet**:

        - **Zostatok**: Pri zverejňovaní návrhov projektových faktúr sa transakcia na účet (medzník fakturácie) pripíše na typ účtu Účtovná kniha *WIP fakturované – na účet* podľa definície na karte **Príjmy** na stránke **Nastavenia zverejňovania v hlavnej knihe** a zaúčtovaná na účet zostatku zákazníka.
         - **Zisk a strata**: Pri zverejňovaní návrhov projektových faktúr sa transakcia na účet (medzník fakturácie) pripíše na typ účtu Účtovná kniha *Fakturované výnosy – na účet* podľa definície na karte **Príjmy** na stránke **Nastavenia zverejňovania v hlavnej knihe** a zaúčtovaná na účet zostatku zákazníka. Účty zostatkov zákazníkov sú definované v časti **Pohľadávky** \> **Nastaviť** \> **Profily zverejňovania zákazníka**.

   Keď definujete profily zverejňovania pre spôsoby fakturácie času a materiálu, máte možnosť nazhromaždiť výnosy podľa typu transakcie (hodiny, výdavok a poplatok). Ak je možnosť **Prírastok** nastavená na **Áno**, nevyfakturované predajné transakcie v integračnom denníku Project Operations sa zaznamenajú do všeobecnej hlavnej knihy. Hodnota predaja sa zaúčtuje na **WIP – účet hodnoty predaja** a pripíšu na účet **Prírastky – hodnota predaja**, ktorý bol nastavený na stránke **Nastavenie zverejňovania v hlavnej knihe** na karte **Výnosy**. 
  
  > [!NOTE]
  > Možnosť **Prírastok** je k dispozícii iba v prípade, že príslušný typ transakcie **Náklady** sa zaúčtuje na účet ziskov a strát.
    
7. Rozbaľte rýchlu kartu **Odhadované**. Polia na tejto karte definujú nastavenia výpočtu pre odhady výnosov z pevnej ceny. Polia na tejto karte sa vzťahujú iba na profily nákladov a výnosov projektu s fakturačnou metódou **Pevná cena**.
8. Vyberte príslušné informácie v nasledujúcich poliach na rýchlej karte **Odhadované**:

    - **Zásada použitá pri výpočtoch dokončenia projektu**:

        - **Dokončená zmluva**: Zhoda nákladov a vykázanie výnosov nastane až na konci projektu. Náklady sa v zostatku prejavia ako WIP, kým nie je projekt dokončený.
        - **Dokončené percento**: Časové rozlíšenie výnosov sa počíta a účtuje do hlavnej knihy každé obdobie na základe percenta dokončenia projektu. Existuje niekoľko metód na výpočet percentuálneho podielu dokončenia. Tieto metódy môžu byť automatické na základe konfigurácie alebo manuálne.
        - **Žiadne WIP**: Toto nastavenie sa používa pre projekty s pevnou cenou s krátkym časovým rozpätím, kde sa faktúra a náklady vyskytujú v rovnakom období. V takom prípade je hodnota poľa **Fakturácia na účet** na rýchlej karte **Hlavná kniha** automaticky nastavená na **Zisk a strata**, aby sa zabezpečilo vykázanie výnosov pri fakturácii. Proces odhadu výnosov sa nepoužije pre profil nákladov a výnosov tohto projektu.

    - **Princíp zhody**: Toto pole určuje, ako sa bude vypočítaná hodnota predaja (akumulovaný výnos) účtovať do hlavnej knihy.

        - Pomocou princípu **Hodnota predaja** systém vypočíta hodnotu predaja porovnaním nákladov a výnosov a potom ich zaúčtuje ako jednu sumu.
        - Pomocou princípu **Výroba a zisk** systém rozdelí hodnotu predaja na realizované náklady a vypočítaný zisk. Tieto sa zverejňujú osobitne.

    - **Šablóny nákladov**: Umožňuje zoskupiť transakcie projektu na základe typu transakcie a kategórie projektu a definovať pravidlá výpočtu percentuálneho dokončenia pre tieto skupiny.
    - **Kódy obdobia**: Definuje frekvenciu, s akou sa počítajú odhady výnosov pre daný profil nákladov a výnosov projektu.
    - **Kategórie pre odhad**: Používa sa na zverejňovanie predajnej hodnoty (akumulovaného výnosu) do transakcií projektu. Najskôr nakonfigurujte kategóriu vyhradeného projektu pre typ transakcie **Poplatok** a potom nastavte príznak **Odhad** pre túto kategóriu projektu. Ďalej v závislosti od zvoleného princípu zhody vyberte túto kategóriu projektu v hodnote **Predaj** alebo v poli **Zisk** v profile nákladov a výnosov projektu.

### <a name="sample-configurations-for-project-cost-and-revenue-profiles"></a>Vzorové konfigurácie profilov nákladov a výnosov projektu

Čas a materiály – žiadne WIP

![Profil nákladov a výnosov: čas a materiály – žiadne WIP](media/time-material-no-wip.png)

Čas a materiály – WIP (výnosy)

![Profil nákladov a výnosov: čas a materiály – WIP](media/time-material-with-wip.png)

Pevná cena – žiadne WIP

![Profil nákladov a výnosov: pevná cena – žiadne WIP](media/fixed-price-no-wip.png)

Pevná cena – dokončená zmluva

![Profil nákladov a výnosov: pevná cena – dokončená zmluva](media/fixed-price-completed-contract.png)

Pevná cena – dokončenie v percentách

![Profil nákladov a výnosov: pevná cena – dokončenie v percentách](media/fixed-price-completed-percentage.png)


## <a name="accounting-event-examples-for-sample-project-cost-and-revenue-profiles"></a>Príklady účtovných udalostí pre vzorové profily nákladov a výnosov projektu.

| Účtovná udalosť                  | Čas a materiál – žiadne WIP                       | Čas a materiál – WIP                                                                                           | Pevná cena – žiadne WIP                                            | Pevná cena – dokončená zmluva                                                                            | Pevná cena – dokončenie v percentách                             |
|-----------------------------------|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| Zaznamenanie časových transakcií do účtovného denníka    | Debet – náklady <br>Kredit – alokácia miezd          | Debet – náklady <br>Kredit – alokácia miezd <br>Debet – hodnota predaja WIP <br>Kredit – Hodnota predaja akumulovaných výnosov                | Debet – náklady <br>Kredit – alokácia miezd                         | Debet – náklady <br>Kredit – alokácia miezd                                                                    | Debet – náklady <br>Kredit – alokácia miezd                       |
| Zaznamenanie výdavkových transakcií do účtovného denníka | Debet – náklady <br>Kredit – účet s odchýlkami pre výdavky | Debet – náklady <br>Kredit – účet s odchýlkami pre výdavky <br>Debet – hodnota predaja WIP <br>Kredit – Hodnota predaja akumulovaných výnosov      | Debet – náklady <br>Kredit – účet s odchýlkami pre výdavky                 | Debet – náklady<br> Kredit – účet s odchýlkami pre výdavky                                                            | Debet – náklady <br>Kredit – účet s odchýlkami pre výdavky               |
| Fakturácia zákazníka                | Debet – zostatok zákazníka <br>Kredit – fakturovaný príjem | Debet – zostatok zákazníka <br>Kredit – fakturovaný príjem <br>Kredit – debetná hodnota predaja WIP – hodnota predaja akumulovaných výnosov | Debet – zostatok zákazníka <br>Kredit – Fakturovaný príjem – na účet | Debet – zostatok zákazníka <br>Kredit – WIP – Fakturované na účet                                                  | Debet – zostatok zákazníka <br>Kredit – WIP – Fakturované na účet    |
| Odhadované príjmy po zaúčtovaní             | Nevzťahuje sa                                   | Nevzťahuje sa                                                                                                    | Nevzťahuje sa                                                  | Debet – hodnota nákladov na WIP <br>Kredit – náklady                                                                         | Debet – WIP – hodnota predaja <br>Kredit – Hodnota predaja akumulovaných výnosov |
| Eliminovať                         | Nevzťahuje sa                                   | Nevzťahuje sa                                                                                                    | Nevzťahuje sa                                                  | Kredit – hodnota nákladov na WIP <br>Debet – náklady <br>Kredit – akumulované výnosy – hodnota predaja <br>Debet – WIP fakturované na účet | Debet – WIP – fakturované na účet <br>Kredit – hodnota predaja WIP     |

## <a name="configure-project-cost-and-revenue-profile-rules"></a>Konfigurácia pravidiel profilov nákladov a výnosov projektu

Pravidlá profilu nákladov a výnosov projektu určujú profil nákladov a výnosov projektu, ktoré sa musia použiť pri spracovaní akýchkoľvek fakturovateľných transakcií projektu. Pravidlá definujte tak, že prejdete na **Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Zaúčtovanie** \> **Pravidlá profilu nákladov a výnosov projektu**.

Pravidlá môžu byť definované zmluvou o projekte, projektovou skupinou alebo konkrétnym projektom. Systém vždy najskôr vyberie pravidlo najvyššej podrobnosti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]