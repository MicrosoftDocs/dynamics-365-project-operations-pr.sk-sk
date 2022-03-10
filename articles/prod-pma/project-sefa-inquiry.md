---
title: Časový plán výdavkov na vyšetrovanie federálnych ocenení
description: Táto téma poskytuje informácie o dotazníku Časový plán výdavkov federálneho ocenenia.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: d0cc3db3fd05fa809f707b15a50380753ac8f9f779f45c13f707321d2b0e0841
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007255"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>Časový plán výdavkov na vyšetrovanie federálnych ocenení

[!include [banner](../includes/banner.md)]

Podľa Úradu pre správu a rozpočet A-133 sa na agentúry, ktoré dostávajú federálne fondy, vzťahujú požiadavky na audit, ktoré sa označujú aj ako jednotné audity. Proces auditu sa používa na opakované podávanie správ o príjmoch a výdavkoch federálnych grantov. Súčasťou správy o jednotnom audite je Časový plán výdavkov federálneho ocenenia (SEFA).

Časový plán výdavkov na federálne ocenenia obsahuje názov a číslo Katalógu federálnej domácej pomoci (CFDA), číslo grantu, rok poskytnutia grantu, názov federálnej agentúry, ktorá poskytuje finančné prostriedky, a názov hesla prostredníctvom subjektu. Dotaz je na konkrétne obdobie. Toto obdobie je zvyčajne rovnaké ako obdobie účtovnej závierky, čo je fiškálny rok.

Dotaz zahŕňa granty, ktoré majú predpokladané dátumy vo vybranom rozsahu dátumov. **Grantová agentúra** v stĺpci dopytu sa zobrazuje zákazník s grantom alebo v prípade grantu s priamym prenosom agentúra s grantom. Pokiaľ ide o prechodný grant, **Agentúra s priamym prechodom** stĺpec zobrazuje zákazníka s grantom. Pokiaľ nejde o prechodný grant, **Agentúra s priamym prechodom** stĺpec bude prázdny.

## <a name="set-up-the-cfda-clusters"></a>Nastavenie klastrov CFDA

Klastre CFDA, ktoré môžu byť spojené s číslami CFDA, musíte nastaviť v dotazníku Schedule of Expenditures of Federal Awards.

1. Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Nastavenie \> Granty \> Katalóg klastrov federálnej domácej pomoci**.
2. Stlačte možnosť **Nový** a vytvorte klaster CFDA.
3. Zadajte názov klastra.
4. Zmeny vykonajte výberom položky **Uložiť**.

## <a name="set-up-cfda-numbers"></a>Nastavte čísla CFDA

Klastre CFDA, ktoré môžu byť priradené ku grantom a môžu byť zaradené v dotazníku Schedule of Expenditures of Federal Awards.

1. Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Nastavenie \> Granty \> Katalóg čísel federálnej domácej pomoci**.
2. Stlačte možnosť **Nový** a vytvorte číslo CFDA.
3. V stĺpci **Číslo** zadajte číslo CFDA.
4. Stlačte kláves **Tab**.
5. V stĺpci **Opis** zadajte názov CFDA.
6. Stlačte kláves **Tab**.
7. V priečinku **Programový klaster** do poľa pridajte vhodný klaster CFDA.
8. Zmeny vykonajte výberom položky **Uložiť**.

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Nastaviť granty pre správu pre Schedule of Expenditures of Federal Awards

1. Prejdite do **Projektové riadenie a účtovníctvo \> Granty \> Granty** a zvoľte si existujúci grant.
2. Na rýchlej karte **Nastavenia** v poli **Katalóg Federal Domestic Assistance** priraďte číslo CFDA. Číslo CFDA na grante určuje klaster CFDA na vykazovanie.
3. Na FastTab **Kontaktné informácie** zadajte informácie o poskytovateľovi vykonaním týchto krokov:

    1. V poli **Zákazník grantu** do poľa zadajte zákazníka, ktorý je zodpovedný za grant. V prípade existujúceho grantu môžu byť tieto informácie už zadané.
    2. Uveďte, či je grantový zákazník donorom. Ak je grantovým zákazníkom donor, nechajte políčko **Priamy prechod** neoznačené. Ak je finančným darcom iný zákazník a zákazník, ktorý je príjemcom grantu, je zodpovedný za výdavky a sledovanie peňazí, označte políčko **Priamy prechod**.

4. Ak ste začiarkli políčko **Priamy prechod** v predchádzajúcom kroku, v priečinku **Grantová agentúra** do poľa zadajte zákazníka, ktorý poskytol grant. Agentúra poskytujúca pomoc a zákazník, ktorý je príjemcom grantu, nemôžu byť rovnakí zákazníci.

Tu je príklad priameho grantu:

Federálna vláda financovala štátny projekt infraštruktúry. Federálna vláda dala peniaze štátu na utratenie. V tomto prípade je federálnou vládou agentúra poskytujúca granty a štát je zákazníkom grantu.

> [!NOTE] 
> Pri prvom zapnutí tejto funkcie sa počiatočné čísla CFDA zadajú pomocou existujúcich čísel v grantoch.

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>Vylúčiť granty z vykazovania SEFA na základe typu grantu

1. Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Nastavenie \> Granty \> Typy grantov**.
2. Na karte rýchlej karte **Predvolené informácie** označte políčko **Vylúčte z rozvrhu výdavkov federálnych ocenení**.
3. Zmeny vykonajte výberom položky **Uložiť**.

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>Spustite Časový plán výdavkov na vyšetrovanie federálnych ocenení

1. Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Dotazy a otázky \> Dotaz na udelenie grantu \> Časový plán výdavkov federálnych ocenení**.
2. V časti **Parametre** dodržiavajte nasledovné kroky:

    1. V poli **Interval dátumu** zvoľte kód pre interval dátumov. Prípadne v poliach **Dátum Od** a **Dátum Do** definujte časový interval.
    2. Voliteľné: Ak chcete do dopytu zahrnúť iba fakturované transakcie, nastavte možnosť **Zahrňte iba fakturované výnosy** na **Áno**.

## <a name="columns"></a>Stĺpce

Dotazník o Časový plán výdavkov na vyšetrovanie federálnych ocenení zahŕňa nasledovné stĺpce:

- Katalóg názvu klastra federálnej domácej pomoci
- Grantová agentúra
- Agentúra s priamym prechodom
- Názov grantu
- ID grantu
- ID žiadosti o grant
- Katalóg klastra federálnej domácej pomoci
- Potvrdenia
- Výdavky


[!INCLUDE[footer-include](../includes/footer-banner.md)]