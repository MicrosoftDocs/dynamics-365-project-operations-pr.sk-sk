---
title: Prečo je predvolene cena na skutočných nákladoch nulová?
description: Riešenie problémov, keď je predvolená cena 0 na skutočných výdavkových nákladoch.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.prod: Project Service
ms.technology: ''
ms.assetid: bc1ebc58-c733-4310-8435-572ed9a9fef9
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 3fb678822877a61d141de75aea29b7d5cdf292c4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755578"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="8c03a-103">Prečo je predvolene cena na skutočných nákladoch nulová?</span><span class="sxs-lookup"><span data-stu-id="8c03a-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8c03a-104">Tieto najčastejšie otázky sa vzťahuje na skutočné výdavky, kde je trieda transakcie stanovená na Výdavky a typ nákladov.</span><span class="sxs-lookup"><span data-stu-id="8c03a-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="8c03a-105">Riešenie problémov so sadbami nákladov pri skutočných výdavkových nákladoch</span><span class="sxs-lookup"><span data-stu-id="8c03a-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="8c03a-106">Prejdite na súvisiace záznam výdavku a presvedčte sa, že v zadávacom poli výdavku je uvedená suma.</span><span class="sxs-lookup"><span data-stu-id="8c03a-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="8c03a-107">Ak záznam pôvodného výdavku nemá vyplnené pole sumy, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="8c03a-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="8c03a-108">Ak chcete vyriešiť tento problém, znova vytvorte záznam výdavku s platnou sumou a odsúhlaste ho.</span><span class="sxs-lookup"><span data-stu-id="8c03a-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
