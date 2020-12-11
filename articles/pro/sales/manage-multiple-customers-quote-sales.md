---
title: Spravovanie viacerých zákazníkov v projektových cenových ponukách – čiastočné
description: Táto téma poskytuje informácie o práci na cenových ponukách s viacerými zákazníkmi, ktorí budú financovať projekt. (Sales)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bdda1a940e733270399d092e543c3982c47174d0
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181659"
---
# <a name="manage-multiple-customers-on-project-quotes---lite"></a><span data-ttu-id="295ce-104">Spravovanie viacerých zákazníkov v projektových cenových ponukách – čiastočné</span><span class="sxs-lookup"><span data-stu-id="295ce-104">Manage multiple customers on project quotes - lite</span></span>

<span data-ttu-id="295ce-105">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="295ce-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="295ce-106">Cenové ponuky projektu podporujú scenár, keď návrh zahŕňa viacerých zákazníkov, ktorí budú financovať obchod.</span><span class="sxs-lookup"><span data-stu-id="295ce-106">Project quotes support the scenario where the proposal involves multiple customers who will fund the deal.</span></span> <span data-ttu-id="295ce-107">Karta **Súhrn** cenovej ponuky obsahuje pole **Potenciálny zákazník**, ktoré identifikuje primárneho zákazníka obchodu.</span><span class="sxs-lookup"><span data-stu-id="295ce-107">The **Summary** tab of the Quote has the **Potential customer** field that identifies the primary customer of the deal.</span></span> <span data-ttu-id="295ce-108">Ďalší zákazníci pre obchod môžu byť nastavení na karte **Zákazníci** cenovej ponuky projektu.</span><span class="sxs-lookup"><span data-stu-id="295ce-108">Other customers for the deal can be set up on the **Customers** tab of the project quote.</span></span>

<span data-ttu-id="295ce-109">Všetky cenové ponuky zákazníkov na karte **Zákazníci** cenovej ponuky projektu budú predvolené ako riadok cenovej ponuky zákazníkov na všetkých **nových** riadkoch cenovej ponuky založenej na projekte vytvorených pre cenovú ponuku.</span><span class="sxs-lookup"><span data-stu-id="295ce-109">All quote customers on the **Customers** tab of the project quote default as quote line customers on any **new** project-based quote lines created for the quote.</span></span> <span data-ttu-id="295ce-110">Žiadne existujúce riadky cenových ponúk založené na projekte nebudú dediť nové zákaznícke záznamy cenových ponúk vytvorené po nich.</span><span class="sxs-lookup"><span data-stu-id="295ce-110">Any existing project-based quote lines will not inherit new quote customer records created after them.</span></span>

<span data-ttu-id="295ce-111">Riadky cenových ponúk založených na produkte sú automaticky spojené s primárnym zákazníkom, ktorý je zároveň zákazníkom v poli **Potenciálny zákazník** na karte **Súhrn** cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-111">Product-based quote lines are automatically associated to the primary customer who is also the customer in the **Potential Customer** field on the **Summary** tab of the quote.</span></span>

<span data-ttu-id="295ce-112">Zákazníci cenových ponúk a zákazníci riadkov cenových ponúk môžu byť pridaní, aktualizovaní alebo vymazaní kedykoľvek pred získaním cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-112">Quote customers and quote line customers can be added, updated, or deleted at any time before the quote is won.</span></span>

## <a name="concept-of-a-primary-customer"></a><span data-ttu-id="295ce-113">Koncept primárneho zákazníka</span><span class="sxs-lookup"><span data-stu-id="295ce-113">Concept of a primary customer</span></span>

<span data-ttu-id="295ce-114">Zákazník, ktorý je na karte Súhrn cenovej ponuky projektu ako potenciálny zákazník je primárnym zákazníkom cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-114">The customer who is on the summary tab of the project quote as the potential customer is the primary customer of the quote.</span></span> <span data-ttu-id="295ce-115">Ak sa pokúsite odstrániť primárneho zákazníka zo zoznamu zákazníkov v cenovej ponuke, uvidíte chybu, že záznam primárneho zákazníka z cenovej ponuky nemožno vymazať.</span><span class="sxs-lookup"><span data-stu-id="295ce-115">When you try to delete the primary customer from customers list on quote, you will see an error that a primary customer record on a quote cannot be deleted.</span></span>

