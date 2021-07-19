---
title: Prehľad riadkov cenových ponúk založených na projekte
description: Táto téma poskytuje informácie o používaní riadkov cenových ponúk založených na projekte pre projektovú úlohu.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: b7076a4b9280472f8c30d0b58c3aa9b9bc86d651
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6369890"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="54da7-103">Prehľad riadkov cenových ponúk založených na projekte</span><span class="sxs-lookup"><span data-stu-id="54da7-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="54da7-104">_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="54da7-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="54da7-105">Riadky cenových ponúk založených na projekte sú navrhnuté tak, aby pomohli odhadnúť projektovú úlohu na zákazke.</span><span class="sxs-lookup"><span data-stu-id="54da7-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="54da7-106">Štruktúra riadku cenovej ponuky založenej na projekte sa pre odhady projektu rozširuje o tieto koncepty:</span><span class="sxs-lookup"><span data-stu-id="54da7-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="54da7-107">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="54da7-107">Billing Method</span></span>
- <span data-ttu-id="54da7-108">Mapovanie projektov a úloh</span><span class="sxs-lookup"><span data-stu-id="54da7-108">Project and Task Mapping</span></span>
- <span data-ttu-id="54da7-109">Zahrnuté triedy transakcií</span><span class="sxs-lookup"><span data-stu-id="54da7-109">Included Transaction classes</span></span>
- <span data-ttu-id="54da7-110">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="54da7-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="54da7-111">Nastavenie účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="54da7-111">Chargeability setup</span></span>
- <span data-ttu-id="54da7-112">Odhad pomocou podrobností o riadku cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="54da7-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="54da7-113">Zákazníci v riadkoch cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="54da7-113">Quote line Customers</span></span>

