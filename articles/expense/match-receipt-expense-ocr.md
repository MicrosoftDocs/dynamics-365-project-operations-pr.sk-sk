---
title: Priradenie potvrdenia k výdavku pomocou optického rozpoznávania znakov (OCR)
description: Táto téma poskytuje informácie o spracovaní účteniek optickým rozpoznávaním znakov (OCR).
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
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897020"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="9a5f5-103">Priradenie potvrdenia k výdavku pomocou optického rozpoznávania znakov (OCR)</span><span class="sxs-lookup"><span data-stu-id="9a5f5-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="9a5f5-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="9a5f5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9a5f5-105">Zadávanie výdavkov bolo vylepšený zavedením spracovaním účteniek optickým rozpoznávaním znakov (OCR).</span><span class="sxs-lookup"><span data-stu-id="9a5f5-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="9a5f5-106">Táto funkcia je navrhnutá tak, aby zlepšila používateľskú skúsenosť pri vytváraní výkazov výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="9a5f5-107">Kľúčové funkcie</span><span class="sxs-lookup"><span data-stu-id="9a5f5-107">Key features</span></span>

- <span data-ttu-id="9a5f5-108">Systém z účtenky vyberie meno obchodníka, dátum a celkovú sumu.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="9a5f5-109">Systém sa pokúsi priradiť nepripojené účtenky k nepripojeným transakciám výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="9a5f5-110">Z účteniek môžete vytvoriť ručne zadané transakcie výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="9a5f5-111">Pripojenie účteniek k výkazu výdavkov</span><span class="sxs-lookup"><span data-stu-id="9a5f5-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="9a5f5-112">Ak chcete pri vytváraní výkazu výdavkov automaticky pripojiť účtenky, ktoré zahŕňajú transakcie kreditnou kartou, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="9a5f5-113">Otvorte pracovný priestor **Správa výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="9a5f5-114">Na karte **Účtenky** overte, či existujú nepripojené účtenky.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="9a5f5-115">Môžete tiež nahrať účtenky na karte **Účtenky**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="9a5f5-116">Na karte **Výdavky** overte, či existujú nepripojené výdavky.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="9a5f5-117">Spravidla tieto výdavky importuje správca výdavkov od vydavateľa kreditnej karty.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="9a5f5-118">Vyberte **Nový výkaz výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-118">Select **New expense report**.</span></span> <span data-ttu-id="9a5f5-119">Upozorňujeme, že pri vytváraní výkazu výdavkov môžete zahrnúť ako výdavky, tak aj účtenky.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="9a5f5-120">Ak pridáte výdavky aj účtenky, spustí sa automatické priraďovanie účteniek k výdavkom.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="9a5f5-121">Vytvorenie alebo spárovanie účteniek s výkazom výdavkov</span><span class="sxs-lookup"><span data-stu-id="9a5f5-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="9a5f5-122">Ak chcete vytvoriť výdavok alebo spárovať výdavok z účtenky, postupujte takto.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="9a5f5-123">Vo výkaze výdavkov, na karte **Príjmy**, pripojte účtenku výberom možnosti **Pridať účtenky**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="9a5f5-124">Pod nahraným obrázkom účtenky si všimnite možnosti **Vytvoriť** a **Spárovať**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="9a5f5-125">Vyberte **Vytvoriť** na vytvorenie ručne zadanej výdavkovej transakcie a vyplnenie hodnôt, ktoré sú načítané z účtenky.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="9a5f5-126">Ak vyberiete **Spárovať**, systém sa pokúsi spárovať existujúci výdavok s účtenkou.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="9a5f5-127">Inštalácia</span><span class="sxs-lookup"><span data-stu-id="9a5f5-127">Installation</span></span>

