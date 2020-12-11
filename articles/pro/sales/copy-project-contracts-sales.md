---
title: Kopírovanie projektových zmlúv – čiastočné
description: Táto téma poskytuje informácie o kopírovaní projektových zmlúv v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4137fc400c7fdd8fecd9d8349bf7f57f3470b51f
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181426"
---
# <a name="copy-project-contracts---lite"></a><span data-ttu-id="cb829-103">Kopírovanie projektových zmlúv – čiastočné</span><span class="sxs-lookup"><span data-stu-id="cb829-103">Copy project contracts - lite</span></span>

<span data-ttu-id="cb829-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="cb829-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb829-105">Nové projektové zmluvy môžete vytvoriť ľahko vytvorením kópií existujúcich zmlúv jedným z dvoch spôsobov:</span><span class="sxs-lookup"><span data-stu-id="cb829-105">You can easily create new project contracts by making copies of existing contracts in one of two ways:</span></span> 

  - <span data-ttu-id="cb829-106">Na stránke zoznamu **Projektové zmluvy** vyberte projektovú zmluvu a potom vyberte položku **Kopírovať**.</span><span class="sxs-lookup"><span data-stu-id="cb829-106">On the **Project Contracts** list page, select a project contract and then select **Copy**.</span></span>
  - <span data-ttu-id="cb829-107">Na stránke s podrobnosťami **Projektová zmluva** vyberte **Kopírovať**.</span><span class="sxs-lookup"><span data-stu-id="cb829-107">On the **Project Contract** details page, select **Copy**.</span></span>

<span data-ttu-id="cb829-108">Otvorí sa dialógové okno, kde môžete zvoliť parametre kopírovanej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cb829-108">A dialog page will open where you can select the parameters of the copied contract.</span></span> <span data-ttu-id="cb829-109">V dialógovom okne sa nachádzajú nasledujúce polia.</span><span class="sxs-lookup"><span data-stu-id="cb829-109">The following fields are included on the dialog.</span></span> <span data-ttu-id="cb829-110">V závislosti od hodnôt, ktoré ste vybrali v tomto dialógovom okne sa môže proces kopírovania zmeniť.</span><span class="sxs-lookup"><span data-stu-id="cb829-110">Depending on the values you select in this dialog, the copy process may change.</span></span>

