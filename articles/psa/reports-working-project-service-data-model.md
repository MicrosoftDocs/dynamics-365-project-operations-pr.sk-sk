---
title: Práca s dátovým modelom Project Service Automation
description: Táto téma poskytuje informácie o tom, ako pracovať s dátovým modelom.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 8d63a1b36abe0a154c43e99738340f32f28c2f5e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120292"
---
# <a name="working-with-the-project-service-automation-data-model"></a><span data-ttu-id="5f4f7-103">Práca s dátovým modelom Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="5f4f7-103">Working with the Project Service Automation data model</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5f4f7-104">Dynamics 365 Project Service Automation rozširuje ostatné entity aplikácií a zavádza svoje vlastné entity v Common Data Service dátovom modeli.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-104">Dynamics 365 Project Service Automation extends other app entities and introduces its own entities in the Common Data Service data model.</span></span> <span data-ttu-id="5f4f7-105">Táto téma opisuje niektoré entity, s ktorými sa stretnete v typických scenároch hlásenia PSA.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-105">This topic describes some of the entities that you will encounter in typical PSA reporting scenarios.</span></span>

## <a name="reporting-on-opportunities"></a><span data-ttu-id="5f4f7-106">Vytváranie zostáv o príležitostiach</span><span class="sxs-lookup"><span data-stu-id="5f4f7-106">Reporting on opportunities</span></span>

<span data-ttu-id="5f4f7-107">Project Service Automation rozširuje entitu **Príležitosti** Dynamics 365 Sales pridaním polí, ktoré umožňujú scenáre založené na projekte.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-107">Project Service Automation extends the Dynamics 365 Sales **Opportunity** entity by adding fields that enable project-based scenarios.</span></span> <span data-ttu-id="5f4f7-108">Tieto polia sú identifikované názvom schémy, ktorá je predurčená s **msdyn\_**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-108">These fields are identified by a schema name that is prefixed with **msdyn\_**.</span></span> <span data-ttu-id="5f4f7-109">Jedno nové pole, ktoré je dôležité pre podávanie správ o možnostiach PSA je **Typ objednávky**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-109">One new field that is important for reporting on PSA opportunities is **Order Type**.</span></span> <span data-ttu-id="5f4f7-110">Hodnota **Založené na práci** tohto poľa naznačuje, že príležitosť je príležitosťou PSA.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-110">A value of **Work Based** for this field indicates that the opportunity is a PSA opportunity.</span></span> <span data-ttu-id="5f4f7-111">Medzi ďalšie polia, ktoré boli pridané do entity, patria **Zmluvná organizácia**, ktorá zachytáva organizáciu, ktorá drží príležitosť, a **Manažér obchodného vzťahu**, ktorý zachytáva názov správcu účtu, ktorý je zodpovedný za túto príležitosť.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-111">Other fields that have been added to the entity include **Contracting Organization**, which captures the organization that is holding the opportunity, and **Account Manager**, which captures the name of the account manager who is responsible for the opportunity.</span></span>

<span data-ttu-id="5f4f7-112">Entita **Riadok príležitosti** obsahuje aj polia, ktoré súvisia s Project Service.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-112">The **Opportunity Line** entity also includes fields that are related to Project Service.</span></span> <span data-ttu-id="5f4f7-113">**Spôsob fakturácie** udáva, či sa má riadok príležitosti účtovať na základe času a materiálov alebo na základe pevnej ceny, pričom **Projekt** zachytáva názov projektu, ktorý túto príležitosť podporuje.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-113">**Billing Method** indicates whether the opportunity line should be billed on a time-and-materials basis or a fixed-price basis, and **Project** captures the name of the project that is backing the opportunity.</span></span> <span data-ttu-id="5f4f7-114">Ostatné polia, ktoré môžete využívať na vykazovanie zachytávajú sumy nákladov a rozpočtov zákazníkov pre položku riadka.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-114">Other fields that you can report on capture costs and customer budget amounts for the line item.</span></span>

## <a name="reporting-on-quotes"></a><span data-ttu-id="5f4f7-115">Vykazovanie o cenových ponukách</span><span class="sxs-lookup"><span data-stu-id="5f4f7-115">Reporting on quotes</span></span>

