---
title: Viacero schvaľovateľov vo výkaze výdavkov
description: Táto téma poskytuje informácie o výkazoch výdavkov, ktoré si vyžadujú schválenie viacerými osobami.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084520"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="b90ac-103">Viacero schvaľovateľov vo výkaze výdavkov</span><span class="sxs-lookup"><span data-stu-id="b90ac-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b90ac-104">V závislosti od politík schvaľovania výdavkov vašej organizácie môže byť potrebné, aby výkaz výdavkov odovzdaný zamestnancom schválila viac ako jedna osoba.</span><span class="sxs-lookup"><span data-stu-id="b90ac-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="b90ac-105">Keď nastavujete proces pracovného postupu na schválenie výkazu výdavkov, môžete pridať prvky pracovného postupu, ktoré zahŕňajú úlohy alebo kroky pre jedného alebo viacerých schvaľovateľov výkazov výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="b90ac-106">Môžete napríklad požadovať, aby všetky výkazy výdavkov schvaľoval najskôr manažér zamestnanca, ktorý správu predložil a potom koordinátor záväzkov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="b90ac-107">Ak sa rozhodnete vyžadovať viacerých schvaľovateľov výkazov výdavkov, môžete prvky pracovného postupu pridať niektorým z nasledujúcich spôsobov:</span><span class="sxs-lookup"><span data-stu-id="b90ac-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="b90ac-108">Pridajte jeden schvaľovací prvok, ktorý má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="b90ac-108">Add one approval element that has one step.</span></span> <span data-ttu-id="b90ac-109">Krok môže napríklad vyžadovať, aby bol výkaz výdavkov priradený k skupine používateľov a aby bol schválený 50 percentami členov skupiny používateľov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="b90ac-110">Pridajte jeden schvaľovací prvok, ktorý má viac krokov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="b90ac-111">Schvaľovací prvok môže mať napríklad nasledujúce kroky:</span><span class="sxs-lookup"><span data-stu-id="b90ac-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="b90ac-112">Vedúci zamestnanca, ktorý predložil výkaz výdavkov, ho schvaľuje.</span><span class="sxs-lookup"><span data-stu-id="b90ac-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="b90ac-113">Referent pre záväzky overuje účtenky a položky výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="b90ac-114">Vlastník rozpočtu schvaľuje výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="b90ac-115">Pridajte viac schvaľovacích prvkov, z ktorých každý má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="b90ac-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="b90ac-116">Môžete napríklad pridať samostatný schvaľovací prvok pre každý z nasledujúcich krokov:</span><span class="sxs-lookup"><span data-stu-id="b90ac-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="b90ac-117">Vedúci zamestnanca schvaľuje výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="b90ac-118">Vlastník rozpočtu schvaľuje výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b90ac-118">The budget owner approves the expense report.</span></span>