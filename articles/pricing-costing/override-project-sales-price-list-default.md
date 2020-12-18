---
title: Prepísanie projektových predajných cenníkov
description: Táto téma poskytuje informácie o vytváraní prispôsobených predajných cenníkov.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: af9baca540d89f4e5e616bdfdd6111bef29abe28
ms.sourcegitcommit: 656a9d03f260c29e988e2ff05b6e07ae0365d6d0
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/04/2020
ms.locfileid: "4672250"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="3ee4e-103">Prepísanie projektových predajných cenníkov</span><span class="sxs-lookup"><span data-stu-id="3ee4e-103">Override project sales price lists</span></span>

<span data-ttu-id="3ee4e-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="3ee4e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="3ee4e-105">Projektové cenníky pre konkrétneho zákazníka</span><span class="sxs-lookup"><span data-stu-id="3ee4e-105">Customer-specific project price lists</span></span>

<span data-ttu-id="3ee4e-106">Cenové dohody s konkrétnym zákazníkom je možné nastaviť ako projektové cenníky v zázname obchodného vzťahu v aplikácii Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="3ee4e-107">Ak chcete nastaviť projektový cenník pre konkrétneho zákazníka, prejdite do oblasti **Predaj** a následne k záznamu obchodného vzťahu.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="3ee4e-108">Otvorte stránku so zoznamom **Obchodné vzťahy**.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="3ee4e-109">Vyhľadajte a dvakrát kliknite na záznam zákazníka, čím otvoríte stránku s podrobnosťami **Obchodného vzťahu**.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="3ee4e-110">Na karte **Projektové cenníky** vyberte **+ Nový projektový cenník**.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="3ee4e-111">Na stránke **Nový projektový cenník** vyberte z rozbaľovacej ponuky cenník.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="3ee4e-112">Zahrnuté budú iba cenníky, ktoré majú nastavený kontext na **Predaj** a ktorých mena sa zhoduje s menou obchodného vzťahu.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="3ee4e-113">Pomenujte priradenie a potom vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="3ee4e-114">Vytvorí sa projektový cenník pre konkrétneho zákazníka.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="3ee4e-115">Tento cenník sa použije na predvolené projektové ceny v projektových cenových ponukách alebo zmluvách vytvorených pre tohto zákazníka, pričom dátum vytvorenia cenovej ponuky alebo projektovej zmluvy spadá do dátumu účinnosti cenníka.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="3ee4e-116">Vlastné ceny na základe projektových ponúk</span><span class="sxs-lookup"><span data-stu-id="3ee4e-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="3ee4e-117">V projektových cenových ponukách môžete mať stanovenú cenu projektu, ktorá sa začína predvoleným štandardným cenníkom, ktorý je predvolený od zákazníka alebo od parametrov projektu.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="3ee4e-118">Ak potrebujete vlastnú cenu pre prácu súvisiacu s projektom v určitej cenovej ponuke, získate ju z entity priradenej k projektovým cenníkom.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="3ee4e-119">Vykonaním nasledujúcich krokov nastavíte projektové cenu špecifickú pre cenovú ponuku.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="3ee4e-120">Otvorte projektovú cenovú ponuku vyberte kartu **Projektové cenníky**.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="3ee4e-121">Vo vedľajšej mriežke vyberte **Vytvorenie vlastných cien**.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="3ee4e-122">Všetky cenníky projektu, ktoré sú priložené k cenovej ponuke, sa skopírujú do nových cenníkov.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="3ee4e-123">Názvy nových cenníkov odrážajú názov cenovej ponuky s časovou pečiatkou, kedy boli tieto cenníky vytvorené.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="3ee4e-124">Môžete použiť každý z týchto cenníkov a aktualizovať ceny práce (cena roly) a výdavkov (cena kategórie).</span><span class="sxs-lookup"><span data-stu-id="3ee4e-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="3ee4e-125">Tieto zmenené budú platiť iba na túto projektovú cenovú ponuku.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="3ee4e-126">Projektové cenníky v projektovej zmluve</span><span class="sxs-lookup"><span data-stu-id="3ee4e-126">Price lists on a project contract</span></span>

<span data-ttu-id="3ee4e-127">V projektovej zmluve je projektová cena vždy predvolená ako vlastný cenník s názvom zmluvy a časovou pečiatkou vytvorenia pripojenou k názvu.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="3ee4e-128">To platí bez ohľadu na to, či bola zmluva vytvorená pri získaní cenovej ponuky, alebo či bola zmluva vytvorená úplne od začiatku.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="3ee4e-129">V prípade potreby môžete toto priradenie k vlastnému cenníku odstrániť a namiesto toho priradiť štandardný cenník k projektovej zmluve.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="3ee4e-130">Ak priraďujete štandardný cenník k projektovým cenníkom v cenovej ponuke alebo zmluve, akékoľvek zmeny cien v cenníku ovplyvnia všetky cenové ponuky a zmluvy, ktoré používajú cenník.</span><span class="sxs-lookup"><span data-stu-id="3ee4e-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>