<span data-ttu-id="5f4f7-116">PSA rozširuje entitu **Cenová ponuka** Sales pridaním polí súvisiacich s projektom.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-116">PSA extends the Sales **Quote** entity by adding project-related fields.</span></span> <span data-ttu-id="5f4f7-117">**Typ objednávky** rozlišuje cenové ponuky PSA od cenových ponúk mimo PSA.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-117">**Order Type** distinguishes PSA quotes from non-PSA quotes.</span></span> <span data-ttu-id="5f4f7-118">Hodnota **Založené na práci** tohto poľa naznačuje, že cenová ponuka je cenovou ponukou PSA.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-118">A value of **Work Based** for this field indicates that the quote is a PSA quote.</span></span> <span data-ttu-id="5f4f7-119">Ďalšie polia, ktoré môžu byť relevantné pre vykazovanie cenových ponúk PSA, zahŕňajú polia čiastky, akú sú **Fakturovateľné náklady**, **Nefakturovateľné náklady**, **Hrubá marža**, **Odhady** a **Rozpočet**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-119">Other fields that can be relevant to reporting on PSA quotes include amount fields, such as **Chargeable Costs**, **Non-chargeable Costs**, **Gross Margin**, **Estimates**, and **Budget**.</span></span> <span data-ttu-id="5f4f7-120">Ďalšie užitočné polia označujú, či je cenová ponuka zisková, či už bude dokončená podľa plánu, a či spĺňa očakávania rozpočtu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-120">Other useful fields indicate whether the quote is profitable, whether it will be completed on schedule, and whether it meets the customer's budget expectations.</span></span>

<span data-ttu-id="5f4f7-121">PSA tiež rozširuje entitu **Riadka cenovej ponuky** Sales.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-121">PSA also extends the Sales **Quote Line** entity.</span></span> <span data-ttu-id="5f4f7-122">Jedno pole, ktoré PSA pridáva, je **Spôsob fakturácie**, ktoré udáva, ako sa bude účtovať riadok cenovej ponuky (čas a materiály alebo pevná cena).</span><span class="sxs-lookup"><span data-stu-id="5f4f7-122">One field that PSA adds is **Billing Method**, which indicates how the quote line will be billed (time and materials or fixed price).</span></span> <span data-ttu-id="5f4f7-123">Ostatné polia, ktoré boli pridané do entity zachytávajúcej súvisiaci projekt, ktorý je podporený riadkom cenovej ponuky, fakturácia, náklady a rozpočet.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-123">Other fields that have been added to the entity capture the related project that is backing the quote line, invoicing, cost, and budget.</span></span>

<span data-ttu-id="5f4f7-124">PSA tiež pridáva nové entity súvisiace s cenovou ponukou k dátovému modelu Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-124">PSA also adds new quote-related entities to the Dynamics 365 data model.</span></span> <span data-ttu-id="5f4f7-125">Tu sú niektoré príklady:</span><span class="sxs-lookup"><span data-stu-id="5f4f7-125">Here are some examples:</span></span>

- <span data-ttu-id="5f4f7-126">**Podrobnosti o riadku cenovej ponuky** – Táto entita obsahuje podrobnosti odhadu projektu na riadku cenovej skupiny.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-126">**Quote Line Detail** – This entity contains the project estimate details of the quote line.</span></span> <span data-ttu-id="5f4f7-127">Má dva záznamy pre každý riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-127">It has two records for each quote line.</span></span> <span data-ttu-id="5f4f7-128">Jeden záznam uchováva informácie o nákladoch a nákladoch riadka cenovej ponuky a druhý záznam uchováva čiastku predaja a podrobnosti predaja riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-128">One record stores the cost and cost details of the quote line, and the other record stores the sales amount and sales details of the quote line.</span></span>
- <span data-ttu-id="5f4f7-129">**Plán faktúry v riadku cenovej ponuky** – Táto entita obsahuje plán fakturácie pre riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-129">**Quote Line Invoice Schedule** – This entity contains the billing schedule for the quote line.</span></span> <span data-ttu-id="5f4f7-130">Tento plán je generovaný na základe fakturačnej frekvencie, ktorá je priradená k riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-130">This schedule is generated based on the invoicing frequency that is assigned to the quote line.</span></span>
- <span data-ttu-id="5f4f7-131">**Medzník v riadku cenovej ponuky** – Táto entita obsahuje fakturačné míľniky pre riadky cenovej ponuky s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-131">**Quote Line Milestone** – This entity contains the billing milestones for fixed-price quote lines.</span></span>
- <span data-ttu-id="5f4f7-132">**Rozdelenie analytických údajov riadka cenovej ponuky** – Táto entita obsahuje finančné podrobnosti riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-132">**Quote Line Analytics Breakdown** – This entity contains financial details of the quote line.</span></span> <span data-ttu-id="5f4f7-133">Tieto podrobnosti môžu byť užitočné pre vykazovanie predajnej sumy s cenovou ponuku a sumy odhadovaných nákladov podľa rôznych dimenzií.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-133">These details can be useful for reporting quoted sales and estimated cost amounts by various dimensions.</span></span>

