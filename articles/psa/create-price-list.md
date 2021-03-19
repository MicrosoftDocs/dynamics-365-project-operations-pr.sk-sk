---
title: Vytvorenie cenníka
description: Ako na vytvorenie cenníka v Project Service
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0732ccca43e404412efae8a91873e43c28d041ca
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290333"
---
# <a name="create-a-price-list-project-service"></a><span data-ttu-id="c0983-103">Vytvorenie cenníka (Project Service)</span><span class="sxs-lookup"><span data-stu-id="c0983-103">Create a price list (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="c0983-104">Cenníky poskytujú šablónu správcom účtu, ktorú môžu použiť na vytvorenie cenových ponúk a projektov a tiež na stanovenie nákladov na projekt.</span><span class="sxs-lookup"><span data-stu-id="c0983-104">Price lists provide a template your account managers can use for creating quotes and projects, and for establishing the costs of a project.</span></span> <span data-ttu-id="c0983-105">Ponúkajú zoznam položiek úloh a nákladov a cenu za každú z nich.</span><span class="sxs-lookup"><span data-stu-id="c0983-105">They provide a line item list of roles and expenses, and the price you will charge for each.</span></span> <span data-ttu-id="c0983-106">Môžete vytvoriť viaceré cenníky, aby ste mohli zachovať samostatné štruktúry cien pre rôzne regióny, kde produkty predávate alebo rôzne predajné kanály.</span><span class="sxs-lookup"><span data-stu-id="c0983-106">You can create multiple price lists so that you can maintain separate price structures for different regions you sell your products in or for different sales channels.</span></span> <span data-ttu-id="c0983-107">Je to dobrý nápad vytvoriť najmenej jeden cenník pre každú menu, v ktorej plánujete účtovať zákazníkov.</span><span class="sxs-lookup"><span data-stu-id="c0983-107">It’s a good idea to create at least one price list for every currency you plan to bill your customers in.</span></span>  
  
<span data-ttu-id="c0983-108">Na vytvorenie finančného odhadu pre vykonanú prácu sa uistite, že každý projekt má zoznam sprievodných nákladov a predajných cien.</span><span class="sxs-lookup"><span data-stu-id="c0983-108">To create financial estimates for the work to be delivered, make sure every project has a backing cost and sales price list.</span></span> <span data-ttu-id="c0983-109">Nastavte predvolené náklady a predajný cenník, ktoré sa vzťahujú na všetky projekty vytvorené vo vašej organizácii.</span><span class="sxs-lookup"><span data-stu-id="c0983-109">Set up a default cost and sales pricelist that applies to all projects created in your organization.</span></span>  
  
<span data-ttu-id="c0983-110">Cenníky sa spoliehajú na úlohy a kategórie výdavkov, takže pred vytvorením cenníka, uistite sa, že ste už nakonfigurovali úlohy a náklady kategórie, ktoré chcete použiť pri vytváraní cenníku.</span><span class="sxs-lookup"><span data-stu-id="c0983-110">Price lists rely on roles and expense categories, so before you create a price list, make sure you’ve already configured the roles and expense categories you want to use while creating the price list.</span></span>  
  
1.  <span data-ttu-id="c0983-111">Prejdite na **Project Service > Cenníky**.</span><span class="sxs-lookup"><span data-stu-id="c0983-111">Go to **Project Service > Price Lists**.</span></span>  
  
2.  <span data-ttu-id="c0983-112">Kliknite na položku **Nový**.</span><span class="sxs-lookup"><span data-stu-id="c0983-112">Click **New**.</span></span>  
  
3.  <span data-ttu-id="c0983-113">V časti **Kontext** zvoľte, či je tento cenník pre **Náklady**, **Nákup** alebo **Predaj**.</span><span class="sxs-lookup"><span data-stu-id="c0983-113">In **Context**, select whether this price list is for **Cost**, **Purchase**, or **Sales**.</span></span>  
  
4.  <span data-ttu-id="c0983-114">V poli **Názov** zadajte názov cenníka.</span><span class="sxs-lookup"><span data-stu-id="c0983-114">In **Name**, enter a name for the price list.</span></span>  
  
5.  <span data-ttu-id="c0983-115">V poli **Mena** zvoľte menu, ktorú použijete pri fakturácii a nákladoch.</span><span class="sxs-lookup"><span data-stu-id="c0983-115">In **Currency**, select the currency you’re going to use for billing or costing.</span></span>  
  
