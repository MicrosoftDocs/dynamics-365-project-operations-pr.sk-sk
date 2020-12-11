---
title: Riadky príležitostí založených na produkte – čiastočné
description: Táto téma poskytuje informácie o riadkových položkách príležitostí založených na produktoch v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fd32bedb94cf36f706c112a845f342d9dde19805
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176359"
---
# <a name="product-based-opportunity-lines---lite"></a><span data-ttu-id="0d32d-103">Riadky príležitostí založených na produkte – čiastočné</span><span class="sxs-lookup"><span data-stu-id="0d32d-103">Product-based opportunity lines - lite</span></span>

<span data-ttu-id="0d32d-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="0d32d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0d32d-105">Riadky príležitostí založených na projekte sú riadkové položky v časti Príležitosť.</span><span class="sxs-lookup"><span data-stu-id="0d32d-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="0d32d-106">Tieto riadky sa zákazníkovi dodávajú ako samostatné riadkové položky na prípadnej faktúre bez akýchkoľvek ďalších služieb s pridanou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="0d32d-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="0d32d-107">Súvisiace výdavky a spotreba sa nesledujú pri úlohách žiadnych súvisiacich projektov.</span><span class="sxs-lookup"><span data-stu-id="0d32d-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="0d32d-108">Riadky založené na produktoch môžu byť katalógové položky alebo produkty určené na zápis.</span><span class="sxs-lookup"><span data-stu-id="0d32d-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="0d32d-109">Väčšina funkcií riadkov založených na produkte príležitosti sleduje funkcie poskytované aplikáciou Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="0d32d-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="0d32d-110">Ďalšie informácie o riadkoch príležitostí založených na projekte nájdete v časti [Pridávanie produktov k príležitosti](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="0d32d-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="0d32d-111">Jedným z konceptov príležitostí založených na produkte, ktorý je špecifický pre príležitosti založené na projekte je **Rozpočet zákazníka**.</span><span class="sxs-lookup"><span data-stu-id="0d32d-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="0d32d-112">Toto pole slúži na sledovanie sumy, ktorú je zákazník ochotný zaplatiť za položku riadka.</span><span class="sxs-lookup"><span data-stu-id="0d32d-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="0d32d-113">Ak je metóda výnosu v súhrne príležitostí nastavená na **Vypočítané systémom** zosumarizujú sa hodnoty rozpočtu zákazníka naprieč produktovými a projektovými riadkami na výpočet odhadovaných výnosov.</span><span class="sxs-lookup"><span data-stu-id="0d32d-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>