| <span data-ttu-id="cb829-111">**Pole**</span><span class="sxs-lookup"><span data-stu-id="cb829-111">**Field**</span></span> | <span data-ttu-id="cb829-112">**Opis**</span><span class="sxs-lookup"><span data-stu-id="cb829-112">**Description**</span></span> | <span data-ttu-id="cb829-113">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="cb829-113">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cb829-114">Predmet</span><span class="sxs-lookup"><span data-stu-id="cb829-114">Topic</span></span> | <span data-ttu-id="cb829-115">Zadajte tému cieľovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cb829-115">Enter the topic of the target contract.</span></span> <span data-ttu-id="cb829-116">Keď sa otvorí stránka dialógového okna, systém nastaví toto pole na názov zdrojovej zmluvy s doplnkom **kópia**.</span><span class="sxs-lookup"><span data-stu-id="cb829-116">When the dialog page opens, the system will set this field to the name of the source contract with **copy** appended to it.</span></span> | <span data-ttu-id="cb829-117">Toto pole nemá žiadny následný dopad.</span><span class="sxs-lookup"><span data-stu-id="cb829-117">There's no downstream impact for this field.</span></span> |
| <span data-ttu-id="cb829-118">Zákazník</span><span class="sxs-lookup"><span data-stu-id="cb829-118">Customer</span></span> | <span data-ttu-id="cb829-119">Odkaz na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu.</span><span class="sxs-lookup"><span data-stu-id="cb829-119">Reference to the customer's company or account record.</span></span> <span data-ttu-id="cb829-120">Po otvorení dialógového okna systém nastaví toto pole na účet uvedený v zdrojovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="cb829-120">When the dialog opens, the system will set this field to the account on the source contract.</span></span> | <span data-ttu-id="cb829-121">Toto pole je primárnym zákazníkom v zmluve.</span><span class="sxs-lookup"><span data-stu-id="cb829-121">This field is the primary customer on the contract.</span></span> |
| <span data-ttu-id="cb829-122">Zmluvná jednotka</span><span class="sxs-lookup"><span data-stu-id="cb829-122">Contracting Unit</span></span> | <span data-ttu-id="cb829-123">Organizačná jednotka, ktorá je zodpovedná za realizáciu projektov spojených s týmto obchodom.</span><span class="sxs-lookup"><span data-stu-id="cb829-123">The Organization unit that is responsible for the delivery of the project(s) associated with this deal.</span></span> <span data-ttu-id="cb829-124">Po otvorení stránky dialógového okna ho systém nastaví na zmluvnú jednotku zdrojovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cb829-124">When the dialog page opens, the system will set it to the contracting unit of the source contract.</span></span> | <span data-ttu-id="cb829-125">Zmluvnou jednotkou je divízia spoločnosti, ktorá bude po uzatvorení obchodu realizovať projekty.</span><span class="sxs-lookup"><span data-stu-id="cb829-125">The contracting unit is the division of the company that will be executing the projects after the deal is closed.</span></span> <span data-ttu-id="cb829-126">Každá zmluvná jednotka má menu.</span><span class="sxs-lookup"><span data-stu-id="cb829-126">Every contracting unit has a currency.</span></span> <span data-ttu-id="cb829-127">Táto mena sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas projektu.</span><span class="sxs-lookup"><span data-stu-id="cb829-127">This currency is used to report estimated and actual costs incurred during the project.</span></span> |
| <span data-ttu-id="cb829-128">Mena</span><span class="sxs-lookup"><span data-stu-id="cb829-128">Currency</span></span> | <span data-ttu-id="cb829-129">Mena, v ktorej sa obchoduje transakcia.</span><span class="sxs-lookup"><span data-stu-id="cb829-129">The currency that the deal is transacted in.</span></span> <span data-ttu-id="cb829-130">Po otvorení stránky dialógového okna systém nastaví toto pole na menu zdrojovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cb829-130">When the dialog page opens, the system will set the field to the currency of the source contract.</span></span> <span data-ttu-id="cb829-131">Mena sa môže zmeniť.</span><span class="sxs-lookup"><span data-stu-id="cb829-131">The currency can be changed.</span></span> <span data-ttu-id="cb829-132">V takom prípade je pole **Kopírovať ceny** vždy nastavené na **Nie**, pretože cenníky na zdrojovej zmluve už nie sú relevantné.</span><span class="sxs-lookup"><span data-stu-id="cb829-132">If it is, the **Copy Pricing** field is always set to **No** because the price lists on source contract are no longer relevant.</span></span> | <span data-ttu-id="cb829-133">Mena sa používa pre predvolené cenníky, na zostavenie finančných odhadov zmluvy a na fakturáciu zákazníkovi, keď dôjde k získaniu obchodu.</span><span class="sxs-lookup"><span data-stu-id="cb829-133">Currency is used for default price lists, for building financial estimates on the contract, and for invoicing the customer when the deal is won.</span></span> |
| <span data-ttu-id="cb829-134">Požadovaný dátum doručenia</span><span class="sxs-lookup"><span data-stu-id="cb829-134">Requested Delivery Date</span></span> | <span data-ttu-id="cb829-135">Dodací termín požadovaný zákazníkom.</span><span class="sxs-lookup"><span data-stu-id="cb829-135">The delivery date requested by the customer.</span></span> | <span data-ttu-id="cb829-136">Dátum sa používa ako konečný dátum pri vytváraní fakturačných dátumov podľa konkrétnej frekvencie.</span><span class="sxs-lookup"><span data-stu-id="cb829-136">This date is used as the end date when you create invoicing dates along a specific frequency.</span></span> |
| <span data-ttu-id="cb829-137">Kopírovať cenu</span><span class="sxs-lookup"><span data-stu-id="cb829-137">Copy pricing</span></span> | <span data-ttu-id="cb829-138">Označuje, či sa má cena v zmluve kopírovať zo zdrojovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cb829-138">Indicates whether the pricing on the contract should be copied from the source contract.</span></span> | <span data-ttu-id="cb829-139">Ak je pole nastavené na **Áno**, cenník projektu a referencie cenníka produktu sa skopírujú zo zdrojovej do cieľovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cb829-139">If the field is set to **Yes**, project and product price list references are copied from the source to the target contract.</span></span> <span data-ttu-id="cb829-140">Ak je vybraná možnosť **Nie**, cenníky sa predvolene nastavujú na základe najnovších cenníkov v parametroch účtu alebo projektu.</span><span class="sxs-lookup"><span data-stu-id="cb829-140">If **No** is selected, price lists default based on the latest price lists on the account or project parameters.</span></span> |

