---
title: Predvolené hodnoty finančnej dimenzie
description: Táto téma poskytuje informácie o tom, ako nastaviť predvolené hodnoty finančnej dimenzie.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: aa6771ba5346fd4133b82c3e670badfa7655299f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131902"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="a1532-103">Predvolené hodnoty finančnej dimenzie</span><span class="sxs-lookup"><span data-stu-id="a1532-103">Financial dimension defaults</span></span>

<span data-ttu-id="a1532-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="a1532-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a1532-105">Dynamics 365 Project Operations používa rámec [Finančné dimenzie](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) v Dynamics 365 Finance na poskytnutie ďalších prehľadov o transakciách v hlavnej a vedľajšej účtovnej knihe projektu.</span><span class="sxs-lookup"><span data-stu-id="a1532-105">Dynamics 365 Project Operations uses the [Financial dimensions](https://docs.microsoft.com/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="a1532-106">Predvolené finančné dimenzie je možné nastaviť na zákazníka, zdroj financovania projektu, medzník, riadok projektovej zmluvy alebo projekt.</span><span class="sxs-lookup"><span data-stu-id="a1532-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="a1532-107">Definovanie predvolených finančných dimenzií pre zákazníka</span><span class="sxs-lookup"><span data-stu-id="a1532-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="a1532-108">Predvolené hodnoty dimenzií zákazníka sú špecifikované v časti Financie.</span><span class="sxs-lookup"><span data-stu-id="a1532-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="a1532-109">Na nastavenie predvolených dimenzií vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="a1532-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="a1532-110">Prejdite do **Pohľadávky** > **Zákazníci** > **Všetci zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="a1532-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="a1532-111">Na stránke **Zákazníci** na karte **Finančné dimenzie** nastavte hodnoty finančnej dimenzie pre konkrétneho zákazníka.</span><span class="sxs-lookup"><span data-stu-id="a1532-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="a1532-112">Definovanie predvolených finančných dimenzií pre projektové zmluvy</span><span class="sxs-lookup"><span data-stu-id="a1532-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="a1532-113">Projektové zmluvy sa vytvárajú a udržiavajú v Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="a1532-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="a1532-114">Účtovné atribúty pre projektové zmluvy sú stanovené v module **Projektový manažment a účtovníctvo** vo Financie.</span><span class="sxs-lookup"><span data-stu-id="a1532-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="a1532-115">Stanovenie finančných dimenzií pre zdroj financovania projektu</span><span class="sxs-lookup"><span data-stu-id="a1532-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="a1532-116">Prejdite do časti **Projektový manažment a účtovníctvo** > **Projekty** > **Projektové zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="a1532-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="a1532-117">Vyberte záznam, ktorý chcete aktualizovať, a na karte **Projektová zmluva** vyberte **Zobraziť predvolené účtovníctvo**.</span><span class="sxs-lookup"><span data-stu-id="a1532-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a1532-118">Rozbaľte **Súvisiace informácie** a vyberte kartu **Zdroje financovania**.</span><span class="sxs-lookup"><span data-stu-id="a1532-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="a1532-119">Nastavte predvolené hodnoty finančnej dimenzie.</span><span class="sxs-lookup"><span data-stu-id="a1532-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="a1532-120">Všimnite si, že finančné dimenzie sa predvolene získavajú z obchodného vzťahu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="a1532-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="a1532-121">Stanovenie finančných dimenzií pre riadok projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="a1532-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="a1532-122">Prejdite do časti **Projektový manažment a účtovníctvo** > **Projekty** > **Projektové zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="a1532-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="a1532-123">Vyberte záznam, ktorý chcete aktualizovať, a na karte **Projektová zmluva** vyberte **Zobraziť predvolené účtovníctvo**.</span><span class="sxs-lookup"><span data-stu-id="a1532-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a1532-124">Rozbaľte **Súvisiace informácie** a vyberte kartu **Riadky zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="a1532-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="a1532-125">Nastavte predvolené hodnoty finančnej dimenzie.</span><span class="sxs-lookup"><span data-stu-id="a1532-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="a1532-126">Predvolené hodnoty finančnej dimenzie sú platné a je možné ich použiť iba pri riadkoch zmluvy s pevnou cenou (medzníkom).</span><span class="sxs-lookup"><span data-stu-id="a1532-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="a1532-127">Tieto predvolené hodnoty sa používajú v súvisiacich transakciách projektu na účte a na riadkoch faktúr.</span><span class="sxs-lookup"><span data-stu-id="a1532-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="a1532-128">Definovanie predvolených finančných dimenzií pre projekty</span><span class="sxs-lookup"><span data-stu-id="a1532-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="a1532-129">Projekty sa vytvárajú a udržiavajú v CDS.</span><span class="sxs-lookup"><span data-stu-id="a1532-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="a1532-130">Účtovné atribúty pre projekty sú stanovené v module **Projektový manažment a účtovníctvo** vo Financie.</span><span class="sxs-lookup"><span data-stu-id="a1532-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="a1532-131">Prejdite do časti **Riadenie projektu a účtovníctvo** > **Projekty** > **Všetky projekty**.</span><span class="sxs-lookup"><span data-stu-id="a1532-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="a1532-132">Vyberte záznam, ktorý chcete aktualizovať, a na karte **Projekt** vyberte **Zobraziť predvolené účtovníctvo**.</span><span class="sxs-lookup"><span data-stu-id="a1532-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="a1532-133">Rozbaľte **Súvisiace informácie** a vyberte kartu **Nastavenie**.</span><span class="sxs-lookup"><span data-stu-id="a1532-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="a1532-134">Nastavte predvolené hodnoty finančnej dimenzie.</span><span class="sxs-lookup"><span data-stu-id="a1532-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="a1532-135">Všimnite si, že finančné dimenzie sa predvolene získavajú z obchodného vzťahu zákazníka.</span><span class="sxs-lookup"><span data-stu-id="a1532-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="a1532-136">Ak je projekt spojený s riadkom zmluvy s viacerými zmluvnými zákazníkmi projektu, primárny zákazník sa použije na predvolené finančné dimenzie.</span><span class="sxs-lookup"><span data-stu-id="a1532-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="a1532-137">Predvolené finančné dimenzie projektu sa používajú na nastavenie predvolených hodnôt záznamov v účtovnom denníku pre časové, nákladové a poplatkové transakcie v **Denníku integrácie Project Operations** a na súvisiacich riadkoch projektových faktúr.</span><span class="sxs-lookup"><span data-stu-id="a1532-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>