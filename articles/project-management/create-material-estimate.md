---
title: Finančné odhady pre materiály na projektoch
description: Táto téma poskytuje informácie o definovaní alebo odhadovaní materiálov na základe projektu.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 98e3611b2b3948aab09a3eadeac7b95b893812e9
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788895"
---
# <a name="financial-estimates-for-materials-on-projects"></a>Finančné odhady pre materiály na projektoch

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations umožňuje projektovým manažérom definovať projektové náklady na materiál pre každý projekt alebo úlohu. Každý odhad materiálu môže byť spojený s konkrétnou projektovou úlohou. Výdavky sú kategorizované do rôznych kategórií výdavkov, ktoré sú definované na organizačnej úrovni. Ceny a kalkulácie pre každú kategóriu výdavkov sú definované v cenníku. 

Vykonaním nasledujúcich krokov zobrazíte, pridáte alebo odstránite odhad materiálu projektu.

1. Prejdite na **Projekty** a vyberte projekt, ktorý chcete aktualizovať.
2. Na karte **Odhady materiálu** sa zobrazí zoznam odhadov materiálov projektu.
3. Vyberte **Nový odhad materiálu** na vytvorenie nového odhadu materiálu. Alebo vyberte odhad materiálu, ktorý chcete odstrániť, a potom vyberte **Odstrániť odhad materiálu**.

Nasledujúca tabuľka poskytuje informácie o poliach na riadku **Odhad materiálu** na projekte. 

| **Pole** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- |
| Úloha | Zoznam úloh v projekte. Patria sem súhrnné úlohy a úlohy listových uzlov. | Keď vyberiete úlohu pre riadok odhadu materiálu, ovplyvnia sa odhadované náklady na materiál a odhadovaný predaj materiálu pre úlohu. Ak je toto pole prázdne, odhad materiálu sa sleduje a sumarizuje iba na úrovni projektu. |
| Vyberte produkt |  Môžete zvoliť, či riadok odhadu platí pre existujúci (katalógový) alebo pridávaný produkt. | Toto pole určuje, či vyberáte produkt z katalógu alebo či ide o pridávaný produkt. |
| Produkt | ID produktu z katalógu produktov. Po výbere ID produktu sa hodnota v poli **Vyberte Produkt** automaticky aktualizuje na **Existujúci produkt**. ID sa používa na načítanie nákladových a predajných cien z cenníka. | Toto pole nemá žiadny následný dopad. |
| Opis pridaného produktu | Textové pole na napísanie do názvu produktu. Toto pole by sa malo použiť, keď je vybraná možnosť **Pridaný** v poli **Vyberte produkt**.| Toto pole nemá žiadny následný dopad. |
| Počiatočný dátum | Predpovedaný dátum, kedy sa predpokladá použitie materiálu. | Toto pole nemá žiadny následný dopad. |
| Jednotková skupina | Predvolená hodnota v tomto poli pochádza z predvolenej jednotkovej skupiny pre katalógový produkt. Toto pole môžete aktualizovať, aby ste vybrali inú jednotkovú skupinu. | Toto pole nemá žiadny následný dopad. |
| Jednotka | Hodnota v tomto poli pochádza z predvolenej jednotky vybraného produktu. Toto pole môžete aktualizovať, aby ste vybrali inú jednotku. | Výsledkom zmeny jednotky je iná predvolená jednotková cena a náklady. |
| Počet | Odhadované množstvo produktu, ktoré sa použije v projekte. | Toto pole nemá žiadny následný dopad. |
| Jednotkové náklady | Jednotkové náklady na vybratý produkt a kombinácia jednotiek, ako sú stanovené v príslušnom cenníku nákladov. | Jednotkové náklady sa vždy zobrazujú v mene nákladov projektu. Ak v cenníku nie sú jednotkové náklady pre kombináciu produktu a jednotky, jednotkové náklady sa predvolene nastavia na 0,00. |
| Jednotková cena | Cena vybratého produktu a kombinácia jednotiek, ako sú stanovené v príslušnom predajnom cenníku. | Jednotková cena sa vždy zobrazuje v mene predajov projektu. Ak v cenníku nie je nastavená jednotková cena pre kombináciu produktu a jednotky, jednotková cena sa predvolene nastaví na 0,00.|
| Celkové náklady | Suma nákladov, ktorá sa počíta ako množstvo \* jednotkové náklady.| Suma nákladov sa vždy zobrazuje v mene nákladov projektu. |
| Celkový predaj | Suma predajov, ktorá sa počíta ako množstvo \* jednotková cena. | Suma predajov sa vždy zobrazuje v mene predajov projektu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
