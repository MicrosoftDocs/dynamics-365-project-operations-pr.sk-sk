---
title: Spracovanie potvrdenia výdavkov
description: Táto téma poskytuje informácie o spracovaní účteniek optickým rozpoznávaním znakov (OCR). Táto funkcia je navrhnutá tak, aby zlepšila používateľskú skúsenosť pri vytváraní výkazov výdavkov v Microsoft Dynamics 365 Finance.
author: stsporen
manager: AnnBe
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: 57ef67412eb3c5795559e4f6d011e97c4d7a1338
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271822"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="3c532-104">Spracovanie potvrdenia výdavkov</span><span class="sxs-lookup"><span data-stu-id="3c532-104">Expense receipt processing</span></span>

<span data-ttu-id="3c532-105">Zadávanie výdavkov bolo vylepšený zavedením spracovaním účteniek optickým rozpoznávaním znakov (OCR).</span><span class="sxs-lookup"><span data-stu-id="3c532-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="3c532-106">Táto funkcia je navrhnutá tak, aby zlepšila používateľskú skúsenosť pri vytváraní výkazov výdavkov.</span><span class="sxs-lookup"><span data-stu-id="3c532-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="3c532-107">Kľúčové funkcie</span><span class="sxs-lookup"><span data-stu-id="3c532-107">Key features</span></span>

- <span data-ttu-id="3c532-108">Z účtenky sa vyberie meno obchodníka, dátum a celková suma.</span><span class="sxs-lookup"><span data-stu-id="3c532-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="3c532-109">Funkcia sa pokúsi priradiť nepripojené účtenky k nepripojeným transakciám výdavkov.</span><span class="sxs-lookup"><span data-stu-id="3c532-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="3c532-110">Z účteniek môžu používatelia vytvoriť ručne zadané transakcie výdavkov.</span><span class="sxs-lookup"><span data-stu-id="3c532-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="3c532-111">Príklady použitia</span><span class="sxs-lookup"><span data-stu-id="3c532-111">Usage examples</span></span>

<span data-ttu-id="3c532-112">Ak chcete pri vytváraní výkazu výdavkov automaticky pripojiť účtenky, ktoré zahŕňajú transakcie kreditnou kartou, postupujte nasledovne:</span><span class="sxs-lookup"><span data-stu-id="3c532-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="3c532-113">Otvorte pracovný priestor **Správa výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="3c532-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="3c532-114">Na karte **Účtenky** overte, či existujú nepripojené účtenky.</span><span class="sxs-lookup"><span data-stu-id="3c532-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="3c532-115">Môžete tiež nahrať účtenky na karte **Účtenky**.</span><span class="sxs-lookup"><span data-stu-id="3c532-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="3c532-116">Na karte **Výdavky** overte, či existujú nepripojené výdavky.</span><span class="sxs-lookup"><span data-stu-id="3c532-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="3c532-117">Spravidla tieto výdavky importuje správca výdavkov od vydavateľa kreditnej karty.</span><span class="sxs-lookup"><span data-stu-id="3c532-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="3c532-118">Vyberte **Nový výkaz výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="3c532-118">Select **New expense report**.</span></span> <span data-ttu-id="3c532-119">Upozorňujeme, že pri vytváraní výkazu výdavkov môžete zahrnúť ako výdavky, tak aj účtenky.</span><span class="sxs-lookup"><span data-stu-id="3c532-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="3c532-120">Ak pridáte výdavky aj účtenky, spustí sa automatické priraďovanie účteniek k výdavkom.</span><span class="sxs-lookup"><span data-stu-id="3c532-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="3c532-121">Ak chcete vytvoriť výdavok alebo spárovať výdavok z účtenky, postupujte nasledovne:</span><span class="sxs-lookup"><span data-stu-id="3c532-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="3c532-122">Vo výkaze výdavkov, na karte **Príjmy**, pripojte účtenku výberom možnosti **Pridať účtenky**.</span><span class="sxs-lookup"><span data-stu-id="3c532-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="3c532-123">Pod nahraným obrázkom účtenky si všimnite možnosti **Vytvoriť** a **Spárovať**.</span><span class="sxs-lookup"><span data-stu-id="3c532-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="3c532-124">Vyberte **Vytvoriť** na vytvorenie ručne zadanej výdavkovej transakcie a vyplnenie hodnôt, ktoré sú načítané z účtenky.</span><span class="sxs-lookup"><span data-stu-id="3c532-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="3c532-125">Ak vyberiete **Spárovať**, systém sa pokúsi spárovať existujúci výdavok s účtenkou.</span><span class="sxs-lookup"><span data-stu-id="3c532-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="3c532-126">Inštalácia</span><span class="sxs-lookup"><span data-stu-id="3c532-126">Installation</span></span>

