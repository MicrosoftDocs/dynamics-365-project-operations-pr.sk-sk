---
title: Definovanie odborností a spôsobilostí
description: Táto téma poskytuje informácie o nastavovaní modulov spôsobilosti na hodnotenie zdrojov.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9376e0b268a3ab682716da604ceecfa1e878da68
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897650"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="ae59f-103">Definovanie odborností a spôsobilostí</span><span class="sxs-lookup"><span data-stu-id="ae59f-103">Define skills and proficiencies</span></span>

<span data-ttu-id="ae59f-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="ae59f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ae59f-105">Odbornosti sú charakteristiky zdrojov, ktoré sú zdieľané medzi Dynamics 365 Project Operations a prípadne aj Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="ae59f-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="ae59f-106">Ak chcete zachovať úložisko zručností v Project Operations, prejdite do ponuky **Zdroje** \> **Odbornosti zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="ae59f-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="ae59f-107">Používanie modelov odbornosti na hodnotenie zdrojov</span><span class="sxs-lookup"><span data-stu-id="ae59f-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="ae59f-108">Zručnosti pre zdroje sú hodnotené podľa modelov odbornosti.</span><span class="sxs-lookup"><span data-stu-id="ae59f-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="ae59f-109">Jednotlivé hodnotenia sú v modeli odbornosti.</span><span class="sxs-lookup"><span data-stu-id="ae59f-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="ae59f-110">Ak chcete vytvoriť model odbornosti, prejdite na **Zdroje** \> **Modely spôsobilosti** a potom stlačte možnosť **Nový**.</span><span class="sxs-lookup"><span data-stu-id="ae59f-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="ae59f-111">V novom modeli hodnotenia zadajte minimálnu hodnotu hodnotenia, maximálnu hodnotu hodnotenia a entitu, ktorá je hodnotená.</span><span class="sxs-lookup"><span data-stu-id="ae59f-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="ae59f-112">V podmriežke **Hodnoty hodnotenia** môžete definovať rôzne hodnoty hodnotenia od minimálnej po maximum.</span><span class="sxs-lookup"><span data-stu-id="ae59f-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="ae59f-113">Tieto hodnoty hodnotenia sa zobrazujú vo filtroch **Požiadavky na zdroje**, **Tabuľa plánovania** a **Asistent plánovania**.</span><span class="sxs-lookup"><span data-stu-id="ae59f-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