<span data-ttu-id="5f4f7-134">Ostatné entity, ktoré PSA pridáva k cenovým ponukám, sú **Projektový cenník riadka cenovej ponuky**, **Kategória zdroja v riadku cenovej ponuky** a **Kategória transakcie v riadku cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-134">Other entities that PSA adds to quotes are **Quote Line Project Price List**, **Quote Line Resource Category**, and **Quote Line Transaction Category**.</span></span>

<span data-ttu-id="5f4f7-135">![Schéma znázorňujúca cenovú ponuku, riadok cenovej ponuky a vzťahy projektu](media/PS-Reporting-image2.png "Schéma znázorňujúca cenovú ponuku, riadok cenovej ponuky a vzťahy projektu")</span><span class="sxs-lookup"><span data-stu-id="5f4f7-135">![Diagram showing quote, quote line, and project relationships](media/PS-Reporting-image2.png "Diagram showing quote, quote line, and project relationships")</span></span>

## <a name="reporting-on-project-contracts"></a><span data-ttu-id="5f4f7-136">Podávanie správ o projektových zmluvách</span><span class="sxs-lookup"><span data-stu-id="5f4f7-136">Reporting on project contracts</span></span>

<span data-ttu-id="5f4f7-137">PSA rozširuje entitu predajnej **objednávky**, ktorá sa používa na zaznamenávané zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-137">PSA extends the Sales **Order** entity that is used when project contracts are recorded.</span></span> <span data-ttu-id="5f4f7-138">Pridá dôležité nové pole **Typ objednávky**, ktoré identifikuje zmluvu ako projektovú zmluvu PSA namiesto predajnej objednávky.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-138">It adds an important new field, **Order Type**, that identifies the contract as a PSA project contract instead of a sales order.</span></span> <span data-ttu-id="5f4f7-139">Hodnota **Založené na práci** tohto poľa naznačuje, že objednávka je zmluvou projektu PSA.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-139">A value of **Work Based** for this field indicates that the order is a PSA project contract.</span></span> <span data-ttu-id="5f4f7-140">Ďalšie nové polia, ktoré sa pridajú do entity **Objednávka**, zachytávajú podrobnosti o nákladoch, stave zmluvy PSA a organizácii, ktorá vlastní zmluvu.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-140">Other new fields that are added to the **Order** entity capture details about costs, PSA contract status, and the organization that owns the contract.</span></span>

<span data-ttu-id="5f4f7-141">PSA tiež rozširuje entitu **Riadky predajných objednávok**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-141">PSA also extends the **Sales Order Line** entity.</span></span> <span data-ttu-id="5f4f7-142">Medzi polia, ktoré pridáva, patria polia, ktoré zachytávajú metódu fakturácie (čas a materiály alebo pevnú cenu), čiastky rozpočtu zákazníka a základný projekt.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-142">Among the fields that it adds are fields that capture the billing method (time and materials or fixed price), customer budget amounts, and the underlying project.</span></span>

<span data-ttu-id="5f4f7-143">PSA tiež pridáva nové entity, ktoré sú určené pre projektové zmluvy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-143">PSA also adds new entities that are designed for project contracts.</span></span> <span data-ttu-id="5f4f7-144">Tu sú niektoré príklady:</span><span class="sxs-lookup"><span data-stu-id="5f4f7-144">Here are some examples:</span></span>

- <span data-ttu-id="5f4f7-145">**Podrobnosti o riadku projektovej zmluvy** – Táto entita obsahuje podrobnosti o úrovni riadka, ktoré sú zrolované do čiastky riadka zmluvy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-145">**Project Contract Line Detail** – This entity contains the line-level details that are rolled up to the contract line amount.</span></span> <span data-ttu-id="5f4f7-146">Tieto môžu byť tak podrobné ako riadkové položky, ktoré sú generované z plánu projektu na úrovni úlohy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-146">These can be as detailed as line items that are generated from a project schedule at the task level.</span></span>
- <span data-ttu-id="5f4f7-147">**Plán faktúr v riadkoch zmluvy** – Táto entita obsahuje plán fakturácie, ktorý vzniká na základe frekvencie faktúry priradenej k riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-147">**Contract Line Invoice Schedule** – This entity contains the billing schedule that is generated based on the invoice frequency that is assigned to the contract line.</span></span>
- <span data-ttu-id="5f4f7-148">**Medzník zmluvy** – Táto entita obsahuje fakturačné míľniky pre riadky zmluvy, ktoré majú fakturačný výraz s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-148">**Contract Milestone** – This entity contains the billing milestones for contract lines that have a fixed-price billing term.</span></span>

