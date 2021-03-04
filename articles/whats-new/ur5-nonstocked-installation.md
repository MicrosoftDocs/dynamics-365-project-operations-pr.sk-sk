---
title: Aktualizujte Project Operations vo svojom prostredí Finance
description: Táto téma poskytuje informácie o tom, ako aktualizovať Project Operations vo vašom prostredí Dynamics 365 Finance.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816644"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="5af7a-103">Aktualizujte Project Operations vo svojom prostredí Finance</span><span class="sxs-lookup"><span data-stu-id="5af7a-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="5af7a-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="5af7a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="5af7a-105">Táto téma poskytuje informácie o tom, ako aktualizovať Dynamics 365 Project Operations vo vašom prostredí Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="5af7a-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="5af7a-106">Existujú tri postupy, ktoré sú potrebné na aktualizáciu Project Operations na verziu 5 (UR5):</span><span class="sxs-lookup"><span data-stu-id="5af7a-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="5af7a-107">Importujte balík do vašej ukážky projektu</span><span class="sxs-lookup"><span data-stu-id="5af7a-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="5af7a-108">Použite aktualizáciu</span><span class="sxs-lookup"><span data-stu-id="5af7a-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="5af7a-109">Aktualizujte svoje prostredie Dataverse</span><span class="sxs-lookup"><span data-stu-id="5af7a-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="5af7a-110">Importujte balík do vášho projektu LCS</span><span class="sxs-lookup"><span data-stu-id="5af7a-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="5af7a-111">Prihláste sa do [Lifecycle Services (LCS)](https://lcs.dynamics.com/) ako vlastník projektu alebo manažér prostredia.</span><span class="sxs-lookup"><span data-stu-id="5af7a-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="5af7a-112">Zo zoznamu projektov vyberte svoj projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="5af7a-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="5af7a-113">Na stránke **Projekt** v skupine **Prostredia** otvorte prostredie, ktoré chcete aktualizovať.</span><span class="sxs-lookup"><span data-stu-id="5af7a-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="5af7a-114">Skontrolujte, či je prostredie spustené.</span><span class="sxs-lookup"><span data-stu-id="5af7a-114">Verify that the environment is running.</span></span> <span data-ttu-id="5af7a-115">Ak nie je spustené, spustite prostredie.</span><span class="sxs-lookup"><span data-stu-id="5af7a-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="5af7a-116">V časti **Nové vydanie** pod **Dostupné aktualizácie** vyberte **Zobraziť aktualizáciu** pre 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="5af7a-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Tlačidlo Zobraziť aktualizácie](media/view-update.png)

6. <span data-ttu-id="5af7a-118">Na stránke **Binárne aktualizácie** vyberte **Uložiť balík**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="5af7a-119">Na stránke **Skontrolovať a uložiť aktualizácie** vyberte **Uložiť balík**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="5af7a-120">Na table **Uložiť balík do knižnice aktív**, ktorá sa otvorí, zadajte názov balíka a potom vyberte **Uložiť balík**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="5af7a-121">Keď LCS dokončí ukladanie balíka, povolí sa tlačidlo **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="5af7a-122">Vyberte položku **Hotovo**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-122">Select **Done**.</span></span> <span data-ttu-id="5af7a-123">LCS overí balík.</span><span class="sxs-lookup"><span data-stu-id="5af7a-123">LCS will verify the package.</span></span> <span data-ttu-id="5af7a-124">Overenie môže trvať niekoľko minút alebo až hodinu.</span><span class="sxs-lookup"><span data-stu-id="5af7a-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="5af7a-125">Použite aktualizáciu balíka</span><span class="sxs-lookup"><span data-stu-id="5af7a-125">Apply the package update</span></span>

1. <span data-ttu-id="5af7a-126">V LCS na stránke **Podrobnosti o prostredí** vyberte **Udržiavať** > **Použiť aktualizácie**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="5af7a-127">V zozname vyberte balík, ktorý ste uložili skôr, a potom vyberte **Použiť**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="5af7a-128">Vyberte **Áno** na potvrdenie, že chcete nasadiť balík.</span><span class="sxs-lookup"><span data-stu-id="5af7a-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Potvrďte dialógové okno nasadenia balíka](media/confirm-package-deployment.png)

4. <span data-ttu-id="5af7a-130">Vyberte **Áno** na potvrdenie, že chcete aktualizovať aplikáciu.</span><span class="sxs-lookup"><span data-stu-id="5af7a-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Potvrďte dialógové okno aktualizácie aplikácie](media/confirm-application-update.png)

<span data-ttu-id="5af7a-132">Spustí sa nasadenie a aktualizácia aplikácie.</span><span class="sxs-lookup"><span data-stu-id="5af7a-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="5af7a-133">Na stránke **Podrobnosti o prostredí** v pravom hornom rohu sa aktualizuje stav prostredia na **Poskytuje sa služba**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="5af7a-134">Aktualizácia bude dokončená približne o dve hodiny.</span><span class="sxs-lookup"><span data-stu-id="5af7a-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="5af7a-135">Informácie o vydaní aplikácie sa aktualizujú na **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** a stav prostredia sa aktualizuje na **Nasadené**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="5af7a-136">Aktualizujte svoje prostredie Dataverse</span><span class="sxs-lookup"><span data-stu-id="5af7a-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="5af7a-137">Prihláste sa do [centra spravovania Power Platform](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="5af7a-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="5af7a-138">V zozname vyhľadajte a otvorte prostredie, ktoré ste použili na inštaláciu Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5af7a-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="5af7a-139">Na stránke **Prostredia** vyberte **Zdroj** > **Aplikácie Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="5af7a-140">V zozname vyhľadajte **Microsoft Dynamics 365 Project Operations** a v stĺpci **Stav** vyberte **Aktualizácia k dispozícii**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="5af7a-141">Začiarknite políčko **Súhlasím s podmienkami služby** a potom vyberte **Aktualizovať**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="5af7a-142">Nainštaluje sa najnovšia verzia riešenia.</span><span class="sxs-lookup"><span data-stu-id="5af7a-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="5af7a-143">Po dokončení inštalácie budete mať nainštalovanú verziu 4.5.0.134.</span><span class="sxs-lookup"><span data-stu-id="5af7a-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="5af7a-144">Konfigurácia nových funkcií</span><span class="sxs-lookup"><span data-stu-id="5af7a-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="5af7a-145">Povolenie mapovania s duálnym zápisom</span><span class="sxs-lookup"><span data-stu-id="5af7a-145">Enable dual-write mapping</span></span>

<span data-ttu-id="5af7a-146">Po dokončení aktualizácie prostredí Finance a Dataverse môžete povoliť požadované mapovania s duálnym zápisom.</span><span class="sxs-lookup"><span data-stu-id="5af7a-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="5af7a-147">Dokončením nasledujúcich postupov povolíte mapovania s duálnym zápisom.</span><span class="sxs-lookup"><span data-stu-id="5af7a-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="5af7a-148">Aktualizujte nastavenia zabezpečenia v prostredí Customer Engagement</span><span class="sxs-lookup"><span data-stu-id="5af7a-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="5af7a-149">Obnovte údaje o entitách</span><span class="sxs-lookup"><span data-stu-id="5af7a-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="5af7a-150">Aktualizujte a spustite mapovania s duálnym zápisom</span><span class="sxs-lookup"><span data-stu-id="5af7a-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="5af7a-151">Aktualizujte nastavenia zabezpečenia v prostredí Dataverse</span><span class="sxs-lookup"><span data-stu-id="5af7a-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="5af7a-152">Nasledujúce aktualizácie bezpečnostných oprávnení pre entity sú vyžadované ako súčasť aktualizácie UR5.</span><span class="sxs-lookup"><span data-stu-id="5af7a-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="5af7a-153">V prostredí Dataverse prejdite na **Nastavenia** a v skupine **Systém** vyberte **Zabezpečenie**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![Nastavenia prostredia Dataverse](media/Picture21.png)

2. <span data-ttu-id="5af7a-155">Vyberte **Roly zabezpečenia**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="5af7a-156">V zozname rolí vyberte **používateľ aplikácie s duálnym zápisom** a vyberte kartu **Vlastné entity**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="5af7a-157">Overte, či má rola povolenia **Čítať** a **Pripojiť k** pre:</span><span class="sxs-lookup"><span data-stu-id="5af7a-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="5af7a-158">**Typ výmenného kurzu meny**</span><span class="sxs-lookup"><span data-stu-id="5af7a-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="5af7a-159">**Účtovná osnova**</span><span class="sxs-lookup"><span data-stu-id="5af7a-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="5af7a-160">**Rozpočtový kalendár**</span><span class="sxs-lookup"><span data-stu-id="5af7a-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="5af7a-161">**Hlavná kniha**</span><span class="sxs-lookup"><span data-stu-id="5af7a-161">**Ledger**</span></span>

5. <span data-ttu-id="5af7a-162">Po aktualizácii roly zabezpečenia prejdite na **Nastavenia** > **Zabezpečenie** > **Tímy**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="5af7a-163">Overte, či bola tímu pridelená rola **používateľ aplikácie s duálnym zápisom**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="5af7a-164">Obnovte dátové entity z aktualizácie</span><span class="sxs-lookup"><span data-stu-id="5af7a-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="5af7a-165">Vo svojom prostredí Finance otvorte pracovný priestor **Správa údajov** a potom otvorte stránku **Parametre rámca**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="5af7a-166">Na karte **Nastavenia entity** vyberte **Obnoviť zoznam entít**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="5af7a-167">Vyberte **Zavrieť** na potvrdenie obnovenia entity.</span><span class="sxs-lookup"><span data-stu-id="5af7a-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="5af7a-168">Dokončenie tohto procesu bude trvať približne 20 minút.</span><span class="sxs-lookup"><span data-stu-id="5af7a-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="5af7a-169">Po dokončení obnovenia budete informovaní.</span><span class="sxs-lookup"><span data-stu-id="5af7a-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="5af7a-170">Aktualizujte mapovania s duálnym zápisom</span><span class="sxs-lookup"><span data-stu-id="5af7a-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="5af7a-171">V pracovnom priestore **Správa údajov** vyberte **Duálny zápis**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="5af7a-172">Vyberte **Použiť riešenia**, vyberte obe riešenia v zozname a potom vyberte **Použiť**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="5af7a-173">Na stránke **Duálny zápis** vyberte nasledujúce mapy tabuliek a potom vyberte **Zastaviť**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="5af7a-174">**Skutočné hodnoty integrácie Project Operations (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="5af7a-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="5af7a-175">**Kategórie výdavkov projektu na integráciu Project Operations (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="5af7a-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="5af7a-176">**Integrácia Project Operations predstavuje skutočnú entitu exportu výdavkov projektu (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="5af7a-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="5af7a-177">Na stránke **Verzia mapy tabuľky** použite novú verziu mapy na každú z troch entít.</span><span class="sxs-lookup"><span data-stu-id="5af7a-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="5af7a-178">Na stránke **Duálny zápis** výberom spustenia reštartujte mapy.</span><span class="sxs-lookup"><span data-stu-id="5af7a-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="5af7a-179">V zozname máp vyberte mapu **Ledger (msdyn_ledgers)** so všetkými predpokladmi a začiarknite políčko **Počiatočná synchronizácia**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="5af7a-180">V poli **Predloha pre počiatočnú synchronizáciu** vyberte **aplikácie Finance and Operations** a potom vyberte **Spustiť**.</span><span class="sxs-lookup"><span data-stu-id="5af7a-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Synchronizácia máp účtovnej knihy](media/DW6.png)
 
