---
title: Nastavenie a použitie konfiguračných údajov v službe Common Data Service pre Project Operations
description: Táto téma poskytuje informácie o nastavení a použití konfiguračných údajov v Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949070"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="e15dd-103">Nastavenie a použitie konfiguračných údajov v službe Common Data Service pre Project Operations</span><span class="sxs-lookup"><span data-stu-id="e15dd-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="e15dd-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="e15dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="e15dd-105">Inštalácia údajov pre nastavenie a konfiguráciu</span><span class="sxs-lookup"><span data-stu-id="e15dd-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="e15dd-106">Stiahnite, odblokujte a rozbaľte súbor [Balík údajov nastavenia a konfigurácie](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="e15dd-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="e15dd-107">Prejdite do rozbaleného priečinka a spustite spustiteľný súbor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e15dd-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e15dd-108">Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e15dd-110">Na strane 2 Sprievodcu CMT vyberte **Office 365** ako **Typ nasadenia**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e15dd-111">Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e15dd-112">Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e15dd-114">Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do organizáciu, do ktorej chcete importovať ukážkové údaje, a vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="e15dd-115">Na strane 4 vyberte súbor zip *SampleSetupAndConfigData* z rozbaleného priečinka.</span><span class="sxs-lookup"><span data-stu-id="e15dd-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Výber súboru ZIP](./media/3ZipFile.png)

![Výber súboru](./media/4SelectAFile.png)

9. <span data-ttu-id="e15dd-118">Po výbere súboru zip vyberte **Import údajov**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-118">After the zip file is selected, select **Import Data**.</span></span>

![Import údajov](./media/5ImportData.png)

10. <span data-ttu-id="e15dd-120">Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete.</span><span class="sxs-lookup"><span data-stu-id="e15dd-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e15dd-121">Po dokončení importovania ukončite sprievodcu CMT.</span><span class="sxs-lookup"><span data-stu-id="e15dd-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e15dd-122">Skontrolujte údaje svojej organizácie v nasledujúcich 19 entitách:</span><span class="sxs-lookup"><span data-stu-id="e15dd-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="e15dd-123">Mena</span><span class="sxs-lookup"><span data-stu-id="e15dd-123">Currency</span></span>
  - <span data-ttu-id="e15dd-124">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="e15dd-124">Organizational Unit</span></span>
  - <span data-ttu-id="e15dd-125">Kontakt</span><span class="sxs-lookup"><span data-stu-id="e15dd-125">Contact</span></span>
  - <span data-ttu-id="e15dd-126">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="e15dd-126">Tax Group</span></span>
  - <span data-ttu-id="e15dd-127">Skupina zákazníkov</span><span class="sxs-lookup"><span data-stu-id="e15dd-127">Customer Group</span></span>
  - <span data-ttu-id="e15dd-128">Jednotka</span><span class="sxs-lookup"><span data-stu-id="e15dd-128">Unit</span></span>
  - <span data-ttu-id="e15dd-129">Skupina jednotiek</span><span class="sxs-lookup"><span data-stu-id="e15dd-129">Unit Group</span></span>
  - <span data-ttu-id="e15dd-130">Cenník</span><span class="sxs-lookup"><span data-stu-id="e15dd-130">Price List</span></span>
  - <span data-ttu-id="e15dd-131">Cenník parametrov projektu</span><span class="sxs-lookup"><span data-stu-id="e15dd-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="e15dd-132">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="e15dd-132">Invoice Frequency</span></span>
  - <span data-ttu-id="e15dd-133">Kategória rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="e15dd-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="e15dd-134">Kategória transakcie</span><span class="sxs-lookup"><span data-stu-id="e15dd-134">Transaction Category</span></span>
  - <span data-ttu-id="e15dd-135">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="e15dd-135">Expense Category</span></span>
  - <span data-ttu-id="e15dd-136">Cena roly</span><span class="sxs-lookup"><span data-stu-id="e15dd-136">Role Price</span></span>
  - <span data-ttu-id="e15dd-137">Cena kategórie transakcie</span><span class="sxs-lookup"><span data-stu-id="e15dd-137">Transaction Category Price</span></span>
  - <span data-ttu-id="e15dd-138">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="e15dd-138">Characteristic</span></span>
  - <span data-ttu-id="e15dd-139">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="e15dd-139">Bookable Resource</span></span>
  - <span data-ttu-id="e15dd-140">Priradenie kategórie rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="e15dd-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="e15dd-141">Charakteristika rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="e15dd-141">Bookable Resource Characteristic</span></span>

