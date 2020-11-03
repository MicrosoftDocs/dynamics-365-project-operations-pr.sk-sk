---
title: Spravujte zdroje
description: Táto téma poskytuje informácie o tom, ako spravovať zdroje.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 5b34ad66750dba9459d551a2527c13111196511e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084565"
---
# <a name="manage-resources"></a><span data-ttu-id="3f476-103">Spravujte zdroje</span><span class="sxs-lookup"><span data-stu-id="3f476-103">Manage resources</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="3f476-104">Dynamics 365 Project Service Automation obsahuje tabuľu správcu zdrojov, ktorá poskytuje vizuálny prehľad dopytu a využitia zdrojov v celej organizácii.</span><span class="sxs-lookup"><span data-stu-id="3f476-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="3f476-105">Grafy na tejto tabuli môžete použiť na vizualizáciu nasledujúcich informácií:</span><span class="sxs-lookup"><span data-stu-id="3f476-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="3f476-106">**Dopyt po zdrojoch** – graf **požiadavky na aktívny zdroj** zobrazuje zdroje, ktoré boli odoslané.</span><span class="sxs-lookup"><span data-stu-id="3f476-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="3f476-107">Zdroje sú agregované buď rolou alebo projektom.</span><span class="sxs-lookup"><span data-stu-id="3f476-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="3f476-108">**Dopyt na nepredložený zdroj** – graf **dopytu na nepriradené zdroje** zobrazuje všetky požiadavky na zdroje, ktoré neboli predložené.</span><span class="sxs-lookup"><span data-stu-id="3f476-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="3f476-109">Pomáha správcom zdrojov zobraziť dopyt, ktorý nie je pevný a môže byť predložený prostredníctvom žiadosti o prostriedky.</span><span class="sxs-lookup"><span data-stu-id="3f476-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="3f476-110">**Fakturovateľné využitie za uplynulý týždeň** – graf **využitia rolí** zobrazuje percento skutočného fakturovateľného využitia organizácie podľa roly proti jeho cieľovému fakturovateľnému využitiu podľa roly.</span><span class="sxs-lookup"><span data-stu-id="3f476-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="3f476-111">Aby bol graf **využitia rolí** k dispozícii, vytvorte prácu, ktorá spúšťa pracovný postup UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="3f476-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="3f476-112">Táto opakovaná úloha sa spúšťa každých sedem dní na výpočet fakturovateľného využitia za predchádzajúcich sedem dní.</span><span class="sxs-lookup"><span data-stu-id="3f476-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="3f476-113">Výsledky sú agregované podľa role.</span><span class="sxs-lookup"><span data-stu-id="3f476-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="3f476-114">Spravujte členov projektového tímu</span><span class="sxs-lookup"><span data-stu-id="3f476-114">Manage project team members</span></span>

<span data-ttu-id="3f476-115">Projektoví manažéri môžu na spravovanie zdrojov na projektoch použiť tabuľu správca prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="3f476-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="3f476-116">Napríklad môžu pridať člena tímu priamo do projektu a rezervovať člena tímu, aby splnil požiadavky na zdroje, ktoré boli zachytené všeobecným prostriedkom.</span><span class="sxs-lookup"><span data-stu-id="3f476-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="3f476-117">Pridajte člena tímu priamo do projektu</span><span class="sxs-lookup"><span data-stu-id="3f476-117">Add a team member directly to a project</span></span>

<span data-ttu-id="3f476-118">Ak chcete pridať člena tímu priamo do projektu, na stránke **projekty** na karte **tím** vyberte položku **nové**.</span><span class="sxs-lookup"><span data-stu-id="3f476-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="3f476-119">Zobrazí sa dialógové okno **rýchle vytvorenie člena projektového tímu**.</span><span class="sxs-lookup"><span data-stu-id="3f476-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="3f476-120">V tomto dialógovom okne môžete vykonávať tieto úlohy:</span><span class="sxs-lookup"><span data-stu-id="3f476-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="3f476-121">**Rezervujte si pomenovaný zdroj** – v poli **rezervovateľné zdroje** vyberte názov zdroja.</span><span class="sxs-lookup"><span data-stu-id="3f476-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="3f476-122">Potom vyberte rolu, nastavte obdobie a vyberte spôsob pridelenia.</span><span class="sxs-lookup"><span data-stu-id="3f476-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="3f476-123">Pomenovaný zdroj, ktorý ste vybrali, sa pridá do projektu pomocou vybratej metódy prideľovania a zdrojového kalendára.</span><span class="sxs-lookup"><span data-stu-id="3f476-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="3f476-124">**Pridať všeobecný zdroj** – ponechajte prázdne pole **rezervovateľného zdroja** a potom vyberte rolu, nastavte obdobie a vyberte preferovaný spôsob pridelenia.</span><span class="sxs-lookup"><span data-stu-id="3f476-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="3f476-125">Všeobecný zdroj sa pridá do tímu ako zástupný symbol, aby držal vzor dopytu, ktorý sa používa na rezerváciu pomenovaných zdrojov v tíme.</span><span class="sxs-lookup"><span data-stu-id="3f476-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="3f476-126">Požiadavka sa vykonáva v súlade s kalendárom projektu.</span><span class="sxs-lookup"><span data-stu-id="3f476-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="3f476-127">**Pridanie pomenovaného zdroja do tímu bez spotreby kapacity zdrojov** – v poli **rezervovateľné zdroje** vyberte zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="3f476-128">Potom vyberte obdobie a vyberte **Nič** ako spôsob pridelenia.</span><span class="sxs-lookup"><span data-stu-id="3f476-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="3f476-129">Zdroj sa pridá do tímu, ale kapacita zdroja nie je spotrebovaná prostredníctvom rezervácie.</span><span class="sxs-lookup"><span data-stu-id="3f476-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="3f476-130">Rezervujte si člena tímu, tak aby splnil požiadavky na zdroje pre všeobecný zdroj</span><span class="sxs-lookup"><span data-stu-id="3f476-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="3f476-131">V PSA si môžete rezervovať všeobecný zdroj v projektovom tíme a môžete špecifikovať úlohu, požadovanú kapacitu a spôsob rozdelenia tejto kapacity.</span><span class="sxs-lookup"><span data-stu-id="3f476-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="3f476-132">V požiadavke na zdroj môžete zadať atribúty, ktoré súvisia so všeobecným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="3f476-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="3f476-133">Tieto atribúty zahŕňajú požadované zručnosti, preferovanú organizačnú jednotku a preferované zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="3f476-134">Ak chcete určiť požadované zručnosti na všeobecný zdroj pre vývojára, postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="3f476-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="3f476-135">Na stránke **projekty** na karte **tím** vyberte položku **nové** , ak chcete rezervovať všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Všeobecný zdroj rezervovaný pre tím](media/Resource-Management-image9.png)

