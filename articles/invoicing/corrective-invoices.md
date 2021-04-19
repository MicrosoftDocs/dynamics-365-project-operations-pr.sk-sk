---
title: Vytvorenie opravných projektových faktúr
description: Táto téma poskytuje informácie o opravných faktúrach v Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32772d64b3fc77f0af9618edff40e3b295593454
ms.sourcegitcommit: 504c09365bf404c1f1aa9b5034c1e1e5bc9d0d54
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5788896"
---
# <a name="create-corrective-project-based-invoices"></a><span data-ttu-id="04035-103">Vytvorenie opravných projektových faktúr</span><span class="sxs-lookup"><span data-stu-id="04035-103">Create corrective project-based invoices</span></span> 

<span data-ttu-id="04035-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="04035-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="04035-105">Potvrdenú projektovú faktúru je možné podľa dohody so zákazníkom a projektovým manažérom opraviť tak, že sa spracujú zmeny alebo pripíšu kredity.</span><span class="sxs-lookup"><span data-stu-id="04035-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="04035-106">Ak chcete vykonať úpravy potvrdenej faktúry, otvorte potvrdenú faktúru a vyberte **Opraviť túto faktúru**.</span><span class="sxs-lookup"><span data-stu-id="04035-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="04035-107">Tento výber nie je k dispozícii, pokiaľ nie je potvrdená projektová faktúra.</span><span class="sxs-lookup"><span data-stu-id="04035-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="04035-108">Z potvrdenej faktúry sa vytvorí nový koncept faktúry.</span><span class="sxs-lookup"><span data-stu-id="04035-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="04035-109">Všetky podrobnosti o riadku faktúry z predtým potvrdenej faktúry sa skopírujú do nového konceptu.</span><span class="sxs-lookup"><span data-stu-id="04035-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="04035-110">Nasleduje niekoľko kľúčových bodov, ktoré vám pomôžu lepšie porozumieť podrobnostiam riadkov v novej opravenej faktúre:</span><span class="sxs-lookup"><span data-stu-id="04035-110">The following are some key points to help you understand more about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="04035-111">Všetky množstvá sa aktualizujú na nulu.</span><span class="sxs-lookup"><span data-stu-id="04035-111">All quantities are updated to zero.</span></span> <span data-ttu-id="04035-112">Toto predpokladá, že všetky fakturované položky sú úplne pripísané.</span><span class="sxs-lookup"><span data-stu-id="04035-112">This assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="04035-113">V prípade potreby môžete tieto množstvá manuálne aktualizovať, aby odrážali množstvo, ktoré sa fakturuje, a nie množstvo, ktoré sa pripisuje.</span><span class="sxs-lookup"><span data-stu-id="04035-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="04035-114">Na základe zadaného množstva aplikácia vypočíta pripísané množstvo.</span><span class="sxs-lookup"><span data-stu-id="04035-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="04035-115">Táto suma sa odráža v skutočnostiach, ktoré sa vytvárajú pri potvrdení opravenej faktúry.</span><span class="sxs-lookup"><span data-stu-id="04035-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="04035-116">Ak robíte zmeny v sume dane, musíte zadať správnu sumu dane, a nie sumu dane, ktorá sa pripisuje.</span><span class="sxs-lookup"><span data-stu-id="04035-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="04035-117">Opravy medzníkov sa vždy spracúvajú ako úplné kredity.</span><span class="sxs-lookup"><span data-stu-id="04035-117">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="04035-118">Ak bola zákazníkovi fakturovaná nesprávna suma, sumy preddavku alebo zálohy je možné opraviť.</span><span class="sxs-lookup"><span data-stu-id="04035-118">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="04035-119">Odsúhlasenia preddavkov a záloh je možné opraviť, ak bola použitá nesprávna suma na odsúhlasenie oproti nákladom na predtým potvrdenej faktúre.</span><span class="sxs-lookup"><span data-stu-id="04035-119">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04035-120">Detaily riadka faktúry, ktoré sú opravami ďalších už fakturovaných poplatkov, majú pole **Oprava** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="04035-120">Invoice line details that are corrections to other already invoiced charges have the **Correction** field set to **Yes**.</span></span> <span data-ttu-id="04035-121">Faktúry, ktoré majú opravené podrobnosti o riadku faktúry, majú pole s názvom **Obsahuje opravy**, ktoré je tiež nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="04035-121">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="04035-122">Skutočné hodnoty vytvorené po potvrdení opravnej faktúry</span><span class="sxs-lookup"><span data-stu-id="04035-122">Actuals created on confirmation of a corrective invoice</span></span>

