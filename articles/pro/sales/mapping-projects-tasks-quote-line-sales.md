---
title: Mapovanie projektov a úloh na riadok cenovej ponuky založenej na projekte
description: Táto téma poskytuje informácie o tom, ako mapovať projekty a úlohy na riadok úlohy založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d714304f408050babae1a6ba74268979e0b6ea4b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272767"
---
# <a name="map-projects-and-tasks-to-a-project-based-quote-line"></a><span data-ttu-id="ba2ff-103">Mapovanie projektov a úloh na riadok cenovej ponuky založenej na projekte</span><span class="sxs-lookup"><span data-stu-id="ba2ff-103">Map projects and tasks to a project-based quote line</span></span>

<span data-ttu-id="ba2ff-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="ba2ff-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ba2ff-105">Na riadkoch cenových ponúk založených na projektoch môžete mapovať konkrétne úlohy projektu, ktorý je už priradený k riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-105">On project-based quote lines, you can map the specific tasks of a project that is already associated to a quote line.</span></span>

<span data-ttu-id="ba2ff-106">Keď mapujete úlohy na riadok cenovej ponuky, nasledujúce položky definované v riadku cenovej ponuky sa budú vzťahovať iba na tieto úlohy:</span><span class="sxs-lookup"><span data-stu-id="ba2ff-106">When you map tasks to a quote line, the following items you defined on the quote line will only apply to those tasks:</span></span>

- <span data-ttu-id="ba2ff-107">Spôsob fakturácie</span><span class="sxs-lookup"><span data-stu-id="ba2ff-107">Billing method</span></span>
- <span data-ttu-id="ba2ff-108">Možností účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="ba2ff-108">Chargeability options</span></span>
- <span data-ttu-id="ba2ff-109">Limity, ktoré sa nesmú prekročiť</span><span class="sxs-lookup"><span data-stu-id="ba2ff-109">Not-to-exceed limits</span></span>
- <span data-ttu-id="ba2ff-110">Zákazníci</span><span class="sxs-lookup"><span data-stu-id="ba2ff-110">Customers</span></span>

<span data-ttu-id="ba2ff-111">Napríklad, môžete mať projekt, kde jedna fáza bude mať pevnú cenu a všetky ostatné fázy budú založené na čase a materiáli.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-111">For example, you might have a project where one phase is fixed price and all the other phases are time and materials.</span></span> <span data-ttu-id="ba2ff-112">V takom prípade môžete prvú fázu a všetky jej podradené úlohy priradiť k riadku cenovej ponuky pre túto fázu s metódou fakturácie za pevnú cenu.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-112">In this case, you can associate the first phase, and all of its child tasks, to the quote line for that phase with a fixed price billing method.</span></span> <span data-ttu-id="ba2ff-113">Potom môžete všetky ostatné fázy priradiť k cenovej ponuke založenej na čase a materiáli.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-113">You can then associate all the other phases to the time and materials-based quote line.</span></span>

## <a name="associate-tasks-to-project-based-quote-lines"></a><span data-ttu-id="ba2ff-114">Priradenie úloh k riadkom cenových ponúk na základe projektu</span><span class="sxs-lookup"><span data-stu-id="ba2ff-114">Associate tasks to project-based quote lines</span></span>

<span data-ttu-id="ba2ff-115">Úlohy môžete priradiť k riadkom cenovej ponuky z nasledujúcich umiestnení:</span><span class="sxs-lookup"><span data-stu-id="ba2ff-115">You can associate tasks with quote lines from the following locations:</span></span>

- <span data-ttu-id="ba2ff-116">Stránka **Projekt** > karta **Fakturácia úloh** (optimálna)</span><span class="sxs-lookup"><span data-stu-id="ba2ff-116">**Project** page > **Task billing** tab (optimal)</span></span>
- <span data-ttu-id="ba2ff-117">Stránka **Riadok cenovej ponuky** > karta **Fakturovateľné úlohy**</span><span class="sxs-lookup"><span data-stu-id="ba2ff-117">**Quote Line** page > **Chargeable tasks** tab</span></span> 

### <a name="from-the-project-page"></a><span data-ttu-id="ba2ff-118">Zo stránky projektu</span><span class="sxs-lookup"><span data-stu-id="ba2ff-118">From the Project page</span></span>

<span data-ttu-id="ba2ff-119">Stránka **Projekt** poskytuje optimálne prostredie na priraďovanie úloh k riadkom cenových ponúk.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-119">The **Project** page provides the optimal experience for associating tasks to quote lines.</span></span> <span data-ttu-id="ba2ff-120">Túto stránku môžete použiť na výber viacerých úloh a na priradenie všetkých úloh, plus ich podradených úloh, k vybranému riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-120">You can use this page to select multiple tasks and associate all of them, plus their child tasks, to the selected quote line.</span></span>