6.  <span data-ttu-id="c0983-116">V poli **Časová jednotka** stanovte časové obdobie, na ktoré sa vzťahuje cena. Môže ísť o deň alebo hodinu.</span><span class="sxs-lookup"><span data-stu-id="c0983-116">In **Time Unit**, specify the period of time the price applies to, such as day or hour.</span></span>  
  
7.  <span data-ttu-id="c0983-117">Podľa potreby vyplňte **Dátum začatia**, **Dátum skončenia** a **Popis**.</span><span class="sxs-lookup"><span data-stu-id="c0983-117">Fill in the **Start Date**, **End Date**, and **Description** as needed.</span></span>  
  
8.  <span data-ttu-id="c0983-118">Kliknite na tlačidlo **Uložiť** a vytvorte záznam, aby ste mohli pokračovať v jeho úprave.</span><span class="sxs-lookup"><span data-stu-id="c0983-118">Click **Save** to create the record so you can continue editing it.</span></span>  
  
9. <span data-ttu-id="c0983-119">Ak chcete pridať cenu roly do cenníka, kliknite na možnosť **+** v časti **Ceny rolí**.</span><span class="sxs-lookup"><span data-stu-id="c0983-119">To add a role price to the price list, click **+** under **Role prices**.</span></span>  
  
10. <span data-ttu-id="c0983-120">V table **Cena roly** vyplňte podrobnosti a potom kliknite na **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="c0983-120">In the **Role Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c0983-121">Pokračujte v pridávaní cien rolí podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="c0983-121">Continue adding role prices as necessary.</span></span> <span data-ttu-id="c0983-122">Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="c0983-122">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
11. <span data-ttu-id="c0983-123">Ak chcete pridať cenu kategórie výdavkov do cenníka, kliknite na možnosť **+** v časti **Ceny kategórií**.</span><span class="sxs-lookup"><span data-stu-id="c0983-123">To add an expense category price to the price list, click **+** under **Category prices**.</span></span>  
  
12. <span data-ttu-id="c0983-124">V table **Cena kategórie transakcie** vyplňte podrobnosti a potom kliknite na **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="c0983-124">In the **Transaction Category Price** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c0983-125">Pokračujte v pridávaní cien kategórií podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="c0983-125">Continue adding category prices as necessary.</span></span> <span data-ttu-id="c0983-126">Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="c0983-126">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
13. <span data-ttu-id="c0983-127">Ak chcete pridať položky do cenníka, kliknite na **+** v časti **Položky v cenníku**.</span><span class="sxs-lookup"><span data-stu-id="c0983-127">To add price list items to the price list, click **+** under **Price List Items**.</span></span>  
  
14. <span data-ttu-id="c0983-128">V table **Položky v cenníku** vyplňte podrobnosti a potom kliknite na **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="c0983-128">In the **Price List Item** pane, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c0983-129">Pokračujte v pridávaní položiek cenníka podľa potreby.</span><span class="sxs-lookup"><span data-stu-id="c0983-129">Continue adding price list items as necessary.</span></span> <span data-ttu-id="c0983-130">Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="c0983-130">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
15. <span data-ttu-id="c0983-131">Ak chcete pridať územný vzťah k cenníku, kliknite na **+** v časti **Územné vzťahy**.</span><span class="sxs-lookup"><span data-stu-id="c0983-131">To add territory relationships to the price list, click **+** under **Territory Relationships**.</span></span>  
  
16. <span data-ttu-id="c0983-132">V okne **Nové pripojenie** vyplňte podrobnosti a potom kliknite na **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="c0983-132">In the **New Connection** window, fill in the details, and then click **Save**.</span></span> <span data-ttu-id="c0983-133">Podľa potreby pokračujte v pridávaní územných vzťahov.</span><span class="sxs-lookup"><span data-stu-id="c0983-133">Continue adding territory relationships as necessary.</span></span> <span data-ttu-id="c0983-134">Keď budete hotoví, kliknite na **Uložiť** v pravom spodnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="c0983-134">When you’re done, click **Save** at the bottom right corner of the screen.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="c0983-135">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="c0983-135">See Also</span></span>  
 [<span data-ttu-id="c0983-136">Konfigurácia Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c0983-136">Configure Project Service Automation</span></span>](../psa/configure.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]