<span data-ttu-id="295ce-116">Primárny zákazník by nemal byť aktualizovaný zo zoznamu zákazníkov v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="295ce-116">The primary customer shouldn't be updated from the customer list on the quote.</span></span> <span data-ttu-id="295ce-117">Primárneho zákazníka však môžete ovplyvniť zmenou potenciálneho zákazníka na karte **Zhrnutie** cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-117">However, you can influence the primary customer by changing the potential customer on the **Summary** tab of the quote.</span></span> <span data-ttu-id="295ce-118">Keď sa toto pole aktualizuje na **Súhrn cenovej ponuky**, novo vybraný potenciálny zákazník je pridaný ako nový zákazník cenovej ponuky s nastaveným príznakom **Primárny**.</span><span class="sxs-lookup"><span data-stu-id="295ce-118">When this field is updated on the **Quote Summary**, the newly selected potential customer is added as a new quote customer with the **Primary** flag set.</span></span> <span data-ttu-id="295ce-119">Starý potenciálny zákazník bude naďalej zákazníkom uvedeným v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="295ce-119">The old potential customer will still be a customer on the quote.</span></span>

## <a name="create-update-or-delete-a-quote-customer-record"></a><span data-ttu-id="295ce-120">Vytvorenie, aktualizovanie alebo odstránenie záznamu zákazníka cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="295ce-120">Create, Update, or Delete a quote customer record</span></span>

<span data-ttu-id="295ce-121">Zákazník cenovej ponuky môže byť vytvorený, aktualizovaný alebo vymazaný na karte **Zákazníci cenovej ponuky** na stránke **Cenová ponuka**.</span><span class="sxs-lookup"><span data-stu-id="295ce-121">A quote customer can be created, updated, or deleted from the **Quote customers** tab on the **Quote** page.</span></span> <span data-ttu-id="295ce-122">Polia uvedené v nasledujúcej tabuľke sa nachádzajú v zázname zákazníka cenovej ponuky v cenovej ponuke projektu.</span><span class="sxs-lookup"><span data-stu-id="295ce-122">The fields listed in the following table are on the quote customer record of a project quote.</span></span>