1. <span data-ttu-id="ba2ff-121">Na karte **Všeobecné** riadku ponuky založenej na projekte skontrolujte, či je vyplnené pole **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-121">On the **General** tab of a project–based quote line, verify the **Project** field is filled out.</span></span>
2. <span data-ttu-id="ba2ff-122">V poli **Zahrnuté úlohy** vyberte **Iba vybrané úlohy**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-122">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="ba2ff-123">Uloženie riadka cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-123">Save the project-based quote line.</span></span> <span data-ttu-id="ba2ff-124">Keď sa obnoví formulár, zobrazí sa karta **Fakturovateľné úlohy**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-124">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="ba2ff-125">Na karte **Všeobecné** vyberte odkaz na projekt z poľa **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-125">On the **General** tab, select the link for the project from the **Project** field.</span></span>
5. <span data-ttu-id="ba2ff-126">Na stránke **Projekt** vyberte kartu **Fakturácia úloh**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-126">On the **Project** page, select the **Task billing** tab.</span></span>
6. <span data-ttu-id="ba2ff-127">V druhej mriežke, ktorá sa vzťahuje na nastavenie fakturácie špecifickej pre úlohu, vyberte jednu alebo viac úloh a potom vyberte **Priradiť riadky cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-127">In the second grid, which applies to task-specific billing setup, select one or more tasks and then select **Associate quote lines**.</span></span>
7. <span data-ttu-id="ba2ff-128">Na dialógovej stránke, ktorá sa zobrazí, vyberte riadok cenovej ponuky, ktorý v ponuke zobrazí riadky cenovej ponuky založené na projekte.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-128">In the dialog page that appears, select a quote line that displays project-based quote lines on the quote.</span></span>
8. <span data-ttu-id="ba2ff-129">V poli **Typ fakturácie** označte, či sú tieto úlohy účtovateľné alebo neúčtovateľné.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-129">In the **Billing type** field, indicate if these tasks are chargeable or non-chargeable.</span></span>
9. <span data-ttu-id="ba2ff-130">Začiarknutím políčka označte, či by priradenie malo obsahovať podradené úlohy vybratých úloh.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-130">Select the check box to indicate if the association should include child tasks of the selected tasks.</span></span> <span data-ttu-id="ba2ff-131">Začiarknutím tohto políčka sa podriadené úlohy vybraných úloh priradia k riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-131">Checking the box will associate the child tasks of the selected tasks to the quote line.</span></span>
10. <span data-ttu-id="ba2ff-132">Výberom možnosti **OK** zatvoríte dialógové okno.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-132">Select **OK** to close the dialog.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="ba2ff-133">Na stránke riadka cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="ba2ff-133">From the Quote line page</span></span>

<span data-ttu-id="ba2ff-134">Projektové úlohy môžete priradiť k riadkom cenovej ponuky na karte **Fakturovateľné úlohy** na stránke **Riadok cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-134">You can associate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

>[!NOTE]
><span data-ttu-id="ba2ff-135">Optimálne miesto na priradenie projektových úloh k riadkom cenových ponúk na karte **Fakturácia úloh** na stránke **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-135">The optimal place to associate project tasks to quote lines is on the **Task billing** tab on the **Project** page.</span></span> <span data-ttu-id="ba2ff-136">Ak priraďujete úlohy na karte **Fakturovateľné úlohy** na stránke **Riadok cenovej ponuky**, musíte každý projekt priradiť manuálne.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-136">If you associate tasks from the **Chargeable tasks** tab on **Quote line** page, you must manually associate each project.</span></span>

1. <span data-ttu-id="ba2ff-137">Na karte **Všeobecné** riadku ponuky založenej na projekte skontrolujte, či je v poli **Projekt** vybraný projekt.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-137">On the **General** tab of a project–based quote line, verify that there is a project selected in the **Project** field.</span></span>
2. <span data-ttu-id="ba2ff-138">V poli **Zahrnuté úlohy** vyberte **Iba vybrané úlohy**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-138">In the **Included tasks** field, select **Selected tasks only**.</span></span>
3. <span data-ttu-id="ba2ff-139">Uloženie riadka cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-139">Save the project-based quote line.</span></span> <span data-ttu-id="ba2ff-140">Keď sa obnoví formulár, zobrazí sa karta **Fakturovateľné úlohy**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-140">When the form refreshes, the **Chargeable tasks** tab displays.</span></span>
4. <span data-ttu-id="ba2ff-141">Na karte **Fakturovateľné úlohy** vyberte **Pridať úlohu riadka cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-141">On the **Chargeable tasks** tab, select **Add a quote line task**.</span></span>
5. <span data-ttu-id="ba2ff-142">Na stránke **Úloha riadka cenovej ponuky** v poli **Úlohy** vyberte úlohu a v poli **Typ fakturácie** vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-142">On the **Quote line task** page, in the **Tasks** field, select the task and in the **Billing type** field, select **Save**.</span></span> 
6. <span data-ttu-id="ba2ff-143">Zatvorí stránku.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-143">Close the page.</span></span> <span data-ttu-id="ba2ff-144">Vybraná úloha je teraz priradená k riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-144">The selected task is now associated to the quote line.</span></span>

