---
title: Nastavenie pracovných postupov pre správu výdavkov
description: Môžete nastaviť proces pracovného postupu na kontrolu a schválenie cestovných a výdavkových dokladov.
author: ShylaThompson
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4070b4fb5109464abdabbce971688fb881dfcf2c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005135"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="eb962-103">Nastavenie pracovných postupov pre správu výdavkov</span><span class="sxs-lookup"><span data-stu-id="eb962-103">Set up Expense management workflows</span></span>

<span data-ttu-id="eb962-104">Môžete nastaviť proces pracovného postupu, ktorý sa používa na kontrolu a schválenie cestovných a výdavkových dokladov.</span><span class="sxs-lookup"><span data-stu-id="eb962-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="eb962-105">Medzi dokumenty, pre ktoré je možné definovať pracovné toky, patria výkazy výdavkov, cestovné požiadavky a žiadosti o hotovostné zálohy.</span><span class="sxs-lookup"><span data-stu-id="eb962-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="eb962-106">Pracovný tok predstavuje obchodný proces.</span><span class="sxs-lookup"><span data-stu-id="eb962-106">A workflow represents a business process.</span></span> <span data-ttu-id="eb962-107">Definuje, ako dokument prechádza systémom, a určuje, kto musí dokončiť úlohu alebo schváliť dokument.</span><span class="sxs-lookup"><span data-stu-id="eb962-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="eb962-108">Používanie systému pracovných postupov vo vašej organizácii má niekoľko výhod:</span><span class="sxs-lookup"><span data-stu-id="eb962-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="eb962-109">**Konzistentné procesy** – môžete definovať proces schvaľovania pre konkrétne dokumenty, ako sú napríklad požiadavky na nákup a výkazy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="eb962-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="eb962-110">Používanie systému pracovných postupov pomáha zabezpečiť, aby boli dokumenty spracovávané a schvaľované konzistentne a efektívne.</span><span class="sxs-lookup"><span data-stu-id="eb962-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="eb962-111">Viditeľnosť procesu – môžete sledovať stav, históriu a metriky výkonu konkrétnej inštancie pracovného postupu.</span><span class="sxs-lookup"><span data-stu-id="eb962-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="eb962-112">To vám pomôže určiť, či je potrebné vykonať zmeny v pracovnom postupe s cieľom zvýšiť efektivitu.</span><span class="sxs-lookup"><span data-stu-id="eb962-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="eb962-113">Centralizovaný pracovný zoznam – používatelia môžu zobraziť centralizovaný pracovný zoznam a zobraziť úlohy a schválenia pracovných postupov, ktoré sú im pridelené.</span><span class="sxs-lookup"><span data-stu-id="eb962-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="eb962-114">**Typy pracovných postupov, ktoré môžete vytvoriť**</span><span class="sxs-lookup"><span data-stu-id="eb962-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="eb962-115">V nasledujúcej tabuľke sú uvedené typy pracovných postupov, ktoré môžete vytvoriť v časti **Výdavky**.</span><span class="sxs-lookup"><span data-stu-id="eb962-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="eb962-116"><strong>Typ</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="eb962-117"><strong>Tento typ použite na</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="eb962-118"><strong>Výkaz výdavkov</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="eb962-119">Vytvorenie pracovných postupov schválenia pre výkazy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="eb962-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="eb962-120"><strong>Automatické zaúčtovanie výkazov výdavkov</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="eb962-121">Vytvorenie pracovných postupov automatického zaúčtovania pre výkazy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="eb962-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="eb962-122"><strong>Položka riadka výdavku</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="eb962-123">Vytvorenie pracovných postupov schválenia pre riadkové položky vo výkaze výdavkov.</span><span class="sxs-lookup"><span data-stu-id="eb962-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="eb962-124"><strong>Automatické zaúčtovanie položky riadka výdavku</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="eb962-125">Vytvorenie pracovných postupov automatického zaúčtovania pre riadkové položky vo výkaze výdavkov.</span><span class="sxs-lookup"><span data-stu-id="eb962-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="eb962-126"><strong>Cestovná žiadanka</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="eb962-127">Vytvorenie pracovných postupov schvaľovania pre cestovné požiadavky.</span><span class="sxs-lookup"><span data-stu-id="eb962-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="eb962-128"><strong>Požiadavka o platbu vopred</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="eb962-129">Vytvorte pracovné postupy schvaľovania pre žiadosti o hotovostné zálohy.</span><span class="sxs-lookup"><span data-stu-id="eb962-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="eb962-130"><strong>Vrátenie dane z pridanej hodnoty</strong></span><span class="sxs-lookup"><span data-stu-id="eb962-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="eb962-131">Vytvorte schvaľovacie pracovné postupy pre vrátenie dane z pridanej hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="eb962-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |



[!INCLUDE[footer-include](../includes/footer-banner.md)]