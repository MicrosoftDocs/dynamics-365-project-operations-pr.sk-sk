---
title: Analýza projektových cenových ponúk
description: Táto téma poskytuje informácie o analýze projektových cenových ponúk.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: acb3f1a2020cfd59f60f828e9092bd7ccde00077
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012470"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="39d13-103">Analýza projektových cenových ponúk</span><span class="sxs-lookup"><span data-stu-id="39d13-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="39d13-104">Dynamics 365 Project Service Automation analyzuje projektové cenové ponuky na odhad ziskovosti.</span><span class="sxs-lookup"><span data-stu-id="39d13-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="39d13-105">Analyzuje tiež, ako dobre je cenová ponuka zarovnaná s očakávaniami zákazníkov o dátume doručenia alebo dátume dokončenia a o rozpočte.</span><span class="sxs-lookup"><span data-stu-id="39d13-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="39d13-106">Analýza ziskovosti</span><span class="sxs-lookup"><span data-stu-id="39d13-106">Profitability analysis</span></span>

<span data-ttu-id="39d13-107">Project Service Automation analyzuje ziskovosť pomocou hrubého zisku a upraveného hrubého zisku.</span><span class="sxs-lookup"><span data-stu-id="39d13-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="39d13-108">Hrubý zisk sa vypočítava pomocou nasledujúceho vzorca:</span><span class="sxs-lookup"><span data-stu-id="39d13-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="39d13-109">Upravený hrubý zisk sa vypočítava pomocou nasledujúceho vzorca:</span><span class="sxs-lookup"><span data-stu-id="39d13-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="39d13-110">Ak sa hodnoty pre hrubý zisk a upravený hrubý zisk líšia širokým rozpätím, veľká časť práce v cenovej ponuke je klasifikovaná ako neúčtovateľná.</span><span class="sxs-lookup"><span data-stu-id="39d13-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="39d13-111">Analýza očakávaní zákazníka</span><span class="sxs-lookup"><span data-stu-id="39d13-111">Analysis of customer expectations</span></span>

<span data-ttu-id="39d13-112">Ak zadáte hodnoty pre nasledujúce polia, môžete analyzovať cenové ponuky a generovať grafy pre očakávania zákazníkov týkajúce sa plánu a rozpočtu:</span><span class="sxs-lookup"><span data-stu-id="39d13-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="39d13-113">**Requested delivery date** pole v hlavičke cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="39d13-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="39d13-114">Pole **Customer budget** pre každý riadok cenovej ponuky (pre riadky založené na projekte a riadky založené na produkte).</span><span class="sxs-lookup"><span data-stu-id="39d13-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="39d13-115">Analýza očakávaní zákazníkov o harmonograme sa vykonáva porovnaním posledného koncového dátumu riadka cenovej ponuky s požadovaným dátumom doručenia vo všetkých riadkoch cenovej ponuky v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="39d13-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="39d13-116">Analýza očakávaní zákazníkov o rozpočte sa vykonáva porovnaním súčtu celkového rozpočtu zákazníka s ponúkanou sumou vo všetkých riadkoch cenových ponúk.</span><span class="sxs-lookup"><span data-stu-id="39d13-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]