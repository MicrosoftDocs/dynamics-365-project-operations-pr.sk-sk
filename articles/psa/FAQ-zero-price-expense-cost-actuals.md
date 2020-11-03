---
title: Prečo je predvolene cena na skutočných nákladoch nulová?
description: Riešenie problémov, keď je predvolená cena 0 na skutočných výdavkových nákladoch.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: 9f4ff8a96250d675faeda3246c2d0a6c5bd83286
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084385"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="83d07-103">Prečo je predvolene cena na skutočných nákladoch nulová?</span><span class="sxs-lookup"><span data-stu-id="83d07-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="83d07-104">Tieto najčastejšie otázky sa vzťahuje na skutočné výdavky, kde je trieda transakcie stanovená na Výdavky a typ nákladov.</span><span class="sxs-lookup"><span data-stu-id="83d07-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="83d07-105">Riešenie problémov so sadbami nákladov pri skutočných výdavkových nákladoch</span><span class="sxs-lookup"><span data-stu-id="83d07-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="83d07-106">Prejdite na súvisiace záznam výdavku a presvedčte sa, že v zadávacom poli výdavku je uvedená suma.</span><span class="sxs-lookup"><span data-stu-id="83d07-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="83d07-107">Ak záznam pôvodného výdavku nemá vyplnené pole sumy, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="83d07-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="83d07-108">Ak chcete vyriešiť tento problém, znova vytvorte záznam výdavku s platnou sumou a odsúhlaste ho.</span><span class="sxs-lookup"><span data-stu-id="83d07-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
