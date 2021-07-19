---
title: Prehľad riadkov projektovej cenovej ponuky
description: Táto téma poskytuje informácie o tom, používať riadky projektovej cenovej ponuky pre prácu na projekte.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: c585bbc55119e678a4f75f5dfe8966a436db1a34
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368090"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="e3b1d-103">Prehľad riadkov projektovej cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="e3b1d-103">Project quote lines overview</span></span>

<span data-ttu-id="e3b1d-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="e3b1d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e3b1d-105">Riadky cenových ponúk založených na projekte sú navrhnuté tak, aby pomohli odhadnúť projektovú úlohu na zákazke.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="e3b1d-106">Štruktúra riadku cenovej ponuky založenej na projekte sa pre odhady projektu rozširuje o tieto koncepty:</span><span class="sxs-lookup"><span data-stu-id="e3b1d-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="e3b1d-107">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="e3b1d-107">Billing Method</span></span>
- <span data-ttu-id="e3b1d-108">Mapovanie projektu</span><span class="sxs-lookup"><span data-stu-id="e3b1d-108">Project Mapping</span></span>
- <span data-ttu-id="e3b1d-109">Zahrnuté triedy transakcií</span><span class="sxs-lookup"><span data-stu-id="e3b1d-109">Included Transaction classes</span></span>
- <span data-ttu-id="e3b1d-110">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="e3b1d-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="e3b1d-111">Nastavenie účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="e3b1d-111">Chargeability setup</span></span>
- <span data-ttu-id="e3b1d-112">Odhad pomocou podrobností o riadku cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="e3b1d-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="e3b1d-113">Zákazníci v riadkoch cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="e3b1d-113">Quote line Customers</span></span>

