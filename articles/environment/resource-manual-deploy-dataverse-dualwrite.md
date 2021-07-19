---
title: Manuálne nasadenie aplikácie Project Operations Dataverse s podporou duálneho zápisu
description: Táto téma vysvetľuje, ako manuálne nasadiť aplikáciu Project Operations Dataverse tak, aby podporovala duálny zápis.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 2ad147da542fc9e7a2705da7a834d1a6512907e5
ms.sourcegitcommit: 205a94ab4168de25b102f31d00a691c8205ba63e
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/18/2021
ms.locfileid: "6274027"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a><span data-ttu-id="dfad4-103">Manuálne nasadenie aplikácie Project Operations Dataverse s podporou duálneho zápisu</span><span class="sxs-lookup"><span data-stu-id="dfad4-103">Manually deploy the Project Operations Dataverse app with dual-write support</span></span>

<span data-ttu-id="dfad4-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="dfad4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dfad4-105">Táto téma vysvetľuje, ako manuálne nasadiť aplikáciu Microsoft Dynamics 365 Project Operations v Microsoft Dataverse tak, aby podporovala duálny zápis.</span><span class="sxs-lookup"><span data-stu-id="dfad4-105">This topic explains how to manually deploy Microsoft Dynamics 365 Project Operations in Microsoft Dataverse so that it supports dual-write.</span></span> <span data-ttu-id="dfad4-106">Project Operations zistí konfiguráciu prostredia a pridá ďalšiu podporu pre duálny zápis, ak sú splnené predpoklady.</span><span class="sxs-lookup"><span data-stu-id="dfad4-106">Project Operations detects the environment's configuration and adds additional support for dual-write if the prerequisites are met.</span></span>

