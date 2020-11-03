---
title: Potvrdenie faktúry pro forma
description: Táto téma poskytuje informácie o potvrdzovaní zálohových faktúr v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4b67ee6848efdcb85cf732c1eaa3e40cdc51a2e2
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084272"
---
# <a name="confirming-a-proforma-invoice"></a><span data-ttu-id="91664-103">Potvrdenie faktúry pro forma</span><span class="sxs-lookup"><span data-stu-id="91664-103">Confirming a proforma invoice</span></span>

<span data-ttu-id="91664-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="91664-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="91664-105">Po potvrdení zálohovej faktúry sa stav projektovej faktúry aktualizuje na **Potvrdená**.</span><span class="sxs-lookup"><span data-stu-id="91664-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="91664-106">Po potvrdení bude faktúra iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="91664-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="91664-107">Odteraz bude možné faktúru opraviť, iba ak dôjde k opravám alebo kreditom iniciovaným zákazníkom alebo ak bude faktúra označená ako zaplatená.</span><span class="sxs-lookup"><span data-stu-id="91664-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="91664-108">Nasledujúca tabuľka obsahuje zoznam skutočných hodnôt vytvorených systémom.</span><span class="sxs-lookup"><span data-stu-id="91664-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="91664-109">Tieto skutočné hodnoty sa vytvoria, keď sa vykonajú určité operácie s konceptom faktúry projektu pred jej potvrdením.</span><span class="sxs-lookup"><span data-stu-id="91664-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="91664-110">
                    <strong>Scenár</strong>
                </span><span class="sxs-lookup"><span data-stu-id="91664-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="91664-111">
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="91664-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="91664-112">Fakturácia zálohy alebo preddavku</span><span class="sxs-lookup"><span data-stu-id="91664-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-113">Skutočná hodnota fakturovaného predaja typu <strong>Preddavok</strong> sa vytvára pre sumu na preddavku alebo na zálohe.</span><span class="sxs-lookup"><span data-stu-id="91664-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-114">Skutočná hodnota nevyfakturovaného predaja so zápornou sumou preddavku alebo zálohy, ktorá sa má použiť na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="91664-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="91664-115">Po úplnom odsúhlasení preddavku alebo zálohy na faktúre.</span><span class="sxs-lookup"><span data-stu-id="91664-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-116">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="91664-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="91664-117">Táto suma je kladná, pretože má zrušiť zápornú hodnotu, ktorá sa vytvorila pri fakturácii preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="91664-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-118">Skutočná hodnota fakturovaného predaja pre sumu na tejto faktúre.</span><span class="sxs-lookup"><span data-stu-id="91664-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="91664-119">Po čiastočnom odsúhlasení preddavku alebo zálohy na faktúre.</span><span class="sxs-lookup"><span data-stu-id="91664-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-120">Nevyfakturovaný obrat predaja preddavku alebo zálohy, ktorý bol vytvorený na odsúhlasenie.</span><span class="sxs-lookup"><span data-stu-id="91664-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="91664-121">Táto suma je kladná, pretože má zrušiť zápornú hodnotu, ktorá sa vytvorila pri fakturácii preddavku alebo zálohy.</span><span class="sxs-lookup"><span data-stu-id="91664-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-122">Skutočná hodnota fakturovaného predaja pre sumu na tejto faktúre.</span><span class="sxs-lookup"><span data-stu-id="91664-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-123">Negatívna skutočná hodnota nevyfakturovaného predaja zostávajúceho preddavku alebo suma zálohy, ktorá sa má použiť na odsúhlasenie na budúcich faktúrach.</span><span class="sxs-lookup"><span data-stu-id="91664-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="91664-124">Fakturácia časovej transakcie bez akýchkoľvek úprav konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="91664-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-125">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="91664-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-126">Vyfakturovaná skutočná hodnota predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="91664-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="91664-127">Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="91664-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-128">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="91664-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-129">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="91664-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-130">Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce hodiny a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="91664-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="91664-131">Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="91664-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-132">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="91664-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-133">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="91664-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="91664-134">Fakturácia transakcie výdavkov bez akýchkoľvek úprav konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="91664-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-135">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="91664-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-136">Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom schválení výdavkov</span><span class="sxs-lookup"><span data-stu-id="91664-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="91664-137">Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="91664-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-138">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="91664-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-139">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="91664-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-140">Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce množstvo a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalent skutočnej hodnoty fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="91664-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="91664-141">Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="91664-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-142">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="91664-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-143">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="91664-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="91664-144">Fakturácia poplatku.</span><span class="sxs-lookup"><span data-stu-id="91664-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-145">Nevyfakturovaný obrat predaja pre sumu poplatkov pri pôvodnom zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="91664-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-146">Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom zázname poplatkov v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="91664-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="91664-147">Fakturácia medzníka.</span><span class="sxs-lookup"><span data-stu-id="91664-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-148">Vyfakturovaná skutočná hodnota predaja pre sumu medzníka pre pôvodný medzník v riadku zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="91664-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="91664-149">Účtovanie riadkov zmlúv založených na produkte.</span><span class="sxs-lookup"><span data-stu-id="91664-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="91664-150">Skutočná hodnota fakturovaného predaja pre riadok produktu s množstvom a sumou pochádzajúcou z riadka zmluvy založenej na produkte.</span><span class="sxs-lookup"><span data-stu-id="91664-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