<span data-ttu-id="e3b1d-114">Nasledujúca tabuľka poskytuje informácie o poliach na karte **Všeobecné** v riadku cenovej ponuky na základe projektu.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="e3b1d-115">Tieto polia pomáhajú vytvoriť základ pre podrobný a prízemných odhad projektovej úlohy.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="e3b1d-116">**Pole**</span><span class="sxs-lookup"><span data-stu-id="e3b1d-116">**Field**</span></span> | <span data-ttu-id="e3b1d-117">**Opis**</span><span class="sxs-lookup"><span data-stu-id="e3b1d-117">**Description**</span></span> | <span data-ttu-id="e3b1d-118">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="e3b1d-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="e3b1d-119">Meno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-119">Name</span></span> | <span data-ttu-id="e3b1d-120">Názov riadka cenovej ponuky, ktorý by vám mal pomôcť identifikovať diskrétnu zložku cenovej ponuky, ktorá sa odhaduje.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="e3b1d-121">Skopírované do riadku zmluvy o projekte, ktorý je vytvorený z tohto riadku cenovej ponuky po získaní ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-122">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="e3b1d-122">Billing Method</span></span> | <span data-ttu-id="e3b1d-123">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z príslušného poľa na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="e3b1d-124">Toto pole obsahuje dva hlavné modely uzatvárania zmlúv podporované v aplikácii Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="e3b1d-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="e3b1d-125">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="e3b1d-125">- Fixed price</span></span></br><span data-ttu-id="e3b1d-126">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-126">- Time and material.</span></span>| <span data-ttu-id="e3b1d-127">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-128">Project</span><span class="sxs-lookup"><span data-stu-id="e3b1d-128">Project</span></span> | <span data-ttu-id="e3b1d-129">Toto voliteľné pole použite na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="e3b1d-130">Keď je projekt mapovaný na riadok cenovej ponuky, pomáha to pri nastavovaní účtovateľných úloh a tiež pri uvádzaní odhadu založeného na projekte k riadku cenovej ponuky ako podrobnosti o riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="e3b1d-131">Ak projekt nie je mapovaný na riadok cenovej ponuky založenej na projekte, odhad by sa mal vytvoriť manuálne vytvorením podrobností o každom riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="e3b1d-132">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-133">Zahrnúť čas</span><span class="sxs-lookup"><span data-stu-id="e3b1d-133">Include Time</span></span> | <span data-ttu-id="e3b1d-134">Príznak **Áno**/**Nie** označuje, či budú časové transakcie alebo náklady na prácu na vybranom projekte zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e3b1d-135">Hodnota **Nie** označuje, že časové transakcie alebo náklady na prácu nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e3b1d-136">Hodnota **Áno** označuje, že časové transakcie alebo náklady na prácu budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e3b1d-137">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-138">Zahrnúť výdavok</span><span class="sxs-lookup"><span data-stu-id="e3b1d-138">Include Expense</span></span> | <span data-ttu-id="e3b1d-139">Príznak **Áno**/**Nie** označuje, či budú výdavkové náklady vybraného projektu zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e3b1d-140">Hodnota **Nie** označuje, že výdavkové náklady nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e3b1d-141">Hodnota **Áno** označuje, že výdavkové náklady budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e3b1d-142">Hodnota z tohto poľa sa prekopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-143">Zahrnúť poplatok</span><span class="sxs-lookup"><span data-stu-id="e3b1d-143">Include Fee</span></span> | <span data-ttu-id="e3b1d-144">Príznak **Áno**/**Nie** označuje, či budú poplatky vybraného projektu zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="e3b1d-145">Hodnota **Nie** označuje, že poplatky nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="e3b1d-146">Hodnota **Áno** označuje, že poplatky budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="e3b1d-147">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-148">Čiastka ponuky</span><span class="sxs-lookup"><span data-stu-id="e3b1d-148">Quoted Amount</span></span> | <span data-ttu-id="e3b1d-149">Toto je suma, ktorá bude zákazníkovi ponúknutá za všetku prácu predpokladanú v tomto riadku cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="e3b1d-150">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z poľa **Rozpočet zákazníka** na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="e3b1d-151">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="e3b1d-152">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-153">Odhad dane</span><span class="sxs-lookup"><span data-stu-id="e3b1d-153">Estimated Tax</span></span> | <span data-ttu-id="e3b1d-154">Toto je upraviteľné pole, kde môže používateľ pridať odhadovanú sumu dane pre riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="e3b1d-155">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky daní v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="e3b1d-156">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-157">Čiastka ponuky po zdanení</span><span class="sxs-lookup"><span data-stu-id="e3b1d-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="e3b1d-158">Toto pole predstavuje čiastku riadka cenovej ponuky po zdanení a je iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="e3b1d-159">Čiastka v tomto poli sa počíta ako *Ponúknutá čiastka + daň*.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="e3b1d-160">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-161">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="e3b1d-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="e3b1d-162">Toto pole je upraviteľné a je k dispozícii iba pre riadky ponúk založené na projekte, ktoré majú spôsob účtovania **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="e3b1d-163">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="e3b1d-164">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="e3b1d-164">Customer Budget</span></span> | <span data-ttu-id="e3b1d-165">Toto pole je upraviteľné a skopíruje sa z príslušného poľa v riadku príležitosti, ak bola cenová ponuka vytvorená z príležitosti.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="e3b1d-166">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="e3b1d-167">Pravidlá overenia pre polia na karte Všeobecné v riadkoch cenových ponúk založených na projekte</span><span class="sxs-lookup"><span data-stu-id="e3b1d-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="e3b1d-168">**Pravidlo 1**: Určitú triedu transakcií vo vybratom projekte je možné zahrnúť iba do jedného riadka cenovej ponuky založenej na projekte cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="e3b1d-169">**Pravidlo 2**: Ak má príležitosť viacero cenových ponúk, môžu existovať riadky cenových ponúk z rôznych cenových ponúk, ktoré všetky odkazujú na ten istý projekt a zahŕňajú rovnakú triedu transakcií.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="e3b1d-170">**Pravidlo 3**: Ak cenové ponuky nepatria do rovnakej príležitosti, nemôžu obsahovať rovnakú triedu projektu a transakcie.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="e3b1d-171">
                    <strong>Príležitosť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="e3b1d-172">
                    <strong>Ponuka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e3b1d-173">
                    <strong>Riadok cenovej ponuky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e3b1d-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e3b1d-175">
                    <strong>Zahrnúť čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="e3b1d-176">
                    <strong>Zahrnúť výdavok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="e3b1d-177">
                    <strong>Zahrnúť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="e3b1d-178">
                    <strong>Poplatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="e3b1d-179">
                    <strong>Platný/neplatný</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="e3b1d-180">
                    <strong>Dôvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e3b1d-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e3b1d-181">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-182">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-183">QL1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-184">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-185">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-186">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-187">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-188">Neplatný</span><span class="sxs-lookup"><span data-stu-id="e3b1d-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-189">Porušenie pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-189">Violation of Rule #1.</span></span> <span data-ttu-id="e3b1d-190">Čas, náklady a poplatky za projekt P1 sú zahrnuté v oboch riadkoch cenových ponúk, QL1 a QL2.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e3b1d-191">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-192">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-193">QL2</span><span class="sxs-lookup"><span data-stu-id="e3b1d-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-194">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-195">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-196">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-197">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-197">Yes</span></span> </p>
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
<span data-ttu-id="e3b1d-198">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-199">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-200">QL1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-201">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-202">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-203">No</span><span class="sxs-lookup"><span data-stu-id="e3b1d-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-204">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-205">Neplatný</span><span class="sxs-lookup"><span data-stu-id="e3b1d-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-206">Porušenie pravidla č. 1.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-206">Violation of Rule #1.</span></span> <span data-ttu-id="e3b1d-207">Čas a poplatky za projekt P1 sú zahrnuté v oboch riadkoch cenových ponúk, QL1 a QL2.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e3b1d-208">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-209">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-210">QL2</span><span class="sxs-lookup"><span data-stu-id="e3b1d-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-211">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-212">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-213">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-214">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-214">Yes</span></span> </p>
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
<span data-ttu-id="e3b1d-215">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-216">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-217">QL1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-218">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-219">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-220">No</span><span class="sxs-lookup"><span data-stu-id="e3b1d-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-221">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-222">Platné</span><span class="sxs-lookup"><span data-stu-id="e3b1d-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="e3b1d-223">Čas a poplatky za projekt P1 sú zahrnuté v QL1.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="e3b1d-224">Výdavky na projekt P1 sú zahrnuté v QL2.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="e3b1d-225">Položky v jednotlivých riadkoch cenovej ponuky sa neprekrývajú, takže je platný.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e3b1d-226">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-227">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-228">QL2</span><span class="sxs-lookup"><span data-stu-id="e3b1d-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-229">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-230">No</span><span class="sxs-lookup"><span data-stu-id="e3b1d-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-231">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-232">No</span><span class="sxs-lookup"><span data-stu-id="e3b1d-232">No</span></span> </p>
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
<span data-ttu-id="e3b1d-233">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-234">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-235">QL1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-236">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-237">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-238">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-239">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-240">Neplatný</span><span class="sxs-lookup"><span data-stu-id="e3b1d-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-241">Porušenie pravidla č. 1 vyššie</span><span class="sxs-lookup"><span data-stu-id="e3b1d-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="e3b1d-242">Q1 zahŕňa čas, výdavky a poplatky za celý projekt P1.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="e3b1d-243">QL2 zahŕňa čas, výdavky a poplatky za celý projekt P1 a prekrýva sa s tým, čo je zahrnuté v Q1.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e3b1d-244">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-245">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-246">QL2</span><span class="sxs-lookup"><span data-stu-id="e3b1d-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-247">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-248">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-249">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-250">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-250">Yes</span></span> </p>
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
<span data-ttu-id="e3b1d-251">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-252">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-253">QL1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-254">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-255">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-256">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-257">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e3b1d-258">Platné</span><span class="sxs-lookup"><span data-stu-id="e3b1d-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-259">Na základe pravidla č. 2 sú Q1 a Q2 dve cenové ponuky pri tej istej príležitosti, takže obidve môžu odhadnúť rovnaké komponenty projektu.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e3b1d-260">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-261">Š2</span><span class="sxs-lookup"><span data-stu-id="e3b1d-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-262">QL1 na Q2</span><span class="sxs-lookup"><span data-stu-id="e3b1d-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-263">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-264">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-265">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-266">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-266">Yes</span></span> </p>
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
<span data-ttu-id="e3b1d-267">O1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-268">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-269">QL1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-270">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-271">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-272">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-273">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e3b1d-274">Platné</span><span class="sxs-lookup"><span data-stu-id="e3b1d-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="e3b1d-275">Na základe pravidla č. 3 sú Q1 a Q2 dve cenové ponuky pri rôznych príležitostiach, takže nemôžu odhadnúť rovnaké komponenty v tom istom projekte.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="e3b1d-276">O2</span><span class="sxs-lookup"><span data-stu-id="e3b1d-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="e3b1d-277">Q1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-278">QL1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-279">P1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-280">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="e3b1d-281">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="e3b1d-282">Áno</span><span class="sxs-lookup"><span data-stu-id="e3b1d-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="e3b1d-283">Neplatný</span><span class="sxs-lookup"><span data-stu-id="e3b1d-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