<span data-ttu-id="5f4f7-149">Ostatné entity, ktoré PSA pridáva k zmluvám, sú **Projektový cenník riadka zmluvy**, **Kategória zdroja v riadku projektovej zmluvy** a **Kategória transakcie v riadku projektovej zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-149">Other entities that PSA adds to contracts are **Project Contract Line Project Price List**, **Project Contract Line Resource Category**, and **Project Contract Line Transaction Category**.</span></span>

<span data-ttu-id="5f4f7-150">![Schéma znázorňujúca objednávku, riadok objednávky a vzťahy projektu](media/PS-Reporting-image3.png "Schéma znázorňujúca objednávku, riadok objednávky a vzťahy projektu")</span><span class="sxs-lookup"><span data-stu-id="5f4f7-150">![Diagram showing order, order line, and project relationships](media/PS-Reporting-image3.png "Diagram showing order, order line, and project relationships")</span></span>

## <a name="reporting-on-projects"></a><span data-ttu-id="5f4f7-151">Podávanie správ o projektoch</span><span class="sxs-lookup"><span data-stu-id="5f4f7-151">Reporting on projects</span></span>

<span data-ttu-id="5f4f7-152">Entita **Projekty** a súvisiace entity sú exkluzívne pre PSA.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-152">The **Projects** entity and its related entities are exclusive to PSA.</span></span> <span data-ttu-id="5f4f7-153">**Projekt** je entita najvyššej úrovne, ktorá sa používa na zachytenie práce a nákladov na strane operácií.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-153">**Project** is the top-level entity that is used to capture the work and cost side of operations.</span></span> <span data-ttu-id="5f4f7-154">Tu je zoznam súvisiacich entít:</span><span class="sxs-lookup"><span data-stu-id="5f4f7-154">Here is a list of the related entities:</span></span>

- <span data-ttu-id="5f4f7-155">**Člen projektového tímu** – Táto entita obsahuje podrobnosti o rezervovateľných zdrojoch, ktoré sú priradené k projektu.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-155">**Project team member** – This entity contains details about the bookable resources that are assigned to the project.</span></span> <span data-ttu-id="5f4f7-156">Tieto zdroje môžu byť generické rezervovateľné zdroje, alebo môžu byť pomenované rezervovateľné zdroje, ktoré sú buď zadané zo strany projektového manažéra, alebo generované z plánu projektu.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-156">Those resources can be generic bookable resources, or they can be named bookable resources that are either entered by the project manager or generated from the project schedule.</span></span>
- <span data-ttu-id="5f4f7-157">**Projektová úloha** – Táto entita obsahuje úlohy, ktoré tvoria plán projektu alebo plán.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-157">**Project Task** – This entity contains the tasks that make up the project plan or schedule.</span></span>
- <span data-ttu-id="5f4f7-158">**Priradenie zdroja** – Táto entita obsahuje priradenie úlohy pre rezervovateľný prostriedok.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-158">**Resource Assignment** – This entity contains the task assignment for the bookable resource.</span></span>
- <span data-ttu-id="5f4f7-159">**Požiadavka na zdroj** – Táto entita obsahuje požiadavky pre všetkých členov tímu všeobecných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-159">**Resource Requirement** – This entity contains the requirements for any generic resource team members.</span></span>
- <span data-ttu-id="5f4f7-160">**Odhad** a **Riadok odhadu** – Tieto entity majú vzťah hlavičky a čiary a obsahujú odhady výdavkov pre projekt.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-160">**Estimate** and **Estimate line** – These entities have a header/line relationship and contain expense estimates for the project.</span></span> <span data-ttu-id="5f4f7-161">Odhady úloh sú uložené v entite **Odhad zdroja**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-161">Task estimates are stored on the **Resource Estimate** entity.</span></span>

<span data-ttu-id="5f4f7-162">![Schéma znázorňujúca požiadavku zdroja a vzťahy projektu](media/PS-Reporting-image4.png "Schéma znázorňujúca požiadavku zdroja a vzťahy projektu")</span><span class="sxs-lookup"><span data-stu-id="5f4f7-162">![Diagram showing resource requirement and project relationships](media/PS-Reporting-image4.png "Diagram showing resource requirement and project relationships")</span></span>

## <a name="reporting-on-resources"></a><span data-ttu-id="5f4f7-163">Podávanie správ o zdrojoch</span><span class="sxs-lookup"><span data-stu-id="5f4f7-163">Reporting on resources</span></span>

