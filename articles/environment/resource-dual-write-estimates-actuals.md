---
title: Integrácia odhadov a skutočných hodnôt projektu
description: Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre odhady a skutočné hodnoty projektu.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577209"
---
# <a name="project-estimates-and-actuals-integration"></a>Integrácia odhadov a skutočných hodnôt projektu

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre odhady a skutočné hodnoty projektu.

## <a name="project-estimates"></a>Odhady projektu

Odhady projektovej práce, nákladov a materiálu sa vytvárajú a udržiavajú v Microsoft Dataverse a synchronizované s aplikáciami Finance and Operations na účely účtovníctva. Operácie vytvárania, aktualizácie a odstraňovania nie sú podporované prostredníctvom aplikácií Finance and Operations.

Vytvorenie odhadov si vyžaduje platnú konfiguráciu účtovníctva pre projekt. Projekty, ktoré sú spojené s riadkami zmluvy, musia mať platný profil nákladov a výnosov projektu definovaný v pravidlách profilu nákladov a výnosov projektu. Viac informácií nájdete v časti [Konfigurácia účtovníctva pre fakturovateľné projekty](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Odhady pracovnej sily

Odhady pracovnej sily vytvára projektový manažér alebo manažér zdrojov, ktorý tiež projektovej úlohe priradí všeobecný alebo pomenovaný zdroj. Záznamy o priradení zdrojov možno skontrolovať na karte **Priradenia zdrojov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy priradenia zdrojov v Dataverse vytvárať záznamy o predpovedi hodín v aplikáciách Finance and Operations pomocou **Integračná entita Project Operations pre odhady hodín (msdyn\_ priradenia zdrojov)**.

   ![Integrácia pracovných odhadov.](./Media/DW4LaborEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy o priradení prostriedkov do pracovnej tabuľky (**ProjCDSEstimateHoursImport**) a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy predpovedí hodín (**ProjForecastEmpl**).

Účtovník projektu kontroluje záznamy prognózovaných hodín vytvorené v aplikáciách Finance and Operations tak, že prejde na **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Hodinové predpovede**.

## <a name="expense-estimates"></a>Odhady nákladov

Odhady výdavkov vytvára projektový manažér na karte **Odhady výdavkov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy o odhade výdavkov sú uložené v entite **Riadok odhadu** v Dataverse. Tieto záznamy odhadov majú triedu transakcií, **Výdavok** a sú synchronizované so záznamami prognóz výdavkov v aplikáciách Finance and Operations **Subjekt integrácie projektových operácií pre odhady výdavkov (msdyn\_ odhady)**.

   ![Integrácia odhadov výdavkov.](./Media/DW4ExpenseEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy odhadov výdavkov do pracovnej tabuľky (**ProjCDSEstimateExpenseImport**) a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy o výdavkoch (**ProjForecastCost**). Odhady riadkov ukladajú odhady predaja a odhady nákladov osobitne. Obchodná logika v aplikáciách Finance and Operations vyplní jeden záznam prognózy výdavkov pomocou tohto detailu v tabuľke príprav.

Účtovník projektu môže skontrolovať záznamy prognózy výdavkov v aplikáciách Financie a operácie tak, že prejde na **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Prognózy výdavkov**.

## <a name="material-estimates"></a>Odhady materiálov

Odhady materiálov vytvára projektový manažér na karte **Odhady materiálov** na stránke **Podrobnosti o projekte** v Dataverse. Záznamy o odhade materiálov sú uložené v entite **Riadok odhadu** v Dataverse. Tieto záznamy odhadov majú triedu transakcií, **Materiál** a sú synchronizované so záznamami prognózy položiek v aplikáciách Finance and Operations **Tabuľka integrácie projektu pre odhady materiálu (msdyn\_ odhady)**.

   ![Integrácia odhadov materiálov.](./Media/DW4MaterialEstimates.png)

Funkcia duálneho zápisu synchronizuje záznamy odhadov materiálov do pracovnej tabuľky **ProjForecastSalesImpor** a potom pomocou obchodnej logiky vytvorí a aktualizuje záznamy o predpovede položky (**ForecastSales**). Odhady riadkov ukladajú odhady predaja a odhady nákladov osobitne. Obchodná logika v aplikáciách Finance and Operations vyplní jeden záznam prognózy položky pomocou tohto detailu v prípravnej tabuľke.

Účtovník projektu môže skontrolovať záznamy prognózy položiek v aplikáciách Financie a operácie tak, že prejde na **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Plán** > **Prognózy položiek**.

## <a name="project-actuals"></a>Skutočné hodnoty projektu

Skutočné hodnoty projektu sú vytvorené v Dataverse na základe času, výdavkov, materiálu a fakturačnej činnosti. V tejto entite Dataverse sú zachytené všetky prevádzkové atribúty týchto transakcií vrátane množstva, nákladovej ceny, predajnej ceny. Ďalšie informácie nájdete v časti [Skutočné hodnoty](../actuals/actuals-overview.md). Skutočné záznamy sa synchronizujú s aplikáciami Finance and Operations pomocou mapy s dvojitým zápisom **Aktuálne informácie o integrácii projektových operácií (msdyn\_ skutočné)** pre následné účtovníctvo.

   ![Integrácia skutočných hodnôt.](./Media/DW4Actuals.png)

Mapa tabuľky **Integrácia skutočných údajov Project Operations** synchronizuje všetky záznamy z entity **Skutočné hodnoty** v Dataverse, s prívlastkom **Vynechať synchronizáciu (iba na interné účely)** nastaveným na **False**. Táto hodnota atribútu je nastavená v Dataverse automaticky pri vytvorení záznamu. Príklady, kde je tento atribút nastavený na **True**, sú:

  - Skutočné náklady na projekt pre medzipodnikové transakcie. Viac informácií nájdete v časti [Vytvorte medzipodnikové transakcie](../project-accounting/create-intercompany-transactions.md). Tieto záznamy sa preskočia, pretože systém znovu vytvorí skutočné náklady projektu v aplikáciách Financie a operácie, keď sa zaúčtuje medzipodniková faktúra dodávateľa.
  - Negatívne nevyfakturované záznamy o predaji vytvorené pri potvrdení proforma faktúry. Tieto záznamy sa preskočia, pretože vedľajšia kniha projektu v aplikáciách Financie a prevádzka nevráti záznam o nevyfakturovanom predaji pri fakturácii, ale zmení stav na úplne vyfakturované.

Mapa tabuľky s dvojitým zápisom synchronizuje záznamy skutočností s postupnou tabuľkou **ProjCDSActualsImport**. Tieto záznamy sú spracovávané periodickým procesom **Import z pracovnej tabuľky** pri vytváraní riadkov denníka integrácie Project Operations a riadkov návrhu faktúry projektu. Viac informácií nájdete v časti [Denník integrácie v Project Operations](../project-accounting/project-operations-integration-journal.md).

Dataverse tiež zachytáva väzby medzi skutočnými transakciami projektu v entite **Kontaktná osoba pre transakciu**. Viac informácií nájdete v časti [Prepojenie skutočných hodnôt s pôvodnými záznamami](../actuals/linkingactuals.md). Prepojenia medzi skutočnými transakciami sú tiež synchronizované s aplikáciami Finance and Operations pomocou mapy s dvojitým zápisom, **Integračná entita pre transakčné vzťahy projektu (msdyn\_ transakčné pripojenia)**. Tieto záznamy sú spracovávané periodickým procesom **Import z pracovnej tabuľky** pri vytváraní riadkov denníka integrácie Project Operations a riadkov návrhu faktúry projektu.

Zaúčtovanie denníka integrácie projektových operácií a návrhu faktúry projektu spustí aktualizáciu v príslušných záznamoch v pracovnej tabuľke **ProjCDSActualsImport**. Systém zachytáva a zaznamenáva nasledujúce účtovné atribúty pre transakcie skutočností:

- Suma účtovnej meny
- Výmenný kurz
- Číslo kupónu
- Suma dane z predaja

Mapa tabuľky **Skutočné hodnoty integrácie Project Operations** aktualizuje príslušné záznamy skutočných hodnôt v Dataverse s touto informáciou.
