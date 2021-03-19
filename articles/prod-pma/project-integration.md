---
title: Integrácia služby Microsoft Project Client
description: Plánovanie a údržba plánu projektu môžu byť zložité, takže projektoví manažéri musia používať nástroje, ktoré im pomáhajú zvládnuť túto úlohu. Integrácia so službou Microsoft Project Client poskytuje podporu pre otvorenie a správu štruktúry rozdelenia práce na projekte.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: e93d23559d1f3aca9022cd97dae3b0726bb5ca05
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289343"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="c67b6-104">Integrácia služby Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="c67b6-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c67b6-105">Plánovanie a údržba plánu projektu môžu byť zložité, takže projektoví manažéri musia používať nástroje, ktoré im pomáhajú zvládnuť túto úlohu.</span><span class="sxs-lookup"><span data-stu-id="c67b6-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="c67b6-106">Integrácia so službou Microsoft Project Client poskytuje podporu pre otvorenie a správu štruktúry rozdelenia práce na projekte.</span><span class="sxs-lookup"><span data-stu-id="c67b6-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="c67b6-107">Manažér projektu môže akékoľvek zmeny zverejniť späť do štruktúry rozdelenia práce na projekte v Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="c67b6-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="c67b6-108">Ak používate júlovú aktualizáciu (verzia 10.0.4), musíte si nainštalovať KB 4054797 a 4055884.</span><span class="sxs-lookup"><span data-stu-id="c67b6-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="c67b6-109">Konfigurácia doplnku Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="c67b6-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="c67b6-110">Pre umožnenie integrácie s Microsoft Project Client musí byť nainštalovaný doplnok Microsoft Dynamics 365 v klientskej aplikácii Microsoft Project používateľa.</span><span class="sxs-lookup"><span data-stu-id="c67b6-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="c67b6-111">To sa deje otvorením **Pracovného priestoru riadenia projektu**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="c67b6-112">•   Kliknite na **Konfigurácia doplnku Project Client** zo sekcie **Odkazy** > **Nastavenie** pracovného priestoru.</span><span class="sxs-lookup"><span data-stu-id="c67b6-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="c67b6-113">•   Kliknite na **Otvoriť** a po výzve na **Spustiť**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-113">•   Click **Open**, then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="c67b6-114">Otvorte a upravte existujúci koncept štruktúry rozdelenia práce Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="c67b6-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="c67b6-115">Ak má projekt v Dynamics 365 Finance už má vytvorenú štruktúru rozdelenia práce, štruktúru rozdelenia práce je možné otvoriť v aplikácii Microsoft Project Client, ak je štruktúra rozdelenia práce v stave konceptu.</span><span class="sxs-lookup"><span data-stu-id="c67b6-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="c67b6-116">Ak ju chcete otvoriť zo stránky **Projekt**, kliknite na odkaz **Otvoriť v Microsoft Project** na karte **Plán**. Túto stránku je tiež možné otvoriť v rámci aplikácie Microsoft Project Client kliknutím na **Otvoriť** v **Microsoft Dynamics 365**. Zo zoznamu vyberte **Právnická osoba** a **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="c67b6-117">Ak používate ako prehliadač Internet Explorer, budete musieť kliknúť na **Uložiť** a manuálne otvoriť z umiestnenia, do ktorého sa súbor stiahne.</span><span class="sxs-lookup"><span data-stu-id="c67b6-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="c67b6-118">Alebo kliknite na **Uložiť a otvoriť**, čím sa súbor otvorí v Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="c67b6-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="c67b6-119">Pri ukladaní nepremenujte názov súboru.</span><span class="sxs-lookup"><span data-stu-id="c67b6-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="c67b6-120">Pred vykonaním akýchkoľvek úprav súboru pomocou programu Microsoft Project Client je potrebné vykonať kontrolu. Kliknite na kartu **Odhlásiť** na karte **Microsoft Dynamics 365**. Toto zabráni ostatným používateľom súčasne upravovať štruktúru rozdelenia práce v rámci aplikácie Finance.</span><span class="sxs-lookup"><span data-stu-id="c67b6-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="c67b6-121">Ak chcete zverejniť štruktúru rozdelenia práce po dokončení akýchkoľvek úprav, kliknite na **Prihlásiť** na karte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="c67b6-122">Ak už bol projektový tím pridaný do projektu v službe Finance, zoznam zdrojov sa vyplní členmi tímu.</span><span class="sxs-lookup"><span data-stu-id="c67b6-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="c67b6-123">Ak do projektu ešte nebol pridaný projektový tím, môžete vybrať zdroje a vytvoriť tím v rámci Microsoft Project Client kliknutím na tlačidlo **Zdroje** na karte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="c67b6-124">Nasledujúce údaje budú v rámci procesu registrácie synchronizované späť do služby Finance:</span><span class="sxs-lookup"><span data-stu-id="c67b6-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="c67b6-125">•   Názov úlohy</span><span class="sxs-lookup"><span data-stu-id="c67b6-125">•   Task name</span></span>

