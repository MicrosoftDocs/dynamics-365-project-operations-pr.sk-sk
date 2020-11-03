---
title: Projektové predajné objednávky pre projekty typu „čas a materiál“
description: Táto téma vysvetľuje, ako vytvoriť projektové predajné objednávky pre projekty typu „čas a materiál“.
author: Yowelle
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 3653a6869dab323be88f1fd0f9fd0f2cb35c456f
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084349"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="0135e-103">Projektové predajné objednávky pre projekty typu „čas a materiál“</span><span class="sxs-lookup"><span data-stu-id="0135e-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0135e-104">Táto téma popisuje, ako vytvoriť predajnú objednávku pre projekt.</span><span class="sxs-lookup"><span data-stu-id="0135e-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="0135e-105">Predajné objednávky je možné vytvoriť iba pre projekty typu **čas a materiál**.</span><span class="sxs-lookup"><span data-stu-id="0135e-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="0135e-106">Ak má projekt typu „čas a materiál“ na projektovej zmluve viac zdrojov financovania, musíte povoliť parameter **Povoliť predajné objednávky pre projekty s viacerými zdrojmi financovania** na stránke **Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="0135e-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="0135e-107">Podpora pre projektové predajné objednávky s viacerými zdrojmi financovania je k dispozícii počnúc vydaním aplikácie 10.0.2 a vyšším.</span><span class="sxs-lookup"><span data-stu-id="0135e-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="0135e-108">Parameter umožňujúci podporu projektových predajných objednávok s viacerými zdrojmi financovania bude odstránený vo vlne vydania v apríli 2020, po ktorej bude táto funkcia vždy povolená.</span><span class="sxs-lookup"><span data-stu-id="0135e-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="0135e-109">Projektové predajné objednávky môžete vytvoriť dvoma spôsobmi:</span><span class="sxs-lookup"><span data-stu-id="0135e-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="0135e-110">Prejdite do samotného projektu.</span><span class="sxs-lookup"><span data-stu-id="0135e-110">Go to the project itself.</span></span> <span data-ttu-id="0135e-111">Na table Akcia vyberte možnosť **Spravovať > Úlohy položiek > Predajná objednávka**.</span><span class="sxs-lookup"><span data-stu-id="0135e-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="0135e-112">Informácie o projekte budú predvolene nastavené na predajnú objednávku z projektu.</span><span class="sxs-lookup"><span data-stu-id="0135e-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="0135e-113">Ak má projektová zmluva viac ako jeden zdroj financovania, budete musieť zvoliť zdroj financovania, aby ste zákazníka nastavili na predajnú objednávku.</span><span class="sxs-lookup"><span data-stu-id="0135e-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="0135e-114">Ak je pre projekt k dispozícii iba jeden zdroj financovania, zákazník sa nastaví automaticky.</span><span class="sxs-lookup"><span data-stu-id="0135e-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="0135e-115">Prejdite na stránku so zoznamom **Všetky predajné objednávky** a vytvorte novú predajnú objednávku.</span><span class="sxs-lookup"><span data-stu-id="0135e-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="0135e-116">Budete musieť vybrať projekt pre predajnú objednávku.</span><span class="sxs-lookup"><span data-stu-id="0135e-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="0135e-117">Po výbere projektu sa zákazník nastaví zo zdroja financovania alebo budete musieť zvoliť zdroj financovania, ak má projektová zmluva viac zdrojov financovania.</span><span class="sxs-lookup"><span data-stu-id="0135e-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

