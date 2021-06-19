---
title: Project Service Automation – prehľad
description: Táto téma obsahuje informácie o riešení integrácie Dynamics 365 Project Service Automation do Dynamics 365 Finance.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005900"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="76a69-103">Project Service Automation – prehľad</span><span class="sxs-lookup"><span data-stu-id="76a69-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="76a69-104">Integračné riešenie Project Service Automation do služby Finance využíva funkciu Integrácia údajov na synchronizáciu údajov naprieč inštanciami Dynamics 365 Finance a Dynamics 365 Project Service Automation cez Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="76a69-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="76a69-105">Integračné šablóny, ktoré sú k dispozícii s funkciou Integrácia údajov, umožňujú tok projektov, projektových zmlúv, riadkov projektových zmlúv, medzníkov riadkov projektových zmlúv, projektových úloh, kategórií transakcií výdavkov, odhadov hodín a odhadov výdavkov z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="76a69-106">Ak používate verziu 7.3.0, musíte nainštalovať KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="76a69-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="76a69-107">Potom budete môcť integrovať projekty s pevnou cenou.</span><span class="sxs-lookup"><span data-stu-id="76a69-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="76a69-108">Ak používate verziu 7.3.0 a prenášate transakcie poplatkov z Project Service Automation, musíte nainštalovať KB 4345320, aby ste mohli zahrnúť tieto poplatky do faktúry za projekt.</span><span class="sxs-lookup"><span data-stu-id="76a69-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="76a69-109">Ak používate verziu 8.0, budete môcť používať integráciu projektovej úlohy, kategórie výdavkov na transakciu, odhady hodín, odhady výdavkov a blokovanie funkcií.</span><span class="sxs-lookup"><span data-stu-id="76a69-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="76a69-110">Ak používate verziu 8.0.1 alebo novšiu, budete môcť synchronizovať skutočné údaje.</span><span class="sxs-lookup"><span data-stu-id="76a69-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="76a69-111">Predtým, ako budete môcť integrovať Project Service Automation Finance, musíte nakonfigurovať parametre integrácie Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="76a69-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="76a69-112">Pre ďalšie informácie si pozrite [Parametre integrácie Project Service Automation](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="76a69-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="76a69-113">Toto integračné riešenie umožňuje priamu synchronizáciu v nasledujúcich scenároch:</span><span class="sxs-lookup"><span data-stu-id="76a69-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="76a69-114">Udržiavanie projektových zmlúv v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="76a69-115">Vytváranie projektov v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="76a69-116">Udržiavanie riadkov projektových zmlúv v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="76a69-117">Udržiavanie medzníkov riadkov projektových zmlúv v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="76a69-118">Udržiavanie projektových úloh v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="76a69-119">Udržiavanie kategórií výdavkov na transakciu vo Finance a ich priama synchronizácia z Finance do Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="76a69-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="76a69-120">Vytváranie odhadov hodín projektov v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="76a69-121">Vytváranie odhadov výdavkov na projekty v Project Service Automation a ich priama synchronizácia z Project Service Automation do Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="76a69-122">Vytváranie skutočných údajov o projektov, výdavkoch a poplatkoch v Project Service Automation a vytvorenie transakcií projektov v integračnom žurnále Project Service Automation, aby ich bolo možné zverejniť v službe Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="76a69-123">Synchronizácia údajov</span><span class="sxs-lookup"><span data-stu-id="76a69-123">Data synchronization</span></span>

<span data-ttu-id="76a69-124">Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje ako súčasť integrácie medzi Project Service Automation a Finance.</span><span class="sxs-lookup"><span data-stu-id="76a69-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="76a69-125">Nie všetky šablóny sú momentálne k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="76a69-125">Not all templates are currently available.</span></span> <span data-ttu-id="76a69-126">Šablóny budú vydané hneď po dokončení.</span><span class="sxs-lookup"><span data-stu-id="76a69-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="76a69-127">[![Integrácia Project Service Automation s Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="76a69-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="76a69-128">Systémové požiadavky na Finance</span><span class="sxs-lookup"><span data-stu-id="76a69-128">System requirements for Finance</span></span>

<span data-ttu-id="76a69-129">Ak chcete použiť riešenie integrácie Project Service Automation do Finance, musíte si nainštalovať Enterprise edition 7.3 s aktualizáciou platformy 12 alebo novšou.</span><span class="sxs-lookup"><span data-stu-id="76a69-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="76a69-130">Systémové požiadavky na Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="76a69-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="76a69-131">Ak chcete použiť riešenie integrácie Project Service Automation do Finance, musíte si nainštalovať nasledujúce komponenty:</span><span class="sxs-lookup"><span data-stu-id="76a69-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="76a69-132">Dynamics 365 Project Service Automation verzia 9.0.0.0 alebo novšia</span><span class="sxs-lookup"><span data-stu-id="76a69-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="76a69-133">Riešenie Od záujemcu po platbu pre Dynamics 365 Sales, verzia 1.14.0.0 (v14) alebo novšia</span><span class="sxs-lookup"><span data-stu-id="76a69-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="76a69-134">Riešenie Project Service Automation do Finance pre Dynamics 365 Project Service Automation, verzia 1.0.0.0 alebo novšia</span><span class="sxs-lookup"><span data-stu-id="76a69-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="76a69-135">Nainštalujte si do svojej inštancie Project Service Automation integračné riešenie Project Service Automation do Finance</span><span class="sxs-lookup"><span data-stu-id="76a69-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="76a69-136">Stiahnite si integračné riešenie Project Service Automation do Finance z [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016) a postupujte podľa pokynov, ktoré sú súčasťou riešenia.</span><span class="sxs-lookup"><span data-stu-id="76a69-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]