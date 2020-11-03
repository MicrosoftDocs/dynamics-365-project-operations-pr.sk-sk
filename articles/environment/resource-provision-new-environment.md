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
# <a name="provision-a-new-environment"></a><span data-ttu-id="256cc-103">Zriadenie nového prostredia</span><span class="sxs-lookup"><span data-stu-id="256cc-103">Provision a new environment</span></span>

<span data-ttu-id="256cc-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="256cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="256cc-105">Táto téma poskytuje informácie o tom, ako zriadiť nové prostredie Dynamics 365 Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.</span><span class="sxs-lookup"><span data-stu-id="256cc-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="256cc-106">Povolenie automatického poskytovania prostriedkov v projekte LCS</span><span class="sxs-lookup"><span data-stu-id="256cc-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="256cc-107">Pomocou nasledujúcich krokov povolíte automatizovaný tok poskytovania prostriedkov v Project Operations pre váš projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="256cc-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="256cc-108">Prejdite do [LCS](https://lcs.dynamics.com/v2) a vyberte dlaždicu **Ukážka správy funkcií**.</span><span class="sxs-lookup"><span data-stu-id="256cc-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="256cc-109">V zozname **Funkcia ukážky** vyberte **Funkcia Project Operations** a potom stlačte **Povolená funkcia ukážky** na povolenie Project Operations.</span><span class="sxs-lookup"><span data-stu-id="256cc-109">In the **Preview feature** list, select **Project Operations Feature** , and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="256cc-110">Tento krok sa vykoná iba jedenkrát pre projekt LCS.</span><span class="sxs-lookup"><span data-stu-id="256cc-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="256cc-111">Zriadenie prostredia Project Operations</span><span class="sxs-lookup"><span data-stu-id="256cc-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="256cc-112">Otvorte nové nasadenie Dynamics 365 Finance [ukážkové prostredie](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) alebo [testovacie prostredie/produkčné prostredie](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure).</span><span class="sxs-lookup"><span data-stu-id="256cc-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="256cc-113">Prejdite sprievodcom **Poskytovanie prostriedkov prostredia**.</span><span class="sxs-lookup"><span data-stu-id="256cc-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="256cc-114">Skontrolujte, či je vybratá verzia aplikácie 10.0.13 alebo vyššia.</span><span class="sxs-lookup"><span data-stu-id="256cc-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="256cc-115">Na poskytovanie prostriedkov Project Operations v časti **Pokročilé nastavenia** vyberte **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="256cc-115">To provision Project Operations, under **Advance settings** , select **Common Data Service**.</span></span> 
4. <span data-ttu-id="256cc-116">Povoľte **Nastavenie Common Data Service** výberom **Áno** a potom zadajte informácie do povinných polí:</span><span class="sxs-lookup"><span data-stu-id="256cc-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="256cc-117">Meno</span><span class="sxs-lookup"><span data-stu-id="256cc-117">Name</span></span>
  - <span data-ttu-id="256cc-118">Oblasť</span><span class="sxs-lookup"><span data-stu-id="256cc-118">Region</span></span>
  - <span data-ttu-id="256cc-119">Jazyk</span><span class="sxs-lookup"><span data-stu-id="256cc-119">Language</span></span>
  - <span data-ttu-id="256cc-120">Mena</span><span class="sxs-lookup"><span data-stu-id="256cc-120">Currency</span></span>
 
5. <span data-ttu-id="256cc-121">V poli **Šablóna Common Data Service** vyberte možnosť **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="256cc-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="256cc-122">Vyberte typ prostredia pre vaše nasadenie.</span><span class="sxs-lookup"><span data-stu-id="256cc-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="256cc-123">Skúšobná verzia založená na predplatnom vám umožní nasadiť prostredie CDS na obdobie 30 dní.</span><span class="sxs-lookup"><span data-stu-id="256cc-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Nastavenia nasadenia](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="256cc-125">Vyberte **Súhlasím** na potvrdenie zmluvných podmienok a potom vyberte **Hotovo** na návrat k nastaveniam nasadenia.</span><span class="sxs-lookup"><span data-stu-id="256cc-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Súhlas s nasadením](./media/2DeploymentConsent.png)

