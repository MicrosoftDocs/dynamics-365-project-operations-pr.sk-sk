---
title: Synchronizujte aktuálne informácie o projekte priamo z Project Service Automation do denníka integrácie projektu na zaúčtovanie v Financie a prevádzka
description: Tento článok popisuje šablóny a základné úlohy, ktoré sa používajú na synchronizáciu skutočných hodnôt projektu priamo z Microsoft Dynamics 365 Project Service Automation do financií a prevádzky.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 7d912a11d9c7bc66ed43911ee32f25092d551cd6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929509"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synchronizujte aktuálne informácie o projekte priamo z Project Service Automation do denníka integrácie projektu na zaúčtovanie v Financie a prevádzka

[!include[banner](../includes/banner.md)]

Tento článok popisuje šablóny a základné úlohy, ktoré sa používajú na synchronizáciu skutočných hodnôt projektu priamo z Dynamics 365 Project Service Automation do Dynamics 365 Finance.

Šablóna synchronizuje transakcie z Project Service Automation do postupnej tabuľky v službe Finance. Po dokončení synchronizácie **musíte** importovať údaje z pracovnej tabuľky do integračného denníka.

> [!NOTE]
> - Integrácia skutočných hodnôt projektu je dostupná od verzie 8.0.1.
> - Ak používate Enterprise Edition 7.3.0, po inštalácii KB 4132657 a KB 4132660 budete môcť tieto šablóny použiť na integráciu projektových úloh, kategórií transakcií výdavkov, odhadov hodín, odhadov výdavkov a skutočných údajov a na nakonfigurovať blokovanie funkcií. Ak musíte resetovať účtovné prerozdelenie, odporúčame vám nainštalovať si aj KB 4131710.
> - Ak používate verziu 7.3.0 a prenášate transakcie poplatkov z Project Service Automation, musíte nainštalovať KB 4345320, aby ste mohli zahrnúť tieto poplatky do faktúry za projekt.
> - Ak zadávate čiastky dane z obratu v časových alebo výdavkových transakciách v Project Service Automation, musíte si nainštalovať Project Service Automation Update 7. V opačnom prípade nebudú daňové skutočnosti spojené s príslušnými časovými alebo výdavkovými skutočnosťami a nebudú synchronizované s Finance. Ďalšie informácie vám poskytne tím podpory.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok údajov pre Project Service Automation do Finance

Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance. Šablóny integrácie, ktorá sú k dispozícii s funkciou integrácie údajov, umožňuje tok údajov o projektových skutočných hodnotách z Project Service Automation do Finance.

Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.