2. <span data-ttu-id="3f476-137">V zobrazení **všetci členovia tímu** v stĺpci **požiadavka zdroja** vyberte prepojenie na pridanie požadovaných zručností pre všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Odkaz na požiadavku](media/Resource-Management-image10.png)

3. <span data-ttu-id="3f476-139">Na stránke **požiadavky na zdroje** , ktorá sa zobrazí v mriežke **zručnosti** , vyberte elipsu ( **...** ) a potom vyberte **pridať novú charakteristiku požiadavky** pre pridanie požadovaných zručnosti pre vývojárov.</span><span class="sxs-lookup"><span data-stu-id="3f476-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis ( **...** ) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Pridajte príkaz nová charakteristika požiadavky](media/Resource-Management-image11.png)

4. <span data-ttu-id="3f476-141">V dialógovom okne **rýchle vytvorenie: charakteristika požiadavky** , ktoré sa zobrazí v poli **charakteristika** , vyberte požadované zručnosti.</span><span class="sxs-lookup"><span data-stu-id="3f476-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="3f476-142">Potom v poli **hodnota hodnotenia** vyberte úroveň odbornosti pre danú zručnosť.</span><span class="sxs-lookup"><span data-stu-id="3f476-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="3f476-143">Nakoniec v poli **požiadavka na zdroj** nastavte požiadavku na zdrojové prostriedky z organizačných jednotiek alebo dokonca pomenovaných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="3f476-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="3f476-144">Po dokončení vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3f476-144">When you've finished, select **Save**.</span></span>

    ![Rýchle vytvorenie: dialógové okno vlastnosti požiadavky](media/Resource-Management-image12.png)

5. <span data-ttu-id="3f476-146">Na stránke **požiadavky na zdroje** vyberte položku **rezervovať** , čím sa splní požiadavka na zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Tlačidlo rezervovať na stránke požiadavky na zdroje](media/Resource-Management-image13.png)

    <span data-ttu-id="3f476-148">Môžete tiež vybrať všeobecný prostriedok v mriežke **všetci členovia tímu** a potom vyberte položku **rezervovať.**</span><span class="sxs-lookup"><span data-stu-id="3f476-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Tlačidlo rezervovať nad mriežkou Všetci členovia tímu](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="3f476-150">V tomto príklade je 40 požadovaných hodín, ale žiadne aktuálne rezervované hodiny, pretože všeobecné zdroje nemajú rezervácie.</span><span class="sxs-lookup"><span data-stu-id="3f476-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="3f476-151">Okrem toho nie sú priradené žiadne hodiny, pretože všeobecný zdroj bol pridaný priamo do tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="3f476-152">Nebolo pridané pomocou priradenia úlohy.</span><span class="sxs-lookup"><span data-stu-id="3f476-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="3f476-153">Na stránke **asistent plánovania** môžete filtrovať dostupné zdroje podľa požiadaviek, ktoré sú zadané v požiadavke na zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="3f476-154">Zdroje sú zoradené podľa parametrov zoradenia, ktoré sú špecifikované na tabuli plánovania.</span><span class="sxs-lookup"><span data-stu-id="3f476-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Stránka Asistent plánovania](media/Resource-Management-image15.png)

    <span data-ttu-id="3f476-156">Tu sú niektoré filtre, ktoré sa často používajú:</span><span class="sxs-lookup"><span data-stu-id="3f476-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="3f476-157">**Charakteristika spolu s hodnotením** - Filter podľa zručností, certifikácií a ďalších zdrojov kvality, okrem hodnotenia odbornosti.</span><span class="sxs-lookup"><span data-stu-id="3f476-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="3f476-158">**Roly** – Filter podľa predvolených rolí priradených k rezervovateľným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="3f476-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="3f476-159">**Organizačné jednotky** – Filter rezervovateľné zdroje organizačnými jednotkami, ku ktorým sú priradené.</span><span class="sxs-lookup"><span data-stu-id="3f476-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="3f476-160">Ak nie ste spokojní s výsledkami úvodného vyhľadávania požiadaviek, môžete zmeniť kritériá filtra.</span><span class="sxs-lookup"><span data-stu-id="3f476-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="3f476-161">Rozbaľte panel **zobrazenie filtra** na ľavej strane a potom vyberte položku **Hľadať** a vyhľadajte ďalšie zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Panel filtrovať zobrazenie](media/Resource-Management-image16.png)

