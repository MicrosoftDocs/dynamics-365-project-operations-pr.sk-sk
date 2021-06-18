---
title: Nastavenie a použitie konfiguračných údajov v Common Data Service
description: Táto téma poskytuje informácie o nastavení a použití konfiguračných údajov v Project Operations.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001310"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="29e62-103">Nastavenie a použitie konfiguračných údajov v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="29e62-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="29e62-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="29e62-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="29e62-105">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="29e62-105">Prerequisites</span></span>

<span data-ttu-id="29e62-106">Skôr než začnete konfigurovať údaje v službe Common Data Service (CDS), musia byť splnené nasledujúce požiadavky:</span><span class="sxs-lookup"><span data-stu-id="29e62-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="29e62-107">Nasadenie prostredia CDS a prostredia Dynamics 365 Finance pre Project Operations.</span><span class="sxs-lookup"><span data-stu-id="29e62-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="29e62-108">Informácie o právnickej osobe z Dynamics 365 Finance sa zdieľajú s prostredím CDS.</span><span class="sxs-lookup"><span data-stu-id="29e62-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="29e62-109">To znamená, že entita **Spoločnosť** v CDS má tieto firemné záznamy:</span><span class="sxs-lookup"><span data-stu-id="29e62-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="29e62-110">THPM</span><span class="sxs-lookup"><span data-stu-id="29e62-110">THPM</span></span>
  - <span data-ttu-id="29e62-111">USPM</span><span class="sxs-lookup"><span data-stu-id="29e62-111">USPM</span></span>
  - <span data-ttu-id="29e62-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="29e62-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="29e62-113">Inštalácia údajov pre nastavenie a konfiguráciu</span><span class="sxs-lookup"><span data-stu-id="29e62-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="29e62-114">Stiahnite, odblokujte a rozbaľte súbor [Balík údajov nastavenia a konfigurácie](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="29e62-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="29e62-115">Prejdite do rozbaleného priečinka a spustite spustiteľný súbor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="29e62-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="29e62-116">Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.</span><span class="sxs-lookup"><span data-stu-id="29e62-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="29e62-118">Na strane 2 Sprievodcu CMT vyberte **Microsoft 365** ako **Typ nasadenia**.</span><span class="sxs-lookup"><span data-stu-id="29e62-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="29e62-119">Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.</span><span class="sxs-lookup"><span data-stu-id="29e62-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="29e62-120">Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="29e62-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="29e62-122">Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do organizáciu, do ktorej chcete importovať ukážkové údaje, a vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="29e62-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="29e62-123">Na strane 4 vyberte súbor zip *SampleSetupAndConfigData* z rozbaleného priečinka.</span><span class="sxs-lookup"><span data-stu-id="29e62-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Výber súboru ZIP](./media/3ZipFile.png)

![Výber súboru](./media/4SelectAFile.png)

9. <span data-ttu-id="29e62-126">Po výbere súboru zip vyberte **Import údajov**.</span><span class="sxs-lookup"><span data-stu-id="29e62-126">After the zip file is selected, select **Import Data**.</span></span>

![Import údajov](./media/5ImportData.png)

10. <span data-ttu-id="29e62-128">Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete.</span><span class="sxs-lookup"><span data-stu-id="29e62-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="29e62-129">Po dokončení importovania ukončite sprievodcu CMT.</span><span class="sxs-lookup"><span data-stu-id="29e62-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="29e62-130">Skontrolujte údaje svojej organizácie v nasledujúcich 26 entitách:</span><span class="sxs-lookup"><span data-stu-id="29e62-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="29e62-131">Mena</span><span class="sxs-lookup"><span data-stu-id="29e62-131">Currency</span></span>
  - <span data-ttu-id="29e62-132">Účtovná osnova</span><span class="sxs-lookup"><span data-stu-id="29e62-132">Chart of Accounts</span></span>
  - <span data-ttu-id="29e62-133">Rozpočtový kalendár</span><span class="sxs-lookup"><span data-stu-id="29e62-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="29e62-134">Typy menových výmenných kurzov</span><span class="sxs-lookup"><span data-stu-id="29e62-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="29e62-135">Deň platby</span><span class="sxs-lookup"><span data-stu-id="29e62-135">Payment Day</span></span>
  - <span data-ttu-id="29e62-136">Platobný plán</span><span class="sxs-lookup"><span data-stu-id="29e62-136">Payment Schedule</span></span>
  - <span data-ttu-id="29e62-137">Platobná podmienka</span><span class="sxs-lookup"><span data-stu-id="29e62-137">Payment Term</span></span>
  - <span data-ttu-id="29e62-138">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="29e62-138">Organizational Unit</span></span>
  - <span data-ttu-id="29e62-139">Kontakt</span><span class="sxs-lookup"><span data-stu-id="29e62-139">Contact</span></span>
  - <span data-ttu-id="29e62-140">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="29e62-140">Tax Group</span></span>
  - <span data-ttu-id="29e62-141">Skupina zákazníkov</span><span class="sxs-lookup"><span data-stu-id="29e62-141">Customer Group</span></span>
  - <span data-ttu-id="29e62-142">Skupina dodávateľov</span><span class="sxs-lookup"><span data-stu-id="29e62-142">Vendor Group</span></span>
  - <span data-ttu-id="29e62-143">Jednotka</span><span class="sxs-lookup"><span data-stu-id="29e62-143">Unit</span></span>
  - <span data-ttu-id="29e62-144">Skupina jednotiek</span><span class="sxs-lookup"><span data-stu-id="29e62-144">Unit Group</span></span>
  - <span data-ttu-id="29e62-145">Cenník</span><span class="sxs-lookup"><span data-stu-id="29e62-145">Price List</span></span>
  - <span data-ttu-id="29e62-146">Cenník parametrov projektu</span><span class="sxs-lookup"><span data-stu-id="29e62-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="29e62-147">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="29e62-147">Invoice Frequency</span></span>
  - <span data-ttu-id="29e62-148">Kategória rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="29e62-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="29e62-149">Kategória transakcie</span><span class="sxs-lookup"><span data-stu-id="29e62-149">Transaction Category</span></span>
  - <span data-ttu-id="29e62-150">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="29e62-150">Expense Category</span></span>
  - <span data-ttu-id="29e62-151">Cena roly</span><span class="sxs-lookup"><span data-stu-id="29e62-151">Role Price</span></span>
  - <span data-ttu-id="29e62-152">Cena kategórie transakcie</span><span class="sxs-lookup"><span data-stu-id="29e62-152">Transaction Category Price</span></span>
  - <span data-ttu-id="29e62-153">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="29e62-153">Characteristic</span></span>
  - <span data-ttu-id="29e62-154">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="29e62-154">Bookable Resource</span></span>
  - <span data-ttu-id="29e62-155">Priradenie kategórie rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="29e62-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="29e62-156">Charakteristika rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="29e62-156">Bookable Resource Characteristic</span></span>