<span data-ttu-id="5f4f7-164">Projektové prostriedky používajú entity **rezervovateľných zdrojov** od Universal Resource Scheduling (URS), ktoré sú zdieľané s inými aplikáciami, ako je napríklad Microsoft Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-164">Project resources use the **Bookable Resource** entities from Universal Resource Scheduling (URS) that are shared with other apps, such as Microsoft Dynamics 365 Field Service.</span></span> <span data-ttu-id="5f4f7-165">Tu je zoznam entít, ktoré možno budete musieť použiť pri správe o zdrojoch projektu:</span><span class="sxs-lookup"><span data-stu-id="5f4f7-165">Here is a list of the entities that you might have to use when you report on project resources:</span></span>

- <span data-ttu-id="5f4f7-166">**Rezervovateľný zdroj** – Táto entita predstavuje používateľa, kontakt, všeobecný prostriedok, konto, skupinu alebo zariadenie, ktoré sa používa v projektovom tíme.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-166">**Bookable Resource** – This entity represents the user, contact, generic resource, account, group, or equipment that is used on the project team.</span></span>
- <span data-ttu-id="5f4f7-167">**Charakteristiky rezervovateľných zdrojov** – Táto entita zahŕňa zručnosti, certifikácie alebo vzdelávanie zdroja.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-167">**Bookable Resource Characteristics** – This entity includes the skills, certifications, or education of the resource.</span></span> <span data-ttu-id="5f4f7-168">Vlastnosti môžu mať hodnoty hodnotenia, ktoré sú definované modelom hodnotenia.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-168">The characteristics can have rating values that are defined by the rating model.</span></span>
- <span data-ttu-id="5f4f7-169">**Kategória rezervovateľného zdroja** – táto entita predstavuje úlohu rezervovateľného prostriedku.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-169">**Bookable Resource Category** – This entity represents the role of the bookable resource.</span></span>
- <span data-ttu-id="5f4f7-170">**Rezervácie rezervovateľných zdrojov** – táto entita predstavuje čas, ktorý je rezervovaný na projektoch pre zdroj.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-170">**Bookable resource bookings** – This entity represents the time that is booked on projects for the resource.</span></span> <span data-ttu-id="5f4f7-171">Každá rezervácia má hlavičku entity a riadok entity a každý riadok má stav, ktorý predstavuje stav rezervácie.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-171">Each booking has both a header entity and line entities, and each line has a status that represents the status of the booking.</span></span>

<span data-ttu-id="5f4f7-172">![Schéma znázorňujúca vlastnosti vzťahov rezervovateľných zdrojov](media/PS-Reporting-image5.png "Schéma znázorňujúca vlastnosti vzťahov rezervovateľných zdrojov")</span><span class="sxs-lookup"><span data-stu-id="5f4f7-172">![Diagram showing bookable resource characteristics relationships](media/PS-Reporting-image5.png "Diagram showing bookable resource characteristics relationships")</span></span>

## <a name="reporting-on-actual-transactions"></a><span data-ttu-id="5f4f7-173">Podávanie správ o skutočných transakciách</span><span class="sxs-lookup"><span data-stu-id="5f4f7-173">Reporting on actual transactions</span></span>

<span data-ttu-id="5f4f7-174">Keď schválime výkaz alebo náklad, alebo faktúru zmluvu v PSA, obchodná transakcia je zachytená v entite **Skutočné hodnoty**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-174">When you approve a timesheet or expense, or invoice a contract in PSA, the business transaction is captured in the **Actual** entity.</span></span> <span data-ttu-id="5f4f7-175">Táto entita môže slúžiť ako základ pre takmer všetky správy týkajúce sa financií v PSA.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-175">This entity can serve as the basis for almost all finance-related reports in PSA.</span></span> <span data-ttu-id="5f4f7-176">Entita **Skutočná hodnota** zachytáva náklady a predajné transakcie pre obchodnú udalosť.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-176">The **Actual** entity captures the cost and sales transactions for the business event.</span></span> <span data-ttu-id="5f4f7-177">Zachytáva tiež mnoho relevantných atribútov.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-177">It also captures many relevant attributes.</span></span>

<span data-ttu-id="5f4f7-178">Keď pracujete s entitou **Skutočná hodnota**, je dôležité, aby ste pochopili, aké transakcie alebo transakcie sa zaznamenávajú v entite, a kedy sa transakcie zaznamenávajú.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-178">When you're working with the **Actual** entity, it's important that you understand what transaction or transactions are recorded in the entity, and when the transactions are recorded.</span></span> <span data-ttu-id="5f4f7-179">Tu je typický postup pri práci s časmi (tok pre položky výdavkov je podobný):</span><span class="sxs-lookup"><span data-stu-id="5f4f7-179">Here is the typical flow when you work with time entries (the flow for expense entries is similar):</span></span>

