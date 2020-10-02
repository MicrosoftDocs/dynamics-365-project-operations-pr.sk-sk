---
title: Jednotky a jednotkové skupiny
description: Táto téma poskytuje informácie o tom, ako vytvoriť jednotky a skupiny jednotiek v Dynamics 365 Project Operations.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898775"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="94668-103">Jednotky a jednotkové skupiny</span><span class="sxs-lookup"><span data-stu-id="94668-103">Units and unit groups</span></span>

<span data-ttu-id="94668-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="94668-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94668-105">Jednotky predstavujú množstvá alebo hodnoty, v ktorých sa produkty alebo služby predávajú.</span><span class="sxs-lookup"><span data-stu-id="94668-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="94668-106">Napríklad ak predávate záhradkárske potreby, možno predať semená v jednotkách balíkoch, debnách alebo paletách.</span><span class="sxs-lookup"><span data-stu-id="94668-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="94668-107">skupina jednotiek je zbierka týchto rôznych jednotiek.</span><span class="sxs-lookup"><span data-stu-id="94668-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="94668-108">Ak chcete vykonať kroky v tejto téme, uistite sa, že máte priradenú rolu Správca systému alebo Sales Professional Manager či ekvivalentné povolenia.</span><span class="sxs-lookup"><span data-stu-id="94668-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="94668-109">Vytvorenie jednotkovej skupiny</span><span class="sxs-lookup"><span data-stu-id="94668-109">Create a unit group</span></span>

1. <span data-ttu-id="94668-110">Na mape lokality zvoľte možnosť **Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="94668-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="94668-111">Vyberte **Nový** a v dialógovom okne **Vytvoriť skupinu jednotiek** zadajte názov jednotky.</span><span class="sxs-lookup"><span data-stu-id="94668-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="94668-112">V poli **Primárna jednotka** zadajte najnižšiu bežnú jednotku merania, ktorá sa bude využívať pri predaji produktu.</span><span class="sxs-lookup"><span data-stu-id="94668-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="94668-113">Môžete napríklad zadať „kus“ alebo „unca“.</span><span class="sxs-lookup"><span data-stu-id="94668-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="94668-114">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="94668-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="94668-115">Pridanie jednotiek do jednotkovej skupiny</span><span class="sxs-lookup"><span data-stu-id="94668-115">Add units to a unit group</span></span>

1. <span data-ttu-id="94668-116">Otvorte jednotkovú skupinu a na karte **Súvisiace** vyberte **Jednotky**.</span><span class="sxs-lookup"><span data-stu-id="94668-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="94668-117">Môžete vidieť, že primárna jednotka je už pridaná.</span><span class="sxs-lookup"><span data-stu-id="94668-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="94668-118">Vyberte **Pridať novú jednotku** a na stránke **Rýchle vytvorenie: Jednotka** v poli **Názov** zadajte názov jednotky.</span><span class="sxs-lookup"><span data-stu-id="94668-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="94668-119">Do poľa **Množstvo** zadajte množstvo, ktoré bude jednotka obsahovať.</span><span class="sxs-lookup"><span data-stu-id="94668-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="94668-120">Ak napríklad krabica obsahuje dva kusy, zadajte hodnotu „2”.</span><span class="sxs-lookup"><span data-stu-id="94668-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="94668-121">V poli **Základná jednotka** vyberte základnú jednotku, aby ste určili najnižšiu jednotku merania pre jednotku.</span><span class="sxs-lookup"><span data-stu-id="94668-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="94668-122">Môžete napríklad zvoliť „Kus“.</span><span class="sxs-lookup"><span data-stu-id="94668-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="94668-123">Vyberte položku **Uložiť**:</span><span class="sxs-lookup"><span data-stu-id="94668-123">Select **Save**:</span></span>
