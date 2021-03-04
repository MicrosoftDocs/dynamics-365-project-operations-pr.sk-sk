---
title: Nastavenie sadzieb fakturácie za prácu
description: Táto téma poskytuje informácie o spôsobe nastavení sadzieb fakturácie práce v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 501458510efca6434a51577aacd1f09d1a4faa25
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180731"
---
# <a name="set-up-labor-bill-rates"></a>Nastavenie sadzieb fakturácie za prácu

**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

Každý cenník obsahuje množinu pracovných cien alebo sadzieb za prácu, ktoré sú platné pre kontext a dátum platnosti uvedený v hlavičke cenníka. Fakturačné sadzby za čas v Dynamics 365 Project Operations je možné nastaviť iba v jednej mene, ktorou je mena v hlavičke cenníka.

1. Ak chcete nastaviť sadzby fakturácie práce pre predajný cenník, vytvorte cenník na základe hlavičky cenníka. 
2. Na karte **Ceny rol** vo vedľajšej mriežke stlačte možnosť **+ Pridať cenu roly**. 
3. Na table **Rýchle vytvorenie** zadajte kombináciu rol a organizačných jednotiek, pre ktoré musíte nastaviť fakturačnú sadzbu.

   V nasledujúcej tabuľke sú uvedené polia na karte **Všeobecné** a na table **Rýchle vytvorenie** cenového riadku roly, na ktorú musíte pamätať pri vytváraní cien role v predajnom cenníku:

    | Pole | Miesto | Popis | Nadväzujúci vplyv |
    | --- | --- | --- | --- |
    | Rola | Karta **Všeobecné** a tabla **Rýchle vytvorenie** | Vyberte rolu, pre ktorú nastavujete fakturačnú sadzbu. | Rola pri prichádzajúcom odhade alebo skutočná hodnota bude porovnaná s týmto riadkom, aby sa štandardne nastavila sadzba fakturácie. |
    | Spoločnosť zaisťujúca zdroje | Karta **Všeobecné** a tabla **Rýchle vytvorenie** | Zvoľte si spoločnosť alebo právnickú osobu, odkiaľ rola pochádza. Napríklad vývojár z Fabrikam India alebo vývojár z Fabrikam USA. | Zdrojová spoločnosť pri prichádzajúcom odhade alebo skutočná bude porovnaná s týmto riadkom, aby sa štandardne nastavili fakturačnú sadzbu. |
    | Zdrojová jednotka | Karta **Všeobecné** a tabla **Rýchle vytvorenie** | Vyberte organizačnú jednotku alebo divíziu spoločnosti, z ktorej rola pochádza. Napríklad vývojár z divízie Robotics spoločnosti Fabrikam India alebo vývojár z divízie Software spoločnosti Fabrikam USA. | Zdrojová jednotka pri prichádzajúcom odhade alebo skutočná bude porovnaná s týmto riadkom, aby sa štandardne nastavili fakturačnú sadzbu. |
    | Cena | Karta **Všeobecné** a tabla **Rýchle vytvorenie** | Nastavte fakturačnú sadzbu pre kombináciu rol, zdrojovej spoločnosti a zdrojovej jednotky. Napríklad vývojár zo spoločnosti Fabrikam India má fakturačnú sadzbu 100 USD alebo vývojár zo spoločnosti Fabrikam USA má fakturačnú sadzbu 150 USD. | Táto cena je predvolenou fakturačnou sadzbou, ktorá predvolene zodpovedá jednotkovým cenám na prichádzajúci odhad alebo skutočný riadok pre triedu transakcie Čas. |
    | Mena | Karta **Všeobecné** a tabla **Rýchle vytvorenie**| Predvolene hodnota meny pochádza z meny v hlavičke predajného cenníka. V predajnom cenníku nemožno menu prepísať. | Táto mena je predvolenou menou jednotkovým cenám na prichádzajúci skutočný riadok pre triedu transakcie času pre predaj. |
    | Plán jednotky | Karta **Všeobecné** a tabla **Rýchle vytvorenie** | Tento jednotkový rozvrh je predvolene nastavený na Čas a nie je možné ho zmeniť v entite ceny rolí, pretože sa v ňom používajú expresné sadzby podľa časových jednotiek. | Toto pole nemá žiadny následný dopad. |
    | Jednotka | Karta **Všeobecné** a tabla **Rýchle vytvorenie** | Hodnota jednotky pochádza z poľa **Jednotka času** v hlavičke cenníka obstarávacej ceny. Hodnotu však možno prepísať. Napríklad vývojár zo spoločnosti Fabrikam India má fakturačnú sadzbu 1000 USD na **indický pracovný deň**. Vývojár zo spoločnosti Fabrikam USA má fakturačnú sadzbu 1500 USD za **pracovný deň v USA**. | Systém používa systém jednotiek a prepočet na základné jednotky na výpočet jednotkových nákladov na výpočet predvolenej ceny za jednotku na prichádzajúcom odhade alebo skutočnom riadku. Napríklad odhad na 10 pracovných dní v Indii za prácu pre vývojára z Indie a jednotka **Pracovný deň v Indii** je definovaná ako 10 hodín. Pri stanovení ceny na tomto riadku odhadu aplikácia vypočíta jednotkovú cenu z odhadu ako 1000 USD/10 hodín = 100 USD za hodinu. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Transferové ceny alebo nastavenie fakturačných sadzieb pre zdroje z iných organizačných jednotiek alebo divízií 