7. <span data-ttu-id="3f476-163">Ak chcete zmeniť spôsob zoradenia výsledkov, vyberte **zoradiť**.</span><span class="sxs-lookup"><span data-stu-id="3f476-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Príkaz Zoradiť](media/Resource-Management-image17.png)

8. <span data-ttu-id="3f476-165">Vyberte zdroje podľa dopytu, ktorý je špecifikovaný v požiadavke, ako je uvedené v hornej časti mriežky.</span><span class="sxs-lookup"><span data-stu-id="3f476-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="3f476-166">Môžete vymazať výber buniek v mriežke a ponechať kapacitu zdroja otvorenú.</span><span class="sxs-lookup"><span data-stu-id="3f476-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="3f476-167">Ako rezervované je možné vybrať len jeden zdroj naraz.</span><span class="sxs-lookup"><span data-stu-id="3f476-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="3f476-168">Vyberte **rezervovať** , ak chcete rezervovať vybratý zdroj a nechať otvorenú panel plánovania, aby ste mohli vybrať ďalšie zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="3f476-169">Prípadne vyberte položku **rezervovať & východ** , ak chcete rezervovať vybratý zdroj a zatvoriť panel plánovania.</span><span class="sxs-lookup"><span data-stu-id="3f476-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Zdroj, ktorý sa má rezervovať](media/Resource-Management-image19.png)

    <span data-ttu-id="3f476-171">Zobrazí sa upozornenie o rezervovaní hodín.</span><span class="sxs-lookup"><span data-stu-id="3f476-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="3f476-172">Indikátory dopytu ukazujú, nakoľko je požiadavka na rezerváciu splnená a koľko zostáva.</span><span class="sxs-lookup"><span data-stu-id="3f476-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="3f476-173">Môžete tiež zistiť, koľko kapacity vybratého prostriedku sa spotrebuje.</span><span class="sxs-lookup"><span data-stu-id="3f476-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="3f476-174">Výberom **rozbaliť** zobrazíte ďalšie podrobnosti o rezerváciách zdrojov.</span><span class="sxs-lookup"><span data-stu-id="3f476-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="3f476-175">Vráťte sa do zobrazenia **všetci členovia tímu** .</span><span class="sxs-lookup"><span data-stu-id="3f476-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="3f476-176">V mriežke si všimnite, že všeobecný prostriedok bol nahradený názvom prostriedku a 40 hodín je uvedených ako rezervované pre daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Aktualizovaná mriežka všetkých členov tímu](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="3f476-178">Nie sú zobrazené žiadne priradené hodiny, pretože boli rezervované priamo v tíme.</span><span class="sxs-lookup"><span data-stu-id="3f476-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="3f476-179">Neboli rezervované pomocou priradenia úloh.</span><span class="sxs-lookup"><span data-stu-id="3f476-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="3f476-180">Priradenie všeobecných zdrojov k úlohe a generovanie zdrojových požiadaviek</span><span class="sxs-lookup"><span data-stu-id="3f476-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="3f476-181">V PSA môžete vytvárať úlohy a potom im priradiť všeobecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="3f476-182">Týmto spôsobom môže byť dopyt po zdroji zastupovaný zástupnými symbolmi, zatiaľ čo vy odhadnete svoj rozvrh a finančné čísla.</span><span class="sxs-lookup"><span data-stu-id="3f476-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="3f476-183">Potom môžete generovať požiadavky na zdroje pre všeobecné zdroje a naplniť ich.</span><span class="sxs-lookup"><span data-stu-id="3f476-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="3f476-184">Na stránke **projekty** , na karte **plán** vyberte položku **pridať** a vytvorte úlohu.</span><span class="sxs-lookup"><span data-stu-id="3f476-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Nová úloha vytvorená](media/Resource-Management-image21.png)

2. <span data-ttu-id="3f476-186">V poli **zdroje** vyberte symbol **výberu zdroja**.</span><span class="sxs-lookup"><span data-stu-id="3f476-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="3f476-187">Zobrazí sa výber zdrojov a zobrazí existujúcich členov tímu projektu.</span><span class="sxs-lookup"><span data-stu-id="3f476-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Výber zdroja](media/Resource-Management-image22.png)

3. <span data-ttu-id="3f476-189">Zadajte názov nového všeobecného prostriedku a potom vyberte položku **vytvoriť.**</span><span class="sxs-lookup"><span data-stu-id="3f476-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Názov nového všeobecného zdroja zadaný](media/Resource-Management-image23.png)

4. <span data-ttu-id="3f476-191">V dialógovom okne **rýchle vytvorenie: člena projektového tímu** , ktoré sa zobrazí v poli **rola** , vyberte rolu pre všeobecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="3f476-192">V poli **zdrojová jednotka** vyberte organizačnú jednotku pre všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="3f476-193">Potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3f476-193">Then select **Save**.</span></span>

    ![Zobrazí sa dialógové okno rýchle vytvorenie: člena projektového tímu.](media/Resource-Management-image24.png)

    <span data-ttu-id="3f476-195">Člen všeobecného tímu je teraz priradený k úlohe.</span><span class="sxs-lookup"><span data-stu-id="3f476-195">The generic team member is now assigned to the task.</span></span>

    ![Člen všeobecného tímu je priradený k úlohe.](media/Resource-Management-image25.png)

    <span data-ttu-id="3f476-197">Na karte **tím** sa zobrazí nový všeobecný člen tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="3f476-198">Všimnite si, že má len pridelené hodiny.</span><span class="sxs-lookup"><span data-stu-id="3f476-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="3f476-199">Tieto hodiny sú súčtom všetkých úloh, ktoré sú priradené všeobecnému členovi tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="3f476-200">Všeobecný člen tímu ešte nemá požadované hodiny alebo požiadavku na zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Všeobecný člen tímu na karte tím](media/Resource-Management-image26.png)

