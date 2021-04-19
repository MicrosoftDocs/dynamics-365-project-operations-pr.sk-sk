---
title: Opravné projektové faktúry
description: Táto téma poskytuje informácie o tom, ako vytvárať a potvrdzovať opravné projektové faktúry v Project Operations.
author: rumant
manager: Annbe
ms.date: 03/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fc96bb40f5207efc381986d46a3e37dfc1dc111c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867060"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="8694d-103">Opravné projektové faktúry</span><span class="sxs-lookup"><span data-stu-id="8694d-103">Corrective project-based invoices</span></span>

<span data-ttu-id="8694d-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="8694d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8694d-105">Potvrdenú projektovú faktúru je možné podľa dohody so zákazníkom a projektovým manažérom opraviť tak, že sa spracujú zmeny alebo pripíšu kredity.</span><span class="sxs-lookup"><span data-stu-id="8694d-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="8694d-106">Ak chcete vykonať úpravy potvrdenej faktúry, otvorte potvrdenú faktúru a vyberte **Opraviť túto faktúru**.</span><span class="sxs-lookup"><span data-stu-id="8694d-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="8694d-107">Tento výber nie je k dispozícii, pokiaľ nie je potvrdená projektová faktúra alebo pokiaľ projektové faktúry neobsahujú zálohy alebo zadržané prostriedky alebo porovnanie záloh alebo zadržaných prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="8694d-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="8694d-108">Z potvrdenej faktúry sa vytvorí nový koncept faktúry.</span><span class="sxs-lookup"><span data-stu-id="8694d-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="8694d-109">Všetky podrobnosti o riadku faktúry z predtým potvrdenej faktúry sa skopírujú do nového konceptu.</span><span class="sxs-lookup"><span data-stu-id="8694d-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="8694d-110">Ďalej sú uvedené niektoré kľúčové body pre podrobnosti o riadkoch v novej opravenej faktúre, ktorým je potrebné porozumieť:</span><span class="sxs-lookup"><span data-stu-id="8694d-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="8694d-111">Všetky množstvá sa aktualizujú na nulu.</span><span class="sxs-lookup"><span data-stu-id="8694d-111">All quantities are updated to zero.</span></span> <span data-ttu-id="8694d-112">Dynamics 365 Project Operations predpokladá, že všetky fakturované položky sú úplne pripísané.</span><span class="sxs-lookup"><span data-stu-id="8694d-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="8694d-113">V prípade potreby môžete tieto množstvá manuálne aktualizovať, aby odrážali množstvo, ktoré sa fakturuje, a nie množstvo, ktoré sa pripisuje.</span><span class="sxs-lookup"><span data-stu-id="8694d-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="8694d-114">Na základe zadaného množstva aplikácia vypočíta pripísané množstvo.</span><span class="sxs-lookup"><span data-stu-id="8694d-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="8694d-115">Táto suma sa odráža v skutočnostiach, ktoré sa vytvárajú pri potvrdení opravenej faktúry.</span><span class="sxs-lookup"><span data-stu-id="8694d-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="8694d-116">Ak robíte zmeny v sume dane, musíte zadať správnu sumu dane, a nie sumu dane, ktorá sa pripisuje.</span><span class="sxs-lookup"><span data-stu-id="8694d-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="8694d-117">Opravy medzníkov sa vždy spracúvajú ako úplné kredity.</span><span class="sxs-lookup"><span data-stu-id="8694d-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="8694d-118">Pre podrobnosti riadka faktúry, ktoré sú opravami ďalších už fakturovaných poplatkov, je pole **Oprava** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="8694d-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="8694d-119">Pre faktúry, ktoré majú opravené podrobnosti riadka faktúry, je pole **Obsahuje opravy** nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="8694d-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="8694d-120">Skutočné hodnoty vytvorené po potvrdení opravnej faktúry</span><span class="sxs-lookup"><span data-stu-id="8694d-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="8694d-121">V nasledujúcej tabuľke sú uvedené skutočné hodnoty, ktoré sa vytvoria pri potvrdení opravnej faktúry.</span><span class="sxs-lookup"><span data-stu-id="8694d-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="8694d-122">
                    <strong>Scenár</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8694d-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="8694d-123">
                    <strong>Skutočné hodnoty vytvorené po potvrdení</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8694d-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8694d-124">Fakturácia plného kreditu z predtým fakturovanej časovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="8694d-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-125">Storno vyfakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="8694d-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-126">Nová skutočná hodnota nefakturovaného predaja pre hodiny a sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="8694d-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8694d-127">Fakturácia čiastočného kreditu pre časovú transakciu.</span><span class="sxs-lookup"><span data-stu-id="8694d-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-128">Storno vyfakturovaného predaja pre hodiny a vyfakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre čas.</span><span class="sxs-lookup"><span data-stu-id="8694d-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-129">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na hodiny a čiastku v podrobnostiach upraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="8694d-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-130">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce hodiny a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="8694d-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8694d-131">Fakturácia plného kreditu z predtým fakturovanej výdavkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="8694d-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-132">Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="8694d-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-133">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="8694d-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8694d-134">Fakturácia čiastočného kreditu z predtým fakturovanej výdavkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="8694d-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-135">Storno vyfakturovaného predaja pre fakturované množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre výdavok.</span><span class="sxs-lookup"><span data-stu-id="8694d-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-136">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach opraveného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="8694d-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-137">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce množstvo a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="8694d-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8694d-138">Fakturácia celého kreditu predtým fakturovanej transakcie materiálu.</span><span class="sxs-lookup"><span data-stu-id="8694d-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-139">Fakturované storno predaja pre množstvo a sumu na pôvodnom riadku faktúry s podrobnosťami za materiál.</span><span class="sxs-lookup"><span data-stu-id="8694d-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-140">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu na pôvodnom riadku faktúry s podrobnosťami za materiál.</span><span class="sxs-lookup"><span data-stu-id="8694d-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="8694d-141">Fakturácia čiastočného kreditu pri transakcii materiálu.</span><span class="sxs-lookup"><span data-stu-id="8694d-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-142">Fakturované storno predaja pre množstvo a sumu fakturovanú na pôvodnom riadku faktúry s podrobnosťami za materiál.</span><span class="sxs-lookup"><span data-stu-id="8694d-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-143">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná za množstvo a sumu na upravenom detaile riadku faktúry, jej storno a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="8694d-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-144">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná pre zostávajúce množstvo a sumu po odpočítaní opravených hodnôt v podrobnostiach o riadku faktúry.</span><span class="sxs-lookup"><span data-stu-id="8694d-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8694d-145">Fakturácia plného kreditu z predtým fakturovanej poplatkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="8694d-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-146">Storno vyfakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="8694d-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-147">Nová skutočná hodnota nefakturovaného predaja pre množstvo a sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="8694d-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8694d-148">Fakturácia čiastočného kreditu z predtým fakturovanej poplatkovej transakcie.</span><span class="sxs-lookup"><span data-stu-id="8694d-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-149">Storno vyfakturovaného predaja pre množstvo a fakturovanú sumu v riadku s podrobnosťami pôvodnej faktúry pre poplatok.</span><span class="sxs-lookup"><span data-stu-id="8694d-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-150">Nová skutočná hodnota nefakturovaného predaja, ktorá je účtovateľná na množstvo a čiastku v podrobnostiach upraveného opravného riadka faktúry, jeho zrušenie a ekvivalentná skutočná hodnota fakturovaného predaja.</span><span class="sxs-lookup"><span data-stu-id="8694d-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8694d-151">Fakturácia plného kreditu z predtým fakturovaného medzníka.</span><span class="sxs-lookup"><span data-stu-id="8694d-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-152">Storno vyfakturovaného predaja pre sumu v riadku s podrobnosťami pôvodnej faktúry pre medzník.</span><span class="sxs-lookup"><span data-stu-id="8694d-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="8694d-153">Stav faktúry medzníka sa aktualizuje z <b>Bola uverejnená faktúra pre zákazníka</b> na <b>Pripravené na fakturáciu</b>.</span><span class="sxs-lookup"><span data-stu-id="8694d-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="8694d-154">Fakturácia čiastočného kreditu z predtým fakturovaného medzníka.</span><span class="sxs-lookup"><span data-stu-id="8694d-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="8694d-155">Tento scenár nie je podporovaný.</span><span class="sxs-lookup"><span data-stu-id="8694d-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
