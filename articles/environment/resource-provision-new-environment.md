---
title: Zriadenie nového prostredia
description: Tento článok poskytuje informácie o tom, ako vytvoriť nové prostredie Project Operations.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9cc3dafd6a2b6f92b585643c5d43ab52a3faf59e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931625"
---
# <a name="provision-a-new-environment"></a>Zriadenie nového prostredia

_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_



Tento článok poskytuje informácie o tom, ako vytvoriť nový Dynamics 365 Project Operations prostredie pre scenáre založené na zdrojoch/nezásobách.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Povolenie automatického poskytovania prostriedkov v projekte LCS

Pomocou nasledujúcich krokov povolíte automatizovaný tok poskytovania prostriedkov v Project Operations pre váš projekt LCS.

1. Prejdite do [LCS](https://lcs.dynamics.com/v2) a vyberte dlaždicu **Ukážka správy funkcií**.
2. V zozname **Funkcia ukážky** vyberte **Funkcia Project Operations** a potom stlačte **Povolená funkcia ukážky** na povolenie Project Operations.

   > [!NOTE]
   > Tento krok sa vykoná iba jedenkrát pre projekt LCS.

## <a name="provision-a-project-operations-environment"></a>Zriadenie prostredia Project Operations

1. Otvorte nový Dynamics 365 Finance [demo prostredie](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) alebo [sandbox/produkčné prostredie](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) nasadenie. 
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
    >
    >![Súhlas s nasadením.](./media/2DeploymentConsent.png)

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

5. Vyberte obe riešenia, **Dynamics 365 Finance and Operations Mapa entít s dvojitým zápisom** a **Dynamics 365 Project Operations Mapy entít s dvojitým zápisom** a potom vyberte **Použiť**.

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
4. Overte, či rola má povolenia **Čítať** a **Pripojiť k** pre nasledujúce entity:
      
      - **Typ výmenného kurzu meny**
      - **Účtovná osnova**
      - **Rozpočtový kalendár**
      - **Hlavná kniha**
      - **Spoločnosť**
      - **Výdavok**

5. Po aktualizácii roly zabezpečenia prejdite na položku **Nastavenia** > **Bezpečnosť** > **Tímy** a vyberte predvolený tím v zobrazení tímu **Vlastník miestneho podniku**.
6. Vyberte možnosť **Spravovať roly** a overte, či je tomuto tímu pridelené bezpečnostné oprávnenie **používateľ aplikácie s duálnym zápisom**.

## <a name="run-project-operations-dual-write-maps"></a>Spustite mapy duálneho zápisu Project Operations

1. Vo svojom projekte LCS prejdite na stránku **Podrobnosti o prostredí**.
2. V časti **Informácie o prostredí Common Data Service** vyberte **Odkaz na CDS for Apps.** Po výbere odkazu budete presmerovaní na zoznam entít v mapovaní.
3. Spustite mapy. Ďalšie informácie nájdete v časti [Verzie máp duálneho zápisu v aplikácii Project Operations](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Skontrolujte, či sú všetky mapy súvisiace s projektom v spustenom stave.

    ![Všetky mapy sú spustené.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Použitie konfiguračných údajov v službe CDS pre Project Operations (voliteľné)

Ak ste použili demo údaje pre prostredie Financie, pozrite si [Nastavenie a použite konfiguračných údajov v Common Data Service pre Project Operations](resource-apply-pro-setup-config-data.md), kde je uvedené, ako aplikovať demo údaje do prostredia CDS.


Vaše prostredie Project Operations je teraz zriadené a nakonfigurované. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
