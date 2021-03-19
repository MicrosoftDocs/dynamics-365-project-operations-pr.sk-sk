---
title: Synchronizácia kapacity zdroja
description: Táto téma poskytuje informácie o tom, ako synchronizovať kapacitu zdroja v rámci kalendárov a projektov.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288593"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="43998-103">Synchronizácia kapacity zdroja</span><span class="sxs-lookup"><span data-stu-id="43998-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43998-104">Procesy synchronizácie zdrojov pomáhajú zaručiť, že informácie pre kalendár a základný kalendár sa prenášajú až do plánovania zdrojov projektu.</span><span class="sxs-lookup"><span data-stu-id="43998-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="43998-105">Ak dôjde k zmene kalendára, procesy vykonajú požadované aktualizácie plánovania zdrojov projektu.</span><span class="sxs-lookup"><span data-stu-id="43998-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="43998-106">Procesy tiež pomáhajú zvýšiť výkon, pretože informácie o zdrojoch z kalendára sú synchronizované vopred.</span><span class="sxs-lookup"><span data-stu-id="43998-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="43998-107">Preto sa aktualizácie informácií o plánovaní zdrojov vyskytujú rýchlejšie.</span><span class="sxs-lookup"><span data-stu-id="43998-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="43998-108">Odporúčame naplánovať procesy ako dávkové, nie po jednom.</span><span class="sxs-lookup"><span data-stu-id="43998-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="43998-109">V opačnom prípade existuje riziko, že niekto zabudne na zahrnuté dátumy pri poslednej synchronizácie informácií.</span><span class="sxs-lookup"><span data-stu-id="43998-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="43998-110">Ak sa nepoužívajú zahrnuté dátumy, počas synchronizácie dátumov môžu nastať medzery.</span><span class="sxs-lookup"><span data-stu-id="43998-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Synchronizácia kalendára](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="43998-112">Synchronizácia súhrnov kapacity zdroja</span><span class="sxs-lookup"><span data-stu-id="43998-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="43998-113">Proces synchronizácie je navrhnutý tak, aby synchronizoval všetky informácie z kalendára zdrojov.</span><span class="sxs-lookup"><span data-stu-id="43998-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="43998-114">Tieto informácie zahŕňajú informácie základného kalendára o akýchkoľvek zmenách v tabuľke kapacity kalendára zdrojov projektu.</span><span class="sxs-lookup"><span data-stu-id="43998-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="43998-115">Ak sú do projektu pridané nové zdroje, synchronizácia pomáha zaručiť, že sú k dispozícii aktualizované informácie z kalendára.</span><span class="sxs-lookup"><span data-stu-id="43998-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="43998-116">Túto synchronizáciu je možné vykonať kedykoľvek.</span><span class="sxs-lookup"><span data-stu-id="43998-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="43998-117">Odporúčame používať dávku.</span><span class="sxs-lookup"><span data-stu-id="43998-117">We recommend that you use a batch.</span></span> <span data-ttu-id="43998-118">Možnosti sú k dispozícii počas synchronizácie rezervácií kapacity.</span><span class="sxs-lookup"><span data-stu-id="43998-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="43998-119">Vyberte **Projektové riadenie a účtovníctvo** &gt; **Pravidelne** &gt; **Synchronizácia kapacity** &gt; **Synchronizácia súhrnov kapacity zdroja**.</span><span class="sxs-lookup"><span data-stu-id="43998-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="43998-120">Nastavte možnosti v nasledujúcej tabuľke.</span><span class="sxs-lookup"><span data-stu-id="43998-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="43998-121">Možnosť</span><span class="sxs-lookup"><span data-stu-id="43998-121">Option</span></span>      | <span data-ttu-id="43998-122">Popis</span><span class="sxs-lookup"><span data-stu-id="43998-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="43998-123">Kód obdobia</span><span class="sxs-lookup"><span data-stu-id="43998-123">Period code</span></span> | <span data-ttu-id="43998-124">Voliteľne vyberte kód intervalu dátumu hlavnej účtovnej knihy, aby ste nastavili dátumy začiatku a konca procesu synchronizácie pre súhrn kapacity zdrojov.</span><span class="sxs-lookup"><span data-stu-id="43998-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="43998-125">Počiatočný dátum</span><span class="sxs-lookup"><span data-stu-id="43998-125">Start date</span></span>  | <span data-ttu-id="43998-126">Zadajte dátum začatia procesu synchronizácie pre súhrn kapacity zdrojov.</span><span class="sxs-lookup"><span data-stu-id="43998-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="43998-127">Dátum skončenia</span><span class="sxs-lookup"><span data-stu-id="43998-127">End date</span></span>    | <span data-ttu-id="43998-128">Zadajte dátum ukončenia procesu synchronizácie pre súhrn kapacity zdrojov.</span><span class="sxs-lookup"><span data-stu-id="43998-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="43998-129">[![Proces synchronizácie](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="43998-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]