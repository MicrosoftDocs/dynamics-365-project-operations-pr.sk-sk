---
title: Nastavte pracovné postupy pre správu výdavkov
description: Môžete nastaviť proces pracovného postupu, ktorý sa používa na kontrolu a schválenie cestovných a výdavkových dokladov.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: db1bda71e18369550cd2d38fee1d0ac40e07555d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084391"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="b44a3-103">Nastavte pracovné postupy pre správu výdavkov</span><span class="sxs-lookup"><span data-stu-id="b44a3-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="b44a3-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="b44a3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b44a3-105">Môžete nastaviť proces pracovného postupu na kontrolu a schválenie cestovných a výdavkových dokladov.</span><span class="sxs-lookup"><span data-stu-id="b44a3-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="b44a3-106">Môžete definovať pracovné postupy pre výkazy výdavkov, cestovné požiadavky a žiadosti o hotovostné zálohy.</span><span class="sxs-lookup"><span data-stu-id="b44a3-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="b44a3-107">Pracovný postup predstavuje obchodný proces a definuje, ako dokument prechádza systémom.</span><span class="sxs-lookup"><span data-stu-id="b44a3-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="b44a3-108">Pracovný postup tiež označuje, kto musí dokončiť úlohu alebo schváliť dokument.</span><span class="sxs-lookup"><span data-stu-id="b44a3-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="b44a3-109">Používanie systému pracovných postupov vo vašej organizácii má niekoľko výhod:</span><span class="sxs-lookup"><span data-stu-id="b44a3-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="b44a3-110">**Konzistentné procesy** : Môžete definovať proces schvaľovania pre konkrétne dokumenty, ako sú napríklad požiadavky na nákup a výkazy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b44a3-110">**Consistent processes** : You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="b44a3-111">Používanie systému pracovných postupov pomáha zabezpečiť, aby boli dokumenty spracovávané a schvaľované konzistentne a efektívne.</span><span class="sxs-lookup"><span data-stu-id="b44a3-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="b44a3-112">**Viditeľnosť procesu** : Môžete sledovať stav, históriu a metriky výkonu konkrétnej inštancie pracovného postupu.</span><span class="sxs-lookup"><span data-stu-id="b44a3-112">**Process visibility** : You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="b44a3-113">To vám pomôže určiť, či je potrebné vykonať zmeny v pracovnom postupe s cieľom zvýšiť efektivitu.</span><span class="sxs-lookup"><span data-stu-id="b44a3-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="b44a3-114">**Centralizovaný pracovný zoznam** : Používatelia môžu zobraziť centralizovaný pracovný zoznam a zobraziť úlohy a schválenia pracovných postupov, ktoré sú im pridelené.</span><span class="sxs-lookup"><span data-stu-id="b44a3-114">**Centralized work list** : Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="b44a3-115">Typy pracovných postupov</span><span class="sxs-lookup"><span data-stu-id="b44a3-115">Workflow types</span></span>

<span data-ttu-id="b44a3-116">V nasledujúcej tabuľke sú uvedené typy pracovných postupov, ktoré môžete vytvoriť v **Správe výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="b44a3-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="b44a3-117"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="b44a3-118"><strong>Tento typ použite na</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="b44a3-119"><strong>Automatické schválenie výkazu výdavkov</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="b44a3-120">Vytvorenie pracovných postupov schválenia pre výkazy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b44a3-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="b44a3-121"><strong>Automatické zaúčtovanie výkazov výdavkov</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="b44a3-122">Vytvorenie pracovných postupov automatického zaúčtovania pre výkazy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b44a3-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="b44a3-123"><strong>Položka riadka výdavku</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="b44a3-124">Vytvorenie pracovných postupov schválenia pre riadkové položky vo výkaze výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b44a3-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="b44a3-125"><strong>Automatické zaúčtovanie položky riadka výdavku</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="b44a3-126">Vytvorenie pracovných postupov automatického zaúčtovania pre riadkové položky vo výkaze výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b44a3-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="b44a3-127"><strong>Cestovná žiadanka</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="b44a3-128">Vytvorenie pracovných postupov schvaľovania pre cestovné požiadavky.</span><span class="sxs-lookup"><span data-stu-id="b44a3-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="b44a3-129"><strong>Požiadavka o platbu vopred</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="b44a3-130">Vytvorte pracovné postupy schvaľovania pre žiadosti o hotovostné zálohy.</span><span class="sxs-lookup"><span data-stu-id="b44a3-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="b44a3-131"><strong>Vrátenie dane z pridanej hodnoty</strong></span><span class="sxs-lookup"><span data-stu-id="b44a3-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="b44a3-132">Vytvorte schvaľovacie pracovné postupy pre vrátenie dane z pridanej hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="b44a3-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
