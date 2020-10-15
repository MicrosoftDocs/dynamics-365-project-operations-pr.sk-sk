---
title: Riadky cenových ponúk založených na projekte (Pro)
description: Táto téma poskytuje informácie o používaní riadkov cenových ponúk založených na projekte pre projektovú úlohu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908585"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="d107b-104">Riadky cenových ponúk založených na projekte (Pro)</span><span class="sxs-lookup"><span data-stu-id="d107b-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="d107b-105">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="d107b-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d107b-106">Riadky cenových ponúk založených na projekte sú navrhnuté tak, aby pomohli odhadnúť projektovú úlohu na zákazke.</span><span class="sxs-lookup"><span data-stu-id="d107b-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="d107b-107">Štruktúra riadku cenovej ponuky založenej na projekte sa pre odhady projektu rozširuje o tieto koncepty:</span><span class="sxs-lookup"><span data-stu-id="d107b-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="d107b-108">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="d107b-108">Billing Method</span></span>
- <span data-ttu-id="d107b-109">Mapovanie projektov a úloh</span><span class="sxs-lookup"><span data-stu-id="d107b-109">Project and Task Mapping</span></span>
- <span data-ttu-id="d107b-110">Zahrnuté triedy transakcií</span><span class="sxs-lookup"><span data-stu-id="d107b-110">Included Transaction classes</span></span>
- <span data-ttu-id="d107b-111">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="d107b-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="d107b-112">Nastavenie účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="d107b-112">Chargeability setup</span></span>
- <span data-ttu-id="d107b-113">Odhad pomocou podrobností o riadku cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="d107b-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="d107b-114">Zákazníci v riadkoch cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="d107b-114">Quote line Customers</span></span>

