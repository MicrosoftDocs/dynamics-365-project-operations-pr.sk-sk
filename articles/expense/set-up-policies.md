---
title: Definovanie politík výdavkov
description: Môžete definovať politiky výdavkov, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fbab7fd94fa429876216ee82b716da8d847fb01a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896660"
---
# <a name="define-expense-policies"></a><span data-ttu-id="bd19c-103">Definovanie politík výdavkov</span><span class="sxs-lookup"><span data-stu-id="bd19c-103">Define expense policies</span></span>

<span data-ttu-id="bd19c-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="bd19c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bd19c-105">Môžete definovať politiky, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="bd19c-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="bd19c-106">Implementácia politík výdavkov vám môže pomôcť efektívne riadiť výdavky.</span><span class="sxs-lookup"><span data-stu-id="bd19c-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="bd19c-107">Napríklad môžete nastaviť politiku pre hotelové výdavky v New Yorku, kde sa uvádza, že náklady na noc nemôžu prekročiť 250 USD.</span><span class="sxs-lookup"><span data-stu-id="bd19c-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="bd19c-108">Ak pracovník predloží výkaz výdavkov alebo cestovnú žiadanku, kde cena za izbu presahuje túto sumu, systém o tom informuje</span><span class="sxs-lookup"><span data-stu-id="bd19c-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="bd19c-109">pracovníka, že bola prekročená suma výdavku určená politikou.</span><span class="sxs-lookup"><span data-stu-id="bd19c-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="bd19c-110">Môžete nakonfigurovať správu, ktorú pracovník dostane, keď</span><span class="sxs-lookup"><span data-stu-id="bd19c-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="bd19c-111">budete definovať politiku.</span><span class="sxs-lookup"><span data-stu-id="bd19c-111">define the policy.</span></span>      
        
<span data-ttu-id="bd19c-112">Môžete definovať tri typy politík:</span><span class="sxs-lookup"><span data-stu-id="bd19c-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="bd19c-113">**Varovanie**: Umožňuje pracovníkovi predložiť výkaz výdavkov alebo cestovnú požiadavku, ale výdavok bude označený pre všetkých schvaľovateľov a</span><span class="sxs-lookup"><span data-stu-id="bd19c-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="bd19c-114">neskoršie hlásenie.</span><span class="sxs-lookup"><span data-stu-id="bd19c-114">for later reporting.</span></span>        

- <span data-ttu-id="bd19c-115">**Chyba**: Vyžaduje, aby pracovník pred predložením výkazu výdavkov alebo cestovnej žiadanky prehodnotil výdavky tak, aby boli v súlade s politikou.</span><span class="sxs-lookup"><span data-stu-id="bd19c-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="bd19c-116">**Odôvodnenie**: Vyžaduje, aby pracovník alebo vedúci pracovník pred odoslaním výkazu výdavkov alebo cestovnej žiadanky uviedol zdôvodnenie prekročenia sumy definovanej politikou.</span><span class="sxs-lookup"><span data-stu-id="bd19c-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="bd19c-117">Tipy týkajúce sa politiky</span><span class="sxs-lookup"><span data-stu-id="bd19c-117">Policy tips</span></span>
<span data-ttu-id="bd19c-118">Tu je niekoľko návrhov, ktoré vám môžu pomôcť pri vytváraní nových politík pre riadenie výdavkov:</span><span class="sxs-lookup"><span data-stu-id="bd19c-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="bd19c-119">Politiky sú účinné od dátumu, čo znamená, že politika nenadobudne účinnosť, ak je vytvorené po dátume, keď došlo k výdavku.</span><span class="sxs-lookup"><span data-stu-id="bd19c-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="bd19c-120">Napríklad dnes vytvoríte novú politiku, ktorý sa má vynucovať, s maximálnym výdavkom na jedlo vo výške 50 USD.</span><span class="sxs-lookup"><span data-stu-id="bd19c-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="bd19c-121">Všetky existujúce výdavky zadané do včera sa nebudú kontrolovať z hľadiska tejto politiky.</span><span class="sxs-lookup"><span data-stu-id="bd19c-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="bd19c-122">Pri vytváraní politiky pre kategóriu výdavkov, ktoré je možné rozpisovať, zvážte pridanie podmienky pre typ riadku výdavkov.</span><span class="sxs-lookup"><span data-stu-id="bd19c-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="bd19c-123">Niektoré politiky, napríklad vyžadovanie účtenky, nemusia mať pre rozpísané riadky zmysel.</span><span class="sxs-lookup"><span data-stu-id="bd19c-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="bd19c-124">V tejto situácii sa politika použije iba na riadok hlavičky alebo na riadok, ktorý nie je rozpísaný.</span><span class="sxs-lookup"><span data-stu-id="bd19c-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="bd19c-125">Politiky riadenia výdavkov sa štandardne vyhodnocujú voči zdrojovej entite.</span><span class="sxs-lookup"><span data-stu-id="bd19c-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="bd19c-126">Pre medzipodnikové scenáre môžete nastaviť, aby sa politika namiesto toho vyhodnocovala voči cieľovej entite (entite, ktorá si požičiava).</span><span class="sxs-lookup"><span data-stu-id="bd19c-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="bd19c-127">Ak chcete spúšťať politiky proti cieľovej entite, zapnite funkciu **Vyhodnocovať politiku výdavkov voči požičiavajúcej si právnickej entite** v pracovnom priestore **Správa funkcií**.</span><span class="sxs-lookup"><span data-stu-id="bd19c-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="bd19c-128">Kedy vyhodnocovať politiky</span><span class="sxs-lookup"><span data-stu-id="bd19c-128">When to evaluate policies</span></span>

<span data-ttu-id="bd19c-129">V parametroch riadenia výdavkov môžete zvoliť vyhodnotenie politík riadenia výdavkov pri uložení riadku alebo pri odoslaní výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="bd19c-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="bd19c-130">Ak sa rozhodnete vyhodnocovať pri ukladaní riadka, používatelia budú mať skôr prehľad o tom, čo musia urobiť, aby mohli vyplniť výkaz výdavkov naraz.</span><span class="sxs-lookup"><span data-stu-id="bd19c-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="bd19c-131">V opačnom prípade môžete oddialiť vyhodnotenie politiky a ušetriť čas overením na konci, počas odosielania do pracovného postupu.</span><span class="sxs-lookup"><span data-stu-id="bd19c-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
