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
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127222"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="26043-103">Aktualizácia odhadu pri dokončení</span><span class="sxs-lookup"><span data-stu-id="26043-103">Update estimate at completion</span></span>

<span data-ttu-id="26043-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="26043-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="26043-105">Je bežné, že projektový manažér reviduje pôvodné odhady úlohy.</span><span class="sxs-lookup"><span data-stu-id="26043-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="26043-106">Projektové opätovné predpoklady sú vnímaním odhadov projektovým manažérom vzhľadom na súčasný stav projektu.</span><span class="sxs-lookup"><span data-stu-id="26043-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="26043-107">Neodporúčame však, aby projektoví manažéri menili základné čísla, pretože projektový základ predstavuje etablovaný zdroj pravdivých informácií pre plán projektu a odhad nákladov, čo odsúhlasili všetci účastníci projektu.</span><span class="sxs-lookup"><span data-stu-id="26043-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="26043-108">Existujú dva spôsoby, ktoré projektový manažér môže znovu predpokladať úsilie na úlohy:</span><span class="sxs-lookup"><span data-stu-id="26043-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="26043-109">Prepísanie predvoleného odhadu času na dokončenie (ETC) s novým odhadom skutočného zostávajúceho úsilia na úlohe.</span><span class="sxs-lookup"><span data-stu-id="26043-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="26043-110">Prepísať predvolené percento priebehu s novým odhadom skutočného priebehu úlohy.</span><span class="sxs-lookup"><span data-stu-id="26043-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="26043-111">Každý z týchto prístupov spôsobuje prepočítanie ETC úlohy, odhadu na dokončenie (EAC) a percenta pokroku a odchýlku predpokladaného úsilia úlohy.</span><span class="sxs-lookup"><span data-stu-id="26043-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="26043-112">EAC, ETC a percento pokroku na súhrnných úlohách sú tiež prepočítané a vytvárajú nový návrh odchýlky úsilia.</span><span class="sxs-lookup"><span data-stu-id="26043-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
