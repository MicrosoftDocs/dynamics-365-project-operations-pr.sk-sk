---
title: Správa projektových cenníkov v projektových zmluvách
description: Táto téma poskytuje informácie o správe projektových cenníkov v projektových zmluvách.
author: rumant
manager: Annbe
ms.date: 10/27/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 2cfac6eda64d1d8e578115bba07942a7d786328f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278617"
---
# <a name="manage-project-price-lists-on-project-contracts"></a><span data-ttu-id="cc75f-103">Správa projektových cenníkov v projektových zmluvách</span><span class="sxs-lookup"><span data-stu-id="cc75f-103">Manage project price lists on project contracts</span></span>

<span data-ttu-id="cc75f-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="cc75f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cc75f-105">Projektové zmluvy v rámci Dynamics 365 Project Operations sú navrhnuté tak, aby podporovali viacdenné efektívne predajné cenníky v rámci zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cc75f-105">Project contracts in Dynamics 365 Project Operations are designed to support multiple date effective sales price lists on a contract.</span></span> <span data-ttu-id="cc75f-106">V aplikácii Project Operations existuje nová pridružená entita s názvom **Projektové cenníky**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-106">In Project Operations, there is a new associated entity called **Project Price Lists**.</span></span> <span data-ttu-id="cc75f-107">Táto entita má vzťah typu jeden k mnohým k projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="cc75f-107">This entity has a one-to-many relationship to a project contract.</span></span>

<span data-ttu-id="cc75f-108">Cenníky projektu sa používajú na ocenenie časových a výdavkových transakcií projektu.</span><span class="sxs-lookup"><span data-stu-id="cc75f-108">Project price lists are used to price time and expense transactions on a project.</span></span> <span data-ttu-id="cc75f-109">Ak má zmluva jeden alebo viac projektových cenníkov, tieto cenníky sa používajú na odhad ceny a času a výdavkov a skutočných údajov o projektoch, ktoré sú spojené so zákazkou prostredníctvom riadka zmluvy.</span><span class="sxs-lookup"><span data-stu-id="cc75f-109">When a contract has one or more project price lists, these price lists are used to price for time and expense estimates and actuals on projects that are associated to the contract through the contract line.</span></span>

<span data-ttu-id="cc75f-110">Ak v projektovej zmluve nie sú uvedené žiadne projektové cenníky, zobrazí sa varovná správa, že neexistujú žiadne projektové cenníky a vaše odhady, skutočná práca na projekte a náklady nebudú oceňované.</span><span class="sxs-lookup"><span data-stu-id="cc75f-110">When there are no project price lists on a project contract, you will see a warning message that there are no project price lists and your estimates, actual project work, and expenses will not be priced.</span></span> <span data-ttu-id="cc75f-111">Za predajné hodnoty sa nebude platiť žiadna cena.</span><span class="sxs-lookup"><span data-stu-id="cc75f-111">There will be no price for sales values.</span></span>

## <a name="associate-or-unassociate-a-project-price-list-on-a-project-contract"></a><span data-ttu-id="cc75f-112">Priradenie alebo zrušenie priradenia projektového cenníka k projektovej zmluve</span><span class="sxs-lookup"><span data-stu-id="cc75f-112">Associate or unassociate a project price list on a project contract</span></span>

### <a name="create-or-associate-a-specific-price-list-for-estimating-project-based-work-and-expenses"></a><span data-ttu-id="cc75f-113">Vytvorenie alebo priradenie konkrétneho cenníka pre odhad projektovej práce a výdavkov</span><span class="sxs-lookup"><span data-stu-id="cc75f-113">Create or associate a specific price list for estimating project-based work and expenses</span></span>

1. <span data-ttu-id="cc75f-114">Na projektovej zmluve vyberte kartu **Projektové cenníky**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-114">On the project contract, select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="cc75f-115">Vo vedľajšej mriežke vyberte **+ Pridať nový projektový cenník**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-115">In the subgrid, select **+ Add New Project Price List**.</span></span>
3. <span data-ttu-id="cc75f-116">Na jazdci **Rýchle vytvorenie** vyberte cenník.</span><span class="sxs-lookup"><span data-stu-id="cc75f-116">On the **Quick Create** slider, select a price list.</span></span> 

  <span data-ttu-id="cc75f-117">Rozbaľovací zoznam zobrazuje všetky cenníky, pre ktoré je nastavený kontext **Predaj**, kde sa mena v cenníku zhoduje s menou na zmluve.</span><span class="sxs-lookup"><span data-stu-id="cc75f-117">The drop-down list shows all price lists that have the context set to **Sales**, where the currency on the price list matches the currency on the contract.</span></span>
  