<span data-ttu-id="54da7-114">Nasledujúca tabuľka poskytuje informácie o poliach na karte **Všeobecné** v riadku cenovej ponuky na základe projektu.</span><span class="sxs-lookup"><span data-stu-id="54da7-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="54da7-115">Tieto polia pomáhajú vytvoriť základ pre podrobný a prízemných odhad projektovej úlohy.</span><span class="sxs-lookup"><span data-stu-id="54da7-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="54da7-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="54da7-116">**Field**</span></span> | <span data-ttu-id="54da7-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="54da7-117">**Description**</span></span> | <span data-ttu-id="54da7-118">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="54da7-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="54da7-119">Meno</span><span class="sxs-lookup"><span data-stu-id="54da7-119">Name</span></span> | <span data-ttu-id="54da7-120">Názov riadka cenovej ponuky, ktorý vám pomôže identifikovať diskrétnu zložku cenovej ponuky, ktorá sa odhaduje.</span><span class="sxs-lookup"><span data-stu-id="54da7-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="54da7-121">Skopírované do riadku zmluvy o projekte, ktorý je vytvorený z tohto riadku cenovej ponuky po získaní ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-122">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="54da7-122">Billing Method</span></span> | <span data-ttu-id="54da7-123">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z príslušného poľa na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="54da7-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="54da7-124">Toto pole obsahuje dva hlavné modely uzatvárania zmlúv podporované v aplikácii Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="54da7-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="54da7-125">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="54da7-125">- Fixed price</span></span></br><span data-ttu-id="54da7-126">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="54da7-126">- Time and material.</span></span>| <span data-ttu-id="54da7-127">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-128">Project</span><span class="sxs-lookup"><span data-stu-id="54da7-128">Project</span></span> | <span data-ttu-id="54da7-129">Toto voliteľné pole použite na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke.</span><span class="sxs-lookup"><span data-stu-id="54da7-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="54da7-130">Keď je projekt mapovaný na riadok cenovej ponuky, pomáha to pri nastavovaní účtovateľných úloh a tiež pri uvádzaní odhadu založeného na projekte k riadku cenovej ponuky ako podrobnosti o riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="54da7-131">Ak projekt nie je mapovaný na riadok cenovej ponuky založenej na projekte, odhad by sa mal vytvoriť manuálne vytvorením podrobností o každom riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="54da7-132">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="54da7-133">Zahrnuté úlohy</span><span class="sxs-lookup"><span data-stu-id="54da7-133">Included Tasks</span></span> | <span data-ttu-id="54da7-134">Označuje, či sa tento riadok cenovej ponuky používa pre všetky alebo niektoré projektové úlohy vybratého projektu.</span><span class="sxs-lookup"><span data-stu-id="54da7-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="54da7-135">Toto pole má nasledujúce možné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="54da7-135">This field has the following possible values:</span></span></br><span data-ttu-id="54da7-136">- Všetky projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="54da7-136">- All project tasks</span></span></br><span data-ttu-id="54da7-137">- Iba vybraté projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="54da7-137">- Selected project tasks only</span></span></br><span data-ttu-id="54da7-138">Prázdna hodnota v tomto poli je ekvivalentná s možnosťou **Všetky projektové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="54da7-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="54da7-139">Keď je na stránke projektu vybrané **Iba vybraté projektové úlohy**, karta **Nastavenie fakturácie úloh** vám umožňuje vybrať konkrétne úlohy a priradiť ich k tomuto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="54da7-140">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-141">Zahrnúť čas</span><span class="sxs-lookup"><span data-stu-id="54da7-141">Include Time</span></span> | <span data-ttu-id="54da7-142">Hodnota **Áno**/**Nie** označuje, či budú časové transakcie alebo pracovné náklady na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-143">Hodnota **Nie** označuje, že časové transakcie alebo náklady na prácu nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-144">Hodnota **Áno** označuje, že časové transakcie alebo náklady na prácu budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="54da7-145">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-146">Zahrnúť výdavok</span><span class="sxs-lookup"><span data-stu-id="54da7-146">Include Expense</span></span> | <span data-ttu-id="54da7-147">Hodnota **Áno**/**Nie** označuje, či budú výdavkové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-148">Hodnota **Nie** označuje, že výdavkové náklady nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-149">Hodnota **Áno** označuje, že výdavkové náklady budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="54da7-150">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-151">Zahrnúť materiál</span><span class="sxs-lookup"><span data-stu-id="54da7-151">Include Material</span></span> | <span data-ttu-id="54da7-152">Hodnota **Áno**/**Nie** označuje, či budú materiálové náklady na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-153">Hodnota **Nie** označuje, že materiálové náklady nebudú zahrnuté do odhadu na tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-154">Hodnota **Áno** označuje, že materiálové náklady budú zahrnuté do odhadu na tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="54da7-155">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-156">Zahrnúť poplatok</span><span class="sxs-lookup"><span data-stu-id="54da7-156">Include Fee</span></span> | <span data-ttu-id="54da7-157">Hodnota **Áno**/**Nie** označuje, či budú poplatky na vybranom projekte zahrnuté do odhadu na tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-158">Hodnota **Nie** označuje, že poplatky nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="54da7-159">Hodnota **Áno** označuje, že poplatky budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="54da7-160">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-161">Čiastka ponuky</span><span class="sxs-lookup"><span data-stu-id="54da7-161">Quoted Amount</span></span> | <span data-ttu-id="54da7-162">Toto je suma, ktorá bude zákazníkovi ponúknutá za všetku predpokladanú prácu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="54da7-163">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z poľa **Rozpočet zákazníka** na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="54da7-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="54da7-164">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="54da7-165">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-166">Odhad dane</span><span class="sxs-lookup"><span data-stu-id="54da7-166">Estimated Tax</span></span> | <span data-ttu-id="54da7-167">Toto je upraviteľné pole, kde môže používateľ pridať odhadovanú sumu dane pre riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="54da7-168">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky daní v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="54da7-169">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-170">Čiastka ponuky po zdanení</span><span class="sxs-lookup"><span data-stu-id="54da7-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="54da7-171">Toto pole predstavuje čiastku riadka cenovej ponuky po zdanení a je iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="54da7-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="54da7-172">Čiastka v tomto poli sa počíta ako *Ponúknutá čiastka + daň*.</span><span class="sxs-lookup"><span data-stu-id="54da7-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="54da7-173">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-174">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="54da7-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="54da7-175">Toto pole je upraviteľné a je k dispozícii iba pre riadky ponúk založené na projekte, ktoré majú spôsob účtovania **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="54da7-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="54da7-176">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="54da7-177">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="54da7-177">Customer Budget</span></span> | <span data-ttu-id="54da7-178">Toto pole je upraviteľné a skopíruje sa z príslušného poľa v riadku príležitosti, ak bola cenová ponuka vytvorená z príležitosti.</span><span class="sxs-lookup"><span data-stu-id="54da7-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="54da7-179">Táto hodnota sa skopíruje do riadka projektovej zmluvy, ktorý sa vytvorí z tohto riadka cenovej ponuky, keď je ponuka získaná.</span><span class="sxs-lookup"><span data-stu-id="54da7-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="54da7-180">Pravidlá overenia pre polia na karte Všeobecné v riadkoch cenových ponúk založených na projekte</span><span class="sxs-lookup"><span data-stu-id="54da7-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="54da7-181">**Pravidlo 1**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt je zahrnutý v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="54da7-182">**Pravidlo 2**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť iba do jedného riadka cenovej ponuky založenej na projekte cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="54da7-183">**Pravidlo 3**: Ak je pole **Zahrnuté úlohy** nastavené na **Iba vybrané projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť do viacerých riadkov cenovej ponuky založenej na projekte cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54da7-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="54da7-184">**Pravidlo 4**: Ak má príležitosť viacero cenových ponúk, môžu existovať riadky cenových ponúk z rôznych cenových ponúk, ktoré všetky odkazujú na ten istý projekt a zahŕňajú rovnakú triedu transakcií.</span><span class="sxs-lookup"><span data-stu-id="54da7-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="54da7-185">**Pravidlo 5**: Ak cenové ponuky nepatria do rovnakej príležitosti, nemôžu obsahovať rovnakú triedu projektu a transakcie.</span><span class="sxs-lookup"><span data-stu-id="54da7-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="54da7-186">
                    <strong>Príležitosť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="54da7-187">
                    <strong>Ponuka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="54da7-188">
                    <strong>Riadok cenovej ponuky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="54da7-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="54da7-190">
                    <strong>Zahrnuté úlohy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="54da7-191">
                    <strong>Zahrnúť čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="54da7-192">
                    <strong>Zahrnúť výdavok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="54da7-193">
                    <strong>Zahrnúť materiál</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="54da7-194">
                    <strong>Zahrnúť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="54da7-195">
                    <strong>Poplatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="54da7-196">
                    <strong>Platný/neplatný</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="54da7-197">
                    <strong>Dôvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="54da7-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-198">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-199">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-200">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-201">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-202">Prázdna</span><span class="sxs-lookup"><span data-stu-id="54da7-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-203">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-204">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-205">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-206">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-207">Neplatný</span><span class="sxs-lookup"><span data-stu-id="54da7-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-208">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="54da7-208">Violation of Rule #2.</span></span> <span data-ttu-id="54da7-209">Čas, náklady a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-210">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-211">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-212">QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-213">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-214">Prázdna</span><span class="sxs-lookup"><span data-stu-id="54da7-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-215">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-216">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-217">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-218">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-219">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-220">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-221">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-222">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-223">Prázdna</span><span class="sxs-lookup"><span data-stu-id="54da7-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-224">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-225">No</span><span class="sxs-lookup"><span data-stu-id="54da7-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-226">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-227">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-228">Neplatný</span><span class="sxs-lookup"><span data-stu-id="54da7-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-229">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="54da7-229">Violation of Rule #2.</span></span> <span data-ttu-id="54da7-230">Čas, materiál a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-231">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-232">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-233">QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-234">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-235">Prázdna</span><span class="sxs-lookup"><span data-stu-id="54da7-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-236">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-237">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-238">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-239">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-240">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-241">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-242">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-243">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-244">Prázdna</span><span class="sxs-lookup"><span data-stu-id="54da7-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-245">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-246">No</span><span class="sxs-lookup"><span data-stu-id="54da7-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-247">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-248">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-249">Platné</span><span class="sxs-lookup"><span data-stu-id="54da7-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-250">Čas, materiál a poplatky za projekt P1 sú zahrnuté v QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="54da7-251">Výdavky na projekt P1 sú zahrnuté v QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="54da7-252">Žiadne prekrývanie toho, čo je obsiahnuté v každom riadku cenovej ponuky, a preto je platné.</span><span class="sxs-lookup"><span data-stu-id="54da7-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-253">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-254">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-255">QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-256">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-257">Prázdna</span><span class="sxs-lookup"><span data-stu-id="54da7-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-258">No</span><span class="sxs-lookup"><span data-stu-id="54da7-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-259">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-260">No</span><span class="sxs-lookup"><span data-stu-id="54da7-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-261">No</span><span class="sxs-lookup"><span data-stu-id="54da7-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-262">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-263">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-264">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-265">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-266">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="54da7-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-267">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-268">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-269">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-270">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-271">Neplatný</span><span class="sxs-lookup"><span data-stu-id="54da7-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-272">Porušenie pravidla č. 2</span><span class="sxs-lookup"><span data-stu-id="54da7-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="54da7-273">Q1 zahŕňa čas, materiál, výdavky a poplatky za podmnožinu úloh v projekte P1</span><span class="sxs-lookup"><span data-stu-id="54da7-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="54da7-274">QL2 zahŕňa čas, výdavky a poplatky za celý projekt P1, a preto sa prekrýva s tým, čo je zahrnuté v Q1.</span><span class="sxs-lookup"><span data-stu-id="54da7-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-275">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-276">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-277">QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-278">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-279">Prázdna</span><span class="sxs-lookup"><span data-stu-id="54da7-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-280">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-281">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-282">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-283">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-284">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-285">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-286">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-287">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-288">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="54da7-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-289">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-290">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-291">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-292">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-293">Platné</span><span class="sxs-lookup"><span data-stu-id="54da7-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-294">Podľa pravidla č. 3</span><span class="sxs-lookup"><span data-stu-id="54da7-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="54da7-295">Q1 zahŕňa čas, materiál, výdavky a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="54da7-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="54da7-296">QL2 zahŕňa čas, materiál, výdavky a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="54da7-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="54da7-297">Jediná ďalšie overenie je okolo podmnožiny úloh na QL1, ktorá sa líši od podmnožiny úloh QL2, aby sa zabezpečilo, že nedôjde k ich prekrývaniu.</span><span class="sxs-lookup"><span data-stu-id="54da7-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="54da7-298">Vykonáva sa prostredníctvom systému, keď sú priradené úlohy.</span><span class="sxs-lookup"><span data-stu-id="54da7-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-299">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-300">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-301">QL2</span><span class="sxs-lookup"><span data-stu-id="54da7-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-302">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-303">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="54da7-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-304">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-305">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-306">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-307">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-308">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-309">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-310">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-311">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-312">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="54da7-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-313">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-314">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-315">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-316">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-317">Platné</span><span class="sxs-lookup"><span data-stu-id="54da7-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-318">Podľa pravidla č. 5 sú Q1 a Q2 dve cenové ponuky tej istej príležitosti, takže obidve môžu odhadnúť rovnaké komponenty projektu.</span><span class="sxs-lookup"><span data-stu-id="54da7-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-319">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-320">Š2</span><span class="sxs-lookup"><span data-stu-id="54da7-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-321">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-322">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-323">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="54da7-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-324">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-325">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-326">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-327">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-328">O1</span><span class="sxs-lookup"><span data-stu-id="54da7-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-329">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-330">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-331">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-332">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="54da7-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-333">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-334">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-335">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-336">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-337">Neplatný</span><span class="sxs-lookup"><span data-stu-id="54da7-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="54da7-338">Podľa pravidla č. 4 sú Q1 a Q2 dve cenové ponuky rôznych príležitostí, takže obidve nemôžu odhadnúť rovnaké komponenty toho istého projektu.</span><span class="sxs-lookup"><span data-stu-id="54da7-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="54da7-339">O2</span><span class="sxs-lookup"><span data-stu-id="54da7-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="54da7-340">Q1</span><span class="sxs-lookup"><span data-stu-id="54da7-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="54da7-341">QL1</span><span class="sxs-lookup"><span data-stu-id="54da7-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-342">P1</span><span class="sxs-lookup"><span data-stu-id="54da7-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="54da7-343">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="54da7-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="54da7-344">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="54da7-345">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="54da7-346">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="54da7-347">Áno</span><span class="sxs-lookup"><span data-stu-id="54da7-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
