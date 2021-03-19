---
title: Odhady zdrojov
description: Táto téma poskytuje informácie o tom, ako sa počítajú odhady zdrojov v Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286537"
---
# <a name="resource-estimates"></a><span data-ttu-id="d4e10-103">Odhady zdrojov</span><span class="sxs-lookup"><span data-stu-id="d4e10-103">Resource estimates</span></span>

<span data-ttu-id="d4e10-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="d4e10-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d4e10-105">Odhady zdrojov pochádzajú z časovo odstupňovaného úsilia, ktoré je definované v štruktúre rozdelenia práce spolu s príslušnými cenovými dimenziami.</span><span class="sxs-lookup"><span data-stu-id="d4e10-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="d4e10-106">Typický výpočet je **rýchlosť/hod. pre každú rolu x hodiny.**</span><span class="sxs-lookup"><span data-stu-id="d4e10-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="d4e10-107">Časovo odstupňované úsilie pre každý zdroj je uložené v zázname o priradení zdroja.</span><span class="sxs-lookup"><span data-stu-id="d4e10-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="d4e10-108">Cena je uložená v preddefinovanom cenníku.</span><span class="sxs-lookup"><span data-stu-id="d4e10-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="d4e10-109">Prevod jednotiek sa uplatňuje na základe príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="d4e10-109">Unit conversion is applied based on the applicable price list.</span></span>

![Odhady zdrojov](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="d4e10-111">Predvolená obstarávacia cena a mena nákladov</span><span class="sxs-lookup"><span data-stu-id="d4e10-111">Default cost price and cost currency</span></span>

<span data-ttu-id="d4e10-112">Obstarávacie ceny sú predvolené od organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="d4e10-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="d4e10-113">Predvolené sadzby fakturácie a meny predaja</span><span class="sxs-lookup"><span data-stu-id="d4e10-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="d4e10-114">Predajné ceny sa uplatňujú raz pre každú dohodu.</span><span class="sxs-lookup"><span data-stu-id="d4e10-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="d4e10-115">Hierarchia predvolených predajných cenníkov je nasledovná:</span><span class="sxs-lookup"><span data-stu-id="d4e10-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="d4e10-116">Organizácia</span><span class="sxs-lookup"><span data-stu-id="d4e10-116">Organization</span></span>
2. <span data-ttu-id="d4e10-117">Zákazník</span><span class="sxs-lookup"><span data-stu-id="d4e10-117">Customer</span></span>
3. <span data-ttu-id="d4e10-118">Cenová ponuka/zmluva</span><span class="sxs-lookup"><span data-stu-id="d4e10-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]