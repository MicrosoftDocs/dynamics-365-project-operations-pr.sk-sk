---
title: Čo je nové September 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní spoločnosti Microsoft zo septembra 2022 Dynamics 365 Project Operations pre scenáre založené na zdrojoch/nezásobách.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621370"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové September 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa vzťahuje na nasledujúce súčasti a verzie systému Microsoft Dynamics 365 Project Operations:

- Projektové operácie v a Dataverse verzia prostredia 4.46.0.60
- Projektový manažment a účtovníctvo v prostredí Dynamics 365 Finance verzia 10.0.29

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

| Oblasť funkcií | Názov funkcie | Ďalšie informácie |
| --- | --- | --- |
| Správa príležitostí | **Revízia a aktivácia cenových ponúk**<br>Project Operations prináša plnú podporu procesu predaja. Cenové ponuky projektov je možné aktivovať, aby predstavovali stav, v ktorom je ponuka len na čítanie a prebieha jej kontrola. Aktivované ponuky je možné revidovať, aby sa vytvorili nové ponuky, ktoré majú zvýšené číslo revízie. Aktivované projektové ponuky alebo revízie cenových ponúk možno uzavrieť ako vyhraté alebo prehraté. | [Aktivácia a revízia projektovej cenovej ponuky](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturácia a tvorba cien | **Neplatenie ceny agnostického časového pásma**<br>Projektové operácie zaviedli koncept agnostického dátumu časového pásma na všetkých skutočných projektoch. Nové pole, **Dátum transakcie**, je teraz k dispozícii v riadkoch denníka a aktuálnych údajoch a bude sa používať na uloženie dátumu transakcie, ale bez konverzie tohto dátumu na koordinovaný svetový čas. Tento dátum sa použije pre následné procesy, ako je nedodržanie ceny a vytvorenie faktúry. | <p>[Stanovte nákladové sadzby pre odhady a skutočné skutočnosti založené na projekte](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Stanovte predajné ceny pre projektové odhady a skutočné skutočnosti](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Fakturácia a tvorba cien | **Prepisy cien platné k dátumu v projektových operáciách**<br>Prepisy cien platné k dátumu poskytujú spôsob, ako prepísať alebo zmeniť konkrétne ceny v cenníku. | [Prepisy cien platné od dátumu](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subdodávky | **Odsúhlasenie subdodávok a faktúr dodávateľa**<br>Táto funkcia umožňuje zákazníkom vytvárať subdodávky na nákup času zdrojov, kategórií výdavkov a materiálov, ktoré sa používajú na prácu na projekte. Zákazníkom tiež umožňuje zaznamenávať vo finančných a prevádzkových aplikáciách faktúry dodávateľov, ktoré budú k dispozícii projektovým manažérom Dataverse na overenie. | <p>[Manažment subdodávok](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Vytvorenie faktúr dodávateľov](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Čas a výdavky | **Globálny schvaľovateľ**<br>Táto funkcia umožňuje nezávislého dodávateľa softvéru (ISV) a centralizované schvaľovanie bez ohľadu na stav projektu alebo člena tímu v projekte. | [Zabezpečenie a schválenia](/dynamics365/project-operations/approvals/approvals-security) |
| Správa výdavkov | **Schopnosť účtovať záväzky v mene dodávateľa**<br>Táto funkcia umožňuje zaúčtovať výkazy výdavkov v mene dodávateľa pre spôsob platby v hotovosti. | [Schopnosť účtovať záväzky v mene dodávateľa](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektové obstarávanie | **Zaplaťte pri platbách dodávateľa**<br>Táto funkcia umožňuje použiť funkciu Pay when paid (PWP) v neskladových prostrediach Project Operations. Umožňuje zablokovať/zadržať platby dodávateľa na základe podmienok uchovávania až do prijatia platby od zákazníka. | [Zaplaťte pri platbách dodávateľa](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektové obstarávanie | **Požiadavky na kúpu projektu**<br>Táto funkcia umožňuje používateľom vytvárať objednávky súvisiace s projektom v právnických osobách, kde je povolená integrácia projektu Dynamics 365 Customer Engagement. Objednávky na nákup projektu je možné použiť na evidenciu obstarávania neskladového materiálu oproti projektu personálom oddelenia obstarávania. Objednávky na nákup projektu sa nebudú synchronizovať s Dataverse. Môžete však použiť virtuálnu entitu na zobrazenie riadkov nákupnej objednávky projektu Dataverse pre informácie projektového manažéra. Náklady na faktúru dodávateľa súvisiace s projektom sú integrované s entitou Skutočnosti projektu v Dataverse. Náklady na projekt sa zaznamenávajú v čiastkovej knihe projektu pomocou denníka Integrácia operácií projektu. | |

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúca tabuľka zobrazuje mapy s duálnym zápisom, ktoré boli upravené alebo pridané vo vydaní Project Operations zo septembra 2022.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| -------------- | ------------------- | ------------|
| Skutočné hodnoty integrácie Project Operations (msdyn_actuals) | 1.0.0.15 | Táto mapa podporuje spracovanie skutočných čiastkových zmlúv s projektovými operáciami pre scenáre založené na zdrojoch. |
| Entita exportu faktúr dodávateľa integrácie Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Táto mapa podporuje spracovanie skutočných čiastkových zmlúv s projektovými operáciami pre scenáre založené na zdrojoch. |
| Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Táto mapa podporuje spracovanie skutočných čiastkových zmlúv s projektovými operáciami pre scenáre založené na zdrojoch. |

Vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí a povoľte všetky súvisiace tabuľkové mapy pri aktualizácii operácií projektu Dataverse riešenie a verzia finančného riešenia. Niektoré funkcie a možnosti nemusia fungovať správne, ak nie je aktivovaná najnovšia verzia mapy. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili mapu predpripravenej tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak pri spustení mapy narazíte na problém, postupujte podľa pokynov v časti [Problém chýbajúcich stĺpcov tabuľky na mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) časti príručky na riešenie problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2754422 | Odhady materiálu a nákladov neplynú do financií, keď sa projekty skopírujú Dataverse. |
| Čas a výdavky | 2787409 | Neplatný schvaľovateľ môže schváliť neprojektový časový záznam. |
| Správa príležitostí | 2788907 | Aktualizované chybové hlásenie o overení jedinečnosti pre riadky objednávky, ktoré obsahujú príznaky. |
| Čas a výdavky | 2842253 | Spracovanie nulovej výnimky na schválenie času. |
| Fakturácia a tvorba cien | 2844181 | Neúspech pri získaní ID korelácie blokuje vytvorenie faktúry. |
| Fakturácia a tvorba cien | 2876628 | QLD, CLD – Rozlíšenie odhadovaného cenníka by malo používať staršie polia rozsahu dátumov v cenníku. |
| Subdodávky | 2893222 | Ak nie je špecifikovaná žiadna rola pre subdodávateľskú líniu, malo by byť možné vybrať túto líniu u člena tímu pre akúkoľvek rolu. |

### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo v oblasti financií

Ak chcete získať informácie o opravách chýb, ktoré sú súčasťou tejto aktualizácie, prihláste sa na Microsoft Dynamics Služby životného cyklu a prezrite si [článok KB](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcie sú v nadchádzajúcom vydaní predvolene zapnuté

V nasledujúcej tabuľke sú uvedené funkcie, ktoré sú predvolene zapnuté vo verzii 10.0.30. Väčšinu funkcií, ktoré boli automaticky zapnuté, je možné vypnúť [Správa funkcií](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V budúcnosti môžu byť niektoré funkcie, ktoré boli automaticky zapnuté, odstránené zo správy funkcií a stať sa povinnými. Táto zmena zaisťuje, že zákazníci používajú aktuálnu funkčnosť, takže vylepšenia môžu stavať na aktuálnej funkcii, keď budú pridané. Funkcie nebudú nikdy automaticky aktivované skôr ako za jeden rok, pokiaľ nie sú určené ako nevyhnutné.

| Názov funkcie | Povoliť dátum | Funkcia bola pridaná | Stav funkcie | Modul |
| --- | --- | --- |--- |--- |
| Povoľte asynchrónne operácie, keď používateľ potrebuje prepínať medzi synchronizáciou a asynchronizáciou | 21. októbra 2022 | 9. apríla 2021 | Predvolene zapnuté | Správa výdavkov |
| Vyžaduje sa vyhodnotenie výdavkovej politiky pre príjmy | 21. októbra 2022 | 20. december 2021 | Predvolene zapnuté | Správa výdavkov |
| Zoznam prehľadov výdavkov vytvorených delegovanými pracovníkmi | 21. októbra 2022 | 19. február 2020 | Predvolene zapnuté | Správa výdavkov |
| Výpočet celkových kilometrov od fiškálny rok | 21. októbra 2022 | 10. mája 2022 | Predvolene zapnuté | Správa výdavkov |
