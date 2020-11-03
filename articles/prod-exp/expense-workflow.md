---
title: Pracovný postup riadenia výdavkov
description: Táto téma vysvetľuje, ako môžete používať systém pracovných tokov v aplikácii Microsoft Dynamics 365 Finance na nastavenie procesu kontroly výkazov výdavkov v správe výdavkov.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5207be92cb58d8ab2658096b3e0f3fc81d73d91e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084519"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="527fa-103">Pracovný postup riadenia výdavkov</span><span class="sxs-lookup"><span data-stu-id="527fa-103">Expense management workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="527fa-104">Systém pracovného toku môžete použiť na nastavenie procesu kontroly výkazov výdavkov v správe výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="527fa-105">Môžete nastaviť pracovný tok, ktorý pomocou nasledujúcich kritérií určuje, kto schvaľuje výkazy výdavkov:</span><span class="sxs-lookup"><span data-stu-id="527fa-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="527fa-106">Hierarchia vykazovania zamestnancov a preddefinované limity schválenia</span><span class="sxs-lookup"><span data-stu-id="527fa-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="527fa-107">Viacúrovňové schválenie, ktoré podporuje dočasných schvaľovateľov a konečného schvaľovateľa</span><span class="sxs-lookup"><span data-stu-id="527fa-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="527fa-108">Finančné rozmery a zodpovednosť za projekt</span><span class="sxs-lookup"><span data-stu-id="527fa-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="527fa-109">Priradenie konkrétnym používateľom alebo skupinám používateľov</span><span class="sxs-lookup"><span data-stu-id="527fa-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="527fa-110">Je možné vytvoriť schválenia pracovných postupov pre výkazy výdavkov, cestovné požiadavky, zálohy v hotovosti a vrátenie dane z pridanej hodnoty (DPH).</span><span class="sxs-lookup"><span data-stu-id="527fa-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="527fa-111">**Príklad**</span><span class="sxs-lookup"><span data-stu-id="527fa-111">**Example**</span></span>

<span data-ttu-id="527fa-112">Nasledujúci proces je príkladom pracovného toku správy výdavkov pre výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="527fa-113">Zamestnanec vytvorí a uloží výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="527fa-114">Zamestnanec predloží výkaz výdavkov na schválenie.</span><span class="sxs-lookup"><span data-stu-id="527fa-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="527fa-115">Schvaľovateľ je identifikovaný na základe pravidiel, ktoré boli definované pri nastavovaní pracovného toku.</span><span class="sxs-lookup"><span data-stu-id="527fa-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="527fa-116">Schvaľovateľ dostane oznámenie, že výkaz výdavkov je pripravený na schválenie.</span><span class="sxs-lookup"><span data-stu-id="527fa-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="527fa-117">Schvaľovateľ skontroluje výkaz výdavkov a overí, či sú splnené nasledujúce podmienky:</span><span class="sxs-lookup"><span data-stu-id="527fa-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="527fa-118">Výdavky neporušujú žiadne zásady týkajúce sa výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="527fa-119">Ak výdavok porušuje zásady, schvaľovateľ overí, či správa o výdavkoch obsahuje platné obchodné odôvodnenie.</span><span class="sxs-lookup"><span data-stu-id="527fa-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="527fa-120">Elektronické potvrdenky sú pripojené k výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="527fa-121">Schvaľovateľ schvaľuje výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="527fa-122">Výkaz výdavkov je priradený koordinátorovi záväzkov na zverejnenie.</span><span class="sxs-lookup"><span data-stu-id="527fa-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="527fa-123">Podľa toho, či je nakonfigurované automatické zverejňovanie, dôjde k jednému z nasledujúcich krokov:</span><span class="sxs-lookup"><span data-stu-id="527fa-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="527fa-124">Ak je nakonfigurované automatické zverejňovanie, výkaz výdavkov sa spracuje na platbu a aktualizuje sa stav výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="527fa-125">Ak automatické zverejňovanie nie je nakonfigurované, koordinátor záväzkov overí, či boli odoslané všetky pôvodné potvrdenky a či sú potvrdenia zarovnané s výdavkami v prehľade výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="527fa-126">Rovnako musia byť overené všetky daňové kódy, ktoré sú zadané vo výkaze výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="527fa-127">Po overení týchto požiadaviek sa zverejní výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="527fa-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="527fa-128">Po zverejnení výkazu výdavkov sa platba za výkaz výdavkov autorizuje a zamestnancovi preplatená suma.</span><span class="sxs-lookup"><span data-stu-id="527fa-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>
