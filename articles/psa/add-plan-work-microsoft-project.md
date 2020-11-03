---
title: Použite doplnok Project Service na plánovanie práce v Microsoft Project | MicrosoftDocs
description: Táto téma poskytuje informácie o tom ako pridávať, konfigurovať a používať doplnok Microsoft Project add-in pre službu Microsoft Project Service.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 04/06/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 1d988419ae5a9d57532902d2553cd7de147e27c1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084494"
---
# <a name="use-the-project-service-automation-add-in-to-plan-your-work-in-microsoft-project"></a><span data-ttu-id="51569-103">Použite doplnok Project Service Automation na plánovanie práce v Microsoft Project</span><span class="sxs-lookup"><span data-stu-id="51569-103">Use the Project Service Automation Add-in to plan your work in Microsoft Project</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] <span data-ttu-id="51569-104">vám zjednodušuje plánovanie projektov vrátane odhadov.</span><span class="sxs-lookup"><span data-stu-id="51569-104">makes it easier for you to do your project planning, including estimates.</span></span> <span data-ttu-id="51569-105">Môžete si definovať prácu tak, aby náklady, úsilie a predajná hodnota boli jasné pri odoslaní finálneho návrhu.</span><span class="sxs-lookup"><span data-stu-id="51569-105">You can define the work so that costs, effort, and sales value are clear as the final proposal is submitted.</span></span>  

 <span data-ttu-id="51569-106">Teraz môžete nainštalovať [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] a naplánovať si svoju prácu v známom prostredí [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-106">Now you can install the [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] and do your planning work in the familiar environment of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span> <span data-ttu-id="51569-107">Použite robustné možnosti plánovania a správy [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a následne si aktualizujte svoj plán projektu v Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51569-107">Use the robust planning and management capabilities of [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and then update your project plan in Project Service Automation.</span></span>  

> [!IMPORTANT]
> - <span data-ttu-id="51569-108">Na použitie správy dokumentov SharePoint na ukladanie vašich súborov [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] pre projekty [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], váš správca [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] vám bude musieť zapnúť funkciu správy dokumentov.</span><span class="sxs-lookup"><span data-stu-id="51569-108">To use SharePoint document management to store your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] files for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projects, your [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] admin will need to turn on document management.</span></span> 
> - <span data-ttu-id="51569-109">[!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] je kompatibilné len s [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span><span class="sxs-lookup"><span data-stu-id="51569-109">The [!INCLUDE[pn_ms_dyn_365_psa_for_ms_project](../includes/pn-ms-dyn-365-psa-for-ms-project.md)] is only compatible with [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] 2016 Professional Edition.</span></span>  

## <a name="download-and-install-the-add-in"></a><span data-ttu-id="51569-110">Stiahnite a nainštalujte si doplnok</span><span class="sxs-lookup"><span data-stu-id="51569-110">Download and install the add-in</span></span>  
 <span data-ttu-id="51569-111">Pripravte si svoje prihlasovacie informácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-111">Have your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] sign-in information ready.</span></span> <span data-ttu-id="51569-112">Tieto informácie budete potrebovať na pripojenie z [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-112">You will need this information to connect from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

1.  <span data-ttu-id="51569-113">V stredisku pre prevzatie softvéru si prevezmite doplnok pre vašu podporovanú verziu programu Project Service buď [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) alebo [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span><span class="sxs-lookup"><span data-stu-id="51569-113">From the Download Center, download the add-in for your supported version of Project Service, either [V2.X](https://go.microsoft.com/fwlink/?linkid=828268) or [V3.4+](https://www.microsoft.com/download/details.aspx?id=57956).</span></span>  

2.  <span data-ttu-id="51569-114">Kliknite na odkaz na stiahnutie.</span><span class="sxs-lookup"><span data-stu-id="51569-114">Click the download link.</span></span>  

3.  <span data-ttu-id="51569-115">Po dokončení sťahovania kliknite na možnosť **Áno** , čím doplnok nainštalujete.</span><span class="sxs-lookup"><span data-stu-id="51569-115">When the download is complete, click **Yes** to install the add-in.</span></span>  

## <a name="configure-the-add-in"></a><span data-ttu-id="51569-116">Nakonfigurujte prídavok</span><span class="sxs-lookup"><span data-stu-id="51569-116">Configure the add-in</span></span>  

1. <span data-ttu-id="51569-117">Otvorte program [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a kliknite na kartu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="51569-117">Open [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and click the **Project Service** tab.</span></span>  

2. <span data-ttu-id="51569-118">Kliknite na tlačidlo **Pripojiť**.</span><span class="sxs-lookup"><span data-stu-id="51569-118">Click **Connect**.</span></span>  

3. <span data-ttu-id="51569-119">Zadajte vaše prihlasovacie údaje a kliknite na tlačidlo **prihlásiť**.</span><span class="sxs-lookup"><span data-stu-id="51569-119">Enter your sign-in information and then click **Sign in**.</span></span>  

   <span data-ttu-id="51569-120">Teraz môžete začať s používaním prídavku.</span><span class="sxs-lookup"><span data-stu-id="51569-120">Now you can start using the add-in.</span></span>  

## <a name="read-from-a-template"></a><span data-ttu-id="51569-121">Čítanie zo šablóny</span><span class="sxs-lookup"><span data-stu-id="51569-121">Read from a template</span></span>  
 <span data-ttu-id="51569-122">Čítanie zo šablóny, ktorú ste si vytvorili v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a skopírovali ich do [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] na začatie projektového plánovania.</span><span class="sxs-lookup"><span data-stu-id="51569-122">Read from a template that you created in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] and copied into [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] to start your project planning.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="51569-123">[Vytvorenie šablóny projektu (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="51569-123">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1.  <span data-ttu-id="51569-124">Na karte **Project Service** kliknite na možnosť **Čítať** > **Šablóna Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="51569-124">From the **Project Service** tab, click **Read** > **Project Service Automation Project Template**.</span></span>  

2.  <span data-ttu-id="51569-125">Zo zoznamu si vyberte šablónu a potom kliknite na možnosť **Otvoriť**.</span><span class="sxs-lookup"><span data-stu-id="51569-125">Choose a project template from the list and then click **Open**.</span></span>  

    > [!NOTE]
    >  <span data-ttu-id="51569-126">Predvolene sa úlohy skopírované zo šablóny do projektu nastavia ako manuálne plánované.</span><span class="sxs-lookup"><span data-stu-id="51569-126">By default, the tasks that are copied from the template into Project are set as manually scheduled.</span></span>  

## <a name="assign-pn_project_service_auto-roles-to-project-resources"></a><span data-ttu-id="51569-127">Priradiť [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] role k projektovým zdrojom</span><span class="sxs-lookup"><span data-stu-id="51569-127">Assign [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] roles to project resources</span></span>  

1.  <span data-ttu-id="51569-128">Otvorte projekt a kliknite na stuhu **Úloha**.</span><span class="sxs-lookup"><span data-stu-id="51569-128">Open a project and click the **Task** ribbon.</span></span>  

2.  <span data-ttu-id="51569-129">Kliknite na ponuku **Ganttovho grafu** a potom vyberte **Hárok zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="51569-129">Click the **Gantt Chart** menu and then choose **Resource Sheet**.</span></span>  

3.  <span data-ttu-id="51569-130">V hárku zdrojov kliknite na rozbaľovaciu ponuku **Rola prostriedku Project Service** a vyberte rolu Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="51569-130">On the Resource Sheet, click the **Project Service Resource Role** drop-down menu and choose a Project Service Automation role.</span></span>  

## <a name="staff-your-project-with-resources"></a><span data-ttu-id="51569-131">Zaplňte svoj projekt zdrojmi</span><span class="sxs-lookup"><span data-stu-id="51569-131">Staff your project with resources</span></span>  

1.  <span data-ttu-id="51569-132">Na karte Project Service vyberte riadok a kliknite na tlačidlo **Vyhľadať zdroje**.</span><span class="sxs-lookup"><span data-stu-id="51569-132">From the Project Service tab, select a row and click **Find Resources**.</span></span>  

2.  <span data-ttu-id="51569-133">Na obrazovke **Rezervovať zdroj** vyberte zdroj, ktorý chcete použiť pre projekt.</span><span class="sxs-lookup"><span data-stu-id="51569-133">On the **Book Resource** screen, select the resource that you want to use for the project.</span></span>  

3.  <span data-ttu-id="51569-134">Kliknite na tlačidlo **Rezervovať** a potom kliknite na položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="51569-134">Click **Book** and then click **OK**.</span></span>  

## <a name="publish-your-project"></a><span data-ttu-id="51569-135">Zverejnite svoj projekt</span><span class="sxs-lookup"><span data-stu-id="51569-135">Publish your project</span></span>  
<span data-ttu-id="51569-136">Pri plánovaní projektu je ďalším krokom importovanie a zverejnenie projektu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-136">When your project planning is complete, the next step is to import and publish the project in to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

<span data-ttu-id="51569-137">Projekt sa naimportuje do [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-137">The project will import into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> <span data-ttu-id="51569-138">Použije sa projekt oceňovania a vytvárania tímov.</span><span class="sxs-lookup"><span data-stu-id="51569-138">The pricing and team generation process are applied.</span></span> <span data-ttu-id="51569-139">Otvorte projekt v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] a zistite, že tím, projektové odhady a štruktúra rozdelenia práce boli vytvorené,</span><span class="sxs-lookup"><span data-stu-id="51569-139">Open the project in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to see that the team, project estimates, and work breakdown structure has been generated.</span></span> <span data-ttu-id="51569-140">Nasledujúca tabuľka ukazuje, kde nájsť výsledky:</span><span class="sxs-lookup"><span data-stu-id="51569-140">The following table shows where to find the results:</span></span>


|                                                                                          |                                                                                                                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
|  [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="51569-141">**Ganttov graf**</span><span class="sxs-lookup"><span data-stu-id="51569-141">**Gantt Chart**</span></span>   | <span data-ttu-id="51569-142">Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Štruktúra rozdelenia práce**.</span><span class="sxs-lookup"><span data-stu-id="51569-142">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Work Breakdown Structure** screen.</span></span> |
| [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="51569-143">**Hárok zdrojov**</span><span class="sxs-lookup"><span data-stu-id="51569-143">**Resource Sheet**</span></span> |   <span data-ttu-id="51569-144">Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Členovia projektového tímu**.</span><span class="sxs-lookup"><span data-stu-id="51569-144">Imports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Team Members** screen.</span></span>   |
|   [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] <span data-ttu-id="51569-145">**Použiť využitie**</span><span class="sxs-lookup"><span data-stu-id="51569-145">**Use Usage**</span></span>    |    <span data-ttu-id="51569-146">Importuje na obrazovku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Odhady projektu**.</span><span class="sxs-lookup"><span data-stu-id="51569-146">Omports into the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] **Project Estimates** screen.</span></span>     |

<span data-ttu-id="51569-147">**Importovať a publikovať svoj projekt**</span><span class="sxs-lookup"><span data-stu-id="51569-147">**To import and publish your project**</span></span>  
1. <span data-ttu-id="51569-148">Na karte **Project Service** kliknite na možnosť **Publikovať** > **Nový projekt Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="51569-148">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project**.</span></span>  

2. <span data-ttu-id="51569-149">V dialógovom okne **Publikovanie v novom projekte v rámci služby Project Service** zadajte **názov projektu** a vyberte **zákazník**.</span><span class="sxs-lookup"><span data-stu-id="51569-149">On **Publish to a new project in Project Service** dialog box, enter the **Project Name** and select the **Customer**.</span></span>  

3. <span data-ttu-id="51569-150">Môžete tiež označiť **Prepojiť plán projektu so systémom Project Service Automation** ne prepojenie súboru projektu s automatizáciou Project Service.</span><span class="sxs-lookup"><span data-stu-id="51569-150">Optionally check the **Link project plan to Project Service Automation** to link the plan Project file to Project Service Automation.</span></span>  

4. <span data-ttu-id="51569-151">Kliknite na položku **Publikovať**.</span><span class="sxs-lookup"><span data-stu-id="51569-151">Click **Publish**.</span></span>  

   <span data-ttu-id="51569-152">Prepojenie súboru projektu na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] urobí súbor projektu hlavným a nastaví štruktúru rozdelenia práce v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="51569-152">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to read-only.</span></span>  <span data-ttu-id="51569-153">S cieľom vykonať zmeny plánu projektu, budete ich musieť urobiť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a zverejniť ich ako aktualizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-153">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

## <a name="edit-a-project-thats-been-imported"></a><span data-ttu-id="51569-154">Upraviť projekt, ktorý ste importovali</span><span class="sxs-lookup"><span data-stu-id="51569-154">Edit a project that’s been imported</span></span>  
 <span data-ttu-id="51569-155">Na zmenu plánu projektu naimportovaného v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] máte dve možnosti:</span><span class="sxs-lookup"><span data-stu-id="51569-155">To make changes to a project plan that's been imported into [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you have two options:</span></span>  

- <span data-ttu-id="51569-156">Otvorte hlavný súbor a upravte ho v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-156">Open the master file and edit it in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

- <span data-ttu-id="51569-157">Zrušte prepojenie súboru a upravte ho priamo v Project Service.</span><span class="sxs-lookup"><span data-stu-id="51569-157">Unlink the file and edit it directly in Project Service.</span></span> <span data-ttu-id="51569-158">V predvolenom nastavení je projekt, ktorý sa odovzdáva z aplikácie [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], zamknutý a možno ho upravovať len v projekte.</span><span class="sxs-lookup"><span data-stu-id="51569-158">By default, a project that’s been uploaded from [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] is locked and can only be edited in Project.</span></span> <span data-ttu-id="51569-159">Na úpravu súboru v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] musí byť zrušené jeho prepojenie.</span><span class="sxs-lookup"><span data-stu-id="51569-159">To edit the file in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], the file has to be unlinked.</span></span>  

### <a name="edit-in-pn_microsoft_project"></a><span data-ttu-id="51569-160">Upraviť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span><span class="sxs-lookup"><span data-stu-id="51569-160">Edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]</span></span>  

1. <span data-ttu-id="51569-161">Z hlavného menu kliknite na tlačidlo **Project Service** > **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="51569-161">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="51569-162">Pre zoznam projektov otvorte projekt vytvorený v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-162">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="51569-163">Kliknite na **Otvoriť v MS Project** z pása s nástrojmi.</span><span class="sxs-lookup"><span data-stu-id="51569-163">Click **Open in MS Project** from the ribbon.</span></span> <span data-ttu-id="51569-164">Týmto sa otvorí prepojený hlavný súbor v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-164">This will open the linked master file in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

### <a name="unlink-a-file-and-edit-in-pn_microsoft_project-service"></a><span data-ttu-id="51569-165">Zrušte prepojenie súboru a upravte ho v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span><span class="sxs-lookup"><span data-stu-id="51569-165">Unlink a file and edit in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] Service</span></span>  

1. <span data-ttu-id="51569-166">Z hlavného menu kliknite na tlačidlo **Project Service** > **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="51569-166">From the main menu, click **Project Service** > **Projects**.</span></span>  

2. <span data-ttu-id="51569-167">Pre zoznam projektov otvorte projekt vytvorený v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-167">From the list of projects, open the one you created in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)].</span></span>  

3. <span data-ttu-id="51569-168">Kliknite na **Zrušiť prepojenie z MS Project** z pása s nástrojmi.</span><span class="sxs-lookup"><span data-stu-id="51569-168">Click **Unlink from MS Project** from the ribbon.</span></span>  

## <a name="upload-a-project-file-to-sharepoint-or-office-groups"></a><span data-ttu-id="51569-169">Odovzdanie súboru Projekt do SharePoint alebo Office Groups</span><span class="sxs-lookup"><span data-stu-id="51569-169">Upload a Project file to SharePoint or Office Groups</span></span>  
 <span data-ttu-id="51569-170">Môžete odovzdať súbor Projekt SharePoint a nájsť ho pod Súvisiace dokumenty pre váš [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] projekt.</span><span class="sxs-lookup"><span data-stu-id="51569-170">You can upload your Project file to SharePoint and find it under the Associated Documents for your [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  <span data-ttu-id="51569-171">Váš správca vám musí nastaviť správu dokumentov SharePoint a tiež povoliť entitu Project.</span><span class="sxs-lookup"><span data-stu-id="51569-171">You need to have your administrator configure SharePoint document management and turn it on for the Project entity.</span></span> 

 <span data-ttu-id="51569-172">Môžete tiež nahrať súbor projektu do [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)], ak máte nastavené Office skupiny.</span><span class="sxs-lookup"><span data-stu-id="51569-172">You can also upload your Project file to [!INCLUDE[pn_onedrive_for_business](../includes/pn-onedrive-for-business.md)] if you have Office Groups set up.</span></span>

### <a name="upload-a-file-for-sharepoint"></a><span data-ttu-id="51569-173">Nahrajte súbor pre SharePoint</span><span class="sxs-lookup"><span data-stu-id="51569-173">Upload a file for SharePoint</span></span>  

1. <span data-ttu-id="51569-174">Z hlavného menu kliknite na tlačidlo **Project Service** > **Nahrať**.</span><span class="sxs-lookup"><span data-stu-id="51569-174">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="51569-175">Zvoľte možnosť **Do projektových dokumentov Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="51569-175">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="51569-176">V dialógovom okne **Povoliť otvorenie v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** zvoľte možnosť **Áno** alebo **Nie**.</span><span class="sxs-lookup"><span data-stu-id="51569-176">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="51569-177">Keď kliknete na **Áno** , budete môcť vybrať tlačidlo **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v Project Service Automation, spustiť [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načítať súbor projektu zo SharePoint knižnice dokumentov.</span><span class="sxs-lookup"><span data-stu-id="51569-177">If you click **Yes** , you'll be able select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="51569-178">Keď kliknete na **Nie** , prepojenie na tlačidlo **Otvoriť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovať.</span><span class="sxs-lookup"><span data-stu-id="51569-178">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="51569-179">Súbor programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] nájdete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod položkou **Dokumenty** pre konkrétny projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-179">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

### <a name="upload-a-file-for-office-groups"></a><span data-ttu-id="51569-180">Nahrajte súbor pre skupiny Office</span><span class="sxs-lookup"><span data-stu-id="51569-180">Upload a file for Office Groups</span></span>  

1. <span data-ttu-id="51569-181">Z hlavného menu kliknite na tlačidlo **Project Service** > **Nahrať**.</span><span class="sxs-lookup"><span data-stu-id="51569-181">From the main menu, click **Project Service** > **Upload**.</span></span>  

2. <span data-ttu-id="51569-182">Zvoľte možnosť **Do projektových dokumentov Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="51569-182">Select **To Project Service Automation Project Documents**.</span></span>  

3. <span data-ttu-id="51569-183">V dialógovom okne **Povoliť otvorenie v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** zvoľte možnosť **Áno** alebo **Nie**.</span><span class="sxs-lookup"><span data-stu-id="51569-183">On the **Enable Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** dialog, select **Yes** or **No**.</span></span>  

   - <span data-ttu-id="51569-184">Keď kliknete na **Áno** , budete môcť vybrať tlačidlo **Otvoriť v [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** v Project Service Automation, spustiť [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a načítať súbor projektu z knižnice dokumentov SharePoint.</span><span class="sxs-lookup"><span data-stu-id="51569-184">If you click **Yes** , you'll be able to select the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button in Project Service Automation, launch [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)], and load the Project file from the SharePoint document library.</span></span>  

   - <span data-ttu-id="51569-185">Keď kliknete na **Nie** , prepojenie na tlačidlo **Otvoriť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** nebude fungovať.</span><span class="sxs-lookup"><span data-stu-id="51569-185">If you click **No** , the link for the **Open in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)]** button won't work.</span></span>  

4. <span data-ttu-id="51569-186">Súbor programu [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] nájdete v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] pod položkou **Dokumenty** pre konkrétny projekt [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-186">The [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] file can be found in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] under **Documents** for the specific [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] project.</span></span>  

## <a name="publish--your-project-as-a-template"></a><span data-ttu-id="51569-187">Publikovať svoj projekt ako šablónu</span><span class="sxs-lookup"><span data-stu-id="51569-187">Publish  your project as a template</span></span>  
 <span data-ttu-id="51569-188">Môžete uložiť projekt a znova ho uložíte ako šablónu v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-188">You can save your project and reuse it by saving it as a project template in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  <span data-ttu-id="51569-189">Projektové šablóny sú opakovane projektové plány v [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-189">Project templates are reusable project plans in [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)] <span data-ttu-id="51569-190">[Vytvorenie šablóny projektu (Project Service Automation)](../psa/create-project-template.md)</span><span class="sxs-lookup"><span data-stu-id="51569-190">[Create a project template (Project Service Automation)](../psa/create-project-template.md)</span></span>  

1. <span data-ttu-id="51569-191">Na karte **Project Service** kliknite na možnosť **Publikovať** > **Nový projekt šablóny Project Service Automation**.</span><span class="sxs-lookup"><span data-stu-id="51569-191">From the **Project Service** tab, click **Publish** > **New Project Service Automation Project Template**.</span></span>  

2. <span data-ttu-id="51569-192">V dialógovom okne **Publikovanie v novom projekte v rámci šablóny Project Service** zadajte **názov šablóny projektu**.</span><span class="sxs-lookup"><span data-stu-id="51569-192">On the **Publish to a new project in Project Service template** dialog box, enter the **Project template name**.</span></span>  

3. <span data-ttu-id="51569-193">Môžete tiež označiť **Prepojiť plán projektu so systémom Project Service Automation** na prepojenie súboru projektu s [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-193">Optionally, check the **Link project plan to Project Service Automation** to link the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>  

4. <span data-ttu-id="51569-194">Kliknite na položku **Publikovať**.</span><span class="sxs-lookup"><span data-stu-id="51569-194">Click **Publish**.</span></span>  

<span data-ttu-id="51569-195">Prepojenie súboru projektu na [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] robí projekt súboru kapitána a nastaví štruktúry rozdelenia práce v šablóne[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="51569-195">Linking the Project file to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] makes the Project file the master and sets the work breakdown structure in the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] template to read-only.</span></span>  <span data-ttu-id="51569-196">S cieľom vykonať zmeny plánu projektu, budete ich musieť urobiť v programe [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] a zverejniť ich ako aktualizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="51569-196">In order to make changes to the project plan, you need to make them in [!INCLUDE[pn_microsoft_project](../includes/pn-microsoft-project.md)] and publish them as updates to [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span></span>

### <a name="see-also"></a><span data-ttu-id="51569-197">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="51569-197">See Also</span></span>  
 [<span data-ttu-id="51569-198">Príručka projektového manažéra</span><span class="sxs-lookup"><span data-stu-id="51569-198">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
