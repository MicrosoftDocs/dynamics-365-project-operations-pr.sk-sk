---
title: Zriadenie nového prostredia
description: Táto téma poskytuje informácie o tom, ako zriadiť nové prostredie Project Operations.
author: sigitac
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fd98ec360cbd89c9fb7e49bfa11cfffeffca541441e641c973a23c141c922cd2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988580"
---
# <a name="provision-a-new-environment"></a>Zriadenie nového prostredia

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Táto téma poskytuje informácie o tom, ako nasadiť nové prostredie Dynamics 365 Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Povolenie automatického poskytovania prostriedkov v projekte LCS

Pomocou nasledujúcich krokov povolíte automatizovaný tok poskytovania prostriedkov v Project Operations pre váš projekt LCS.

1. Prejdite do [LCS](https://lcs.dynamics.com/v2) a vyberte dlaždicu **Ukážka správy funkcií**.
2. V zozname **Funkcia ukážky** vyberte **Funkcia Project Operations** a potom stlačte **Povolená funkcia ukážky** na povolenie Project Operations.

> [!NOTE]
> Tento krok sa vykoná iba jedenkrát pre projekt LCS.

## <a name="provision-a-project-operations-environment"></a>Zriadenie prostredia Project Operations

1. Otvorte nové nasadenie Dynamics 365 Finance [ukážkové prostredie](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) alebo [testovacie prostredie/produkčné prostredie](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure). 
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

![Nastavenia nasadenia.](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Vyberte **Súhlasím** na potvrdenie zmluvných podmienok a potom vyberte **Hotovo** na návrat k nastaveniam nasadenia.

![Súhlas s nasadením.](./media/2DeploymentConsent.png)

7. Voliteľné – použitie ukážkových údajov pre prostredie. Prejdite na položku **Pokročilé nastavenia**, vyberte **Prispôsobiť konfiguráciu databázy SQL** a nastavte **Zadať množinu údajov pre databázu aplikácií** na možnosť **Ukážka**.

8. Vyplňte zvyšné povinné polia v sprievodcovi a potvrďte nasadenie. Čas na zabezpečenie prostredia sa líši podľa typu prostredia. Poskytovanie prostriedkov môže trvať až šesť hodín.

  Po úspešnom dokončení nasadenia sa prostredie zobrazí ako **Nasadené**.

9. Ak chcete potvrdiť, že sa prostredie úspešne nasadilo, vyberte **Prihlásiť sa** a potvrďte prihlásením sa do prostredia.

![Podrobnosti o prostredí.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Aplikovanie aktualizácií na prostredie Finance

Project Operations vyžaduje prostredie Finance s verziou aplikácie **10.0.13 (10.0.569.20009)** alebo vyššou.

Možno budete musieť vo svojom prostredí Finance použiť aktualizácie týkajúce sa kvality, aby ste mohli získať túto verziu.

1. V LCS, na stránke **Podrobnosti o prostredí** v časti **Dostupné aktualizácie** vyberte **Zobraziť aktualizáciu**.

![Zobraziť aktualizácie.](./media/5ViewUpdates.png)

2. Na stránke **Binárne aktualizácie** vyberte **Uložiť balík.**

![Uložiť balík.](./media/6SavePackage.png)

3. Kliknite na **Vybrať všetko** a potom vyberte **Uložiť balík**.

![Preskúmanie a ukladanie aktualizácií.](./media/7ReviewAndSaveUpdates.png)

4. Zadajte názov a popis balíka a potom vyberte **Uložiť**. V závislosti od internetového pripojenia môže tento proces trvať nejaký čas.

![Nahrajte balík do knižnice aktív.](./media/8UploadPackageToAssetsLibrary.png)

5. Po uložení balíka vyberte **Hotovo** a uložte tento balík do knižnice aktív vo vašom projekte LCS.

Uloženie a overenie platnosti balíka môže trvať ~15 minút.

6. Ak chcete použiť aktualizáciu, prejdite na stránku **Podrobnosti o prostredí** v LCS a vyberte **Zachovať** > **Použiť aktualizácie**.

![Udržiavanie prostredí.](./media/9MaintainEnvironment.png)

7. V zozname aktualizácií vyberte balík, ktorý ste vytvorili, a vyberte **Použiť**.

![Použitie aktualizácií.](./media/10ApplyUpdates.png)

Servis prostredia bude nejaký čas trvať. Po dokončení sa prostredie vráti do nasadeného stavu.

![Nasadené prostredie.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Nadviažte spojenie s dvojitým zápisom 

1. Vo svojom projekte LCS prejdite na stránku **Podrobnosti o prostredí**.
2. V časti **Informácie o prostredí Common Data Service** vyberte **Odkaz na CDS for Apps**.
3. Po dokončení prepojenia znova vyberte **Odkaz na CDS for Apps**. Budete presmerovaný na dvojitý zápis vo financiách.

![Prepojenie na CDS.](./media/12LinktoCDS.png)

4. Vyberte **Použiť riešenie** na prístup k entitám, ktoré budú mapované v integrácii.

![Použiť riešenia.](./media/13ApplySolutions.png)

5. Vyberte obe riešenia, **Mapa entity s duálnym zápisom Dynamics 365 Finance and Operations** a **Mapy entít s duálnym zápisom Dynamics 365 Project Operations** a potom vyberte **Použiť**.

![Potvrďte riešenia.](./media/14ConfirmSolutions.png)

Po uplatnení riešení sa entity dvojitého zápisu použijú na prostredie.

![Použitie riešení.](./media/15ApplyingSolutions.png)

Po použití entít sa v prostredí zobrazia všetky dostupné mapovania.

![Mapy s duálnym zápisom.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Po aktualizácii obnovte údajové entity

1. V časti Financie prejdite na pracovný priestor **Správa údajov**.

![Pracovný priestor na správu údajov.](./media/16DataManagement.png)

2. Vyberte dlaždicu **Parametre platformy**.

![Parametre platformy.](./media/17FrameworkParameters.png)

3. Na stránke **Nastavenia entity** vyberte **Obnoviť zoznam entít**.

![Obnoviť zoznam entít.](./media/18RefreshEntityList.png)

Obnovenie bude trvať približne 20 minút. Po dokončení dostanete upozornenie.

![Obnovenie potvrdenia.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>Aktualizácia nastavení zabezpečenia v aplikácii Project Operations prostredia Dataverse

1. Prejdite do aplikácie Project Operations v prostredí Dataverse. 
2. Kliknite na položku **Nastavenie** > **Zabezpečenie** > **Roly zabezpečenia**. 
3. Na stránke **Roly zabezpečenia** v zozname rolí vyberte **používateľ aplikácie s duálnym zápisom** a vyberte kartu **Vlastné entity**.  
4. Overte, či má rola povolenia **Čítať** a **Pripojiť k** pre:
      
      - **Typ výmenného kurzu meny**
      - **Účtovná osnova**
      - **Rozpočtový kalendár**
      - **Hlavná kniha**

5. Po aktualizácii roly zabezpečenia prejdite na položku **Nastavenia** > **Bezpečnosť** > **Tímy** a vyberte predvolený tím v zobrazení tímu **Vlastník miestneho podniku**.
6. Vyberte možnosť **Spravovať roly** a overte, či je tomuto tímu pridelené bezpečnostné oprávnenie **používateľ aplikácie s duálnym zápisom**.

## <a name="run-project-operations-dual-write-maps"></a>Spustite mapy duálneho zápisu Project Operations

1. Vo svojom projekte LCS prejdite na stránku **Podrobnosti o prostredí**.
2. V časti **Informácie o prostredí Common Data Service** vyberte **Odkaz na CDS for Apps.** Po výbere odkazu budete presmerovaní na zoznam entít v mapovaní.
3. Spustite mapy podľa popisu v nasledujúcej tabuľke. Postupujte podľa nižšie uvedeného poradia.

| **Mapa entity** | **Obnoviť entitu** | **Počiatočná synchronizácia** | **Predloha pre počiatočnú synchronizáciu** | **Spustenie predpokladov** | **Počiatočná synchronizácia predpokladov** |
| --- | --- | --- | --- | --- | --- |
| **Roly projektových zdrojov pre všetky spoločnosti (bookableresourcecategories)** | No | Áno | Common Data Service | No | Nie je k dispozícii |
| **Právnické entity (cdm\_spoločnosti)** | No | Áno | Aplikácie Finance and Operations | No | Nie je k dispozícii |
| **Účtovná kniha (msdyn_ledgers)** | No | Áno | Aplikácie Finance and Operations | Áno | Áno, aplikácie Finance and Operations |
| **Skutočné hodnoty integrácie Project Operations (msdyn\_skutočné hodnoty)** | No | No | Nie je k dispozícii | Áno | No |
| **Riadky zmlúv projektu (salesorderdetails)** | No | No | Nie je k dispozícii | No | No |
| **Integračná entita pre transakčné vzťahy projektu (msdyn\_transactionconnections)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Medzníky integrácie riadka zmluvy Project Operations (msdyn\_contractlinesscheduleofvalues)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita integrácie Project Operations pre odhady výdavkov (msdyn\_estimateslines)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita exportu výdavkov projektu integrácie entity exportovania kategórií výdavkov (msdyn\_expensecategories)** | No | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita exportu výdavkov projektu integrácie Project Operations (msdyn\_expenses)** | Áno | No | Nie je k dispozícii | No | Nie je k dispozícii |
| **Entita integrácie Project Operations pre odhady hodín (msdyn\_resourceassignments)** | Áno | No | Nie je k dispozícii | No | Nie je k dispozícii |


4. Ak chcete obnoviť entitu, vyberte názov mapy a potom vyberte **Obnoviť entity**. 


![Obnoviť mapu.](./media/20RefreshMapping.png)

5. Po dokončení obnovenia spustite priraďovanie. Pred povolením ďalšej mapy skontrolujte, či je mapa v tabuľke v stave **Spustené**. Spustenie máp s väčším počtom predpokladov môže chvíľu trvať.

Ak chcete spustiť mapu s predpokladmi, povoľte prepínač **Zobraziť mapy súvisiacich entít**. Ak je v tabuľke pri možnosti **Počiatočná synchronizácia predpokladu** uvedené **Nie**, overte, či je príznak **Počiatočná synchronizácia** nastavený na **Vypnuté** vo všetkých nevyhnutných mapách predtým ako ju spustíte.

![Spustiť mapu.](./media/21RunMap.png)

6. Skontrolujte, či sú všetky mapy súvisiace s projektom v spustenom stave.

![Všetky mapy sú spustené.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Použitie konfiguračných údajov v službe CDS pre Project Operations (voliteľné)

Ak ste použili demo údaje pre prostredie Financie, pozrite si [Nastavenie a použite konfiguračných údajov v Common Data Service pre Project Operations](resource-apply-pro-setup-config-data.md), kde je uvedené, ako aplikovať demo údaje do prostredia CDS.


Vaše prostredie Project Operations je teraz zriadené a nakonfigurované. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]