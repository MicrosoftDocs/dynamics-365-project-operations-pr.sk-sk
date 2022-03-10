---
title: Nastavenie nákladových sadzieb za prácu – čiastočné
description: Táto téma poskytuje informácie o tom, ako nastaviť sadzby nákladov pre prácu v Project Operations.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c7b00d018f20dd79d5a6f8444a25ed4768cc6b220023fd08967eb917e2f4f2b6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006130"
---
# <a name="set-up-labor-cost-rates---lite"></a>Nastavenie nákladových sadzieb za prácu – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Každý cenník obsahuje množinu pracovných cien (rolové ceny), ktoré zodpovedajú obsahu a dátumu účinnosti cenníka.

1. Vytvorte cenník a na karte **Cena roly** vo vedľajšej mriežke vyberte **Nová rola**.
2. Na stránke **Rýchle vytvorenie** vyberte rolovú a organizačnú jednotku.
3. Do povinných polí zadajte všetky ďalšie informácie.

Nasledujúca tabuľka obsahuje niektoré z polí, ktoré sú dôležité pri vytváraní sadzieb ceny za prácu v cenníku nákladov.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| Rola | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Vyberte si rolu, na ktorú sa sadzba za prácu vzťahuje. | Rola pri prichádzajúcom odhade alebo skutočná bude porovnaná s týmto riadkom, aby sa štandardne nastavili náklady na rolu. |
| Zdrojová jednotka | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Vyberte organizačnú jednotku alebo divíziu spoločnosti, z ktorej sa bude táto rola využívať. Napríklad vývojár z divízie Robotics spoločnosti Fabrikam India alebo vývojár z divízie Software spoločnosti Fabrikam USA. | Zdrojová jednotka pri prichádzajúcom odhade alebo skutočná bude porovnaná s týmto riadkom, aby sa štandardne nastavili náklady na rolu. |
| Cena | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Nastavte nákladovú sadzbu pre kombináciu rol, zdrojovej spoločnosti a zdrojovej jednotky. Napríklad vývojár z Fabrikam India stojí 1000 INR alebo vývojár z Fabrikam USA stojí 150 USD. | Cena je sadzba nákladov, ktorá predvolene zodpovedá jednotkovým nákladom na prichádzajúci odhad alebo skutočný riadok pre triedu transakcie **Čas**. |
| Mena | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Hodnota meny štandardne pochádza z meny v hlavičke cenníka nákladov, ale dá sa prepísať. Napríklad vývojár zo spoločnosti Fabrikam India stojí 1 000 INR. Vývojár zo spoločnosti Fabrikam USA stojí 150 USD. | Táto mena predvolene zodpovedá jednotkovým nákladom na prichádzajúci skutočný riadok pre triedu transakcie **Čas**. Pri odhade projektu sa hodnota meny prevedie na menu projektu a zobrazí sa v časovo odstupňovanom zobrazení odhadu. |
| Plán jednotky | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Jednotkový rozvrh je predvolene nastavený na Čas a nie je možné ho zmeniť v entite ceny rolí, pretože sa v ňom používajú expresné sadzby podľa časových jednotiek. | Nemá to žiadny vplyv na následné prvky. |
| Jednotka | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Hodnota predvolene pochádza z poľa **Jednotka času** v hlavičke cenníka obstarávacej ceny. Hodnota môže byť prepísaná. Napríklad vývojár zo spoločnosti Fabrikam India stojí 1 000 INR na **indický pracovný deň**. Vývojár zo spoločnosti Fabrikam USA stojí 150 USD na **pracovný deň v USA**. | Systém používa systém jednotiek a prepočet na základné jednotky na výpočet jednotkových nákladov na výpočet predvolenej ceny za jednotku na prichádzajúcom odhade alebo skutočnom riadku. Napríklad odhad na 10 **pracovných dní v Indii** za prácu pre vývojára z Indie a jednotka **Pracovný deň v Indii** je definovaná ako 10 hodín. Pri výpočte nákladov na tento riadok odhadu aplikácia vypočíta jednotkové náklady z odhadu ako: 1 000 INR/10 hodín = 100 INR za hodinu, ktoré sa prevedú na USD a zobrazia sa ako jednotkové náklady na stránke **Odhady projektu**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Transferové ceny a náklady na zdroje mimo vašej divízie alebo právnickej osoby

