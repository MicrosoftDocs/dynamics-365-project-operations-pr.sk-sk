---
title: Aktualizácia atribútov doplnkov o nové cenové dimenzie
description: Táto téma poskytuje informácie o aktualizácii atribútov doplnkov pre cenové dimenzie.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643237"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="06a66-103">Aktualizácia atribútov doplnkov o nové cenové dimenzie</span><span class="sxs-lookup"><span data-stu-id="06a66-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="06a66-104">Táto téma poskytuje informácie o aktualizácii atribútov doplnkov pre cenové dimenzie.</span><span class="sxs-lookup"><span data-stu-id="06a66-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="06a66-105">Táto téma sa týka iba funkcií cenovej ponuky a zmluvy v Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="06a66-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="06a66-106">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="06a66-106">Prerequisites</span></span>
<span data-ttu-id="06a66-107">Pred vykonaním krokov v tejto téme musíte mať dokončené postupy v nasledujúcich témach:</span><span class="sxs-lookup"><span data-stu-id="06a66-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="06a66-108">Vytvorenie vlastných polí a entít</span><span class="sxs-lookup"><span data-stu-id="06a66-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="06a66-109">Pridanie vlastných polí do entít nastavenia cien a transakcií </span><span class="sxs-lookup"><span data-stu-id="06a66-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="06a66-110">[Nastavenie vlastných polí ako cenových dimenzií](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="06a66-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="06a66-111">Ak ste tieto postupy nedokončili, dokončite ich a potom sa vráťte na túto tému.</span><span class="sxs-lookup"><span data-stu-id="06a66-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="06a66-112">Registrácia doplnku</span><span class="sxs-lookup"><span data-stu-id="06a66-112">Register a plug-in</span></span>
<span data-ttu-id="06a66-113">Keď sa na stránke **Riadok cenovej ponuky** pre riadok ponuky projektu vytvorí detail riadka cenovej ponuky, systém vytvorí dva riadky odhadu.</span><span class="sxs-lookup"><span data-stu-id="06a66-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="06a66-114">Jeden riadok je pre stranu nákladov odhadu a druhý riadok pre stranu predaja.</span><span class="sxs-lookup"><span data-stu-id="06a66-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="06a66-115">Toto je rovnaké pre riadky projektových zmlúv.</span><span class="sxs-lookup"><span data-stu-id="06a66-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="06a66-116">Keď vykonáte zmenu množstva alebo poľa na strane nákladov, táto zmena tiež vykoná na strane predaja.</span><span class="sxs-lookup"><span data-stu-id="06a66-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="06a66-117">Je to možné, pretože doplnky PreOperation na Quotelinedetail a entity podrobností riadka zmluvy spájajú špecifické atribúty na strane nákladov so stranou predaja transakcie.</span><span class="sxs-lookup"><span data-stu-id="06a66-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="06a66-118">Ak potrebujete vykonať zmeny v hodnotách cenových dimenzií na strane predaja aj na strane nákladov, je potrebné po vykonaní zmien v cenovej dimenzii znova zaregistrovať nasledujúce doplnky.</span><span class="sxs-lookup"><span data-stu-id="06a66-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="06a66-119">Toto sú doplnky na aktualizáciu a opätovnú registráciu:</span><span class="sxs-lookup"><span data-stu-id="06a66-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="06a66-120">PreOperationContractLineDetailUpdate – **Aktualizuje msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="06a66-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="06a66-121">PreOperationQuoteLineDetailUpdate - **Aktualizuje msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="06a66-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="06a66-122">Vykonaním nasledujúcich krokov aktualizujete a znova zaregistrujete doplnky.</span><span class="sxs-lookup"><span data-stu-id="06a66-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="06a66-123">Otvorte **PluginRegistrationTool** a pripojte sa k svojmu prostrediu Project Operations Dataverse.</span><span class="sxs-lookup"><span data-stu-id="06a66-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="06a66-124">Vyberte **Vyhľadávať** a zadajte niekoľko prvých písmen doplnku, ktorý sa má aktualizovať.</span><span class="sxs-lookup"><span data-stu-id="06a66-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="06a66-125">Po rozpoznaní doplnku ho označte a potom vyberte možnosť **Vybrať na hlavnom formulári**.</span><span class="sxs-lookup"><span data-stu-id="06a66-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="06a66-126">Vyberte krok **Aktualizovať msdyn_orderlinetransaction**, kliknite pravým tlačidlom myši a potom vyberte položku **Aktualizovať**.</span><span class="sxs-lookup"><span data-stu-id="06a66-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="06a66-127">Na dialógovej stránke **Aktualizovať** vyberte tri bodky (**...**) v atribútoch filtrovania.</span><span class="sxs-lookup"><span data-stu-id="06a66-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="06a66-128">Otvorí sa okno s atribútmi filtrovania, ktoré poskytuje zoznam všetkých atribútov v entite a cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="06a66-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="06a66-129">Začiarknite políčka pre atribúty cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="06a66-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="06a66-130">Výberom tlačidla **OK** zatvoríte stránku a potom vyberte **Aktualizovať krok**.</span><span class="sxs-lookup"><span data-stu-id="06a66-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="06a66-131">Opakujte kroky 2 až 7 pre druhý doplnok **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="06a66-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="06a66-132">Pre tento doplnok budete musieť aktualizovať krok **Aktualizácia msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="06a66-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="06a66-133">Zatvorte nástroj **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="06a66-133">Close **PluginRegistrationTool**.</span></span>
