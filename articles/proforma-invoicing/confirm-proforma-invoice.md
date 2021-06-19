---
title: Potvrdenie projektovej faktúry pro forma
description: Táto téma poskytuje informácie o tom, ako potvrdiť projektovú faktúru pro forma.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012155"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="9d401-103">Potvrdenie projektovej faktúry pro forma</span><span class="sxs-lookup"><span data-stu-id="9d401-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="9d401-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="9d401-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="9d401-105">Po potvrdení zálohovej faktúry sa stav projektovej faktúry aktualizuje na **Potvrdená**.</span><span class="sxs-lookup"><span data-stu-id="9d401-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="9d401-106">Po potvrdení bude faktúra iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="9d401-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="9d401-107">Odteraz bude možné faktúru opraviť, iba ak dôjde k opravám alebo kreditom iniciovaným zákazníkom.</span><span class="sxs-lookup"><span data-stu-id="9d401-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="9d401-108">Nasledujúca tabuľka obsahuje zoznam skutočných hodnôt vytvorených systémom.</span><span class="sxs-lookup"><span data-stu-id="9d401-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="9d401-109">Tieto skutočné hodnoty sa vytvoria, keď sa vykonajú určité operácie s konceptom faktúry projektu pred jej potvrdením.</span><span class="sxs-lookup"><span data-stu-id="9d401-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="9d401-110">
                    <strong>Scenár</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9d401-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="9d401-111">
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="9d401-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-112">Fakturácia zálohy alebo preddavku</span><span class="sxs-lookup"><span data-stu-id="9d401-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-113">Skutočná hodnota fakturovaného predaja typu <strong>Preddavok</strong> sa vytvára pre sumu na preddavku alebo na zálohe.</span><span class="sxs-lookup"><span data-stu-id="9d401-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-114">Nevyfakturovaná skutočná hodnota predaja so zápornou čiastkou preddavku alebo zálohy, ktorý sa má použiť na vyrovnanie.</span><span class="sxs-lookup"><span data-stu-id="9d401-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-115">Po úplnom odsúhlasení preddavku alebo zálohy na faktúre.</span><span class="sxs-lookup"><span data-stu-id="9d401-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-116">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="9d401-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9d401-117">Táto suma je kladná, pretože má zrušiť zápornú hodnotu, ktorá sa vytvorila pri fakturácii preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="9d401-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-118">Skutočná hodnota fakturovaného predaja pre sumu na tejto faktúre.</span><span class="sxs-lookup"><span data-stu-id="9d401-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9d401-119">Po čiastočnom odsúhlasení preddavku alebo zálohy na faktúre.</span><span class="sxs-lookup"><span data-stu-id="9d401-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-120">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="9d401-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="9d401-121">Táto suma je kladná, pretože má zrušiť zápornú hodnotu, ktorá sa vytvorila pri fakturácii preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="9d401-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-122">Skutočná hodnota fakturovaného predaja pre sumu na tejto faktúre.</span><span class="sxs-lookup"><span data-stu-id="9d401-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-123">Negatívna skutočná hodnota nevyfakturovaného predaja zostávajúceho preddavku alebo suma zálohy, ktorá sa má použiť na odsúhlasenie na budúcich faktúrach.</span><span class="sxs-lookup"><span data-stu-id="9d401-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-124">Fakturácia časovej transakcie bez akýchkoľvek úprav konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="9d401-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-125">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="9d401-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-126">Vyfakturovaná skutočná hodnota predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="9d401-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9d401-127">Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="9d401-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-128">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="9d401-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-129">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-130">Nová skutočná hodnota nevyfakturovaného predaja, ktorý nie je možné účtovať za zostávajúce hodiny a čiastku po odpočítaní opravených hodnôt v detaile upraveného riadku faktúry, storno skutočnej hodnoty predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-131">Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="9d401-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-132">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="9d401-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-133">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-134">Fakturácia transakcie výdavkov bez akýchkoľvek úprav konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="9d401-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-135">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9d401-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-136">Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9d401-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9d401-137">Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="9d401-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-138">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9d401-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-139">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-140">Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce množstvo a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalent skutočnej hodnoty fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-141">Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="9d401-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-142">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9d401-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-143">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-144">Fakturácia materiálovej transakcie bez akýchkoľvek úprav konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="9d401-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-145">Nefakturované storno predaja pre množstvo a sumu na pôvodne schválenom použití materiálu.</span><span class="sxs-lookup"><span data-stu-id="9d401-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-146">Fakturovaná skutočná hodnota predaja pre množstvo a sumu na pôvodne schválenom použití materiálu.</span><span class="sxs-lookup"><span data-stu-id="9d401-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="9d401-147">Fakturácia materiálovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="9d401-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-148">Nefakturované storno predaja pre množstvo a sumu na pôvodne schválenom čase.</span><span class="sxs-lookup"><span data-stu-id="9d401-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-149">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-150">Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce množstvo a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalent skutočnej hodnoty fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-151">Fakturácia materiálovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="9d401-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-152">Nefakturované storno predaja pre množstvo a sumu na pôvodne schválenom použití materiálu.</span><span class="sxs-lookup"><span data-stu-id="9d401-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-153">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="9d401-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="9d401-154">Fakturácia poplatku.</span><span class="sxs-lookup"><span data-stu-id="9d401-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-155">Nevyfakturovaný obrat predaja pre sumu poplatkov pri pôvodnom zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="9d401-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-156">Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom zázname poplatkov v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="9d401-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="9d401-157">Fakturácia medzníka.</span><span class="sxs-lookup"><span data-stu-id="9d401-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="9d401-158">Vyfakturovaná skutočná hodnota predaja pre sumu medzníka pre pôvodný medzník v riadku zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="9d401-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