Projektové spoločnosti bežne využívajú na prácu na projektoch zamestnancov z rôznych divízií spoločnosti alebo právnických osôb. Projekt môže vykonávať jedna právnická osoba, ale zamestnanci alebo konzultanti, ktorí na projekte pracujú, môžu pochádzať od rovnakej právnickej osoby alebo od inej entity, prípadne môže ísť o kombináciu oboch. V rámci Dynamics 365 Project Operations je právnickou osobou, ktorá je vlastníkom dodávky projektu, **Vlastniaca spoločnosť** a divíziou, ktorá vlastní dodávku, je **Zmluvná jednotka**. Ďalšími právnickými osobami, ktoré poskytujú zdroje, sú **Spoločnosti zabezpečujúce zdroje** a divízie, ktoré poskytujú zdroje, sú **Zdrojové jednotky**. Vo väčšine krajín sa od spoločností vyžaduje, aby zabezpečili, že právnická osoba alebo divízia, ktorá financuje zdroje, účtuje od vlastniacej spoločnosti a zmluvnej jednotky za použitie zdrojov.

Napríklad spoločnosť Fabrikam musí zabezpečiť, aby spoločnosť Fabrikam India-Robotics mala dohodnutý cenník so spoločnosťami Fabrikam US-Robotics alebo Fabrikam UK-Robotics.

Vývojár zo spoločnosti Fabrikam India-Robotic účtuje poplatky za $ 100, keď ich požičal spoločnosti Fabrikam US-Robotics, a $150, keď ich požičal spoločnosti Fabrikam U-Robotics.

### <a name="set-up-costs-for-outside-resources"></a>Nastavte náklady na externé zdroje

1. Vytvorte cenník nákladov s názvom,*Sadzby nákladov spoločnosti Fabrikam US-Robotics* a nastavte rozsah účinných dátumov.
2. V cenníku nákladov nastavte sadzby pomocou informácií z nasledujúcej tabuľky. 

| Rola | Spoločnosť zaisťujúca zdroje | Zdrojová jednotka | Nákladová sadzba |
| --- | --- | --- | --- |
| Vývojár | Fabrikam India | Fabrikam India-Robotics | $100 |
| Vývojár | Fabrikam Philippines | Fabrikam Philippines-Robotics | $ 90 |
| Vývojár | Fabrikam US | Fabrikam US-Robotics | $ 150 |

3. Pripojte tento cenník nákladov k organizačnej jednotke Fabrikam US-Robotics.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Nastavte transferové ceny pre zdroj v príslušnej mene 

V rámci Project Operations je možné stanovovať ceny zdrojov v akejkoľvek mene. Mena je predvolene nastavená na hodnotu uvedenú v hlavičke cenníka, ale je možné ju zmeniť.

Pomocou príkladu na nastavenie ceny prevodu je možné informácie zmeniť na:

Spoločnosť Fabrikam musí zabezpečiť, aby spoločnosť Fabrikam India-Robotics mala dohodnutú cenu práce so spoločnosťami Fabrikam US-Robotics alebo Fabrikam UK-Robotics.

Vývojár zo spoločnosti Fabrikam India-Robotics si účtuje poplatok 5000 INR, pri poskytnutí spoločnosti Fabrikam US-Robotics, a 5500 INR pri poskytnutí spoločnosti Fabrikam UK-Robotics.

V cenníku nákladov pre spoločnosť Fabrikam US-Robotics možno sadzby nákladov vyjadriť ako:

| Rola | Spoločnosť zaisťujúca zdroje | Náklady |
| --- | --- | --- |
| Vývojár | Fabrikam India | 5000 INR |
| Vývojár | Fabrikam US | 115 USD |

V cenníku nákladov pre spoločnosť Fabrikam UK-Robotics možno sadzby nákladov vyjadriť ako:

| Rola | Spoločnosť zaisťujúca zdroje | Náklady |
| --- | --- | --- |
| Vývojár | Fabrikam India | 5500 INR |
| Vývojár | Fabrikam UK | 115 GBP |

Cenník nákladov môže poskytovať sadzby práce vo viacerých menách. Pri generovaní odhadu nákladov na projekt Project Operations prevedie tieto sadzby nákladov na menu projektu a zobrazí ich používateľovi. Keď je časový záznam schválený a je vytvorená skutočná cena, skutočná cena sa nacení v mene zodpovedajúceho cenového riadku role v cenníku nákladov. Skutočné náklady za čas na jednom projekte je možné zaznamenať vo viacerých menách. Pri zhrnutí alebo zosumarizovaní skutočných nákladov práce na úrovni projektu, Project Operations prevedie všetky sumy nákladov práce do meny projektu, ktorú môže používateľ zobraziť.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]