<span data-ttu-id="04035-123">V nasledujúcej tabuľke sú uvedené skutočné hodnoty, ktoré sa vytvoria pri potvrdení opravnej faktúry.</span><span class="sxs-lookup"><span data-stu-id="04035-123">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="04035-124">
                    <strong>Scenár</strong>
                </span><span class="sxs-lookup"><span data-stu-id="04035-124">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="04035-125">
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="04035-125">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="04035-126">Potvrdenie opravy fakturovaného preddavku alebo zálohy.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="04035-126">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-127">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="04035-127">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="04035-128">Táto suma je kladná, pretože má zrušiť zápornú hodnotu, ktorá sa vytvorila pri fakturácii preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="04035-128">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-129">Storno skutočnej hodnoty fakturovaného predaja sa vytvorí pre sumu preddavku alebo zálohy na stornovanie pôvodného fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="04035-129">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-130">Nový opravený fakturovaný predaj sa vytvorí pre opravenú sumu v riadku opravenej faktúry založenej na preddavku alebo zálohe.</span><span class="sxs-lookup"><span data-stu-id="04035-130">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-131">Skutočná hodnota nevyfakturovaného predaja so zápornou sumou v opravenom riadku faktúry založenej na preddavku alebo zálohe, ktorý sa má použiť na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="04035-131">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="04035-132">Potvrdenie o oprave predtým odsúhlaseného preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="04035-132">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-133">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="04035-133">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="04035-134">Táto suma je kladná a má zrušiť zápornú hodnotu, ktorá sa vytvorila pri predchádzajúcom odsúhlasení.</span><span class="sxs-lookup"><span data-stu-id="04035-134">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-135">Skutočná hodnota stornovaného fakturovaného predaja pre sumu na predchádzajúcej faktúre.</span><span class="sxs-lookup"><span data-stu-id="04035-135">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-136">Nový opravený fakturovaný predaj pre opravenú sumu preddavku, ktorý sa použije v opravenej faktúre.</span><span class="sxs-lookup"><span data-stu-id="04035-136">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-137">Skutočná hodnota nevyfakturovaného predaja so zápornou sumou v opravenom zostávajúcom preddavku alebo zálohe, ktorý sa má použiť na odsúhlasenie v ďalších faktúrach.</span><span class="sxs-lookup"><span data-stu-id="04035-137">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04035-138">Fakturácia plného kreditu z predtým fakturovanej časovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="04035-138">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-139">Storno vyfakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="04035-139">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-140">Nová skutočná hodnota nefakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="04035-140">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="04035-141">Fakturácia čiastočného kreditu pre časovú transakciu.</span><span class="sxs-lookup"><span data-stu-id="04035-141">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-142">Storno vyfakturovaného predaja pre hodiny a vyfakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="04035-142">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-143">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="04035-143">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-144">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce hodiny a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="04035-144">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04035-145">Fakturácia plného kreditu z predtým fakturovanej výdavkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="04035-145">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-146">Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="04035-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-147">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="04035-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="04035-148">Fakturácia čiastočného kreditu z predtým fakturovanej výdavkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="04035-148">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-149">Storno vyfakturovaného predaja pre fakturované množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="04035-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-150">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach opraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="04035-150">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-151">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce množstvo a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="04035-151">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04035-152">Fakturácia plného kreditu z predtým fakturovanej poplatkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="04035-152">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-153">Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="04035-153">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-154">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="04035-154">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="04035-155">Fakturácia čiastočného kreditu z predtým fakturovanej poplatkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="04035-155">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-156">Storno vyfakturovaného predaja pre množstvo a fakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="04035-156">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-157">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného opravného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="04035-157">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="04035-158">Fakturácia plného kreditu z predtým fakturovaného medzníka.</span><span class="sxs-lookup"><span data-stu-id="04035-158">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-159">Storno vyfakturovaného predaja pre sumu v riadku s podrobnosťami pôvodnej faktúry pre medzník.</span><span class="sxs-lookup"><span data-stu-id="04035-159">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="04035-160">Stav faktúry medzníka sa aktualizuje z <b>Faktúra pre zákazníka bola zaúčtovaná</b> na <b>Pripravené na fakturáciu</b>.</span><span class="sxs-lookup"><span data-stu-id="04035-160">The invoice status on the milestone is updated from <b>Customer invoice posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="04035-161">Fakturácia čiastočného kreditu z predtým fakturovaného medzníka.</span><span class="sxs-lookup"><span data-stu-id="04035-161">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="04035-162">Nepodporované</span><span class="sxs-lookup"><span data-stu-id="04035-162">Unsupported</span></span> </p>
            </td>
        </tr>        
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
