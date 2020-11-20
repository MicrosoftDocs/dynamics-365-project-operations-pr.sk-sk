---
title: Prehľad riadkov cenových ponúk založených na projekte – čiastočné
description: Táto téma poskytuje informácie o používaní riadkov cenových ponúk založených na projekte pre projektovú úlohu. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: be1663c0d226fa19fe4b9df566e16d215f1fc08e
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181111"
---
# <a name="project-based-quote-lines-overview---lite"></a><span data-ttu-id="1dd1f-104">Prehľad riadkov cenových ponúk založených na projekte – čiastočné</span><span class="sxs-lookup"><span data-stu-id="1dd1f-104">Project-based quote lines overview - lite</span></span>

<span data-ttu-id="1dd1f-105">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="1dd1f-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1dd1f-106">Riadky cenových ponúk založených na projekte sú navrhnuté tak, aby pomohli odhadnúť projektovú úlohu na zákazke.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="1dd1f-107">Štruktúra riadku cenovej ponuky založenej na projekte sa pre odhady projektu rozširuje o tieto koncepty:</span><span class="sxs-lookup"><span data-stu-id="1dd1f-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="1dd1f-108">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="1dd1f-108">Billing Method</span></span>
- <span data-ttu-id="1dd1f-109">Mapovanie projektov a úloh</span><span class="sxs-lookup"><span data-stu-id="1dd1f-109">Project and Task Mapping</span></span>
- <span data-ttu-id="1dd1f-110">Zahrnuté triedy transakcií</span><span class="sxs-lookup"><span data-stu-id="1dd1f-110">Included Transaction classes</span></span>
- <span data-ttu-id="1dd1f-111">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="1dd1f-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="1dd1f-112">Nastavenie účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="1dd1f-112">Chargeability setup</span></span>
- <span data-ttu-id="1dd1f-113">Odhad pomocou podrobností o riadku cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="1dd1f-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="1dd1f-114">Zákazníci v riadkoch cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="1dd1f-114">Quote line Customers</span></span>