<span data-ttu-id="3c532-127">Táto funkcia funguje v kombinácii s funkciou **Prepracované výkazy výdavkov**, ktorá pomáha zjednodušiť skúsenosti s výdavkami.</span><span class="sxs-lookup"><span data-stu-id="3c532-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="3c532-128">Táto funkcia je k dispozícii iba pre prostredia Tier 2+, ktorými sú Sandbox a Production.</span><span class="sxs-lookup"><span data-stu-id="3c532-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="3c532-129">Ak chcete používať tieto pokročilé možnosti výdavkov, nainštalujte si doplnok Služba riadenia výdavkov pre Microsoft Dynamics 365 Finance a zapnite funkcie vo vašej inštancii.</span><span class="sxs-lookup"><span data-stu-id="3c532-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="3c532-130">V Microsoft Dynamics Lifecycle Services (LCS) môžete pristupovať k doplnku z vášho projektu.</span><span class="sxs-lookup"><span data-stu-id="3c532-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="3c532-131">Prihláste sa do LCS a otvorte požadované prostredie.</span><span class="sxs-lookup"><span data-stu-id="3c532-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="3c532-132">Prejdite do časti **Všetky podrobnosti**.</span><span class="sxs-lookup"><span data-stu-id="3c532-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="3c532-133">Vyberte **Údržba** alebo prejdite nadol na rýchlu kartu **Doplnky prostredia**.</span><span class="sxs-lookup"><span data-stu-id="3c532-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="3c532-134">Vyberte **Nainštalovať nový doplnok**.</span><span class="sxs-lookup"><span data-stu-id="3c532-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="3c532-135">Vyberte **Služba riadenia výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="3c532-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="3c532-136">Postupujte podľa inštalačnej príručky a vyjadrite súhlas s obchodnými podmienkami.</span><span class="sxs-lookup"><span data-stu-id="3c532-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="3c532-137">Vyberte **Nainštalovať**.</span><span class="sxs-lookup"><span data-stu-id="3c532-137">Select **Install**.</span></span>

<span data-ttu-id="3c532-138">V pracovnom priestore **Správa funkcií** zapnite nasledujúce funkcie:</span><span class="sxs-lookup"><span data-stu-id="3c532-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="3c532-139">Prepracované výkazy výdavkov</span><span class="sxs-lookup"><span data-stu-id="3c532-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="3c532-140">Automatické párovanie a vytváranie výdavkov z účtenky</span><span class="sxs-lookup"><span data-stu-id="3c532-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="3c532-141">Po zapnutí týchto funkcií prebehnú nasledujúce akcie:</span><span class="sxs-lookup"><span data-stu-id="3c532-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="3c532-142">Existujúci pracovný priestor **Riadenie výdavkov** sa nahradí novým pracovným priestorom.</span><span class="sxs-lookup"><span data-stu-id="3c532-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="3c532-143">Pridá sa nové položka ponuky pre viditeľnosť poľa výdavkov.</span><span class="sxs-lookup"><span data-stu-id="3c532-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="3c532-144">Stále môžete otvoriť predchádzajúcu stránku **Výkazy výdavkov** tak, že prejdete na **Správa výdavkov> Moje výdavky > Výkazy výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="3c532-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="3c532-145">Pracovné postupy a akékoľvek schválenia vás stále dovedú na stránku s existujúcimi výkazmi výdavkov.</span><span class="sxs-lookup"><span data-stu-id="3c532-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="3c532-146">Účtenky budú spracované prostredníctvom Microsoft Azure Cognitive Services a metadáta budú extrahované a pridané.</span><span class="sxs-lookup"><span data-stu-id="3c532-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="3c532-147">Je pridaná možnosť, ktorá vám umožní vytvoriť výkaz výdavkov, ktorý obsahuje spárované nepriradené účtenky.</span><span class="sxs-lookup"><span data-stu-id="3c532-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="3c532-148">Možnosť, ktorá sa pridáva do výkazov výdavkov, vám umožňuje vytvoriť výdavkový riadok z účtenky alebo sa pokúsiť spárovať existujúcu účtenku s existujúcim výdavkovým riadkom.</span><span class="sxs-lookup"><span data-stu-id="3c532-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="3c532-149">Ďalšie informácie o funkcii nového zobrazenia prehľadov výdavkov nájdete v časti [Prepracované výkazy výdavkov](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="3c532-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="3c532-150">Najčastejšie otázky</span><span class="sxs-lookup"><span data-stu-id="3c532-150">Frequently asked questions</span></span>

<span data-ttu-id="3c532-151">**Používa spoločnosť Microsoft moje údaje pre svoje modely?**</span><span class="sxs-lookup"><span data-stu-id="3c532-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="3c532-152">Nie, spoločnosť Microsoft vytvorila všeobecný model strojového učenia pre svoju službu spracovania účteniek.</span><span class="sxs-lookup"><span data-stu-id="3c532-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="3c532-153">Tento model nie je založený na účtenkách, ktoré nahráte.</span><span class="sxs-lookup"><span data-stu-id="3c532-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="3c532-154">**Kde je táto funkcia k dispozícii a kde sa spracúva?**</span><span class="sxs-lookup"><span data-stu-id="3c532-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="3c532-155">Momentálne sú podporované USA.</span><span class="sxs-lookup"><span data-stu-id="3c532-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="3c532-156">**Kam smerujú moje účtenky?**</span><span class="sxs-lookup"><span data-stu-id="3c532-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="3c532-157">Služba Finance kontaktuje Cognitive Services s cieľom získať údaje polí.</span><span class="sxs-lookup"><span data-stu-id="3c532-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="3c532-158">Cognitive Services si počas spracovania ponechajú kópiu vašej účtenky až 24 hodín.</span><span class="sxs-lookup"><span data-stu-id="3c532-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="3c532-159">Po dokončení spracovania Cognitive Services účtenku odstránia.</span><span class="sxs-lookup"><span data-stu-id="3c532-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="3c532-160">Účtenky sú stále uložené v službe Finance.</span><span class="sxs-lookup"><span data-stu-id="3c532-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="3c532-161">Viac informácií nájdete v časti [Umožnite porozumieť účtenkám s novou funkciou rozpoznávania formulárov](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="3c532-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]