Projektové spoločnosti často na prácu na projektoch využívajú zamestnancov z rôznych právnických osôb a rôznych divízií v rámci právnickej osoby. Projekty možno realizovať z istej právnickej osoby a divízie, kým zamestnanci alebo konzultanti pracujúci na projekte môžu pochádzať z rovnakej či odlišnej právnickej osoby či divízie. Projekt by mohol pozostávať aj z kombinácie ľudí z rôznych právnických osôb a divízií. V rámci Project Operations je právnickou osobou, ktorá vlastní dodávku projektu, **Vlastniaca spoločnosť** a divízia, ktorá vlastní dodávku, je **Zmluvná jednotka**. Ďalšími inými právnickými osobami, ktoré poskytujú zdroje, sú **Spoločnosti zabezpečujúce zdroje** a divízie, ktoré poskytujú zdroje, sú **Zdrojové jednotky**. Kvôli rozdielom v nákladoch na pracovnú silu v rôznych geografických oblastiach a na trhoch práce po celom svete sú fakturačné sadzby za prácu pre rôzne geografické oblasti tiež odlišné.

Napríklad vývojárovi z divízie Robotics spoločnosti Fabrikam India pracujúcej na projekte v USA je fakturovaná sadzba 100 USD za hodinu. Vývojárovi z divízie Robotics spoločnosti Fabrikam US, ktorý pracuje na projekte USA, je účtovaná sadzba 150 USD za hodinu. 

### <a name="example-set-up-a-bill-rate"></a>Príklad: Nastavte fakturačnú sadzbu 

1. Vytvorte predajný cenník s názvom *Sadzby fakturácie Fabrikam US* a nastavte účinnosť dátumu.
2. V predajnom cenníku zadajte nasledujúce informácie o sadzbe:

    | Rola | Spoločnosť zaisťujúca zdroje | Zdrojová jednotka | Sadzba fakturácie |
    | --- | --- | --- | --- |
    | Vývojár | Fabrikam India | Fabrikam India – Robotics | $100 |
    | Vývojár | Fabrikam Philippines | Fabrikam Philippines – Robotics | $ 90 |
    | Vývojár | Fabrikam US | Fabrikam US – Robotics | $ 150 |

3. Pripojte predajný cenník, **Sadzby fakturácie Fabrikam US** do cenníka projektu projektovej zmluvy alebo na určitý účet.


[!INCLUDE[footer-include](../includes/footer-banner.md)]