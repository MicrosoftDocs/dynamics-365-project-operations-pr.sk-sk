---
title: Integrácia nastavenia a konfiguračných údajov aplikácie Project Operations
description: Táto téma poskytuje informácie o nastavení a konfigurácii máp duálneho zápisu pre Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986555"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integrácia nastavenia a konfiguračných údajov aplikácie Project Operations

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre entity nastavenia a konfigurácie.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektové zmluvy, riadky zmluvy a projekty

Projektové zmluvy, riadky zmlúv a projekty sa vytvárajú v Dataverse a synchronizované s aplikáciami Finance and Operations pre ďalšie účtovníctvo. Záznamy v týchto entitách je možné vytvárať a mazať iba v Dataverse. K týmto záznamom však možno pridať účtovné atribúty, ako sú predvolené hodnoty skupiny dane z obratu a finančné dimenzie v aplikácie Finance and Operations.

  ![Koncepty projektovej integráciu zmluvy.](./media/1ProjectContract.jpg)

Sledujú sa potenciáli predaja, príležitosti a ponuky Dataverse a nesynchronizovať s aplikáciami Finance and Operations, pretože s touto aktivitou nie je spojené žiadne následné účtovníctvo.

Funkčnosť projektovej zmluvy v Dataverse vytvára záznam zmluvy o projekte v aplikáciách Finance and Operations použitím tabuľkovej mapy **Hlavičky kontraktov projektu (objednávky)**. Ukladanie projektovej zmluvy v Dataverse tiež začína vytváranie záznamu zákazkovej entity zákazky projektu. Tento záznam je synchronizovaný s aplikáciami Finance and Operations pomocou tabuľkovej mapy **Zdroj financovania projektu (msdyn\_projectcontractssplitbillingrules)**. Táto mapa tiež synchronizuje dodatky, aktualizácie a odstránenia zákazníkov zo zmluvy o projekte. Rozdelené fakturačné percentá medzi zákazníkov so zmluvami na projekty sú zvládnuté iba v Dataverse a nie sú synchronizované s aplikáciami Finance and Operations.

Po vytvorení projektovej zmluvy v Dataverse, účtovník projektu môže aktualizovať účtovné atribúty pre túto zmluvu o projekte v aplikáciách Finance and Operations v **Projektové riadenie a účtovníctvo** > **Zmluvy o projekte** > **Príprava** > **Zobraziť predvolené účtovníctvo**. Účtovník môže skontrolovať funkčné atribúty zmluvy o projekte, ako je požadovaný dátum dodania a výška zmluvy, výberom ID zmluvy o projekte v aplikáciách Finance and Operations, ktoré otvárajú súvisiaci záznam zmluvy o projekte v Dataverse.

Entita projektu je synchronizovaná s aplikáciami Finance and Operations pomocou tabuľkovej mapy **Projects V2 (msdyn\_projects)**. Účtovník projektu môže:

  - Skontrolujte projekty v aplikáciách Finance and Operations prechodom do ponuky **Projektový manažment a účtovníctvo** > **Všetky projekty**. 
  - Aktualizujte účtovné atribúty projektu v aplikáciách Finance and Operations prechodom do ponuky **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Nastaviť** > **Zobraziť predvolené účtovníctvo**.  
  - Skontrolujte operačné atribúty projektu, napríklad odhadované dátumy začiatku a konca, výberom ID projektu v aplikáciách Finance and Operations, ktoré otvárajú súvisiaci záznam projektu v Dataverse.

Projekt je spojený so zmluvou o projekte prostredníctvom entity **Riadok projektovej zmluvy**.

Riadky projektovej zmluvy v Dataverse vytvárajú pravidlo fakturácie zmluvy o projekte v aplikáciách Finance and Operations použitím tabuľkovej mapy **Riadky zmluvy projektu (salesorderdetails)**. Metóda fakturácie definuje typ pravidla fakturácie zmluvy o projekte v aplikáciách Finance and Operations:

  - Riadky projektovej zmluvy s metódou fakturácie za čas a materiál vytvárajú pravidlo fakturácie za čas a typ materiálu.
  - Riadky kontraktu s metódou fakturácie za pevnú cenu vytvárajú pravidlo fakturácie míľnikov.

