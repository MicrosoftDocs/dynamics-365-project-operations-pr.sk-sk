---
title: Prehľad riadkov zmlúv založených na projekte
description: Táto téma poskytuje informácie o práci s riadkami zmluvy založenými na projekte.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 22e8ff927c5ff6c3748a35031e7703e3fcfe0dab
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369935"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="295e7-103">Prehľad riadkov zmlúv založených na projekte</span><span class="sxs-lookup"><span data-stu-id="295e7-103">Project-based contract lines overview</span></span>

<span data-ttu-id="295e7-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="295e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="295e7-105">Riadky zmluvy založené na projekte v Dynamics 365 Project Operations sú navrhnuté tak, aby uchovávali odhad a fakturačné dohody pre konkrétne komponenty projektovej úlohy na zákazke.</span><span class="sxs-lookup"><span data-stu-id="295e7-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="295e7-106">Štruktúra riadka zmluvy založeného na projekte sa rozširuje pre odhady projektu a scenáre fakturácie s týmito konceptmi:</span><span class="sxs-lookup"><span data-stu-id="295e7-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="295e7-107">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="295e7-107">Billing method</span></span>
- <span data-ttu-id="295e7-108">Mapovanie projektov a úloh</span><span class="sxs-lookup"><span data-stu-id="295e7-108">Project and task mapping</span></span>
- <span data-ttu-id="295e7-109">Zahrnuté triedy transakcií</span><span class="sxs-lookup"><span data-stu-id="295e7-109">Included transaction classes</span></span>
- <span data-ttu-id="295e7-110">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="295e7-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="295e7-111">Nastavenie účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="295e7-111">Chargeability setup</span></span>
- <span data-ttu-id="295e7-112">Odhady pomocou podrobností riadku zmluvy</span><span class="sxs-lookup"><span data-stu-id="295e7-112">Estimates using contract line details</span></span>
- <span data-ttu-id="295e7-113">Zákazníci v riadku zmluvy</span><span class="sxs-lookup"><span data-stu-id="295e7-113">Contract line customers</span></span>

