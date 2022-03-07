---
title: Synchronizujte kategórie výdavkov projektu medzi Finance and Operations a Project Service Automation
description: Táto téma popisuje šablóny a základné úlohu, ktoré sa používajú na synchronizáciu projektových kategórií výdavkov medzi Microsoft Dynamics 365 Finance a Dynamics 365 Project Service Automation.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 52c79f8b641d4b2df3b30964331633f2487402f8f8d229b540f9544c0f848557
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "7001135"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synchronizujte kategórie výdavkov projektu medzi Finance and Operations a Project Service Automation

[!include[banner](../includes/banner.md)]

Táto téma popisuje šablóny a základné úlohu, ktoré sa používajú na synchronizáciu projektových kategórií výdavkov medzi Dynamics 365 Finance a Dynamics 365 Project Service Automation.

> [!NOTE]
> - Integrácia projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií sú k dispozícii vo verzii 8.0.
> - Integrácia skutočných hodnôt je k dispozícii vo verzii 8.0.1 alebo novšej.
> - Ak používate Enterprise Edition 7.3.0, po inštalácii KB 4132657 a KB 4132660 budete môcť tieto šablóny použiť na integráciu projektových úloh, kategórií transakcií výdavkov, odhadov hodín, odhadov výdavkov a skutočných údajov a na nakonfigurovať blokovanie funkcií. Ak musíte resetovať účtovné prerozdelenie, odporúčame vám nainštalovať si aj KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Tok údajov pre Project Service Automation a Finance

Integračné riešenie Project Service Automation a služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Project Service Automation a Finance. Šablóna integrácie, ktorá je k dispozícii s funkciou integrácie údajov, umožňuje tok údajov o kategóriách transakcie projektových výdavkov medzi Finance a Project Service Automation.

Ak sú kategórie výdavkov projektu zvládnuté v aplikácii Finance, integračný tok ide najskôr od Finance do Project Service Automation. ID integrácie kategórií výdavkov projektu sa potom aktualizujú synchronizáciou z Project Service Automation do Finance.

Ak sú kategórie výdavkov projektu zvládnuté v Project Service Automation, integračný tok ide najskôr od Project Service Automation do Finance. Pred synchronizáciou z Project Service Automation musia byť kategórie projektov už nakonfigurované v aplikácii Finance. Následne sa synchronizujú z Finance späť do Project Service Automation a potom znova z Project Service Automation do Finance. Týmto spôsobom pomôžete zaručiť, že kategórie budú prepojené a že sa nevytvárajú duplikáty.

> [!NOTE]
> Kategórie projektových výdavkov sú zvyčajne zvládnuté vo Finance. Ak však nie sú, alebo ak už boli kategórie výdavkov vytvorené v Project Service Automation, musíte ich najskôr synchronizovať pomocou šablóny kategórií výdavkov projektu (PSA až Fin a Ops). Potom vykonajte synchronizáciu pomocou šablóny Kategórie výdavkov projektu (Fin and Ops to PSA). Potom by ste mali synchronizáciu z Project Service Automation do Finance spustiť ešte raz.
>
> Ak synchronizujete najskôr z Project Service Automation, pred spustením synchronizácie musia byť v službe Finance splnené nasledujúce požiadavky:
>
> - Zdieľaná kategória, ktorá sa zhoduje s kategóriou projektu, ktorá je nastavená v Project Service Automation, musí existovať a musí byť povolená pre **Projekt** aj **Výdavok**.
> - Pre každú právnickú entitu Finance s ktorou sa musí integrovať, musia existovať nasledujúce kategórie projektu:
>
>     - Existuje **Kategória projektu**. 
>     - **Použiť do výdavkov** je aktivované.
>     - **Aktívny v denníku** je aktivované.
>     - **Typ transakcie** je nastavený na **Výdavok**.

Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje medzi Project Service Automation a Finance.

[![Tok údajov pre integráciu Project Service Automation s Finance.](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synchronizujte kategórie výdavkov projektu medzi Finance a Project Service Automation

### <a name="template-and-task"></a>Šablóna a úloha

Šablónu nájdete v zozname centrum správcu Microsoft Power Apps, zvoľte možnosť **Projekty** a potom v pravom hornom rohu vyberte možnosť **Nový projekt**, kde si vyberiete verejné šablóny.

Nasledujúca šablóna a základná úloha sa používajú na synchronizáciu kategórií výdavkov z Finance do Project Service Automation:

- **Názov šablóny v časti Integrácia údajov:** Kategórie transakcie výdavkov projektu (Fin a Ops do PSA)
- **Názov úlohy v projekte:** Synchronizujte kategórie s PSA

### <a name="entity-set"></a>Nastavenie entity

| Finance                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integračná entita pre kategórie | Kategórie transakcií     |

### <a name="entity-flow"></a>Tok entity

Kategórie projektových výdavkov sa spravujú vo Finance a synchronizujú sa s Project Service Automation ako kategórie transakcií.

### <a name="power-query"></a>Power Query

Pri synchronizácii s Project Service Automation musíte na nastavenie typu fakturácie v kategórii transakcií použiť Microsoft Power Query for Excel. Šablóna Kategórie výdavkov projektu (Fin and Ops to PSA) poskytuje predvolený stĺpec a mapovanie. Ak vytvárate vlastnú šablónu, musíte pridať podmienený stĺpec v Power Query. Postupujte nasledovne.

1. Kliknutím na šípku otvoríte mapovanie úlohy kategórií výdavkov projektu v šablóne Kategórie transakcií výdavkov projektu (Fin a Ops do PSA).
2. Kliknite na prepojenie **Pokročilý dotaz a filtrovanie**, čím otvoríte Power Query.
2. Stlačte možnosť **Pridať podmienený stĺpec**.
3. Zadajte názov nového stĺpca, napríklad **BillingType**.
4. Zadajte nasledujúcu podmienku: **ak CATEGORYID sa nerovná null, potom 19235001, inak null**.
5. V stĺpci kliknite na možnosť **OK**.
6. Nezabudnite tento nový stĺpec namapovať na mapovacej stránke.

Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov. Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Finance do Project Service Automation.

[![Kategória výdavkov projektu na priradenie šablóny Project Service Automation.](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synchronizujte kategórie výdavkov projektu z Project Service Automation do Finance

### <a name="template-and-task"></a>Šablóna a úloha

Nasledujúca šablóna a základná úloha sa používajú na synchronizáciu kategórií výdavkov z Project Service Automation do Finance:

- **Názov šablóny v časti Integrácia údajov:** Kategórie transakcie výdavkov projektu (PSA do Fin a Ops)
- **Názov úlohy v projekte:** Synchronizujte kategórie do Fin Ops

### <a name="entity-set"></a>Nastavenie entity

| Project Service Automation | Financie                           |
|----------------------------|-----------------------------------|
| Kategórie transakcií     | Integračná entita pre kategórie |

### <a name="entity-flow"></a>Tok entity

Kategórie projektových výdavkov sa spravujú vo Finance a synchronizujú sa s Project Service Automation ako kategórie transakcií. Synchronizácia späť do Finance aktualizuje kategóriu projektu vo FInance s ID integrácie z Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Mapovanie šablón v integrácii údajov

Nasledujúca ilustrácia ukazuje príklad mapovania úlohy šablóny v Integrácii údajov.

> [!NOTE]
> Mapovanie zobrazuje informácie o poli, ktoré sa budú synchronizovať z Project Service Automation do Finance.

[![Priradenie šablóny Project Service Automation do Finance.](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]