---
title: Čo je nové September 2022 – Nasadenie Project Operations lite
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní nasadenia Microsoft Dynamics 365 Project Operations lite zo septembra 2022.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634872"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Čo je nové September 2022 – Nasadenie Project Operations lite

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.46.0.60

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

| Oblasť funkcií | Názov funkcie | Ďalšie informácie |
| --- | --- | --- |
| Správa príležitostí | **Revízia a aktivácia cenových ponúk**<br>Project Operations prináša plnú podporu procesu predaja. Cenové ponuky projektov je možné aktivovať, aby predstavovali stav, v ktorom je ponuka len na čítanie a prebieha jej kontrola. Aktivované cenové ponuky je možné revidovať, aby sa vytvorili nové cenové ponuky, ktoré majú vyššie číslo revízie. Aktivované revízie cenových ponúk projektu je možné uzavrieť ako Získaná alebo Nevyužitá. | [Aktivácia a revízia projektovej cenovej ponuky](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturácia a tvorba cien | **Predvolená cena bez znalosti časového pásma**<br>Project Operations zaviedli koncept bez znalosti dátumu časového pásma pre všetky skutočné hodnoty projektov. Nové pole, **Dátum transakcie**, je teraz k dispozícii v záznamoch v účtovnom denníku a skutočných hodnotách a bude sa používať na uloženie dátumu transakcie, ale bez konverzie tohto dátumu na koordinovaný svetový čas. Tento dátum sa použije pre následné procesy, ako je nedodržanie ceny a vytvorenie faktúry. | <p>[Určenie nákladových sadzieb pre odhady a skutočné hodnoty založené na projektoch](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Určenie predajných cien pre odhady a skutočné hodnoty založené na projektoch](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Fakturácia a tvorba cien | **Prepisy cien s dátumom účinnosti v Project Operations**<br>Prepísanie cien s dátumom účinnosti poskytuje spôsob, ako prepísať alebo zmeniť konkrétne ceny v cenníku. | [Prepísania cien s dátumom účinnosti](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Čas a výdavky | **Globálny schvaľovateľ**<br>Táto funkcia povoľuje nezávislého dodávateľa softvéru (ISV) a centralizované schvaľovanie bez ohľadu na stav projektu alebo člena tímu v projekte. | [Zabezpečenie a schválenia](/dynamics365/project-operations/approvals/approvals-security) |
|Plánovanie a sledovanie projektu|**Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu** </br> </br>Rozhranie API na úpravu kontúr priradenia zdrojov umožňuje vývojárom programovo špecifikovať úsilie zadávateľa úlohy v akomkoľvek podporovanom rozsahu dátumov, aby bolo možné podrobnejšie plánovať časovo rozložené úsilie.|[Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2754422 | Odhady materiálu a výdavkov neprechádzajú do Dynamics 365 Finance, keď sa projekty skopírujú v Dataverse. |
| Čas a výdavky | 2787409 | Neplatný schvaľovateľ môže schváliť neprojektový časový záznam. |
| Správa príležitostí | 2788907 | Aktualizované chybové hlásenie o overení jedinečnosti pre riadky objednávky, ktoré obsahujú príznaky. |
| Čas a výdavky | 2842253 | Spracovanie nulovej výnimky na schválenie času. |
| Fakturácia a tvorba cien | 2844181 | Neúspech pri získaní ID korelácie blokuje vytvorenie faktúry. |
| Fakturácia a tvorba cien | 2876628 | QLD, CLD – Riešenie odhadovaného cenníka by malo používať staršie polia rozsahu dátumov v cenníku. |
| Subdodávateľské zmluvy | 2893222 | Ak nie je špecifikovaná žiadna rola pre riadok subdodávateľskej zmluvy, malo by byť možné vybrať tento riadok u člena tímu pre akúkoľvek rolu. |
