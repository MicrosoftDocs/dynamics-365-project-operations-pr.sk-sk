---
title: Definovanie politík výdavkov
description: Môžete definovať politiky výdavkov, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 863d1e44dad9fa0d2174cf77582a1d820988e92d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276097"
---
# <a name="define-expense-policies"></a>Definovanie politík výdavkov

_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

Môžete definovať politiky, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek.         
Implementácia politík výdavkov vám môže pomôcť efektívne riadiť výdavky.         

Napríklad môžete nastaviť politiku pre hotelové výdavky v New Yorku, kde sa uvádza, že náklady na noc nemôžu prekročiť 250 USD.       
Ak pracovník predloží výkaz výdavkov alebo cestovnú žiadanku, kde cena za izbu presahuje túto sumu, systém o tom informuje         
pracovníka, že bola prekročená suma výdavku určená politikou. Môžete nakonfigurovať správu, ktorú pracovník dostane, keď        
budete definovať politiku.      
        
Môžete definovať tri typy politík:         
        
- **Varovanie**: Umožňuje pracovníkovi predložiť výkaz výdavkov alebo cestovnú požiadavku, ale výdavok bude označený pre všetkých schvaľovateľov a         
  neskoršie hlásenie.        

- **Chyba**: Vyžaduje, aby pracovník pred predložením výkazu výdavkov alebo cestovnej žiadanky prehodnotil výdavky tak, aby boli v súlade s politikou.        
 
 - **Odôvodnenie**: Vyžaduje, aby pracovník alebo vedúci pracovník pred odoslaním výkazu výdavkov alebo cestovnej žiadanky uviedol zdôvodnenie prekročenia sumy definovanej politikou.        

## <a name="policy-tips"></a>Tipy týkajúce sa politiky
Tu je niekoľko návrhov, ktoré vám môžu pomôcť pri vytváraní nových politík pre riadenie výdavkov: 

- Politiky sú účinné od dátumu, čo znamená, že politika nenadobudne účinnosť, ak je vytvorené po dátume, keď došlo k výdavku. Napríklad dnes vytvoríte novú politiku, ktorý sa má vynucovať, s maximálnym výdavkom na jedlo vo výške 50 USD. Všetky existujúce výdavky zadané do včera sa nebudú kontrolovať z hľadiska tejto politiky.
- Pri vytváraní politiky pre kategóriu výdavkov, ktoré je možné rozpisovať, zvážte pridanie podmienky pre typ riadku výdavkov. Niektoré politiky, napríklad vyžadovanie účtenky, nemusia mať pre rozpísané riadky zmysel. V tejto situácii sa politika použije iba na riadok hlavičky alebo na riadok, ktorý nie je rozpísaný. 
- Politiky riadenia výdavkov sa štandardne vyhodnocujú voči zdrojovej entite. Pre medzipodnikové scenáre môžete nastaviť, aby sa politika namiesto toho vyhodnocovala voči cieľovej entite (entite, ktorá si požičiava). Ak chcete spúšťať politiky proti cieľovej entite, zapnite funkciu **Vyhodnocovať politiku výdavkov voči požičiavajúcej si právnickej entite** v pracovnom priestore **Správa funkcií**.

## <a name="when-to-evaluate-policies"></a>Kedy vyhodnocovať politiky

V parametroch riadenia výdavkov môžete zvoliť vyhodnotenie politík riadenia výdavkov pri uložení riadku alebo pri odoslaní výkazu výdavkov. Ak sa rozhodnete vyhodnocovať pri ukladaní riadka, používatelia budú mať skôr prehľad o tom, čo musia urobiť, aby mohli vyplniť výkaz výdavkov naraz. V opačnom prípade môžete oddialiť vyhodnotenie politiky a ušetriť čas overením na konci, počas odosielania do pracovného postupu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]