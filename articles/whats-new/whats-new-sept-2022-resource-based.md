---
title: Čo je nové September 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Tento článok poskytuje informácie o aktualizáciách kvality dostupných vo vydaní Microsoft Dynamics 365 Project Operations Project Operations v septembri 2022 pre scenáre založené na zdrojoch/neskladovaných položkách.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634825"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Čo je nové September 2022 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok sa týka nasledujúcich komponentov a verzií Microsoft Dynamics 365 Project Operations:

- Project Operations v prostredí Dataverse verzie 4.46.0.60
- Projektový manažment a účtovníctvo v prostrední Dynamics 365 Finance, verzia 10.0.29

## <a name="features-included-in-this-release"></a>Funkcie dostupné v tomto vydaní

| Oblasť funkcií | Názov funkcie | Ďalšie informácie |
| --- | --- | --- |
| Správa príležitostí | **Revízia a aktivácia cenových ponúk**<br>Project Operations prináša plnú podporu procesu predaja. Cenové ponuky projektov je možné aktivovať, aby predstavovali stav, v ktorom je ponuka len na čítanie a prebieha jej kontrola. Aktivované cenové ponuky je možné revidovať, aby sa vytvorili nové cenové ponuky, ktoré majú vyššie číslo revízie. Aktivované revízie cenových ponúk projektu je možné uzavrieť ako Získaná alebo Nevyužitá. | [Aktivácia a revízia projektovej cenovej ponuky](/dynamics365/project-operations/sales/activation-and-revision) |
| Fakturácia a tvorba cien | **Predvolená cena bez znalosti časového pásma**<br>Project Operations zaviedli koncept bez znalosti dátumu časového pásma pre všetky skutočné hodnoty projektov. Nové pole, **Dátum transakcie**, je teraz k dispozícii v záznamoch v účtovnom denníku a skutočných hodnotách a bude sa používať na uloženie dátumu transakcie, ale bez konverzie tohto dátumu na koordinovaný svetový čas. Tento dátum sa použije pre následné procesy, ako je nedodržanie ceny a vytvorenie faktúry. | <p>[Určenie nákladových sadzieb pre odhady a skutočné hodnoty založené na projektoch](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Určenie predajných cien pre odhady a skutočné hodnoty založené na projektoch](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Fakturácia a tvorba cien | **Prepisy cien s dátumom účinnosti v Project Operations**<br>Prepísanie cien s dátumom účinnosti poskytuje spôsob, ako prepísať alebo zmeniť konkrétne ceny v cenníku. | [Prepísania cien s dátumom účinnosti](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subdodávateľské zmluvy | **Odsúhlasenie subdodávateľských zmlúv a faktúr dodávateľa**<br>Táto funkcia umožňuje zákazníkom vytvárať subdodávateľské zmluvy na nákup času zdrojov, kategórií výdavkov a materiálov, ktoré sa používajú na prácu na projekte. Zákazníkom tiež umožňuje zaznamenávať aplikáciách na riadenie financií a prevádzok faktúry dodávateľov, ktoré budú k dispozícii projektovým manažérom v Dataverse na overenie. | <p>[Správa subdodávateľských zmlúv](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Vytvorenie faktúr dodávateľov](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Čas a výdavky | **Globálny schvaľovateľ**<br>Táto funkcia umožňuje nezávislého dodávateľa softvéru (ISV) a centralizované schvaľovanie bez ohľadu na stav projektu alebo člena tímu v projekte. | [Zabezpečenie a schválenia](/dynamics365/project-operations/approvals/approvals-security) |
| Správa výdavkov | **Schopnosť účtovať výdavkový záväzok v mene dodávateľa**<br>Táto funkcia umožňuje zaúčtovať výkazy výdavkov v mene dodávateľa pre spôsob platby v hotovosti. | [Schopnosť účtovať výdavkový záväzok v mene dodávateľa](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektové obstarávanie | **Platba po zaplatení platieb dodávateľom**<br>Táto funkcia umožňuje použiť funkciu Zaplatiť po zaplatení (PWP) v neskladových prostrediach Project Operations. Umožňuje zablokovať/zadržať platby dodávateľa na základe podmienok zadržania až do prijatia platby od zákazníka. | [Platba po zaplatení platieb dodávateľom](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektové obstarávanie | **Žiadosti o nákup v rámci projektu**<br>Táto funkcia umožňuje používateľom vytvárať objednávky súvisiace s projektom v právnických osobách, kde je povolená integrácia Project Operations v Dynamics 365 Customer Engagement. Projektové nákupné objednávky je možné použiť na evidenciu obstarávania neskladového materiálu oproti projektu personálom oddelenia obstarávania. Projektové nákupné objednávky sa nebudú synchronizovať s Dataverse. Môžete však použiť virtuálnu entitu na zobrazenie riadkov projektovej nákupnej objednávky v Dataverse pre informácie projektového manažéra. Náklady na faktúru dodávateľa súvisiace s projektom sú integrované s entitou Skutočné hodnoty projektu v Dataverse. Náklady na projekt sa zaznamenávajú do čiastkovej účtovnej knihy projektu pomocou denníka Integrácia Project Operations. | |
|Plánovanie a sledovanie projektu|**Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu** </br> </br>Rozhranie API na úpravu kontúr priradenia zdrojov umožňuje vývojárom programovo špecifikovať úsilie zadávateľa úlohy v akomkoľvek podporovanom rozsahu dátumov, aby bolo možné podrobnejšie plánovať časovo rozložené úsilie.|[Na vykonávanie operácií s entitami plánovania použite rozhrania API pre plánovanie projektu](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>Aktualizácie máp duálneho zapisovania v aplikácii Project Operations

Nasledujúca tabuľka zobrazuje mapy duálneho zápisu, ktoré boli upravené alebo pridané vo vydaní Project Operations zo septembra 2022.

| Mapa entity | Aktualizovaná verzia | Vytvoril |
| -------------- | ------------------- | ------------|
| Skutočné hodnoty integrácie Project Operations (msdyn_actuals) | 1.0.0.15 | Táto mapa podporuje spracovanie skutočných hodnôt subdodávateľských zmlúv s Project Operations pre scenáre založené na zdrojoch. |
| Entita exportu faktúr dodávateľa integrácie Project Operations (msdyn_projectvendorinvoices) | 1.0.0.2 | Táto mapa podporuje spracovanie skutočných hodnôt subdodávateľských zmlúv s Project Operations pre scenáre založené na zdrojoch. |
| Riadok entity exportu faktúr projektu dodávateľa projektu Project Operations (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Táto mapa podporuje spracovanie skutočných hodnôt subdodávateľských zmlúv s Project Operations pre scenáre založené na zdrojoch. |

Pri aktualizácii riešenia Project Operations Dataverse a verzie riešenia Finance vždy spúšťajte najnovšiu verziu mapy vo svojom prostredí, no zároveň aktivujte všetky mapy príslušnej tabuľky. Ak nie je aktivovaná najnovšia verzia mapy, niektoré funkcie a možnosti nemusia fungovať správne. Aktívnu verziu mapy môžete vidieť v stĺpci **Verzia** na stránke **Duálny zápis**. Novú verziu mapy aktivujete výberom možnosti **Verzie mapy tabuľky**, zvolením najnovšej verzie a potom uložením vybratej verzie. Ak ste prispôsobili predpripravenú mapu tabuľky, znova použite zmeny. Ďalšie informácie si prečítajte v časti [Správa životného cyklu aplikácie](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Ak narazíte na problém pri spúšťaní mapy, postupujte podľa pokynov v časti [Problém s chýbajúcimi stĺpcami tabuľky v mapách](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) v časti Sprievodca riešením problémov s duálnym zápisom.

## <a name="quality-updates"></a>Aktualizácie kvality

### <a name="project-operations-on-dataverse"></a>Project Operations v prostredí Dataverse

| Oblasť funkcií | Číslo odkazu | Aktualizácia kvality |
| --- | --- | --- |
| Fakturácia a tvorba cien | 2754422 | Odhady materiálu a výdavkov neprechádzajú do Finance, keď sa projekty skopírujú v Dataverse. |
| Čas a výdavky | 2787409 | Neplatný schvaľovateľ môže schváliť neprojektový časový záznam. |
| Správa príležitostí | 2788907 | Aktualizované chybové hlásenie o overení jedinečnosti pre riadky objednávky, ktoré obsahujú príznaky. |
| Čas a výdavky | 2842253 | Spracovanie nulovej výnimky na schválenie času. |
| Fakturácia a tvorba cien | 2844181 | Neúspech pri získaní ID korelácie blokuje vytvorenie faktúry. |
| Fakturácia a tvorba cien | 2876628 | QLD, CLD – Riešenie odhadovaného cenníka by malo používať staršie polia rozsahu dátumov v cenníku. |
| Subdodávateľské zmluvy | 2893222 | Ak nie je špecifikovaná žiadna rola pre riadok subdodávateľskej zmluvy, malo by byť možné vybrať tento riadok u člena tímu pre akúkoľvek rolu. |

### <a name="project-management-and-accounting-in-finance"></a>Projektový manažment a účtovníctvo vo Finance

Informácie o opravách zahrnutých v tejto aktualizácii nájdete po prihlásení do Microsoft Dynamics Lifecycle Services a zobrazení [článku vedomostnej databázy](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcie sú v nadchádzajúcom vydaní predvolene zapnuté

V nasledujúcej tabuľke sú uvedené funkcie, ktoré sú predvolene zapnuté vo verzii 10.0.30. Väčšinu funkcií, ktoré boli automaticky zapnuté, je možné vypnúť v ponuke [Správa funkcií](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). V budúcnosti môžu byť niektoré funkcie, ktoré boli automaticky zapnuté, odstránené zo Správy funkcií a môžu sa stať povinnými. Táto zmena zaisťuje, že zákazníci používajú aktuálne funkcie, takže vylepšenia môžu stavať na aktuálnych funkciách, keď budú pridané. Funkcie nebudú nikdy automaticky aktivované skôr ako za jeden rok, pokiaľ nie sú určené ako nevyhnutné.

| Názov funkcie | Dátum povolenia | Funkcia bola pridaná | Stav funkcie | Modul |
| --- | --- | --- |--- |--- |
| Povolenie asynchrónnej operácie, keď používateľ potrebuje prepínať medzi synchrónnymi a asynchrónnymi operáciami | 21. októbra 2022 | 9. apríla 2021 | Štandardne zapnuté | Správa výdavkov |
| Vyžaduje sa vyhodnotenie výdavkovej politiky pre príjmy | 21. októbra 2022 | 20. december 2021 | Štandardne zapnuté | Správa výdavkov |
| Zoznam prehľadov výdavkov vytvorených delegovanými pracovníkmi | 21. októbra 2022 | 19. február 2020 | Štandardne zapnuté | Správa výdavkov |
| Výpočet celkového počtu najazdených kilometrov podľa fiškálneho roku | 21. októbra 2022 | 10. mája 2022 | Štandardne zapnuté | Správa výdavkov |
