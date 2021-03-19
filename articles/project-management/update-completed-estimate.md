---
title: Aktualizácia odhadu pri dokončení
description: Táto téma poskytuje informácie o aktualizácii projekcie úsilia na projekt.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 0e63bdb815a6f758c57d055c8c03d92e04700445
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286447"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="8c4c8-103">Aktualizácia odhadu pri dokončení</span><span class="sxs-lookup"><span data-stu-id="8c4c8-103">Update estimate at completion</span></span>

<span data-ttu-id="8c4c8-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="8c4c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8c4c8-105">Je bežné, že projektový manažér reviduje pôvodné odhady úlohy.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="8c4c8-106">Projektové opätovné predpoklady sú vnímaním odhadov projektovým manažérom vzhľadom na súčasný stav projektu.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="8c4c8-107">Neodporúčame však, aby projektoví manažéri menili základné čísla, pretože projektový základ predstavuje etablovaný zdroj pravdivých informácií pre plán projektu a odhad nákladov, čo odsúhlasili všetci účastníci projektu.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="8c4c8-108">Existujú dva spôsoby, ktoré projektový manažér môže znovu predpokladať úsilie na úlohy:</span><span class="sxs-lookup"><span data-stu-id="8c4c8-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="8c4c8-109">Prepísanie predvoleného odhadu času na dokončenie (ETC) s novým odhadom skutočného zostávajúceho úsilia na úlohe.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="8c4c8-110">Prepísať predvolené percento priebehu s novým odhadom skutočného priebehu úlohy.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="8c4c8-111">Každý z týchto prístupov spôsobuje prepočítanie ETC úlohy, odhadu na dokončenie (EAC) a percenta pokroku a odchýlku predpokladaného úsilia úlohy.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="8c4c8-112">EAC, ETC a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový návrh odchýlky úsilia.</span><span class="sxs-lookup"><span data-stu-id="8c4c8-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]