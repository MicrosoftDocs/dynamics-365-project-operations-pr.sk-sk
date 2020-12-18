---
title: Nastavenie a použitie konfiguračných údajov v Common Data Service
description: Táto téma poskytuje informácie o nastavení a použití konfiguračných údajov v Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7742e81316b217066f9f3b8d5c23aa64f1a7efc4
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642247"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="1bae8-103">Nastavenie a použitie konfiguračných údajov v Common Data Service</span><span class="sxs-lookup"><span data-stu-id="1bae8-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="1bae8-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="1bae8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="1bae8-105">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="1bae8-105">Prerequisites</span></span>

<span data-ttu-id="1bae8-106">Skôr ako začnete konfigurovať údaje v Common Data Service (CDS), musia byť splnené nasledujúce predpoklady:</span><span class="sxs-lookup"><span data-stu-id="1bae8-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="1bae8-107">Nasadenie prostredia CDS a prostredia Dynamics 365 Finance pre Project Operations.</span><span class="sxs-lookup"><span data-stu-id="1bae8-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="1bae8-108">Informácie o právnickej osobe z Dynamics 365 Finance sa zdieľajú s prostredím CDS.</span><span class="sxs-lookup"><span data-stu-id="1bae8-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="1bae8-109">To znamená, že entita **Spoločnosť** v CDS má tieto firemné záznamy:</span><span class="sxs-lookup"><span data-stu-id="1bae8-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="1bae8-110">THPM</span><span class="sxs-lookup"><span data-stu-id="1bae8-110">THPM</span></span>
  - <span data-ttu-id="1bae8-111">USPM</span><span class="sxs-lookup"><span data-stu-id="1bae8-111">USPM</span></span>
  - <span data-ttu-id="1bae8-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="1bae8-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="1bae8-113">Inštalácia údajov pre nastavenie a konfiguráciu</span><span class="sxs-lookup"><span data-stu-id="1bae8-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="1bae8-114">Stiahnite, odblokujte a rozbaľte súbor [Balík údajov nastavenia a konfigurácie](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="1bae8-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="1bae8-115">Prejdite do rozbaleného priečinka a spustite spustiteľný súbor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="1bae8-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="1bae8-116">Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="1bae8-118">Na strane 2 Sprievodcu CMT vyberte **Microsoft 365** ako **Typ nasadenia**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="1bae8-119">Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="1bae8-120">Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="1bae8-122">Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do organizáciu, do ktorej chcete importovať ukážkové údaje, a vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="1bae8-123">Na strane 4 vyberte súbor zip *SampleSetupAndConfigData* z rozbaleného priečinka.</span><span class="sxs-lookup"><span data-stu-id="1bae8-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Výber súboru ZIP](./media/3ZipFile.png)

![Výber súboru](./media/4SelectAFile.png)

9. <span data-ttu-id="1bae8-126">Po výbere súboru zip vyberte **Import údajov**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-126">After the zip file is selected, select **Import Data**.</span></span>

![Import údajov](./media/5ImportData.png)

10. <span data-ttu-id="1bae8-128">Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete.</span><span class="sxs-lookup"><span data-stu-id="1bae8-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="1bae8-129">Po dokončení importovania ukončite sprievodcu CMT.</span><span class="sxs-lookup"><span data-stu-id="1bae8-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="1bae8-130">Skontrolujte údaje svojej organizácie v nasledujúcich 19 entitách:</span><span class="sxs-lookup"><span data-stu-id="1bae8-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="1bae8-131">Mena</span><span class="sxs-lookup"><span data-stu-id="1bae8-131">Currency</span></span>
  - <span data-ttu-id="1bae8-132">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="1bae8-132">Organizational Unit</span></span>
  - <span data-ttu-id="1bae8-133">Kontakt</span><span class="sxs-lookup"><span data-stu-id="1bae8-133">Contact</span></span>
  - <span data-ttu-id="1bae8-134">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="1bae8-134">Tax Group</span></span>
  - <span data-ttu-id="1bae8-135">Skupina zákazníkov</span><span class="sxs-lookup"><span data-stu-id="1bae8-135">Customer Group</span></span>
  - <span data-ttu-id="1bae8-136">Jednotka</span><span class="sxs-lookup"><span data-stu-id="1bae8-136">Unit</span></span>
  - <span data-ttu-id="1bae8-137">Skupina jednotiek</span><span class="sxs-lookup"><span data-stu-id="1bae8-137">Unit Group</span></span>
  - <span data-ttu-id="1bae8-138">Cenník</span><span class="sxs-lookup"><span data-stu-id="1bae8-138">Price List</span></span>
  - <span data-ttu-id="1bae8-139">Cenník parametrov projektu</span><span class="sxs-lookup"><span data-stu-id="1bae8-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="1bae8-140">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="1bae8-140">Invoice Frequency</span></span>
  - <span data-ttu-id="1bae8-141">Kategória rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="1bae8-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="1bae8-142">Kategória transakcie</span><span class="sxs-lookup"><span data-stu-id="1bae8-142">Transaction Category</span></span>
  - <span data-ttu-id="1bae8-143">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="1bae8-143">Expense Category</span></span>
  - <span data-ttu-id="1bae8-144">Cena roly</span><span class="sxs-lookup"><span data-stu-id="1bae8-144">Role Price</span></span>
  - <span data-ttu-id="1bae8-145">Cena kategórie transakcie</span><span class="sxs-lookup"><span data-stu-id="1bae8-145">Transaction Category Price</span></span>
  - <span data-ttu-id="1bae8-146">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="1bae8-146">Characteristic</span></span>
  - <span data-ttu-id="1bae8-147">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="1bae8-147">Bookable Resource</span></span>
  - <span data-ttu-id="1bae8-148">Priradenie kategórie rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="1bae8-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="1bae8-149">Charakteristika rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="1bae8-149">Bookable Resource Characteristic</span></span>

