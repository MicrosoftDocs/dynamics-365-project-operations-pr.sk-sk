---
title: Synchronizujte odhady projektov priamo z Project Service Automation s financiami a prevádzkou
description: Tento článok popisuje šablóny a základné úlohy, ktoré sa používajú na synchronizáciu odhadov hodín projektu a odhadov nákladov na projekt priamo z nich Microsoft Dynamics 365 Project Service Automation do Dynamics 365 Finance.
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
ms.openlocfilehash: 2a71a2a7ca0c9179ddd5667364d8b5c9e413b917
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029824"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synchronizujte odhady projektov priamo z Project Service Automation s financiami a prevádzkou

[!include[banner](../includes/banner.md)]

Tento článok popisuje šablóny a základné úlohy, ktoré sa používajú na synchronizáciu odhadov hodín projektu a odhadov nákladov na projekt priamo z nich Dynamics 365 Project Service Automation na Dynamics 365 Finance.

> [!NOTE]
> - Integrácia projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií sú k dispozícii vo verzii 8.0.
> - Integrácia skutočných hodnôt je k dispozícii vo verzii 8.0.1 alebo novšej.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Tok údajov pre Project Service Automation do Finance

Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance. Šablóna integrácie, ktorá je k dispozícii s funkciou integrácie údajov, umožňuje tok údajov o kategóriách transakcie projektových odhadov hodín a projektových odhadov výdavkov z Project Service Automation do Finance.

Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.

