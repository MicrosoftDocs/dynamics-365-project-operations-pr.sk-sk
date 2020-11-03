---
title: Vytváranie vlastných riešení pre cenové dimenzie
description: Táto téma vysvetľuje, ako vytvoriť vlastné riešenie pri vytváraní vlastných cenových dimenzií.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084373"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="ab17e-103">Vytváranie vlastných riešení pre cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="ab17e-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab17e-104">Všetky zmeny vlastných cenových dimenzií by mali byť v samostatnom riešení.</span><span class="sxs-lookup"><span data-stu-id="ab17e-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="ab17e-105">Táto dôležitá najlepšia prax poskytuje flexibilitu v budúcnosti na aktualizáciu alebo odstránenie zmien podľa potreby, pomôže pri opätovnom použití vašej práce a uľahčuje port týchto zmien na inú inštanciu.</span><span class="sxs-lookup"><span data-stu-id="ab17e-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="ab17e-106">Potom, čo vykonáte všetky požadované zmeny, exportujte toto riešenie ako **spravované riešenie** a importujte ho do iných inštancií na opätovné použitie nastavení cien.</span><span class="sxs-lookup"><span data-stu-id="ab17e-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="ab17e-107">Vyberte položku **Nastavenia** > **Riešenia** a potom vyberte položku **Nové**.</span><span class="sxs-lookup"><span data-stu-id="ab17e-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="ab17e-108">Pomenujte riešenie, **dimenzie cien \<your organization name>** , zadajte zostávajúce požadované informácie a potom vyberte **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="ab17e-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Vytvorenie vlastného riešenia pre dimenzie cien](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="ab17e-110">Pridajte všetky požadované entity a súvisiace súčasti do riešenia Cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="ab17e-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="ab17e-111">Budete musieť pridať nasledujúce entity služby Project Service na vaše cenové riešenie.</span><span class="sxs-lookup"><span data-stu-id="ab17e-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="ab17e-112">Dokončite kroky v tomto postupe tak, aby sa niektoré dôležité zmeny schémy v cenovom riešení tak, že entity sa dozvedia o nových cenových dimenziách.</span><span class="sxs-lookup"><span data-stu-id="ab17e-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="ab17e-113">Vyberte **Nastavenia** > **Riešenia** a potom dvakrát kliknite na **Dimenzie cien \<your organization name>**.</span><span class="sxs-lookup"><span data-stu-id="ab17e-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="ab17e-114">V prehľadávači riešení, na ľavom navigačnom paneli vyberte **Pridať existujúce** > **Entity**.</span><span class="sxs-lookup"><span data-stu-id="ab17e-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="ab17e-115">V dialógovom okne **súčasti riešenia** vyberte nasledujúce entity:</span><span class="sxs-lookup"><span data-stu-id="ab17e-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="ab17e-116">Skutočnosť</span><span class="sxs-lookup"><span data-stu-id="ab17e-116">Actual</span></span>
- <span data-ttu-id="ab17e-117">Rezervovateľný zdroj</span><span class="sxs-lookup"><span data-stu-id="ab17e-117">Bookable Resource</span></span>
- <span data-ttu-id="ab17e-118">Riadok odhadu</span><span class="sxs-lookup"><span data-stu-id="ab17e-118">Estimate Line</span></span>
- <span data-ttu-id="ab17e-119">Projektová úloha</span><span class="sxs-lookup"><span data-stu-id="ab17e-119">Project Task</span></span>
- <span data-ttu-id="ab17e-120">Podrobnosti o riadku faktúry</span><span class="sxs-lookup"><span data-stu-id="ab17e-120">Invoice Line Detail</span></span>
- <span data-ttu-id="ab17e-121">Záznam v účtovnom denníku</span><span class="sxs-lookup"><span data-stu-id="ab17e-121">Journal Line</span></span>
- <span data-ttu-id="ab17e-122">Podrobnosti o riadku projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="ab17e-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="ab17e-123">Člen projektového tímu</span><span class="sxs-lookup"><span data-stu-id="ab17e-123">Project Team Member</span></span>
- <span data-ttu-id="ab17e-124">Podrobnosti o riadku cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="ab17e-124">Quote Line Detail</span></span>
- <span data-ttu-id="ab17e-125">Prirážka k cene roly</span><span class="sxs-lookup"><span data-stu-id="ab17e-125">Role Price Markup</span></span>
- <span data-ttu-id="ab17e-126">Cena roly</span><span class="sxs-lookup"><span data-stu-id="ab17e-126">Role Price</span></span> 
- <span data-ttu-id="ab17e-127">Zadanie času</span><span class="sxs-lookup"><span data-stu-id="ab17e-127">Time Entry</span></span> 

> ![Pridanie existujúcich entít do riešenia cenových dimenzií](media/Existing-entities-to-PD-solution.png)

> ![Výber súčastí riešenia](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="ab17e-130">Nezabudnite zahrnúť všetky formuláre a zobrazenia pre každú vybranú entitu.</span><span class="sxs-lookup"><span data-stu-id="ab17e-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="ab17e-131">Keď sa zobrazí výzva na zahrnutie všetkých závislých entít pre entity vybraté vyššie, vyberte položku **Nie**.</span><span class="sxs-lookup"><span data-stu-id="ab17e-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Nezahrnúť súvisiace súčasti](media/Do-not-include-required.png)