1. <span data-ttu-id="5f4f7-180">Keď je položka času uložená, v entite **Skutočná hodnota** sa nevytvoria žiadne záznamy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-180">When the time entry is saved, no records are created in the **Actual** entity.</span></span>
2. <span data-ttu-id="5f4f7-181">Keď je položka času odoslaná, v entite **Skutočná hodnota** sa nevytvoria žiadne záznamy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-181">When the time entry is submitted, no records are created in the **Actual** entity.</span></span>
3. <span data-ttu-id="5f4f7-182">Po schválení časovej položky sa vytvorí jeden záznam v entite **Skutočná hodnota** a môže sa vytvoriť aj druhý záznam.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-182">When the time entry is approved, one record is be created in the **Actual** entity, and a second record can also be created.</span></span> <span data-ttu-id="5f4f7-183">Prvý záznam ukladá náklady na zadanie času.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-183">The first record stores the cost of the time entry.</span></span> <span data-ttu-id="5f4f7-184">Druhý záznam ukladá nefakturovanú čiastku predaja zadania času.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-184">The second record stores the unbilled sales amount of the time entry.</span></span> <span data-ttu-id="5f4f7-185">Druhý záznam závisí od projektu, ktorý má zákazníka, cenovú ponuku alebo riadok zmluvy, ktorý mu bol priradený.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-185">The second record is dependent on the project either having a customer, a quote, or a contract line assigned to it.</span></span>

    | <span data-ttu-id="5f4f7-186">Dátum dokumentu</span><span class="sxs-lookup"><span data-stu-id="5f4f7-186">Document date</span></span> | <span data-ttu-id="5f4f7-187">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="5f4f7-187">Transaction type</span></span> | <span data-ttu-id="5f4f7-188">Trieda transakcie</span><span class="sxs-lookup"><span data-stu-id="5f4f7-188">Transaction class</span></span> | <span data-ttu-id="5f4f7-189">Zákazník</span><span class="sxs-lookup"><span data-stu-id="5f4f7-189">Customer</span></span>         | <span data-ttu-id="5f4f7-190">Zmluva</span><span class="sxs-lookup"><span data-stu-id="5f4f7-190">Contract</span></span>   | <span data-ttu-id="5f4f7-191">Zdroj</span><span class="sxs-lookup"><span data-stu-id="5f4f7-191">Resource</span></span>     | <span data-ttu-id="5f4f7-192">Rola zdroja</span><span class="sxs-lookup"><span data-stu-id="5f4f7-192">Resource role</span></span> | <span data-ttu-id="5f4f7-193">Typ fakturácie</span><span class="sxs-lookup"><span data-stu-id="5f4f7-193">Billing type</span></span> | <span data-ttu-id="5f4f7-194">Množstvo</span><span class="sxs-lookup"><span data-stu-id="5f4f7-194">Quantity</span></span> | <span data-ttu-id="5f4f7-195">Jednotková cena</span><span class="sxs-lookup"><span data-stu-id="5f4f7-195">Unit price</span></span> | <span data-ttu-id="5f4f7-196">Čiastka</span><span class="sxs-lookup"><span data-stu-id="5f4f7-196">Amount</span></span> |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|--------|
    | <span data-ttu-id="5f4f7-197">2/3/18</span><span class="sxs-lookup"><span data-stu-id="5f4f7-197">2/3/18</span></span>        | <span data-ttu-id="5f4f7-198">Náklady</span><span class="sxs-lookup"><span data-stu-id="5f4f7-198">Cost</span></span>             | <span data-ttu-id="5f4f7-199">Time</span><span class="sxs-lookup"><span data-stu-id="5f4f7-199">Time</span></span>              | <span data-ttu-id="5f4f7-200">Alpine Ski House</span><span class="sxs-lookup"><span data-stu-id="5f4f7-200">Alpine ski house</span></span> | <span data-ttu-id="5f4f7-201">Alpine CRM</span><span class="sxs-lookup"><span data-stu-id="5f4f7-201">Alpine CRM</span></span> | <span data-ttu-id="5f4f7-202">Jarmila Gajdošová</span><span class="sxs-lookup"><span data-stu-id="5f4f7-202">Ashley Chinn</span></span> | <span data-ttu-id="5f4f7-203">Project Mgr</span><span class="sxs-lookup"><span data-stu-id="5f4f7-203">Project Mgr</span></span>   | <span data-ttu-id="5f4f7-204">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="5f4f7-204">Chargeable</span></span>   | <span data-ttu-id="5f4f7-205">8.0</span><span class="sxs-lookup"><span data-stu-id="5f4f7-205">8.0</span></span>      | <span data-ttu-id="5f4f7-206">50.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-206">50.00</span></span>      | <span data-ttu-id="5f4f7-207">400.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-207">400.00</span></span> |
    | <span data-ttu-id="5f4f7-208">2/3/18</span><span class="sxs-lookup"><span data-stu-id="5f4f7-208">2/3/18</span></span>        | <span data-ttu-id="5f4f7-209">Nefakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="5f4f7-209">Unbilled sales</span></span>   | <span data-ttu-id="5f4f7-210">Time</span><span class="sxs-lookup"><span data-stu-id="5f4f7-210">Time</span></span>              | <span data-ttu-id="5f4f7-211">Alpine Ski House</span><span class="sxs-lookup"><span data-stu-id="5f4f7-211">Alpine ski house</span></span> | <span data-ttu-id="5f4f7-212">Alpine CRM</span><span class="sxs-lookup"><span data-stu-id="5f4f7-212">Alpine CRM</span></span> | <span data-ttu-id="5f4f7-213">Jarmila Gajdošová</span><span class="sxs-lookup"><span data-stu-id="5f4f7-213">Ashley Chinn</span></span> | <span data-ttu-id="5f4f7-214">Project Mgr</span><span class="sxs-lookup"><span data-stu-id="5f4f7-214">Project Mgr</span></span>   | <span data-ttu-id="5f4f7-215">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="5f4f7-215">Chargeable</span></span>   | <span data-ttu-id="5f4f7-216">8.0</span><span class="sxs-lookup"><span data-stu-id="5f4f7-216">8.0</span></span>      | <span data-ttu-id="5f4f7-217">100.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-217">100.00</span></span>     | <span data-ttu-id="5f4f7-218">800.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-218">800.00</span></span> |

    <span data-ttu-id="5f4f7-219">Tieto dva záznamy sú samostatné, ale súvisiace záznamy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-219">These two records are separate but related records.</span></span> <span data-ttu-id="5f4f7-220">Nie sú ani inkasá ani kredity.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-220">They are neither debits nor credits.</span></span>