<span data-ttu-id="9a5f5-128">Ak chcete používať tieto pokročilé možnosti výdavkov, nainštalujte si doplnok Služba riadenia výdavkov pre Microsoft Dynamics 365 Finance a zapnite funkcie vo vašej inštancii.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="9a5f5-129">V Microsoft Dynamics Lifecycle Services (LCS) môžete pristupovať k doplnku z vášho projektu.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="9a5f5-130">Prihláste sa do LCS a otvorte požadované prostredie.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="9a5f5-131">Prejdite do časti **Všetky podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="9a5f5-132">Vyberte **Údržba** alebo prejdite nadol na rýchlu kartu **Doplnky prostredia**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="9a5f5-133">Vyberte **Nainštalovať nový doplnok**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="9a5f5-134">Vyberte **Služba riadenia výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="9a5f5-135">Postupujte podľa inštalačnej príručky a vyjadrite súhlas s obchodnými podmienkami.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="9a5f5-136">Vyberte **Nainštalovať**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-136">Select **Install**.</span></span>

<span data-ttu-id="9a5f5-137">V pracovnom priestore **Správa funkcií** zapnite nasledujúce funkcie:</span><span class="sxs-lookup"><span data-stu-id="9a5f5-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="9a5f5-138">Prepracované výkazy výdavkov</span><span class="sxs-lookup"><span data-stu-id="9a5f5-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="9a5f5-139">Automatické párovanie a vytváranie výdavkov z účtenky</span><span class="sxs-lookup"><span data-stu-id="9a5f5-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="9a5f5-140">Po zapnutí týchto funkcií prebehnú nasledujúce akcie:</span><span class="sxs-lookup"><span data-stu-id="9a5f5-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="9a5f5-141">Existujúci pracovný priestor **Riadenie výdavkov** sa nahradí novým pracovným priestorom.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="9a5f5-142">Pridá sa nové položka ponuky pre viditeľnosť poľa výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="9a5f5-143">Stále môžete otvoriť predchádzajúcu stránku **Výkazy výdavkov** tak, že prejdete na **Správa výdavkov> Moje výdavky > Výkazy výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="9a5f5-144">Pracovné postupy a akékoľvek schválenia vás stále dovedú na stránku s existujúcimi výkazmi výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="9a5f5-145">Účtenky budú spracované prostredníctvom Microsoft Azure Cognitive Services a metadáta budú extrahované a pridané.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="9a5f5-146">Je pridaná možnosť, ktorá vám umožní vytvoriť výkaz výdavkov, ktorý obsahuje spárované nepriradené účtenky.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="9a5f5-147">Možnosť, ktorá sa pridáva do výkazov výdavkov, vám umožňuje vytvoriť výdavkový riadok z účtenky alebo sa pokúsiť spárovať existujúcu účtenku s existujúcim výdavkovým riadkom.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="9a5f5-148">Najčastejšie otázky</span><span class="sxs-lookup"><span data-stu-id="9a5f5-148">Frequently asked questions</span></span>

<span data-ttu-id="9a5f5-149">**Používa spoločnosť Microsoft moje údaje pre svoje modely?**</span><span class="sxs-lookup"><span data-stu-id="9a5f5-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="9a5f5-150">Nie, spoločnosť Microsoft vytvorila všeobecný model strojového učenia pre svoju službu spracovania účteniek.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="9a5f5-151">Tento model nie je založený na účtenkách, ktoré nahráte.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="9a5f5-152">**Kde je táto funkcia k dispozícii a kde sa spracúva?**</span><span class="sxs-lookup"><span data-stu-id="9a5f5-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="9a5f5-153">Momentálne sú podporované USA.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="9a5f5-154">**Kam smerujú moje účtenky?**</span><span class="sxs-lookup"><span data-stu-id="9a5f5-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="9a5f5-155">Služba Finance kontaktuje Cognitive Services s cieľom získať údaje polí.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="9a5f5-156">Cognitive Services si počas spracovania ponechajú kópiu vašej účtenky až 24 hodín.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="9a5f5-157">Po dokončení spracovania Cognitive Services účtenku odstránia.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="9a5f5-158">Účtenky sú stále uložené v službe Finance.</span><span class="sxs-lookup"><span data-stu-id="9a5f5-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="9a5f5-159">Viac informácií nájdete v časti [Umožnite porozumieť účtenkám s novou funkciou rozpoznávania formulárov](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="9a5f5-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
