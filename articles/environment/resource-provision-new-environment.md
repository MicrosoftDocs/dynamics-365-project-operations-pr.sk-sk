---
title: Zriadenie nového prostredia
description: Táto téma poskytuje informácie o tom, ako zriadiť nové prostredie Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a43b947207b6d4276ef27ec996713bf3883e7906
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084251"
---
# <a name="provision-a-new-environment"></a>Zriadenie nového prostredia

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

Táto téma poskytuje informácie o tom, ako zriadiť nové prostredie Dynamics 365 Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Povolenie automatického poskytovania prostriedkov v projekte LCS

Pomocou nasledujúcich krokov povolíte automatizovaný tok poskytovania prostriedkov v Project Operations pre váš projekt LCS.

1. Prejdite do [LCS](https://lcs.dynamics.com/v2) a vyberte dlaždicu **Ukážka správy funkcií**.
2. V zozname **Funkcia ukážky** vyberte **Funkcia Project Operations** a potom stlačte **Povolená funkcia ukážky** na povolenie Project Operations.

> [!NOTE]
> Tento krok sa vykoná iba jedenkrát pre projekt LCS.

## <a name="provision-a-project-operations-environment"></a>Zriadenie prostredia Project Operations

1. Otvorte nové nasadenie Dynamics 365 Finance [ukážkové prostredie](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) alebo [testovacie prostredie/produkčné prostredie](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
2. Prejdite sprievodcom **Poskytovanie prostriedkov prostredia**. 

> [!IMPORTANT]
> Skontrolujte, či je vybratá verzia aplikácie 10.0.13 alebo vyššia.

3. Na poskytovanie prostriedkov Project Operations v časti **Pokročilé nastavenia** vyberte **Common Data Service**. 
4. Povoľte **Nastavenie Common Data Service** výberom **Áno** a potom zadajte informácie do povinných polí:

  - Meno
  - Oblasť
  - Jazyk
  - Mena
 
5. V poli **Šablóna Common Data Service** vyberte možnosť **Project Operations** 

6. Vyberte typ prostredia pre vaše nasadenie. Skúšobná verzia založená na predplatnom vám umožní nasadiť prostredie CDS na obdobie 30 dní. 

![Nastavenia nasadenia](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Vyberte **Súhlasím** na potvrdenie zmluvných podmienok a potom vyberte **Hotovo** na návrat k nastaveniam nasadenia.

![Súhlas s nasadením](./media/2DeploymentConsent.png)

7. Vyplňte zvyšné povinné polia v sprievodcovi a potvrďte nasadenie. Čas poskytovania prostriedkov prostredia sa líši v závislosti od typu prostredia. Poskytovanie prostriedkov môže trvať až šesť hodín.

  Po úspešnom dokončení nasadenia sa prostredie zobrazí ako **Nasadené**.

8. Ak chcete skontrolovať, či sa prostredie úspešne nasadilo, vyberte **Prihlásiť sa** a potvrďte prihlásením sa do prostredia.

![Podrobnosti o prostredí ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>Použitie ukážkových údajov Project Operations Finance (voliteľný krok)

Použite ukážkové údaje Project Operations Finance na vydanie služby 10.0.13 prostredia na cloudovom hostiteľskom systéme podľa popisu v [tomto článku](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Aplikovanie aktualizácií na prostredie Finance

Project Operations vyžaduje prostredie Finance s verziou aplikácie **10.0.13 (10.0.569.20009)** alebo vyššou.

Možno budete musieť vo svojom prostredí Finance použiť aktualizácie týkajúce sa kvality, aby ste mohli získať túto verziu.

1. V LCS, na stránke **Podrobnosti o prostredí** v časti **Dostupné aktualizácie** vyberte **Zobraziť aktualizáciu**.

![Zobraziť aktualizácie](./media/5ViewUpdates.png)

2. Na stránke **Binárne aktualizácie** vyberte **Uložiť balík.**

![Uložiť balík](./media/6SavePackage.png)

3. Kliknite na **Vybrať všetko** a potom vyberte **Uložiť balík**.

![Preskúmanie a ukladanie aktualizácií](./media/7ReviewAndSaveUpdates.png)

4. Zadajte názov a popis balíka a potom vyberte **Uložiť**. V závislosti od internetového pripojenia môže tento proces trvať nejaký čas.

![Nahrajte balík do knižnice aktív](./media/8UploadPackageToAssetsLibrary.png)

5. Po uložení balíka vyberte **Hotovo** a uložte tento balík do knižnice aktív vo vašom projekte LCS.

Uloženie a overenie platnosti balíka môže trvať ~15 minút.

6. Ak chcete použiť aktualizáciu, prejdite na stránku **Podrobnosti o prostredí** v LCS a vyberte **Zachovať** > **Použiť aktualizácie**.

![Udržiavanie prostredí](./media/9MaintainEnvironment.png)

7. V zozname aktualizácií vyberte balík, ktorý ste vytvorili, a vyberte **Použiť**.

![Použitie aktualizácií](./media/10ApplyUpdates.png)

Servis prostredia bude nejaký čas trvať. Po dokončení sa prostredie vráti do nasadeného stavu.

![Nasadené prostredie](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Nadviažte spojenie s dvojitým zápisom 

1. Vo svojom projekte LCS prejdite na stránku **Podrobnosti o prostredí**.
2. V časti **Informácie o prostredí Common Data Service** vyberte **Odkaz na CDS for Apps**.
3. Po dokončení prepojenia znova vyberte **Odkaz na CDS for Apps**. Budete presmerovaný na dvojitý zápis vo financiách.

![Prepojenie na CDS](./media/12LinktoCDS.png)

4. Vyberte **Použiť riešenie** na prístup k entitám, ktoré budú mapované v integrácii.

![Použiť riešenia](./media/13ApplySolutions.png)

5. Vyberte obe riešenia **Mapa entít Dynamics 365 Finance and Operations s dvojitým zápisom** a **Mapy entít Dynamics 365 Project Operations s dvojitým zápisom** a potom vyberte **Použiť**.

![Potvrďte riešenia](./media/14ConfirmSolutions.png)

Po uplatnení riešení sa entity dvojitého zápisu použijú na prostredie.

![Použitie riešení](./media/15ApplyingSolutions.png)

Po použití entít sa v prostredí zobrazia všetky dostupné mapovania.

![Mapy s duálnym zápisom](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Po aktualizácii obnovte údajové entity

1. V časti Financie prejdite na pracovný priestor **Správa údajov**.

![Pracovný priestor na správu údajov](./media/16DataManagement.png)

2. Vyberte dlaždicu **Parametre platformy**.

![Parametre platformy](./media/17FrameworkParameters.png)

3. Na stránke **Nastavenia entity** vyberte **Obnoviť zoznam entít**.

![Obnoviť zoznam entít](./media/18RefreshEntityList.png)

Obnovenie bude trvať približne 20 minút. Po dokončení dostanete upozornenie.

![Obnovenie potvrdenia](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>Spustite mapy duálneho zápisu Project Operations

1. Vo svojom projekte LCS prejdite na stránku **Podrobnosti o prostredí**.
2. V časti **Informácie o prostredí Common Data Service** vyberte **Odkaz na CDS for Apps.** Po výbere odkazu budete presmerovaní na zoznam entít v mapovaní.
3. Spustite mapy podľa popisu v nasledujúcej tabuľke. Postupujte podľa nižšie uvedeného poradia.

| **Mapa entity** | **Obnoviť entitu** | **Počiatočná synchronizácia** | **Predloha pre počiatočnú synchronizáciu** | **Spustenie predpokladov** | **Počiatočná synchronizácia predpokladov** |
| --- | --- | --- | --- | --- | --- |
| **Roly projektových zdrojov pre všetky spoločnosti (bookableresourcecategories)** | No | Áno | Common Data Service | No | Nie je k dispozícii |
| **Právnické entity (cdm\_spoločnosti)** | No | Áno | Aplikácie Finance and Operations | No | Nie je k dispozícii |
| **Skutočné hodnoty integrácie Project Operations (msdyn\_skutočné hodnoty)** | No | No | Nie je k dispozícii | Áno | No |
| **Riadky zmlúv projektu (salesorderdetails)** | No | No | Nie je k dispozícii | No | No |
| **Integračná entita pre transakčné vzťahy projektu (msdyn\_transactionconnections)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Medzníky integrácie riadka zmluvy Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita integrácie Project Operations pre odhady výdavkov (msdyn\_estimateslines)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita exportu výdavkov projektu integrácie entity exportovania kategórií výdavkov (msdyn\_expensecategories)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita exportu výdavkov projektu integrácie Project Operations (msdyn\_expenses)** | Áno | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita integrácie Project Operations pre odhady hodín (msdyn\_resourceassignments)** | Áno | No | Nie je k dispozícii | No | Nie je k dispozícii |


4. Ak chcete obnoviť entitu, vyberte názov mapy a potom vyberte **Obnoviť entity**. 


![Obnoviť mapu](./media/20RefreshMapping.png)

5. Po dokončení obnovenia spustite priraďovanie. Pred povolením ďalšej mapy skontrolujte, či je mapa v tabuľke v stave **Spustené**. Spustenie máp s väčším počtom predpokladov môže chvíľu trvať.

Ak chcete spustiť mapu s predpokladmi, povoľte prepínač **Zobraziť mapy súvisiacich entít**. Ak je v tabuľke pri možnosti **Počiatočná synchronizácia predpokladu** uvedené **Nie** , overte, či je príznak **Počiatočná synchronizácia** nastavený na **Vypnuté** vo všetkých nevyhnutných mapách predtým ako ju spustíte.

![Spustiť mapu](./media/21RunMap.png)

6. Skontrolujte, či sú všetky mapy súvisiace s projektom v spustenom stave.

![Všetky mapy sú spustené](./media/22AllMapsRunning.png)

Vaše prostredie Project Operations je teraz zriadené a nakonfigurované.