4. <span data-ttu-id="5f4f7-221">Ak je zmluva priradená k projektu, keď je položka času fakturovaná, v entite **Skutočná hodnota** sa vytvoria ďalšie dva záznamy.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-221">If a contract is associated with the project, when the time entry is invoiced, two more records are created in the **Actual** entity.</span></span> <span data-ttu-id="5f4f7-222">Najprv sa vytvorí záporná čiastka pre nefakturovaný predajný záznam.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-222">First, a negative amount for the unbilled sales record is created.</span></span> <span data-ttu-id="5f4f7-223">Tento záznam v podstate vracia nefakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-223">This record essentially reverses the unbilled sale.</span></span> <span data-ttu-id="5f4f7-224">Po druhé, vytvorí sa transakcia pre fakturovaný predaj.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-224">Second, a transaction for the billed sale is created.</span></span> <span data-ttu-id="5f4f7-225">Tieto záznamy sú znova samostatné, ale súvisiace záznamy, nie inkasá ani kredity.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-225">Once again, these records are separate but related records, not debits and credits.</span></span>

    | <span data-ttu-id="5f4f7-226">Dátum dokumentu</span><span class="sxs-lookup"><span data-stu-id="5f4f7-226">Document date</span></span> | <span data-ttu-id="5f4f7-227">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="5f4f7-227">Transaction type</span></span> | <span data-ttu-id="5f4f7-228">Trieda transakcie</span><span class="sxs-lookup"><span data-stu-id="5f4f7-228">Transaction class</span></span> | <span data-ttu-id="5f4f7-229">Zákazník</span><span class="sxs-lookup"><span data-stu-id="5f4f7-229">Customer</span></span>         | <span data-ttu-id="5f4f7-230">Zmluva</span><span class="sxs-lookup"><span data-stu-id="5f4f7-230">Contract</span></span>   | <span data-ttu-id="5f4f7-231">Zdroj</span><span class="sxs-lookup"><span data-stu-id="5f4f7-231">Resource</span></span>     | <span data-ttu-id="5f4f7-232">Rola zdroja</span><span class="sxs-lookup"><span data-stu-id="5f4f7-232">Resource role</span></span> | <span data-ttu-id="5f4f7-233">Typ fakturácie</span><span class="sxs-lookup"><span data-stu-id="5f4f7-233">Billing type</span></span> | <span data-ttu-id="5f4f7-234">Množstvo</span><span class="sxs-lookup"><span data-stu-id="5f4f7-234">Quantity</span></span> | <span data-ttu-id="5f4f7-235">Jednotková cena</span><span class="sxs-lookup"><span data-stu-id="5f4f7-235">Unit price</span></span> | <span data-ttu-id="5f4f7-236">Čiastka</span><span class="sxs-lookup"><span data-stu-id="5f4f7-236">Amount</span></span>   |
    |---------------|------------------|-------------------|------------------|------------|--------------|---------------|--------------|----------|------------|----------|
    | <span data-ttu-id="5f4f7-237">2/4/18</span><span class="sxs-lookup"><span data-stu-id="5f4f7-237">2/4/18</span></span>        | <span data-ttu-id="5f4f7-238">Nefakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="5f4f7-238">Unbilled sales</span></span>   | <span data-ttu-id="5f4f7-239">Time</span><span class="sxs-lookup"><span data-stu-id="5f4f7-239">Time</span></span>              | <span data-ttu-id="5f4f7-240">Alpine Ski House</span><span class="sxs-lookup"><span data-stu-id="5f4f7-240">Alpine ski house</span></span> | <span data-ttu-id="5f4f7-241">Alpine CRM</span><span class="sxs-lookup"><span data-stu-id="5f4f7-241">Alpine CRM</span></span> | <span data-ttu-id="5f4f7-242">Jarmila Gajdošová</span><span class="sxs-lookup"><span data-stu-id="5f4f7-242">Ashley Chinn</span></span> | <span data-ttu-id="5f4f7-243">Project Mgr</span><span class="sxs-lookup"><span data-stu-id="5f4f7-243">Project Mgr</span></span>   | <span data-ttu-id="5f4f7-244">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="5f4f7-244">Chargeable</span></span>   | <span data-ttu-id="5f4f7-245">- 8.0</span><span class="sxs-lookup"><span data-stu-id="5f4f7-245">- 8.0</span></span>    | <span data-ttu-id="5f4f7-246">100.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-246">100.00</span></span>     | <span data-ttu-id="5f4f7-247">- 800.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-247">- 800.00</span></span> |
    | <span data-ttu-id="5f4f7-248">2/4/18</span><span class="sxs-lookup"><span data-stu-id="5f4f7-248">2/4/18</span></span>        | <span data-ttu-id="5f4f7-249">Fakturovaný predaj</span><span class="sxs-lookup"><span data-stu-id="5f4f7-249">Billed sales</span></span>     | <span data-ttu-id="5f4f7-250">Time</span><span class="sxs-lookup"><span data-stu-id="5f4f7-250">Time</span></span>              | <span data-ttu-id="5f4f7-251">Alpine Ski House</span><span class="sxs-lookup"><span data-stu-id="5f4f7-251">Alpine ski house</span></span> | <span data-ttu-id="5f4f7-252">Alpine CRM</span><span class="sxs-lookup"><span data-stu-id="5f4f7-252">Alpine CRM</span></span> | <span data-ttu-id="5f4f7-253">Jarmila Gajdošová</span><span class="sxs-lookup"><span data-stu-id="5f4f7-253">Ashley Chinn</span></span> | <span data-ttu-id="5f4f7-254">Project Mgr</span><span class="sxs-lookup"><span data-stu-id="5f4f7-254">Project Mgr</span></span>   | <span data-ttu-id="5f4f7-255">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="5f4f7-255">Chargeable</span></span>   | <span data-ttu-id="5f4f7-256">8.0</span><span class="sxs-lookup"><span data-stu-id="5f4f7-256">8.0</span></span>      | <span data-ttu-id="5f4f7-257">100.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-257">100.00</span></span>     | <span data-ttu-id="5f4f7-258">800.00</span><span class="sxs-lookup"><span data-stu-id="5f4f7-258">800.00</span></span>   |