![Dokončenie importu](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="1bae8-151">Aktualizujte konfigurácie Project Operations</span><span class="sxs-lookup"><span data-stu-id="1bae8-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="1bae8-152">Prejdite do prostredia CE.</span><span class="sxs-lookup"><span data-stu-id="1bae8-152">Navigate to the CE environment.</span></span> <span data-ttu-id="1bae8-153">Nájdete ho po otvorení [Power Platform Centrum spravovania](https://admin.powerplatform.microsoft.com/environments) a výberom prostredia a potom výberom **Otvorené prostredie**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvorenie prostredia](./media/7OpenEnvironment.png)

2. <span data-ttu-id="1bae8-155">Prejdite do **Projekty** > **Zdroje** a potom vyberte **Nový** na vytvorenie rezervovateľného zdroja pre vášho používateľa.</span><span class="sxs-lookup"><span data-stu-id="1bae8-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervovateľné zdroje](./media/8BookableResources.png)

3. <span data-ttu-id="1bae8-157">Na karte **Všeobecné** vyberte svojho správcu.</span><span class="sxs-lookup"><span data-stu-id="1bae8-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="1bae8-158">Skontrolujte, či sa časové pásmo zhoduje s tým, v ktorom sa nachádzate.</span><span class="sxs-lookup"><span data-stu-id="1bae8-158">Verify that the time zone matches the one you are in.</span></span> 

![Nový rezervovateľný zdroj](./media/9NewBookableResource.png)

4. <span data-ttu-id="1bae8-160">Na karte **Plánovanie** v poli **Spoločnosť** vyberte spoločnosť **USPM** a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta Plánovanie](./media/10SchedulingTab.png)

5. <span data-ttu-id="1bae8-162">Stlačte kartu **Pracovný čas**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-162">Select the **Work hours** tab.</span></span>  

![Pracovné hodiny](./media/11WorkHours.png)

6. <span data-ttu-id="1bae8-164">Dvakrát kliknite na ľubovoľnú hodnotu v kalendári a vyberte **Upraviť** > **Všetky udalosti v rade**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Pracovný kalendár](./media/12WorkCalendar.png)

7. <span data-ttu-id="1bae8-166">Zmeňte pracovný čas na osemhodinový (8) pracovný deň, víkendy označte ako dni pracovného pokoja a uistite sa, že časové pásmo zodpovedá tomu vášmu.</span><span class="sxs-lookup"><span data-stu-id="1bae8-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="1bae8-167">Vyberte položku **Uložiť a zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-167">Select **Save and close**.</span></span>

![Aktualizovanie kalendára](./media/13UpdateCalendar.png)

9. <span data-ttu-id="1bae8-169">Prejdite do **Nastavenia** > **Šablóny kalendára** a vyberte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Šablóny kalendárov](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="1bae8-171">Zadajte názov, vyberte zdroj šablóny, ktorú ste vytvorili, a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Uloženie šablóny kalendára](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="1bae8-173">Prejdite do **Parametre** a dvakrát kliknite na záznam.</span><span class="sxs-lookup"><span data-stu-id="1bae8-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametre projektu](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="1bae8-175">Aktualizujte nasledujúce polia:</span><span class="sxs-lookup"><span data-stu-id="1bae8-175">Update the following fields:</span></span>

 - <span data-ttu-id="1bae8-176">**Predvolená spoločnosť**: USPM</span><span class="sxs-lookup"><span data-stu-id="1bae8-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="1bae8-177">**Predvolená organizačná jednotka**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="1bae8-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="1bae8-178">**Frekvencia faktúr**: Siedmy a posledný deň</span><span class="sxs-lookup"><span data-stu-id="1bae8-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="1bae8-179">**Šablóna pracovného času**: Zmena na šablónu, ktorú ste vytvorili.</span><span class="sxs-lookup"><span data-stu-id="1bae8-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="1bae8-180">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="1bae8-180">Select **Save**.</span></span> 

![Aktualizované parametre projektu](./media/17UpdatedProjectParameters.png)