4. <span data-ttu-id="cc75f-118">Zadajte popis priradenia projektového cenníka, zvoľte **Uložiť** a potom zatvorte jazdec **Rýchle vytvorenie**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-118">Enter a description for the project price list association, select **Save**, and then close the **Quick Create** slider.</span></span>

   <span data-ttu-id="cc75f-119">Vytvorí sa priradenie cenníka projektu.</span><span class="sxs-lookup"><span data-stu-id="cc75f-119">A project price list association is created.</span></span>
   
5. <span data-ttu-id="cc75f-120">Opakovaním krokov 1 – 4 priraďte k projektovej zmluve viac ako jeden projektový cenník.</span><span class="sxs-lookup"><span data-stu-id="cc75f-120">Repeat steps 1-4 to associate more than one project price list to the project contract.</span></span> <span data-ttu-id="cc75f-121">Viac projektových cenníkov vytvorte iba vtedy, ak máte rozdielny dátum účinnosti pre každý z pridružených projektových cenníkov.</span><span class="sxs-lookup"><span data-stu-id="cc75f-121">Only create multiple project price lists if you have different date effectivity on each of the associated project price list.</span></span>

> [!NOTE]
> <span data-ttu-id="cc75f-122">Aplikácia Project Operations nepodporuje prekrývanie dátumovej účinnosti projektových cenníkov.</span><span class="sxs-lookup"><span data-stu-id="cc75f-122">Project Operations doesn't support overlapping the date effectivity of the project price lists.</span></span> <span data-ttu-id="cc75f-123">Ak existuje viac projektových cenníkov pre transakciu s daným dátumom, cena tejto transakcie bude predvolene nastavená na nulu.</span><span class="sxs-lookup"><span data-stu-id="cc75f-123">If there are multiple project prices lists for a transaction with a given date, the price on that transaction will be defaulted to zero.</span></span>

### <a name="remove-a-project-price-list-association"></a><span data-ttu-id="cc75f-124">Odstránenie priradenie projektového cenníka</span><span class="sxs-lookup"><span data-stu-id="cc75f-124">Remove a project price list association</span></span>

- <span data-ttu-id="cc75f-125">Vyberte projektový cenník a potom zvoľte na vedľajšej mriežke možnosť **Odstrániť projektový cenník zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-125">Select the project price list, and then select **Delete Contract Project Price List** on the subgrid.</span></span> 

  <span data-ttu-id="cc75f-126">Cenník sa odstráni z projektových cenníkov v zmluve.</span><span class="sxs-lookup"><span data-stu-id="cc75f-126">The price list is removed from the project price lists on the contract.</span></span> <span data-ttu-id="cc75f-127">Samotný cenník sa neodstráni.</span><span class="sxs-lookup"><span data-stu-id="cc75f-127">The price list itself will not be deleted.</span></span> <span data-ttu-id="cc75f-128">Odstráni sa iba priradenie k zmluve.</span><span class="sxs-lookup"><span data-stu-id="cc75f-128">Only the association to the contract will be deleted.</span></span>

## <a name="set-up-automatic-defaulting-of-project-price-lists-on-a-contract"></a><span data-ttu-id="cc75f-129">Nastavenie automatického predvolenia projektových cenníkov v zmluve</span><span class="sxs-lookup"><span data-stu-id="cc75f-129">Set up automatic defaulting of project price lists on a contract</span></span>

<span data-ttu-id="cc75f-130">Projektový cenník je možné nastaviť ako predvolený zoznam v projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="cc75f-130">A project price list can be set up as the default list on a project contract.</span></span> <span data-ttu-id="cc75f-131">Toto nastavenie môže pomôcť zabezpečiť, aby všetky zmluvy vo vašej organizácii vždy začínali štandardným cenníkom pre dané cenové obdobie.</span><span class="sxs-lookup"><span data-stu-id="cc75f-131">This setup can help ensure that all contracts in your organization always start with a standard price list for that price period.</span></span>

### <a name="set-up-the-organizational-default-for-project-price-lists"></a><span data-ttu-id="cc75f-132">Nastavenie predvolenej hodnoty organizácie pre projektové cenníky</span><span class="sxs-lookup"><span data-stu-id="cc75f-132">Set up the organizational default for project price lists</span></span>

