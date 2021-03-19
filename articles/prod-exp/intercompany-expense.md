---
title: Medzipodnikové výdavky
description: Táto téma poskytuje informácie o spôsobe použitia medzipodnikových výdavkov na priradenie výdavkov pracovníka k právnickej osobe, pre ktorú bola práca vykonaná.
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
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271552"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="dd9a9-103">Medzipodnikové výdavky</span><span class="sxs-lookup"><span data-stu-id="dd9a9-103">Intercompany expenses</span></span>

<span data-ttu-id="dd9a9-104">Pracovník, ktorý je zamestnaný v jednej právnickej entite v organizácii, môže vykonávať prácu pre inú právnickú entitu v tej istej organizácii.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="dd9a9-105">Môžete použiť medzipodnikové výdavky na priradenie výdavkov pracovníka k právnickej osobe, pre ktorú bola práca vykonaná.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="dd9a9-106">Právnická entita, ktorá zamestnáva pracovníka, sa nazýva požičiavajúca právnická entita.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="dd9a9-107">Právnická entita, za ktorú pracovník znáša výdavky, sa nazýva požičiavajúca si právnická entita.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="dd9a9-108">Predtým, ako pracovník bude môcť vytvárať a odosielať medzipodnikové výdavky, musíte povoliť riadky medzipodnikových výdavkov.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="dd9a9-109">V prenajímajúcej právnickej osobe na stránke **Parametre riadenia výdavkov** vyberte možnosť **Povoliť riadky medzipodnikových výdavkov**.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="dd9a9-110">Zaúčtovanie dane pre medzipodnikové náklady</span><span class="sxs-lookup"><span data-stu-id="dd9a9-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dd9a9-111">Predtým, ako budete môcť vo svojom výkaze výdavkov použiť daňové skupiny spojené s požičiavajúcou (zdrojovou) právnickou osobou namiesto požičiavajúcej (cieľovej) právnickej osoby, musíte povoliť funkciu v nastavení dane z obratu hlavnej knihy.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="dd9a9-112">Keď je parameter **Právnická osoba pre účtovanie medzipodnikových daní** nastavený na **Zdroj** a možnosť **Použiť pravidlá zdaňovania dane z obratu** je nastavená na **Nie**, použije sa daňová kombinácia pre požičiavajúcu právnickú osobu.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="dd9a9-113">Keď je rovnaký parameter nastavený na **Cieľ**, použije sa daňová kombinácia pre požičiavajúcu si právnickú entitu.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="dd9a9-114">Pre právnické entity v Spojených štátoch, keď je parameter nastavený na **Zdroj**, musí byť pole **Pohľadávka z obratu** nakonfigurované aj na novej stránke **Skupiny účtovania v hlavnej knihe**.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="dd9a9-115">Účtovný nástroj použije informácie z tohto poľa pre účtovný záznam súvisiaci s daňou.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="dd9a9-116">Správanie je konzistentné pre riadky výdavkov zaúčtované s projektom alebo bez neho.</span><span class="sxs-lookup"><span data-stu-id="dd9a9-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]