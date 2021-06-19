---
title: Vytvorenie nového projektu
description: Táto téma poskytuje informácie o tom, ako vytvoriť nový projekt.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006260"
---
# <a name="create-a-new-project"></a><span data-ttu-id="9c6fa-103">Vytvorenie nového projektu</span><span class="sxs-lookup"><span data-stu-id="9c6fa-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c6fa-104">Podľa nasledujúcich pokynov vytvoríte nový projekt.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="9c6fa-105">Na stránke **Projektový manažment** vyberte **Nový projekt** a zadajte nasledujúce hodnoty:</span><span class="sxs-lookup"><span data-stu-id="9c6fa-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="9c6fa-106">**Typ projektu:** Čas a materiál</span><span class="sxs-lookup"><span data-stu-id="9c6fa-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="9c6fa-107">**Názov projektu:** Fáza 2 inovácie na XYZ</span><span class="sxs-lookup"><span data-stu-id="9c6fa-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="9c6fa-108">**Skupina projektov:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="9c6fa-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="9c6fa-109">**Identifikátor projektovej zmluvy:** 00000002</span><span class="sxs-lookup"><span data-stu-id="9c6fa-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="9c6fa-110">Vyberte **Vytvoriť projekt**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="9c6fa-111">Priradenie zdroja k projektu</span><span class="sxs-lookup"><span data-stu-id="9c6fa-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="9c6fa-112">Na stránke **Pracovníci** v zozname **Pracovníci** vyberte záznam pre pracovníka, pre ktorého ste predtým nastavili kompetencie, a otvorte záznam pracovníka.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="9c6fa-113">Na table Akcia na karte **Projekt** v skupine **Nastavenie** vyberte **Priradiť projekty**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="9c6fa-114">Na stránke **Priradenia projektu na overenie zdrojov** na karte **Projekty** v poli **Pridať projekt k vybraným projektom** nastavte filter na projekt **Fáza 2 inovácie na XYZ**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="9c6fa-115">Na table **Zostávajúce projekty** vyberte projekt a potom ho kliknutím na tlačidlo so šípkou pridajte na tablu **Vybrané projekty**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="9c6fa-116">Podľa potreby môžete k zdroju tiež priradiť kategórie.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="9c6fa-117">Typ kategórie je buď **Náklady** alebo **Príjem**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="9c6fa-118">Typ kategórie určuje vaša organizácia.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-118">The category type is determined by your organization.</span></span> <span data-ttu-id="9c6fa-119">Ak pre zdroj nie sú priradené žiadne kategórie, služba Finance vyhľadá predvolenú kategóriu hodinových cien pre náklady a výnosy.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="9c6fa-120">Nastavenie zdroja projektu a charakteristiky roly</span><span class="sxs-lookup"><span data-stu-id="9c6fa-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="9c6fa-121">Projektový manažér môže pomocou funkcie financovania projektu vytvoriť roly, ktoré sú potrebné pre projekt.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="9c6fa-122">Roly je možné použiť, ak potvrdené zdroje nie sú pri rezervácii zdrojov stále známe.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="9c6fa-123">Roly je možné dočasne rezervovať ako plánované zdroje, aby ste mohli pokračovať v etapách plánovania projektu.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="9c6fa-124">[![Ukážka roly](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="9c6fa-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="9c6fa-125">**Scenár:** Contoso bolo poverené dokončím časového a materiálového projektu, ktorý má schválenú osnovu projektu.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="9c6fa-126">Junior projektový manažér ešte stále dokončuje rozsah projektu.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="9c6fa-127">Správca zdrojov v súčasnosti identifikuje konkrétne zdroje, ktoré budú vyhradené na prácu na novom projekte.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="9c6fa-128">Z dôvodu kritickej povahy projektu požiadal sponzor projektu jednu z rolí Senior projektového manažéra.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="9c6fa-129">Správca zdrojov musí získať nový zdroj a definovať rolu v systéme pre prípad, že junior projektový manažér vyžaduje informácie o zdroji počas plánovania projektu.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="9c6fa-130">Nasledujúce kroky ukazujú, ako môže správca zdrojov nastaviť rolu Senior projektového manažéra a priradiť k nej vlastnosti zdrojov.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="9c6fa-131">Neskôr sa dá rola použiť na vyhľadanie dostupných zdrojov, ktoré zodpovedajú požadovaným kompetenciám v oblasti zdrojov.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="9c6fa-132">Na stránke **Nastaviť roly** vyberte **Nová** a zadajte nasledujúce hodnoty:</span><span class="sxs-lookup"><span data-stu-id="9c6fa-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="9c6fa-133">**ID roly:** Senior projektový manažér</span><span class="sxs-lookup"><span data-stu-id="9c6fa-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="9c6fa-134">**Opis:** Senior projektový manažér</span><span class="sxs-lookup"><span data-stu-id="9c6fa-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="9c6fa-135">Stlačte možnosť **Vytvoriť**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-135">Select **Create**.</span></span>
3. <span data-ttu-id="9c6fa-136">Vyberte rolu **Senior projektový manažér** a potom vyberte **Nakonfigurovať vlastnosti**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="9c6fa-137">V poli **Typ vlastností** vyberte **Zručnosť**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="9c6fa-138">V poli **Dostupné vlastnosti** zadajte hľadanú zručnosť.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="9c6fa-139">V poli **Typ vlastnosti** vyberte **Certifikát**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="9c6fa-140">V poli **Dostupné vlastnosti** zadajte hľadaný typ certifikátu.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="9c6fa-141">Priradenie zdroja projektu k projektu</span><span class="sxs-lookup"><span data-stu-id="9c6fa-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="9c6fa-142">Na stránke **Všetky projekty** vyberte projekt **Fáza 2 inovácie na XYZ**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="9c6fa-143">Na karte **Projektový tím a plánovanie** vyberte **Pridať**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="9c6fa-144">V poli **Rola** vyberte **Člen tímu**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="9c6fa-145">Vyberte **Rezervovať z kalendára**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="9c6fa-146">Na stránke **Dostupnosť zdrojov** vyberte **Zobraziť nastavenia**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="9c6fa-147">Na stránke **Upraviť nastavenia zobrazenia** zadajte nasledujúce hodnoty:</span><span class="sxs-lookup"><span data-stu-id="9c6fa-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="9c6fa-148">**Formát pre zobrazenie rozsahu dátumov:** Deň</span><span class="sxs-lookup"><span data-stu-id="9c6fa-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="9c6fa-149">**Zobraziť popisy dostupnosti:** Áno</span><span class="sxs-lookup"><span data-stu-id="9c6fa-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="9c6fa-150">**Zobraziť zostávajúcu kapacitu:** Áno</span><span class="sxs-lookup"><span data-stu-id="9c6fa-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="9c6fa-151">V zozname zdrojov vyberte zdroj.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="9c6fa-152">Vyberte **Pevná rezervácia** a **Plná kapacita**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="9c6fa-153">Priradenie zdroja k predvolenej role</span><span class="sxs-lookup"><span data-stu-id="9c6fa-153">Assign a resource to a default role</span></span>

