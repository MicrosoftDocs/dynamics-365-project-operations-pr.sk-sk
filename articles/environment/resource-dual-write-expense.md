---
title: Integrácia správy výdavkov
description: Tento článok poskytuje informácie o integrácii výkazu výdavkov v projektových operáciách pomocou duálneho zápisu.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64c318dc1915a9a87b6ae3c6b8a2aa6d3c9cd36
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8924633"
---
# <a name="expense-management-integration"></a>Integrácia správy výdavkov

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Tento článok poskytuje informácie o integrácii výkazov výdavkov v prevádzke projektu [plné nasadenie nákladov](../expense/expense-overview.md) pomocou duálneho zápisu.

## <a name="expense-categories"></a>Kategórie výdavkov

Pri úplnom nasadení nákladov sa kategórie výdavkov vytvárajú a udržiavajú v aplikáciách Finance and Operations. Ak chcete vytvoriť novú kategóriu výdavkov, postupujte takto:

1. V Microsoft Dataverse vytvorte kategóriu **Transakcia**. Integrácia s duálnym zápisom zosynchronizuje túto kategóriu transakcií s aplikáciami Finance and Operations. Viac informácií nájdete v časti [Konfigurácia kategórií projektov](/dynamics365/project-operations/project-accounting/configure-project-categories) a v časti [Integrácia nastavenia a konfiguračných údajov aplikácie Project Operations](resource-dual-write-setup-integration.md). Výsledkom tejto integrácie je, že systém vytvorí štyri zdieľané záznamy kategórií v aplikáciách Finance and Operations.
2. V časti Finance choďte na **Správa výdavkov** > **Nastaviť** > **Zdieľané kategórie** a vyberte zdieľanú kategóriu s triedou transakcie **Výdavky**. Nastavte parameter **Môže byť použitý vo výdaji** na **True** a definujte typ výdavkov, ktorý sa má použiť.
3. Pomocou tohto záznamu zdieľanej kategórie vytvorte novú kategóriu výdavkov prechodom na **Správa výdavkov** > **Nastaviť** > **Kategórie výdavkov** a stlačením možnosti **Nový**. Keď sa záznam uloží, duálny zápis použije mapu tabuľky **Entita exportu kategórií výdavkov integrácie projektu Project Operations (msdyn\_expensecategories)** na synchronizáciu tohto záznamu s Dataverse.

  ![Integrácia kategórií výdavkov.](./media/DW6ExpenseCategories.png)

Kategórie výdavkov v aplikáciách Finance and Operations sú špecifické pre spoločnosť alebo právnickú osobu. Existujú samostatné, zodpovedajúce záznamy špecifické pre právnické osoby v Dataverse. Keď projektový manažér odhadne výdavky, nemôže si vybrať kategórie výdavkov, ktoré boli vytvorené pre projekt, ktorý vlastní iná spoločnosť ako spoločnosť, ktorá vlastní projekt, na ktorom pracujú. 

## <a name="expense-reports"></a>Výkazy výdavkov

Prehľady výdavkov sa vytvárajú a schvaľujú v aplikáciách Finance and Operations. Viac informácií nájdete v časti [Vytváranie a spracovanie výkazov výdavkov v systéme Dynamics 365 Project Operations](/learn/modules/create-process-expense-reports/). Po schválení výkazu výdavkov projektovým manažérom sa zaúčtuje do hlavnej knihy. V Project Operations sa riadky výkazu výdavkov súvisiacich s projektom účtujú pomocou špeciálnych pravidiel účtovania:

  - Náklady súvisiace s projektom (vrátane nevratnej dane) sa okamžite neúčtujú na účet nákladov projektu v hlavnej knihe, ale namiesto toho sa zaúčtujú na účet integrácie výdavkov. Tento účet je konfigurovaný v časti **Projektový manažment a účtovníctvo** > **Nastavenie** > **Parametre projektového manažmentu a účtovníctva** na karte **Project Operations v Dynamics 365 Customer engagement**.
  - Duálny zápis sa synchronizuje s Dataverse použitím mapy tabuľky **Entita exportu výdavkov projektu integrácie Project Operations (msdyn\_expenses)**.
  - Vedľajšia účtovná kniha dane, vedľajšia účtovná kniha dodávateľa a ďalšie finančné účtovania sa zaznamenávajú tak, ako je to využívané v čase zverejnenia výkazu o výdavkoch.

  ![Integrácia výkazov o výdavkoch.](./media/DW6ExpenseReports.png)

Keď sa píše záznam do entity **Výdavky** v Dataverse, systém spustí automatizovaný proces schválenia záznamu. V prípade potreby je možné stav automatizovaného schvaľovacieho procesu skontrolovať v Dataverse tým, že pôjdete do **Pokročilé nastavenia** > **Systém** > **Systémové úlohy**. Po dokončení schválenia sa v entite **Skutočné hodnoty** vytvoria záznamy triedy transakcie výdavkov.

Skutočnosti týkajúce sa výdavkov sa potom spracujú pomocou mapy tabuľky s dvojitým zápisom **Skutočné hodnoty integrácie Project Operations (msdy\_n_actuals)**. Ďalšie informácie nájdete v časti [Odhady a skutočné hodnoty projektu](resource-dual-write-estimates-actuals.md).

Periodický proces, **Import z prípravy** vytvára riadky denníka výdavkov súvisiace s výkazom výdavkov v denníku integrácie Project Operations. Ofsetový účet je predvolene nastavený na účet integrácie výdavkov. Denník integrácie zverejňovania vymaže zostatok na účte pre transakciu výdavkov a presunie sumu výdavkov na účet nákladov projektu. Systém tiež vytvorí vedľajšiu knihu projektu na účely následnej fakturácie a vykazovania výnosov.
