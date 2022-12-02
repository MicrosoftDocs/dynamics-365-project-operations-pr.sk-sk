---
title: Obchodné transakcie v aplikácii Project Operations
description: Tento článok poskytuje prehľad konceptu obchodných transakcií v Microsoft Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923299"
---
# <a name="business-transactions-in-project-operations"></a>Obchodné transakcie v aplikácii Project Operations

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_

V Microsoft Dynamics 365 Project Operations je *obchodná transakcia* abstraktný koncept, ktorý nie je zastúpený žiadnou entitou. Avšak, niektoré bežné polia a procesy na entitách sú navrhnuté tak, aby používali koncept obchodných transakcií. Nasledujúce entity používajú túto abstrakciu:

- Podrobnosti o riadku cenovej ponuky
- Podrobnosti o riadku zmluvy
- Riadky odhadov
- Záznamy v účtovnom denníku
- Skutočné hodnoty

Z týchto entít sú Podrobnosti o riadku cenovej ponuky, Podrobnosti o riadku zmluvy a Riadky odhadov mapovanú na *fázu odhadu* v životnom cykle projektu. Záznamy v účtovnom denníku a Entity skutočných hodnôt sú priradené k *fáze vykonania* v životnom cykle projektu.

Project Operations zaobchádza so záznamami vo všetkých týchto piatich entitách ako s obchodnými transakciami. Jediným rozdielom je, že záznamy v entitách, ktoré sú mapované do fázy odhadu (Podrobnosti o riadku cenovej ponuky, Podrobnosti o riadku zmluvy a Riadky odhadov) , sa považujú za *finančné prognózy*, zatiaľ čo záznamy v entitách, ktoré sú mapovanú do fázy vykonania, sa považujú za *finančné skutočnosti*, ktoré sa už vyskytli.

Ďalšie informácie nájdete v časti [Estimates](../project-management/estimating-projects-overview.md) a [Actuals](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepty, ktoré sú jedinečné pre obchodné transakcie

Tieto pojmy sú jedinečné pre koncept obchodných transakcií:

- Typ transakcie
- Trieda transakcie
- Počiatok transakcie
- Kontaktná osoba transakcie

### <a name="transaction-type"></a>Typ transakcie

Typ transakcie predstavuje načasovanie a kontext finančného vplyvu na projekt. Je to definované množinou možností, ktorá má nasledujúce podporované hodnoty v Project Operations:

- Náklady
- Projektová zmluva
- Nefakturovaný predaj
- Fakturovaný predaj
- Predaj medzi organizáciami
- Náklady zdrojovej jednotky

### <a name="transaction-class"></a>Trieda transakcie

Trieda transakcie predstavuje rôzne typy nákladov, ktoré vznikli na projektoch. Je to definované množinou možností, ktorá má nasledujúce podporované hodnoty v Project Operations:

- Čas
- Výdavok
- Materiál
- Poplatok
- Medzník
- Daň

> [!NOTE]
> Hodnota **Medzník** sa zvyčajne používa v obchodnej logike pre fakturáciu s pevnou cenou v Project Operations.

### <a name="transaction-origin"></a>Počiatok transakcie

Pôvod transakcie je entita, ktorá ukladá pôvod každej obchodnej transakcie, aby pomohla s vykazovaním a sledovateľnosťou. Keď sa začne s realizáciou projektu, každá obchodná transakcia vytvorí ďalšiu obchodnú transakciu, ktorá bude následne vytvárať ďalšiu obchodnú transakciu a tak ďalej.

### <a name="transaction-connection"></a>Kontaktná osoba transakcie

Transakčné pripojenie je entita, ktorá uchováva vzťah medzi dvoma podobnými obchodnými transakciami, ako sú náklady a súvisiace skutočné hodnoty predaja alebo transakcie zrušenia, ktoré sú spustené fakturačnými činnosťami, ako je potvrdenie faktúry alebo opravy faktúry.

Počiatok transakcie a transakčné pripojenie vám spolu pomáhajú sledovať vzťahy medzi obchodnými transakciami a akciami, ktoré spôsobili vytvorenie konkrétnej obchodnej transakcie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