<span data-ttu-id="9c6fa-154">Aby ste pomohli projektovým manažérom alebo správcom zdrojov, aby sa mohli hlbšie ponoriť do zdrojov, ktoré je možné rezervovať pre projekt.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="9c6fa-155">Môžete priradiť predvolenú rolu k existujúcemu zdroju alebo k novo získanému zdroju.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="9c6fa-156">Napríklad keď bol Daniel prijatý do zamestnania, mal skúsenosti a zručnosti na to, aby obsadil úlohu obchodného analytika.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="9c6fa-157">Správca zdrojov pridelil túto rolu ako predvolenú rolu Daniela.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="9c6fa-158">Preto správca zdrojov pridal Daniela do skupiny obchodných analytikov, ktorí sú k dispozícii na prácu na projektoch.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="9c6fa-159">Počas rezervácie zdrojov môžu projektoví manažéri filtrovať zdroje rolí, ktoré sú k dispozícii na prácu na projektoch.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="9c6fa-160">Tieto informácie môžu použiť ako jedno kritérium, keď uskutočňujú multikriteriálnu rozhodovaciu analýzu počas plnenia zdrojov.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="9c6fa-161">Môžu tiež pridať do filtra ďalšie charakteristiky zdrojov, aby vyhľadali zdroje, ktoré majú špecifické zručnosti, vzdelanie a skúsenosti pre daný projekt.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="9c6fa-162">**Scenár:** Schválený projekt sa začal a rola Senior projektového manažéra bola vyhradená ako plánovaný zdroj počas fázy plánovania projektu.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="9c6fa-163">Správca zdrojov teraz získal zdroj na splnenie úlohy Senior projektový manažér.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="9c6fa-164">Na stránke **Zoznam zdrojov** vyberte **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="9c6fa-165">Na stránke **Rola zdroja** vyberte **Nová** a zadajte nasledujúce hodnoty:</span><span class="sxs-lookup"><span data-stu-id="9c6fa-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="9c6fa-166">**Účinná:** Zadajte aktuálny dátum.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="9c6fa-167">**Exspirácia:** Zadajte **Nikdy**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="9c6fa-168">**Rola:** Zadajte **Senior projektový manažér**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="9c6fa-169">Vyberte **Uložiť** a potom zatvorte stránku.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="9c6fa-170">Na karte **Kompetencie** pridajte zručnosť **ProjectMgmt** a certifikát **PMP**.</span><span class="sxs-lookup"><span data-stu-id="9c6fa-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]