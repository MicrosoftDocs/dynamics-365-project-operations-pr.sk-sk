---
title: Nastavenie politík výdavkov
description: Môžete stanoviť politiky výdavkov, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek v Microsoft Dynamics 365 Finance.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650113"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="6fce3-103">Nastavenie politík výdavkov</span><span class="sxs-lookup"><span data-stu-id="6fce3-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6fce3-104">Môžete definovať politiky, ktoré musia vaši pracovníci dodržiavať pri zadávaní a odosielaní výkazov výdavkov a cestovných požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="6fce3-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="6fce3-105">Implementácia politík výdavkov vám môže pomôcť efektívne riadiť výdavky.</span><span class="sxs-lookup"><span data-stu-id="6fce3-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="6fce3-106">Napríklad môžete nastaviť politiku pre hotelové výdavky v New Yorku, kde sa uvádza, že náklady na noc nemôžu prekročiť 250 USD.</span><span class="sxs-lookup"><span data-stu-id="6fce3-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="6fce3-107">Ak pracovník predloží výkaz výdavkov alebo cestovnú žiadanku, kde cena za izbu presahuje túto sumu, systém o tom informuje</span><span class="sxs-lookup"><span data-stu-id="6fce3-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="6fce3-108">pracovníka, že bola prekročená suma výdavku určená politikou.</span><span class="sxs-lookup"><span data-stu-id="6fce3-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="6fce3-109">Môžete nakonfigurovať správu, ktorú pracovník dostane, keď</span><span class="sxs-lookup"><span data-stu-id="6fce3-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="6fce3-110">budete definovať politiku.</span><span class="sxs-lookup"><span data-stu-id="6fce3-110">define the policy.</span></span>      
        
<span data-ttu-id="6fce3-111">Môžete definovať tri typy politík:</span><span class="sxs-lookup"><span data-stu-id="6fce3-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="6fce3-112">Varovanie – Umožňuje pracovníkovi predložiť výkaz výdavkov alebo cestovnú požiadavku, ale výdavok bude označený pre všetkých schvaľovateľov a</span><span class="sxs-lookup"><span data-stu-id="6fce3-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="6fce3-113">neskoršie hlásenie.</span><span class="sxs-lookup"><span data-stu-id="6fce3-113">for later reporting.</span></span>        

- <span data-ttu-id="6fce3-114">Chyba – Vyžaduje, aby pracovník pred predložením výkazu výdavkov alebo cestovnej žiadanky prehodnotil výdavky tak, aby boli v súlade s politikou.</span><span class="sxs-lookup"><span data-stu-id="6fce3-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="6fce3-115">Odôvodnenie – Vyžaduje, aby pracovník alebo vedúci pracovník pred odoslaním výkazu výdavkov alebo cestovnej žiadanky uviedol zdôvodnenie prekročenia sumy definovanej politikou.</span><span class="sxs-lookup"><span data-stu-id="6fce3-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="6fce3-116">Tipy týkajúce sa politiky</span><span class="sxs-lookup"><span data-stu-id="6fce3-116">Policy tips</span></span>
<span data-ttu-id="6fce3-117">Tu je niekoľko návrhov, ktoré vám môžu pomôcť pri vytváraní nových politík pre riadenie výdavkov.</span><span class="sxs-lookup"><span data-stu-id="6fce3-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="6fce3-118">Politiky sú účinné od dátumu a politika nenadobudne účinnosť, ak je vytvorená po dátume, keď došlo k výdavku.</span><span class="sxs-lookup"><span data-stu-id="6fce3-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="6fce3-119">Napríklad ak dnes vytvárate novú politiku na vynútenie maximálnych výdavkov na stravovanie vo výške $50, žiadne existujúce výdavky zadané od včera nebudú oproti týmto pravidlám skontrolované.</span><span class="sxs-lookup"><span data-stu-id="6fce3-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="6fce3-120">Pri vytváraní politiky pre kategóriu výdavkov, ktoré je možné rozpisovať, zvážte pridanie podmienky pre typ riadku výdavkov.</span><span class="sxs-lookup"><span data-stu-id="6fce3-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="6fce3-121">Niektoré zásady, napríklad vyžadovanie potvrdenia, nemusia mať zmysel pre riadky s položkami a mali by sa uplatňovať iba na riadok hlavičky alebo riadok bez položiek.</span><span class="sxs-lookup"><span data-stu-id="6fce3-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="6fce3-122">Politiky riadenia výdavkov sa štandardne vyhodnocujú voči zdrojovej entite.</span><span class="sxs-lookup"><span data-stu-id="6fce3-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="6fce3-123">Pre medzipodnikové scenáre môžete nastaviť, aby sa politika namiesto toho vyhodnocovala voči cieľovej entite (entite, ktorá si požičiava).</span><span class="sxs-lookup"><span data-stu-id="6fce3-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="6fce3-124">Ak chcete spúšťať politiky proti cieľovej entite, zapnite funkciu Vyhodnocovať politiku výdavkov voči požičiavajúcej si právnickej entite v pracovnom priestore **Správa funkcií**.</span><span class="sxs-lookup"><span data-stu-id="6fce3-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="6fce3-125">Kedy vyhodnocovať politiky</span><span class="sxs-lookup"><span data-stu-id="6fce3-125">When to evaluate policies</span></span>

<span data-ttu-id="6fce3-126">V parametroch riadenia výdavkov existuje možnosť buď zvoliť vyhodnotenie politík riadenia výdavkov pri uložení riadku, alebo pri odoslaní výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="6fce3-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="6fce3-127">Ak sa rozhodnete vyhodnocovať pri ukladaní riadka, zaistí to, že používatelia budú mať skôr prehľad o tom, čo musia urobiť, aby mohli vyplniť výkaz výdavkov naraz.</span><span class="sxs-lookup"><span data-stu-id="6fce3-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="6fce3-128">V opačnom prípade môžete oddialiť vyhodnotenie politiky a ušetriť čas, ak k overeniu dôjde na konci, počas odosielania do pracovného postupu.</span><span class="sxs-lookup"><span data-stu-id="6fce3-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
