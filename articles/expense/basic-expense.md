---
title: Záznam o výdavku (čiastočný)
description: Táto téma poskytuje informácie o tom, ako pracovať so záznamom o výdavku pri čiastočnom nasadení.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084248"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="a8c6a-103">Záznam o výdavku (čiastočný)</span><span class="sxs-lookup"><span data-stu-id="a8c6a-103">Expense entry (lite)</span></span>

<span data-ttu-id="a8c6a-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="a8c6a-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a8c6a-105">Základné alebo čiastočné riadenie výdavkov je schopnosť zaznamenávať jednoduché výdavky.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="a8c6a-106">Môžete zaúčtovať výdavky oproti projektu a potom ich schvaľovateľ projektu skontroluje a schváli.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="a8c6a-107">Ďalšie informácie o možnostiach výdavkov v Dynamics 365 Project Operations nájdete na stránke [Prehľad výdavkov](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a8c6a-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="a8c6a-108">Zachytenie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="a8c6a-108">Capture a basic expense</span></span>

<span data-ttu-id="a8c6a-109">Môžete zachytiť svoje výdavky, aby ste ich mohli predložiť schvaľovateľovi.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="a8c6a-110">Prejdite do **Výdavky** a vyberte **Nový**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-110">Go to **Expenses** , and select **New**.</span></span>
2. <span data-ttu-id="a8c6a-111">Na stránke **Nové výdavky** zadajte požadované informácie o výdavkoch a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="a8c6a-112">Predloženie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="a8c6a-112">Submit a basic expense</span></span>

<span data-ttu-id="a8c6a-113">Keď skončíte so zachytávaním všetkých svojich výdavkov a budete pripravení na ich schválenie, musíte ich predložiť.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="a8c6a-114">Prejdite do **Výdavky** a vyberte výdavok.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-114">Go to **Expenses** , and select an expense.</span></span> <span data-ttu-id="a8c6a-115">Alebo vyberte všetky výdavky pomocou začiarkavacieho políčka v hlavičke.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="a8c6a-116">Stlačte možnosť **Odoslať**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-116">Select **Submit**.</span></span> <span data-ttu-id="a8c6a-117">Systém spracuje vybrané položky a potom vytvorí žiadosti o schválenie výdavkov.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="a8c6a-118">Odvolanie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="a8c6a-118">Recall a basic expense</span></span>

<span data-ttu-id="a8c6a-119">Ak omylom predložíte výdavok, môžete ho odvolať.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="a8c6a-120">Čas, ktorý je potrebný na odvolanie záznamu o výdavkoch, závisí od fázy jeho schválenia.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="a8c6a-121">Ak schvaľovateľ ešte neschválil záznam, k odvolaniu môže dôjsť okamžite.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="a8c6a-122">Ak však už bol záznam schválený, požaduje sa od schvaľovateľa, aby schválil odvolanie a zrušil transakcie.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="a8c6a-123">Prejdite do **Výdavky** a potom v zozname výdavkov vyberte výdavok na odvolanie.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-123">Go to **Expenses** , and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="a8c6a-124">Vyberte položku **Odvolať**.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-124">Select **Recall**.</span></span> <span data-ttu-id="a8c6a-125">Ak záznam o výdavkoch ešte nebol schválený, systém ho okamžite odvolá.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="a8c6a-126">Ak bol záznam o výdavkoch už schválený, vytvorí sa požiadavka na odvolanie, aby sa schvaľovateľ informoval, že chcete výdavok zrušiť.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="a8c6a-127">Schvaľovateľ potom potvrdí, že je možné vykonať zrušenie a záznam sa vráti.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="a8c6a-128">Odstránenie základných výdavkov</span><span class="sxs-lookup"><span data-stu-id="a8c6a-128">Delete a basic expense</span></span>

<span data-ttu-id="a8c6a-129">Výdavky, ktoré ešte neboli odoslané, je možné odstrániť.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="a8c6a-130">Ak chcete odstrániť výdavok, ktorý už bol predložený, musíte ho najskôr odvolať.</span><span class="sxs-lookup"><span data-stu-id="a8c6a-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="a8c6a-131">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="a8c6a-131">See also</span></span>

- [<span data-ttu-id="a8c6a-132">Prehľad schválení</span><span class="sxs-lookup"><span data-stu-id="a8c6a-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