| <span data-ttu-id="295ce-123">**Pole**</span><span class="sxs-lookup"><span data-stu-id="295ce-123">**Field**</span></span> | <span data-ttu-id="295ce-124">**Miesto**</span><span class="sxs-lookup"><span data-stu-id="295ce-124">**Location**</span></span> | <span data-ttu-id="295ce-125">**Opis**</span><span class="sxs-lookup"><span data-stu-id="295ce-125">**Description**</span></span> | <span data-ttu-id="295ce-126">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="295ce-126">**Downstream impact**</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="295ce-127">Konto</span><span class="sxs-lookup"><span data-stu-id="295ce-127">Account</span></span> | <span data-ttu-id="295ce-128">Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-128">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="295ce-129">Zobrazenie zoznamu všetkých aktívnych účtov.</span><span class="sxs-lookup"><span data-stu-id="295ce-129">Lists all the active accounts.</span></span> <span data-ttu-id="295ce-130">Po vytvorení záznamu je toto pole uzamknuté.</span><span class="sxs-lookup"><span data-stu-id="295ce-130">This field is locked after the record is created.</span></span> <span data-ttu-id="295ce-131">Ak ho chcete aktualizovať, odstráňte záznam a znova ho vytvorte.</span><span class="sxs-lookup"><span data-stu-id="295ce-131">If you want to update it, delete the record, and re-create it.</span></span> <span data-ttu-id="295ce-132">Ak ste zaznamenali akékoľvek skutočné hodnoty alebo ak je záznam cenovej ponuky zákazníka primárnym zákazníkom, budete môcť záznam odstrániť.</span><span class="sxs-lookup"><span data-stu-id="295ce-132">If you have recorded any actuals, or if the quote customer record is a primary customer, you will be allowed to delete the record.</span></span> | <span data-ttu-id="295ce-133">Zákazníci cenových ponúk sa pri vytváraní riadkov cenových ponúk kopírujú ako zákazníci cenových ponúk.</span><span class="sxs-lookup"><span data-stu-id="295ce-133">Quote customers are copied over as quote line customers when a quote line is created.</span></span> <span data-ttu-id="295ce-134">Po získaní cenovej ponuky sa zákazníci cenovej ponuky prekopírujú aj k zákazníkom so zmluvou o projekte.</span><span class="sxs-lookup"><span data-stu-id="295ce-134">Quote customers are also copied over to the project contract customers when a quote is won.</span></span> |
| <span data-ttu-id="295ce-135">Percento rozdelenia fakturácie</span><span class="sxs-lookup"><span data-stu-id="295ce-135">Billing split percent</span></span> | <span data-ttu-id="295ce-136">Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-136">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="295ce-137">Predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripíše tomuto zákazníkovi cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-137">Represent the percentage of each unbilled sales transaction that will be attributed to this quote customer.</span></span> | <span data-ttu-id="295ce-138">Skopírované do nových riadkov cenových ponúk a zmluvných zákazníkov projektu.</span><span class="sxs-lookup"><span data-stu-id="295ce-138">Copied over to new quote lines and to project contract customers.</span></span> |
| <span data-ttu-id="295ce-139">Meno kontaktu platiteľa</span><span class="sxs-lookup"><span data-stu-id="295ce-139">Bill to Contact Name</span></span> | <span data-ttu-id="295ce-140">Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-140">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="295ce-141">Toto je textové pole a malo by sa použiť na identifikáciu kontaktnej osoby pre zákazníka.</span><span class="sxs-lookup"><span data-stu-id="295ce-141">This is a text field and should be used to identify the Invoice contact person for this customer.</span></span> <span data-ttu-id="295ce-142">Sú predvolené zo záznamu súvisiaceho obchodného vzťahu</span><span class="sxs-lookup"><span data-stu-id="295ce-142">These are defaulted from the related account record</span></span> | <span data-ttu-id="295ce-143">Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa Meno kontaktu platiteľa na faktúre, ktorá je generovaná pre tohto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="295ce-143">Copied over to project contract customers when a Quote is won and in turn to the Bill to Contract name field on the Invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="295ce-144">Fakturačné meno</span><span class="sxs-lookup"><span data-stu-id="295ce-144">Bill to Name</span></span> | <span data-ttu-id="295ce-145">Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-145">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="295ce-146">Toto textové pole by sa malo použiť na identifikáciu kontaktnej osoby faktúry pre zákazníka.</span><span class="sxs-lookup"><span data-stu-id="295ce-146">This text field should be used to identify the invoice contact person for this customer.</span></span> | <span data-ttu-id="295ce-147">Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa **Meno kontaktu platiteľa** na faktúre, ktorá je generovaná pre tohto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="295ce-147">Copied to the project contract customers when a quote is won and in turn to the **Bill to Contract Name** field on the invoice that is generated for this customer.</span></span> |
| <span data-ttu-id="295ce-148">Platobné podmienky</span><span class="sxs-lookup"><span data-stu-id="295ce-148">Payment Terms</span></span> | <span data-ttu-id="295ce-149">Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-149">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="295ce-150">Toto je množina možností s hodnotami, ktoré sú predvolené zo záznamu súvisiaceho obchodného vzťahu.</span><span class="sxs-lookup"><span data-stu-id="295ce-150">This is an option set with values that default from the related account record.</span></span> | <span data-ttu-id="295ce-151">Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky a následne do poľa **Meno kontaktu platiteľa** na faktúre, ktorá je generovaná pre tohto zákazníka,</span><span class="sxs-lookup"><span data-stu-id="295ce-151">Copied to the project contract customers when a quote is won and in turn, to the **Bill to Contract Name** field on the invoice that is generated for this customer,</span></span> |
| <span data-ttu-id="295ce-152">Zaokrúhľuje</span><span class="sxs-lookup"><span data-stu-id="295ce-152">Is Rounding</span></span> | <span data-ttu-id="295ce-153">Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-153">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="295ce-154">Označuje, či je tento zákazník predvoleným zákazníkom zaokrúhľovania pre túto dohodu.</span><span class="sxs-lookup"><span data-stu-id="295ce-154">Indicates if this customer is a default rounding customer for this deal.</span></span> | <span data-ttu-id="295ce-155">Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-155">Copied to the project contract customers when a quote is won.</span></span> |
| <span data-ttu-id="295ce-156">Limit, ktorý sa nesmie prekročiť</span><span class="sxs-lookup"><span data-stu-id="295ce-156">Not-to-exceed limit</span></span> | <span data-ttu-id="295ce-157">Upraviteľná mriežka na karte **Zákazníci cenovej ponuky** a vo formulároch **Hlavné** a **Rýchle vytvorenie** pre zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-157">Editable grid on the **Quote Customers** tab and the **Main** and **Quick Create** forms for a quote customer.</span></span> | <span data-ttu-id="295ce-158">Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude fakturovaná tomuto zákazníkovi za túto zákazku</span><span class="sxs-lookup"><span data-stu-id="295ce-158">Indicates if there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for this engagement</span></span> | <span data-ttu-id="295ce-159">Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-159">Copied to the project contract customers when a quote is won.</span></span> |