<span data-ttu-id="5f4f7-259">Entita **Pôvod transakcie** zaznamenáva pôvod záznamu **Skutočná hodnota** a entita **Kontaktná osoba pre transakciu** zaznamenáva súvisiace záznamy pre záznam **Skutočná hodnota**.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-259">The **Transaction Origin** entity records the origin of the **Actual** record, and the **Transaction Connection** entity records the related records for the **Actual** record.</span></span> <span data-ttu-id="5f4f7-260">Okrem toho záznam **Skutočná hodnota** obsahuje odkazy projektu, projektovú zmluvy (objednávka), rezervovateľný zdroj a zákazníka.</span><span class="sxs-lookup"><span data-stu-id="5f4f7-260">Additionally, the **Actual** record contains references the project, project contract (order), bookable resource, and customer.</span></span>

<span data-ttu-id="5f4f7-261">![Schéma znázorňujúca transakčné spojenie, pôvod a skutočné vzťahy](media/PS-Reporting-image6.png "Schéma znázorňujúca transakčné spojenie, pôvod a skutočné vzťahy")</span><span class="sxs-lookup"><span data-stu-id="5f4f7-261">![Diagram showing transaction connection, origin and actual relationships](media/PS-Reporting-image6.png "Diagram showing transaction connection, origin and actual relationships")</span></span>