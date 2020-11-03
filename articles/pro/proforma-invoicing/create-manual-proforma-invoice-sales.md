---
title: Vytvorenie manuálnej zálohovej faktúry
description: Táto téma poskytuje informácie o manuálnom vytváraní zálohovej faktúry v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5e93206737507bf6698a9746815c790d3dfc904
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/20/2020
ms.locfileid: "4084593"
---
# <a name="creating-a-manual-proforma-invoice"></a><span data-ttu-id="8a4c2-103">Vytvorenie manuálnej zálohovej faktúry</span><span class="sxs-lookup"><span data-stu-id="8a4c2-103">Creating a manual proforma invoice</span></span>

<span data-ttu-id="8a4c2-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="8a4c2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8a4c2-105">V Dynamics 365 Project Operations možno zálohové faktúry podľa potreby vytvárať manuálne.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="8a4c2-106">Zálohovú faktúru môžete vytvoriť manuálne na stránke so zoznamom **Projektové zmluvy** alebo na stránke s podrobnosťami **Projektová zmluva**.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="8a4c2-107">Stránka so zoznamom projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="8a4c2-107">Project Contracts list page</span></span>

<span data-ttu-id="8a4c2-108">Na stránke so zoznamom **Projektové zmluvy** vyberte jednu alebo viac projektových zmlúv a vytvorte faktúry pre všetky vybrané záznamy.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="8a4c2-109">Systém kontroluje, ktoré z vybraných projektových zmlúv majú nevybavené termíny **Pripravené na faktúru** datované pred dnešným dátumom.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog  dated before today's date.</span></span> <span data-ttu-id="8a4c2-110">Z týchto zmlúv systém vytvára koncepty zálohových faktúr.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="8a4c2-111">Ak má projektová zmluva viac zákazníkov, môže byť pre každého zákazníka vytvorená jedna faktúra a pre každú projektovú zmluvu viac faktúr.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="8a4c2-112">Všetky vytvorené faktúry pre projekt sú k dispozícii na stránke **Faktúra** v časti **Fakturácia** v oblasti **Predaj**.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="8a4c2-113">Stránka s podrobnosťami o projektovej zmluve</span><span class="sxs-lookup"><span data-stu-id="8a4c2-113">Project Contract details page</span></span>

<span data-ttu-id="8a4c2-114">Zálohovú faktúru je možné vytvoriť aj na stránke s podrobnosťami **Projektová zmluva** , kde sa vytvorí faktúra pre konkrétnu projektovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-114">A proforma invoice can also be created from the **Project Contract** details page, which creates the invoice for that specific project contract.</span></span> <span data-ttu-id="8a4c2-115">Systém overí, či má projektová zmluva nevybavený termín **Pripravené na faktúru** datovaný pred dnešným dátumom.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-115">The system verifies that the project contract has a **Ready to Invoice** backlog that is dated before today's date.</span></span> <span data-ttu-id="8a4c2-116">Z týchto zmlúv systém vytvára koncepty zálohových faktúr na základe počtu zákazníkov v každom riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="8a4c2-117">Po vytvorení samostatnej zálohovej faktúry sa otvorí stránka **Faktúra**.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="8a4c2-118">Ak je pre túto projektovú zmluvu vytvorených viac faktúr, tak sa otvorí stránka so zoznamom **Faktúry** , kde sa zobrazia všetky vytvorené faktúry.</span><span class="sxs-lookup"><span data-stu-id="8a4c2-118">If there are multiple invoices created for that project contract, then the **Invoices** list page opens to show all of the created invoices.</span></span>