<span data-ttu-id="295e7-114">Nasledujúca tabuľka obsahuje polia na karte **Všeobecné** riadkov zmlúv založených na projektoch, ktoré pomáhajú pripraviť základ pre podrobný, základný odhad a fakturačné podmienky pre prácu na projekte.</span><span class="sxs-lookup"><span data-stu-id="295e7-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="295e7-115">Pole</span><span class="sxs-lookup"><span data-stu-id="295e7-115">Field</span></span> | <span data-ttu-id="295e7-116">Popis</span><span class="sxs-lookup"><span data-stu-id="295e7-116">Description</span></span> | <span data-ttu-id="295e7-117">Nadväzujúci vplyv</span><span class="sxs-lookup"><span data-stu-id="295e7-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="295e7-118">**Názov**</span><span class="sxs-lookup"><span data-stu-id="295e7-118">**Name**</span></span> | <span data-ttu-id="295e7-119">Názov riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-119">Name of the contract line.</span></span> <span data-ttu-id="295e7-120">Toto identifikuje samostatnú zložku zmluvy, ktorá sa odhaduje.</span><span class="sxs-lookup"><span data-stu-id="295e7-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="295e7-121">Pri projektovej zmluve vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušnej hodnoty riadku cenovej ponuky založeného na projekte.</span><span class="sxs-lookup"><span data-stu-id="295e7-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="295e7-122">Názov skopírovaný na riadok projektovej faktúry, ktorý je vytvorený z tohto riadku zmluvy pri vytváraní faktúry.</span><span class="sxs-lookup"><span data-stu-id="295e7-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="295e7-123">**Spôsob fakturácie**</span><span class="sxs-lookup"><span data-stu-id="295e7-123">**Billing Method**</span></span> | <span data-ttu-id="295e7-124">V prípade projektovej zmluvy vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušného poľa v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295e7-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="295e7-125">Toto je množina možností, ktorá predstavuje dva hlavné modely uzatvárania zmlúv podporované aplikáciou Project Operations:</span><span class="sxs-lookup"><span data-stu-id="295e7-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="295e7-126">- **Pevná cena**</span><span class="sxs-lookup"><span data-stu-id="295e7-126">- **Fixed Price**</span></span></br><span data-ttu-id="295e7-127">- **Čas a materiál**</span><span class="sxs-lookup"><span data-stu-id="295e7-127">- **Time and Material**</span></span> | <span data-ttu-id="295e7-128">Skutočná transakcia bude spracovaná na základe spôsobu fakturácie odkazovaného riadka zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="295e7-129">Ak má riadok zmluvy, na ktorý odkazuje skutočná hodnota, časovú a materiálovú metódu fakturácie, vytvoria sa skutočné záznamy o nákladoch a nevyfakturovaných predajoch.</span><span class="sxs-lookup"><span data-stu-id="295e7-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="295e7-130">Ak má riadok zmluvy, na ktorý odkazuje skutočná hodnota, spôsob fakturácie s pevnou cenou, vytvorí sa iba skutočná hodnota nákladu.</span><span class="sxs-lookup"><span data-stu-id="295e7-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="295e7-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="295e7-131">**Project**</span></span> | <span data-ttu-id="295e7-132">Toto pole sa používa na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke.</span><span class="sxs-lookup"><span data-stu-id="295e7-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="295e7-133">Táto hodnota sa použije v spojení s položkami **Zahrnuté úlohy** a **Zahrnuté triedy transakcií** na vyriešenie odkazu na riadok zmluvy v skutočnom alebo odhadovanom riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="295e7-134">**Zahrnuté úlohy**</span><span class="sxs-lookup"><span data-stu-id="295e7-134">**Included Tasks**</span></span> | <span data-ttu-id="295e7-135">Označuje, či tento riadok zmluvy obsahuje všetky projektové úlohy pre vybratý projekt alebo iba podmnožinu úloh.</span><span class="sxs-lookup"><span data-stu-id="295e7-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="295e7-136">Toto je množina možností, ktorá má nasledujúce možné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="295e7-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="295e7-137">- **Všetky projektové úlohy**</span><span class="sxs-lookup"><span data-stu-id="295e7-137">- **All Project Tasks**</span></span></br><span data-ttu-id="295e7-138">- **Iba vybraté projektové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="295e7-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="295e7-139">Prázdna hodnota v tomto poli sa rovná výberu možnosti **Všetky projektové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="295e7-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="295e7-140">Ak je vybraté **Iba vybrané úlohy**, môžete vybrať konkrétne úlohy a priradiť ich k tomuto riadku zmluvy na karte **Nastavenie fakturácie úloh** na stránke **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="295e7-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="295e7-141">Hodnota sa použije v spojení s triedami **Projekt** a **Zahrnuté transakcie** na vyriešenie odkazu na riadok zmluvy na záznamu riadka so skutočnou alebo odhadovanou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="295e7-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="295e7-142">**Zahrnúť čas**</span><span class="sxs-lookup"><span data-stu-id="295e7-142">**Include Time**</span></span> | <span data-ttu-id="295e7-143">Hodnota **Áno**/**Nie** označuje, či budú časové transakcie alebo pracovné náklady na vybranom projekte zahrnuté v tomto riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="295e7-144">Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté časové transakcie ani náklady na prácu.</span><span class="sxs-lookup"><span data-stu-id="295e7-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="295e7-145">Hodnota **Áno** naznačuje, že budú.</span><span class="sxs-lookup"><span data-stu-id="295e7-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="295e7-146">Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka.</span><span class="sxs-lookup"><span data-stu-id="295e7-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="295e7-147">**Zahrnúť výdavok**</span><span class="sxs-lookup"><span data-stu-id="295e7-147">**Include Expense**</span></span> | <span data-ttu-id="295e7-148">Hodnota **Áno**/**Nie** označuje, či budú výdavkové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="295e7-149">Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté nákladové výdavky.</span><span class="sxs-lookup"><span data-stu-id="295e7-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="295e7-150">Hodnota **Áno** naznačuje, že budú.</span><span class="sxs-lookup"><span data-stu-id="295e7-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="295e7-151">Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka.</span><span class="sxs-lookup"><span data-stu-id="295e7-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="295e7-152">**Zahrnúť materiály**</span><span class="sxs-lookup"><span data-stu-id="295e7-152">**Include Materials**</span></span> | <span data-ttu-id="295e7-153">Hodnota **Áno**/**Nie** označuje, či budú materiálové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="295e7-154">Hodnota **Nie** označuje, že materiálové náklady nebudú zahrnuté do tohto riadka zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="295e7-155">Hodnota **Áno** naznačuje, že budú.</span><span class="sxs-lookup"><span data-stu-id="295e7-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="295e7-156">Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka.</span><span class="sxs-lookup"><span data-stu-id="295e7-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="295e7-157">**Zahrnúť poplatok**</span><span class="sxs-lookup"><span data-stu-id="295e7-157">**Include Fee**</span></span> | <span data-ttu-id="295e7-158">Hodnota **Áno**/**Nie** označuje, či budú poplatky na vybranom projekte zahrnuté do odhadu na tomto riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="295e7-159">Hodnota **Nie** označuje, že na tomto riadku zmluvy nebudú zahrnuté poplatky.</span><span class="sxs-lookup"><span data-stu-id="295e7-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="295e7-160">Hodnota **Áno** naznačuje, že budú.</span><span class="sxs-lookup"><span data-stu-id="295e7-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="295e7-161">Táto hodnota sa používa v spojení s projektom na vyriešenie referencie riadka zmluvy na skutočnom alebo odhadovanom zázname riadka.</span><span class="sxs-lookup"><span data-stu-id="295e7-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="295e7-162">**Zmluvná suma**</span><span class="sxs-lookup"><span data-stu-id="295e7-162">**Contracted Amount**</span></span> | <span data-ttu-id="295e7-163">Na riadku zmluvy s pevnou cenou je táto suma dohodnutou hodnotou, ktorá bude zákazníkovi fakturovaná za všetky pracovné komponenty spojené s týmto riadkom zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="295e7-164">Na riadku zmluvy s časom a materiálom je táto suma odhadovanou hodnotou toho, čo bude zákazníkovi fakturované za všetky pracovné komponenty spojené s týmto riadkom zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="295e7-165">V prípade projektovej zmluvy vytvorenej z cenovej ponuky sa táto hodnota skopíruje z príslušného poľa v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295e7-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="295e7-166">Ak má riadok zmluvy založený na projekte podrobnosti riadku, toto pole je uzamknuté pre úpravy a je zosumarizované z čiastky v podrobnostiach riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="295e7-167">Ak má riadok zmluvy podrobnosti o riadku, je možné túto hodnotu upraviť zmenou čiastok v detaile riadku.</span><span class="sxs-lookup"><span data-stu-id="295e7-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="295e7-168">Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie sumy pred zdanením v periodických medzníkoch na fakturovanie.</span><span class="sxs-lookup"><span data-stu-id="295e7-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="295e7-169">**Odhad dane**</span><span class="sxs-lookup"><span data-stu-id="295e7-169">**Estimated Tax**</span></span> | <span data-ttu-id="295e7-170">Používateľ môže toto pole upraviť a do riadku zmluvy vložiť predpokladanú sumu dane.</span><span class="sxs-lookup"><span data-stu-id="295e7-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="295e7-171">Ak má riadok zmluvy založený na projekte podrobnosti riadku, toto pole je uzamknuté pre úpravy a je zosumarizované z čiastky dane v podrobnostiach riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="295e7-172">Ak má riadok zmluvy podrobnosti o riadku, je možné túto hodnotu upraviť zmenou čiastok dane v podrobnostiach riadka.</span><span class="sxs-lookup"><span data-stu-id="295e7-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="295e7-173">Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie dane v periodických medzníkoch na fakturovanie.</span><span class="sxs-lookup"><span data-stu-id="295e7-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="295e7-174">**Zmluvná suma po zdanení**</span><span class="sxs-lookup"><span data-stu-id="295e7-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="295e7-175">Suma v riadku zmluvy po zdanení.</span><span class="sxs-lookup"><span data-stu-id="295e7-175">The contract line amount after tax.</span></span> <span data-ttu-id="295e7-176">Toto pole je iba na čítanie a počíta sa ako **Zmluvná suma + daň**.</span><span class="sxs-lookup"><span data-stu-id="295e7-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="295e7-177">Na riadku zmluvy s pevnou cenou sa táto hodnota používa na generovanie periodických medzníkoch na fakturovanie.</span><span class="sxs-lookup"><span data-stu-id="295e7-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="295e7-178">**Limit, ktorý sa nesmie prekročiť**</span><span class="sxs-lookup"><span data-stu-id="295e7-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="295e7-179">Používateľ môže toto pole upravovať a je k dispozícii iba na riadkoch zmlúv založených na projektoch, ktoré majú metódu fakturácie nastavenú ako čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="295e7-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="295e7-180">Používateľ môže toto pole upraviť.</span><span class="sxs-lookup"><span data-stu-id="295e7-180">The user can edit this field.</span></span> <span data-ttu-id="295e7-181">Keď skutočný čas a materiál odkazuje na tento riadok zmluvy pre čas a materiál, suma na skutočnom sa vyhodnotí oproti limitu na riadku zmluvy, ktorý sa nesmie prekročiť.</span><span class="sxs-lookup"><span data-stu-id="295e7-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="295e7-182">Toto hodnotenie sa dokončí po zaúčtovaní už vynaložených a pridelených súm.</span><span class="sxs-lookup"><span data-stu-id="295e7-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="295e7-183">**Rozpočet zákazníka**</span><span class="sxs-lookup"><span data-stu-id="295e7-183">**Customer Budget**</span></span> | <span data-ttu-id="295e7-184">Toto pole sa dá upravovať a kopíruje sa zo zodpovedajúceho poľa na riadku cenovej ponuky, ak zmluva bola vytvorená z cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295e7-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="295e7-185">Toto pole slúži iba na informačné účely a nemá žiadny následný význam.</span><span class="sxs-lookup"><span data-stu-id="295e7-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="295e7-186">Pravidlá overenia možností na karte Všeobecné v riadkoch zmlúv založených na projektoch</span><span class="sxs-lookup"><span data-stu-id="295e7-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="295e7-187">Pravidlo 1: Ak je pole **Zahrnuté úlohy** prázdne alebo nastavené na **Všetky projektové úlohy**, všetky úlohy projektu sú zahrnuté v riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="295e7-188">Pravidlo 2: Keď je pole **Zahrnuté úlohy** prázdne alebo výslovne nastavené na **Všetky projektové úlohy**, projekt a určitú triedu transakcií možno zahrnúť iba do jedného riadka zmluvy založenej na projekte v rámci zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="295e7-189">Pravidlo 3: Keď je pole **Zahrnuté úlohy** nastavené na **Iba vybraté projektové úlohy**, projekt a určitú triedu transakcií možno zahrnúť do viacerých riadkov zmluvy založenej na projekte v rámci zmluvy.</span><span class="sxs-lookup"><span data-stu-id="295e7-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="295e7-190">
                    <strong>Zmluva</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="295e7-191">
                    <strong>Riadok zmluvy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="295e7-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="295e7-193">
                    <strong>Zahrnuté úlohy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="295e7-194">
                    <strong>Zahrnúť čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="295e7-195">
                    <strong>Zahrnúť výdavok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="295e7-196">
                    <strong>Zahrnúť materiály</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="295e7-197">
                    <strong>Zahrnúť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="295e7-198">
                    <strong>Poplatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="295e7-199">
                    <strong>Platný/neplatný</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="295e7-200">
                    <strong>Dôvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="295e7-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-201">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-202">CL1</span><span class="sxs-lookup"><span data-stu-id="295e7-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-203">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-204">Prázdna</span><span class="sxs-lookup"><span data-stu-id="295e7-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-205">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-206">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-207">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-208">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-209">Neplatný</span><span class="sxs-lookup"><span data-stu-id="295e7-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-210">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="295e7-210">Violation of Rule #2.</span></span> <span data-ttu-id="295e7-211">Čas, náklady, materiály a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy CL1 a CL2.</span><span class="sxs-lookup"><span data-stu-id="295e7-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-212">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-213">CL2</span><span class="sxs-lookup"><span data-stu-id="295e7-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-214">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-215">Prázdna</span><span class="sxs-lookup"><span data-stu-id="295e7-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-216">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-217">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-218">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-219">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-220">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-221">CL1</span><span class="sxs-lookup"><span data-stu-id="295e7-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-222">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-223">Prázdna</span><span class="sxs-lookup"><span data-stu-id="295e7-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-224">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-225">No</span><span class="sxs-lookup"><span data-stu-id="295e7-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-226">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-227">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-228">Neplatný</span><span class="sxs-lookup"><span data-stu-id="295e7-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-229">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="295e7-229">Violation of Rule #2.</span></span> <span data-ttu-id="295e7-230">Čas, materiály a poplatky za projekt P1 sú zahrnuté v oboch riadkoch zmluvy CL1 a CL2.</span><span class="sxs-lookup"><span data-stu-id="295e7-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-231">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-232">CL2</span><span class="sxs-lookup"><span data-stu-id="295e7-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-233">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-234">Prázdna</span><span class="sxs-lookup"><span data-stu-id="295e7-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-235">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-236">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-237">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-238">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-239">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-240">CL1</span><span class="sxs-lookup"><span data-stu-id="295e7-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-241">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-242">Prázdna</span><span class="sxs-lookup"><span data-stu-id="295e7-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-243">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-244">No</span><span class="sxs-lookup"><span data-stu-id="295e7-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-245">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-246">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-247">Platné</span><span class="sxs-lookup"><span data-stu-id="295e7-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-248">Čas, materiály a poplatky za projekt P1 sú zahrnuté v CL1.</span><span class="sxs-lookup"><span data-stu-id="295e7-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="295e7-249">Výdavky na projekt P1 sú zahrnuté v CL2.</span><span class="sxs-lookup"><span data-stu-id="295e7-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="295e7-250">Žiadne prekrývanie toho, čo je obsiahnuté v každom riadku zmluvy, a preto je platné.</span><span class="sxs-lookup"><span data-stu-id="295e7-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-251">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-252">CL2</span><span class="sxs-lookup"><span data-stu-id="295e7-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-253">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-254">Prázdna</span><span class="sxs-lookup"><span data-stu-id="295e7-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-255">No</span><span class="sxs-lookup"><span data-stu-id="295e7-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-256">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-257">No</span><span class="sxs-lookup"><span data-stu-id="295e7-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-258">No</span><span class="sxs-lookup"><span data-stu-id="295e7-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-259">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-260">CL1</span><span class="sxs-lookup"><span data-stu-id="295e7-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-261">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-262">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="295e7-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-263">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-264">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-265">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-266">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-267">Neplatný</span><span class="sxs-lookup"><span data-stu-id="295e7-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-268">Porušenie pravidla č. 2</span><span class="sxs-lookup"><span data-stu-id="295e7-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="295e7-269">C1 zahŕňa čas, materiály, výdavky a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="295e7-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="295e7-270">CL2 zahŕňa čas, , materiály, výdavky a poplatky za celý projekt P1, a preto sa prekrýva s tým, čo je zahrnuté v C1.</span><span class="sxs-lookup"><span data-stu-id="295e7-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-271">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-272">CL2</span><span class="sxs-lookup"><span data-stu-id="295e7-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-273">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-274">Prázdna</span><span class="sxs-lookup"><span data-stu-id="295e7-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-275">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-276">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-277">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-278">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-279">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-280">CL1</span><span class="sxs-lookup"><span data-stu-id="295e7-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-281">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-282">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="295e7-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-283">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-284">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-285">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-286">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-287">Platné</span><span class="sxs-lookup"><span data-stu-id="295e7-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="295e7-288">Podľa pravidla č. 3</span><span class="sxs-lookup"><span data-stu-id="295e7-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="295e7-289">C1 zahŕňa čas, výdavky, materiály a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="295e7-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="295e7-290">CL2 zahŕňa čas, výdavky, materiály a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="295e7-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="295e7-291">Jediné ďalšie overenie je okolo podmnožiny úloh na CL1, ktorá sa líši od podmnožiny úloh CL2, aby sa zabezpečilo, že tu nedôjde k prekrývaniu.</span><span class="sxs-lookup"><span data-stu-id="295e7-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="295e7-292">Vykonáva sa prostredníctvom systému, keď sú priradené úlohy.</span><span class="sxs-lookup"><span data-stu-id="295e7-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="295e7-293">C1</span><span class="sxs-lookup"><span data-stu-id="295e7-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="295e7-294">CL2</span><span class="sxs-lookup"><span data-stu-id="295e7-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-295">P1</span><span class="sxs-lookup"><span data-stu-id="295e7-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="295e7-296">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="295e7-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-297">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="295e7-298">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-299">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="295e7-300">Áno</span><span class="sxs-lookup"><span data-stu-id="295e7-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