[![Dátový tok pre integráciu Project Service Automation s Finance and Operations.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Skutočné hodnoty projektu z Project Service Automation

### <a name="template-and-tasks"></a>Šablóna a úlohy

Dostupné šablóny nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt**, kde si vyberiete verejné šablóny.

Nasledujúca šablóna a základné úlohy sa používajú na synchronizáciu skutočných hodnôt z Project Service Automation do Finance:

- **Názov šablóny v časti Integrácia údajov:** Projektové skutočné hodnoty (PSA do Fin a Ops)
- **Názov úloh v projekte:**

    - Skutočné údaje
    - TransactionConnections

### <a name="entity-set"></a>Nastavenie entity

| Project Service Automation | Finance                                   |
|----------------------------|----------------------------------------------------------|
| Skutočné údaje                    | Integračná entita pre skutočné hodnoty projektu                   |
| Kontaktné osoby pre transakcie    | Integračná entita pre transakčné vzťahy projektu |

### <a name="entity-flow"></a>Tok entity

Projektové skutočné hodnoty sa spravujú v Project Service Automation a synchronizujú sa s denníkom projektovej integrácie vo Finance. Účtovníctvo sa použije na základe predvolených finančných dimenzií a nastavenia účtovania.

### <a name="prerequisites"></a>Predpoklady

Predtým, ako môže dôjsť k synchronizácii skutočností, musíte nakonfigurovať integračné parametre Project Service Automation a synchronizovať projekty, projektové úlohy a transakčné kategórie výdavkov na projekt.

### <a name="power-query"></a>Power Query

V šablóne skutočných projektov musíte použiť Microsoft Power Query aby Excel dokončil tieto úlohy:

- Transformujte typ transakcie v Project Service Automation na správny typ transakcie v službe Finance. Táto transformácia je už definovaná v šablóne skutočné hodnoty projektu (PSA pre Fin a Ops).
- Transformujte typ fakturácie v Project Service Automation na správny typ fakturácie v službe Finance. Táto transformácia je už definovaná v šablóne skutočné hodnoty projektu (PSA pre Fin a Ops). Typ fakturácie sa potom namapuje na vlastnosť riadku na základe konfigurácie na strane **Integračné parametre Project Service Automation**.
- Filtrujte podľa konkrétnych organizačných jednotiek zdrojov, ktoré sa musia synchronizovať s touto šablónou.
- Ak sa medzipodnikový čas alebo skutočné údaje medzipodnikových výdavkov synchronizujú s Finance, musíte transformovať organizačnú jednotku zmluvy na správny právny subjekt v službe Finance. V šablóne skutočných hodnôt projektu (PSA pre Fin a Ops) je definovaný podmienený stĺpec založený na ukážkových údajoch. Posledný vložený podmienený stĺpec musíte aktualizovať na správne právnické osoby. V opačnom prípade môže dôjsť k chybe integrácie alebo k importovaniu nesprávnych skutočných transakcií do služby Finance.
- Ak sa medzipodnikový čas alebo skutočné údaje medzipodnikových výdavkov nebudú synchronizovať s Finance, musíte zo šablóny odstrániť posledný vložený podmienený stĺpec. V opačnom prípade môže dôjsť k chybe integrácie alebo k importovaniu nesprávnych skutočných transakcií do služby Finance.

#### <a name="contract-organizational-unit"></a>Zmluvná organizačná jednotka
Ak chcete aktualizovať vložený podmienený stĺpec v šablóne, kliknite na šípku **Mapovať** na otvorenie mapovania. Vyberte **Rozšírené dopytovanie a filtrovanie** odkaz na otvorenie Power Query.

- Ak používate predvolenú šablónu Project facts (PSA to Fin and Ops), v Power Query, vyberte posledný **Vložená podmienka** z **Aplikované kroky** oddiele. V zázname **Funkcia** nahraďte **USSI** za názov právnej entity, ktorá sa musí použiť pri integrácii. Pridajte ďalšie podmienky k záznamu **Funkcie** podľa potreby a aktualizujte podmienku **inak** z **USMF** na správnu právnu entitu.
- Ak vytvárate novú šablónu, musíte pridať stĺpec, ktorý podporuje medzipodnikový čas a výdavky. Zvoľte možnosť **Pridať podmienený stĺpec** a zadajte názov stĺpca, napríklad **LegalEntity**. Zadajte podmienku pre stĺpec, kde ak **msdyn\_contractorganizationalunitid.msdyn\_name** je \<organizational unit\>, potom \<enter the legal entity\>; inak ide o príznak null.

### <a name="template-mapping-in-data-integration"></a>Mapovanie šablón v integrácii údajov

Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov. Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.

[![Mapovanie šablón - Skutočné údaje.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Mapovanie šablón – Transakčné spojenia.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Import z pracovnej tabuľky po integrácii z Project Service Automation

Periodický proces importu z pracovnej tabuľky musí byť spustený po synchronizácii skutočností z Project Service Automation do Finance. Tento proces naimportuje transakcie projektu z pracovnej tabuľky do integračného denníka Project Service Automation, kde sa použije účtovníctvo a môžu sa zaúčtovať importované transakcie. Odporúčame vám spustiť tento proces v dávkovom režime; môže byť voliteľne nastavený tak, aby fungoval ako opakujúca sa dávka.

## <a name="update-actuals-from-finance"></a>Aktualizujte údaje z Finance

### <a name="template-and-tasks"></a>Šablóna a úlohy

Nasledujúca šablóna a príslušné úlohy sa používajú na synchronizáciu čísla dokladu a dane z obratu zaúčtované projektové transakcie z Finance do Project Service Automation:

- **Názov šablóny v časti Integrácia údajov:** Projektové skutočné hodnoty (PSA do Fin a Ops)
- **Názov úloh v projekte:**

    - Skutočné údaje 
    - TransactionConnections

### <a name="entity-set"></a>Nastavenie entity

| Finance                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Integračná entita pre skutočné hodnoty projektu                   | Skutočné údaje                    |
| Integračná entita pre transakčné vzťahy projektu | Kontaktné osoby pre transakcie    |

### <a name="entity-flow"></a>Tok entity

Projektové skutočné hodnoty sa spravujú v Project Service Automation a synchronizujú sa s denníkom projektovej integrácie vo Finance. Po zverejnení skutočností v službe Finance sa aktualizujú v Project Service Automation o číslo dokladu z aplikácie Finance. Ak boli do aplikácie Finance pridané dane z obratu, nové skutočné údaje o dani sa vytvoria v Project Service Automation.

### <a name="power-query"></a>Power Query

V šablóne aktualizácie skutočných projektov musíte použiť Power Query na dokončenie týchto úloh:

- Transformujte typ transakcie v Finance na správny typ transakcie v službe Project Service Automation. Táto transformácia je už definovaná v šablóne aktualizácie skutočných hodnôt projektu (PSA pre Fin a Ops).
- Transformujte typ fakturácie vo Finance na správny typ fakturácie v službe Project Service Automation. Táto transformácia je už definovaná v šablóne aktualizácie skutočných hodnôt projektu (PSA pre Fin a Ops).

### <a name="template-mapping-in-data-integration"></a>Mapovanie šablón v integrácii údajov

Nasledujúca ilustrácia ukazuje príklady mapovania úlohy šablóny v Integrácii údajov. Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Finance do Project Service Automation.

[![Mapovanie šablón – Aktualizácia skutočných údajov.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Mapovanie šablón – Aktualizácia transakcie.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]