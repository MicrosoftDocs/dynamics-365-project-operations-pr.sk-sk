---
title: Opravné projektové faktúry
description: Táto téma poskytuje informácie o tom, ako vytvárať a potvrdzovať opravné faktúry v Project Operations.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dfa5535597ee6e144259c9246b33075f3492285e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004100"
---
# <a name="corrective-project-invoices"></a><span data-ttu-id="48d9e-103">Opravné projektové faktúry</span><span class="sxs-lookup"><span data-stu-id="48d9e-103">Corrective project invoices</span></span>

<span data-ttu-id="48d9e-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="48d9e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="48d9e-105">Potvrdenú projektovú faktúru je možné podľa dohody so zákazníkom a projektovým manažérom opraviť tak, že sa spracujú zmeny alebo pripíšu kredity.</span><span class="sxs-lookup"><span data-stu-id="48d9e-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="48d9e-106">Ak chcete vykonať úpravy potvrdenej faktúry, otvorte potvrdenú faktúru a vyberte **Opraviť túto faktúru**.</span><span class="sxs-lookup"><span data-stu-id="48d9e-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="48d9e-107">Tento výber nie je k dispozícii, pokiaľ nie je potvrdená projektová faktúra.</span><span class="sxs-lookup"><span data-stu-id="48d9e-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="48d9e-108">Z potvrdenej faktúry sa vytvorí nový koncept faktúry.</span><span class="sxs-lookup"><span data-stu-id="48d9e-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="48d9e-109">Všetky podrobnosti o riadku faktúry z predtým potvrdenej faktúry sa skopírujú do nového konceptu.</span><span class="sxs-lookup"><span data-stu-id="48d9e-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="48d9e-110">Ďalej sú uvedené niektoré kľúčové body pre podrobnosti o riadkoch v novej opravenej faktúre, ktorým je potrebné porozumieť:</span><span class="sxs-lookup"><span data-stu-id="48d9e-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="48d9e-111">Všetky množstvá sa aktualizujú na nulu.</span><span class="sxs-lookup"><span data-stu-id="48d9e-111">All quantities are updated to zero.</span></span> <span data-ttu-id="48d9e-112">Aplikácia predpokladá, že všetky fakturované položky sú úplne pripísané.</span><span class="sxs-lookup"><span data-stu-id="48d9e-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="48d9e-113">V prípade potreby môžete tieto množstvá manuálne aktualizovať, aby odrážali množstvo, ktoré sa fakturuje, a nie množstvo, ktoré sa pripisuje.</span><span class="sxs-lookup"><span data-stu-id="48d9e-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="48d9e-114">Na základe zadaného množstva aplikácia vypočíta pripísané množstvo.</span><span class="sxs-lookup"><span data-stu-id="48d9e-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="48d9e-115">Táto suma sa odráža v skutočnostiach, ktoré sa vytvárajú pri potvrdení opravenej faktúry.</span><span class="sxs-lookup"><span data-stu-id="48d9e-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="48d9e-116">Ak robíte zmeny v sume dane, musíte zadať správnu sumu dane, a nie sumu dane, ktorá sa pripisuje.</span><span class="sxs-lookup"><span data-stu-id="48d9e-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="48d9e-117">Predtým potvrdené riadky zmlúv založené na produkte sa nekopírujú.</span><span class="sxs-lookup"><span data-stu-id="48d9e-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="48d9e-118">Spracovanie opráv vo projektovej faktúre založenej na produkte nie je podporované.</span><span class="sxs-lookup"><span data-stu-id="48d9e-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="48d9e-119">Opravy medzníkov sa vždy spracúvajú ako úplné kredity.</span><span class="sxs-lookup"><span data-stu-id="48d9e-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="48d9e-120">Ak bola zákazníkovi fakturovaná nesprávna suma, sumy preddavku alebo zálohy je možné opraviť.</span><span class="sxs-lookup"><span data-stu-id="48d9e-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="48d9e-121">Odsúhlasenia preddavkov a záloh je možné opraviť, ak bola použitá nesprávna suma na odsúhlasenie oproti nákladom na predtým potvrdenej faktúre.</span><span class="sxs-lookup"><span data-stu-id="48d9e-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="48d9e-122">Podrobnosti o riadku faktúry, ktoré sú opravami ďalších už fakturovaných nákladov, majú pole **Oprava** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="48d9e-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="48d9e-123">Faktúry, ktoré majú opravené podrobnosti o riadku faktúry, majú pole s názvom **Obsahuje opravy**, ktoré je tiež nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="48d9e-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="48d9e-124">Skutočné hodnoty vytvorené po potvrdení opravnej faktúry</span><span class="sxs-lookup"><span data-stu-id="48d9e-124">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="48d9e-125">V nasledujúcej tabuľke sú uvedené skutočné hodnoty, ktoré sa vytvoria pri potvrdení opravnej faktúry.</span><span class="sxs-lookup"><span data-stu-id="48d9e-125">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="48d9e-126">
                    <strong>Scenár</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48d9e-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="48d9e-127">
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="48d9e-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="48d9e-128">Potvrdenie opravy fakturovaného preddavku alebo zálohy.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="48d9e-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-129">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="48d9e-130">Táto suma je kladná, pretože má zrušiť zápornú hodnotu, ktorá sa vytvorila pri fakturácii preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="48d9e-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-131">Storno skutočnej hodnoty fakturovaného predaja sa vytvorí pre sumu preddavku alebo zálohy na stornovanie pôvodného fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="48d9e-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-132">Nový opravený fakturovaný predaj sa vytvorí pre opravenú sumu v riadku opravenej faktúry založenej na preddavku alebo zálohe.</span><span class="sxs-lookup"><span data-stu-id="48d9e-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-133">Skutočná hodnota nevyfakturovaného predaja so zápornou sumou v opravenom riadku faktúry založenej na preddavku alebo zálohe, ktorý sa má použiť na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="48d9e-134">Potvrdenie o oprave predtým odsúhlaseného preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="48d9e-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-135">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="48d9e-136">Táto suma je kladná a má zrušiť zápornú hodnotu, ktorá sa vytvorila pri predchádzajúcom odsúhlasení.</span><span class="sxs-lookup"><span data-stu-id="48d9e-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-137">Skutočná hodnota stornovaného fakturovaného predaja pre sumu na predchádzajúcej faktúre.</span><span class="sxs-lookup"><span data-stu-id="48d9e-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-138">Nový opravený fakturovaný predaj pre opravenú sumu preddavku, ktorý sa použije v opravenej faktúre.</span><span class="sxs-lookup"><span data-stu-id="48d9e-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-139">Skutočná hodnota nevyfakturovaného predaja so zápornou sumou v opravenom zostávajúcom preddavku alebo zálohe, ktorý sa má použiť na odsúhlasenie v ďalších faktúrach.</span><span class="sxs-lookup"><span data-stu-id="48d9e-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48d9e-140">Fakturácia plného kreditu z predtým fakturovanej časovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-141">Storno vyfakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="48d9e-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-142">Nová skutočná hodnota nefakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="48d9e-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="48d9e-143">Fakturácia čiastočného kreditu pre časovú transakciu.</span><span class="sxs-lookup"><span data-stu-id="48d9e-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-144">Storno vyfakturovaného predaja pre hodiny a vyfakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="48d9e-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-145">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="48d9e-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-146">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce hodiny a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="48d9e-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48d9e-147">Fakturácia plného kreditu z predtým fakturovanej výdavkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-148">Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="48d9e-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-149">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="48d9e-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="48d9e-150">Fakturácia čiastočného kreditu z predtým fakturovanej výdavkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-151">Storno vyfakturovaného predaja pre fakturované množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="48d9e-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-152">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach opraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="48d9e-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-153">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce množstvo a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="48d9e-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48d9e-154">Fakturácia celého kreditu predtým fakturovanej transakcie materiálu.</span><span class="sxs-lookup"><span data-stu-id="48d9e-154">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-155">Fakturované storno predaja pre množstvo a sumu na pôvodnom riadku faktúry s podrobnosťami za materiál.</span><span class="sxs-lookup"><span data-stu-id="48d9e-155">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-156">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu na pôvodnom riadku faktúry s podrobnosťami za materiál.</span><span class="sxs-lookup"><span data-stu-id="48d9e-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="48d9e-157">Fakturácia čiastočného kreditu pri transakcii materiálu.</span><span class="sxs-lookup"><span data-stu-id="48d9e-157">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-158">Fakturované storno predaja pre množstvo a sumu fakturovanú na pôvodnom riadku faktúry s podrobnosťami za materiál.</span><span class="sxs-lookup"><span data-stu-id="48d9e-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-159">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná za množstvo a sumu na upravenom detaile riadku faktúry, jej storno a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="48d9e-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-160">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce množstvo a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="48d9e-160">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48d9e-161">Fakturácia plného kreditu z predtým fakturovanej poplatkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-161">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-162">Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="48d9e-162">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-163">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="48d9e-163">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="48d9e-164">Fakturácia čiastočného kreditu z predtým fakturovanej poplatkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="48d9e-164">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-165">Storno vyfakturovaného predaja pre množstvo a fakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="48d9e-165">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-166">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného opravného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="48d9e-166">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="48d9e-167">Fakturácia plného kreditu z predtým fakturovaného medzníka.</span><span class="sxs-lookup"><span data-stu-id="48d9e-167">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-168">Storno vyfakturovaného predaja pre sumu v riadku s podrobnosťami pôvodnej faktúry pre medzník.</span><span class="sxs-lookup"><span data-stu-id="48d9e-168">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="48d9e-169">Stav faktúry medzníka sa aktualizuje z <b>Bola uverejnená faktúra pre zákazníka</b> na <b>Pripravené na fakturáciu</b>.</span><span class="sxs-lookup"><span data-stu-id="48d9e-169">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="48d9e-170">Fakturácia čiastočného kreditu z predtým fakturovaného medzníka.</span><span class="sxs-lookup"><span data-stu-id="48d9e-170">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-171">Nepodporované</span><span class="sxs-lookup"><span data-stu-id="48d9e-171">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="48d9e-172">Kredity a opravy predtým fakturovaného riadku zmluvy založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="48d9e-172">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="48d9e-173">Nepodporované</span><span class="sxs-lookup"><span data-stu-id="48d9e-173">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
