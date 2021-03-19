---
title: Vytvorenie zálohy ad hoc v zmluve
description: Táto téma poskytuje informácie o vytvorení zálohy v zmluve podľa potreby.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2f0a6391a3bf6dd39d21504a6f286e4ff1954183
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273616"
---
# <a name="creating-an-ad-hoc-advance-on-a-contract"></a><span data-ttu-id="314eb-103">Vytvorenie zálohy ad hoc v zmluve</span><span class="sxs-lookup"><span data-stu-id="314eb-103">Creating an ad hoc advance on a contract</span></span>

<span data-ttu-id="314eb-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="314eb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="314eb-105">Microsoft Dynamics 365 Project Operations podporuje fakturačné scenáre, ktoré zahŕňajú preddavky a zálohy.</span><span class="sxs-lookup"><span data-stu-id="314eb-105">Microsoft Dynamics 365 Project Operations supports invoicing scenarios that involve pre-payments and advances.</span></span> <span data-ttu-id="314eb-106">Proces používania **Záloh** v **Project Operations** je podobný zmluvám založeným na **Preddavkoch**.</span><span class="sxs-lookup"><span data-stu-id="314eb-106">The process for using **Advances** in **Project Operations** is similar to **Retainer** contracts.</span></span> 

<span data-ttu-id="314eb-107">Podľa nasledujúcich pokynov môžete zákazníkovi fakturovať zálohu.</span><span class="sxs-lookup"><span data-stu-id="314eb-107">Complete the following steps to invoice the customer for an advance.</span></span>

1. <span data-ttu-id="314eb-108">Choďte na stránku **Projektová zmluva** a potom vyberte kartu **Zálohy a preddavky**.</span><span class="sxs-lookup"><span data-stu-id="314eb-108">Go to the **Project Contract** page, and then select the **Advances and Retainers** tab.</span></span>
2. <span data-ttu-id="314eb-109">Vo vedľajšej mriežke, ktorá obsahuje zoznam všetkých predtým zaznamenaných záloh a preddavkov, vyberte **+ Nový preddavok projektovej zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="314eb-109">In the subgrid that lists all the previously recorded advances and prepayments, select **+ New Project contract retainer**.</span></span> 

    <span data-ttu-id="314eb-110">Otvorí sa formulár **Rýchle vytvorenie** na zaznamenanie zálohy alebo preddavku.</span><span class="sxs-lookup"><span data-stu-id="314eb-110">The **Quick Create** form opens for recording a prepayment or advance.</span></span>
    
