---
title: Vytvorenie projektového tímu
description: Táto téma poskytuje informácie o tom, ako vytvoriť a spravovať projektové tímy.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d3d39aa28565692bf894ff8d4fc8f8c3c5542d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006215"
---
# <a name="create-a-project-team"></a><span data-ttu-id="6cd9c-103">Vytvorenie projektového tímu</span><span class="sxs-lookup"><span data-stu-id="6cd9c-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6cd9c-104">Ak chcete použiť roly, ktoré boli predtým v projekte nastavené, musí projektový manažér priradiť tieto roly k projektu.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="6cd9c-105">K projektu je možné priradiť viac rolí.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="6cd9c-106">Aby sa predišlo zámene, sú tieto roly počas rezervácie automaticky označené.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="6cd9c-107">Ak napr. projektový manažér vyžaduje troch softvérových inžinierov, tri roly softvérového inžiniera, ktoré majú označenie **softvérový inžinier 1**, **softvérový inžinier 2** a **softvérový inžinier 3** sa generujú automaticky.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="6cd9c-108">Ak boli pre danú rolu predtým nastavené vlastnosti, použijú sa ako filter počas hľadania zdroja.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="6cd9c-109">Podľa potreby je možné pridať ďalšie vlastnosti, aby sa hľadanie ešte vylepšilo.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="6cd9c-110">Nastavenia zobrazenia je možné tiež prispôsobiť, aby sa získal lepší prehľad o dostupnosti zdrojov.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="6cd9c-111">K dispozícii sú možnosti zobrazenia hodinovej, dennej, týždennej, mesačnej, štvrťročnej a ročnej dostupnosti.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="6cd9c-112">K dispozícii je tiež možnosť zobraziť dostupnú a zostávajúcu kapacitu zdrojov.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="6cd9c-113">Táto možnosť je užitočná na správu času, keď odhadujete dostupný čas na aktivity alebo dostupnosť zdrojov.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="6cd9c-114">Projektový manažér môže na stránke zvoliť rolu a potom, ak je k dispozícii zdroj, ktorý vyhovuje požiadavke, vybrať rezerváciu zdroja na vyplnenie roly.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="6cd9c-115">Upozorňujeme, že v tomto okamihu fázy plánovania nie je potrebné rezervovať zdroje.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="6cd9c-116">Pri vytváraní štruktúry WBS môžete roly nahradiť personálnymi zdrojmi pre projekt.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="6cd9c-117">Ak sú roly nahradené personálnymi zdrojmi v štruktúre WBS, nastavenie zdrojov automaticky aktualizuje zoznam a plánovanie projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="6cd9c-118">[![Zoznam projektového tímu, ktorý zahŕňa roly aj skutočné zdroje](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="6cd9c-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="6cd9c-119">Projektový manažér má rôzne možnosti rezervácie zdroja pre projekt, ako napr. **Zostávajúca kapacita**, **Plná kapacita**, **Percento kapacity** a **Uveďte hodiny**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="6cd9c-120">Tieto možnosti rezervácie je možné kedykoľvek zrušiť, ak sa zmení priradenie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="6cd9c-121">Podporované sú dva typy rezervácií:</span><span class="sxs-lookup"><span data-stu-id="6cd9c-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="6cd9c-122">**Pevná rezervácia** – Rezervácia zdroja bola schválená a bolo potvrdené, že bude pracovať na zákazke po stanovenú dobu.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="6cd9c-123">**Predbežná rezervácia** – Rezervácia zdroja bola predbežne nastavené na prácu na zákazke po stanovenú dobu.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="6cd9c-124">Nasledujúci postup vysvetľuje, ako vytvoriť projektový tím.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="6cd9c-125">Vytvorenie projektového tímu</span><span class="sxs-lookup"><span data-stu-id="6cd9c-125">Create a project team</span></span>

1. <span data-ttu-id="6cd9c-126">Na stránke so zoznamom **Všetky projekty** vyberte projekt a potom vyberte **Upraviť**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="6cd9c-127">Na karte **Projektový tím a plánovanie** v poli **Naplánujte dátum ukončenia** zadajte do poľa dátum začatia plánu plus jeden mesiac.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="6cd9c-128">Napríklad, ak je dátum začatia plánu 24. júna 2017 (24. 6. 2017), zadajte **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="6cd9c-129">Stlačte možnosť **Pridať**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-129">Select **Add**.</span></span>
4. <span data-ttu-id="6cd9c-130">V table **Pridať do projektu roly** v poli **Rola** vyberte **Senior projektový manažér**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="6cd9c-131">Vyberte **Požadované kompetencie**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="6cd9c-132">Na stránke **Vybrať vlastnosti** sú predvolene vybrané vlastnosti, ktoré ste predtým nastavili pre rolu Senior projektového manažéra.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="6cd9c-133">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-133">Select **OK**.</span></span>
7. <span data-ttu-id="6cd9c-134">Na stránke **Pridajte do projektu roly** v poli **Počet zdrojov** zadajte **1**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="6cd9c-135">V poli **Zdroje** vyhľadávanie zobrazuje všetky zdroje, ktoré majú požadované kompetencie.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="6cd9c-136">Vyberte **Daniel Goldschmidt** a potom **Vytvoriť**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="6cd9c-137">Na stránke **Projekt** vyberte položku **Pridať**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="6cd9c-138">V table **Pridať do projektu roly** v poli **Rola** vyberte **Člen tímu**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="6cd9c-139">V poli **Počet zdrojov** zadajte **5**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="6cd9c-140">Stlačte možnosť **Vytvoriť**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-140">Select **Create**.</span></span>
12. <span data-ttu-id="6cd9c-141">Na stránke **Projekty** vyberte **Vyplniť zdroj**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="6cd9c-142">Monitorovanie projektových tímov</span><span class="sxs-lookup"><span data-stu-id="6cd9c-142">Monitor project teams</span></span>
1. <span data-ttu-id="6cd9c-143">Na stránke **Všetky projekty** vyberte prepojenie **ID projektu** pre projekt **Fáza 2 inovácie XYZ**.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="6cd9c-144">Na rýchlej karte **Projektový tím a plánovanie** skontrolujte správnosť zdrojov projektu, ktoré sú uvedené.</span><span class="sxs-lookup"><span data-stu-id="6cd9c-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]