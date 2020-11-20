---
title: Potvrdenie faktúry pro forma
description: Táto téma poskytuje informácie o potvrdení proforma faktúry.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128122"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="a3ae4-103">Potvrdenie faktúry pro forma</span><span class="sxs-lookup"><span data-stu-id="a3ae4-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="a3ae4-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="a3ae4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a3ae4-105">Po potvrdení zálohovej faktúry sa stav projektovej faktúry aktualizuje na **Potvrdená**.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="a3ae4-106">Po potvrdení bude faktúra iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="a3ae4-107">Odteraz bude možné faktúru opraviť, iba ak dôjde k opravám alebo kreditom iniciovaným zákazníkom alebo ak bude označená ako zaplatená.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="a3ae4-108">Nasledujúca tabuľka obsahuje zoznam skutočných hodnôt vytvorených systémom.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="a3ae4-109">Tieto skutočné hodnoty sa vytvoria, keď sa vykonajú určité operácie s konceptom faktúry projektu pred jej potvrdením.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="a3ae4-110">
                    <strong>Scenár</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a3ae4-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="a3ae4-111">
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="a3ae4-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a3ae4-112">Fakturácia časovej transakcie bez akýchkoľvek úprav konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-113">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-114">Vyfakturovaná skutočná hodnota predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a3ae4-115">Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-116">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-117">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-118">Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce hodiny a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a3ae4-119">Fakturácia časovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-120">Nevyfakturovaný obrat predaja pre hodiny a sumu pri pôvodnom schválení času.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-121">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a3ae4-122">Fakturácia transakcie výdavkov bez akýchkoľvek úprav konceptu faktúry.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-123">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-124">Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="a3ae4-125">Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa znížilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-126">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-127">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-128">Nová skutočná hodnota nefakturovaného predaja, ktorá je neúčtovateľná na zostávajúce množstvo a čiastku po odpočítaní opravených hodnôt v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a3ae4-129">Fakturácia výdavkovej transakcie, ktorá bola upravená tak, aby sa zvýšilo množstvo.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-130">Nevyfakturovaný obrat predaja pre množstvo a sumu pri pôvodnom schválení výdavkov.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-131">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného riadka faktúry, zrušenie skutočnej hodnoty nevyfakturovaného predaja a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="a3ae4-132">Fakturácia poplatku.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-133">Nevyfakturovaný obrat predaja pre sumu poplatkov pri pôvodnom zázname v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-134">Vyfakturovaná skutočná hodnota predaja pre množstvo a sumu pri pôvodnom zázname poplatkov v účtovnom denníku.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="a3ae4-135">Fakturácia medzníka.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="a3ae4-136">Vyfakturovaná skutočná hodnota predaja pre sumu medzníka pre pôvodný medzník v riadku zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="a3ae4-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
