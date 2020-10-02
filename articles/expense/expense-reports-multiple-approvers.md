---
title: Výkazy výdavkov a viacerí schvaľovatelia
description: Táto téma poskytuje informácie o výkazoch výdavkov, ktoré si vyžadujú schválenie viac ako jednou osobou.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 818092dd631d07cc0a7d63c9eec51eeff4f67ffe
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897110"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="ec3f5-103">Výkazy výdavkov a viacerí schvaľovatelia</span><span class="sxs-lookup"><span data-stu-id="ec3f5-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="ec3f5-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="ec3f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ec3f5-105">V závislosti od politík schvaľovania výdavkov vašej organizácie môže byť potrebné, aby odovzdaný výkaz výdavkov schválila viac ako jedna osoba.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="ec3f5-106">Keď nastavujete proces pracovného postupu na schválenie výkazu výdavkov, môžete pridať prvky pracovného postupu, ktoré zahŕňajú úlohy alebo kroky pre jedného alebo viacerých schvaľovateľov výkazov výdavkov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="ec3f5-107">Môžete napríklad požadovať, aby všetky výkazy výdavkov schvaľovali dve samostatné osoby, manažér zamestnanca, ktorý správu predložil, a koordinátor záväzkov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="ec3f5-108">Ak sa rozhodnete vyžadovať viacerých schvaľovateľov výkazov výdavkov, môžete prvky pracovného postupu pridať niektorým z nasledujúcich spôsobov:</span><span class="sxs-lookup"><span data-stu-id="ec3f5-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="ec3f5-109">Pridajte jeden schvaľovací prvok, ktorý má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-109">Add one approval element that has one step.</span></span> <span data-ttu-id="ec3f5-110">Krok môže napríklad vyžadovať, aby bol výkaz výdavkov priradený k skupine používateľov a aby bol schválený 50 percentami členov skupiny používateľov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="ec3f5-111">Pridajte jeden schvaľovací prvok, ktorý má viac krokov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="ec3f5-112">Schvaľovací prvok môže mať napríklad nasledujúce kroky:</span><span class="sxs-lookup"><span data-stu-id="ec3f5-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="ec3f5-113">Vedúci zamestnanca, ktorý predložil výkaz výdavkov, ho schvaľuje.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="ec3f5-114">Referent pre záväzky overuje účtenky a položky výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="ec3f5-115">Vlastník rozpočtu schvaľuje výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="ec3f5-116">Pridajte viac schvaľovacích prvkov, z ktorých každý má jeden krok.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="ec3f5-117">Môžete napríklad pridať samostatný schvaľovací prvok pre každý z nasledujúcich krokov:</span><span class="sxs-lookup"><span data-stu-id="ec3f5-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="ec3f5-118">Vedúci zamestnanca schvaľuje výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="ec3f5-119">Vlastník rozpočtu schvaľuje výkaz výdavkov.</span><span class="sxs-lookup"><span data-stu-id="ec3f5-119">The budget owner approves the expense report.</span></span>
