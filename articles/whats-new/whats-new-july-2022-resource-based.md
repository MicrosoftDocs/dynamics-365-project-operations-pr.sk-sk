---
title: Novinky v júli 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft z júla 2022 Dynamics 365 Project Operations pre scenáre založené na zdrojoch/nezásobách.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: cbee9281d2fae485a3ebcd38bb884a2b2322f8d1
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183936"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Novinky v júli 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.44.0.22
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.28

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

V tomto vydaní nie sú k dispozícii žiadne aktualizácie máp duálneho zápisu Project Operations. Aktuálny zoznam a verzie máp duálneho zápisu Project Operations nájdete na v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](../environment/resource-dual-write-maps.md).

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili mapu predpripravenej tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak pri spustení mapy narazíte na problém, postupujte podľa pokynov v časti [Problém chýbajúcich stĺpcov tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Nasadenie a konfigurácia | 2761472 | Chyba inštalácie Project Operations je spracovaná. |
| Fakturácia a tvorba cien | 2746940 | Názov riadku subdodávky by mal mať maximálnu dĺžku 100 znakov. |
| Fakturácia a tvorba cien | 2739162 | Zákazníci musia mať možnosť vidieť tlačidlá na páse s nástrojmi v zobrazení skutočnej mriežky. |
| Plánovanie a sledovanie projektu | 2730318 | Aktualizované overenie pre nepodporované znaky v predmete projektu. |
| Fakturácia a tvorba cien | 2705361 | Skutočné míľnikové fakturované predaje musia byť zahrnuté v poliach sledovania projektu. |
| Fakturácia a tvorba cien | 2675880 | Zabráňte prepojeniu projektu so zmluvnou líniou, ktorá nie je založená na práci. |
| Fakturácia a tvorba cien | 2664396 | Ak je cenník uložený bez ponuky, musí sa vyskytnúť chyba, ktorá uvádza, že ponuka nemôže byť prázdna. |
| Fakturácia a tvorba cien | 2184019 | The **Fakturácia podľa úloh** karta by sa nemala zobrazovať pre projekty, ktoré nemajú žiadnu podpornú zmluvu alebo cenovú ponuku. |

### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo v oblasti financií

Ak chcete získať informácie o opravách chýb, ktoré sú súčasťou tejto aktualizácie, prihláste sa na Microsoft Dynamics Služby životného cyklu (LCS) a pozrite si [článok KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcie sú v nadchádzajúcom vydaní predvolene zapnuté

V nasledujúcej tabuľke sú uvedené funkcie, ktoré sú predvolene zapnuté vo verzii 10.0.29. Väčšinu funkcií, ktoré boli automaticky zapnuté, je možné vypnúť [Správa funkcií](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V budúcnosti môžu byť niektoré funkcie, ktoré boli automaticky zapnuté, odstránené zo správy funkcií a stať sa povinnými. Táto zmena zaisťuje, že zákazníci používajú aktuálnu funkčnosť, takže vylepšenia môžu stavať na aktuálnej funkcii, keď budú pridané. Funkcie nebudú nikdy automaticky aktivované skôr ako za jeden rok, pokiaľ nie sú určené ako nevyhnutné.

| Názov funkcie | Povoliť dátum | Funkcia bola pridaná | Stav funkcie | Modul |
| --- | --- | --- |--- |--- |
| Povoliť úpravu hodinovej transakcie na základe zmeny prideľovania pravidiel financovania | 16. september 2022 | 7. októbra 2020 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Funkcia stornovania zálohovej faktúry projektovej objednávky | 16. september 2022 | 6. októbra 2021 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Odstráňte riadky návrhu faktúry, keď používate operácie projektu pre scenáre založené na zdrojoch/nezásoby | 16. september 2022 | 6. októbra 2021 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Upravte účtovníctvo zaúčtovanej transakcie projektu | 16. september 2022 | 10. mája 2020 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Povoliť predvolené nastavenie účtovania pre projekt | 16. september 2022 | 19. február 2020 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Povoliť pre projekt viac riadkov zmluvy | 16. september 2022 | 29. júna 2020 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Ak aktuálny stav schválenia neumožňuje úpravy, nastavte denníky Hodiny projektu ako na čítanie | 16. september 2022 | 6. októbra 2021 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Povoľte synchronizáciu predajných riadkov z nákupných riadkov, keď sa aktualizujú nákupné riadky a je zapnutý parameter správy zmien nákupných objednávok | 16. september 2022 | 7. októbra 2020 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Povoliť operácie projektu na Dynamics 365 Customer Engagement | 16. september 2022 | 29. júna 2020 | Predvolene zapnuté | Projektový manažment a účtovníctvo |
| Funkcia opravy zvrátenia transakcie projektu | 16. september 2022 | 13. júl 2020 | Predvolene zapnuté | Projektový manažment a účtovníctvo |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcie, ktoré sa stanú povinnými v nadchádzajúcom vydaní

V nasledujúcej tabuľke sú uvedené funkcie, ktoré sú povinné od verzie 10.0.29.

| Názov funkcie | Povoliť dátum | Funkcia bola pridaná | Stav funkcie | Modul |
| --- | --- | --- | --- | --- |
| Vypočítajte viazanú hodnotu zdroja financovania bez zaokrúhlenia výmenného kurzu | 16. september 2022 | 14. júna 2020 | Povinné | Projektový manažment a účtovníctvo |
| Povoliť účtovanie úpravy projektu s rovnakým účtovným účtom ako pôvodná transakcia | 16. september 2022 | 14. júna 2020 | Povinné | Projektový manažment a účtovníctvo |
| Detail viazanej sumy projektovej zmluvy | 16. september 2022 | 31. august 2019 | Povinné | Projektový manažment a účtovníctvo |
| Povoliť triedenie podľa zdroja počas vytvárania návrhu projektovej faktúry | 16. september 2022 | 31. august 2019 | Povinné | Projektový manažment a účtovníctvo |
