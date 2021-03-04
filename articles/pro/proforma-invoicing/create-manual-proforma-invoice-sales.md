---
title: Vytvorenie manuálnej faktúry pro forma – čiastočné
description: Táto téma poskytuje informácie o manuálnom vytváraní zálohovej faktúry v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764522"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="640f3-103">Vytvorenie manuálnej faktúry pro forma – čiastočné</span><span class="sxs-lookup"><span data-stu-id="640f3-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="640f3-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="640f3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="640f3-105">V Dynamics 365 Project Operations je možné podľa potreby vytvárať proforma faktúry ručne.</span><span class="sxs-lookup"><span data-stu-id="640f3-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="640f3-106">Zálohovú faktúru môžete vytvoriť manuálne na stránke so zoznamom **Projektové zmluvy** alebo na stránke s podrobnosťami **Projektová zmluva**.</span><span class="sxs-lookup"><span data-stu-id="640f3-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="640f3-107">Stránka so zoznamom projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="640f3-107">Project Contracts list page</span></span>

<span data-ttu-id="640f3-108">Na stránke so zoznamom **Projektové zmluvy** vyberte jednu alebo viac projektových zmlúv a vytvorte faktúry pre všetky vybrané záznamy.</span><span class="sxs-lookup"><span data-stu-id="640f3-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="640f3-109">Systém kontroluje, ktoré z vybraných projektových zmlúv majú nevybavené termíny **Pripravené na faktúru** datované pred dnešným dátumom.</span><span class="sxs-lookup"><span data-stu-id="640f3-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="640f3-110">Z týchto zmlúv systém vytvára koncepty zálohových faktúr.</span><span class="sxs-lookup"><span data-stu-id="640f3-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="640f3-111">Ak má projektová zmluva viac zákazníkov, môže byť pre každého zákazníka vytvorená jedna faktúra a pre každú projektovú zmluvu viac faktúr.</span><span class="sxs-lookup"><span data-stu-id="640f3-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="640f3-112">Všetky vytvorené faktúry pre projekt sú k dispozícii na stránke **Faktúra** v časti **Fakturácia** v oblasti **Predaj**.</span><span class="sxs-lookup"><span data-stu-id="640f3-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="640f3-113">Stránka s podrobnosťami o projektovej zmluve</span><span class="sxs-lookup"><span data-stu-id="640f3-113">Project Contract details page</span></span>

<span data-ttu-id="640f3-114">Proforma faktúra môže byť vytvorená aj na stránke s podrobnosťami **Zmluva o projekte**.</span><span class="sxs-lookup"><span data-stu-id="640f3-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="640f3-115">Systém overuje, ktoré z projektových zmlúv majú nevybavené termíny **Pripravené na faktúru** datované pred dnešným dátumom.</span><span class="sxs-lookup"><span data-stu-id="640f3-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="640f3-116">Z týchto zmlúv systém vytvára koncepty zálohových faktúr na základe počtu zákazníkov v každom riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="640f3-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="640f3-117">Po vytvorení samostatnej zálohovej faktúry sa otvorí stránka **Faktúra**.</span><span class="sxs-lookup"><span data-stu-id="640f3-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="640f3-118">Ak sa pre túto projektovú zmluvu vytvorí viac faktúr, otvorí sa stránka so zoznamom **Faktúry**, kde sa zobrazia všetky vytvorené faktúry.</span><span class="sxs-lookup"><span data-stu-id="640f3-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
