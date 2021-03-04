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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146367"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="bfbe6-103">Prečo je cena v prípade skutočných výdavkových nákladov predvolene nulová</span><span class="sxs-lookup"><span data-stu-id="bfbe6-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="bfbe6-104">Tieto najčastejšie otázky sa vzťahuje na skutočné výdavky, kde je trieda transakcie stanovená na Výdavky a typ nákladov.</span><span class="sxs-lookup"><span data-stu-id="bfbe6-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="bfbe6-105">Riešenie problémov so sadbami nákladov pri skutočných výdavkových nákladoch</span><span class="sxs-lookup"><span data-stu-id="bfbe6-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="bfbe6-106">Prejdite na súvisiace záznam výdavku a presvedčte sa, že v zadávacom poli výdavku je uvedená suma.</span><span class="sxs-lookup"><span data-stu-id="bfbe6-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="bfbe6-107">Ak záznam pôvodného výdavku nemá vyplnené pole sumy, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="bfbe6-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="bfbe6-108">Ak chcete vyriešiť tento problém, znova vytvorte záznam výdavku s platnou sumou a odsúhlaste ho.</span><span class="sxs-lookup"><span data-stu-id="bfbe6-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
