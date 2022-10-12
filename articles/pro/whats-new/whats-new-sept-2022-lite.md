---
title: Čo je nové September 2022 – Nasadenie Project Operations lite
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft zo septembra 2022 Dynamics 365 Project Operations lite nasadenie.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621379"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Čo je nové September 2022 – Nasadenie Project Operations lite

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.46.0.60

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

| Oblasť funkcií | Názov funkcie | Ďalšie informácie |
| --- | --- | --- |
| Správa príležitostí | **Revízia a aktivácia cenových ponúk**<br>Project Operations prináša plnú podporu procesu predaja. Cenové ponuky projektov je možné aktivovať, aby predstavovali stav, v ktorom je ponuka len na čítanie a prebieha jej kontrola. Aktivované ponuky je možné revidovať, aby sa vytvorili nové ponuky, ktoré majú zvýšené číslo revízie. Aktivované projektové ponuky alebo revízie cenových ponúk možno uzavrieť ako vyhraté alebo prehraté. | [Aktivácia a revízia projektovej cenovej ponuky](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturácia a tvorba cien | **Neplatenie ceny agnostického časového pásma**<br>Projektové operácie zaviedli koncept agnostického dátumu časového pásma na všetkých skutočných projektoch. Nové pole, **Dátum transakcie**, je teraz k dispozícii v riadkoch denníka a aktuálnych údajoch a bude sa používať na uloženie dátumu transakcie, ale bez konverzie tohto dátumu na koordinovaný svetový čas. Tento dátum sa použije pre následné procesy, ako je nedodržanie ceny a vytvorenie faktúry. | <p>[Stanovte nákladové sadzby pre odhady a skutočné skutočnosti založené na projekte](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Stanovte predajné ceny pre projektové odhady a skutočné skutočnosti](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Fakturácia a tvorba cien | **Prepisy cien platné k dátumu v projektových operáciách**<br>Prepisy cien platné k dátumu poskytujú spôsob, ako prepísať alebo zmeniť konkrétne ceny v cenníku. | [Prepisy cien platné od dátumu](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Čas a výdavky | **Globálny schvaľovateľ**<br>Táto funkcia umožňuje nezávislého dodávateľa softvéru (ISV) a centralizované schvaľovanie bez ohľadu na stav projektu alebo člena tímu v projekte. | [Zabezpečenie a schválenia](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Aktualizácie kvality

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2754422 | Odhady materiálu a nákladov neplynú do Dynamics 365 Finance, keď sa projekty skopírujú Dataverse. |
| Čas a výdavky | 2787409 | Neplatný schvaľovateľ môže schváliť neprojektový časový záznam. |
| Správa príležitostí | 2788907 | Aktualizované chybové hlásenie o overení jedinečnosti pre riadky objednávky, ktoré obsahujú príznaky. |
| Čas a výdavky | 2842253 | Spracovanie nulovej výnimky na schválenie času. |
| Fakturácia a tvorba cien | 2844181 | Neúspech pri získaní ID korelácie blokuje vytvorenie faktúry. |
| Fakturácia a tvorba cien | 2876628 | QLD, CLD – Rozlíšenie odhadovaného cenníka by malo používať staršie polia rozsahu dátumov v cenníku. |
| Subdodávky | 2893222 | Ak nie je špecifikovaná žiadna rola pre subdodávateľskú líniu, malo by byť možné vybrať túto líniu u člena tímu pre akúkoľvek rolu. |