## <a name="editing-billing-split-percentages"></a><span data-ttu-id="295ce-160">Úprava percenta rozdelenia fakturácie</span><span class="sxs-lookup"><span data-stu-id="295ce-160">Editing billing split percentages</span></span>

<span data-ttu-id="295ce-161">Percentuálne podiely rozdelenia fakturácie môžete upraviť pomocou prostredia na úpravy v mriežke.</span><span class="sxs-lookup"><span data-stu-id="295ce-161">You can edit the billing split percentages by using the in-line grid edit experience.</span></span> <span data-ttu-id="295ce-162">Ak percentá rozdelenia fakturácie nedosiahnu 100 %, dôjde k chybe.</span><span class="sxs-lookup"><span data-stu-id="295ce-162">When the billing split percentages don't total 100%, an error will occur.</span></span> <span data-ttu-id="295ce-163">Po aktualizácii percentuálnych podielov rozdelenia fakturácie chybu obnovte obnovením stránky.</span><span class="sxs-lookup"><span data-stu-id="295ce-163">After you update the billing split percentages, refresh the page to remove the error.</span></span>

<span data-ttu-id="295ce-164">Môžete tiež skúsiť vybrať **Rovnomerne distribuovať** na vedľajšej mriežke zákazníkov cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="295ce-164">You can also try selecting **Evenly Distribute** on the quote customers' subgrid.</span></span> <span data-ttu-id="295ce-165">Táto akcia prideľuje rozdelenie fakturácie všetkým zákazníkom cenových ponúk.</span><span class="sxs-lookup"><span data-stu-id="295ce-165">This action allocates billing splits to all quote customers.</span></span> <span data-ttu-id="295ce-166">Ak existuje nejaký faktor zaokrúhľovania, pridá sa k zákazníkovi zaokrúhľovania.</span><span class="sxs-lookup"><span data-stu-id="295ce-166">If there is any rounding factor, that will be added to the rounding customer.</span></span> <span data-ttu-id="295ce-167">Jeden zo zákazníkov cenovej ponuky je vždy označený ako zákazník zaokrúhľovania.</span><span class="sxs-lookup"><span data-stu-id="295ce-167">One of the quote customers is always tagged as the rounding customer.</span></span> <span data-ttu-id="295ce-168">to znamená, že záznam zákazníka cenovej ponuky má nastavený príznak **Zaokrúhľovanie** na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="295ce-168">this means that the quote customer record has the **Rounding** flag set to **Yes**.</span></span> <span data-ttu-id="295ce-169">Spravidla ide o primárneho zákazníka cenovej ponuky, ale túto voľbu je možné zmeniť.</span><span class="sxs-lookup"><span data-stu-id="295ce-169">Typically this is the primary customer of the quote, but that can be changed.</span></span>