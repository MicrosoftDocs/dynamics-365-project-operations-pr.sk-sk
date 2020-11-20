---
title: Použitie ukážkových údajov nastavenia a konfigurácie – čiastočné
description: Táto téma poskytuje informácie o tom, ako použiť ukážkové údaje nastavenia a konfigurácie pre Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5cfc270c07a568d692f6cd180b9c367ae185044c
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401282"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="beecf-103">Použitie ukážkových údajov nastavenia a konfigurácie pre Project Operations – čiastočné</span><span class="sxs-lookup"><span data-stu-id="beecf-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="beecf-104">_\*\*Jednoduché nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="beecf-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

## <a name="prerequisites"></a><span data-ttu-id="beecf-105">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="beecf-105">Prerequisites</span></span>

<span data-ttu-id="beecf-106">Pred začatím konfigurácie musíte mať zriadené prostredie Common Data Service (CDS) pre Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="beecf-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="beecf-107">Pokyny</span><span class="sxs-lookup"><span data-stu-id="beecf-107">Instructions</span></span>

1. <span data-ttu-id="beecf-108">Stiahnite si [Balík hlavných údajov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="beecf-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="beecf-109">Prejdite do priečinka *ProjOpsDemoDataSetupAndMaster – integrovaný CMT* a spustite spustiteľný súbor, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="beecf-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="beecf-110">Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.</span><span class="sxs-lookup"><span data-stu-id="beecf-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="beecf-112">Na strane 2 Sprievodcu CMT vyberte **Microsoft 365** ako **Typ nasadenia**.</span><span class="sxs-lookup"><span data-stu-id="beecf-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="beecf-113">Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.</span><span class="sxs-lookup"><span data-stu-id="beecf-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="beecf-114">Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a potom vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="beecf-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="beecf-116">Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do ktorej organizácie chcete importovať ukážkové údaje, a potom vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="beecf-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="beecf-117">Na strane 4 vyberte súbor zip, *MasterAndSetupData* z rozbaleného priečinka *ProjOpsDemoDataSetupAndMaster – integrovaný CMT*.</span><span class="sxs-lookup"><span data-stu-id="beecf-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Súbor Zip](./media/3ZipFile.png)

![Výber súboru](./media/4SelectAFile.png)

9. <span data-ttu-id="beecf-120">Po výbere súboru zip vyberte **Import údajov**.</span><span class="sxs-lookup"><span data-stu-id="beecf-120">After the zip file is selected, select **Import Data**.</span></span>

![Importovať údaje](./media/5ImportData.png)

10. <span data-ttu-id="beecf-122">Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete.</span><span class="sxs-lookup"><span data-stu-id="beecf-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="beecf-123">Po dokončení ukončite sprievodcu CMT.</span><span class="sxs-lookup"><span data-stu-id="beecf-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="beecf-124">Skontrolujte údaje svojej organizácie v nasledujúcich 20 entitách:</span><span class="sxs-lookup"><span data-stu-id="beecf-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="beecf-125">Mena</span><span class="sxs-lookup"><span data-stu-id="beecf-125">Currency</span></span>
-   <span data-ttu-id="beecf-126">Konto</span><span class="sxs-lookup"><span data-stu-id="beecf-126">Account</span></span>
-   <span data-ttu-id="beecf-127">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="beecf-127">Organizational Unit</span></span>
-   <span data-ttu-id="beecf-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="beecf-128">Contact</span></span>
-   <span data-ttu-id="beecf-129">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="beecf-129">Tax Group</span></span>
-   <span data-ttu-id="beecf-130">Skupina zákazníkov</span><span class="sxs-lookup"><span data-stu-id="beecf-130">Customer Group</span></span>
-   <span data-ttu-id="beecf-131">Jednotka</span><span class="sxs-lookup"><span data-stu-id="beecf-131">Unit</span></span>
-   <span data-ttu-id="beecf-132">Skupina jednotiek</span><span class="sxs-lookup"><span data-stu-id="beecf-132">Unit Group</span></span>
-   <span data-ttu-id="beecf-133">Cenník</span><span class="sxs-lookup"><span data-stu-id="beecf-133">Price List</span></span>
-   <span data-ttu-id="beecf-134">Cenník parametrov projektu</span><span class="sxs-lookup"><span data-stu-id="beecf-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="beecf-135">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="beecf-135">Invoice Frequency</span></span>
-   <span data-ttu-id="beecf-136">Kategória rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="beecf-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="beecf-137">Kategória transakcie</span><span class="sxs-lookup"><span data-stu-id="beecf-137">Transaction Category</span></span>
-   <span data-ttu-id="beecf-138">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="beecf-138">Expense Category</span></span>
-   <span data-ttu-id="beecf-139">Cena roly</span><span class="sxs-lookup"><span data-stu-id="beecf-139">Role Price</span></span>
-   <span data-ttu-id="beecf-140">Cena kategórie transakcie</span><span class="sxs-lookup"><span data-stu-id="beecf-140">Transaction Category Price</span></span>
-   <span data-ttu-id="beecf-141">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="beecf-141">Characteristic</span></span>
-   <span data-ttu-id="beecf-142">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="beecf-142">Bookable Resource</span></span>
-   <span data-ttu-id="beecf-143">Priradenie kategórie rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="beecf-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="beecf-144">Charakteristika rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="beecf-144">Bookable Resource Characteristic</span></span>

![Dokončenie importu](./media/6CompleteImport.png)