<span data-ttu-id="dfad4-107">Počas nasadenia do Microsoft Dynamics Lifecycle Services (LCS), ak ste postupovali podľa pokynov v tejto téme, môžete preskočiť nasadenie integrácie Microsoft Power Platform (predtým známa ako prostredie Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="dfad4-107">During deployment through Microsoft Dynamics Lifecycle Services (LCS), if you've followed the instructions in this topic, you can skip the deployment of the Microsoft Power Platform integration (previously known as the Common Data Service environment).</span></span>

<span data-ttu-id="dfad4-108">Proces nasadenia Project Operations v Dataverse, aby podporoval duálny zápis, má štyri hlavné kroky:</span><span class="sxs-lookup"><span data-stu-id="dfad4-108">The process of deploying Project Operations in Dataverse so that it supports dual-write has four main steps:</span></span>

1. <span data-ttu-id="dfad4-109">[Vytvorte nové prostredie v Dataverse, ktoré podporuje duálny zápis](#create).</span><span class="sxs-lookup"><span data-stu-id="dfad4-109">[Create a new environment in Dataverse that supports dual-write](#create).</span></span>
2. <span data-ttu-id="dfad4-110">[Pridajte do prostredia predpoklady pre duálny zápis](#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="dfad4-110">[Add dual-write prerequisites to the environment](#prerequisites).</span></span>
3. <span data-ttu-id="dfad4-111">[Pridajte aplikáciu Project Operations Dataverse](#dataverse).</span><span class="sxs-lookup"><span data-stu-id="dfad4-111">[Add the Project Operations Dataverse app](#dataverse).</span></span>
4. <span data-ttu-id="dfad4-112">[Prepojte svoje prostredia](#link).</span><span class="sxs-lookup"><span data-stu-id="dfad4-112">[Link your environments](#link).</span></span>

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a><span data-ttu-id="dfad4-113">Vytvorte nové prostredie v Dataverse, ktoré podporuje duálny zápis.</span><span class="sxs-lookup"><span data-stu-id="dfad4-113">Create a new environment in Dataverse that supports dual-write</span></span>

<span data-ttu-id="dfad4-114">Na dokončenie tohto postupu sa musíte prihlásiť ako správca.</span><span class="sxs-lookup"><span data-stu-id="dfad4-114">To complete this procedure, you must sign in as an administrator.</span></span>

1. <span data-ttu-id="dfad4-115">Otvorte [centrum správy Power Platform](https://admin.powerplatform.com) a prihláste sa ako správca.</span><span class="sxs-lookup"><span data-stu-id="dfad4-115">Open the [Power Platform admin center](https://admin.powerplatform.com), and sign in as an administrator.</span></span>
2. <span data-ttu-id="dfad4-116">Vytvorte nové prostredie a pomenujte ho.</span><span class="sxs-lookup"><span data-stu-id="dfad4-116">Create a new environment, and name it.</span></span>
3. <span data-ttu-id="dfad4-117">Vyberte typ prostredia.</span><span class="sxs-lookup"><span data-stu-id="dfad4-117">Select the environment type.</span></span> <span data-ttu-id="dfad4-118">Ak ste sa zaregistrovali na odber skúšobnej ponuky, stlačte možnosť **Skúšobná verzia (na základe predplatného)**.</span><span class="sxs-lookup"><span data-stu-id="dfad4-118">If you signed up for the trial offer, select **Trial (subscription-based)**.</span></span>
4. <span data-ttu-id="dfad4-119">Potvrďte oblasť nasadenia.</span><span class="sxs-lookup"><span data-stu-id="dfad4-119">Confirm the deployment region.</span></span>
5. <span data-ttu-id="dfad4-120">Aktivujte možnosť **Vytvoriť databázu pre toto prostredie**.</span><span class="sxs-lookup"><span data-stu-id="dfad4-120">Enable the **Create a database for this environment** option.</span></span> 
6. <span data-ttu-id="dfad4-121">Potvrďte jazyk a potom potvrďte, že mena sa zhoduje s menou vašej aplikácie Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dfad4-121">Confirm the language, and then confirm that the currency matches the currency for your Finance and Operations apps.</span></span>
7. <span data-ttu-id="dfad4-122">Aktivujte možnosť **Aplikácie Dynamics 365** a potvrďte, že je pole **Automaticky nasadiť tieto aplikácie** nastavené na **Žiadne**.</span><span class="sxs-lookup"><span data-stu-id="dfad4-122">Enable the **Dynamics 365 apps** option, and confirm that the **Automatically deploy these apps** field is set to **None**.</span></span>
8. <span data-ttu-id="dfad4-123">Ak je skupina zabezpečenia požadovaná, pridajte ju.</span><span class="sxs-lookup"><span data-stu-id="dfad4-123">Add a security group, if a security group is required.</span></span>
9. <span data-ttu-id="dfad4-124">Výberom položky **Uložiť** vytvoríte prostredie.</span><span class="sxs-lookup"><span data-stu-id="dfad4-124">Select **Save** to create the environment.</span></span>
10. <span data-ttu-id="dfad4-125">Počkajte, kým sa nasadenie nedokončí a prostredie nedosiahne stav **Pripravené**.</span><span class="sxs-lookup"><span data-stu-id="dfad4-125">Wait until the deployment is completed and the environment reaches the **Ready** state.</span></span>

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a><span data-ttu-id="dfad4-126">Pridajte do prostredia predpoklady pre duálny zápis.</span><span class="sxs-lookup"><span data-stu-id="dfad4-126">Add dual-write prerequisites to the environment</span></span>

<span data-ttu-id="dfad4-127">Podpora duálneho zápisu obsahuje ďalšie polia, ktoré sa pridávajú ku kľúčovým entitám, ako je napríklad entita **Spoločnosť**.</span><span class="sxs-lookup"><span data-stu-id="dfad4-127">Dual-write support includes additional fields that are added to key entities, such as the **Company** entity.</span></span> <span data-ttu-id="dfad4-128">Ak pridávate podporu duálneho zápisu do existujúceho prostredia, bude pravdepodobne potrebné aktualizovať údaje, aby ste podporu povolili.</span><span class="sxs-lookup"><span data-stu-id="dfad4-128">If you're adding dual-write support to an existing environment, you might have to update the data to enable the support.</span></span> <span data-ttu-id="dfad4-129">Informácie o tom, ako načítať údaje, nájdete v časti [Bootstrap údajov spoločnosti](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span><span class="sxs-lookup"><span data-stu-id="dfad4-129">For information about how to bootstrap the data, see [Bootstrap company data](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data).</span></span> <span data-ttu-id="dfad4-130">Ďalšie informácie o duálnom zápise nájdete v časti [Systémové požiadavky pre duálny zápis](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span><span class="sxs-lookup"><span data-stu-id="dfad4-130">For more information about dual-write, see [Dual-write system requirements](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).</span></span>

<span data-ttu-id="dfad4-131">Dokončením tohto postupu pridáte do svojho prostredia predpoklady pre duálny zápis.</span><span class="sxs-lookup"><span data-stu-id="dfad4-131">Complete this procedure to add the dual-write prerequisites to your environment.</span></span>

1. <span data-ttu-id="dfad4-132">Otvorte prostredie, ktoré ste práve vytvorili, a potom prejdite do ponuky **Zdroj** \> **Aplikácie Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="dfad4-132">Open the environment that you just created, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="dfad4-133">V zozname aplikácii stlačte možnosť **Základné riešenie duálneho zápisu** a nainštalujte ho.</span><span class="sxs-lookup"><span data-stu-id="dfad4-133">Select **Dual-write core solution** in the app list, and install it.</span></span>
3. <span data-ttu-id="dfad4-134">Počkajte, kým sa inštalácia nedokončí.</span><span class="sxs-lookup"><span data-stu-id="dfad4-134">Wait until the installation is completed.</span></span> <span data-ttu-id="dfad4-135">Potom stlačte v zozname aplikácii možnosť **Riešenie orchestrácie aplikácie duálneho zápisu** a nainštalujte ju.</span><span class="sxs-lookup"><span data-stu-id="dfad4-135">Then select **Dual-write application orchestration solution** in the app list, and install it.</span></span>

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a><span data-ttu-id="dfad4-136">Pridanie aplikácie Project Operations Dataverse</span><span class="sxs-lookup"><span data-stu-id="dfad4-136">Add the Project Operations Dataverse app</span></span>

<span data-ttu-id="dfad4-137">Tento postup môžete dokončiť, iba ak ste pred inštaláciou Project Operations dokončili predchádzajúce postupy.</span><span class="sxs-lookup"><span data-stu-id="dfad4-137">You can complete this procedure only if you completed the previous procedures before you installed Project Operations.</span></span> <span data-ttu-id="dfad4-138">Počas inštalácie systém analyzuje konfiguráciu prostredia a v prípade potreby pridáva podporu pre duálny zápis.</span><span class="sxs-lookup"><span data-stu-id="dfad4-138">During installation, the system analyzes the environment configuration and adds support for dual-write if it's required.</span></span>

1. <span data-ttu-id="dfad4-139">Otvorte prostredie, ktoré ste vytvorili predtým, a potom prejdite do ponuky **Zdroj** \> **Aplikácie Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="dfad4-139">Open the environment that you created earlier, and then go to **Resource** \> **Dynamics 365 apps**.</span></span>
2. <span data-ttu-id="dfad4-140">V zozname aplikácií stlačte možnosť **Microsoft Dynamics 365 Project Operations** a nainštalujte ju.</span><span class="sxs-lookup"><span data-stu-id="dfad4-140">Select **Microsoft Dynamics 365 Project Operations** in the app list, and install it.</span></span>

## <a name="link-your-environments"></a><a name="link"></a><span data-ttu-id="dfad4-141">Prepojte svoje prostredia</span><span class="sxs-lookup"><span data-stu-id="dfad4-141">Link your environments</span></span>

<span data-ttu-id="dfad4-142">Po nasadení prostredia Dataverse môžete vytvoriť prepojenie s aplikáciami Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="dfad4-142">After the Dataverse environment is deployed, you can set up the link in your Finance and Operations apps.</span></span> <span data-ttu-id="dfad4-143">Postupujte podľa pokynov v časti [Na prepojenie prostredí použite sprievodcu dvojitým zápisom](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span><span class="sxs-lookup"><span data-stu-id="dfad4-143">Follow the steps in [Use the dual-write wizard to link your environments](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).</span></span>
