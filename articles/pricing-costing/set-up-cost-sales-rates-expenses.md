---
title: Nastavenie nákladových a predajných sadzieb pre výdavky
description: Táto téma poskytuje informácie o tom, ako nastaviť cenu a sadzby predaja pre kategórie transakcie a výdavkov.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ee52daae18c5f9f0b630e54359021fffe1759274
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274927"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Nastavenie nákladových a predajných sadzieb pre výdavky

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V kategórii môžete nastaviť nákladové a predajné ceny pre kategórie transakcií v rámci Dynamics 365 Project Operations. Pretože náklady a predajné ceny sú určené pre výdavky, musí byť každá kategória transakcií, ktorá ich zahŕňa, tiež nastavená ako kategória výdavkov. Toto nastavenie zaisťuje presnosť následných funkcií. Cena a predajné ceny pre transakčné kategórie môžu byť uvedené iba v jednej mene, ktorou musí byť mena v hlavičke cenníka.

Ak chcete nastaviť ceny a sadzby predaja pre kategórie transakcií, postupujte takto. 

1. Vytvorte cenník na základe hlavičky cenníka. 
2. V položke **Ceny kategórií**, v ponuke vedľajšej mriežky, vyberte **+ Cena novej kategórie**. 
3. Na stránke **Rýchle vytvorenie** zadajte kategóriu transakcie a jednotku, pre ktorú vytvárate novú cenu.

V nasledujúcej tabuľke sú uvedené polia na karte **Všeobecné** a na stránke **Rýchle vytvorenie** cenového riadku kategórie, na ktorú by ste mali pamätať pri vytváraní cien kategórie v predajnom alebo nákladovom cenníku.

| Pole | Miesto | Popis | Nadväzujúci vplyv |
| --- | --- | --- | --- |
| Kategória transakcie | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Vyberte kategóriu transakcií, pre ktorú vytvárate predajnú alebo nákladovú cenu. | Kategória transakcie pri prichádzajúcom odhade alebo skutočná hodnota výdavkov bude porovnaná s týmto riadkom, aby sa štandardne nastavili sadzbu nákladov alebo predajov pre kategóriu transakcie. |
| Plán jednotky | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Jednotkový plán je predvolený z jednotkového plánu transakčnej kategórie. | Toto pole nemá žiadny následný dopad. |
| Jednotka | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Vyberte jednotku, pre ktorú sa sadzby nastavujú. | Jednotka na vstupnom odhade alebo skutočná je porovnaná s jednotkou na tomto riadku, aby sa štandardne nastavila miera na odhad nákladov alebo skutočné náklady. |
| Spôsob určenia ceny | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Možné hodnoty pre pole **Spôsob určenia ceny** sú **Cena za jednotku**, **V rámci nákladov** a **Prirážka nad rámec nákladov**. | Počas nastavenia ceny vyberte možnosť **Cena za jednotku**, čím sa uzamkne pole **Percento** v kategórii cena. Po zvolení možnosti **V rámci nákladov** sa polia **Cena** a **Percento** uzamknú v predajnom cenníku. Výberom možnosti **Prirážka nad rámec nákladov** sa uzamkne pole **Cena** v predajnom cenníku. Na prichádzajúcom skutočnom riadku pre výdavky výsledkom metódy oceňovania **V rámci nákladov** alebo **Prirážka nad rámec nákladov** je, že príslušnej nevyfakturovanej predajnej línii je priradená cena, ktorá sa rovná cene skutočnej ceny alebo sa počíta ako prirážka k cene. |
| Cena | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Nastavte jednotkovú sadzbu pre kategóriu transakcie a kombináciu jednotiek. Napríklad miera najazdených kilometrov je 10 USD na míľu a 8 USD na kilometer. | Sadzba za míľu je sadzba nákladov, ktorá predvolene zodpovedá jednotkovej cene alebo nákladom na prichádzajúci odhad alebo skutočný riadok pre triedu transakcie výdavkov.|
| Percento | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Nastavte percento nad nákladmi pre kategóriu transakcie a kombináciu jednotiek. Napríklad sadzba predaja leteniek by mala byť zvýšená o 10 percent nad cenu vzniknutých výdavkov na letenky. | Toto percento nad rámec nákladov platí pre predajné cenníky len vtedy, ak je zvolená možnosť oceňovania **Prirážka nad rámec nákladov**. |
| Mena | Karta **Všeobecné** a stránky **Rýchle vytvorenie** | Táto hodnota predvolene pochádza z meny v hlavičke cenníka obstarávacej ceny. V prípade cien v kategórii transakcií nemožno menu prepísať. | Táto mena predvolene zodpovedá jednotkovým cenám na prichádzajúci skutočný riadok pre triedu transakcie výdavkov pre náklady a predaj. |

## <a name="pricing-methods-for-expenses"></a>Metódy oceňovania výdavkov

Keď nastavujete ceny kategórií, ktoré sú relevantné iba v súvislosti s oceňovaním nákladov, môžete použiť jednu z nasledujúcich troch metód oceňovania:

- **Jednotková cena**
- **V rámci nákladov**
- **Prirážka nad rámec nákladov**

### <a name="price-per-unit"></a>Cena za jednotku
Ak je táto cenová metóda vybraná v cenovom riadku kategórie, ktorý je prepojený s cenníkom predajnej ceny, predvolená cena pre kombináciu kategórie a jednotky je v odhade aj v skutočnej hodnote. Odhad odkazuje na riadky odhadu projektu pre náklady, podrobne na riadok cenovej ponuky a podrobne na riadok zmluvy pre výdavky.

### <a name="at-cost"></a>V rámci nákladov
Ak je táto cenová metóda vybraná v cenovom riadku kategórie, ktorý je prepojený s cenníkom predajnej ceny, predvolená cena pre kombináciu kategórie a jednotky je výlučne aj v skutočnej hodnote. Napríklad nevyfakturované skutočné predaje pre triedu nákladových transakcií. Jednotková cena je stanovená na skutočný nevyfakturovaný predaj z jednotkovej ceny na skutočnú cenu daného výdavku. Predvolené nastavenie ceny na základe nákladov sa nevykonáva na základe odhadov výdavkov projektu alebo podrobností riadka ponuky a riadka zmluvy na strane výdavkov.

### <a name="markup-over-cost"></a>Prirážka nad rámec nákladov
Ak je táto cenová metóda vybraná v cenovom riadku kategórie, ktorý je prepojený s cenníkom predajnej ceny, predvolená cena pre kombináciu kategórie a jednotky je výlučne aj v skutočnej hodnote. Napríklad nevyfakturované skutočné predaje pre triedu nákladových transakcií. Táto jednotková cena je nastavená na skutočný nevyfakturovaný predaj na vypočítanú hodnotu z jednotkovej ceny na skutočnom náklade pre daný výdavok po uplatnení definovaného percenta prirážky. Predvolené nastavenie ceny na základe nákladov sa nevykonáva na základe odhadov výdavkov projektu alebo podrobností riadka ponuky a riadka zmluvy na strane výdavkov.


[!INCLUDE[footer-include](../includes/footer-banner.md)]