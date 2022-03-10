---
title: Prehľad medzipodnikovej fakturácie
description: Táto téma poskytuje informácie a príklady medzipodnikovej fakturácie pre projekty.
author: sigitac
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: c343c5bf525574e496036793cd4e131394e8b1b471153147a66cfebe1acf3fce
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005410"
---
# <a name="intercompany-invoicing-overview"></a>Prehľad medzipodnikovej fakturácie

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Vaša organizácia môže mať viac divízií, dcérskych spoločností a ďalších právnych subjektov, ktoré si navzájom prenášajú produkty a služby na účely projektov. Právnická osoba, ktorá poskytuje službu alebo produkt, sa nazýva *požičiavajúca právnická osoba*. Právnická osoba, ktorá prijíma službu alebo produkt, sa nazýva *požičiavajúca si právnická osoba*.

Nasledujúci obrázok znázorňuje typický scenár, keď dva právne subjekty, Contoso Robotics USA (požičiavajúca si právnická osoba) a Contoso Robotics UK (požičiavajúca právnická osoba) zdieľajú zdroje na realizáciu projektu pre zákazníka, spoločnosť Adventure Works. Pre tento scenár je Contoso Robotics USA zmluvne poverená dodaním diela spoločnosti Adventure Works.

![Medzipodniková fakturácia.](./media/IntercompanyScenario.png) 

Dynamics 365 Project Operations používa na spracovanie medzipodnikových transakcií nasledujúci postup:

1. Zdroje z požičiavajúcej právnickej osoby zaznamenávajú medzipodnikové časové alebo nákladové transakcie podľa času rezervácie a výdavkov voči projektom u požičiavajúcej si právnickej osoby.
2. Časové a nákladové výdavky sa zaznamenávajú u požičiavajúcej spoločnosti pomocou cenníka jednotkových obstarávacích cien požičiavajúcej si spoločnosti.
3. Medzipodnikové nefakturované obchodné transakcie sa zaznamenávajú u požičiavajúcej spoločnosti pomocou cenníka jednotkových obstarávacích cien požičiavajúcej si spoločnosti.
4. Nevyfakturované výnosy sa zaznamenávajú v požičiavajúcej si spoločnosti pomocou predajného cenníka projektovej zmluvy. Zákazníkovi je možné fakturovať, keď sa zaznamenajú nevyfakturované výnosy. Zákazník nemusí čakať, kým sa dokončí spracovanie medzipodnikovej faktúry.
5. Medzipodnikové zákaznícke faktúry sa v požičiavajúcej spoločnosti vytvárajú pravidelne. Faktúry sa vytvárajú ručne alebo pomocou periodického automatizovaného procesu. Pre každú požičiavajúcu si právnickú osobu je možné vytvoriť jednu faktúru alebo je možné vytvoriť samostatné faktúry podľa projektu.
6. Keď je zaúčtovaná medzipodniková faktúra zákazníka u požičiavajúcej právnickej osoby, zodpovedajúca nevybavená faktúra dodávateľa sa vytvorí u požičiavajúcej si právnickej osoby. Po zaúčtovaní faktúry sa náklady na čakajúcej faktúre dodávateľa zaznamenajú do vedľajšej účtovnej knihy projektu.

Nasledujúci diagram ilustruje medzipodnikovú fakturáciu, pretože sa týka účtovných udalostí a očakávaných zaúčtovaní do hlavnej účtovnej knihy.

![Medzipodnikový postup.](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a>Ďalšie zdroje

- [Konfigurácia medzipodnikovej fakturácie](configure-intercompany-invoicing.md)
- [Záznam medzipodnikových transakcií](create-intercompany-transactions.md)
- [Vytvorenie medzipodnikových faktúr zákazníkov a dodávateľov](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]