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
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127398"
---
# <a name="resource-estimates"></a><span data-ttu-id="f6c2c-103">Odhady zdrojov</span><span class="sxs-lookup"><span data-stu-id="f6c2c-103">Resource estimates</span></span>

<span data-ttu-id="f6c2c-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="f6c2c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f6c2c-105">Odhady zdrojov pochádzajú z časovo odstupňovaného úsilia, ktoré je definované v štruktúre rozdelenia práce spolu s príslušnými cenovými dimenziami.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="f6c2c-106">Typický výpočet je **rýchlosť/hod. pre každú rolu x hodiny.**</span><span class="sxs-lookup"><span data-stu-id="f6c2c-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="f6c2c-107">Časovo odstupňované úsilie pre každý zdroj je uložené v zázname o priradení zdroja.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="f6c2c-108">Cena je uložená v preddefinovanom cenníku.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="f6c2c-109">Prevod jednotiek sa uplatňuje na základe príslušného cenníka.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-109">Unit conversion is applied based on the applicable price list.</span></span>

![Odhady zdrojov](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="f6c2c-111">Predvolená obstarávacia cena a mena nákladov</span><span class="sxs-lookup"><span data-stu-id="f6c2c-111">Default cost price and cost currency</span></span>

<span data-ttu-id="f6c2c-112">Obstarávacie ceny sú predvolené od organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="f6c2c-113">Predvolené sadzby fakturácie a meny predaja</span><span class="sxs-lookup"><span data-stu-id="f6c2c-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="f6c2c-114">Predajné ceny sa uplatňujú raz pre každú dohodu.</span><span class="sxs-lookup"><span data-stu-id="f6c2c-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="f6c2c-115">Hierarchia predvolených predajných cenníkov je nasledovná:</span><span class="sxs-lookup"><span data-stu-id="f6c2c-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="f6c2c-116">Organizácia</span><span class="sxs-lookup"><span data-stu-id="f6c2c-116">Organization</span></span>
2. <span data-ttu-id="f6c2c-117">Zákazník</span><span class="sxs-lookup"><span data-stu-id="f6c2c-117">Customer</span></span>
3. <span data-ttu-id="f6c2c-118">Cenová ponuka/zmluva</span><span class="sxs-lookup"><span data-stu-id="f6c2c-118">Quote/contract</span></span>
