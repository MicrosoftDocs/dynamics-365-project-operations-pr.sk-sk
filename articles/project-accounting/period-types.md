---
title: Druhy období
description: Táto téma poskytuje informácie o tom, ako nastaviť typy období pre odhad výnosov.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287302"
---
# <a name="period-types"></a><span data-ttu-id="dcc3d-103">Typy období</span><span class="sxs-lookup"><span data-stu-id="dcc3d-103">Period types</span></span>

<span data-ttu-id="dcc3d-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="dcc3d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="dcc3d-105">Typ obdobia definuje, ako často sa odhadujú výnosy v projekte.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="dcc3d-106">Táto téma poskytuje informácie o tom, ako nastaviť typy období pre odhad výnosov.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="dcc3d-107">Vytvorenie a práca s typmi období</span><span class="sxs-lookup"><span data-stu-id="dcc3d-107">Create and work with period types</span></span>
<span data-ttu-id="dcc3d-108">Ak chcete vytvárať a pracovať s typmi období, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="dcc3d-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="dcc3d-109">Vo vašom prostredí Dynamics 365 Finance prejdite do **Projektový manažment a účtovníctvo** > **Nastavenie** > **Odhady** > **Typy období**.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="dcc3d-110">Ak chcete vytvoriť nový typ obdobia, vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-110">Select **New** to create new period type.</span></span> <span data-ttu-id="dcc3d-111">Zadajte názov a popis.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-111">Enter a name and description.</span></span>
3. <span data-ttu-id="dcc3d-112">V poli **Frekvencia** vyberte hodnotu:</span><span class="sxs-lookup"><span data-stu-id="dcc3d-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="dcc3d-113">Ak vyberiete **Týždenne**, **Dvojtýždenne**, **Polmesačne**, **Mesačne**, **Denne**, **Štvrťročne** alebo **Ročne**, kalendár sa použije na generovanie období.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="dcc3d-114">Ak vyberiete **Obdobie účtovnej knihy**, na generovanie období sa použijú obdobia hlavnej účtovnej knihy z konfigurácie hlavnej účtovnej knihy.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="dcc3d-115">Ak vyberiete **Neobmedzene**, môžete určiť vlastné obdobia.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="dcc3d-116">Vyberte záznam typu obdobia a potom vyberte **Generovať obdobia** na vytvorenie období pre typ obdobia.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="dcc3d-117">Na základe zvolenej frekvencie období môžete mať možnosť určiť dátum začatia alebo počet období, ktoré sa majú vygenerovať.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="dcc3d-118">Vyberte **Obdobia** na kontrolu generovaných období.</span><span class="sxs-lookup"><span data-stu-id="dcc3d-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]