1. <span data-ttu-id="cc75f-133">Prejdite do ponuky **Nastavenie** > **Všeobecné** a potom vyberte **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-133">Go to **Settings** > **General**, and then select **Parameters**.</span></span>
2. <span data-ttu-id="cc75f-134">Na stránke so zoznamom **Aktívne parametre** vyberte záznam a dvojitým kliknutím ho otvorte.</span><span class="sxs-lookup"><span data-stu-id="cc75f-134">In the **Active Parameters** list page, select and double-click the record to open it.</span></span> <span data-ttu-id="cc75f-135">Pri dvojitom kliknutí sa uistite, že neklikáte na hodnotu poľa, ktorá je hypertextovým odkazom.</span><span class="sxs-lookup"><span data-stu-id="cc75f-135">While double–clicking, make sure that you are not clicking on a field value that is hyperlink.</span></span> 
3. <span data-ttu-id="cc75f-136">Na stránke **Aktívne parametre** vyberte kartu **Cenník**. Vedľajšia mriežka zobrazuje zoznam predvolených cenníkov.</span><span class="sxs-lookup"><span data-stu-id="cc75f-136">On the **Active Parameters** page, select the **Price List** tab. A subgrid shows a list of default price lists.</span></span> <span data-ttu-id="cc75f-137">Toto je zoznam štandardných nákladových a predajných cenníkov.</span><span class="sxs-lookup"><span data-stu-id="cc75f-137">This is a list of standard cost and sales price lists.</span></span> <span data-ttu-id="cc75f-138">Ak budete mať na tomto mieste priradený cenník **Predaj** pre každú menu, v ktorej predávate, budete mať istotu, že cenník pre predaj je predvolený pre všetky zmluvy, ktoré vytvoríte pre zákazníkov, ktorí obchodujú v tejto mene.</span><span class="sxs-lookup"><span data-stu-id="cc75f-138">Having a **Sales** price list associated here for every currency that you sell in ensures that the sales price list is the default on any contract that you create for customers that transact in this currency.</span></span>

### <a name="set-up-a-customer-specific-project-price-list"></a><span data-ttu-id="cc75f-139">Vytvorenie projektového cenníka pre konkrétneho zákazníka</span><span class="sxs-lookup"><span data-stu-id="cc75f-139">Set up a customer-specific project price list</span></span>

<span data-ttu-id="cc75f-140">Ak ste so zákazníkmi dohodli rámcovú cenovú dohodu, môžete vytvoriť aj projektové cenníky špecifické pre zákazníka.</span><span class="sxs-lookup"><span data-stu-id="cc75f-140">You can also set up customer–specific project price lists when you have negotiated a master pricing agreement with your customers.</span></span>

1. <span data-ttu-id="cc75f-141">Prejdite do časti **Predaj** > **Zákazníci**.</span><span class="sxs-lookup"><span data-stu-id="cc75f-141">Go to **Sales** > **Customers**.</span></span>
2. <span data-ttu-id="cc75f-142">Zo zoznamu aktívnych obchodných vzťahov vyberte zákazníka, pre ktorého má špeciálny cenník.</span><span class="sxs-lookup"><span data-stu-id="cc75f-142">From the list of active accounts, select the customer for whom have special price list.</span></span>
3. <span data-ttu-id="cc75f-143">Vyberte záznam zákazníka, aby ste ho otvorili, a potom vyberte kartu **Projektové cenníky**. Na vedľajšej mriežke sa zobrazí zoznam projektových cenníkov špecifických pre tohto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="cc75f-143">Select the customer record to open it and then select the **Project Price Lists** tab. A subgrid shows a list of project price lists specific to this customer.</span></span> 
4. <span data-ttu-id="cc75f-144">Vytvorte tu nové priradenie cenníkov, aby bol projektový cenník špecifický pre tohto zákazníka.</span><span class="sxs-lookup"><span data-stu-id="cc75f-144">Create a new price list association here to have project price list specific to this customer.</span></span>

## <a name="custom-pricing-on-a-project-contract"></a><span data-ttu-id="cc75f-145">Vlastné ceny v projektovej zmluve</span><span class="sxs-lookup"><span data-stu-id="cc75f-145">Custom pricing on a project contract</span></span>

<span data-ttu-id="cc75f-146">Keď budete mať predvolené projektové cenníky pre organizácie a zákazníkov, vaše projektové zmluvy sa automaticky vytvoria s týmito asociáciami projektových cenníkov.</span><span class="sxs-lookup"><span data-stu-id="cc75f-146">After you have organizational and customer-specific default project price lists, your project contracts will be created with these project price list associations automatically.</span></span> <span data-ttu-id="cc75f-147">Projektové cenníky v projektovej zmluve sa však vždy kopírujú s dátumom a názvom zmluvy, ktorý je k nim pripojený.</span><span class="sxs-lookup"><span data-stu-id="cc75f-147">However, project price lists on a project contract are always copied with the date and contract name appended to them.</span></span> <span data-ttu-id="cc75f-148">Manažéri obchodných vzťahov a projektoví manažéri potom môžu upravovať ceny v týchto kópiách.</span><span class="sxs-lookup"><span data-stu-id="cc75f-148">The account and project managers can then begin making edits to prices on these copies.</span></span> <span data-ttu-id="cc75f-149">Tieto zmenené ceny sa budú vzťahovať iba na túto projektovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="cc75f-149">These changed prices will be applicable to this project contract only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]