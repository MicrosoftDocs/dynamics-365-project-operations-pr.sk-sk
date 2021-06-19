---
title: Finančné odhady pre výdavky na projekty
description: Táto téma poskytuje informácie o definovaní alebo odhade výdavkov na základe projektu.
author: rumant
ms.date: 03/19/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 18d8568fae35fc251d9cf48d900b8a436e2e4500
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014180"
---
# <a name="financial-estimates-for-expenses-on-projects"></a>Finančné odhady pre výdavky na projekty
_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations umožňuje projektovým manažérom definovať projektové výdavky pre každý projekt alebo úlohu. Každá položka výdavku môže byť spojená s konkrétnou projektovou úlohou. Výdavky sú kategorizované do rôznych kategórií výdavkov, ktoré sú definované na organizačnej úrovni. Ceny a kalkulácie pre každú kategóriu výdavkov sú definované v cenníku. 

Ak chcete zobraziť, pridať alebo odstrániť projektové výdavky, postupujte podľa nasledujúcich krokov.

1. Prejdite do časti **Projekty** a vyberte projekt, na ktorom chcete pracovať.
2. Vyberte kartu **Odhady projektu** a prezrite si zoznam projektových výdavkov.
3. Vyberte **Nový výdavok** na pridanie výdavku. Alebo vyberte výdavok, ktorý chcete odstrániť, a potom vyberte **Odstrániť výdavok**.

Nasledujúca tabuľka poskytuje informácie o poliach na riadku **Odhad výdavkov** v projekte. 

| **Pole** | **Opis** | **Nadväzujúci vplyv** |
| --- | --- | --- |
| Úloha | Zoznam úloh v projekte. Patria sem súhrnné úlohy a úlohy listových uzlov. | Výber úlohy pre riadok odhadu výdavkov ovplyvní odhadované výdavkové náklady a odhadované predajné výdavky na úlohu. Ak je toto pole prázdne, odhad výdavkov sa sleduje a sumarizuje iba na úrovni projektu. |
| Kategória | Zoznam kategórií transakcií, ktoré majú prepojené kategórie výdavkov v aplikácii. | Výber kategórie vedie k stanoveniu cien a kalkulácií na riadku odhadu výdavkov. |
| Počiatočný dátum | Predpokladaný dátum, kedy dôjde k výdavku. | Toto pole nemá žiadny následný dopad. |
| Jednotková skupina | Predvolená hodnota v tomto poli pochádza z jednotkovej skupiny, ktorá je nastavená ako predvolená vybranú kategóriu. Toto pole môžete aktualizovať, aby ste vybrali inú jednotkovú skupinu. | Toto pole nemá žiadny následný dopad. |
| Jednotka | Hodnota v tomto poli sa predvolene nastaví na predvolenú jednotku vybranej kategórie. Toto pole môžete aktualizovať, aby ste vybrali inú jednotku. | Výsledkom zmeny jednotky je iná predvolená jednotková cena a náklady. |
| Počet | Množstvo predpokladaných výdavkov, ktoré vzniknú. | Toto pole nemá žiadny následný dopad. |
| Jednotkové náklady | Náklady kombinácie vybranej kategórie a jednotky, ako sú stanovené v príslušnom cenníku nákladov. | Jednotkové náklady sa vždy zobrazujú v mene nákladov projektu. |
| Jednotková cena | Cena vybranej kombinácia kategórie a jednotky, ako je stanovená v príslušnom predajnom cenníku. | Jednotková cena sa vždy zobrazuje v mene predajov projektu. |
| Celkové náklady | Suma nákladov, ktorá sa počíta ako množstvo \* jednotkové náklady.| Suma nákladov sa vždy zobrazuje v mene nákladov projektu. |
| Celkový predaj | Suma predajov, ktorá sa počíta ako množstvo \* jednotková cena. | Suma predajov sa vždy zobrazuje v mene predajov projektu. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]
