---
title: Opravené faktúry
description: Táto téma poskytuje informácie o opravených faktúrach.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: b31e702cc15bbb3937e8c4b305064212f63ce919
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084532"
---
# <a name="corrected-invoices"></a><span data-ttu-id="8ac7c-103">Opravené faktúry</span><span class="sxs-lookup"><span data-stu-id="8ac7c-103">Corrected invoices</span></span>

<span data-ttu-id="8ac7c-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="8ac7c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="8ac7c-105">Potvrdené faktúry môžu byť editované.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="8ac7c-106">Keď upravíte potvrdenú faktúru, vytvorí sa koncept opravenej faktúry.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="8ac7c-107">Pretože predpoklad je, že chcete zvrátiť všetky transakcie a množstvá z pôvodnej faktúry, opravená faktúra obsahuje všetky transakcie z pôvodnej faktúry a všetky množstvá na nej sú 0 (nula).</span><span class="sxs-lookup"><span data-stu-id="8ac7c-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="8ac7c-108">Keď niektoré transakcie nevyžadujú opravu, môžete ich odstrániť z konceptu opravnej faktúry.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="8ac7c-109">Ak chcete zvrátiť alebo vrátiť iba čiastočné množstvo, môžete upraviť pole Množstvo v detaile riadka.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="8ac7c-110">Ak otvoríte detail riadka faktúry, môžete vidieť pôvodné množstvo faktúry.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="8ac7c-111">Potom môžete upraviť aktuálne množstvo faktúr tak, aby bolo menšie ako alebo väčšie ako pôvodné množstvo faktúry.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="8ac7c-112">Po potvrdení opravnej faktúry, sú stornované pôvodné fakturované skutočné hodnoty a sú vytvorené nové fakturované skutočné hodnoty predaja.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="8ac7c-113">Ak bolo množstvo znížené, rozdiel spôsobí nové vytvorenie ďalších nefakturovaných skutočných hodnôt predaja.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="8ac7c-114">Ak bol napríklad pôvodný fakturovaný predaj osem hodín a detail riadka opravenej faktúry má znížené množstvo šiestich hodín, pôvodný fakturovaný predajný riadok sa vráti späť a vytvoria dve nové skutočné hodnoty:</span><span class="sxs-lookup"><span data-stu-id="8ac7c-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="8ac7c-115">Skutočná hodnota fakturovaného predaja je šesť hodín.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="8ac7c-116">Skutočná hodnota nefakturovaného predaja sú dve hodiny.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="8ac7c-117">Táto transakcia môže byť fakturovaná neskôr alebo označená ako nefakturovateľná v závislosti od rokovaní so zákazníkom.</span><span class="sxs-lookup"><span data-stu-id="8ac7c-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>