<span data-ttu-id="1dd1f-115">Nasledujúca tabuľka poskytuje informácie o poliach na karte **Všeobecné** v riadku cenovej ponuky na základe projektu.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="1dd1f-116">Tieto polia pomáhajú vytvoriť základ pre podrobný a prízemných odhad projektovej úlohy.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="1dd1f-117">**Pole**</span><span class="sxs-lookup"><span data-stu-id="1dd1f-117">**Field**</span></span> | <span data-ttu-id="1dd1f-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="1dd1f-118">**Description**</span></span> | <span data-ttu-id="1dd1f-119">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="1dd1f-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="1dd1f-120">Meno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-120">Name</span></span> | <span data-ttu-id="1dd1f-121">Názov riadka cenovej ponuky, ktorý by vám mal pomôcť identifikovať diskrétnu zložku cenovej ponuky, ktorá sa odhaduje.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="1dd1f-122">Skopírované do riadku zmluvy o projekte, ktorý je vytvorený z tohto riadku cenovej ponuky po získaní ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-123">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="1dd1f-123">Billing Method</span></span> | <span data-ttu-id="1dd1f-124">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z príslušného poľa na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="1dd1f-125">Toto pole obsahuje dva hlavné zmluvné modely, ktoré podporuje Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="1dd1f-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="1dd1f-126">- Pevná cena</span><span class="sxs-lookup"><span data-stu-id="1dd1f-126">- Fixed price</span></span></br><span data-ttu-id="1dd1f-127">- Čas a materiál.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-127">- Time and material.</span></span>| <span data-ttu-id="1dd1f-128">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-129">Project</span><span class="sxs-lookup"><span data-stu-id="1dd1f-129">Project</span></span> | <span data-ttu-id="1dd1f-130">Toto voliteľné pole použite na identifikáciu projektu, ktorý sa použije na vykonanie práce na tejto zákazke.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="1dd1f-131">Keď je projekt mapovaný na riadok cenovej ponuky, pomáha to pri nastavovaní účtovateľných úloh a tiež pri uvádzaní odhadu založeného na projekte k riadku cenovej ponuky ako podrobnosti o riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="1dd1f-132">Ak projekt nie je mapovaný na riadok cenovej ponuky založenej na projekte, odhad by sa mal vytvoriť manuálne vytvorením podrobností o každom riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="1dd1f-133">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="1dd1f-134">Zahrnuté úlohy</span><span class="sxs-lookup"><span data-stu-id="1dd1f-134">Included Tasks</span></span> | <span data-ttu-id="1dd1f-135">Označuje, či sa tento riadok cenovej ponuky používa pre všetky alebo niektoré projektové úlohy vybratého projektu.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="1dd1f-136">Toto pole má nasledujúce možné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="1dd1f-136">This field has the following possible values:</span></span></br><span data-ttu-id="1dd1f-137">- Všetky projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="1dd1f-137">- All project tasks</span></span></br><span data-ttu-id="1dd1f-138">- Iba vybraté projektové úlohy</span><span class="sxs-lookup"><span data-stu-id="1dd1f-138">- Selected project tasks only</span></span></br><span data-ttu-id="1dd1f-139">Prázdna hodnota v tomto poli je ekvivalentná s možnosťou **Všetky projektové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="1dd1f-140">Ak je na stránke projektu vybraná možnosť **Iba vybrané projektové úlohy**, tak vám karta **Nastavenie fakturácie úloh** umožňuje vybrať konkrétne úlohy a priradiť ich k tomuto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="1dd1f-141">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-142">Zahrnúť čas</span><span class="sxs-lookup"><span data-stu-id="1dd1f-142">Include Time</span></span> | <span data-ttu-id="1dd1f-143">Príznak **Áno**/**Nie** označuje, či budú časové transakcie alebo náklady na prácu na vybranom projekte zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1dd1f-144">Hodnota **Nie** označuje, že časové transakcie alebo náklady na prácu nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1dd1f-145">Hodnota **Áno** označuje, že časové transakcie alebo náklady na prácu budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1dd1f-146">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-147">Zahrnúť výdavok</span><span class="sxs-lookup"><span data-stu-id="1dd1f-147">Include Expense</span></span> | <span data-ttu-id="1dd1f-148">Príznak **Áno**/**Nie** označuje, či budú výdavkové náklady vybraného projektu zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1dd1f-149">Hodnota **Nie** označuje, že výdavkové náklady nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1dd1f-150">Hodnota **Áno** označuje, že výdavkové náklady budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1dd1f-151">Hodnota z tohto poľa sa prekopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-152">Zahrnúť poplatok</span><span class="sxs-lookup"><span data-stu-id="1dd1f-152">Include Fee</span></span> | <span data-ttu-id="1dd1f-153">Príznak **Áno**/**Nie** označuje, či budú poplatky vybraného projektu zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="1dd1f-154">Hodnota **Nie** označuje, že poplatky nebudú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="1dd1f-155">Hodnota **Áno** označuje, že poplatky budú zahrnuté do odhadu v tomto riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="1dd1f-156">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-157">Čiastka ponuky</span><span class="sxs-lookup"><span data-stu-id="1dd1f-157">Quoted Amount</span></span> | <span data-ttu-id="1dd1f-158">Toto je suma, ktorá bude zákazníkovi ponúknutá za všetku prácu predpokladanú v tomto riadku cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="1dd1f-159">Pri cenovej ponuke vytvorenej z príležitosti sa táto hodnota skopíruje z poľa **Rozpočet zákazníka** na riadka príležitosti.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="1dd1f-160">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="1dd1f-161">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-162">Odhad dane</span><span class="sxs-lookup"><span data-stu-id="1dd1f-162">Estimated Tax</span></span> | <span data-ttu-id="1dd1f-163">Toto je upraviteľné pole, kde môže používateľ pridať odhadovanú sumu dane pre riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="1dd1f-164">Ak riadok cenovej ponuky založený na projekte obsahuje podrobnosti o riadku, toto pole je uzamknuté pre úpravy a je zhrnuté z čiastky daní v podrobnostiach riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="1dd1f-165">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-166">Čiastka ponuky po zdanení</span><span class="sxs-lookup"><span data-stu-id="1dd1f-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="1dd1f-167">Toto pole predstavuje čiastku riadka cenovej ponuky po zdanení a je iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="1dd1f-168">Čiastka v tomto poli sa počíta ako *Ponúknutá čiastka + daň*.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="1dd1f-169">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-170">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="1dd1f-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="1dd1f-171">Toto pole je upraviteľné a je k dispozícii iba pre riadky ponúk založené na projekte, ktoré majú spôsob účtovania **Čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="1dd1f-172">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="1dd1f-173">Rozpočet zákazníka</span><span class="sxs-lookup"><span data-stu-id="1dd1f-173">Customer Budget</span></span> | <span data-ttu-id="1dd1f-174">Toto pole je upraviteľné a skopíruje sa z príslušného poľa v riadku príležitosti, ak bola cenová ponuka vytvorená z príležitosti.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="1dd1f-175">Hodnota z tohto poľa sa skopíruje do riadka zmluvy o projekte, ktorý je vytvorený z tohto riadka cenovej ponuky po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="1dd1f-176">Pravidlá overenia pre polia na karte Všeobecné v riadkoch cenových ponúk založených na projekte</span><span class="sxs-lookup"><span data-stu-id="1dd1f-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="1dd1f-177">**Pravidlo 1**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt je zahrnutý v riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="1dd1f-178">**Pravidlo 2**: Ak je pole **Zahrnuté úlohy** prázdne alebo ak je nastavené na **Všetky projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť iba do jedného riadka cenovej ponuky založenej na projekte cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="1dd1f-179">**Pravidlo 3**: Ak je pole **Zahrnuté úlohy** nastavené na **Iba vybrané projektové úlohy**, projekt a určitú triedu transakcií je možné zahrnúť do viacerých riadkov cenovej ponuky založenej na projekte cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="1dd1f-180">**Pravidlo 4**: Ak má príležitosť viacero cenových ponúk, môžu existovať riadky cenových ponúk z rôznych cenových ponúk, ktoré všetky odkazujú na ten istý projekt a zahŕňajú rovnakú triedu transakcií.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="1dd1f-181">**Pravidlo 5**: Ak cenové ponuky nepatria do rovnakej príležitosti, nemôžu obsahovať rovnakú triedu projektu a transakcie.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="1dd1f-182">
                    <strong>Príležitosť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="1dd1f-183">
                    <strong>Ponuka</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1dd1f-184">
                    <strong>Riadok cenovej ponuky</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1dd1f-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="1dd1f-186">
                    <strong>Zahrnuté úlohy</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1dd1f-187">
                    <strong>Zahrnúť čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="1dd1f-188">
                    <strong>Zahrnúť výdavok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="1dd1f-189">
                    <strong>Zahrnúť</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="1dd1f-190">
                    <strong>Poplatok</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="1dd1f-191">
                    <strong>Platný/neplatný</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="1dd1f-192">
                    <strong>Dôvod</strong>
                </span><span class="sxs-lookup"><span data-stu-id="1dd1f-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-193">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-194">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-195">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-196">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-197">Prázdna</span><span class="sxs-lookup"><span data-stu-id="1dd1f-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-198">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-199">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-200">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-201">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1dd1f-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-202">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-202">Violation of Rule #2.</span></span> <span data-ttu-id="1dd1f-203">Čas, náklady a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-204">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-205">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-206">QL2</span><span class="sxs-lookup"><span data-stu-id="1dd1f-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-207">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-208">Prázdna</span><span class="sxs-lookup"><span data-stu-id="1dd1f-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-209">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-210">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-211">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-211">Yes</span></span> </p>
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
<span data-ttu-id="1dd1f-212">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-213">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-214">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-215">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-216">Prázdna</span><span class="sxs-lookup"><span data-stu-id="1dd1f-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-217">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-218">No</span><span class="sxs-lookup"><span data-stu-id="1dd1f-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-219">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-220">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1dd1f-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-221">Porušenie pravidla č. 2.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-221">Violation of Rule #2.</span></span> <span data-ttu-id="1dd1f-222">Čas a poplatky za projekt P1 sú zahrnuté v riadkoch cenových ponúk QL1 a QL2.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-223">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-224">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-225">QL2</span><span class="sxs-lookup"><span data-stu-id="1dd1f-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-226">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-227">Prázdna</span><span class="sxs-lookup"><span data-stu-id="1dd1f-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-228">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-229">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-230">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-230">Yes</span></span> </p>
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
<span data-ttu-id="1dd1f-231">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-232">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-233">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-234">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-235">Prázdna</span><span class="sxs-lookup"><span data-stu-id="1dd1f-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-236">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-237">No</span><span class="sxs-lookup"><span data-stu-id="1dd1f-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-238">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-239">Platné</span><span class="sxs-lookup"><span data-stu-id="1dd1f-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="1dd1f-240">Čas a poplatky za projekt P1 sú zahrnuté v QL1.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="1dd1f-241">Výdavky na projekt P1 sú zahrnuté v QL2.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="1dd1f-242">Položky v jednotlivých riadkoch cenovej ponuky sa neprekrývajú a je platný.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-243">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-244">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-245">QL2</span><span class="sxs-lookup"><span data-stu-id="1dd1f-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-246">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-247">Prázdna</span><span class="sxs-lookup"><span data-stu-id="1dd1f-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-248">No</span><span class="sxs-lookup"><span data-stu-id="1dd1f-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-249">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-250">No</span><span class="sxs-lookup"><span data-stu-id="1dd1f-250">No</span></span> </p>
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
<span data-ttu-id="1dd1f-251">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-252">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-253">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-254">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-255">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="1dd1f-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-256">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-257">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-258">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-259">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1dd1f-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-260">Porušenie pravidla č. 2 vyššie</span><span class="sxs-lookup"><span data-stu-id="1dd1f-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="1dd1f-261">Q1 zahŕňa čas, výdavky a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1dd1f-262">QL2 zahŕňa čas, výdavky a poplatky za celý projekt P1 a prekrýva sa s tým, čo je zahrnuté v Q1.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-263">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-264">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-265">QL2</span><span class="sxs-lookup"><span data-stu-id="1dd1f-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-266">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-267">Prázdna</span><span class="sxs-lookup"><span data-stu-id="1dd1f-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-268">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-269">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-270">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-270">Yes</span></span> </p>
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
<span data-ttu-id="1dd1f-271">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-272">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-273">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-274">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-275">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="1dd1f-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-276">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-277">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-278">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-279">Platné</span><span class="sxs-lookup"><span data-stu-id="1dd1f-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-280">Podľa pravidla č. 3 vyššie,</span><span class="sxs-lookup"><span data-stu-id="1dd1f-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="1dd1f-281">Q1 zahŕňa čas, výdavky a poplatky za podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1dd1f-282">QL2 zahŕňa čas, výdavky a poplatky pre podmnožinu úloh v projekte P1.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="1dd1f-283">Jediná ďalšia validácia je okolo podmnožiny úloh na QL1, ktorá sa líši od podmnožiny úloh na QL2.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="1dd1f-284">To zaručuje, že nedôjde k žiadnemu prekrytiu.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="1dd1f-285">Vykonáva sa prostredníctvom systému, keď sú priradené úlohy.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-286">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-287">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-288">QL2</span><span class="sxs-lookup"><span data-stu-id="1dd1f-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-289">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-290">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="1dd1f-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-291">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-292">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-293">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-293">Yes</span></span> </p>
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
<span data-ttu-id="1dd1f-294">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-295">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-296">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-297">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-298">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="1dd1f-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-299">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-300">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-301">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1dd1f-302">Platné</span><span class="sxs-lookup"><span data-stu-id="1dd1f-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-303">Na základe pravidla č. 5 sú Q1 a Q2 dve cenové ponuky pri tej istej príležitosti, takže obidve môžu odhadnúť rovnaké komponenty projektu.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-304">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-305">Š2</span><span class="sxs-lookup"><span data-stu-id="1dd1f-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-306">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-307">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-308">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="1dd1f-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-309">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-310">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-311">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-311">Yes</span></span> </p>
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
<span data-ttu-id="1dd1f-312">O1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-313">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-314">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-315">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-316">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="1dd1f-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-317">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-318">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-319">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1dd1f-320">Platné</span><span class="sxs-lookup"><span data-stu-id="1dd1f-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="1dd1f-321">Na základe pravidla č. 4 sú Q1 a Q2 dve cenové ponuky pri rôznych príležitostiach, takže nemôžu odhadnúť rovnaké komponenty v tom istom projekte.</span><span class="sxs-lookup"><span data-stu-id="1dd1f-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="1dd1f-322">O2</span><span class="sxs-lookup"><span data-stu-id="1dd1f-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="1dd1f-323">Q1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-324">QL1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-325">P1</span><span class="sxs-lookup"><span data-stu-id="1dd1f-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="1dd1f-326">Všetky projektové alebo prázdne</span><span class="sxs-lookup"><span data-stu-id="1dd1f-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-327">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="1dd1f-328">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="1dd1f-329">Áno</span><span class="sxs-lookup"><span data-stu-id="1dd1f-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="1dd1f-330">Neplatný</span><span class="sxs-lookup"><span data-stu-id="1dd1f-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

