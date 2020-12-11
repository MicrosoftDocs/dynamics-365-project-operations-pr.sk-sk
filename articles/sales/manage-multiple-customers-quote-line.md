---
title: Spravovanie viacerých zákazníkov v riadkoch cenových ponúk založených na projekte
description: Táto téma poskytuje informácie o tom, ako spravovať viacerých zákazníkov v riadkoch cenovej ponuky založenej na projekte.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 48336af0ad522e9d6aa68fa82ffa7921f09662d4
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118582"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a><span data-ttu-id="d16e7-103">Spravovanie viacerých zákazníkov v riadkoch cenových ponúk založených na projekte</span><span class="sxs-lookup"><span data-stu-id="d16e7-103">Manage multiple customers on project-based quote lines</span></span>

<span data-ttu-id="d16e7-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="d16e7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d16e7-105">Riadky cenových ponúk založených na projekte podporujú scenáre, kde každý riadok cenovej ponuky obsahuje zoznam zákazníkov, ktorí zaň platia.</span><span class="sxs-lookup"><span data-stu-id="d16e7-105">Project-based quote lines support scenarios where each quote line has a list of customers that are paying for it.</span></span> <span data-ttu-id="d16e7-106">Tento zoznam zákazníkov v riadku cenovej ponuky založenej na projekte môže byť rovnaký ako zoznam zákazníkov v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="d16e7-106">This list of customers on the project-based quote line can be same as the list of customers on the quote.</span></span> <span data-ttu-id="d16e7-107">Môžete tiež zmeniť zoznam zákazníkov, aby sa líšili.</span><span class="sxs-lookup"><span data-stu-id="d16e7-107">You can also change the list of customers to be different.</span></span> <span data-ttu-id="d16e7-108">Na vytvorenie prípadnej zmluvy o projekte po získaní cenovej ponuky projektu sa zoznam zákazníkov v riadku cenovej ponuky založenej na projekte skopíruje do zodpovedajúceho riadku zmluvy založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="d16e7-108">To create the eventual project contract when a project quote is won, the customer list on project-based quote line is copied to the corresponding project–based contract line.</span></span> <span data-ttu-id="d16e7-109">Zákazníci projektovej ponuky založenej na projekte sa skopírujú do projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="d16e7-109">Customers on the project-based quote are copied to the project contract.</span></span>

<span data-ttu-id="d16e7-110">Keď fakturujete prípadnú projektovú zmluvu, zoznam zákazníkov v riadku zmluvy na základe projektu má prednosť pred zoznamom na projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="d16e7-110">When you invoice the eventual project contract, the customer list on the project-based contract line takes priority over the list on the project contract.</span></span> <span data-ttu-id="d16e7-111">Zoznam zákazníkov na zmluve o projekte sa používa iba na predvolenie nových riadkov zmlúv o projekte.</span><span class="sxs-lookup"><span data-stu-id="d16e7-111">The customer list on the project contract is only used to default new project contract lines.</span></span>

<span data-ttu-id="d16e7-112">Všetky cenové ponuky zákazníkov na karte **Zákazníci** cenovej ponuky projektu budú predvolené ako riadok cenovej ponuky zákazníkov na všetkých nových riadkoch cenovej ponuky založenej na projekte vytvorených pre cenovú ponuku na projekt.</span><span class="sxs-lookup"><span data-stu-id="d16e7-112">All quote customers on the **Customers** tab of the project quote default as quote line customers on any new project-based quote lines created for the project quote.</span></span> <span data-ttu-id="d16e7-113">Žiadne existujúce riadky cenových ponúk založené na projekte nezdedia nové zákaznícke záznamy cenových ponúk vytvorené po nich.</span><span class="sxs-lookup"><span data-stu-id="d16e7-113">Any existing project-based quote lines don't inherit new quote customer records created after them.</span></span>

## <a name="create-update-or-delete-a-quote-line-customer-record"></a><span data-ttu-id="d16e7-114">Vytvorenie, aktualizovanie alebo odstránenie záznamu zákazníka riadka cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="d16e7-114">Create, update, or delete a quote line customer record</span></span>

<span data-ttu-id="d16e7-115">Na karte **Zákazníci riadka cenovej ponuky** na stránke **Riadok cenovej ponuky založenej na projekte** môžete vytvoriť, aktualizovať alebo vymazať zákazníka riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-115">You can create, update, or delete a quote line customer on the **Quote line customers** tab on the **Project-based quote line** page.</span></span> <span data-ttu-id="d16e7-116">Keď do riadka cenovej ponuky založenej na projekte pridáte nového zákazníka, zákazník sa pridá aj do celkovej ponuky ako zákazník ponuky s predvoleným percentom rozdelenia fakturácie na celkovú cenovú ponuku 0 %.</span><span class="sxs-lookup"><span data-stu-id="d16e7-116">When you add a new customer on the project-based quote line, the customer is also added to the overall quote as a quote customer, with a default billing split percentage on the overall quote of 0%.</span></span> <span data-ttu-id="d16e7-117">Percento rozdelenia fakturácie na celkovej cenovej ponuke sa skopíruje do nových riadkov cenovej ponuky a do prípadnej projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="d16e7-117">The billing split percentage on the overall quote is copied to new quote lines and to the eventual project contract.</span></span> <span data-ttu-id="d16e7-118">Keď však fakturujete zo zmluvy, použije sa percento rozdelenia fakturácie na úrovni riadka cenovej ponuky, nie percento rozdelenia fakturácie na celkovej úrovni zmluvy.</span><span class="sxs-lookup"><span data-stu-id="d16e7-118">However, when you invoice from the contract, the billing split percentage at the quote line level is used, not the billing split percentage at the overall contract level.</span></span> 

