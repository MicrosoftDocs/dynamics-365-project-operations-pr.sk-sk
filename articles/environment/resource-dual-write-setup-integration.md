---
title: Integrácia nastavenia a konfiguračných údajov aplikácie Project Operations
description: Táto téma poskytuje informácie o nastavení a konfigurácii máp duálneho zápisu pre Project Operations.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586915"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>Integrácia nastavenia a konfiguračných údajov aplikácie Project Operations

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie o integrácii duálneho zápisu Project Operations pre entity nastavenia a konfigurácie.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektové zmluvy, riadky zmluvy a projekty

Projektové zmluvy, zmluvné línie a projekty sa vytvárajú v Dataverse a synchronizované s aplikáciami Finance and Operations pre ďalšie účtovníctvo. Záznamy v týchto entitách je možné vytvárať a mazať iba v Dataverse. Účtovné atribúty, ako sú predvolené hodnoty skupiny dane z predaja a finančné dimenzie, však možno pridať do týchto záznamov v aplikáciách Financie a operácie.

  ![Koncepty projektovej integráciu zmluvy.](./media/1ProjectContract.jpg)

V rámci predajnej aktivity sa sledujú potenciálni zákazníci, príležitosti a cenové ponuky Dataverse a nesynchronizujte sa s aplikáciami Finance and Operations, pretože s touto aktivitou nie je spojené žiadne následné účtovníctvo.

Funkčnosť projektovej zmluvy v Dataverse vytvorí záznam projektovej zmluvy v aplikáciách Finance and Operations pomocou **Hlavičky projektových zmlúv (predajcovia)** tabuľková mapa. Ukladanie projektovej zmluvy v Dataverse tiež začína vytváranie záznamu zákazkovej entity zákazky projektu. Tento záznam je synchronizovaný s aplikáciami Finance and Operations pomocou **Zdroj financovania projektu (msdyn\_ pravidlá rozdelenia projektových zmlúv)** tabuľková mapa. Táto mapa tiež synchronizuje dodatky, aktualizácie a odstránenia zákazníkov zo zmluvy o projekte. Percentá delenia fakturácie medzi zmluvných zákazníkov projektu sú zvládnuté iba v Dataverse a nie sú synchronizované s aplikáciami Finance and Operations.

Po vytvorení projektovej zmluvy v Dataverse, môže účtovník projektu aktualizovať atribúty účtovania pre túto projektovú zmluvu v aplikáciách Financie a operácie tak, že prejde na **Projektový manažment a účtovníctvo** > **Projektové zmluvy** > **Nastaviť** > **Zobraziť predvolené účtovníctvo**. Účtovník môže skontrolovať atribúty zmluvy o prevádzkovom projekte, ako je požadovaný dátum dodania a suma zmluvy, výberom ID projektovej zmluvy v aplikáciách Finance and Operations, čím sa otvorí súvisiaci záznam zmluvy o projekte v Dataverse.

Entita projektu je synchronizovaná s aplikáciami Finance and Operations pomocou **Projekty V2 (msdyn\_ projekty)** tabuľková mapa. Účtovník projektu môže:

  - Prezrite si projekty v aplikáciách Finance and Operations na **Projektový manažment a účtovníctvo** > **Všetky projekty**. 
  - Aktualizujte účtovné atribúty pre projekt v aplikáciách Finance and Operations tak, že prejdete na **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Nastaviť** > **Zobraziť predvolené účtovníctvo**.  
  - Skontrolujte atribúty prevádzkového projektu, ako sú odhadované dátumy začiatku a ukončenia, výberom ID projektu v aplikáciách Finance and Operations, čím sa otvorí súvisiaci záznam projektu v Dataverse.

Projekt je spojený so zmluvou o projekte prostredníctvom entity **Riadok projektovej zmluvy**.

Linky projektovej zmluvy v Dataverse vytvorí pravidlo fakturácie projektovej zmluvy v aplikáciách Finance and Operations pomocou **Linky projektových zmlúv (podrobnosti o predajnej objednávke)** tabuľková mapa. Spôsob fakturácie definuje typ pravidla fakturácie projektovej zmluvy v aplikáciách Finance and Operations:

  - Riadky projektovej zmluvy s metódou fakturácie za čas a materiál vytvárajú pravidlo fakturácie za čas a typ materiálu.
  - Riadky kontraktu s metódou fakturácie za pevnú cenu vytvárajú pravidlo fakturácie míľnikov.