[![Tok údajov pre integráciu Project Service Automation s Finance.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Odhady hodín projektu

### <a name="template-and-tasks"></a>Šablóna a úlohy

Dostupné šablóny nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt**, kde si vyberiete verejné šablóny.

Nasledujúca šablóna a základné úlohy sa používajú na synchronizáciu odhadov hodín z Project Service Automation do Finance:

- **Názov šablóny v časti Integrácia údajov:** Odhady hodín projektu (PSA do Fin a Ops)
- **Názov úloh v projekte:**

    - Vzťahy transakcie
    - Odhady nákladov

### <a name="entity-set"></a>Nastavenie entity

| Project Service Automation | Financie                                       |
|----------------------------|-----------------------------------------------|
| Projektové úlohy              | Entita integrácie pre odhady hodín projektu |

### <a name="entity-flow"></a>Tok entity

Projektové odhady hodín sa spravujú v Project Service Automation a synchronizujú s Finance ako prognózy hodín.

### <a name="prerequisites"></a>Predpoklady

Predtým, ako môže dôjsť k synchronizácii odhadov hodín projektu, musíte synchronizovať projekty, projektové úlohy a kategórie transakcií výdavkov na projekt.

### <a name="power-query"></a>Power Query

V šablóne odhadov hodín projektu musíte použiť Microsoft Power Query aby Excel dokončil tieto úlohy:

- Nastavte predvolené ID modelu predpovede, ktoré sa použije, keď integrácia vytvorí nové predpovede hodín.
- Odfiltrujte všetky záznamy týkajúce sa konkrétnych zdrojov v úlohe, ktoré zlyhajú pri integrácii, do hodinových predpovedí.
- Odfiltrujte všetky prázdne riadky kategórií transakcií. Nedokončenie tejto úlohy môže mať za následok nesprávnu predpoveď hodín.

#### <a name="set-the-default-forecast-model-id"></a>Nastavte predvolené ID modelu prognózy

Ak chcete aktualizovať predvolené ID modelu prognózy v šablóne, kliknite na šípku **Mapovať** na otvorenie mapovania. Potom stlačte odkaz **Pokročilý dotaz a filtrovanie**.

- Ak používate predvolenú šablónu Odhady hodín projektu (PSA po Fin a Ops) stlačte ikonu **Vložený stav** v zozname **Uplatnené kroky**. V zázname **Funkcia** nahraďte **O\_forecast** za názov ID modelu predpovede, ktoré sa musí použiť pri integrácii. Predvolená šablóna obsahuje ID modelu prognózy z ukážkových údajov.
- Ak vytvárate novú šablónu, musíte pridať tento stĺpec. In Power Query, vyberte **Pridať podmienený stĺpec** a zadajte názov nového stĺpca, ako napr **ID modelu**. Zadajte podmienku pre stĺpec, kde, ak projektová úloha nemá hodnotu null, potom \<enter the forecast model ID\>; inak null.

#### <a name="filter-out-resource-specific-records"></a>Odfiltrujte záznamy týkajúce sa konkrétnych zdrojov

Šablóna Odhady hodín projektu (PSA pre Fin a Ops) má predvolený filter, ktorý odstráni všetky záznamy špecifické pre daný zdroj. Ak vytvárate vlastnú šablónu, musíte pridať tento filter. Vyberte prepojenie **Pokročilý dotaz a filtrovanie** na filtrovanie v stĺpci **msdyn\_islinetask** tak, že sa zahrnú iba záznamy s príznakom **False**.

#### <a name="filter-out-empty-transaction-category-rows"></a>Odfiltrujte všetky prázdne riadky kategórií transakcií

Ak chcete odstrániť všetky riadky, ktoré majú prázdne kategórie transakcií, musíte pridať filter. Táto úloha je povinná bez ohľadu na to, či používate predvolenú šablónu alebo si vytvoríte vlastnú šablónu. Tento filter odstráni všetky súhrnné riadky z Project Service Automation, ktoré by mohli spôsobiť, že hodinové predpovede v aplikácii Finance budú nesprávne. Stlačte možnosť **Pokročilý dotaz a filtrovanie** na odfiltrovanie záznamov s príznakom null v stĺpci **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Mapovanie šablón v integrácii údajov

Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov. Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.

[![Mapovanie šablón úlohy v integrácii údajov.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Odhady projektových výdavkov

### <a name="template-and-tasks"></a>Šablóna a úlohy

Nasledujúca šablóna a základné úlohy sa používajú na synchronizáciu odhadov výdavkov z Project Service Automation do Finance:

- **Názov šablóny v časti Integrácia údajov:** Projektové odhady výdavkov (PSA do Fin a Ops)
- **Názov úloh v projekte:**

    - Vzťahy transakcie 
    - Odhady nákladov

### <a name="entity-set"></a>Nastavenie entity

| Project Service Automation | Financie                                                  |
|----------------------------|----------------------------------------------------------|
| Kontaktné osoby pre transakcie    | Integračná entita pre transakčné vzťahy projektu |
| Riadky odhadov             | Entita integrácie pre odhady projektových výdavkov         |

### <a name="entity-flow"></a>Tok entity

Projektové odhady výdavkov sa spravujú v Project Service Automation a synchronizujú s Finance ako prognózy výdavkov.

### <a name="prerequisites"></a>Predpoklady

Predtým, ako môže dôjsť k synchronizácii odhadov výdavkov projektu, musíte synchronizovať projekty, projektové úlohy a kategórie transakcií výdavkov na projekt.

### <a name="power-query"></a>Power Query

V šablóne odhadov výdavkov na projekt musíte použiť Power Query dokončiť nasledujúce úlohy:

- Filtrujte tak, aby boli zahrnuté iba riadkové záznamy odhadu výdavkov.
- Nastavte predvolené ID modelu predpovede, ktoré sa použije, keď integrácia vytvorí nové predpovede hodín.
- Transformujte typy fakturácie.
- Transformujte typy transakcií.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrujte tak, aby boli zahrnuté iba riadky odhadov výdavkov

Šablóna Odhady výdavkov projektu (PSA na Fin a Ops) má predvolený filter, ktorý v integrácii obsahuje iba riadky výdavkov. Ak vytvárate vlastnú šablónu, musíte pridať tento filter. Zvoľte úlohu **Transakčné vzťahy** a potom kliknite na šípku **Mapovať** na otvorenie mapovania. Stlačte odkaz **Pokročilý dotaz a filtrovanie**. Filtrujte stĺpec **msdyn\_transactiontype1** tak, aby obsahoval iba **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Nastavte predvolené ID modelu prognózy

Ak chcete aktualizovať predvolené ID modelu prognózy v šablóne, kliknite na úlohu **Odhady výdavkov** a potom kliknutím na šípku **Mapovať** otvorte mapovanie. Stlačte odkaz **Pokročilý dotaz a filtrovanie**.

- Ak používate predvolenú šablónu odhadov výdavkov na projekt (PSA to Fin and Ops), v Power Query, vyberte prvú **Vložená podmienka** z **Aplikované kroky** oddiele. V zázname **Funkcia** nahraďte **O\_forecast** za názov ID modelu predpovede, ktoré sa musí použiť pri integrácii. Predvolená šablóna obsahuje ID modelu prognózy z ukážkových údajov.
- Ak vytvárate novú šablónu, musíte pridať tento stĺpec. In Power Query, vyberte **Pridať podmienený stĺpec** a zadajte názov nového stĺpca, ako napr **ID modelu**. Zadajte podmienku pre stĺpec, kde, ak ID riadku odhadu nemá hodnotu null, potom \<enter the forecast model ID\>; inak null.

#### <a name="transform-the-billing-types"></a>Transformujte typy fakturácie

Šablóna Odhady výdavkov na projekt (PSA do Fin a Ops) obsahuje podmienený stĺpec, ktorý sa používa na transformáciu typov fakturácie, ktoré sa prijímajú z Project Service Automation počas integrácie. Ak vytvárate vlastnú šablónu, musíte pridať tento podmienený stĺpec. Stlačte prepojenie **Pokročilý dopyt a filtrovanie** a potom vyberte **Pridať podmienený stĺpec**. Zadajte názov nového stĺpca, napríklad **BillingType**. Potom zadajte nasledujúcu podmienku:

Ak **msdyn\_billingtype** = 192350000, potom **NonChargeable**  
alebo ak **msdyn\_billingtype** = 192350001, potom **Chargeable**  
alebo ak **msdyn\_billingtype** = 192350002, potom **Complimentary**  
Inak **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformujte typy transakcií

Šablóna Odhady výdavkov na projekt (PSA do Fin a Ops) obsahuje podmienený stĺpec, ktorý sa používa na transformáciu typov transakcie, ktoré sa prijímajú z Project Service Automation počas integrácie. Ak vytvárate vlastnú šablónu, musíte pridať tento podmienený stĺpec. Stlačte prepojenie **Pokročilý dopyt a filtrovanie** a potom vyberte **Pridať podmienený stĺpec**. Zadajte názov nového stĺpca, napríklad **TransactionType**. Potom zadajte nasledujúcu podmienku:

Ak **msdyn\_transactiontypecode** = 192350000, potom **Cost**  
alebo ak **msdyn\_transactiontypecode** = 192350005, potom **Sales**  
Inak **null**

### <a name="template-mapping-in-data-integration"></a>Mapovanie šablón v integrácii údajov

Nasledujúca ilustrácia ukazuje príklady mapovania úlohy šablóny v Integrácii údajov. Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.

[![Mapovanie šablón transakcií s odhadom výdavkov.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Mapovanie šablón odhadov výdavkov.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]