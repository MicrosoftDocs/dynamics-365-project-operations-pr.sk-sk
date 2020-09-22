---
title: Zrušenie predtým schváleného času a položiek výdavkov
description: Táto téma poskytuje informácie o zrušení schváleného času projektu a nákladov transakcie.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755500"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="d05ba-103">Zrušenie predtým schváleného času a položiek výdavkov</span><span class="sxs-lookup"><span data-stu-id="d05ba-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d05ba-104">V najnovšej verzii Dynamics 365 Project Service Automation môžu schvaľovatelia zrušiť položky času alebo výdavkov, ktoré predtým schválili.</span><span class="sxs-lookup"><span data-stu-id="d05ba-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="d05ba-105">Zrušenie predtým schváleného času a výdavkových položiek</span><span class="sxs-lookup"><span data-stu-id="d05ba-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="d05ba-106">Ak chcete zrušiť položku času alebo výdavkov, ktoré ste predtým schválili, postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="d05ba-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="d05ba-107">Prejdite na **projekty** \> **moja práca** \> **schválenia**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="d05ba-108">Na stránke zoznam **schválení** zmeňte zobrazenie na **moje predchádzajúce schválenia**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="d05ba-109">Zobrazí sa zoznam položiek času a výdavkov, ktoré ste predtým schválili.</span><span class="sxs-lookup"><span data-stu-id="d05ba-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="d05ba-110">Vyberte jednu alebo viac položiek a potom vyberte položku **zrušiť schválenie**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="d05ba-111">Zobrazí sa upozorňujúce hlásenie.</span><span class="sxs-lookup"><span data-stu-id="d05ba-111">You receive a warning message.</span></span>
4. <span data-ttu-id="d05ba-112">Ak chcete zrušiť schválenie, stlačte tlačidlo **OK**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="d05ba-113">Pochopte vplyv zrušenia schválenia času alebo výdavkov</span><span class="sxs-lookup"><span data-stu-id="d05ba-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="d05ba-114">Ak sa schválenie zruší, existuje prevádzkový dopad aj finančný dopad.</span><span class="sxs-lookup"><span data-stu-id="d05ba-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="d05ba-115">Prevádzkový dopad</span><span class="sxs-lookup"><span data-stu-id="d05ba-115">Operational impact</span></span>

<span data-ttu-id="d05ba-116">Na strane operácie pri zrušení schválenia sa stav záznamu obnoví na **draft**a schválenie sa už nezobrazí v zobrazení **moje minulé schválenia**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="d05ba-117">Namiesto zrušených schválení sa zobrazí **Časové položky na schválenie** alebo **výdavkové položky na schválenie**, v závislosti od toho, či to bola časová položka alebo výdavková položka.</span><span class="sxs-lookup"><span data-stu-id="d05ba-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="d05ba-118">Okrem toho stav súvisiacich časových alebo výdavkových položiek sa zmení na **odoslané**, takže súvisiaca položka je v súlade so schváleniami, ktoré majú štatút **Draftu**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="d05ba-119">Ako schvaľovateľ môžete upraviť niektoré polia schválenia, ktoré majú stav **Draftu**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="d05ba-120">Tieto polia zahŕňajú **typ fakturácie** a **Fakturovateľné hodiny pre položky času**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="d05ba-121">Po zmene môžete záznam znova schváliť.</span><span class="sxs-lookup"><span data-stu-id="d05ba-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="d05ba-122">Prípadne môžete položku zamietnuť.</span><span class="sxs-lookup"><span data-stu-id="d05ba-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="d05ba-123">Ak odmietnete schválenie časovej položky, stav položky sa zmení na **vrátený**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="d05ba-124">Ak odmietnete schválenie výdavkovej položky, stav položky sa zmení na **zamietnutý**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="d05ba-125">Funkčne, sa vrátené a odmietnuté položky správajú rovnako ako položka, ktorá má stav **Draftu**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="d05ba-126">Člen projektového tímu môže buď vykonať požadované zmeny v položke a potom ho znova odoslať na schválenie, alebo úplne odstrániť položku.</span><span class="sxs-lookup"><span data-stu-id="d05ba-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="d05ba-127">Finančný vplyv</span><span class="sxs-lookup"><span data-stu-id="d05ba-127">Financial impact</span></span>

<span data-ttu-id="d05ba-128">Projekt je tiež ovplyvnený finančne, ak je schválenie zrušené.</span><span class="sxs-lookup"><span data-stu-id="d05ba-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="d05ba-129">Po prvé, zodpovedajúce skutočné hodnoty nákladov a predaja sa aktualizujú nasledujúcim spôsobom:</span><span class="sxs-lookup"><span data-stu-id="d05ba-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="d05ba-130">Stav úpravy je nastavený na **upravené**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="d05ba-131">Stav fakturácie je nastavený na **zrušené**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="d05ba-132">Ďalšie, storno položky sú vytvorené v tabuľke skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="d05ba-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="d05ba-133">Ak chcete vytvoriť storno položky, systém skopíruje hodnoty polí z pôvodných skutočných hodnôt.</span><span class="sxs-lookup"><span data-stu-id="d05ba-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="d05ba-134">Iba hodnoty, ktoré nie sú skopírované, sú hodnoty množstva.</span><span class="sxs-lookup"><span data-stu-id="d05ba-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="d05ba-135">Tieto hodnoty sa namiesto toho obrátili.</span><span class="sxs-lookup"><span data-stu-id="d05ba-135">These values are reversed instead.</span></span> <span data-ttu-id="d05ba-136">Obrátené skutočné hodnoty sú vytvorené pre skutočné hodnoty **nákladov**, aj pre **nefakturovaných predajov**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="d05ba-137">Pole **Stav nastavenia** v obrátenom stave je nastavené na **nenastaviteľné**a stav fakturácie je nastavený na **zrušené**.</span><span class="sxs-lookup"><span data-stu-id="d05ba-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="d05ba-138">Po týchto zmenách, množstvo, ktoré je zaznamenané ako vynaložené na projekt a nevybavené príjmy projektu predĺžia obchodný vzťah pre hodnoty, ktoré tieto skutočné údaje predstavujú.</span><span class="sxs-lookup"><span data-stu-id="d05ba-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