3. <span data-ttu-id="314eb-111">V nasledujúcej tabuľke sú uvedené polia na zaznamenanie zálohy a úvahy, na ktoré treba pamätať pri vytváraní nových:</span><span class="sxs-lookup"><span data-stu-id="314eb-111">The table below lists the fields for recording an advance and the considerations to keep in mind as you create new ones:</span></span>

    | <span data-ttu-id="314eb-112">Pole</span><span class="sxs-lookup"><span data-stu-id="314eb-112">Field</span></span> | <span data-ttu-id="314eb-113">Popis</span><span class="sxs-lookup"><span data-stu-id="314eb-113">Description</span></span> | <span data-ttu-id="314eb-114">Nadväzujúci vplyv</span><span class="sxs-lookup"><span data-stu-id="314eb-114">Downstream impact</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="314eb-115">**Zákazník projektovej zmluvy**</span><span class="sxs-lookup"><span data-stu-id="314eb-115">**Project Contract Customer**</span></span> | <span data-ttu-id="314eb-116">Toto pole označuje, ktorému zákazníkovi v zmluve bude fakturovaná táto záloha.</span><span class="sxs-lookup"><span data-stu-id="314eb-116">This field indicates which customer on the contract will be invoiced for this advance.</span></span> | <span data-ttu-id="314eb-117">Ak máte v zmluve viac zákazníkov a chcete každému z nich fakturovať konkrétnu zálohu alebo preddavok, vytvorte zálohu pre každého zákazníka osobitne.</span><span class="sxs-lookup"><span data-stu-id="314eb-117">If you have multiple customers on the contract and want to invoice each of them for a specific retainer or advance amount, create an advance for each customer individually.</span></span> |
    | <span data-ttu-id="314eb-118">**Opis**</span><span class="sxs-lookup"><span data-stu-id="314eb-118">**Description**</span></span> | <span data-ttu-id="314eb-119">Opis účelu alebo načasovania zálohy, ktorý pomáha pri identifikácii tejto zálohy.</span><span class="sxs-lookup"><span data-stu-id="314eb-119">The description of the purpose or timing of the advance to help identify this advance.</span></span> | <span data-ttu-id="314eb-120">Tento opis sa zobrazuje na riadku faktúry pre túto zálohu.</span><span class="sxs-lookup"><span data-stu-id="314eb-120">This description is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="314eb-121">**Suma**</span><span class="sxs-lookup"><span data-stu-id="314eb-121">**Amount**</span></span> | <span data-ttu-id="314eb-122">Suma zálohy alebo preddavku.</span><span class="sxs-lookup"><span data-stu-id="314eb-122">The amount for the pre-payment or advance.</span></span> | <span data-ttu-id="314eb-123">Táto suma sa zobrazuje na riadku faktúry pre túto zálohu.</span><span class="sxs-lookup"><span data-stu-id="314eb-123">This amount is displayed on the invoice line for this advance.</span></span> |
    | <span data-ttu-id="314eb-124">**Dátum fakturácie**</span><span class="sxs-lookup"><span data-stu-id="314eb-124">**Invoice Date**</span></span> | <span data-ttu-id="314eb-125">Dátum, kedy je tento preddavok fakturovaný zákazníkovi.</span><span class="sxs-lookup"><span data-stu-id="314eb-125">The date on which this advance is invoiced to the customer.</span></span> | <span data-ttu-id="314eb-126">Toto je dátum automatizovaného procesu vytvárania faktúry na vytvorenie riadku faktúry pre tento preddavok.</span><span class="sxs-lookup"><span data-stu-id="314eb-126">This is the date for the automated invoice creation process to create an invoice line for this advance.</span></span> |
    | <span data-ttu-id="314eb-127">**Stav faktúry**</span><span class="sxs-lookup"><span data-stu-id="314eb-127">**Invoice Status**</span></span> | <span data-ttu-id="314eb-128">Toto je nastavenie možnosti, ktoré označuje, či je tento preddavok pridaný do konceptu faktúry pre tohto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="314eb-128">This is an option setting that indicates whether this advance is added to a draft invoice for this customer.</span></span> <span data-ttu-id="314eb-129">Možné hodnoty sú:</span><span class="sxs-lookup"><span data-stu-id="314eb-129">The possible values are:</span></span></br><span data-ttu-id="314eb-130">- **Nepripravené na fakturáciu**</span><span class="sxs-lookup"><span data-stu-id="314eb-130">- **Not ready to invoice**</span></span></br><span data-ttu-id="314eb-131">- **Pripravené na faktúru**</span><span class="sxs-lookup"><span data-stu-id="314eb-131">- **Ready to invoice**</span></span> | <span data-ttu-id="314eb-132">Keď sú záloha alebo preddavok označené ako **Pripravené na fakturáciu**, sú pridané ako čas riadku na koncepte faktúry.</span><span class="sxs-lookup"><span data-stu-id="314eb-132">When an advance or pre-payment is marked as **Ready to invoice**, it is added as a line time on a draft invoice.</span></span> <span data-ttu-id="314eb-133">Na vyrovnanie s nákladmi na projekt na ďalšie fakturačné obdobie je možné použiť iba plne fakturovaný preddavok.</span><span class="sxs-lookup"><span data-stu-id="314eb-133">Only a fully invoiced advance can be used to reconcile against project costs for the next invoice period.</span></span> |

4. <span data-ttu-id="314eb-134">Vyberte **Uložiť a zavrieť** v dialógovom okne rýchleho vytvorenia na zaznamenanie zálohy alebo preddavku.</span><span class="sxs-lookup"><span data-stu-id="314eb-134">Select **Save and close** on the quick create dialog to record the advance or the pre-payment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]