7. <span data-ttu-id="256cc-127">Vyplňte zvyšné povinné polia v sprievodcovi a potvrďte nasadenie.</span><span class="sxs-lookup"><span data-stu-id="256cc-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="256cc-128">Čas poskytovania prostriedkov prostredia sa líši v závislosti od typu prostredia.</span><span class="sxs-lookup"><span data-stu-id="256cc-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="256cc-129">Poskytovanie prostriedkov môže trvať až šesť hodín.</span><span class="sxs-lookup"><span data-stu-id="256cc-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="256cc-130">Po úspešnom dokončení nasadenia sa prostredie zobrazí ako **Nasadené**.</span><span class="sxs-lookup"><span data-stu-id="256cc-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="256cc-131">Ak chcete skontrolovať, či sa prostredie úspešne nasadilo, vyberte **Prihlásiť sa** a potvrďte prihlásením sa do prostredia.</span><span class="sxs-lookup"><span data-stu-id="256cc-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Podrobnosti o prostredí ](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="256cc-133">Použitie ukážkových údajov Project Operations Finance (voliteľný krok)</span><span class="sxs-lookup"><span data-stu-id="256cc-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="256cc-134">Použite ukážkové údaje Project Operations Finance na vydanie služby 10.0.13 prostredia na cloudovom hostiteľskom systéme podľa popisu v [tomto článku](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="256cc-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="256cc-135">Aplikovanie aktualizácií na prostredie Finance</span><span class="sxs-lookup"><span data-stu-id="256cc-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="256cc-136">Project Operations vyžaduje prostredie Finance s verziou aplikácie **10.0.13 (10.0.569.20009)** alebo vyššou.</span><span class="sxs-lookup"><span data-stu-id="256cc-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="256cc-137">Možno budete musieť vo svojom prostredí Finance použiť aktualizácie týkajúce sa kvality, aby ste mohli získať túto verziu.</span><span class="sxs-lookup"><span data-stu-id="256cc-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="256cc-138">V LCS, na stránke **Podrobnosti o prostredí** v časti **Dostupné aktualizácie** vyberte **Zobraziť aktualizáciu**.</span><span class="sxs-lookup"><span data-stu-id="256cc-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Zobraziť aktualizácie](./media/5ViewUpdates.png)

2. <span data-ttu-id="256cc-140">Na stránke **Binárne aktualizácie** vyberte **Uložiť balík.**</span><span class="sxs-lookup"><span data-stu-id="256cc-140">On the **Binary updates** page, select **Save package.**</span></span>

![Uložiť balík](./media/6SavePackage.png)

3. <span data-ttu-id="256cc-142">Kliknite na **Vybrať všetko** a potom vyberte **Uložiť balík**.</span><span class="sxs-lookup"><span data-stu-id="256cc-142">Click **Select all** and then select **Save package**.</span></span>

![Preskúmanie a ukladanie aktualizácií](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="256cc-144">Zadajte názov a popis balíka a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="256cc-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="256cc-145">V závislosti od internetového pripojenia môže tento proces trvať nejaký čas.</span><span class="sxs-lookup"><span data-stu-id="256cc-145">Depending on the internet connection, this process might take some time.</span></span>

![Nahrajte balík do knižnice aktív](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="256cc-147">Po uložení balíka vyberte **Hotovo** a uložte tento balík do knižnice aktív vo vašom projekte LCS.</span><span class="sxs-lookup"><span data-stu-id="256cc-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="256cc-148">Uloženie a overenie platnosti balíka môže trvať ~15 minút.</span><span class="sxs-lookup"><span data-stu-id="256cc-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="256cc-149">Ak chcete použiť aktualizáciu, prejdite na stránku **Podrobnosti o prostredí** v LCS a vyberte **Zachovať** > **Použiť aktualizácie**.</span><span class="sxs-lookup"><span data-stu-id="256cc-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Udržiavanie prostredí](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="256cc-151">V zozname aktualizácií vyberte balík, ktorý ste vytvorili, a vyberte **Použiť**.</span><span class="sxs-lookup"><span data-stu-id="256cc-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Použitie aktualizácií](./media/10ApplyUpdates.png)

<span data-ttu-id="256cc-153">Servis prostredia bude nejaký čas trvať.</span><span class="sxs-lookup"><span data-stu-id="256cc-153">Environment servicing will take some time.</span></span> <span data-ttu-id="256cc-154">Po dokončení sa prostredie vráti do nasadeného stavu.</span><span class="sxs-lookup"><span data-stu-id="256cc-154">After it is complete, the environment will return to a deployed state.</span></span>

![Nasadené prostredie](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="256cc-156">Nadviažte spojenie s dvojitým zápisom</span><span class="sxs-lookup"><span data-stu-id="256cc-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="256cc-157">Vo svojom projekte LCS prejdite na stránku **Podrobnosti o prostredí**.</span><span class="sxs-lookup"><span data-stu-id="256cc-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="256cc-158">V časti **Informácie o prostredí Common Data Service** vyberte **Odkaz na CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="256cc-158">Under **Common Data Service Environment Information** , select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="256cc-159">Po dokončení prepojenia znova vyberte **Odkaz na CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="256cc-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="256cc-160">Budete presmerovaný na dvojitý zápis vo financiách.</span><span class="sxs-lookup"><span data-stu-id="256cc-160">You will be redirected to Dual Write in Finance.</span></span>

![Prepojenie na CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="256cc-162">Vyberte **Použiť riešenie** na prístup k entitám, ktoré budú mapované v integrácii.</span><span class="sxs-lookup"><span data-stu-id="256cc-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Použiť riešenia](./media/13ApplySolutions.png)

5. <span data-ttu-id="256cc-164">Vyberte obe riešenia **Mapa entít Dynamics 365 Finance and Operations s dvojitým zápisom** a **Mapy entít Dynamics 365 Project Operations s dvojitým zápisom** a potom vyberte **Použiť**.</span><span class="sxs-lookup"><span data-stu-id="256cc-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps** , and then select **Apply**.</span></span>

![Potvrďte riešenia](./media/14ConfirmSolutions.png)

<span data-ttu-id="256cc-166">Po uplatnení riešení sa entity dvojitého zápisu použijú na prostredie.</span><span class="sxs-lookup"><span data-stu-id="256cc-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Použitie riešení](./media/15ApplyingSolutions.png)

<span data-ttu-id="256cc-168">Po použití entít sa v prostredí zobrazia všetky dostupné mapovania.</span><span class="sxs-lookup"><span data-stu-id="256cc-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Mapy s duálnym zápisom](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="256cc-170">Po aktualizácii obnovte údajové entity</span><span class="sxs-lookup"><span data-stu-id="256cc-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="256cc-171">V časti Financie prejdite na pracovný priestor **Správa údajov**.</span><span class="sxs-lookup"><span data-stu-id="256cc-171">In Finance, go to the **Data management** workspace.</span></span>

![Pracovný priestor na správu údajov](./media/16DataManagement.png)

2. <span data-ttu-id="256cc-173">Vyberte dlaždicu **Parametre platformy**.</span><span class="sxs-lookup"><span data-stu-id="256cc-173">Select the **Framework parameters** tile.</span></span>

![Parametre platformy](./media/17FrameworkParameters.png)

3. <span data-ttu-id="256cc-175">Na stránke **Nastavenia entity** vyberte **Obnoviť zoznam entít**.</span><span class="sxs-lookup"><span data-stu-id="256cc-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Obnoviť zoznam entít](./media/18RefreshEntityList.png)

<span data-ttu-id="256cc-177">Obnovenie bude trvať približne 20 minút.</span><span class="sxs-lookup"><span data-stu-id="256cc-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="256cc-178">Po dokončení dostanete upozornenie.</span><span class="sxs-lookup"><span data-stu-id="256cc-178">You will receive an alert when it is complete.</span></span>

![Obnovenie potvrdenia](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="256cc-180">Spustite mapy duálneho zápisu Project Operations</span><span class="sxs-lookup"><span data-stu-id="256cc-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="256cc-181">Vo svojom projekte LCS prejdite na stránku **Podrobnosti o prostredí**.</span><span class="sxs-lookup"><span data-stu-id="256cc-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="256cc-182">V časti **Informácie o prostredí Common Data Service** vyberte **Odkaz na CDS for Apps.**</span><span class="sxs-lookup"><span data-stu-id="256cc-182">Under **Common Data Service Environment Information** , select **Link to CDS for Apps.**</span></span> <span data-ttu-id="256cc-183">Po výbere odkazu budete presmerovaní na zoznam entít v mapovaní.</span><span class="sxs-lookup"><span data-stu-id="256cc-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="256cc-184">Spustite mapy podľa popisu v nasledujúcej tabuľke.</span><span class="sxs-lookup"><span data-stu-id="256cc-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="256cc-185">Postupujte podľa nižšie uvedeného poradia.</span><span class="sxs-lookup"><span data-stu-id="256cc-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="256cc-186">**Mapa entity**</span><span class="sxs-lookup"><span data-stu-id="256cc-186">**Entity Map**</span></span> | <span data-ttu-id="256cc-187">**Obnoviť entitu**</span><span class="sxs-lookup"><span data-stu-id="256cc-187">**Refresh entity**</span></span> | <span data-ttu-id="256cc-188">**Počiatočná synchronizácia**</span><span class="sxs-lookup"><span data-stu-id="256cc-188">**Initial sync**</span></span> | <span data-ttu-id="256cc-189">**Predloha pre počiatočnú synchronizáciu**</span><span class="sxs-lookup"><span data-stu-id="256cc-189">**Master for initial sync**</span></span> | <span data-ttu-id="256cc-190">**Spustenie predpokladov**</span><span class="sxs-lookup"><span data-stu-id="256cc-190">**Run prerequisites**</span></span> | <span data-ttu-id="256cc-191">**Počiatočná synchronizácia predpokladov**</span><span class="sxs-lookup"><span data-stu-id="256cc-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="256cc-192">**Roly projektových zdrojov pre všetky spoločnosti (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="256cc-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="256cc-193">No</span><span class="sxs-lookup"><span data-stu-id="256cc-193">No</span></span> | <span data-ttu-id="256cc-194">Áno</span><span class="sxs-lookup"><span data-stu-id="256cc-194">Yes</span></span> | <span data-ttu-id="256cc-195">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="256cc-195">Common Data Service</span></span> | <span data-ttu-id="256cc-196">No</span><span class="sxs-lookup"><span data-stu-id="256cc-196">No</span></span> | <span data-ttu-id="256cc-197">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-197">N\A</span></span> |
| <span data-ttu-id="256cc-198">**Právnické entity (cdm\_spoločnosti)**</span><span class="sxs-lookup"><span data-stu-id="256cc-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="256cc-199">No</span><span class="sxs-lookup"><span data-stu-id="256cc-199">No</span></span> | <span data-ttu-id="256cc-200">Áno</span><span class="sxs-lookup"><span data-stu-id="256cc-200">Yes</span></span> | <span data-ttu-id="256cc-201">Aplikácie Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="256cc-201">Finance and Operations apps</span></span> | <span data-ttu-id="256cc-202">No</span><span class="sxs-lookup"><span data-stu-id="256cc-202">No</span></span> | <span data-ttu-id="256cc-203">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-203">N\A</span></span> |
| <span data-ttu-id="256cc-204">**Skutočné hodnoty integrácie Project Operations (msdyn\_skutočné hodnoty)**</span><span class="sxs-lookup"><span data-stu-id="256cc-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="256cc-205">No</span><span class="sxs-lookup"><span data-stu-id="256cc-205">No</span></span> | <span data-ttu-id="256cc-206">No</span><span class="sxs-lookup"><span data-stu-id="256cc-206">No</span></span> | <span data-ttu-id="256cc-207">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-207">N\A</span></span> | <span data-ttu-id="256cc-208">Áno</span><span class="sxs-lookup"><span data-stu-id="256cc-208">Yes</span></span> | <span data-ttu-id="256cc-209">No</span><span class="sxs-lookup"><span data-stu-id="256cc-209">No</span></span> |
| <span data-ttu-id="256cc-210">**Riadky zmlúv projektu (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="256cc-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="256cc-211">No</span><span class="sxs-lookup"><span data-stu-id="256cc-211">No</span></span> | <span data-ttu-id="256cc-212">No</span><span class="sxs-lookup"><span data-stu-id="256cc-212">No</span></span> | <span data-ttu-id="256cc-213">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-213">N\A</span></span> | <span data-ttu-id="256cc-214">No</span><span class="sxs-lookup"><span data-stu-id="256cc-214">No</span></span> | <span data-ttu-id="256cc-215">No</span><span class="sxs-lookup"><span data-stu-id="256cc-215">No</span></span> |
| <span data-ttu-id="256cc-216">**Integračná entita pre transakčné vzťahy projektu (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="256cc-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="256cc-217">No</span><span class="sxs-lookup"><span data-stu-id="256cc-217">No</span></span> | <span data-ttu-id="256cc-218">No</span><span class="sxs-lookup"><span data-stu-id="256cc-218">No</span></span> | <span data-ttu-id="256cc-219">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-219">N\A</span></span> | <span data-ttu-id="256cc-220">No</span><span class="sxs-lookup"><span data-stu-id="256cc-220">No</span></span> | <span data-ttu-id="256cc-221">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-221">N\A</span></span> |
| <span data-ttu-id="256cc-222">**Medzníky integrácie riadka zmluvy Project Operations (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="256cc-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="256cc-223">No</span><span class="sxs-lookup"><span data-stu-id="256cc-223">No</span></span> | <span data-ttu-id="256cc-224">No</span><span class="sxs-lookup"><span data-stu-id="256cc-224">No</span></span> | <span data-ttu-id="256cc-225">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-225">N\A</span></span> | <span data-ttu-id="256cc-226">No</span><span class="sxs-lookup"><span data-stu-id="256cc-226">No</span></span> | <span data-ttu-id="256cc-227">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-227">N\A</span></span> |
| <span data-ttu-id="256cc-228">**Entita integrácie Project Operations pre odhady výdavkov (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="256cc-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="256cc-229">No</span><span class="sxs-lookup"><span data-stu-id="256cc-229">No</span></span> | <span data-ttu-id="256cc-230">No</span><span class="sxs-lookup"><span data-stu-id="256cc-230">No</span></span> | <span data-ttu-id="256cc-231">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-231">N\A</span></span> | <span data-ttu-id="256cc-232">No</span><span class="sxs-lookup"><span data-stu-id="256cc-232">No</span></span> | <span data-ttu-id="256cc-233">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-233">N\A</span></span> |
| <span data-ttu-id="256cc-234">**Entita exportu výdavkov projektu integrácie entity exportovania kategórií výdavkov (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="256cc-234">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="256cc-235">No</span><span class="sxs-lookup"><span data-stu-id="256cc-235">No</span></span> | <span data-ttu-id="256cc-236">No</span><span class="sxs-lookup"><span data-stu-id="256cc-236">No</span></span> | <span data-ttu-id="256cc-237">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-237">N\A</span></span> | <span data-ttu-id="256cc-238">No</span><span class="sxs-lookup"><span data-stu-id="256cc-238">No</span></span> | <span data-ttu-id="256cc-239">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-239">N\A</span></span> |
| <span data-ttu-id="256cc-240">**Entita exportu výdavkov projektu integrácie Project Operations (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="256cc-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="256cc-241">Áno</span><span class="sxs-lookup"><span data-stu-id="256cc-241">Yes</span></span> | <span data-ttu-id="256cc-242">No</span><span class="sxs-lookup"><span data-stu-id="256cc-242">No</span></span> | <span data-ttu-id="256cc-243">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-243">N\A</span></span> | <span data-ttu-id="256cc-244">No</span><span class="sxs-lookup"><span data-stu-id="256cc-244">No</span></span> | <span data-ttu-id="256cc-245">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-245">N\A</span></span> |
| <span data-ttu-id="256cc-246">**Entita integrácie Project Operations pre odhady hodín (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="256cc-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="256cc-247">Áno</span><span class="sxs-lookup"><span data-stu-id="256cc-247">Yes</span></span> | <span data-ttu-id="256cc-248">No</span><span class="sxs-lookup"><span data-stu-id="256cc-248">No</span></span> | <span data-ttu-id="256cc-249">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-249">N\A</span></span> | <span data-ttu-id="256cc-250">No</span><span class="sxs-lookup"><span data-stu-id="256cc-250">No</span></span> | <span data-ttu-id="256cc-251">Nie je k dispozícii</span><span class="sxs-lookup"><span data-stu-id="256cc-251">N\A</span></span> |


4. <span data-ttu-id="256cc-252">Ak chcete obnoviť entitu, vyberte názov mapy a potom vyberte **Obnoviť entity**.</span><span class="sxs-lookup"><span data-stu-id="256cc-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Obnoviť mapu](./media/20RefreshMapping.png)

5. <span data-ttu-id="256cc-254">Po dokončení obnovenia spustite priraďovanie.</span><span class="sxs-lookup"><span data-stu-id="256cc-254">After the refresh is complete, run the map.</span></span> <span data-ttu-id="256cc-255">Pred povolením ďalšej mapy skontrolujte, či je mapa v tabuľke v stave **Spustené**.</span><span class="sxs-lookup"><span data-stu-id="256cc-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="256cc-256">Spustenie máp s väčším počtom predpokladov môže chvíľu trvať.</span><span class="sxs-lookup"><span data-stu-id="256cc-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="256cc-257">Ak chcete spustiť mapu s predpokladmi, povoľte prepínač **Zobraziť mapy súvisiacich entít**.</span><span class="sxs-lookup"><span data-stu-id="256cc-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="256cc-258">Ak je v tabuľke pri možnosti **Počiatočná synchronizácia predpokladu** uvedené **Nie** , overte, či je príznak **Počiatočná synchronizácia** nastavený na **Vypnuté** vo všetkých nevyhnutných mapách predtým ako ju spustíte.</span><span class="sxs-lookup"><span data-stu-id="256cc-258">If the table indicates **Prerequisite initial sync** is **No** , verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Spustiť mapu](./media/21RunMap.png)

6. <span data-ttu-id="256cc-260">Skontrolujte, či sú všetky mapy súvisiace s projektom v spustenom stave.</span><span class="sxs-lookup"><span data-stu-id="256cc-260">Validate all project related maps are in the running state.</span></span>

![Všetky mapy sú spustené](./media/22AllMapsRunning.png)

<span data-ttu-id="256cc-262">Vaše prostredie Project Operations je teraz zriadené a nakonfigurované.</span><span class="sxs-lookup"><span data-stu-id="256cc-262">Your Project Operations environment is now provisioned and configured.</span></span>