<span data-ttu-id="c67b6-126">•   Počiatočný dátum</span><span class="sxs-lookup"><span data-stu-id="c67b6-126">•   Start date</span></span>

<span data-ttu-id="c67b6-127">•   Dátum dokončenia</span><span class="sxs-lookup"><span data-stu-id="c67b6-127">•   Finish date</span></span>

<span data-ttu-id="c67b6-128">•   Predchodcovia</span><span class="sxs-lookup"><span data-stu-id="c67b6-128">•   Predecessors</span></span>

<span data-ttu-id="c67b6-129">•   Názvy zdrojov</span><span class="sxs-lookup"><span data-stu-id="c67b6-129">•   Resource names</span></span>

<span data-ttu-id="c67b6-130">•   Kategória</span><span class="sxs-lookup"><span data-stu-id="c67b6-130">•   Category</span></span>

<span data-ttu-id="c67b6-131">•   Kategória zdroja</span><span class="sxs-lookup"><span data-stu-id="c67b6-131">•   Resource category</span></span>

<span data-ttu-id="c67b6-132">•   Pracovné hodiny</span><span class="sxs-lookup"><span data-stu-id="c67b6-132">•   Work hours</span></span>

<span data-ttu-id="c67b6-133">•   Poznámky</span><span class="sxs-lookup"><span data-stu-id="c67b6-133">•   Notes</span></span>

<span data-ttu-id="c67b6-134">•   Priorita</span><span class="sxs-lookup"><span data-stu-id="c67b6-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="c67b6-135">Ak do svojho súboru Microsoft Project Client pridáte ďalšie stĺpce, neuložia sa do súboru a nezobrazia sa pri opätovnom otvorení súboru.</span><span class="sxs-lookup"><span data-stu-id="c67b6-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="c67b6-136">Vytvorte štruktúru rozdelenia práce pre existujúci projekt pomocou Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="c67b6-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="c67b6-137">Ak chcete vytvoriť novú štruktúru rozdelenia práce pomocou Microsoft Project Client, postupujte podľa nasledujúcich pokynov:</span><span class="sxs-lookup"><span data-stu-id="c67b6-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="c67b6-138">Otvorte Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="c67b6-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="c67b6-139">Na karte **Microsoft Dynamics 365** kliknite na položku **Otvoriť**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="c67b6-140">Vyberte **Právnu entitu** pre projekt.</span><span class="sxs-lookup"><span data-stu-id="c67b6-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="c67b6-141">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="c67b6-142">Kliknite na **Odhlásiť** na karte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="c67b6-143">Keď ste pripravení na zverejnenie v službe Finance, kliknite na ikonu **Prihlásiť** na karte **Microsoft Dynamics 365**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="c67b6-144">Výmena existujúcej štruktúry rozdelenia práce pre existujúci projekt pomocou Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="c67b6-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="c67b6-145">Ak chcete vytvoriť novú štruktúru rozdelenia práce pomocou Microsoft Project Client a nahradiť existujúcu štruktúru rozdelenia práce pre existujúci projekt, postupujte nasledovne:</span><span class="sxs-lookup"><span data-stu-id="c67b6-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="c67b6-146">Otvorte Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="c67b6-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="c67b6-147">Vytvorte plán v Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="c67b6-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="c67b6-148">Na karte **Microsoft Dynamics 365** Kliknite na **Uložiť zmeny** > **Nahradiť existujúci projekt**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="c67b6-149">Vyberte **Právnu entitu** pre projekt.</span><span class="sxs-lookup"><span data-stu-id="c67b6-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="c67b6-150">Vyberte **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="c67b6-151">Kliknite na tlačidlo **OK**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="c67b6-152">Vytvorenie nového projektu v rámci Microsoft Project Client</span><span class="sxs-lookup"><span data-stu-id="c67b6-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="c67b6-153">Otvorte Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="c67b6-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="c67b6-154">Vytvorte plán v Microsoft Project Client.</span><span class="sxs-lookup"><span data-stu-id="c67b6-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="c67b6-155">Na karte **Microsoft Dynamics 365** kliknite na **Uložiť zmeny** > **Uložiť do nového projektu**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="c67b6-156">Vyberte **Právnu entitu** pre projekt.</span><span class="sxs-lookup"><span data-stu-id="c67b6-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="c67b6-157">V prípade potreby zadajte **ID projektu**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-157">Enter the **Project ID**, if necessary.</span></span>

6.  <span data-ttu-id="c67b6-158">Zadajte **Názov produktu**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="c67b6-159">Vyberte **Typ projektu**, **Projektová skupina** a **ID projektovej zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-159">Select the **Project type**, **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="c67b6-160">Prípadne môžete vytvoriť novú projektovú zmluvu kliknutím na **Nová**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="c67b6-161">Vyberte **Kalendár**, ktorý sa má použiť na zabezpečenie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="c67b6-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="c67b6-162">Kliknite na tlačidlo **OK**.</span><span class="sxs-lookup"><span data-stu-id="c67b6-162">Click **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]