## <a name="disassociate-tasks-from-projectbased-quote-lines"></a><span data-ttu-id="ba2ff-145">Zrušenie priradenia úloh v riadkoch cenových ponúk na základe projektu</span><span class="sxs-lookup"><span data-stu-id="ba2ff-145">Disassociate tasks from project–based quote lines</span></span>

### <a name="from-the-project-page"></a><span data-ttu-id="ba2ff-146">Zo stránky projektu</span><span class="sxs-lookup"><span data-stu-id="ba2ff-146">From the Project page</span></span>

<span data-ttu-id="ba2ff-147">Táto metóda poskytuje najoptimálnejšie prostredie na zrušenie priradenia úloh z riadkov cenových ponúk.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-147">This method provides the most optimal experience for disassociating tasks from quote lines.</span></span> <span data-ttu-id="ba2ff-148">Z vybratého riadku cenovej ponuky môžete vybrať viacero úloh a zrušiť priradenie všetkých z nich plus ich podradených úloh.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-148">You can select multiple tasks and disassociate all of the them, plus their child tasks, from the selected quote line.</span></span>

1. <span data-ttu-id="ba2ff-149">Na karte **Všeobecné** riadku ponuky založenej na projekte v poli **Projekt** vyberte prepojenie projektu.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-149">On the **General** tab of a project–based quote line, in the **Project** field, select the project link.</span></span>
2. <span data-ttu-id="ba2ff-150">Na stránke **Projekt** vyberte kartu **Fakturácia úloh**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-150">On the **Project** page, select the **Task billing** tab.</span></span>
3. <span data-ttu-id="ba2ff-151">V druhej mriežke, ktorá sa vzťahuje na nastavenie fakturácie špecifickej pre úlohu, vyberte jednu alebo viac úloh a potom vyberte **Zrušiť priradenie riadkov cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-151">In the second grid, which applies to task-specific billing setup, select one or more tasks, and then select **Disassociate quote lines**.</span></span>
4. <span data-ttu-id="ba2ff-152">Na zobrazenej dialógovej stránke vyberte riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-152">In the dialog page that appears, select a quote line.</span></span>
5. <span data-ttu-id="ba2ff-153">Začiarknutím políčka označte, či sa má priradenie odstrániť aj z podradených úloh vybratých úloh.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-153">Select the check box to indicate whether the association should also be removed from child tasks of the selected tasks.</span></span> <span data-ttu-id="ba2ff-154">Začiarknutím tohto políčka sa zruší aj priradenie podriadených úloh z riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-154">Checking the box will also disassociate the child tasks of the selected tasks to the quote line.</span></span>
6. <span data-ttu-id="ba2ff-155">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-155">Select **OK**.</span></span> <span data-ttu-id="ba2ff-156">Výstražné hlásenie správa informuje, že ak odstránite toto priradenie, všetky skutočné hodnoty predtým zaznamenané v úlohe môžu byť obrátené.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-156">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
7. <span data-ttu-id="ba2ff-157">Vyberte **OK**, ak chcete pokračovať a odstrániť priradenie medzi úlohou a riadkom cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-157">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

### <a name="from-the-quote-line-page"></a><span data-ttu-id="ba2ff-158">Na stránke riadka cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="ba2ff-158">From the Quote line page</span></span>

<span data-ttu-id="ba2ff-159">Priradenie projektových úloh môžete zrušiť v riadkoch cenovej ponuky na karte **Fakturovateľné úlohy** na stránke **Riadok cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-159">You can also disassociate project tasks to quote lines from the **Chargeable tasks** tab on **Quote line** page.</span></span>

1. <span data-ttu-id="ba2ff-160">Na karte **Fakturovateľné úlohy** vyberte **Odstrániť úlohu riadka cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-160">On the **Chargeable tasks** tab, select **Delete a quote line task**.</span></span>
2. <span data-ttu-id="ba2ff-161">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-161">Select **OK**.</span></span> <span data-ttu-id="ba2ff-162">Výstražné hlásenie správa informuje, že ak odstránite toto priradenie, všetky skutočné hodnoty predtým zaznamenané v úlohe môžu byť obrátené.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-162">A warning message informs you that if you remove this association, any actuals previously recorded on the task could be reversed.</span></span> 
3. <span data-ttu-id="ba2ff-163">Vyberte **OK**, ak chcete pokračovať a odstrániť priradenie medzi úlohou a riadkom cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-163">Select **OK** to continue and remove the association between the task and the project-based quote line.</span></span>

>[!NOTE]
> <span data-ttu-id="ba2ff-164">Tento postup neodstráni úlohu z projektu.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-164">This procedure doesn't delete the task from the project.</span></span> <span data-ttu-id="ba2ff-165">Odstráni iba priradenie úlohy z riadku cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="ba2ff-165">It only removes the task association from the project-based quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]