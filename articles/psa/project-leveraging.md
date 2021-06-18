---
title: Odhady predaja a projekty
description: Táto téma poskytuje informácie o tom, ako využiť plán a odhady v procese predaja.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 49d109be3d55e7f208edb2698e420f40bb7843df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998430"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="bf85f-103">Odhady predaja a projekty</span><span class="sxs-lookup"><span data-stu-id="bf85f-103">Sales estimates and projects</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bf85f-104">Počas procesu predaja môžete vytvoriť odhady predaja prepojením projektu s predajnou cenovou ponukou.</span><span class="sxs-lookup"><span data-stu-id="bf85f-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="bf85f-105">Týmto spôsobom sa môže vyskytnúť definovaný odhad počas predajného procesu, aby sa využili výhody možnosti plánovania a odhadu projektu.</span><span class="sxs-lookup"><span data-stu-id="bf85f-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="bf85f-106">Ak predaj prekročí, plán, ktorý bol použitý na účely odhadu predaja, môže byť použitý ako základ pre ďalšie upresnenie projektového plánu.</span><span class="sxs-lookup"><span data-stu-id="bf85f-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="bf85f-107">Prepojenie projektu s riadkom cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="bf85f-107">Linking a project to a quote line</span></span>

<span data-ttu-id="bf85f-108">Keď vytvoríte riadok cenovej ponuky založený na projekte, môžete vytvoriť nový projekt alebo priradiť existujúci projekt na stránke **riadok cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="bf85f-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Formulár riadka cenovej ponuky](media/project-8.png)
 
<span data-ttu-id="bf85f-110">Keď vytvoríte nový projekt z podrobností riadka cenovej ponuky, môžete využiť šablóny projektu.</span><span class="sxs-lookup"><span data-stu-id="bf85f-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="bf85f-111">Šablóny projektu sú modelové projekty, ktoré predstavujú štandardné projektové plány a finančné odhady, ktoré sú typické pre organizáciu.</span><span class="sxs-lookup"><span data-stu-id="bf85f-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="bf85f-112">Môžu tiež reprezentovať kópie projektových plánov a odhadov z minulých projektov.</span><span class="sxs-lookup"><span data-stu-id="bf85f-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Podrobnosti o riadku cenovej ponuky](media/project-9.png)
  
<span data-ttu-id="bf85f-114">Keď vytvoríte projekt z cenovej ponuky, projekt sa automaticky priradí k riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="bf85f-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="bf85f-115">Zložky odhadov v projekte</span><span class="sxs-lookup"><span data-stu-id="bf85f-115">Components of estimates in a project</span></span>

<span data-ttu-id="bf85f-116">Plán vám umožňuje rozdeliť prácu na úlohy, udržiavať hierarchiu úloh, určiť, aké zdroje sú potrebné na dokončenie úlohy a priradiť odhad úsilia, ktoré je potrebné na dokončenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="bf85f-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="bf85f-117">Pracovné úsilie a odhady plánu môžete definovať pomocou polí na karte **plán** na stránke **projekt**.</span><span class="sxs-lookup"><span data-stu-id="bf85f-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="bf85f-118">Keďže je v projekte priradený cenník, finančné odhady sa vypočítavajú pomocou nákladov a predajných cien definovaných v ceníku.</span><span class="sxs-lookup"><span data-stu-id="bf85f-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="bf85f-119">Import odhadov z projektu do cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="bf85f-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="bf85f-120">Po definovaní odhadov projektu ich môžete importovať do riadka cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="bf85f-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="bf85f-121">Na stránke **Podrobnosti riadka cenovej** vyberte položku **importovať z odhadov** na páse s nástrojmi a zhrňte odhady projektov podľa typu transakcie, roly alebo úlohy.</span><span class="sxs-lookup"><span data-stu-id="bf85f-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]