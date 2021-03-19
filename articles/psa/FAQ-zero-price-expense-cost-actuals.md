---
title: Prečo je predvolene cena na skutočných nákladoch nulová?
description: Riešenie problémov, keď je predvolená cena 0 na skutočných výdavkových nákladoch.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: 742b0b9c495b4b3ecb4705be3ece5656f0322ca9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285874"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="ab52f-103">Prečo je cena v prípade skutočných výdavkových nákladov predvolene nulová</span><span class="sxs-lookup"><span data-stu-id="ab52f-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="ab52f-104">Tieto najčastejšie otázky sa vzťahuje na skutočné výdavky, kde je trieda transakcie stanovená na Výdavky a typ nákladov.</span><span class="sxs-lookup"><span data-stu-id="ab52f-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="ab52f-105">Riešenie problémov so sadbami nákladov pri skutočných výdavkových nákladoch</span><span class="sxs-lookup"><span data-stu-id="ab52f-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="ab52f-106">Prejdite na súvisiace záznam výdavku a presvedčte sa, že v zadávacom poli výdavku je uvedená suma.</span><span class="sxs-lookup"><span data-stu-id="ab52f-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="ab52f-107">Ak záznam pôvodného výdavku nemá vyplnené pole sumy, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="ab52f-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="ab52f-108">Ak chcete vyriešiť tento problém, znova vytvorte záznam výdavku s platnou sumou a odsúhlaste ho.</span><span class="sxs-lookup"><span data-stu-id="ab52f-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]