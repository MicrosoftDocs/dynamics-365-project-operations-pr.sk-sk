---
title: Konfigurácia medzipodnikovej fakturácie
description: Táto téma poskytuje informácie a príklady konfigurácie medzipodnikovej fakturácie pre projekty.
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09bbd1bf640cc86b16afb8c2b824329b92f833df836e9313491d57a2f1646440
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994070"
---
# <a name="configure-intercompany-invoicing"></a>Konfigurácia medzipodnikovej fakturácie

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Vykonaním nasledujúcich krokov nastavíte medzipodnikovú fakturáciu pre projekty v Dynamics 365 Project Operations. Medzipodnikové transakcie sú časové a nákladové transakcie z projektovej zmluvy, ktoré patria jednej spoločnosti alebo organizačnej jednotke, zatiaľ čo zdroje projektovej zmluvy sú súčasťou inej spoločnosti alebo organizačnej jednotky.

## <a name="example-configure-intercompany-invoicing"></a>Príklad: Konfigurácia medzipodnikovej fakturácie

V nasledujúcom príklade Contoso Robotics USA (USPM) je požičiavajúca si právnická osoba a Contoso Robotics UK (GBPM) je požičiavajúca právnická osoba. 

1. **Nakonfigurujte medzipodnikové účtovníctvo medzi právnickými osobami**. Každá dvojica požičiavajúcich si a požičiavajúcich právnických osôb musí byť nakonfigurovaná na stránke hlavnej účtovnej knihy [Medzipodnikové účtovníctvo](/dynamics365/finance/general-ledger/intercompany-accounting-setup).
    
    1. V Dynamics 365 Finance prejdite do ponuky **Hlavná účtovná kniha** > **Nastavenie zaúčtovania** > **Medzipodnikové účtovníctvo**. Vytvorte záznam s nasledujúcimi informáciami:

        - **Pôvodná spoločnosť** = **GBPM**
        - **Cieľová spoločnosť** = **USPM**

2. **Nakonfigurujte obchodný vzťah medzi právnickými osobami**. Záznam zákazníka, ktorý predstavuje požičiavajúcu si právnickú osobu, musí byť vytvorený v požičiavajúcej právnickej osobe. Záznam dodávateľa, ktorý predstavuje požičiavajúcu právnickú osobu, musí byť vytvorený v požičiavajúcej si právnickej osobe.

     1. V aplikácii Finance vyberte právnickú osobu **GBPM**.
     2. Prejdite do **Pohľadávky** > **Zákazník** > **Všetci zákazníci**. Vytvorte nový záznam pre právnickú osobu **USPM**.
     3. Rozbaľte **Názov**, odfiltrujte záznamy podľa **Typu** a vyberte **Právnické osoby**. 
     4. Nájdite a vyberte záznam zákazníka pre **Contoso Robotics USA (USPM)**.
     5. Vyberte **Použiť zhodu**. 
     6. Vyberte skupinu zákazníkov **50 - Medzipodnikoví zákazníci** a potom uložte záznam.
     7. Vyberte právnickú entitu **USPM**.
     8. Prejdite do **Záväzky** > **Dodávatelia** > **Všetci dodávatelia**. Vytvorte nový záznam pre právnickú osobu **GBPM**.
     9. Rozbaľte **Názov**, odfiltrujte záznamy podľa **Typu** a vyberte **Právnické osoby**. 
     10. Nájdite a vyberte záznam zákazníka pre **Contoso Robotics UK (GBPM)**.
     11. Vyberte **Použiť zhodu**, vyberte skupinu dodávateľov a záznam uložte.
     12. V zázname dodávateľa vyberte **Všeobecné** > **Nastaviť** > **Medzipodniková**.
     13. Na karte **Obchodný vzťah** nastavte **Aktívny** na **Áno**.
     14. Nastavte pole **Zákaznícka spoločnosť** do **GBPM** a v **Záznam môjho účtu**, vyberte záznam zákazníka, ktorý ste vytvorili skôr v postupe.

3. **Nakonfigurujte medzipodnikové nastavenia v parametroch projektového manažmentu a účtovníctva**. 

    1. Vyberte právnickú osobu **USPM** a prejdite do **Projektový manažment a účtovníctvo** > **Nastaviť** > **Parametre projektového manažmentu a účtovníctva**.
    2. Na karte **Medzipodniková** vyberte kategóriu obstarávania tak, aby zodpovedala automaticky generovaným faktúram dodávateľa.
    3. V **predvolenej kategórii** vyberte **Medzipodnikové zdroje**.
    4. Vyberte právnickú osobu **GBPM** a prejdite do **Projektový manažment a účtovníctvo** > **Nastaviť** > **Parametre projektového manažmentu a účtovníctva**.
    5. Na karte **Medzipodniková** vyberte predvolenú kategóriu projektu pre každý typ transakcie. Kategórie projektov sa používajú na konfiguráciu dane, keď fakturovaná kategória v medzipodnikových transakciách existuje iba v požičiavajúcej právnickej osobe. Môžete si zvoliť hromadenie výnosov z medzipodnikových transakcií. Časové rozlíšenie nastane, keď sa transakcie zaúčtujú prostredníctvom denníka integrácie Project Operations v požičiavajúcej právnickej osobe. Denník sa vráti späť, keď sa zaúčtuje medzipodniková faktúra.
    6. V skupine **Pri požičiavaní zdrojov** vyberte **...** > **Nový**. 
    7. V mriežke vyberte z nasledujúcich informácií:

          - **Požičiavajúca si právnická osoba** = **USPM**
          - **Prírastok príjmu** = **Áno**
          - **Predvolená kategória časového rozvrhu** = **Predvolené – hodina**
          - **Predvolená kategória výdavkov** = **Predvolené – výdavok**