<span data-ttu-id="d16e7-119">V nasledujúcej tabuľke sú uvedené polia v zákazníckom zázname riadka cenovej ponuky z riadka cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="d16e7-119">The following table shows the fields on the quote line customer record of a project-based quote line.</span></span>

| <span data-ttu-id="d16e7-120">Pole</span><span class="sxs-lookup"><span data-stu-id="d16e7-120">Field</span></span> | <span data-ttu-id="d16e7-121">Oblasť</span><span class="sxs-lookup"><span data-stu-id="d16e7-121">Location</span></span> | <span data-ttu-id="d16e7-122">Popis a pokyny</span><span class="sxs-lookup"><span data-stu-id="d16e7-122">Description and guidance</span></span> | <span data-ttu-id="d16e7-123">Nadväzujúci vplyv</span><span class="sxs-lookup"><span data-stu-id="d16e7-123">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="d16e7-124">**Obchodný vzťah**</span><span class="sxs-lookup"><span data-stu-id="d16e7-124">**Account**</span></span> | <span data-ttu-id="d16e7-125">Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formulár na rýchle vytvorenie pre riadok zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-125">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="d16e7-126">Zobrazenie zoznamu všetkých aktívnych účtov.</span><span class="sxs-lookup"><span data-stu-id="d16e7-126">Lists all active accounts.</span></span> <span data-ttu-id="d16e7-127">Po vytvorení záznamu je toto pole uzamknuté.</span><span class="sxs-lookup"><span data-stu-id="d16e7-127">This field is locked after the record is created.</span></span> <span data-ttu-id="d16e7-128">Ak potrebujete aktualizovať pole, vymažte a znova vytvorte záznam.</span><span class="sxs-lookup"><span data-stu-id="d16e7-128">If you need to update the field, delete and recreate the record.</span></span> <span data-ttu-id="d16e7-129">Ak ste zaznamenali nejaké skutočné hodnoty, záznam nemôžete vymazať.</span><span class="sxs-lookup"><span data-stu-id="d16e7-129">If you recorded any actuals, you can't delete the record.</span></span> | <span data-ttu-id="d16e7-130">Keď si vyberiete obchodný vzťah z hlavného zoznamu obchodných vzťahov, ktorý chcete pridať, zákazník riadka cenovej ponuky sa tiež pridá ako zákazník cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-130">When you pick an account from the master list of accounts to add, the Quote line customer is also added as a Quote customer.</span></span> <span data-ttu-id="d16e7-131">Po získaní cenovej ponuky sa zákazníci riadka cenovej ponuky prekopírujú k zákazníkom riadka zmluvy o projekte.</span><span class="sxs-lookup"><span data-stu-id="d16e7-131">Quote line customers are copied to the project contract line customers when a quote is won.</span></span> |
| <span data-ttu-id="d16e7-132">**Percento rozdelenia fakturácie**</span><span class="sxs-lookup"><span data-stu-id="d16e7-132">**Billing split percent**</span></span> | <span data-ttu-id="d16e7-133">Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formulár na rýchle vytvorenie pre riadok zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-133">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="d16e7-134">Predstavuje percento každej nevyfakturovanej predajnej transakcie, ktorá sa pripíše tomuto zákazníkovi riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-134">Represents the percentage of each unbilled sales transaction that will be attributed to this quote line customer.</span></span> | <span data-ttu-id="d16e7-135">Skopírované k zákazníkom riadka zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="d16e7-135">Copied over to project contract line customers.</span></span> |
| <span data-ttu-id="d16e7-136">**Limit, ktorý sa nesmie prekročiť**</span><span class="sxs-lookup"><span data-stu-id="d16e7-136">**Not-to-exceed limit**</span></span> | <span data-ttu-id="d16e7-137">Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formulár na rýchle vytvorenie pre riadok zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-137">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="d16e7-138">Označuje, či existuje dohodnutý limit alebo strop celkovej sumy, ktorá bude fakturovaná tomuto zákazníkovi za tento riadok cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-138">Indicates whether there is a negotiated limit or cap to the overall amount that will be invoiced to this customer for this quoted line.</span></span> | <span data-ttu-id="d16e7-139">Skopírované do zákazníkov riadka zmluvy projektu po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-139">Copied over to project contract line customers when a quote is won.</span></span> |
| <span data-ttu-id="d16e7-140">**Vlastniaca spoločnosť**</span><span class="sxs-lookup"><span data-stu-id="d16e7-140">**Owning company**</span></span> | <span data-ttu-id="d16e7-141">Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formulár na rýchle vytvorenie pre riadok zákazníka cenovej ponuky,</span><span class="sxs-lookup"><span data-stu-id="d16e7-141">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer,</span></span> | <span data-ttu-id="d16e7-142">Právnická entita, pre ktorú je tento zákazník nastavený v module **Projektové riadenie a účtovníctvo**.</span><span class="sxs-lookup"><span data-stu-id="d16e7-142">The legal entity in which this customer is set up in the **Project management and accounting** module.</span></span> <span data-ttu-id="d16e7-143">Toto pole je iba na čítanie a je nastavené na spoločnosť, ktorá vlastní samotnú cenovú ponuku.</span><span class="sxs-lookup"><span data-stu-id="d16e7-143">This field is read-only and is set to the owning company of the quote itself.</span></span> <span data-ttu-id="d16e7-144">Zoznam zákazníkov, ktorých je možné pridať do poľa **Obchodný vzťah** je už filtrované do zoznamu z vlastniacej spoločnosti v module **Projektové riadenie a účtovníctvo** v Project Operations.</span><span class="sxs-lookup"><span data-stu-id="d16e7-144">The list of customers to add in the **Account** field is already filtered to the list from the owning company in the **Project management and accounting** module of Project Operations.</span></span> | <span data-ttu-id="d16e7-145">Vlastnícka spoločnosť sa rovná pojmu právnická entita.</span><span class="sxs-lookup"><span data-stu-id="d16e7-145">The owning company equates to the concept of legal entity.</span></span> <span data-ttu-id="d16e7-146">Všetky náklady a výnosy, ktoré vzniknú z tohto projektu, sa účtujú v hlavnej účtovnej knihe vlastniacej spoločnosti.</span><span class="sxs-lookup"><span data-stu-id="d16e7-146">All costs and revenue that accrue from this project are accounted in the General ledger of the owning company.</span></span> |
| <span data-ttu-id="d16e7-147">**Zaokrúhľuje**</span><span class="sxs-lookup"><span data-stu-id="d16e7-147">**Is rounding**</span></span> | <span data-ttu-id="d16e7-148">Upraviteľná mriežka na karte **Zákazníci riadka cenovej ponuky**, hlavný formulár a formulár na rýchle vytvorenie pre riadok zákazníka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-148">An editable grid on the **Quote line customers** tab, the main form, and the quick create form for a quote line customer.</span></span> | <span data-ttu-id="d16e7-149">Označuje, či je tento zákazník predvoleným zákazníkom zaokrúhľovania pre tento riadok cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="d16e7-149">Indicates whether this customer is a default rounding customer for this project-based quote line.</span></span> | <span data-ttu-id="d16e7-150">Skopírované do zmluvných zákazníkov projektu po získaní cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-150">Copied over to project contract customers when a quote is won.</span></span> |

