---
title: Definovanie odborností a spôsobilostí
description: Táto téma poskytuje informácie o nastavovaní modulov spôsobilosti na hodnotenie zdrojov.
author: ruhercul
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 982f64677b74f2195eacc287fc07b80c34f7acc0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6015350"
---
# <a name="define-skills-and-proficiencies"></a><span data-ttu-id="05b62-103">Definovanie odborností a spôsobilostí</span><span class="sxs-lookup"><span data-stu-id="05b62-103">Define skills and proficiencies</span></span>

<span data-ttu-id="05b62-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="05b62-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="05b62-105">Zručnosti sú charakteristiky zdrojov, ktoré sú zdieľané medzi Dynamics 365 Project Operations a prípadne aj Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="05b62-105">Skills are resource characteristics that are shared between Dynamics 365 Project Operations and if present, Dynamics 365 Field Service.</span></span> 

- <span data-ttu-id="05b62-106">Ak chcete zachovať úložisko zručností v Project Operations, prejdite do ponuky **Zdroje** \> **Odbornosti zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="05b62-106">To maintain the repository of skills in Project Operations, go to **Resources** \> **Resource Skills**.</span></span> 

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="05b62-107">Používanie modelov odbornosti na hodnotenie zdrojov</span><span class="sxs-lookup"><span data-stu-id="05b62-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="05b62-108">Zručnosti pre zdroje sú hodnotené podľa modelov odbornosti.</span><span class="sxs-lookup"><span data-stu-id="05b62-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="05b62-109">Jednotlivé hodnotenia sú v modeli odbornosti.</span><span class="sxs-lookup"><span data-stu-id="05b62-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="05b62-110">Ak chcete vytvoriť model odbornosti, prejdite na **Zdroje** \> **Modely spôsobilosti** a potom stlačte možnosť **Nový**.</span><span class="sxs-lookup"><span data-stu-id="05b62-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="05b62-111">V novom modeli hodnotenia zadajte minimálnu hodnotu hodnotenia, maximálnu hodnotu hodnotenia a entitu, ktorá je hodnotená.</span><span class="sxs-lookup"><span data-stu-id="05b62-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="05b62-112">Vo vedľajšej mriežke **Hodnoty hodnotenia** môžete definovať rôzne hodnoty hodnotenia od minimálnej po maximum.</span><span class="sxs-lookup"><span data-stu-id="05b62-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>


<span data-ttu-id="05b62-113">Tieto hodnoty hodnotenia sa zobrazujú vo filtroch **Požiadavky na zdroje**, **Tabuľa plánovania** a **Asistent plánovania**.</span><span class="sxs-lookup"><span data-stu-id="05b62-113">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]