5. <span data-ttu-id="3f476-202">Teraz môžete priradiť všeobecného člena tímu k iným úlohám pomocou výberu zdrojov.</span><span class="sxs-lookup"><span data-stu-id="3f476-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Všeobecný člen tímu vo výbere zdrojov](media/Resource-Management-image27.png)

    <span data-ttu-id="3f476-204">Po dokončení priraďovania všeobecného zdroja k úlohám môžete vygenerovať požiadavku zdroja pre všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="3f476-205">Na karte **tím** vyberte všeobecný zdroj a potom vyberte **generovať požiadavku.**</span><span class="sxs-lookup"><span data-stu-id="3f476-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Príkaz generovať požiadavku](media/Resource-Management-image28.png)

    <span data-ttu-id="3f476-207">Po vygenerovaní požiadavky, všeobecný člen tímu bude mať požadované hodiny a odkaz na zdroj požiadavky.</span><span class="sxs-lookup"><span data-stu-id="3f476-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Odkaz na požiadavku na zdroj](media/Resource-Management-image29.png)

    <span data-ttu-id="3f476-209">Po dokončení rezervácie pomenovaného zdroja sa všeobecný zdroj odstráni z tímu a je nahradený pomenovaným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="3f476-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Všeobecný prostriedok nahradený pomenovným zdrojom](media/Resource-Management-image30.png)

    <span data-ttu-id="3f476-211">Na karte **plán** sa všeobecné priradenia zdrojov odstránia a nahradia názvom zdroja.</span><span class="sxs-lookup"><span data-stu-id="3f476-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Na karte plán sa priradenia všeobecných zdrojov odstránia a nahradia sa názvom zdroja.](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="3f476-213">Toto správanie sa vyskytuje len v prípade, že pomenovaný zdroj je plne rezervovaný pre všeobecné zdroje požiadavky.</span><span class="sxs-lookup"><span data-stu-id="3f476-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="3f476-214">Keď buď pomenovaný zdroj čiastočne nahradí požiadavku na generické zdroje alebo viaceré pomenované prostriedky nahradia požiadavku na generické zdroje, všeobecný zdroj zostáva priradený k úlohe.</span><span class="sxs-lookup"><span data-stu-id="3f476-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="3f476-215">Na nasledujúcom obrázku, bola 80-hodinová úloha naplánovaná na päťdňové trvanie (16 hodín denne počas piatich dní) a priradený všeobecný zdroj, ktorý je pomenovaný **funkčný**.</span><span class="sxs-lookup"><span data-stu-id="3f476-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80-hodinová, päťdňová úloha priradená k funkčnému všeobecnému zdroju](media/Resource-Management-image32.png)

    <span data-ttu-id="3f476-217">Keď vygenerujete požiadavku, je to pre 80 hodín v priebehu piatich dní.</span><span class="sxs-lookup"><span data-stu-id="3f476-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Požiadavka vytvorená pre 80 hodín počas piatich dní](media/Resource-Management-image33.png)

    <span data-ttu-id="3f476-219">Keďže dostupné zdroje fungujú len osem hodín denne, na splnenie požiadavky sú potrebné dva zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Druhý zdroj](media/Resource-Management-image35.png)

    <span data-ttu-id="3f476-221">Na karte **tím** teraz môžete vidieť, že všeobecný zdroj nemá požadované hodiny, ale priradené hodiny sa stále zobrazujú spolu s dvomi pomenovanými zdrojmi, ktoré tvoria naplnenie.</span><span class="sxs-lookup"><span data-stu-id="3f476-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Dve pomenované zdroje na karte tím](media/Resource-Management-image36.png)

    <span data-ttu-id="3f476-223">Na karte **plán** zostáva všeobecný zdroj priradený k úlohe.</span><span class="sxs-lookup"><span data-stu-id="3f476-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Všeobecné zdroje na karte Plánovanie](media/Resource-Management-image37.png)

<span data-ttu-id="3f476-225">PSA nepriraďuje oba zdroje k úlohe, pretože toto správanie by produkovalo menej predvídateľný harmonogram.</span><span class="sxs-lookup"><span data-stu-id="3f476-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="3f476-226">V tomto jednoduchom príklade je jednoduché rozdeliť hodiny rovnomerne medzi dva zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="3f476-227">Avšak, v zložitejších scenároch, ktoré zahŕňajú viac úloh a viac zdrojov, PSA bude musieť urobiť predpoklady o tom, ako by mal prideliť rezervácie, ktoré sú prijaté pre viac zdrojov naprieč viacerými úlohami.</span><span class="sxs-lookup"><span data-stu-id="3f476-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="3f476-228">Preto v týchto scenároch, projektový manažér je zodpovedný za analyzovanieí viacerých rezervácií a ich priraďovanie podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="3f476-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="3f476-229">Na pridelenie rezervácie, projektový manažér priradí úlohy zo všeobecných zdrojov na pomenované zdroje a potom používa zobrazenie **odsúhlasenie** na uistenie sa, že pridelenie funguje s rezervami.</span><span class="sxs-lookup"><span data-stu-id="3f476-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="3f476-230">Upravte požiadavku na zdroj</span><span class="sxs-lookup"><span data-stu-id="3f476-230">Edit a resource requirement</span></span>