Riadky projektovej zmluvy si môže účtovník projektu pozrieť v aplikáciách Financie a operácie na adrese **Projektový manažment a účtovníctvo** > **Projektové zmluvy** > **Nastaviť** > **Zobraziť predvolené účtovníctvo** a kontrolu podrobností na stránke **Zmluvné linky** tab. Účtovník môže na tejto karte nastaviť aj predvolené finančné dimenzie pre riadky zmluvy o spôsobe účtovania s pevnou cenou.

## <a name="billing-milestones"></a>Míľniky fakturácie

Riadky kontraktov projektu využívajúce metódu fakturácie s pevnou cenou sa fakturujú prostredníctvom čiastkových cieľov fakturácie. Fakturačné míľniky sa synchronizujú s projektovými transakciami na účte v aplikáciách Finance and Operations pomocou **Míľniky zmluvy o integrácii projektových operácií (msdyn\_ zmluvný plán hodnôt)** tabuľková mapa.

  ![Integrácie medzníkov fakturácie.](./media/2Milestones.jpg)

Účtovník môže skontrolovať transakcie na účte a upraviť účtovné atribúty pre tieto transakcie tak, že prejde na **Projektový manažment a účtovníctvo** > **Zmluvy o projekte** > **Zachovať** > **Transakcie na účte** alebo **Projektový manažment a účtovníctvo** > **Všetky projekty** > **Zachovať** > **Transakcie na účte**.

Keď prvýkrát vytvoríte míľnik fakturácie pre daný riadok zmluvy projektu, systém automaticky vytvorí projekt odhadu výnosov z pevnej ceny pre projekt spojený s týmto riadkom zmluvy. Projekty odhadu výnosov za pevnú cenu môžete skontrolovať v časti **Projektový manažment a účtovníctvo** > **Projekty odhadov výnosov s pevnou cenou**.

### <a name="project-tasks"></a>Projektové úlohy

Projektové úlohy sú synchronizované s aplikáciami Finance and Operations cez **Projektové úlohy (msdyn\_ projektové úlohy)** tabuľková mapa len na referenčné účely. Vytváranie, aktualizácia a odstraňovanie operácií nie je podporované prostredníctvom aplikácií Finance and Operations.

  ![Integrácia projektových úloh.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektové zdroje

The **Roly projektových zdrojov** entita je synchronizovaná s aplikáciami Finance and Operations pomocou **Roly projektových zdrojov pre všetky spoločnosti (kategórie bookableresourcecategories)** tabuľková mapa len na referenčné účely. Pretože roly zdrojov v Dataverse nie sú špecifické pre spoločnosť, systém automaticky vytvára príslušné záznamy rolí zdrojov špecifických pre spoločnosť v aplikáciách Finance and Operations automaticky pre všetky právnické osoby zahrnuté do rozsahu integrácie s duálnym zápisom.

![Integrácia rol zdrojov.](./media/5Resources.jpg)

Projektové zdroje v Projektových operáciách sú udržiavané v Dataverse a nie sú synchronizované s aplikáciami Finance and Operations.

### <a name="transaction-categories"></a>Kategórie transakcií

Kategórie transakcií sú udržiavané v Dataverse a synchronizované s aplikáciami Finance and Operations pomocou **Kategórie projektových transakcií (msdyn\_ kategórie transakcií)** tabuľková mapa. Po synchronizácii záznamu kategórie transakcií systém automaticky vytvorí štyri záznamy zdieľaných kategórií. Každý záznam zodpovedá typu transakcie v aplikáciách Finance and Operations a spája ich so záznamom kategórie transakcie.

![Integrácia kategórií transakcií.](./media/4TransactionCategories.jpg)

Použitie kategórií transakcií na účely odhadov a skutočností vyžaduje, aby účtovník projektu alebo správca systému vytvoril zodpovedajúce kategórie projektu v každej právnickej osobe. Viac informácií nájdete v časti [Konfigurácia projektových kategórií](../project-accounting/configure-project-categories.md).
