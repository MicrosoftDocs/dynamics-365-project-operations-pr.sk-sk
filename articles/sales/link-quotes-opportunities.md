---
title: Vytvorenie projektových cenových ponúk z príležitostí
description: Táto téma poskytuje informácie o vytváraní cenových ponúk projektu z príležitostí.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084276"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="ec224-103">Vytvorenie projektových cenových ponúk z príležitostí</span><span class="sxs-lookup"><span data-stu-id="ec224-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="ec224-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="ec224-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ec224-105">Cenové ponuky je možné vytvárať z projektových príležitostí nasledujúcimi spôsobmi:</span><span class="sxs-lookup"><span data-stu-id="ec224-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="ec224-106">Na karte **Cenové ponuky** , na stránke **Príležitosť projektu**</span><span class="sxs-lookup"><span data-stu-id="ec224-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="ec224-107">V toku procesu predaja príležitosti</span><span class="sxs-lookup"><span data-stu-id="ec224-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="ec224-108">Aktualizáciou odkazu príležitosti v existujúcej cenovej ponuke</span><span class="sxs-lookup"><span data-stu-id="ec224-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="ec224-109">Na karte Cenové ponuky, na stránke Projektová príležitosť</span><span class="sxs-lookup"><span data-stu-id="ec224-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="ec224-110">Ak chcete vytvoriť projektovú cenovú ponuku z príležitosti, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="ec224-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="ec224-111">Otvorte stránku **Projektová príležitosť** a vyberte kartu **Cenové ponuky**.</span><span class="sxs-lookup"><span data-stu-id="ec224-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="ec224-112">Na vedľajšej mriežke **Cenové ponuky** vyberte **+** na vytvorenie novej projektovej cenovej ponuky založenej na príležitosti.</span><span class="sxs-lookup"><span data-stu-id="ec224-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="ec224-113">Všetky riadky príležitostí a súvisiace cenníky projektu sa skopírujú do novej cenovej ponuky príležitosti.</span><span class="sxs-lookup"><span data-stu-id="ec224-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="ec224-114">V toku procesu predaja príležitosti</span><span class="sxs-lookup"><span data-stu-id="ec224-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="ec224-115">Ak chcete vytvoriť cenovú ponuku z toku predajného procesu príležitosti, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="ec224-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="ec224-116">V toku procesu predaja príležitosti otvorte príležitosť.</span><span class="sxs-lookup"><span data-stu-id="ec224-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="ec224-117">Vyberte etapu **Schváliť**.</span><span class="sxs-lookup"><span data-stu-id="ec224-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="ec224-118">Vyberte **Ďalej** a potom vyberte **+ Vytvoriť** na vytvorenie novej cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="ec224-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="ec224-119">Väčšina informácií na karte **Súhrn** pre túto novú cenovú ponuku bude mať predvolenú hodnotu z príležitosti.</span><span class="sxs-lookup"><span data-stu-id="ec224-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="ec224-120">Zadajte požadované informácie, ktoré chýbajú, alebo podľa potreby aktualizujte predvolené hodnoty na karte **Súhrn** ,</span><span class="sxs-lookup"><span data-stu-id="ec224-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="ec224-121">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="ec224-121">Select **Save**.</span></span> <span data-ttu-id="ec224-122">Vytvorí sa nová cenová ponuka a spojí sa s príležitosťou.</span><span class="sxs-lookup"><span data-stu-id="ec224-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="ec224-123">Teraz si môžete pozrieť informácie o cenovej ponuke na karte **Cenové ponuky** na stránke **Príležitosť**.</span><span class="sxs-lookup"><span data-stu-id="ec224-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="ec224-124">Proces predaja príležitosti sa posúva do ďalšej fázy, **Navrhnúť**.</span><span class="sxs-lookup"><span data-stu-id="ec224-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="ec224-125">Aktualizáciou odkazu príležitosti v existujúcej cenovej ponuke</span><span class="sxs-lookup"><span data-stu-id="ec224-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="ec224-126">Existujúca cenová ponuka môže byť prepojená s príležitosťou.</span><span class="sxs-lookup"><span data-stu-id="ec224-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="ec224-127">Ak chcete aktualizovať informácie o príležitosti pre existujúcu cenovú ponuku, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="ec224-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="ec224-128">Otvorte stránku **Cenová ponuka** a vyberte kartu **Súhrn**.</span><span class="sxs-lookup"><span data-stu-id="ec224-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="ec224-129">V poli **Príležitosť** vyberte príležitosť, ktorú chcete prepojiť s cenovou ponukou.</span><span class="sxs-lookup"><span data-stu-id="ec224-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="ec224-130">Cenovú ponuku si môžete pozrieť v mriežke **Cenové ponuky** v časti Príležitosť.</span><span class="sxs-lookup"><span data-stu-id="ec224-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="ec224-131">Pomocou procesu predaja príležitosti sa príležitosť môže presunúť do ďalšej fázy, **Navrhnúť**.</span><span class="sxs-lookup"><span data-stu-id="ec224-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="ec224-132">Keď presuniete príležitosť do tejto fázy, môžete si vybrať túto cenovú ponuku zo zoznamu cenových ponúk spojených s touto príležitosťou.</span><span class="sxs-lookup"><span data-stu-id="ec224-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="ec224-133">Výber tejto cenovej ponuky znamená, že sa s ňou posúvate vpred.</span><span class="sxs-lookup"><span data-stu-id="ec224-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="ec224-134">Všetky ostatné cenové ponuky spojené s príležitosťou budú stále k dispozícii a aktívne, kým sa jedna z nich nevyužije.</span><span class="sxs-lookup"><span data-stu-id="ec224-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="ec224-135">Proces predaja môžete presunúť späť do predchádzajúcej fázy **Kvalifikovať** , a vybrať ďalšiu ponuku, s ktorou budete pokračovať ďalej.</span><span class="sxs-lookup"><span data-stu-id="ec224-135">You can move the sales process back to the previous stage **Qualify** , and pick another quote to move forward with.</span></span>