<span data-ttu-id="3f476-231">Po vytvorení požiadavky zdroja môže manažér projektu alebo Správca zdrojov upraviť podrobnosti, aby sa pri použití tabule plánovania spresnili kritériá vyhľadávania.</span><span class="sxs-lookup"><span data-stu-id="3f476-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="3f476-232">Ak chcete upraviť požiadavku zdroja, postupujte nasledovne.</span><span class="sxs-lookup"><span data-stu-id="3f476-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="3f476-233">Na stránke **projekty** , na karte **tím** vyberte odkaz na akúkoľvek požiadavku na všeobecný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="3f476-234">Na stránke **požiadavky na zdroj** , ktorá sa zobrazí, môžete aktualizovať niekoľko atribútov.</span><span class="sxs-lookup"><span data-stu-id="3f476-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="3f476-235">Tu sú niektoré príklady:</span><span class="sxs-lookup"><span data-stu-id="3f476-235">Here are some examples:</span></span>

    - <span data-ttu-id="3f476-236">Názov</span><span class="sxs-lookup"><span data-stu-id="3f476-236">Name</span></span>
    - <span data-ttu-id="3f476-237">Dátum Od</span><span class="sxs-lookup"><span data-stu-id="3f476-237">From Date</span></span>
    - <span data-ttu-id="3f476-238">Dátum Do</span><span class="sxs-lookup"><span data-stu-id="3f476-238">To Date</span></span>
    - <span data-ttu-id="3f476-239">Trvanie</span><span class="sxs-lookup"><span data-stu-id="3f476-239">Duration</span></span>
    - <span data-ttu-id="3f476-240">Typ zdroja</span><span class="sxs-lookup"><span data-stu-id="3f476-240">Resource Type</span></span>

<span data-ttu-id="3f476-241">Na stránke **požiadavka na zdroj** môže manažér projektu alebo Správca prostriedkov definovať aj nasledujúce informácie:</span><span class="sxs-lookup"><span data-stu-id="3f476-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="3f476-242">Odbornosti</span><span class="sxs-lookup"><span data-stu-id="3f476-242">Skills</span></span>
- <span data-ttu-id="3f476-243">Roly</span><span class="sxs-lookup"><span data-stu-id="3f476-243">Roles</span></span>
- <span data-ttu-id="3f476-244">Predvoľby zdrojov</span><span class="sxs-lookup"><span data-stu-id="3f476-244">Resource preferences</span></span>
- <span data-ttu-id="3f476-245">Preferovaná organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="3f476-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="3f476-246">Aktualizujte rezervácie zdrojov po ich rezervovaní na projekte</span><span class="sxs-lookup"><span data-stu-id="3f476-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="3f476-247">Po pridaní všeobecného alebo pomenovaného zdroja do projektového tímu môžete zmeniť rezervácie prostriedku.</span><span class="sxs-lookup"><span data-stu-id="3f476-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="3f476-248">Ak chcete pridať člena tímu priamo do projektu, na stránke **projekty** na karte **tím** vyberte položku člen tímu a potm vyberte **nový**.</span><span class="sxs-lookup"><span data-stu-id="3f476-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Tabuľa plánovania otvorená pre vybraný člen tímu](media/Resource-Management-image40.png)

    <span data-ttu-id="3f476-250">Zobrazí sa tabuľa plánovania a zobrazí sa rezervácia člena projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="3f476-251">Rozbaľte záznam člena tímu a zobrazte hodiny, ktoré boli rezervované proti tomuto projektu, a ďalšie projekty, ktoré spotrebúvajú kapacitu člena tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="3f476-252">Výberom a presunutím rezervácie ju rozšírte alebo skráťte.</span><span class="sxs-lookup"><span data-stu-id="3f476-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="3f476-253">Zobrazí sa dialógové okno **vytvorenie rezervačného prostriedku** , ktoré umožňuje upraviť rezerváciu.</span><span class="sxs-lookup"><span data-stu-id="3f476-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dialógové okno vytvorenie rezervácie zdroja](media/Resource-Management-image41.png)

3. <span data-ttu-id="3f476-255">Kliknite pravým tlačidlom myši na rezerváciu.</span><span class="sxs-lookup"><span data-stu-id="3f476-255">Right-click the booking.</span></span> <span data-ttu-id="3f476-256">Potom môžete použiť kontextovú ponuku na dokončenie nasledujúcich akcií:</span><span class="sxs-lookup"><span data-stu-id="3f476-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="3f476-257">Zmeňte stav rezervácie</span><span class="sxs-lookup"><span data-stu-id="3f476-257">Change the booking status.</span></span>
    - <span data-ttu-id="3f476-258">Upravte rezerváciu</span><span class="sxs-lookup"><span data-stu-id="3f476-258">Edit the booking.</span></span>
    - <span data-ttu-id="3f476-259">Nahraďte zdroj v projektovom tíme.</span><span class="sxs-lookup"><span data-stu-id="3f476-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="3f476-260">Zmeňte stav rezervácie</span><span class="sxs-lookup"><span data-stu-id="3f476-260">Change the booking status</span></span>

<span data-ttu-id="3f476-261">Môžete zmeniť ľubovoľný predvolený alebo vlastný stav rezervácie.</span><span class="sxs-lookup"><span data-stu-id="3f476-261">You can change any default or custom booking status.</span></span>

![Príkaz zmena stavu](media/Resource-Management-image42.png)