## <a name="edit-billing-split-percentages"></a><span data-ttu-id="d16e7-151">Upraviť percentá rozdelenia fakturácie</span><span class="sxs-lookup"><span data-stu-id="d16e7-151">Edit billing split percentages</span></span>

<span data-ttu-id="d16e7-152">Percentuálne rozdelenie fakturácie môžete upraviť priamo.</span><span class="sxs-lookup"><span data-stu-id="d16e7-152">You can edit billing split percentages in-line.</span></span> <span data-ttu-id="d16e7-153">Ak percentá rozdelenia fakturácie nedosiahnu 100 %, dôjde k chybe.</span><span class="sxs-lookup"><span data-stu-id="d16e7-153">When the billing split percentages don't total 100%, an error occurs.</span></span> <span data-ttu-id="d16e7-154">Po úprave percentuálnych podielov rozdelenia fakturácie chybu obnovte obnovením stránky riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-154">After you edit the billing split percentages, refresh the quote line page to remove the error.</span></span>

<span data-ttu-id="d16e7-155">Pomocou akcie rovnomerného rozloženia vo vedľajšej mriežke zákazníkov riadka cenovej ponuky prideľte rozdelenie fakturácie všetkým zákazníkom riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="d16e7-155">Use the evenly distribute action on the quote line customers subgrid to allocate billing splits to all quote line customers.</span></span> <span data-ttu-id="d16e7-156">Ak existuje faktor zaokrúhľovania, pridá sa k zákazníkovi zaokrúhľovania.</span><span class="sxs-lookup"><span data-stu-id="d16e7-156">If there's a rounding factor, that will be added to the rounding customer.</span></span> <span data-ttu-id="d16e7-157">Jeden zo zákazníkov riadka cenovej ponuky je vždy označený ako zákazník zaokrúhľovania, čo znamená, že v zázname zákazníka riadka cenovej ponuky je príznak zaokrúhľovania nastavený na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="d16e7-157">One of the quote line customers is always tagged as the rounding customer, which means that quote line customer record has the rounding flag set to **Yes**.</span></span> 