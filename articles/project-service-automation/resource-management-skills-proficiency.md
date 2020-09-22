---
title: Modely zručností a odbornosti
description: Táto téma poskytuje informácie o používaní zručností a modulov spôsobilosti.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755662"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="9ff1e-103">Modely zručností a odbornosti</span><span class="sxs-lookup"><span data-stu-id="9ff1e-103">Skills and proficiency models</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9ff1e-104">Zručnosti sú charakteristiky zdrojov, ktoré sú zdieľané medzi Dynamics 365 Project Service Automation a prípadne aj Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="9ff1e-105">Ak chcete zachovať úložisko zručností v Project Service Automation, prejdite do ponuky **Zdroje** \> **Odbornosti zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![Odbornosti zdrojov](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="9ff1e-107">Používanie modelov odbornosti na hodnotenie zdrojov</span><span class="sxs-lookup"><span data-stu-id="9ff1e-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="9ff1e-108">Zručnosti pre zdroje sú hodnotené podľa modelov odbornosti.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="9ff1e-109">Jednotlivé hodnotenia sú v modeli odbornosti.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="9ff1e-110">Ak chcete vytvoriť model odbornosti, prejdite na **Zdroje** \> **Modely spôsobilosti** a potom stlačte možnosť **Nový**.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="9ff1e-111">V novom modeli hodnotenia zadajte minimálnu hodnotu hodnotenia, maximálnu hodnotu hodnotenia a entitu, ktorá je hodnotená.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="9ff1e-112">V podmriežke **Hodnoty hodnotenia** môžete definovať rôzne hodnoty hodnotenia od minimálnej po maximum.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-112">In the **Rating Values** sub-grid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![Minimálne a maximálne definované hodnotenia](media/Resource-Management-image85.png)

<span data-ttu-id="9ff1e-114">Tieto hodnoty hodnotenia sa zobrazujú vo filtroch **Požiadavky na zdroje**, **Tabuľa plánovania** a **Asistent plánovania**.</span><span class="sxs-lookup"><span data-stu-id="9ff1e-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