<span data-ttu-id="3f476-263">V PSA sú obsiahnuté nasledujúce stavy:</span><span class="sxs-lookup"><span data-stu-id="3f476-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="3f476-264">**Zrušené** – tento stav zruší rezerváciu zdroja a uvoľní kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="3f476-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="3f476-265">**Tvrdá rezervácia** – tento stav spotrebuje kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="3f476-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="3f476-266">Rezervácia má zvyčajne tento stav pri otvorení **udržiavať rezervácie** od mriežky **všetkých členov tímu** na stránke **projekty**.</span><span class="sxs-lookup"><span data-stu-id="3f476-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="3f476-267">**Jemná rezervácia** – tento stav pridá zdroj do tímu, ale nespotrebuje kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="3f476-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="3f476-268">To naznačuje, že zdroj bol vyhradený pre potenciálnu prácu, ale stále má kapacitu, ak je to potrebné na iné pracovné miesta.</span><span class="sxs-lookup"><span data-stu-id="3f476-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="3f476-269">Vzhľadom na celkovú dostupnosť zdrojov majú mäkké rezervácie iný status ako tvrdé rezervácie.</span><span class="sxs-lookup"><span data-stu-id="3f476-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="3f476-270">**Navrhovaný** – tento stav predstavuje návrh manažéra zdroja alebo projektového manažéra.</span><span class="sxs-lookup"><span data-stu-id="3f476-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="3f476-271">Návrhy nespotrebúvajú kapacitu zdroja a zdroj nie je pridaný do projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="3f476-272">Ak chcete tvrdú rezerváciu zdroja v tíme, projektový manažér musí prijať návrh.</span><span class="sxs-lookup"><span data-stu-id="3f476-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="3f476-273">Odošle žiadosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="3f476-273">Submit resource requests</span></span>

<span data-ttu-id="3f476-274">Požiadavky na zdroje sa používajú na vykonanie dopytu (požiadavka na zdroje), ktorú musí správca zdrojov splniť.</span><span class="sxs-lookup"><span data-stu-id="3f476-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="3f476-275">Pre všeobecný zdroj, ktorý je už v tíme, môžete priamo odoslať požiadavku zdroja.</span><span class="sxs-lookup"><span data-stu-id="3f476-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="3f476-276">Žiadosť o zdroj možno splniť dvomi spôsobmi:</span><span class="sxs-lookup"><span data-stu-id="3f476-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="3f476-277">Správca zdroja priamo splní požiadavku.</span><span class="sxs-lookup"><span data-stu-id="3f476-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="3f476-278">V tomto prípade sa všeobecný zdroj nahradí tvrdou rezerváciou s pomenovaným zdrojom.</span><span class="sxs-lookup"><span data-stu-id="3f476-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="3f476-279">Správca zdrojov navrhne zdroj projektovému manažérovi a projektový manažér schváli alebo odmieta navrhovaný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="3f476-280">Priame naplnenie požiadaviek na zdroje</span><span class="sxs-lookup"><span data-stu-id="3f476-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="3f476-281">Keď vzniká požiadavka na zdroj, projektový manažér môže odoslať požiadavku zdroja pre všeobecný zdroj výberom zdroja a následným výberom položky **Odoslať žiadosť.**</span><span class="sxs-lookup"><span data-stu-id="3f476-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Tlačidlo odoslať žiadosť](media/Resource-Management-image45.png)

<span data-ttu-id="3f476-283">Komentáre k zdroju možno poskytnúť správcovi zdrojov, ktorý spĺňa požiadavku.</span><span class="sxs-lookup"><span data-stu-id="3f476-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="3f476-284">Po odoslaní žiadosti, sa pole **stav** pre člena tímu zmení na **odoslané**.</span><span class="sxs-lookup"><span data-stu-id="3f476-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Zadávanie voliteľných komentárov](media/Resource-Management-image46.png)

<span data-ttu-id="3f476-286">Keď správca zdrojov splní požiadavku, všeobecný člen tímu sa nahradí názvom zdroja v mriežke **všetkých členov** tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Všeobecný člen tímu nahradený názvom zdroja v mriežke všetkých členov tímu](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="3f476-288">Použitie návrhu zdroja pre žiadosti o zdroje</span><span class="sxs-lookup"><span data-stu-id="3f476-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="3f476-289">Namiesto priamej rezervácie zdroja na žiadosť o zdroje môže správca zdrojov navrhnúť zdroj pre projektového manažéra.</span><span class="sxs-lookup"><span data-stu-id="3f476-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="3f476-290">Správca zdrojov môže túto možnosť použiť, ak nie je k dispozícii presná zhoda požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="3f476-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="3f476-291">Keď správca zdrojov navrhne zdroj, projektový manažér vidí, že pole **stav** pre všeobecného člena tímu sa zmení na **prieskum potrieb**.</span><span class="sxs-lookup"><span data-stu-id="3f476-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Stav všeobecného člena tímu sa zmenil na potreba preskúmať](media/Resource-Management-image48.png)

<span data-ttu-id="3f476-293">Ak chcete zobraziť navrhovaný zdroj spolu s vizualizáciou vplyvu rezervácie návrhu, dvakrát kliknite na člena tímu, ktorý má stav **potreba preskúmať**.</span><span class="sxs-lookup"><span data-stu-id="3f476-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="3f476-294">Potom vyberte kartu **navrhované zdroje**.</span><span class="sxs-lookup"><span data-stu-id="3f476-294">Then select the **Proposed Resources** tab.</span></span>

![Karta navrhované zdroje](media/Resource-Management-image49.png)