![Dokončenie importu](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="29e62-158">Aktualizujte konfigurácie Project Operations</span><span class="sxs-lookup"><span data-stu-id="29e62-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="29e62-159">Prejdite do prostredia CE.</span><span class="sxs-lookup"><span data-stu-id="29e62-159">Navigate to the CE environment.</span></span> <span data-ttu-id="29e62-160">Nájdete ho po otvorení [Power Platform Centrum spravovania](https://admin.powerplatform.microsoft.com/environments) a výberom prostredia a potom výberom **Otvorené prostredie**.</span><span class="sxs-lookup"><span data-stu-id="29e62-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvorenie prostredia](./media/7OpenEnvironment.png)

2. <span data-ttu-id="29e62-162">Prejdite do **Projekty** > **Zdroje** a potom vyberte **Nový** na vytvorenie rezervovateľného zdroja pre vášho používateľa.</span><span class="sxs-lookup"><span data-stu-id="29e62-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervovateľné zdroje](./media/8BookableResources.png)

3. <span data-ttu-id="29e62-164">Na karte **Všeobecné** vyberte svojho správcu.</span><span class="sxs-lookup"><span data-stu-id="29e62-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="29e62-165">Skontrolujte, či sa časové pásmo zhoduje s tým, v ktorom sa nachádzate.</span><span class="sxs-lookup"><span data-stu-id="29e62-165">Verify that the time zone matches the one you are in.</span></span> 

![Nový rezervovateľný zdroj](./media/9NewBookableResource.png)

4. <span data-ttu-id="29e62-167">Na karte **Plánovanie** v poli **Spoločnosť** vyberte spoločnosť **USPM** a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="29e62-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta Plánovanie](./media/10SchedulingTab.png)

5. <span data-ttu-id="29e62-169">Stlačte kartu **Pracovný čas**.</span><span class="sxs-lookup"><span data-stu-id="29e62-169">Select the **Work hours** tab.</span></span>  

![Pracovné hodiny](./media/11WorkHours.png)

6. <span data-ttu-id="29e62-171">Dvakrát kliknite na ľubovoľnú hodnotu v kalendári a vyberte **Upraviť** > **Všetky udalosti v rade**.</span><span class="sxs-lookup"><span data-stu-id="29e62-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Pracovný kalendár](./media/12WorkCalendar.png)

7. <span data-ttu-id="29e62-173">Zmeňte pracovný čas na osemhodinový (8) pracovný deň, víkendy označte ako dni pracovného pokoja a uistite sa, že časové pásmo zodpovedá tomu vášmu.</span><span class="sxs-lookup"><span data-stu-id="29e62-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="29e62-174">Vyberte položku **Uložiť a zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="29e62-174">Select **Save and close**.</span></span>

![Aktualizovanie kalendára](./media/13UpdateCalendar.png)

9. <span data-ttu-id="29e62-176">Prejdite do **Nastavenia** > **Šablóny kalendára** a vyberte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="29e62-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Šablóny kalendárov](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="29e62-178">Zadajte názov, vyberte zdroj šablóny, ktorú ste vytvorili, a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="29e62-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Uloženie šablóny kalendára](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="29e62-180">Prejdite do **Parametre** a dvakrát kliknite na záznam.</span><span class="sxs-lookup"><span data-stu-id="29e62-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametre projektu](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="29e62-182">Aktualizujte nasledujúce polia:</span><span class="sxs-lookup"><span data-stu-id="29e62-182">Update the following fields:</span></span>

 - <span data-ttu-id="29e62-183">**Predvolená spoločnosť**: USPM</span><span class="sxs-lookup"><span data-stu-id="29e62-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="29e62-184">**Predvolená organizačná jednotka**: Contoso Global Robotics</span><span class="sxs-lookup"><span data-stu-id="29e62-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="29e62-185">**Frekvencia faktúr**: Siedmy a posledný deň</span><span class="sxs-lookup"><span data-stu-id="29e62-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="29e62-186">**Šablóna pracovného času**: Zmena na šablónu, ktorú ste vytvorili.</span><span class="sxs-lookup"><span data-stu-id="29e62-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="29e62-187">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="29e62-187">Select **Save**.</span></span> 

![Aktualizované parametre projektu](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