<span data-ttu-id="d107b-115">Nasledujúca tabuľka poskytuje informácie o poliach na karte **Všeobecné** v riadku cenovej ponuky na základe projektu.</span><span class="sxs-lookup"><span data-stu-id="d107b-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="d107b-116">Tieto polia pomáhajú vytvoriť základ pre podrobný a prízemných odhad projektovej úlohy.</span><span class="sxs-lookup"><span data-stu-id="d107b-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="d107b-117">**Pole**</span><span class="sxs-lookup"><span data-stu-id="d107b-117">**Field**</span></span> | <span data-ttu-id="d107b-118">**Relevantnosť, účel a pokyny**</span><span class="sxs-lookup"><span data-stu-id="d107b-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="d107b-119">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="d107b-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="d107b-120">Meno</span><span class="sxs-lookup"><span data-stu-id="d107b-120">Name</span></span> | <span data-ttu-id="d107b-121">Názov riadka cenovej ponuky, ktorý by vám mal pomôcť identifikovať diskrétnu zložku cenovej ponuky, ktorá sa odhaduje.</span><span class="sxs-lookup"><span data-stu-id="d107b-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="d107b-122">Skopírované do riadku zmluvy o projekte, ktorý je vytvorený z tohto riadku cenovej ponuky po získaní ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-123">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="d107b-123">Billing Method</span></span> | <span data-ttu-id="d107b-124">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z príslušného poľa na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="d107b-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="d107b-125">Toto pole obsahuje dva hlavné zmluvné modely, ktoré podporuje Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d107b-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="d107b-126">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="d107b-126">- Fixed price</span></span></br><span data-ttu-id="d107b-127">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="d107b-127">- Time and material.</span></span>| <span data-ttu-id="d107b-128">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-129">Project</span><span class="sxs-lookup"><span data-stu-id="d107b-129">Project</span></span> | <span data-ttu-id="d107b-130">Toto voliteľné pole použite na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke.</span><span class="sxs-lookup"><span data-stu-id="d107b-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="d107b-131">Keď je projekt mapovaný na riadok cenovej ponuky, pomáha to pri nastavovaní účtovateľných úloh a tiež pri uvádzaní odhadu založeného na projekte k riadku cenovej ponuky ako podrobnosti o riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="d107b-132">Ak projekt nie je mapovaný na riadok cenovej ponuky založenej na projekte, odhad by sa mal vytvoriť manuálne vytvorením podrobností o každom riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="d107b-133">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="d107b-134">Zahrnuté úlohy</span><span class="sxs-lookup"><span data-stu-id="d107b-134">Included Tasks</span></span> | <span data-ttu-id="d107b-135">Označuje, či sa tento riadok cenovej ponuky používa pre všetky alebo niektoré projektové úlohy vybratého projektu.</span><span class="sxs-lookup"><span data-stu-id="d107b-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="d107b-136">Toto pole má nasledujúce možné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="d107b-136">This field has the following possible values:</span></span></br><span data-ttu-id="d107b-137">- Všetky projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="d107b-137">- All project tasks</span></span></br><span data-ttu-id="d107b-138">- Iba vybraté projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="d107b-138">- Selected project tasks only</span></span></br><span data-ttu-id="d107b-139">Prázdna hodnota v tomto poli je ekvivalentná s možnosťou **Všetky projektové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="d107b-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="d107b-140">Ak je na stránke projektu vybraná možnosť **Iba vybrané projektové úlohy**, tak vám karta **Nastavenie fakturácie úloh** umožňuje vybrať konkrétne úlohy a priradiť ich k tomuto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="d107b-141">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-142">Zahrnúť čas</span><span class="sxs-lookup"><span data-stu-id="d107b-142">Include Time</span></span> | <span data-ttu-id="d107b-143">Príznak **Áno**/**Nie** označuje, či budú časové transakcie alebo náklady na prácu na vybranom projekte zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d107b-144">Hodnota **Nie** označuje, že časové transakcie alebo náklady na prácu nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d107b-145">Hodnota **Áno** označuje, že časové transakcie alebo náklady na prácu budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d107b-146">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-147">Zahrnúť výdavok</span><span class="sxs-lookup"><span data-stu-id="d107b-147">Include Expense</span></span> | <span data-ttu-id="d107b-148">Príznak **Áno**/**Nie** označuje, či budú výdavkové náklady vybraného projektu zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d107b-149">Hodnota **Nie** označuje, že výdavkové náklady nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d107b-150">Hodnota **Áno** označuje, že výdavkové náklady budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d107b-151">Hodnota z tohto poľa sa prekopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-152">Zahrnúť poplatok</span><span class="sxs-lookup"><span data-stu-id="d107b-152">Include Fee</span></span> | <span data-ttu-id="d107b-153">Príznak **Áno**/**Nie** označuje, či budú poplatky vybraného projektu zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="d107b-154">Hodnota **Nie** označuje, že poplatky nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="d107b-155">Hodnota **Áno** označuje, že poplatky budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="d107b-156">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-157">Čiastka ponuky</span><span class="sxs-lookup"><span data-stu-id="d107b-157">Quoted Amount</span></span> | <span data-ttu-id="d107b-158">Toto je suma, ktorá bude zákazníkovi ponúknutá za všetku prácu predpokladanú v tomto riadku cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="d107b-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="d107b-159">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z poľa **Rozpočet zákazníka** na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="d107b-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="d107b-160">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="d107b-161">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-162">Odhad dane</span><span class="sxs-lookup"><span data-stu-id="d107b-162">Estimated Tax</span></span> | <span data-ttu-id="d107b-163">Toto je upraviteľné pole, kde môže používateľ pridať odhadovanú sumu dane pre riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="d107b-164">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky daní v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="d107b-165">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-166">Čiastka ponuky po zdanení</span><span class="sxs-lookup"><span data-stu-id="d107b-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="d107b-167">Toto pole predstavuje čiastku riadka cenovej ponuky po zdanení a je iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="d107b-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="d107b-168">Čiastka v tomto poli sa počíta ako *Ponúknutá čiastka + daň*.</span><span class="sxs-lookup"><span data-stu-id="d107b-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="d107b-169">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-170">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="d107b-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="d107b-171">Toto pole je upraviteľné a je k dispozícii iba pre riadky ponúk založené na projekte, ktoré majú spôsob účtovania **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="d107b-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="d107b-172">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="d107b-173">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="d107b-173">Customer Budget</span></span> | <span data-ttu-id="d107b-174">Toto pole je upraviteľné a skopíruje sa z príslušného poľa v riadku príležitosti, ak bola cenová ponuka vytvorená z príležitosti.</span><span class="sxs-lookup"><span data-stu-id="d107b-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="d107b-175">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="d107b-176">Pravidlá overenia pre polia na karte Všeobecné v riadkoch cenových ponúk založených na projekte</span><span class="sxs-lookup"><span data-stu-id="d107b-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="d107b-177">**Pravidlo 1**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt je zahrnutý v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="d107b-178">**Pravidlo 2**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť iba do jedného riadka cenovej ponuky založenej na projekte cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="d107b-179">**Pravidlo 3**: Ak je pole **Zahrnuté úlohy** nastavené na **Iba vybrané projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť do viacerých riadkov cenovej ponuky založenej na projekte cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d107b-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="d107b-180">**Pravidlo 4**: Ak má príležitosť viacero cenových ponúk, môžu existovať riadky cenových ponúk z rôznych cenových ponúk, ktoré všetky odkazujú na ten istý projekt a zahŕňajú rovnakú triedu transakcií.</span><span class="sxs-lookup"><span data-stu-id="d107b-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="d107b-181">**Pravidlo 5**: Ak cenové ponuky nepatria do rovnakej príležitosti, nemôžu obsahovať rovnakú triedu projektu a transakcie.</span><span class="sxs-lookup"><span data-stu-id="d107b-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="d107b-182">
                    <strong>Príležitosť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="d107b-183">
                    <strong>Ponuka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d107b-184">
                    <strong>Riadok cenovej ponuky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d107b-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="d107b-186">
                    <strong>Zahrnuté úlohy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d107b-187">
                    <strong>Zahrnúť čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="d107b-188">
                    <strong>Zahrnúť výdavok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="d107b-189">
                    <strong>Zahrnúť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="d107b-190">
                    <strong>Poplatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="d107b-191">
                    <strong>Platný/neplatný</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="d107b-192">
                    <strong>Dôvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="d107b-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-193">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-194">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-195">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-196">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-197">Prázdna</span><span class="sxs-lookup"><span data-stu-id="d107b-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-198">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-199">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-200">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-201">Neplatný</span><span class="sxs-lookup"><span data-stu-id="d107b-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-202">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="d107b-202">Violation of Rule #2.</span></span> <span data-ttu-id="d107b-203">Čas, náklady a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2.</span><span class="sxs-lookup"><span data-stu-id="d107b-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-204">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-205">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-206">QL2</span><span class="sxs-lookup"><span data-stu-id="d107b-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-207">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-208">Prázdna</span><span class="sxs-lookup"><span data-stu-id="d107b-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-209">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-210">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-211">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-211">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-212">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-213">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-214">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-215">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-216">Prázdna</span><span class="sxs-lookup"><span data-stu-id="d107b-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-217">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-218">No</span><span class="sxs-lookup"><span data-stu-id="d107b-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-219">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-220">Neplatný</span><span class="sxs-lookup"><span data-stu-id="d107b-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-221">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="d107b-221">Violation of Rule #2.</span></span> <span data-ttu-id="d107b-222">Čas a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2.</span><span class="sxs-lookup"><span data-stu-id="d107b-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-223">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-224">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-225">QL2</span><span class="sxs-lookup"><span data-stu-id="d107b-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-226">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-227">Prázdna</span><span class="sxs-lookup"><span data-stu-id="d107b-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-228">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-229">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-230">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-230">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-231">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-232">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-233">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-234">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-235">Prázdna</span><span class="sxs-lookup"><span data-stu-id="d107b-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-236">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-237">No</span><span class="sxs-lookup"><span data-stu-id="d107b-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-238">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-239">Platné</span><span class="sxs-lookup"><span data-stu-id="d107b-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="d107b-240">Čas a poplatky za projekt P1 sú zahrnuté v QL1.</span><span class="sxs-lookup"><span data-stu-id="d107b-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="d107b-241">Výdavky na projekt P1 sú zahrnuté v QL2.</span><span class="sxs-lookup"><span data-stu-id="d107b-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="d107b-242">Položky v jednotlivých riadkoch cenovej ponuky sa neprekrývajú a je platný.</span><span class="sxs-lookup"><span data-stu-id="d107b-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-243">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-244">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-245">QL2</span><span class="sxs-lookup"><span data-stu-id="d107b-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-246">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-247">Prázdna</span><span class="sxs-lookup"><span data-stu-id="d107b-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-248">No</span><span class="sxs-lookup"><span data-stu-id="d107b-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-249">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-250">No</span><span class="sxs-lookup"><span data-stu-id="d107b-250">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-251">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-252">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-253">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-254">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-255">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="d107b-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-256">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-257">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-258">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-259">Neplatný</span><span class="sxs-lookup"><span data-stu-id="d107b-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-260">Porušenie pravidla č. 2 vyššie</span><span class="sxs-lookup"><span data-stu-id="d107b-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="d107b-261">Q1 zahŕňa čas, výdavky a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="d107b-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d107b-262">QL2 zahŕňa čas, výdavky a poplatky za celý projekt P1 a prekrýva sa s tým, čo je zahrnuté v Q1.</span><span class="sxs-lookup"><span data-stu-id="d107b-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-263">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-264">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-265">QL2</span><span class="sxs-lookup"><span data-stu-id="d107b-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-266">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-267">Prázdna</span><span class="sxs-lookup"><span data-stu-id="d107b-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-268">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-269">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-270">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-270">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-271">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-272">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-273">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-274">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-275">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="d107b-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-276">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-277">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-278">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-279">Platné</span><span class="sxs-lookup"><span data-stu-id="d107b-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-280">Podľa pravidla č. 3 vyššie,</span><span class="sxs-lookup"><span data-stu-id="d107b-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="d107b-281">Q1 zahŕňa čas, výdavky a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="d107b-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d107b-282">QL2 zahŕňa čas, výdavky a poplatky pre podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="d107b-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="d107b-283">Jediná ďalšia validácia je okolo podmnožiny úloh na QL1, ktorá sa líši od podmnožiny úloh na QL2.</span><span class="sxs-lookup"><span data-stu-id="d107b-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="d107b-284">To zaručuje, že nedôjde k žiadnemu prekrytiu.</span><span class="sxs-lookup"><span data-stu-id="d107b-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="d107b-285">Vykonáva sa prostredníctvom systému, keď sú priradené úlohy.</span><span class="sxs-lookup"><span data-stu-id="d107b-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-286">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-287">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-288">QL2</span><span class="sxs-lookup"><span data-stu-id="d107b-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-289">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-290">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="d107b-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-291">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-292">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-293">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-293">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-294">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-295">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-296">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-297">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-298">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="d107b-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-299">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-300">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-301">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d107b-302">Platné</span><span class="sxs-lookup"><span data-stu-id="d107b-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-303">Na základe pravidla č. 5 sú Q1 a Q2 dve cenové ponuky pri tej istej príležitosti, takže obidve môžu odhadnúť rovnaké komponenty projektu.</span><span class="sxs-lookup"><span data-stu-id="d107b-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-304">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-305">Š2</span><span class="sxs-lookup"><span data-stu-id="d107b-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-306">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-307">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-308">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="d107b-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-309">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-310">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-311">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-311">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-312">O1</span><span class="sxs-lookup"><span data-stu-id="d107b-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-313">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-314">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-315">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-316">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="d107b-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-317">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-318">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-319">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d107b-320">Platné</span><span class="sxs-lookup"><span data-stu-id="d107b-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="d107b-321">Na základe pravidla č. 4 sú Q1 a Q2 dve cenové ponuky pri rôznych príležitostiach, takže nemôžu odhadnúť rovnaké komponenty v tom istom projekte.</span><span class="sxs-lookup"><span data-stu-id="d107b-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="d107b-322">O2</span><span class="sxs-lookup"><span data-stu-id="d107b-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="d107b-323">Q1</span><span class="sxs-lookup"><span data-stu-id="d107b-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-324">QL1</span><span class="sxs-lookup"><span data-stu-id="d107b-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-325">P1</span><span class="sxs-lookup"><span data-stu-id="d107b-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="d107b-326">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="d107b-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-327">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="d107b-328">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="d107b-329">Áno</span><span class="sxs-lookup"><span data-stu-id="d107b-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="d107b-330">Neplatný</span><span class="sxs-lookup"><span data-stu-id="d107b-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