<span data-ttu-id="cb829-141">Keď stránke dialógového okna vyberiete **OK**, systém vytvorí kópiu zmluvy na základe vybratých parametrov.</span><span class="sxs-lookup"><span data-stu-id="cb829-141">When you select **OK** on the dialog page, the system creates a copy of the contract based on the parameters selected.</span></span> <span data-ttu-id="cb829-142">Otvorí sa nová zmluva.</span><span class="sxs-lookup"><span data-stu-id="cb829-142">The new contract will open.</span></span>

<span data-ttu-id="cb829-143">Nasledujúce informácie sa nekopírujú zo **zdrojovej** do **cieľovej zmluvy**:</span><span class="sxs-lookup"><span data-stu-id="cb829-143">The following information isn't copied from the **Source** to the **Target Contract**:</span></span>

  - <span data-ttu-id="cb829-144">Plány faktúry</span><span class="sxs-lookup"><span data-stu-id="cb829-144">Invoice schedules</span></span>
  - <span data-ttu-id="cb829-145">Zákazníci v zmluve a v riadku zmluvy</span><span class="sxs-lookup"><span data-stu-id="cb829-145">Contract and contract line customers</span></span>
  - <span data-ttu-id="cb829-146">Odkaz na projekt v riadkoch zmlúv založených na projekte</span><span class="sxs-lookup"><span data-stu-id="cb829-146">Project reference on the project-based contract lines</span></span>
  - <span data-ttu-id="cb829-147">Informácie o rozpočte zákazníka</span><span class="sxs-lookup"><span data-stu-id="cb829-147">Customer budget information</span></span>

<span data-ttu-id="cb829-148">Pretože sú tieto informácie veľmi špecifické pre každú zmluvy, tieto polia a záznamy sa nekopírujú.</span><span class="sxs-lookup"><span data-stu-id="cb829-148">Because this information is specific to each contract, these fields and records aren't copied.</span></span> <span data-ttu-id="cb829-149">Skopírujú sa riadky zmluvy pre projekty a produkty, odhady podrobností v riadku zmluvy a hodnoty na úrovni zmluvy, ktoré sa nemajú prekročiť.</span><span class="sxs-lookup"><span data-stu-id="cb829-149">Contract lines for projects and products, estimations on contract line details, and not-to-exceed values at the contract level are copied.</span></span> <span data-ttu-id="cb829-150">Predvolené ceny a sadzby nákladov závisia od výberu v poli **Kopírovať ceny** na stránke dialógového okna **Kopírovať parametre**.</span><span class="sxs-lookup"><span data-stu-id="cb829-150">Price and cost rate defaulting depend on the selection in the **Copy pricing** field on the **Copy Parameters** dialog page.</span></span>