---
title: Integrácia odhadov a skutočných hodnôt projektu
description: Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre odhady a skutočné hodnoty projektu.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c558ab1eb5070f6d1a2db06b630e8807cc67819f9bdd57c15ec346f484e04fe9
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7006310"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrácia odhadov a skutočných hodnôt projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre odhady a skutočné hodnoty projektu.

## <a name="project-estimates"></a>Odhady projektu

Odhady projektovej práce, výdavkov a materiálu sa vytvárajú a udržiavajú v Microsoft Dataverse a synchronizované s aplikáciami Finance and Operations na účtovné účely. Operácie na vytváranie, aktualizáciu a mazanie nie sú prostredníctvom servera podporované v aplikáciách Finance and Operations.

Vytvorenie odhadov si vyžaduje platnú konfiguráciu účtovníctva pre projekt. Projekty, ktoré sú spojené s riadkami zmluvy, musia mať platný profil nákladov a výnosov projektu definovaný v pravidlách profilu nákladov a výnosov projektu. Viac informácií nájdete v časti [Konfigurácia účtovníctva pre fakturovateľné projekty](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Odhady pracovnej sily

Odhady pracovnej sily vytvára projektový manažér alebo manažér zdrojov, ktorý tiež projektovej úlohe priradí všeobecný alebo pomenovaný zdroj. Záznamy o priradení zdrojov možno skontrolovať na karte **Priradenia zdrojov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy o priradení zdrojov v Dataverse vytvárajú záznamy predpovedí hodín v aplikáciách Finance and Operations pomocou **Entity integrácie Project Operations pre hodinové odhady (msdyn\_resourceassignments)**.

   ![Integrácia pracovných odhadov.](./Media/DW4LaborEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy o priradení prostriedkov do pracovnej tabuľky (**ProjCDSEstimateHoursImport**) a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy predpovedí hodín (**ProjForecastEmpl**).

Účtovník projektu kontroluje záznamy o predpovedi hodín vytvorené v aplikáciách Finance and Operations prechodom do ponuky **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Predpovede hodín**.

## <a name="expense-estimates"></a>Odhady nákladov

Odhady výdavkov vytvára projektový manažér na karte **Odhady výdavkov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy o odhade výdavkov sú uložené v entite **Riadok odhadu** v Dataverse. Tieto odhady majú transakčnú triedu, **Výdavky** a sú synchronizované so záznamami prognóz výdavkov v aplikáciách Finance and Operations použitím **Entity integrácie Project Operations pre odhady výdavkov (msdyn\_estimatelines)**.

   ![Integrácia odhadov výdavkov.](./Media/DW4ExpenseEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy odhadov výdavkov do pracovnej tabuľky (**ProjCDSEstimateExpenseImport**) a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy o výdavkoch (**ProjForecastCost**). Odhady riadkov ukladajú odhady predaja a odhady nákladov osobitne. Obchodná logika v aplikáciách Finance and Operations vyplní jeden záznam prognózy výdavkov pomocou tohto detailu v pracovnej tabuľke.

Účtovník projektu kontroluje alebo zobrazuje záznamy o predpovedi výdavkov vytvorené v aplikáciách Finance and Operations prechodom do ponuky **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Predpovede výdavkov**.

## <a name="material-estimates"></a>Odhady materiálov

Odhady materiálov vytvára projektový manažér na karte **Odhady materiálov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy o odhade materiálov sú uložené v entite **Riadok odhadu** v Dataverse. Tieto odhady majú transakčnú triedu, **Materiál** a sú synchronizované so záznamami prognóz položky v aplikáciách Finance and Operations použitím **Tabuľky integrácie Project Operations pre odhady výdavkov (msdyn\_estimatelines)**.

   ![Integrácia odhadov materiálov.](./Media/DW4MaterialEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy odhadov materiálov do pracovnej tabuľky **ProjForecastSalesImpor** a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy o predpovede položky (**ForecastSales**). Odhady riadkov ukladajú odhady predaja a odhady nákladov osobitne. Obchodná logika v aplikáciách Finance and Operations vyplní jeden záznam prognózy položky pomocou tohto detailu v pracovnej tabuľke.

Účtovník projektu kontroluje alebo zobrazuje záznamy o predpovedi položiek vytvorené v aplikáciách Finance and Operations prechodom do ponuky **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Predpovede položiek**.

## <a name="project-actuals"></a>Skutočné hodnoty projektu

Skutočné hodnoty projektu sú vytvorené v Dataverse na základe času, výdavkov, materiálu a fakturačnej činnosti. V tejto entite Dataverse sú zachytené všetky prevádzkové atribúty týchto transakcií vrátane množstva, nákladovej ceny, predajnej ceny. Ďalšie informácie nájdete v časti [Skutočné hodnoty](../actuals/actuals-overview.md). Skutočné záznamy sa synchronizujú s aplikáciami Finance and Operations pomocou mapy tabuľky s dvojitým zápisom, **Skutočné hodnoty integrácie Project Operations (msdyn\_actuals)** pre následné účtovníctvo.

   ![Integrácia skutočných hodnôt.](./Media/DW4Actuals.png)

Mapa tabuľky **Integrácia skutočných údajov Project Operations** synchronizuje všetky záznamy z entity **Skutočné hodnoty** v Dataverse, s prívlastkom **Vynechať synchronizáciu (iba na interné účely)** nastaveným na **False**. Táto hodnota atribútu je nastavená v Dataverse automaticky pri vytvorení záznamu. Príklady, kde je tento atribút nastavený na **True**, sú:

  - Skutočné náklady na projekt pre medzipodnikové transakcie. Viac informácií nájdete v časti [Vytvorte medzipodnikové transakcie](../project-accounting/create-intercompany-transactions.md). Tieto záznamy sa preskočia, pretože systém obnoví skutočné náklady projektu v aplikáciách Finance and Operations, keď sa zaúčtuje faktúra medzipodnikového dodávateľa.
  - Negatívne nevyfakturované záznamy o predaji vytvorené pri potvrdení proforma faktúry. Tieto záznamy sa preskočia, pretože vedľajšia kniha projektu sa nachádza v aplikáciách Finance and Operations a nezvráti nevyfakturovaný záznam o predaji pri fakturácii, ale zmení stav na úplne fakturovaný.

Mapa tabuľky s dvojitým zápisom synchronizuje záznamy skutočností s postupnou tabuľkou **ProjCDSActualsImport**. Tieto záznamy sú spracovávané periodickým procesom **Import z pracovnej tabuľky** pri vytváraní riadkov denníka integrácie Project Operations a riadkov návrhu faktúry projektu. Viac informácií nájdete v časti [Denník integrácie v Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse tiež zachytáva väzby medzi skutočnými transakciami projektu v entite **Kontaktná osoba pre transakciu**. Viac informácií nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](../actuals/linkingactuals.md). Synchronizujú sa aj odkazy medzi skutočnými aplikáciami Finance and Operations využitím mapy tabuľky dvojitého zápisu, **Entita integrácie pre transakčné vzťahy projektu (msdyn\_transactionconnections)**. Tieto záznamy sú spracovávané periodickým procesom **Import z pracovnej tabuľky** pri vytváraní riadkov denníka integrácie Project Operations a riadkov návrhu faktúry projektu.

Zaúčtovanie denníka integrácie projektových operácií a návrhu faktúry projektu spustí aktualizáciu v príslušných záznamoch v pracovnej tabuľke **ProjCDSActualsImport**. Systém zachytáva a zaznamenáva nasledujúce účtovné atribúty pre transakcie skutočností:

- Suma účtovnej meny
- Výmenný kurz
- Číslo kupónu
- Suma dane z predaja

Mapa tabuľky **Skutočné hodnoty integrácie Project Operations** aktualizuje príslušné záznamy skutočných hodnôt v Dataverse s touto informáciou.
