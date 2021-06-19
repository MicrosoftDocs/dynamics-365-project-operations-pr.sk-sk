---
title: Množiny schválení
description: Táto téma poskytuje informácie o množine schválení, žiadostiach a podmnožinách týchto operácií.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116890"
---
# <a name="approval-sets"></a><span data-ttu-id="d88f9-103">Množiny schválení</span><span class="sxs-lookup"><span data-stu-id="d88f9-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d88f9-104">Množiny schválení zoskupujú žiadosti o schválenie do menších podmnožín operácií.</span><span class="sxs-lookup"><span data-stu-id="d88f9-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="d88f9-105">Toto zoskupenie umožňuje, aby projekt spracovával schválenia v správnom poradí, a umožňuje ich opakovanie a radenie.</span><span class="sxs-lookup"><span data-stu-id="d88f9-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="d88f9-106">Zoskupenie zvyšuje spoľahlivosť a sledovateľnosť spracovania schválení pri veľkom objeme schválení.</span><span class="sxs-lookup"><span data-stu-id="d88f9-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="d88f9-107">Množiny schválení označujú celkový stav spracovania ich súvisiacich záznamov.</span><span class="sxs-lookup"><span data-stu-id="d88f9-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="d88f9-108">Keď sa záznam o schválení spracuje pomocou množiny schválení, presunie sa zo stavu **Odoslané** do stavu **Schválené** a odpojí sa z množiny schválení.</span><span class="sxs-lookup"><span data-stu-id="d88f9-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="d88f9-109">Ak záznam po odoslaní na schválenie zlyhá, zostane v stave **Odoslané** a množina schválení sa označí za neúspešnú.</span><span class="sxs-lookup"><span data-stu-id="d88f9-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="d88f9-110">Množina schválení zaznamená chybové hlásenie o neúspechu.</span><span class="sxs-lookup"><span data-stu-id="d88f9-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="d88f9-111">Spracúvanie schválení a množín schválení</span><span class="sxs-lookup"><span data-stu-id="d88f9-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="d88f9-112">Schválenia, ktoré sú zaradené do frontu na spracovanie, možno vidieť v zobrazení **Spracúvanie schválení**.</span><span class="sxs-lookup"><span data-stu-id="d88f9-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="d88f9-113">Systém sa pokúsi niekoľkokrát asynchrónne spracovať všetky záznamy vrátane opakovaného pokusu o schválenie, ak predchádzajúce pokusy zlyhali.</span><span class="sxs-lookup"><span data-stu-id="d88f9-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="d88f9-114">Pole **Životnosť množiny schválení** zaznamenáva počet pokusov, ktoré zostávajú na spracovanie množiny, kým bude označená ako neúspešná.</span><span class="sxs-lookup"><span data-stu-id="d88f9-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="d88f9-115">Neúspešné schválenia a množiny schválení</span><span class="sxs-lookup"><span data-stu-id="d88f9-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="d88f9-116">Zobrazenie **Neúspešné schválenia** obsahuje zoznam všetkých schválení, ktoré si vyžadujú zásah používateľa.</span><span class="sxs-lookup"><span data-stu-id="d88f9-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="d88f9-117">Otvorte príslušné protokoly o množinách schválení, aby ste určili príčinu zlyhania.</span><span class="sxs-lookup"><span data-stu-id="d88f9-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="d88f9-118">Výberom možnosti **Skúsiť znova** zvýšite životnosť množiny schválení, presuniete množinu schválení späť do stavu **Spracováva sa** a pokúsite sa o spracovanie zostávajúcich záznamov.</span><span class="sxs-lookup"><span data-stu-id="d88f9-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="d88f9-119">Konfigurácia množín schválení</span><span class="sxs-lookup"><span data-stu-id="d88f9-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="d88f9-120">Povolenie funkcie Množiny schválení</span><span class="sxs-lookup"><span data-stu-id="d88f9-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="d88f9-121">Skôr než povolíte funkciu Množiny schválení, skontrolujte, či sa v súčasnosti nespracovávajú žiadne schválenia.</span><span class="sxs-lookup"><span data-stu-id="d88f9-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="d88f9-122">Prejdite na stránku **Parametre projektu** a vyberte možnosť **Ovládací prvok funkcie** > **Povoliť moderné schválenia**.</span><span class="sxs-lookup"><span data-stu-id="d88f9-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="d88f9-123">Vypnutie funkcie Množiny schválení</span><span class="sxs-lookup"><span data-stu-id="d88f9-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="d88f9-124">Skôr než vypnete funkciu Množiny schválení, skontrolujte, či sa v súčasnosti nespracovávajú žiadne schválenia.</span><span class="sxs-lookup"><span data-stu-id="d88f9-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="d88f9-125">Prejdite na stránku **Parametre projektu** a vyberte možnosť **Ovládací prvok funkcie** > **Zakázať moderné schválenia**.</span><span class="sxs-lookup"><span data-stu-id="d88f9-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="d88f9-126">Konfigurácia asynchrónnej hranice</span><span class="sxs-lookup"><span data-stu-id="d88f9-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="d88f9-127">Keď sa vytvoria množiny schválení, spracovanie sa presunie do pozadia, keď zvolený počet záznamov na schválenie prekročí stanovenú hranicu.</span><span class="sxs-lookup"><span data-stu-id="d88f9-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="d88f9-128">Pomocou poľa **Asynchrónna hranica** nakonfigurujte, kedy sa má spracovanie schválenia spustiť synchrónne alebo asynchrónne.</span><span class="sxs-lookup"><span data-stu-id="d88f9-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="d88f9-129">Platné hodnoty sú:</span><span class="sxs-lookup"><span data-stu-id="d88f9-129">Valid values are:</span></span>

  - <span data-ttu-id="d88f9-130">Nula: Všetky žiadosti by sa mali spracovávať asynchrónne.</span><span class="sxs-lookup"><span data-stu-id="d88f9-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="d88f9-131">Čísla väčšie ako nula: Schválenia sa spracovávajú asynchrónne iba v prípade, že zadaný počet schválení prekročí túto hodnotu.</span><span class="sxs-lookup"><span data-stu-id="d88f9-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
