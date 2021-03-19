---
title: Vytvorenie riešenia pre vlastné cenové dimenzie
description: Táto téma poskytuje informácie o vytváraní riešení pre vlastné cenové dimenzie.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278437"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="0a231-103">Vytvorenie riešenia pre vlastné cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="0a231-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="0a231-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="0a231-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="0a231-105">Všetky zmeny vlastných cenových dimenzií by mali byť v samostatnom riešení.</span><span class="sxs-lookup"><span data-stu-id="0a231-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="0a231-106">Tento dôležitý najlepší postup poskytuje flexibilitu pri aktualizácii alebo odstraňovaní zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje portovanie týchto zmien na iné inštancie.</span><span class="sxs-lookup"><span data-stu-id="0a231-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="0a231-107">Po vykonaní požadovaných zmien exportujte toto riešenie ako **spravované** riešenie a importujte ho do iných inštancií na opätovné použitie.</span><span class="sxs-lookup"><span data-stu-id="0a231-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="0a231-108">Vytvorenie riešenia pre vlastné cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="0a231-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="0a231-109">Vyberte položku **Nastavenia** > **Riešenia** a potom vyberte položku **Nové**.</span><span class="sxs-lookup"><span data-stu-id="0a231-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="0a231-110">Pomenujte riešenie ako *Cenové dimenzie <your organization name>*.</span><span class="sxs-lookup"><span data-stu-id="0a231-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="0a231-111">Zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="0a231-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Vytvorenie vlastného riešenia pre cenové dimenzie](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="0a231-113">Pridajte všetky požadované entity a súvisiace súčasti do riešenia Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="0a231-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="0a231-114">Pridajte do svojho cenového riešenia nasledujúce entity Project Service, aby ste mohli urobiť dôležité zmeny schémy v cenovom riešení.</span><span class="sxs-lookup"><span data-stu-id="0a231-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="0a231-115">Po dokončení tohto postupu entity rozpoznajú nové cenové dimenzie.</span><span class="sxs-lookup"><span data-stu-id="0a231-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="0a231-116">Vyberte **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **<*názov vašej organizácie*> cenové dimenzie**.</span><span class="sxs-lookup"><span data-stu-id="0a231-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="0a231-117">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Pridať existujúce** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="0a231-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="0a231-118">V dialógovom okne **súčasti riešenia** vyberte nasledujúce entity:</span><span class="sxs-lookup"><span data-stu-id="0a231-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="0a231-119">**Skutočnosť**</span><span class="sxs-lookup"><span data-stu-id="0a231-119">**Actual**</span></span>
   - <span data-ttu-id="0a231-120">**Rezervovateľný zdroj**</span><span class="sxs-lookup"><span data-stu-id="0a231-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="0a231-121">**Riadok odhadu**</span><span class="sxs-lookup"><span data-stu-id="0a231-121">**Estimate Line**</span></span>
   - <span data-ttu-id="0a231-122">**Projektová úloha**</span><span class="sxs-lookup"><span data-stu-id="0a231-122">**Project Task**</span></span>
   - <span data-ttu-id="0a231-123">**Podrobnosti o riadku faktúry**</span><span class="sxs-lookup"><span data-stu-id="0a231-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="0a231-124">**Záznam v účtovnom denníku**</span><span class="sxs-lookup"><span data-stu-id="0a231-124">**Journal Line**</span></span>
   - <span data-ttu-id="0a231-125">**Podrobnosti o riadku projektovej zmluvy**</span><span class="sxs-lookup"><span data-stu-id="0a231-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="0a231-126">**Člen projektového tímu**</span><span class="sxs-lookup"><span data-stu-id="0a231-126">**Project Team Member**</span></span>
   - <span data-ttu-id="0a231-127">**Podrobnosti o riadku cenovej ponuky**</span><span class="sxs-lookup"><span data-stu-id="0a231-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="0a231-128">**Prirážka k cene roly**</span><span class="sxs-lookup"><span data-stu-id="0a231-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="0a231-129">**Cena roly**</span><span class="sxs-lookup"><span data-stu-id="0a231-129">**Role Price**</span></span>
   - <span data-ttu-id="0a231-130">**Zadanie času**</span><span class="sxs-lookup"><span data-stu-id="0a231-130">**Time Entry**</span></span>
 
   ![Pridanie existujúcich entít do vlastného riešenia cenovej dimenzie](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="0a231-132">Pre každú entitu skontrolujte pridávané komponenty a konečný zoznam aktív entity pre každú entitu.</span><span class="sxs-lookup"><span data-stu-id="0a231-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="0a231-133">Zahrňte všetky formuláre a zobrazenia pre každú vybranú entitu.</span><span class="sxs-lookup"><span data-stu-id="0a231-133">Include all forms and views for each of the selected entities.</span></span>

  ![Pridané entity](./media/solution-component-selection.png)


5.  <span data-ttu-id="0a231-135">Po zobrazení výzvy na zahrnutie akýchkoľvek závislých entít pre vybrané entity vyberte **Nie, nezahŕňať požadované komponenty.**</span><span class="sxs-lookup"><span data-stu-id="0a231-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Vrátane závislých entít](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]