Riadky projektovej zmluvy môžu byť skontrolované účtovníkom projektu v aplikáciách Finance and Operations prechodom do ponuky **Projektový manažment a účtovníctvo** > **Zmluvy o projekte** > **Nastaviť** > **Zobraziť predvolené účtovníctvo** a preskúmaním karty **Riadky zmluvy**. Účtovník môže tiež na tejto karte nastaviť predvolené finančné dimenzie pre riadky zmluvy s metódou fakturácie za pevnú cenu.

## <a name="billing-milestones"></a>Míľniky fakturácie

Riadky kontraktov projektu využívajúce metódu fakturácie s pevnou cenou sa fakturujú prostredníctvom čiastkových cieľov fakturácie. Míľniky fakturácie sa synchronizujú s projektom transakcií na účte v aplikáciách Finance and Operations pomocou tabuľkovej mapy **Míľniky riadkov zmluvy integrácie Project Operations (msdyn\_contractlinescheduleofvalues)**.

  ![Integrácie medzníkov fakturácie.](./media/2Milestones.jpg)

Účtovník môže skontrolovať transakcie na účte a upraviť účtovné atribúty pre tieto transakcie tak, že prejde na **Projektový manažment a účtovníctvo** > **Zmluvy o projekte** > **Zachovať** > **Transakcie na účte** alebo **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Zachovať** > **Transakcie na účte**.

Keď prvýkrát vytvoríte míľnik fakturácie pre daný riadok zmluvy projektu, systém automaticky vytvorí projekt odhadu výnosov z pevnej ceny pre projekt spojený s týmto riadkom zmluvy. Projekty odhadu výnosov za pevnú cenu môžete skontrolovať v časti **Projektový manažment a účtovníctvo** > **Projekty odhadov výnosov s pevnou cenou**.

### <a name="project-tasks"></a>Projektové úlohy

Úlohy projektu sa synchronizujú do aplikácií Finance and Operations prostredníctvom tabuľkovej mapy **Projektové úlohy (msdyn\_projecttasks)** iba na informačné účely. Vytvorenie, aktualizácia a odstránenie operácií nie je podporované cez aplikácie Finance and Operations.

  ![Integrácia projektových úloh.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektové zdroje

Entita **Roly projektových zdrojov** je synchronizovaná s aplikáciami Finance and Operations pomocou tabuľkovej mapy **Roly projektových zdrojov pre všetky spoločnosti (bookableresourcecategories)** iba na informačné účely. Pretože roly zdrojov v Dataverse nie sú špecifické pre spoločnosť, systém v nich automaticky vytvára príslušné záznamy o rolách zdrojov špecifických pre spoločnosť v aplikáciách Finance and Operations automaticky pre všetky právnické osoby zahrnuté do rozsahu integrácie duálneho zápisu.

![Integrácia rol zdrojov.](./media/5Resources.jpg)

Zdroje projektu v časti Project Operations sú udržiavané v Dataverse a nie sú synchronizované s aplikáciami Finance and Operations.

### <a name="transaction-categories"></a>Kategórie transakcií

Transakčné kategórie sa udržiavajú v Dataverse a synchronizované s aplikáciami Finance and Operations použitím tabuľkovej mapy **Kategórie transakcií projektu (msdyn\_transactioncategories)**. Po synchronizácii záznamu kategórie transakcií systém automaticky vytvorí štyri záznamy zdieľaných kategórií. Každý záznam zodpovedá typu transakcie v aplikáciách Finance and Operations a prepojí ich so záznamom kategórie transakcií.

![Integrácia kategórií transakcií.](./media/4TransactionCategories.jpg)

Použitie kategórií transakcií na účely odhadov a skutočností vyžaduje, aby účtovník projektu alebo správca systému vytvoril zodpovedajúce kategórie projektu v každej právnickej osobe. Viac informácií nájdete v časti [Konfigurácia projektových kategórií](../project-accounting/configure-project-categories.md).
