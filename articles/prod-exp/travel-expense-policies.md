---
title: Nastavenie politík výdavkov
description: Môžete stanoviť politiky výdavkov, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek v Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650113"
---
# <a name="set-up-expense-policies"></a>Nastavenie politík výdavkov

[!include [banner](../includes/banner.md)]

Môžete definovať politiky, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek.         
Implementácia politík výdavkov vám môže pomôcť efektívne riadiť výdavky.         

Napríklad môžete nastaviť politiku pre hotelové výdavky v New Yorku, kde sa uvádza, že náklady na noc nemôžu prekročiť 250 USD.       
Ak pracovník predloží výkaz výdavkov alebo cestovnú žiadanku, kde cena za izbu presahuje túto sumu, systém o tom informuje        
pracovníka, že bola prekročená suma výdavku určená politikou. Môžete nakonfigurovať správu, ktorú pracovník dostane, keď        
budete definovať politiku.      
        
Môžete definovať tri typy politík:         
        
- Varovanie – Umožňuje pracovníkovi predložiť výkaz výdavkov alebo cestovnú požiadavku, ale výdavok bude označený pre všetkých schvaľovateľov a        
  neskoršie hlásenie.        

- Chyba – Vyžaduje, aby pracovník pred predložením výkazu výdavkov alebo cestovnej žiadanky prehodnotil výdavky tak, aby boli v súlade s politikou.       
 
 - Odôvodnenie – Vyžaduje, aby pracovník alebo vedúci pracovník pred odoslaním výkazu výdavkov alebo cestovnej žiadanky uviedol zdôvodnenie prekročenia sumy definovanej politikou.        

## <a name="policy-tips"></a>Tipy týkajúce sa politiky
Tu je niekoľko návrhov, ktoré vám môžu pomôcť pri vytváraní nových politík pre riadenie výdavkov. 
* Politiky sú účinné od dátumu a politika nenadobudne účinnosť, ak je vytvorená po dátume, keď došlo k výdavku. Napríklad ak dnes vytvárate novú politiku na vynútenie maximálnych výdavkov na stravovanie vo výške $50, žiadne existujúce výdavky zadané od včera nebudú oproti týmto pravidlám skontrolované.
* Pri vytváraní politiky pre kategóriu výdavkov, ktoré je možné rozpisovať, zvážte pridanie podmienky pre typ riadku výdavkov. Niektoré zásady, napríklad vyžadovanie potvrdenia, nemusia mať zmysel pre riadky s položkami a mali by sa uplatňovať iba na riadok hlavičky alebo riadok bez položiek. 
* Politiky riadenia výdavkov sa štandardne vyhodnocujú voči zdrojovej entite. Pre medzipodnikové scenáre môžete nastaviť, aby sa politika namiesto toho vyhodnocovala voči cieľovej entite (entite, ktorá si požičiava). Ak chcete spúšťať politiky proti cieľovej entite, zapnite funkciu Vyhodnocovať politiku výdavkov voči požičiavajúcej si právnickej entite v pracovnom priestore **Správa funkcií**.

## <a name="when-to-evaluate-policies"></a>Kedy vyhodnocovať politiky

V parametroch riadenia výdavkov existuje možnosť buď zvoliť vyhodnotenie politík riadenia výdavkov pri uložení riadku, alebo pri odoslaní výkazu výdavkov. Ak sa rozhodnete vyhodnocovať pri ukladaní riadka, zaistí to, že používatelia budú mať skôr prehľad o tom, čo musia urobiť, aby mohli vyplniť výkaz výdavkov naraz. V opačnom prípade môžete oddialiť vyhodnotenie politiky a ušetriť čas, ak k overeniu dôjde na konci, počas odosielania do pracovného postupu.