4. **Nastavte medzipodnikové nákladové a výnosové účty v nastavení zaúčtovania v účtovnej knihe**. Na medzipodnikový účet príjmov sa pripíše, keď sa fakturácia medzipodnikového zákazníka zaúčtuje u požičiavajúcej právnickej osoby. Z medzipodnikového účtu výdavkov sa odpíše, keď sa fakturácia zodpovedajúceho čakajúceho zákazníka zaúčtuje u požičiavajúcej si právnickej osoby. Tieto účty sú zriadené u príslušných právnických osobách. 
      
     1. V aplikácii Finance vyberte požičiavajúcu si právnickú osobu **USPM**. 
     2. Prejdite do **Projektové riadenie a účtovníctvo** > **Nastaviť** > **Zverejňovanie** > **Nastavenie zaúčtovania v účtovnej knihe**. 
     3. Na karte **Nákladové účty** v ponuke **Typ účtu účtovnej knihy** vyberte **Medzipodnikové náklady**. Vytvorte nový záznam s nasledujúcimi informáciami:
      
        - **Požičiavajúca právnická osoba** = **GBPM**
        - **Hlavný účet** = Vyberte hlavný účet pre medzipodnikové náklady. Toto nastavenie je povinné. Nastavenie sa používa pre medzipodnikové toky v službe Finance, ale nie v medzipodnikových tokoch týkajúcich sa projektu. Tento výber nemá žiadny následný vplyv. 
        
     4. Vyberte požičiavajúcu právnickú entitu **GBPM**. 
     5. Prejdite do **Projektové riadenie a účtovníctvo** > **Nastaviť** > **Zverejňovanie** > **Nastavenie zaúčtovania v účtovnej knihe**. 
     6. Na karte **Výnosové účty** v ponuke **Typ účtu účtovnej knihy** vyberte **Medzipodnikové výnosy**. Vytvorte nový záznam s nasledujúcimi informáciami:

        - **Požičiavajúca si právnická osoba** = **USPM**
        - **Hlavný účet** = Vyberte hlavný účet pre medzipodnikové výnosy. Toto nastavenie je povinné. Nastavenie sa používa pre medzipodnikové toky v službe Finance, ale nie v medzipodnikových tokoch týkajúcich sa projektu. Tento výber nemá žiadny následný vplyv. 

5. **Nastavte prevodové ceny pracovnej sily**. Medzipodnikové prevodové ceny sú konfigurované v časti Project Operations v Dataverse. Nakonfigurujte [nákladové sadzby za prácu](../pricing-costing/set-up-labor-cost-rate.md#transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity) a [sadzby fakturácie za prácu](../pricing-costing/set-up-labor-bill-rate.md#transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions) pre medzipodnikovú fakturáciu. Prevodové ceny nie sú podporované pri medzipodnikových výdavkových transakciách. Medzipodniková jednotková predajná cena bude vždy nastavená na rovnakú hodnotu ako jednotková cena zdroja.

      Náklady na zdroj vývojára v Contoso Robotics UK je 88 GBP za hodinu. Contoso Robotics UK bude fakturovať Contoso Robotics USA 120 USD za každú hodinu, kedy tento zdroj pracoval na projektoch v USA. Contoso Robotics USA bude fakturovať zákazníkovi Adventure Works 200 USD za prácu vykonanú zdrojom pre vývojára Contoso Robotics UK.

      1. V aplikácii Project Operations v Dataverse prejdite na **Predaj** > **Cenníky**. Vytvorte nový cenník nákladov s názvom **Sadzby nákladov Contoso Robotics UK.** 
      2. V cenníku obstarávacích cien vytvorte záznam s nasledujúcimi informáciami:
         - **Rola** = **Vývojár**
         - **Náklady** = **88 GBP**
      3. Prejdite do ponuky **Nastavenia** > **Organizačné jednotky** a pripojte tento cenník nákladov k organizačnej jednotke **Contoso Robotics UK**.
      4. Prejdite do **Predaj** > **Cenníky**. Vytvorte cenník nákladov s názvom **Sadzby nákladov Contoso Robotics USA.** 
      5. V cenníku obstarávacích cien vytvorte záznam s nasledujúcimi informáciami:
          - **Rola** = **Vývojár**
          - **Zdrojová spoločnosť** = **Contoso Robotics UK**
          - **Náklady** = **120 USD**
      6. Prejdite do ponuky **Nastavenia** > **Organizačné jednotky** a pripojte tento cenník nákladov **Contoso Robotics USA** k organizačnej jednotke **Contoso Robotics USA**.
      7. Prejdite do **Predaj** > **Cenníky**. Vytvorte predajný cenník s názvom **Fakturačné sadzby Adventure Works**. 
      8. V cenníku predajných cien vytvorte záznam s nasledujúcimi informáciami:
          - **Rola** = **Vývojár**
          - **Zdrojová spoločnosť** = **Contoso Robotics UK**
          - **Sadzba fakturácie** = **200 USD**
      9. Prejdite na **Predaj** > **Zmluvy o projekte** a pripojte cenník **Fakturačné sadzby spoločnosti Adventure Works** do cenníka projektu spoločnosti Adventure Works projektovej zmluvy.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
