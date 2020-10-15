---
title: Cestovné žiadanky
description: Táto téma poskytuje informácie o cestovných žiadankách.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 0261405abb9305d7f6abcde9cb90d9b184868580
ms.sourcegitcommit: a0f80d024a5d3112a39781815bd31d0c05ddaf6f
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/30/2020
ms.locfileid: "3906328"
---
# <a name="travel-requisitions"></a><span data-ttu-id="b3435-103">Cestovné žiadanky</span><span class="sxs-lookup"><span data-stu-id="b3435-103">Travel requisitions</span></span>

<span data-ttu-id="b3435-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="b3435-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b3435-105">V cestovnej žiadanke je uvedený zoznam výdavkov, ktoré vzniknú pri cestovaní.</span><span class="sxs-lookup"><span data-stu-id="b3435-105">A travel requisition lists the expenses that will be incurred for the purpose of travel.</span></span> <span data-ttu-id="b3435-106">Cestovná žiadanka sa predkladá na kontrolu a môže sa použiť na autorizáciu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b3435-106">A travel requisition is submitted for review and can be used to authorize expenses.</span></span>

<span data-ttu-id="b3435-107">Môže sa od vás vyžadovať predloženie cestovnej žiadanky ešte predtým, ako vám vzniknú akékoľvek výdavky, ktoré sa účtujú organizácii.</span><span class="sxs-lookup"><span data-stu-id="b3435-107">You may be required to submit a travel requisition before you incur any expense that is charged to the organization.</span></span> <span data-ttu-id="b3435-108">Táto požiadavka platí bez ohľadu na to, či účtujete výdavky na firemnú kreditnú kartu, míňate hotovosť, ktorú ste dostali z hotovostnej zálohy, alebo či vám vzniknú hotovostné výdavky, ktoré vám organizácia uhradí.</span><span class="sxs-lookup"><span data-stu-id="b3435-108">This requirement applies, regardless of whether you charge expenses to a corporate credit card, spend cash that you received from a cash advance, or incur out-of-pocket expenses that will be reimbursed by the organization.</span></span>

<span data-ttu-id="b3435-109">Cestovné žiadanky a politiky možno použiť na pomoc s riadením výdavkov organizácie.</span><span class="sxs-lookup"><span data-stu-id="b3435-109">Travel requisitions and policies can be used to help manage organization expenditures.</span></span> <span data-ttu-id="b3435-110">Napríklad, ak vaša organizácia pracuje na projekte s pevnou cenou, ktorý vyžaduje cestovanie, cestovné náklady členov projektového tímu musia zodpovedať rozpočtu projektu.</span><span class="sxs-lookup"><span data-stu-id="b3435-110">For example, if your organization is working on a fixed-price project that requires travel, the travel expenses of the project's team members must fit within the project budget.</span></span> <span data-ttu-id="b3435-111">Požadovaním schválenia cestovných výdavkov pred ich vznikom môže organizácia pomôcť zabezpečiť, aby projekt zostal v rámci rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="b3435-111">By requiring that travel expenses be approved before they are incurred, the organization can help make sure that the project remains within budget.</span></span>

## <a name="configuration"></a><span data-ttu-id="b3435-112">Konfigurácia</span><span class="sxs-lookup"><span data-stu-id="b3435-112">Configuration</span></span> 

<span data-ttu-id="b3435-113">Cestovné žiadanky je možné nakonfigurovať ako „povinné“ povolením parametra „Predbežná autorizácia cesty je povinná“ v parametroch správy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b3435-113">Travel Requisitions can be configured as "mandatory" by enabling the "Pre-authorization of travel is mandatory" parameter in Expense Management Parameters.</span></span> 

## <a name="create-and-submit-a-travel-requisition"></a><span data-ttu-id="b3435-114">Vytvorenie a odoslanie cestovnej žiadanky</span><span class="sxs-lookup"><span data-stu-id="b3435-114">Create and submit a travel requisition</span></span>