<span data-ttu-id="3f476-296">Vyberte možnosť **prijať všetky návrhy** , aby ste prijali všetky navrhované zdroje alebo **odmietnuť všetky návrhy** na ich odmietnutie.</span><span class="sxs-lookup"><span data-stu-id="3f476-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="3f476-297">Ak akceptujete navrhované zdroje, sú na projekte natvrdo rezervované ako členovia tímu a nahradia všeobecné zdroje.</span><span class="sxs-lookup"><span data-stu-id="3f476-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="3f476-298">Musíte buď prijať alebo odmietnuť všetky navrhované prostriedky.</span><span class="sxs-lookup"><span data-stu-id="3f476-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="3f476-299">Nemôžete ich čiastočne akceptovať ani odmietnuť.</span><span class="sxs-lookup"><span data-stu-id="3f476-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="3f476-300">Nahraďte zdroj v projektovom tíme.</span><span class="sxs-lookup"><span data-stu-id="3f476-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="3f476-301">Projektový manažér niekedy musí nahradiť rezervovaného člena tímu na projekte.</span><span class="sxs-lookup"><span data-stu-id="3f476-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="3f476-302">Ak chcete pridať člena tímu priamo do projektu, na stránke **projekty** na karte **tím** vyberte položku zdroj ktorý potrebuje výmenu a potom vyberte **udržiavať rezervácie**.</span><span class="sxs-lookup"><span data-stu-id="3f476-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="3f476-303">Rozbaľte zdroj na zobrazenie projektov, ku ktorým je priradený.</span><span class="sxs-lookup"><span data-stu-id="3f476-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Rozšírený zdroj na zobrazenie priradených projektov](media/Resource-Management-image50.png)

3. <span data-ttu-id="3f476-305">Kliknite na projektr pravým tlačidlom myši, a potom vyberte **nahradiť zdroj**.</span><span class="sxs-lookup"><span data-stu-id="3f476-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="3f476-306">Ak poznáte zdroj, ktorým chcete nahradiť aktuálny zdroj, vyberte alebo zadajte názov a potom vyberte položku **znova priradiť.**</span><span class="sxs-lookup"><span data-stu-id="3f476-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Určenie náhradného zdroja](media/Resource-Management-image51.png)

    <span data-ttu-id="3f476-308">Prípadne, ak chcete vyhľadať zdroj, postupujte podľa týchto krokov:</span><span class="sxs-lookup"><span data-stu-id="3f476-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="3f476-309">Vyberte **Hľadať náhradu**.</span><span class="sxs-lookup"><span data-stu-id="3f476-309">Select **Find Substitution**.</span></span>

        ![Hľadanie náhradného zdroja](media/Resource-Management-image52.png)

        <span data-ttu-id="3f476-311">Asistent plánovania vráti zoznam dostupných náhradníkov.</span><span class="sxs-lookup"><span data-stu-id="3f476-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="3f476-312">V Asistentovi plánovania môžete ďalej filtrovať dostupné zdroje a nájsť vhodnú náhradu.</span><span class="sxs-lookup"><span data-stu-id="3f476-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Zoznam dostupných náhrad.](media/Resource-Management-image53.png)

    2. <span data-ttu-id="3f476-314">K nahradeniu zdroja vyberte zdroj, ktorý chcete a potom vyberte **nahradiť**.</span><span class="sxs-lookup"><span data-stu-id="3f476-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Náhradný zdroj je vybraný](media/Resource-Management-image54.png)

    <span data-ttu-id="3f476-316">Rezervácie a priradenia sú nahradené novým zdrojom.</span><span class="sxs-lookup"><span data-stu-id="3f476-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervácie a priradenia nahradené novým zdrojom.](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="3f476-318">Zmierenie rezervácií a priradení člena tímu</span><span class="sxs-lookup"><span data-stu-id="3f476-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="3f476-319">Pre členov tímu sú rezervácie a priradenia voľne spojené.</span><span class="sxs-lookup"><span data-stu-id="3f476-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="3f476-320">Inými slovami, zdroje môžu mať úlohy, ale žiadne rezervácie, alebo môžu mať rezerváciu, ale žiadne úlohy.</span><span class="sxs-lookup"><span data-stu-id="3f476-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="3f476-321">V ideálnom prípade by mali byť rezervácie a úlohy zarovnané tak, aby zdroje zaplnili kapacity na plnenie úloh.</span><span class="sxs-lookup"><span data-stu-id="3f476-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="3f476-322">Rezervácie však môžu byť založené na dostupnosti a časovanie úloh sa môže zmeniť, keď projekt pokračuje.</span><span class="sxs-lookup"><span data-stu-id="3f476-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="3f476-323">Preto voľné spojenie rezervácií a úloh poskytuje flexibilitu.</span><span class="sxs-lookup"><span data-stu-id="3f476-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="3f476-324">PSA má kartu **odsúhlasenie** , ktorá umožňuje projektovým manažérom zosúladiť rezervácie členov tímu a ich úlohy pre projektové tímy.</span><span class="sxs-lookup"><span data-stu-id="3f476-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Karta zmierenia](media/Resource-Management-image56.png)

