---
title: Použitie ukážkových údajov nastavenia a konfigurácie – čiastočné
description: Táto téma poskytuje informácie o tom, ako použiť ukážkové údaje nastavenia a konfigurácie pre Project Operations.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997170"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="f3865-103">Použitie ukážkových údajov nastavenia a konfigurácie pre Project Operations – čiastočné</span><span class="sxs-lookup"><span data-stu-id="f3865-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="f3865-104">_\*\*Jednoduché nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="f3865-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f3865-105">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="f3865-105">Prerequisites</span></span>

<span data-ttu-id="f3865-106">Pred začatím konfigurácie musíte mať zriadené prostredie Common Data Service (CDS) pre Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="f3865-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="f3865-107">Pokyny</span><span class="sxs-lookup"><span data-stu-id="f3865-107">Instructions</span></span>

1. <span data-ttu-id="f3865-108">Stiahnite si [Balík hlavných údajov](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="f3865-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="f3865-109">Prejdite do priečinka *ProjOpsSampleSetupData - iba CMT s CE* a spustite spustiteľný súbor *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f3865-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f3865-110">Na strane 1 Common Data Service Sprievodcu migráciou konfigurácie (CMT) vyberte **Import údajov** a potom vyberte **Pokračovať**.</span><span class="sxs-lookup"><span data-stu-id="f3865-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Migrácia konfigurácie](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f3865-112">Na strane 2 Sprievodcu CMT vyberte **Microsoft 365** ako **Typ nasadenia**.</span><span class="sxs-lookup"><span data-stu-id="f3865-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f3865-113">Vyberte možnosť **Zobraziť zoznam dostupných organizácií** a začiarkavacie políčka **Zobraziť rozšírené**.</span><span class="sxs-lookup"><span data-stu-id="f3865-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f3865-114">Vyberte oblasť svojho nájomníka, zadajte svoje poverenia a potom vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="f3865-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Prihlásenie do konfigurácie](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f3865-116">Na strane 3 zo zoznamu Organizácie v časti Nájomník vyberte, do ktorej organizácie chcete importovať ukážkové údaje, a potom vyberte **Prihlásiť sa**.</span><span class="sxs-lookup"><span data-stu-id="f3865-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f3865-117">Na strane 4 vyberte súbor .zip *SampleSetupAndConfigData* z rozbaleného priečinka *ProjOpsSampleSetupData - iba CMT s CE*.</span><span class="sxs-lookup"><span data-stu-id="f3865-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Súbor Zip](./media/3ZipFile.png)

   ![Vybrať súbor](./media/4SelectAFile.png)

9. <span data-ttu-id="f3865-120">Po výbere súboru zip vyberte **Import údajov**.</span><span class="sxs-lookup"><span data-stu-id="f3865-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importovať údaje](./media/5ImportData.png)

10. <span data-ttu-id="f3865-122">Import bude trvať približne dve až desať minút v závislosti od rýchlosti vašej siete.</span><span class="sxs-lookup"><span data-stu-id="f3865-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f3865-123">Po dokončení ukončite sprievodcu CMT.</span><span class="sxs-lookup"><span data-stu-id="f3865-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f3865-124">Skontrolujte údaje svojej organizácie v nasledujúcich 18 entitách:</span><span class="sxs-lookup"><span data-stu-id="f3865-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="f3865-125">Mena</span><span class="sxs-lookup"><span data-stu-id="f3865-125">Currency</span></span>
    -   <span data-ttu-id="f3865-126">Konto</span><span class="sxs-lookup"><span data-stu-id="f3865-126">Account</span></span>
    -   <span data-ttu-id="f3865-127">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="f3865-127">Organizational Unit</span></span>
    -   <span data-ttu-id="f3865-128">Kontakt</span><span class="sxs-lookup"><span data-stu-id="f3865-128">Contact</span></span>
    -   <span data-ttu-id="f3865-129">Jednotka</span><span class="sxs-lookup"><span data-stu-id="f3865-129">Unit</span></span>
    -   <span data-ttu-id="f3865-130">Skupina jednotiek</span><span class="sxs-lookup"><span data-stu-id="f3865-130">Unit Group</span></span>
    -   <span data-ttu-id="f3865-131">Cenník</span><span class="sxs-lookup"><span data-stu-id="f3865-131">Price List</span></span>
    -   <span data-ttu-id="f3865-132">Cenník parametrov projektu</span><span class="sxs-lookup"><span data-stu-id="f3865-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="f3865-133">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="f3865-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="f3865-134">Kategória rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="f3865-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="f3865-135">Kategória transakcie</span><span class="sxs-lookup"><span data-stu-id="f3865-135">Transaction Category</span></span>
    -   <span data-ttu-id="f3865-136">Kategória výdavku</span><span class="sxs-lookup"><span data-stu-id="f3865-136">Expense Category</span></span>
    -   <span data-ttu-id="f3865-137">Cena roly</span><span class="sxs-lookup"><span data-stu-id="f3865-137">Role Price</span></span>
    -   <span data-ttu-id="f3865-138">Cena kategórie transakcie</span><span class="sxs-lookup"><span data-stu-id="f3865-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="f3865-139">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="f3865-139">Characteristic</span></span>
    -   <span data-ttu-id="f3865-140">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="f3865-140">Bookable Resource</span></span>
    -   <span data-ttu-id="f3865-141">Priradenie kategórie rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="f3865-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="f3865-142">Charakteristika rezervovateľného zdroja</span><span class="sxs-lookup"><span data-stu-id="f3865-142">Bookable Resource Characteristic</span></span>

    ![Dokončenie importu](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
