---
title: Medzipodnikové výdavky
description: Pracovník, ktorý je zamestnaný v jednej právnickej entite v organizácii, môže vykonávať prácu pre inú právnickú entitu v tej istej organizácii. V tejto situácii môžete pomocou funkcie medzipodnikových výdavkov priradiť výdavky pracovníka právnickej entite, pre ktorú bola práca vykonaná.
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084515"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="1f32a-104">Medzipodnikové výdavky</span><span class="sxs-lookup"><span data-stu-id="1f32a-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f32a-105">Pracovník, ktorý je zamestnaný v jednej právnickej entite v organizácii, môže vykonávať prácu pre inú právnickú entitu v tej istej organizácii.</span><span class="sxs-lookup"><span data-stu-id="1f32a-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="1f32a-106">V tejto situácii môžete pomocou funkcie medzipodnikových výdavkov priradiť výdavky pracovníka právnickej entite, pre ktorú bola práca vykonaná.</span><span class="sxs-lookup"><span data-stu-id="1f32a-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="1f32a-107">Právnická entita, ktorá zamestnáva pracovníka, sa nazýva požičiavajúca právnická entita.</span><span class="sxs-lookup"><span data-stu-id="1f32a-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="1f32a-108">Právnická entita, za ktorú pracovník znáša výdavky, sa nazýva požičiavajúca si právnická entita.</span><span class="sxs-lookup"><span data-stu-id="1f32a-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="1f32a-109">Predtým, ako pracovník môže vytvoriť a odoslať výdavky na prácu, ktorá sa vykonáva pre inú právnickú entitu, v požičiavajúcej právnickej osobe, na stránke **Parametre správy výdavkov** vyberte možnosť **Povoliť medzipodnikové riadky výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="1f32a-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="1f32a-110">Zaúčtovanie dane pre medzipodnikové náklady</span><span class="sxs-lookup"><span data-stu-id="1f32a-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f32a-111">Ak chcete vo výkaze výdavkov použiť daňové skupiny, ktoré sú spojené s požičiavajúcou (zdrojovou) právnickou entitou, namiesto požičiavajúcej si (cieľovej) právnickej entity, budete to musieť nakonfigurovať v nastavení dane z predaja v hlavnej knihe.</span><span class="sxs-lookup"><span data-stu-id="1f32a-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="1f32a-112">Keď je parameter hlavnej knihy **Právnická entita pre účtovanie daní medzi spoločnosťami** nastavená na **Zdroj** a **Použiť pravidlá zdaňovania dane z predaja** je nastavená na **Nie** , použije sa daňová kombinácia pre požičiavajúcu právnickú entitu.</span><span class="sxs-lookup"><span data-stu-id="1f32a-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="1f32a-113">Keď je rovnaký parameter nastavený na **Cieľ** , použije sa daňová kombinácia pre požičiavajúcu si právnickú entitu.</span><span class="sxs-lookup"><span data-stu-id="1f32a-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="1f32a-114">Pre právnické entity v Spojených štátoch, keď je parameter nastavený na **Zdroj** , musí byť pole **Pohľadávka z obratu** nakonfigurované aj na novej stránke **Skupiny účtovania v hlavnej knihe**.</span><span class="sxs-lookup"><span data-stu-id="1f32a-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="1f32a-115">Účtovný nástroj použije informácie z tohto poľa pre účtovný záznam súvisiaci s daňou.</span><span class="sxs-lookup"><span data-stu-id="1f32a-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="1f32a-116">Správanie je konzistentné pre riadky výdavkov zaúčtované s projektom alebo bez neho.</span><span class="sxs-lookup"><span data-stu-id="1f32a-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