1. <span data-ttu-id="b3435-115">Prejdite do časti **Moje výdavky: cestovné žiadanky** a vyberte **Nová cestovná žiadanka**.</span><span class="sxs-lookup"><span data-stu-id="b3435-115">Go to **My expenses: Travel Requisition**, and select **New travel Requisition**.</span></span>
2. <span data-ttu-id="b3435-116">Zadajte účel a cieľ žiadanky.</span><span class="sxs-lookup"><span data-stu-id="b3435-116">Enter a purpose and destination for the requisition.</span></span>
3. <span data-ttu-id="b3435-117">V poli **Popis cesty** zadajte ďalšie informácie.</span><span class="sxs-lookup"><span data-stu-id="b3435-117">In the  **Travel description** field, enter any additional information.</span></span> 
4. <span data-ttu-id="b3435-118">Pre každý z očakávaných výdavkov, napríklad za letenku, stravu alebo prenájom auta, vytvorte riadkovú položku výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b3435-118">For each of the expected expenses, such as Flight, meals, or car rental, create an expense line item.</span></span> <span data-ttu-id="b3435-119">Uveďte predpokladaný dátum, odhadovanú sumu a menu pre každý výdavok.</span><span class="sxs-lookup"><span data-stu-id="b3435-119">Include the estimated date, estimated amount, and the currency for each expense.</span></span> 
5. <span data-ttu-id="b3435-120">Po dokončení pridávania očakávaných výdavkov vyberte možnosť **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="b3435-120">When you have finished adding the expected expenses, select **Save**.</span></span>
6. <span data-ttu-id="b3435-121">Keď ste pripravení na odoslanie cestovnej žiadanky, zvoľte **Pracovný tok** > **Odoslať**.</span><span class="sxs-lookup"><span data-stu-id="b3435-121">When you are ready to submit the travel requisition, select **Workflow** > **Submit**.</span></span>

<span data-ttu-id="b3435-122">Schválené cestovné žiadanky si môžete pozrieť v časti **Moje výdavky: cestovné žiadanky**.</span><span class="sxs-lookup"><span data-stu-id="b3435-122">You can view your approved travel requisitions under **My Expenses: Travel Requisition**.</span></span> 

## <a name="view-available-travel-requisitions"></a><span data-ttu-id="b3435-123">Zobrazenie dostupných cestovných žiadaniek</span><span class="sxs-lookup"><span data-stu-id="b3435-123">View available travel requisitions</span></span>

<span data-ttu-id="b3435-124">Všetky svoje cestovné žiadanky si môžete pozrieť v časti **Moje výdavky: cestovné žiadanky**.</span><span class="sxs-lookup"><span data-stu-id="b3435-124">You can view all of your travel requisitions under **My Expenses: Travel Requisitions**.</span></span>

## <a name="approve-travel-requisitions"></a><span data-ttu-id="b3435-125">Schválenie cestovných žiadaniek</span><span class="sxs-lookup"><span data-stu-id="b3435-125">Approve travel requisitions</span></span>

<span data-ttu-id="b3435-126">Vyberte cestovnú žiadanku, ktorú chcete schváliť, a potom vyberte **Pracovný postup** > **Schváliť**.</span><span class="sxs-lookup"><span data-stu-id="b3435-126">Select the travel requisition that you want to approve, and then select **Workflow** > **Approve**.</span></span>  

## <a name="submit-an-expense-report-using-your-approved-travel-requisition"></a><span data-ttu-id="b3435-127">Odošlite výkaz výdavkov pomocou svojej schválenej cestovnej žiadanky</span><span class="sxs-lookup"><span data-stu-id="b3435-127">Submit an expense report using your approved travel requisition</span></span>

1. <span data-ttu-id="b3435-128">Vytvorte nový výkaz výdavkov a v hlavičke výkazu výdavkov a zo zoznamu schválených cestovných žiadaniek vyberte **Mapovať na cestovnú žiadanku**.</span><span class="sxs-lookup"><span data-stu-id="b3435-128">Create a new expense report and in the expense report header, and from the list of approved travel requisitions, select **Map to Travel requisition**.</span></span>
2. <span data-ttu-id="b3435-129">Pole **Suma cestovnej žiadanky** sa automaticky aktualizuje v hlavičke výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b3435-129">The **Travel requisition amount** field is automatically updated in the expense report header.</span></span>
3. <span data-ttu-id="b3435-130">Pridajte všetky výdavky spojené s cestou.</span><span class="sxs-lookup"><span data-stu-id="b3435-130">Add each expense incurred for the trip.</span></span> <span data-ttu-id="b3435-131">Ak je povolené pole **Predbežne schválené** aktualizuje sa zosúladená a schválená suma pre konkrétnu kategóriu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="b3435-131">If the **Pre-authorized** field is enabled, the reconciled amount and authorized amount for the specific expense category will be updated.</span></span>

> [!NOTE]
> <span data-ttu-id="b3435-132">Keď mapujete výkaz výdavkov na schválenú cestovnú žiadanku, suma transakcie nemôže byť vyššia ako schválená suma.</span><span class="sxs-lookup"><span data-stu-id="b3435-132">When you map an expense report to an approved travel requisition, the transaction amount can't be greater than the authorized amount.</span></span> 