![Dokončenie importu](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="e15dd-143">Aktualizujte konfigurácie Project Operations</span><span class="sxs-lookup"><span data-stu-id="e15dd-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="e15dd-144">Prejdite do prostredia CE.</span><span class="sxs-lookup"><span data-stu-id="e15dd-144">Navigate to the CE environment.</span></span> <span data-ttu-id="e15dd-145">Nájdete ho po otvorení [Power Platform Centrum spravovania](https://admin.powerplatform.microsoft.com/environments) a výberom prostredia a potom výberom **Otvorené prostredie**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Otvorenie prostredia](./media/7OpenEnvironment.png)

2. <span data-ttu-id="e15dd-147">Prejdite do **Projekty** > **Zdroje** a potom vyberte **Nový** na vytvorenie rezervovateľného zdroja pre vášho používateľa.</span><span class="sxs-lookup"><span data-stu-id="e15dd-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervovateľné zdroje](./media/8BookableResources.png)

3. <span data-ttu-id="e15dd-149">Na karte **Všeobecné** vyberte svojho správcu.</span><span class="sxs-lookup"><span data-stu-id="e15dd-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="e15dd-150">Skontrolujte, či sa časové pásmo zhoduje s tým, v ktorom sa nachádzate.</span><span class="sxs-lookup"><span data-stu-id="e15dd-150">Verify that the time zone matches the one you are in.</span></span> 

![Nový rezervovateľný zdroj](./media/9NewBookableResource.png)

4. <span data-ttu-id="e15dd-152">Na karte **Plánovanie** v poli **Spoločnosť** vyberte spoločnosť **USPM** a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Karta Plánovanie](./media/10SchedulingTab.png)

5. <span data-ttu-id="e15dd-154">Stlačte kartu **Pracovný čas**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-154">Select the **Work hours** tab.</span></span>  

![Pracovné hodiny](./media/11WorkHours.png)

6. <span data-ttu-id="e15dd-156">Dvakrát kliknite na ľubovoľnú hodnotu v kalendári a vyberte **Upraviť** > **Všetky udalosti v rade**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Pracovný kalendár](./media/12WorkCalendar.png)

7. <span data-ttu-id="e15dd-158">Zmeňte pracovný čas na osemhodinový (8) pracovný deň, víkendy označte ako dni pracovného pokoja a uistite sa, že časové pásmo zodpovedá tomu vášmu.</span><span class="sxs-lookup"><span data-stu-id="e15dd-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="e15dd-159">Vyberte položku **Uložiť a zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-159">Select **Save and close**.</span></span>

![Aktualizovanie kalendára](./media/13UpdateCalendar.png)

9. <span data-ttu-id="e15dd-161">Prejdite do **Nastavenia** > **Šablóny kalendára** a vyberte **Nová**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Šablóny kalendárov](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="e15dd-163">Zadajte názov, vyberte zdroj šablóny, ktorú ste vytvorili, a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Uloženie šablóny kalendára](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="e15dd-165">Prejdite do **Parametre** a dvakrát kliknite na záznam.</span><span class="sxs-lookup"><span data-stu-id="e15dd-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Parametre projektu](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="e15dd-167">Aktualizujte nasledujúce polia:</span><span class="sxs-lookup"><span data-stu-id="e15dd-167">Update the following fields:</span></span>

 - <span data-ttu-id="e15dd-168">**Predvolená spoločnosť**: USPM</span><span class="sxs-lookup"><span data-stu-id="e15dd-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="e15dd-169">**Predvolená organizačná jednotka**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="e15dd-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="e15dd-170">**Frekvencia faktúr**: Siedmy a posledný deň</span><span class="sxs-lookup"><span data-stu-id="e15dd-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="e15dd-171">**Šablóna pracovného času**: Zmena na šablónu, ktorú ste vytvorili.</span><span class="sxs-lookup"><span data-stu-id="e15dd-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="e15dd-172">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="e15dd-172">Select **Save**.</span></span> 

![Aktualizované parametre projektu](./media/17UpdatedProjectParameters.png)
