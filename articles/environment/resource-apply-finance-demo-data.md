---
title: Použitie ukážkových údajov aplikácie Project Operations v prostredí na cloudovom hostiteľskom systéme Finance
description: Táto téma vysvetľuje, ako aplikovať ukážkové údaje z Project Operations do prostredia na cloudovom hostiteľskom systéme Dynamics 365 Finance.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1a94862d5a024eb1630f33c0c96699e8b4b49bf2
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949075"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="e4d87-103">Použitie ukážkových údajov aplikácie Project Operations v prostredí na cloudovom hostiteľskom systéme Finance</span><span class="sxs-lookup"><span data-stu-id="e4d87-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="e4d87-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="e4d87-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

><span data-ttu-id="e4d87-105">[Dôležité] Táto téma sa týka iba systému Microsoft Dynamics 365 Finance verzie 10.0.13 a je možné ju používať iba v prostredí hosťovanom v cloude.</span><span class="sxs-lookup"><span data-stu-id="e4d87-105">[Important] This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="e4d87-106">Kroky v tejto téme vykonajte **PRED** použitím aktualizácií prostredia týkajúcich sa kvality.</span><span class="sxs-lookup"><span data-stu-id="e4d87-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="e4d87-107">Vo svojom projekte LCS otvorte stránku **Podrobnosti o prostredí**.</span><span class="sxs-lookup"><span data-stu-id="e4d87-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="e4d87-108">Pamätajte na to, že obsahuje podrobnosti potrebné na pripojenie k prostrediu pomocou protokolu RDP (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="e4d87-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Podrobnosti o prostredí](./media/1EnvironmentDetails.png)

<span data-ttu-id="e4d87-110">Prvou súpravou zvýraznených poverení sú poverenia pre lokálny účet a obsahujú hypertextový odkaz na pripojenie k vzdialenej ploche.</span><span class="sxs-lookup"><span data-stu-id="e4d87-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="e4d87-111">Poverenia zahŕňajú používateľské meno a heslo správcu prostredia.</span><span class="sxs-lookup"><span data-stu-id="e4d87-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="e4d87-112">Druhá súprava poverení sa používa na prihlásenie na server SQL v tomto prostredí.</span><span class="sxs-lookup"><span data-stu-id="e4d87-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="e4d87-113">Pripojte sa k vzdialenej ploche pomocou hypertextového odkazu v časti **Lokálne účty** a použite **Poverenia lokálneho účtu** na overenie.</span><span class="sxs-lookup"><span data-stu-id="e4d87-113">Remote to the environment by the hyperlink in **Local Accounts**, and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="e4d87-114">Prejdite do časti **Internetové informačné služby** > **Fondy aplikácií** > **AOSService** a zastavte službu.</span><span class="sxs-lookup"><span data-stu-id="e4d87-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="e4d87-115">V tomto okamihu zastavíte službu, aby ste mohli pokračovať v nahradzovaní databázy SQL.</span><span class="sxs-lookup"><span data-stu-id="e4d87-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Zastavenie AOS](./media/2StopAOS.png)

4. <span data-ttu-id="e4d87-117">Prejdite na **Služby** a zastavte nasledujúce dve položky:</span><span class="sxs-lookup"><span data-stu-id="e4d87-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="e4d87-118">Microsoft Dynamics 365 Unified Operations: Služba dávkovej správy</span><span class="sxs-lookup"><span data-stu-id="e4d87-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="e4d87-119">Microsoft Dynamics 365 Unified Operations: Platforma na import a export údajov</span><span class="sxs-lookup"><span data-stu-id="e4d87-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Zastavenie služieb](./media/3StopServices.png)

5. <span data-ttu-id="e4d87-121">Otvorte Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="e4d87-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="e4d87-122">Prihláste sa pomocou poverení servera SQL a použite meno používateľa axdbadmin a heslo zo stránky **Podrobnosti prostredia** LCS.</span><span class="sxs-lookup"><span data-stu-id="e4d87-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![SQL Server Management Studio](./media/4SSMS.png)

6. <span data-ttu-id="e4d87-124">V Prieskumníkovi objektov, **Databázy** a nájdite **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="e4d87-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="e4d87-125">Databázu nahradíte novou databázou, ktorá sa nachádza v časti [Centrum sťahovania](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="e4d87-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="e4d87-126">Skopírujte súbor zip do virtuálneho počítača, ku ktorému ste vzdialene pripojení, a rozbaľte obsah súboru zip.</span><span class="sxs-lookup"><span data-stu-id="e4d87-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="e4d87-127">V programe SQL Server Management Studio kliknite pravým tlačidlom myši na **AxDB** a potom vyberte **Úlohy** > **Obnoviť** > **Databáza**.</span><span class="sxs-lookup"><span data-stu-id="e4d87-127">In SQL Server Management Studio, right-click **AxDB**, and then select **Tasks** > **Restore** > **Database**.</span></span>

![Obnovenie databázy](./media/5RestoreDatabase.png)

9. <span data-ttu-id="e4d87-129">Vyberte **Zdrojové zariadenie** a prejdite na súbor rozbalený zo súboru zip, ktorý ste skopírovali.</span><span class="sxs-lookup"><span data-stu-id="e4d87-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Zdrojové zariadenia](./media/6SourceDevice.png)

10. <span data-ttu-id="e4d87-131">Vyberte **Možnosti** a potom vyberte **Prepísať existujúcu databázu** a **Zatvoriť existujúce pripojenia k cieľovej databáze**.</span><span class="sxs-lookup"><span data-stu-id="e4d87-131">Select **Options**, and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="e4d87-132">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="e4d87-132">Select **OK**.</span></span>

![Obnovenie nastavení](./media/7RestoreSetting.png)

<span data-ttu-id="e4d87-134">Dostanete potvrdenie, že obnovenie AXDB bolo úspešné.</span><span class="sxs-lookup"><span data-stu-id="e4d87-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="e4d87-135">Po prijatí tohto potvrdenia môžete zavrieť SQL Services Management Studio.</span><span class="sxs-lookup"><span data-stu-id="e4d87-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="e4d87-136">Prejdite späť do časti **Internetové informačné služby** > **Fondy aplikácií** > **AOSService** a spustite AOSService.</span><span class="sxs-lookup"><span data-stu-id="e4d87-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="e4d87-137">Prejdite do časti **Služby** a spustite dve služby, ktoré ste zastavili predtým.</span><span class="sxs-lookup"><span data-stu-id="e4d87-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="e4d87-138">Vyhľadajte nástroj AdminUserProvisioning na tomto virtuálnom počítači.</span><span class="sxs-lookup"><span data-stu-id="e4d87-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="e4d87-139">Prejdite na K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="e4d87-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="e4d87-140">Spustite súbor .ext pomocou svojej adresy používateľa v poli **E-mailová adresa**.</span><span class="sxs-lookup"><span data-stu-id="e4d87-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="e4d87-141">Stlačte možnosť **Odoslať**.</span><span class="sxs-lookup"><span data-stu-id="e4d87-141">Select **Submit**.</span></span>

![Poskytovanie používateľa správcu](./media/8AdminUserProvisioning.png)

<span data-ttu-id="e4d87-143">Dokončenie trvá pár minút.</span><span class="sxs-lookup"><span data-stu-id="e4d87-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="e4d87-144">Mali by ste dostať potvrdzujúce hlásenie, že správca bol úspešne aktualizovaný.</span><span class="sxs-lookup"><span data-stu-id="e4d87-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="e4d87-145">Nakoniec spustite príkazový riadok ako správca a vykonajte iisreset</span><span class="sxs-lookup"><span data-stu-id="e4d87-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![Resetovanie IIS](./media/9IISReset.png)

18. <span data-ttu-id="e4d87-147">Ukončite reláciu vzdialenej plochy a pomocou stránky **Podrobnosti o prostredí** LCS sa prihláste do prostredia a uistite sa, že funguje podľa očakávaní.</span><span class="sxs-lookup"><span data-stu-id="e4d87-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
