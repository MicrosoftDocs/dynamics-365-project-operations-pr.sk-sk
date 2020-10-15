---
title: Použitie ukážkových údajov nastavenia a konfigurácie
description: Táto téma poskytuje informácie o tom, ako použiť ukážkové údaje nastavenia a konfigurácie pre Project Operations.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949067"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="e531e-103">Použitie ukážkových údajov nastavenia a konfigurácie pre jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma</span><span class="sxs-lookup"><span data-stu-id="e531e-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="e531e-104">_\*\*Jednoduché nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="e531e-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="e531e-105">Stiahnite si [Balík hlavných údajov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="e531e-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="e531e-106">Prejdite do priečinka *ProjOpsDemoDataSetupAndMaster – integrovaný CMT* a spustite spustiteľný súbor, *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="e531e-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="e531e-107">Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.</span><span class="sxs-lookup"><span data-stu-id="e531e-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="e531e-109">Na strane 2 Sprievodcu CMT vyberte **Office 365** ako **Typ nasadenia**.</span><span class="sxs-lookup"><span data-stu-id="e531e-109">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="e531e-110">Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.</span><span class="sxs-lookup"><span data-stu-id="e531e-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="e531e-111">Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a potom vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="e531e-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="e531e-113">Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do ktorej organizácie chcete importovať ukážkové údaje, a potom vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="e531e-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="e531e-114">Na strane 4 vyberte súbor zip, *MasterAndSetupData* z rozbaleného priečinka *ProjOpsDemoDataSetupAndMaster – integrovaný CMT*.</span><span class="sxs-lookup"><span data-stu-id="e531e-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Súbor Zip](./media/3ZipFile.png)

![Výber súboru](./media/4SelectAFile.png)

9. <span data-ttu-id="e531e-117">Po výbere súboru zip vyberte **Import údajov**.</span><span class="sxs-lookup"><span data-stu-id="e531e-117">After the zip file is selected, select **Import Data**.</span></span>

![Importovať údaje](./media/5ImportData.png)

10. <span data-ttu-id="e531e-119">Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete.</span><span class="sxs-lookup"><span data-stu-id="e531e-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="e531e-120">Po dokončení ukončite sprievodcu CMT.</span><span class="sxs-lookup"><span data-stu-id="e531e-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="e531e-121">Skontrolujte údaje svojej organizácie v nasledujúcich 20 entitách:</span><span class="sxs-lookup"><span data-stu-id="e531e-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="e531e-122">Mena</span><span class="sxs-lookup"><span data-stu-id="e531e-122">Currency</span></span>
- <span data-ttu-id="e531e-123">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="e531e-123">Organizational Unit</span></span>
- <span data-ttu-id="e531e-124">Kontakt</span><span class="sxs-lookup"><span data-stu-id="e531e-124">Contact</span></span>
- <span data-ttu-id="e531e-125">Daňová skupina</span><span class="sxs-lookup"><span data-stu-id="e531e-125">Tax Group</span></span>
- <span data-ttu-id="e531e-126">Skupina zákazníkov</span><span class="sxs-lookup"><span data-stu-id="e531e-126">Customer Group</span></span>
- <span data-ttu-id="e531e-127">Jednotka</span><span class="sxs-lookup"><span data-stu-id="e531e-127">Unit</span></span>
- <span data-ttu-id="e531e-128">Skupina jednotiek</span><span class="sxs-lookup"><span data-stu-id="e531e-128">Unit Group</span></span>
- <span data-ttu-id="e531e-129">Cenník</span><span class="sxs-lookup"><span data-stu-id="e531e-129">Price List</span></span>
- <span data-ttu-id="e531e-130">Cenník parametrov projektu</span><span class="sxs-lookup"><span data-stu-id="e531e-130">Project Parameter Price List</span></span>
- <span data-ttu-id="e531e-131">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="e531e-131">Invoice Frequency</span></span>
- <span data-ttu-id="e531e-132">Podrobnosti o frekvencii faktúr</span><span class="sxs-lookup"><span data-stu-id="e531e-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="e531e-133">Kategória rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="e531e-133">Bookable Resource Category</span></span>
- <span data-ttu-id="e531e-134">Kategória transakcie</span><span class="sxs-lookup"><span data-stu-id="e531e-134">Transaction Category</span></span>
- <span data-ttu-id="e531e-135">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="e531e-135">Expense Category</span></span>
- <span data-ttu-id="e531e-136">Cena roly</span><span class="sxs-lookup"><span data-stu-id="e531e-136">Role Price</span></span>
- <span data-ttu-id="e531e-137">Cena kategórie transakcie</span><span class="sxs-lookup"><span data-stu-id="e531e-137">Transaction Category Price</span></span>
- <span data-ttu-id="e531e-138">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="e531e-138">Characteristic</span></span>
- <span data-ttu-id="e531e-139">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="e531e-139">Bookable Resource</span></span>
- <span data-ttu-id="e531e-140">Priradenie kategórie rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="e531e-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="e531e-141">Charakteristika rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="e531e-141">Bookable Resource Characteristic</span></span>

![Dokončenie importu](./media/6CompleteImport.png)
