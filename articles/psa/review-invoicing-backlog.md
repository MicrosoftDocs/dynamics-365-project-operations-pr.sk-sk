---
title: Skontrolujte fakturačné oneskorenie projektov a projektových zmlúv
description: Táto téma poskytuje informácie o tom, ako skontrolovať čas, výdavky a backlogy produktu a ako ich označiť ako pripravené na fakturáciu.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 092455a131f556e4f943f6bb89d7e38358f0a697
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150507"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="25e21-103">Skontrolujte fakturačné oneskorenie projektov a projektových zmlúv</span><span class="sxs-lookup"><span data-stu-id="25e21-103">Review the invoicing backlog on projects and project contracts</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="25e21-104">Ak je transakcia pripravená na vytvorenie a spracovanie faktúry, transakcia by mala byť označená ako **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="25e21-105">Táto téma popisuje typy transakcií, ktoré je možné vytvoriť.</span><span class="sxs-lookup"><span data-stu-id="25e21-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="25e21-106">Prezrite si backlog fakturácie času a materiálu</span><span class="sxs-lookup"><span data-stu-id="25e21-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="25e21-107">Keď je položka času alebo výdavkov predložená a schválená pre projekt, PSA vytvorí skutočný projekt.</span><span class="sxs-lookup"><span data-stu-id="25e21-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="25e21-108">Ak kombinácia projektu a transakcie triedy sú priradené k riadku zmluvy pre čas a materiály projektu, dve skutočné hodnoty sa vytvoria po schválení položky:</span><span class="sxs-lookup"><span data-stu-id="25e21-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="25e21-109">Skutočné údaje nákladov</span><span class="sxs-lookup"><span data-stu-id="25e21-109">Cost actual</span></span> 
- <span data-ttu-id="25e21-110">Nevyfakturované skutočné hodnoty predajov</span><span class="sxs-lookup"><span data-stu-id="25e21-110">Unbilled sales actual</span></span>

<span data-ttu-id="25e21-111">Neúčtované predajné skutočné hodnoty predstavujú fakturačný backlog a stav fakturácie musí byť nastavený na **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="25e21-112">Po vytvorení faktúry projektu sa nevyfakturované skutočné hodnoty predajov s označením **Pripravené na fakturáciu** skopírujú ako podrobnosti riadka faktúry.</span><span class="sxs-lookup"><span data-stu-id="25e21-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="25e21-113">Ak chcete skontrolovať fakturačné oneskorenie pre čas a materiály, prejdite na **Predaj** \> **Fakturácia** \> **Backlog pre fakturáciu času a materiálu**.</span><span class="sxs-lookup"><span data-stu-id="25e21-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="25e21-114">Vyberte všetky neúčtované predajné skutočné hodnoty, ktoré sú pripravené na fakturáciu, a potom vyberte položku **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="25e21-115">Stav fakturácie týchto skutočných hodnôt sa zmení na možnosť **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Backlog pre fakturáciu času a materiálu](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="25e21-117">Backlog pre fakturáciu produktov</span><span class="sxs-lookup"><span data-stu-id="25e21-117">Review the product billing backlog</span></span>

<span data-ttu-id="25e21-118">V prípade, že projektová zmluva má riadky zmluvy založené na produkte, tieto riadky sa považujú za fakturáciu pri každom vytvorení faktúry pre zmluvu o projekte.</span><span class="sxs-lookup"><span data-stu-id="25e21-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="25e21-119">Každý produkt, ktorý má riadky zmluvy, ktoré sú označené ako **Pripravené na faktúru**, sa skopíruje do faktúry projektu ako riadky projektových faktúr.</span><span class="sxs-lookup"><span data-stu-id="25e21-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="25e21-120">Ak chcete skontrolovať backlog fakturácie pre produkty, prejdite na **Predaj** \> **Fakturácia** \> **Backlog pre fakturáciu produktov**.</span><span class="sxs-lookup"><span data-stu-id="25e21-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="25e21-121">Zvoľte všetky riadky zmluvy produktovej faktúry, ktoré sú pripravené na fakturáciu a potom stlačte možnosť **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="25e21-122">Stav fakturácie týchto riadkov sa zmení na možnosť **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Backlog pre fakturáciu produktov](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="25e21-124">Skontrolujte medzníky fakturácie na zmluvách s pevnou cenou</span><span class="sxs-lookup"><span data-stu-id="25e21-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="25e21-125">Každý riadok projektovej zmluvy, ktorý má fakturačnú metódu s pevnou cenou, musí definovať čiastkové ciele zmluvy.</span><span class="sxs-lookup"><span data-stu-id="25e21-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="25e21-126">Tieto míľniky zmluvy možno fakturovať iba vtedy, ak sú označené príznakom **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="25e21-127">Ak chcete skontrolovať fakturačné míľniky, prejdite na ponuku **Predaj** \> **Faktúra** \> **Medzníky pevných cien**.</span><span class="sxs-lookup"><span data-stu-id="25e21-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="25e21-128">Zvoľte si medzníky, ktoré sú pripravené na fakturáciu a následne stlačte možnosť **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="25e21-129">Stav fakturácie týchto medzných hodnôt sa zmení na možnosť **Pripravené na faktúru**.</span><span class="sxs-lookup"><span data-stu-id="25e21-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Medzníky pevných cien](media/FPBacklog.png)
