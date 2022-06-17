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

V Microsofte Dynamics 365 Project Operations, *transakcia* je abstraktný pojem, ktorý nie je reprezentovaný žiadnou entitou. Avšak, niektoré bežné polia a procesy na entitách sú navrhnuté tak, aby používali koncept obchodných transakcií. Nasledujúce entity používajú túto abstrakciu:

- Podrobnosti o riadku cenovej ponuky
- Podrobnosti o riadku zmluvy
- Riadky odhadov
- Záznamy v účtovnom denníku
- Skutočné hodnoty

Z týchto entít sú namapované podrobnosti o riadku cenovej ponuky, podrobnosti o riadku zmluvy a riadky odhadu *fáza odhadu* v životnom cykle projektu. Riadky denníka a entity Actuals sú namapované na *realizačná fáza* v životnom cykle projektu.

Project Operations zaobchádza so záznamami vo všetkých piatich týchto subjektoch ako s obchodnými transakciami. Jediný rozdiel je v tom, že sa berú do úvahy záznamy v entitách, ktoré sú namapované do fázy odhadu (podrobnosti riadku cenovej ponuky, podrobnosti zmluvného riadku a riadky odhadu).*finančné prognózy*, pričom sa berú do úvahy záznamy v entitách, ktoré sú namapované do fázy vykonávania (riadky denníka a skutočné údaje).*finančné fakty* ktoré sa už vyskytli.

Ďalšie informácie nájdete v časti [Estimates](../project-management/estimating-projects-overview.md) a [Actuals](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Koncepty, ktoré sú jedinečné pre obchodné transakcie

Tieto pojmy sú jedinečné pre koncept obchodných transakcií:

- Typ transakcie
- Trieda transakcie
- Počiatok transakcie
- Kontaktná osoba transakcie

### <a name="transaction-type"></a>Typ transakcie

Typ transakcie predstavuje načasovanie a kontext finančného vplyvu na projekt. Je definovaný množina možností, ktorý má v prevádzke projektu nasledujúce podporované hodnoty:

- Náklady
- Projektová zmluva
- Nefakturovaný predaj
- Fakturovaný predaj
- Predaj medzi organizáciami
- Náklady zdrojovej jednotky

### <a name="transaction-class"></a>Trieda transakcie

Trieda transakcie predstavuje rôzne typy nákladov, ktoré vznikli na projektoch. Je definovaný množina možností, ktorý má v prevádzke projektu nasledujúce podporované hodnoty:

- Čas
- Výdavok
- Materiál
- Poplatok
- Medzník
- Daň

> [!NOTE]
> The **Míľnik** hodnota sa zvyčajne používa v obchodnej logike na fakturáciu s pevnou cenou v prevádzke projektu.

### <a name="transaction-origin"></a>Počiatok transakcie

Pôvod transakcie je entita, ktorá uchováva pôvod každej obchodnej transakcie, aby pomohla s vykazovaním a sledovateľnosťou. Keď sa začne realizácia projektu, každá obchodná transakcia vytvorí ďalšiu obchodnú transakciu, ktorá následne vytvorí ďalšiu obchodnú transakciu atď.

### <a name="transaction-connection"></a>Kontaktná osoba transakcie

Transakčné spojenie je entita, ktorá uchováva vzťah medzi dvoma podobnými obchodnými transakciami, ako sú skutočné náklady a súvisiace predaje alebo stornovania transakcií, ktoré sa spúšťajú fakturačnými činnosťami, ako je potvrdenie faktúry alebo opravy faktúr.

Spoločne entity pôvodu transakcie a pripojenia transakcie vám pomôžu sledovať vzťahy medzi obchodnými transakciami a akciami, ktoré spôsobili vytvorenie konkrétnej obchodnej transakcie.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