<span data-ttu-id="3f476-326">Na karte **odsúhlasenie** sa zobrazujú rezervácie a priradenia na úrovni jednotlivých priradení úloh pre každého člena tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="3f476-327">To zobrazuje hodiny v bunkách, ktoré môžu reprezentovať časové periódy od mesiacov ku dňom.</span><span class="sxs-lookup"><span data-stu-id="3f476-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="3f476-328">Na karte sa tiež zobrazuje celková čistá suma projektu spolu s celkovým stĺpcom.</span><span class="sxs-lookup"><span data-stu-id="3f476-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="3f476-329">Pre každý zdroj karta vypočíta rozdiel medzi rezerváciami člena tímu a súhrnom priradení úloh člena tímu.</span><span class="sxs-lookup"><span data-stu-id="3f476-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="3f476-330">V ideálnom prípade by tento rozdiel mal byť 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="3f476-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="3f476-331">Inými slovami, nemal by existovať žiadny rozdiel medzi rezerváciou a úlohami.</span><span class="sxs-lookup"><span data-stu-id="3f476-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="3f476-332">Rozdiely sú farebné a zatienené aby upozornili na dve podmienky:</span><span class="sxs-lookup"><span data-stu-id="3f476-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="3f476-333">**Nedostatok rezervácií** – Nedostatky rezervácií sa objavia, keď má zdroj viac priradení než rezervácie.</span><span class="sxs-lookup"><span data-stu-id="3f476-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="3f476-334">Keďže táto kapacita nebola vyhradená, projektový manažér by túto podmienku mal chcieť napraviť rozšírením rezervácií prostriedkov na krytie deficitu.</span><span class="sxs-lookup"><span data-stu-id="3f476-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="3f476-335">**Rozšírené rezervácie** – Nadmerná rezervácia nastane, keď sa zdroj zarezervuje do projektu, no nebude priradený k úlohám.</span><span class="sxs-lookup"><span data-stu-id="3f476-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="3f476-336">Táto podmienka môže byť prijateľná v prípadoch, keď bol zdroj rezervovaný do projektu pred priradením úlohy.</span><span class="sxs-lookup"><span data-stu-id="3f476-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="3f476-337">V ostatných prípadoch však zdroj nie je naplánovaný na priraďenie k úlohe.</span><span class="sxs-lookup"><span data-stu-id="3f476-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="3f476-338">V takýchto prípadoch by mal projektový manažér zvážiť zrušenie rezervácií prostriedku tak, aby sa kapacita mohla použiť pre iný projekt.</span><span class="sxs-lookup"><span data-stu-id="3f476-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="3f476-339">V niektorých prípadoch, keď zobrazíte čas na vyššej úrovni ako na úrovni dňa (napríklad na úrovni mesiaca), môže sa zobraziť čistý rozdiel nula pre zdroj (inými slovami, rezervácie = úlohy).</span><span class="sxs-lookup"><span data-stu-id="3f476-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="3f476-340">Avšak, ak si prezriete čas na úrovni týždňa, môžete vidieť, že existujú úlohy nula hodín a rezervácie 40 hodín v prvom týždni, ale úlohy 40 hodín a rezervácie nula hodín v druhom týždni.</span><span class="sxs-lookup"><span data-stu-id="3f476-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="3f476-341">Celkovo sú rezervácie a úlohy zmierené, ale líšia sa od jedného týždňa do nasledujúceho.</span><span class="sxs-lookup"><span data-stu-id="3f476-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="3f476-342">Keď zobrazíte čas na vyšších úrovniach, bunky na karte **odsúhlasenie** majú indikátor, ktorý vám oznámi, že existujú rozdiely na nižších úrovniach.</span><span class="sxs-lookup"><span data-stu-id="3f476-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="3f476-343">Dvojitým kliknutím na bunku môžete zväčšiť zobrazenie rozdielu.</span><span class="sxs-lookup"><span data-stu-id="3f476-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="3f476-344">Potom môžete kliknutím pravým tlačidlom myši na vzdialiť. Výberom prostriedku a následným použitím ovládacieho prvku **ďalší rozdiel** na paneli s nástrojmi mriežky môžete prejsť na ďalší rozdiel medzi rezerváciami a priradeniami pre daný zdroj.</span><span class="sxs-lookup"><span data-stu-id="3f476-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="3f476-345">Potom môžete použiť na vrátenie kontrolu **predchádzajúci rozdiel**.</span><span class="sxs-lookup"><span data-stu-id="3f476-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="3f476-346">V časti **nastavenia** môžete tiež vypnúť ukazovateľ rozdielu a správanie navigácie.</span><span class="sxs-lookup"><span data-stu-id="3f476-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Ukazovateľ rozdielu](media/Resource-Management-image57.png)

<span data-ttu-id="3f476-348">Ak máte priradenia úloh pre zdroj, ale žiadne rezervácie, na stránke **projekty** na karte **odsúhlasenie** vyberte nedostatok rezervácie a potom vyberte položku **rozšíriť rezerváciu.**</span><span class="sxs-lookup"><span data-stu-id="3f476-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="3f476-349">Zobrazí sa dialógové okno **rozšíriť rezerváciu** a zobrazí sa rezervácia, ktorá je potrebná na vyriešenie nedostatku zdroja.</span><span class="sxs-lookup"><span data-stu-id="3f476-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="3f476-350">Zobrazuje aj existujúce rezervácie zdrojov vo všetkých projektoch alebo iných plánovateľných entitách.</span><span class="sxs-lookup"><span data-stu-id="3f476-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="3f476-351">Ak vyberiete **OK** , ak chcete vytvoriť rezerváciu zdroja bez ohľadu na dostupnosť tohto prostriedku, môžete spôsobiť prekročenie rezervácie.</span><span class="sxs-lookup"><span data-stu-id="3f476-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialógové okno rozšírenie rezervácie](media/Resource-Management-image58.png)

<span data-ttu-id="3f476-353">Projektový manažér alebo správca zdrojov potom môže pomocou tabule plánovania spravovať všetky situácie, v ktorých je zdroj prerezervovaný nad rámec jeho kapacity.</span><span class="sxs-lookup"><span data-stu-id="3f476-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
