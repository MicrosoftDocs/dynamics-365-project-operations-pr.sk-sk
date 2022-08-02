---
title: Integrácia odhadov a skutočných hodnôt projektu
description: Tento článok poskytuje informácie o integrácii duálneho zápisu Project Operations pre odhady a skutočnosti projektu.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029099"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrácia odhadov a skutočných hodnôt projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok poskytuje informácie o integrácii duálneho zápisu Project Operations pre odhady a skutočnosti projektu.

## <a name="project-estimates"></a>Odhady projektu

Odhady projektovej práce, nákladov a materiálu sa vytvárajú a udržiavajú v Microsoft Dataverse a synchronizované s finančnými a prevádzkovými aplikáciami na účely účtovníctva. Operácie vytvárania, aktualizácie a odstraňovania nie sú podporované prostredníctvom aplikácií pre financie a operácie.

Vytvorenie odhadov si vyžaduje platnú konfiguráciu účtovníctva pre projekt. Projekty, ktoré sú spojené s riadkami zmluvy, musia mať platný profil nákladov a výnosov projektu definovaný v pravidlách profilu nákladov a výnosov projektu. Viac informácií nájdete v časti [Konfigurácia účtovníctva pre fakturovateľné projekty](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Odhady pracovnej sily

Odhady pracovnej sily vytvára projektový manažér alebo manažér zdrojov, ktorý tiež projektovej úlohe priradí všeobecný alebo pomenovaný zdroj. Záznamy o priradení zdrojov možno skontrolovať na karte **Priradenia zdrojov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy priradenia zdrojov v Dataverse vytvárať záznamy o predpovedi hodín vo finančných a prevádzkových aplikáciách pomocou **Integračná entita Project Operations pre odhady hodín (msdyn\_ priradenia zdrojov)**.

   ![Integrácia pracovných odhadov.](./Media/DW4LaborEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy o priradení prostriedkov do pracovnej tabuľky (**ProjCDSEstimateHoursImport**) a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy predpovedí hodín (**ProjForecastEmpl**).

Účtovník projektu kontroluje záznamy prognózovaných hodín vytvorené vo finančných a prevádzkových aplikáciách tak, že prejde na **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Hodinové predpovede**.

## <a name="expense-estimates"></a>Odhady nákladov

Odhady výdavkov vytvára projektový manažér na karte **Odhady výdavkov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy o odhade výdavkov sú uložené v entite **Riadok odhadu** v Dataverse. Tieto záznamy odhadov majú triedu transakcií, **Výdavok** a sú synchronizované so záznamami prognóz výdavkov vo finančných a prevádzkových aplikáciách, ktoré používajú **Subjekt integrácie projektových operácií pre odhady výdavkov (msdyn\_ odhady)**.

   ![Integrácia odhadov výdavkov.](./Media/DW4ExpenseEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy odhadov výdavkov do pracovnej tabuľky (**ProjCDSEstimateExpenseImport**) a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy o výdavkoch (**ProjForecastCost**). Odhady riadkov ukladajú odhady predaja a odhady nákladov osobitne. Obchodná logika v aplikáciách pre financie a operácie vyplní jeden záznam prognózy výdavkov pomocou tohto detailu v prípravnej tabuľke.

Účtovník projektu môže skontrolovať záznamy prognóz výdavkov vo finančných a prevádzkových aplikáciách tak, že prejde na **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Prognózy výdavkov**.

## <a name="material-estimates"></a>Odhady materiálov

Odhady materiálov vytvára projektový manažér na karte **Odhady materiálov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy o odhade materiálov sú uložené v entite **Riadok odhadu** v Dataverse. Tieto záznamy odhadov majú triedu transakcií, **Materiál** a sú synchronizované so záznamami prognózy položiek vo finančných a prevádzkových aplikáciách, ktoré používajú **Tabuľka integrácie projektu pre odhady materiálu (msdyn\_ odhady)**.

   ![Integrácia odhadov materiálov.](./Media/DW4MaterialEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy odhadov materiálov do pracovnej tabuľky **ProjForecastSalesImpor** a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy o predpovede položky (**ForecastSales**). Odhady riadkov ukladajú odhady predaja a odhady nákladov osobitne. Obchodná logika v aplikáciách pre financie a operácie vyplní jeden záznam prognózy položky pomocou tohto detailu v prípravnej tabuľke.

Účtovník projektu môže skontrolovať záznamy prognózy položiek vo finančných a prevádzkových aplikáciách tak, že prejde na **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Prognózy položiek**.

## <a name="project-actuals"></a>Skutočné hodnoty projektu

Skutočné hodnoty projektu sú vytvorené v Dataverse na základe času, výdavkov, materiálu a fakturačnej činnosti. V tejto entite Dataverse sú zachytené všetky prevádzkové atribúty týchto transakcií vrátane množstva, nákladovej ceny, predajnej ceny. Ďalšie informácie nájdete v časti [Skutočné hodnoty](../actuals/actuals-overview.md). Aktuálne záznamy sa synchronizujú s finančnými a prevádzkovými aplikáciami pomocou mapy s dvojitým zápisom **Aktuálne informácie o integrácii projektových operácií (msdyn\_ skutočné)** pre následné účtovníctvo.

   ![Integrácia skutočných hodnôt.](./Media/DW4Actuals.png)

Mapa tabuľky **Integrácia skutočných údajov Project Operations** synchronizuje všetky záznamy z entity **Skutočné hodnoty** v Dataverse, s prívlastkom **Vynechať synchronizáciu (iba na interné účely)** nastaveným na **False**. Táto hodnota atribútu je nastavená v Dataverse automaticky pri vytvorení záznamu. Príklady, kde je tento atribút nastavený na **True**, sú:

  - Skutočné náklady na projekt pre medzipodnikové transakcie. Viac informácií nájdete v časti [Vytvorte medzipodnikové transakcie](../project-accounting/create-intercompany-transactions.md). Tieto záznamy sa preskočia, pretože systém znovu vytvorí skutočné náklady projektu vo finančných a prevádzkových aplikáciách pri zaúčtovaní medzipodnikovej faktúry dodávateľa.
  - Negatívne nevyfakturované záznamy o predaji vytvorené pri potvrdení proforma faktúry. Tieto záznamy sa preskočia, pretože vedľajšia kniha projektu v aplikáciách pre financie a prevádzku nestornuje záznam o nevyfakturovaných predajoch pri fakturácii, ale zmení stav na plne fakturované.

Mapa tabuľky s dvojitým zápisom synchronizuje záznamy skutočností s postupnou tabuľkou **ProjCDSActualsImport**. Tieto záznamy sú spracovávané periodickým procesom **Import z pracovnej tabuľky** pri vytváraní riadkov denníka integrácie Project Operations a riadkov návrhu faktúry projektu. Viac informácií nájdete v časti [Denník integrácie v Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse tiež zachytáva väzby medzi skutočnými transakciami projektu v entite **Kontaktná osoba pre transakciu**. Viac informácií nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](../actuals/linkingactuals.md). Prepojenia medzi skutočnými transakciami sú tiež synchronizované s finančnými a prevádzkovými aplikáciami pomocou mapy s dvojitým zápisom, **Integračná entita pre transakčné vzťahy projektu (msdyn\_ transakčné pripojenia)**. Tieto záznamy sú spracovávané periodickým procesom **Import z pracovnej tabuľky** pri vytváraní riadkov denníka integrácie Project Operations a riadkov návrhu faktúry projektu.

Zaúčtovanie denníka integrácie projektových operácií a návrhu faktúry projektu spustí aktualizáciu v príslušných záznamoch v pracovnej tabuľke **ProjCDSActualsImport**. Systém zachytáva a zaznamenáva nasledujúce účtovné atribúty pre transakcie skutočností:

- Suma účtovnej meny
- Výmenný kurz
- Číslo kupónu
- Suma dane z predaja

Mapa tabuľky **Skutočné hodnoty integrácie Project Operations** aktualizuje príslušné záznamy skutočných hodnôt v Dataverse s touto informáciou.
