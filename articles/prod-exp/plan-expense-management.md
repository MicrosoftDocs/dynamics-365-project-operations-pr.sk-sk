---
title: Konfigurácia správy výdavkov
description: Tento článok popisuje úvahy a rozhodnutia, ktoré musíte urobiť počas procesu plánovania pred konfiguráciou správy výdavkov v systéme Microsoft Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e2291515cc154fb5b34ca5802135791958bea1e5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084512"
---
# <a name="configure-expense-management"></a><span data-ttu-id="82f52-103">Konfigurácia správy výdavkov</span><span class="sxs-lookup"><span data-stu-id="82f52-103">Configure expense management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82f52-104">Táto téma popisuje úvahy a rozhodnutia, ktoré musíte urobiť počas procesu plánovania pred konfiguráciou správy výdavkov.</span><span class="sxs-lookup"><span data-stu-id="82f52-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="82f52-105">V správe výdavkov môžete ukladať informácie o spôsoboch platby, cestovných požiadavkách, správach o výdavkoch, pravidlách atď.</span><span class="sxs-lookup"><span data-stu-id="82f52-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="82f52-106">Pretože veľa rozhodnutí, ktoré urobíte pri plánovaní svojej konfigurácie pre správu výdavkov, je založených na hierarchii a finančnej štruktúre vašej organizácie, musíte si prečítať plánovacie dokumenty pre tieto oblasti.</span><span class="sxs-lookup"><span data-stu-id="82f52-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="82f52-107">Medzipodnikové výdavky</span><span class="sxs-lookup"><span data-stu-id="82f52-107">Intercompany expenses</span></span>

<span data-ttu-id="82f52-108">Ak povolíte medzipodnikové výdavky, umožníte právnickým osobám a zamestnancom znášať výdavky v mene inej právnickej osoby a vyberať platby od právnických osôb, ktoré sú zamestnancami vo vašej organizácii.</span><span class="sxs-lookup"><span data-stu-id="82f52-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="82f52-109">Napríklad zamestnanec v právnickej osobe A dokončí projekt pre právnickú osobu B a v rámci projektu vzniknú cestovné náklady.</span><span class="sxs-lookup"><span data-stu-id="82f52-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="82f52-110">Ak sú povolené medzipodnikové výdavky, zamestnanec môže potom podať výkaz výdavkov, ktorý zaúčtuje náklady právnickej osobe B, a výdavok musí potom zaplatiť právnická osoba A. Ak vaša organizácia nemá viac právnických osôb, nemusíte povoliť medzipodnikové výdavky.</span><span class="sxs-lookup"><span data-stu-id="82f52-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="82f52-111">**Rozhodnutie:** Chcete povoliť medzipodnikové výdavky?</span><span class="sxs-lookup"><span data-stu-id="82f52-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="82f52-112">Finančný manažment</span><span class="sxs-lookup"><span data-stu-id="82f52-112">Financial management</span></span>

<span data-ttu-id="82f52-113">Správa výdavkov je úzko prepojená s finančným riadením vašej organizácie.</span><span class="sxs-lookup"><span data-stu-id="82f52-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="82f52-114">Mnoho konfigurácie pre správu výdavkov bude závisieť od vašich rozhodnutí o financiách vašej organizácie.</span><span class="sxs-lookup"><span data-stu-id="82f52-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="82f52-115">Nasledujúce časti popisujú rôzne oblasti, ktoré si vyžadujú plánovanie a rozhodovanie na základe finančných rozhodnutí vašej organizácie a na vedení vášho vodcovského tímu.</span><span class="sxs-lookup"><span data-stu-id="82f52-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="82f52-116">Za každý deň</span><span class="sxs-lookup"><span data-stu-id="82f52-116">Per diems</span></span>

<span data-ttu-id="82f52-117">Musíte definovať diéty zamestnancov, ktoré poskytuje vaša organizácia.</span><span class="sxs-lookup"><span data-stu-id="82f52-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="82f52-118">Pretože diéty sa zvyčajne používajú na pokrytie výdavkov, ako je strava, ubytovanie a ďalšie vedľajšie výdavky, môžete vytvoriť pravidlá pre denné diéty, ktoré vaša organizácia ponúka.</span><span class="sxs-lookup"><span data-stu-id="82f52-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="82f52-119">Sadzby za diéty môžu byť založené na ročnom období, mieste cesty alebo oboch.</span><span class="sxs-lookup"><span data-stu-id="82f52-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="82f52-120">Keď definujete pravidlo týkajúce sa diéty, môžete určiť, že bude zadržané percento z diéty, ak pracovník dostane bezplatné stravovanie alebo služby.</span><span class="sxs-lookup"><span data-stu-id="82f52-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="82f52-121">Môžete tiež definovať triedy sadzieb diét na stanovenie minimálneho a maximálneho počtu hodín, pre ktoré môže platiť diéta pre cestu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="82f52-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="82f52-122">**Rozhodnutia:**</span><span class="sxs-lookup"><span data-stu-id="82f52-122">**Decisions:**</span></span>

- <span data-ttu-id="82f52-123">Predvolené pravidlá diéty pre prvý a posledný deň:</span><span class="sxs-lookup"><span data-stu-id="82f52-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="82f52-124">Aký je minimálny počet hodín, ktoré si zamestnanec môže nárokovať za deň a stále dostávať diéty?</span><span class="sxs-lookup"><span data-stu-id="82f52-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="82f52-125">Dochádza k zníženiu sumy, ktorá sa ponúka za jedlo prvý a posledný deň?</span><span class="sxs-lookup"><span data-stu-id="82f52-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="82f52-126">Ak dôjde k zníženiu, aké je percento zníženia?</span><span class="sxs-lookup"><span data-stu-id="82f52-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="82f52-127">Dochádza k zníženiu sumy, ktorá sa ponúka za hotel prvý a posledný deň?</span><span class="sxs-lookup"><span data-stu-id="82f52-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="82f52-128">Ak dôjde k zníženiu, aké je percento zníženia?</span><span class="sxs-lookup"><span data-stu-id="82f52-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="82f52-129">Dochádza k zníženiu sumy, ktorá sa ponúka za iné náklady vzniknuté prvý a posledný deň?</span><span class="sxs-lookup"><span data-stu-id="82f52-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="82f52-130">Ak dôjde k zníženiu, aké je percento zníženia?</span><span class="sxs-lookup"><span data-stu-id="82f52-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="82f52-131">Predvolené pravidlá diét:</span><span class="sxs-lookup"><span data-stu-id="82f52-131">Default per diem rules:</span></span>

    - <span data-ttu-id="82f52-132">Dochádza k percentuálnemu zníženiu diét za každé jedlo, ak je napríklad jedlo bezplatné?</span><span class="sxs-lookup"><span data-stu-id="82f52-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="82f52-133">Ak dôjde k zníženiu, aké je percento zníženia pre každé jedlo?</span><span class="sxs-lookup"><span data-stu-id="82f52-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="82f52-134">Počíta sa zníženie na jedlo vypočítané za deň, na cestu alebo podľa počtu jedál za deň?</span><span class="sxs-lookup"><span data-stu-id="82f52-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="82f52-135">Mali by byť sumy za diéty zaokrúhlené bežným spôsobom alebo zaokrúhlené nahor?</span><span class="sxs-lookup"><span data-stu-id="82f52-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="82f52-136">Počítajú sa diéty za 24 hodín alebo za kalendárny deň?</span><span class="sxs-lookup"><span data-stu-id="82f52-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="82f52-137">Pravidlá diéty založené na umiestnení:</span><span class="sxs-lookup"><span data-stu-id="82f52-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="82f52-138">Líšia sa sadzby diéty podľa miesta?</span><span class="sxs-lookup"><span data-stu-id="82f52-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="82f52-139">Aké miesta sú zahrnuté?</span><span class="sxs-lookup"><span data-stu-id="82f52-139">What locations are included?</span></span>
    - <span data-ttu-id="82f52-140">Ak sa sadzby za diéty líšia v závislosti od lokality, pre každú lokalitu sa uvádza percentuálna suma pri nasledujúcich druhoch výdavkov:</span><span class="sxs-lookup"><span data-stu-id="82f52-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="82f52-141">Jedlá</span><span class="sxs-lookup"><span data-stu-id="82f52-141">Meals</span></span>
        - <span data-ttu-id="82f52-142">Hotel</span><span class="sxs-lookup"><span data-stu-id="82f52-142">Hotel</span></span>
        - <span data-ttu-id="82f52-143">Iné výdavky</span><span class="sxs-lookup"><span data-stu-id="82f52-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="82f52-144">Denníky a účty riadenia výdavkov</span><span class="sxs-lookup"><span data-stu-id="82f52-144">Expense management journals and accounts</span></span>

<span data-ttu-id="82f52-145">Správa výdavkov vyžaduje, aby ste používali viac denníkov a účtov.</span><span class="sxs-lookup"><span data-stu-id="82f52-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="82f52-146">Musíte sa napríklad rozhodnúť, či sa ten istý účet používa na hotovostné zálohy a spory o kreditné karty.</span><span class="sxs-lookup"><span data-stu-id="82f52-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="82f52-147">**Rozhodnutia:**</span><span class="sxs-lookup"><span data-stu-id="82f52-147">**Decisions:**</span></span>

- <span data-ttu-id="82f52-148">Do ktorého denníka hlavnej knihy sa zaúčtujú schválené výkazy výdavkov?</span><span class="sxs-lookup"><span data-stu-id="82f52-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="82f52-149">Aký účet sa používa na hotovostné zálohy?</span><span class="sxs-lookup"><span data-stu-id="82f52-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="82f52-150">Mali by sa peňažné zálohy zaúčtovať okamžite?</span><span class="sxs-lookup"><span data-stu-id="82f52-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="82f52-151">Spôsoby platby</span><span class="sxs-lookup"><span data-stu-id="82f52-151">Payment methods</span></span>

<span data-ttu-id="82f52-152">Ak zamestnancom umožníte, aby v mene vašej firmy znášali výdavky, musíte definovať spôsoby platby, ktoré môžu zamestnanci používať.</span><span class="sxs-lookup"><span data-stu-id="82f52-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="82f52-153">Môžete napríklad povoliť zamestnancom používať hotovosť alebo firemnú kreditnú kartu.</span><span class="sxs-lookup"><span data-stu-id="82f52-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="82f52-154">Môžete tiež umožniť zamestnancom používať osobné kreditné karty a potom zamestnancom refundovať náklady.</span><span class="sxs-lookup"><span data-stu-id="82f52-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="82f52-155">Pre každý povolený spôsob platby musíte urobiť nasledujúce rozhodnutia.</span><span class="sxs-lookup"><span data-stu-id="82f52-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="82f52-156">**Rozhodnutia:**</span><span class="sxs-lookup"><span data-stu-id="82f52-156">**Decisions:**</span></span>

- <span data-ttu-id="82f52-157">Aké spôsoby platby sú povolené?</span><span class="sxs-lookup"><span data-stu-id="82f52-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="82f52-158">Kto vlastní výdavky na spôsob platby?</span><span class="sxs-lookup"><span data-stu-id="82f52-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="82f52-159">Existuje typ offsetového účtu?</span><span class="sxs-lookup"><span data-stu-id="82f52-159">Is there an offset account type?</span></span> <span data-ttu-id="82f52-160">Ak existuje typ offsetového účtu, čo to je?</span><span class="sxs-lookup"><span data-stu-id="82f52-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="82f52-161">Ak existuje typ offsetového účtu, aký je účet?</span><span class="sxs-lookup"><span data-stu-id="82f52-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="82f52-162">Ak je platobnou metódou kreditná karta, mala by sa platobná metóda použiť iba pri importovaných transakciách?</span><span class="sxs-lookup"><span data-stu-id="82f52-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="82f52-163">Kategórie výdavkov a zdieľané kategórie</span><span class="sxs-lookup"><span data-stu-id="82f52-163">Expense categories and shared categories</span></span>

<span data-ttu-id="82f52-164">Keď zamestnanci vytvárajú výkaz výdavkov, každý výdavok, ktorý zaznamenajú, musí byť priradený ku kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="82f52-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="82f52-165">Kategórie výdavkov sú odvodené od zdieľaných kategórií, ktoré je možné zdieľať medzi právnymi entitami vo vašej organizácii.</span><span class="sxs-lookup"><span data-stu-id="82f52-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="82f52-166">Tieto kategórie možno zdieľať aj v rámci riadenia projektu a účtovníctva v závislosti od toho, ako je definovaná vaša organizácia.</span><span class="sxs-lookup"><span data-stu-id="82f52-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="82f52-167">Na základe definície vašej organizácie a pokynov implementačného tímu musíte určiť, či sa kategórie, ktoré sa používajú v správe výdavkov, použijú iba v správe výdavkov, alebo či sa majú zdieľať medzi správou projektu a účtovania a správou výdavkov.</span><span class="sxs-lookup"><span data-stu-id="82f52-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="82f52-168">Upozorňujeme, že tieto kategórie možno zdieľať medzi projektom a výdavkami alebo projektom a výrobou, no nie medzi výdavkami a výrobou.</span><span class="sxs-lookup"><span data-stu-id="82f52-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="82f52-169">Pre každú kategóriu výdavkov musíte urobiť nasledujúce rozhodnutia.</span><span class="sxs-lookup"><span data-stu-id="82f52-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="82f52-170">**Rozhodnutia:**</span><span class="sxs-lookup"><span data-stu-id="82f52-170">**Decisions:**</span></span>

- <span data-ttu-id="82f52-171">Čo je kategória výdavku?</span><span class="sxs-lookup"><span data-stu-id="82f52-171">What is the expense category?</span></span> <span data-ttu-id="82f52-172">Príklady zahŕňajú kategórie letov, hotelov alebo najazdených kilometrov.</span><span class="sxs-lookup"><span data-stu-id="82f52-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="82f52-173">Dá sa kategória výdavkov použiť aj v projektovom manažmente a účtovníctve?</span><span class="sxs-lookup"><span data-stu-id="82f52-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="82f52-174">Čo je typ výdavku?</span><span class="sxs-lookup"><span data-stu-id="82f52-174">What is the expense type?</span></span>
- <span data-ttu-id="82f52-175">Aký je predvolený spôsob platby pre kategóriu výdavkov?</span><span class="sxs-lookup"><span data-stu-id="82f52-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="82f52-176">Musia byť výdavky v kategórii výdavkov rozpísané na jednotlivé položky?</span><span class="sxs-lookup"><span data-stu-id="82f52-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="82f52-177">Aký je hlavný predvolený obchodný vzťah pre kategóriu výdavkov?</span><span class="sxs-lookup"><span data-stu-id="82f52-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="82f52-178">Aká je predvolená skupina dane z predaja položky pre kategóriu výdavkov?</span><span class="sxs-lookup"><span data-stu-id="82f52-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="82f52-179">Sú pre kategóriu výdavkov povolené ďalšie spôsoby platby?</span><span class="sxs-lookup"><span data-stu-id="82f52-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="82f52-180">Ak sú povolené ďalšie spôsoby platby, aké sú?</span><span class="sxs-lookup"><span data-stu-id="82f52-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="82f52-181">Existujú v tejto kategórii výdavkov podkategórie?</span><span class="sxs-lookup"><span data-stu-id="82f52-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="82f52-182">Ak existujú podkategórie, musíte uskutočniť aj nasledujúce rozhodnutia:</span><span class="sxs-lookup"><span data-stu-id="82f52-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="82f52-183">Je niektorá z podkategórií vylúčená z vrátenia dane?</span><span class="sxs-lookup"><span data-stu-id="82f52-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="82f52-184">Čo je skupina dane z predaja položky v podkategóriách?</span><span class="sxs-lookup"><span data-stu-id="82f52-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="82f52-185">Ak sa kategória výdavkov používa aj v projektovom manažmente a účtovníctve, odpovedzte na zostávajúce otázky.</span><span class="sxs-lookup"><span data-stu-id="82f52-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="82f52-186">V opačnom prípade prejdite na ďalšiu časť.</span><span class="sxs-lookup"><span data-stu-id="82f52-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="82f52-187">Ktoré nákladové účty sa použijú na nasledujúce výdavky?</span><span class="sxs-lookup"><span data-stu-id="82f52-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="82f52-188">Náklady</span><span class="sxs-lookup"><span data-stu-id="82f52-188">Cost</span></span>
    - <span data-ttu-id="82f52-189">Alokácia miezd</span><span class="sxs-lookup"><span data-stu-id="82f52-189">Payroll allocation</span></span>
    - <span data-ttu-id="82f52-190">Hodnota nákladov WIP</span><span class="sxs-lookup"><span data-stu-id="82f52-190">WIP-cost value</span></span>
    - <span data-ttu-id="82f52-191">Nákladová položka</span><span class="sxs-lookup"><span data-stu-id="82f52-191">Cost-item</span></span>
    - <span data-ttu-id="82f52-192">WIP – nákladová hodnota – položka</span><span class="sxs-lookup"><span data-stu-id="82f52-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="82f52-193">Akumulovaná strata</span><span class="sxs-lookup"><span data-stu-id="82f52-193">Accrued loss</span></span>
    - <span data-ttu-id="82f52-194">WIP – akumulovaná strata</span><span class="sxs-lookup"><span data-stu-id="82f52-194">WIP-accrued loss</span></span>

- <span data-ttu-id="82f52-195">Ktoré výnosové účty sa použijú na nasledujúce?</span><span class="sxs-lookup"><span data-stu-id="82f52-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="82f52-196">Fakturovaný príjem</span><span class="sxs-lookup"><span data-stu-id="82f52-196">Invoiced revenue</span></span>
    - <span data-ttu-id="82f52-197">Akumulované výnosy – hodnota predaja</span><span class="sxs-lookup"><span data-stu-id="82f52-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="82f52-198">WIP – hodnota predaja</span><span class="sxs-lookup"><span data-stu-id="82f52-198">WIP-sales value</span></span>
    - <span data-ttu-id="82f52-199">Akumulované výnosy – produkcia</span><span class="sxs-lookup"><span data-stu-id="82f52-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="82f52-200">WIP – produkcia</span><span class="sxs-lookup"><span data-stu-id="82f52-200">WIP-production</span></span>
    - <span data-ttu-id="82f52-201">Akumulované výnosy – zisk</span><span class="sxs-lookup"><span data-stu-id="82f52-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="82f52-202">WIP – zisk</span><span class="sxs-lookup"><span data-stu-id="82f52-202">WIP-profit</span></span>
    - <span data-ttu-id="82f52-203">Akumulované výnosy – predplatné</span><span class="sxs-lookup"><span data-stu-id="82f52-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="82f52-204">WIP – predplatné</span><span class="sxs-lookup"><span data-stu-id="82f52-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="82f52-205">Dane</span><span class="sxs-lookup"><span data-stu-id="82f52-205">Taxes</span></span>

<span data-ttu-id="82f52-206">Pri daniach súvisiacich s výdavkami musíte určiť, čo je zahrnuté alebo povolené v prehľadoch výdavkov.</span><span class="sxs-lookup"><span data-stu-id="82f52-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="82f52-207">**Rozhodnutia:**</span><span class="sxs-lookup"><span data-stu-id="82f52-207">**Decisions:**</span></span>

- <span data-ttu-id="82f52-208">Je daň z obratu zahrnutá do výšky výdavkov?</span><span class="sxs-lookup"><span data-stu-id="82f52-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="82f52-209">Malo by sa povoliť vrátenie dane z výdavkov?</span><span class="sxs-lookup"><span data-stu-id="82f52-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="82f52-210">Ak ste sa pri plánovaní hlavnej knihy rozhodli uplatniť daň z obratu v USA a použiť pravidlá dane, nemôžete povoliť vrátenie daní z výdavkov.</span><span class="sxs-lookup"><span data-stu-id="82f52-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="82f52-211">(Ak chcete použiť daň z obratu v USA a použiť daňové pravidlá, nastavte možnosť **Použiť pravidlá zdaňovania dane z obratu** na **Áno**.)</span><span class="sxs-lookup"><span data-stu-id="82f52-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="82f52-212">Politiky</span><span class="sxs-lookup"><span data-stu-id="82f52-212">Policies</span></span>

<span data-ttu-id="82f52-213">Vytvorením politík výkazov výdavkov môžete pomôcť svojej organizácii ušetriť čas a peniaze, keď zamestnancom vzniknú v jej mene výdavky.</span><span class="sxs-lookup"><span data-stu-id="82f52-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="82f52-214">Pravidlá pomáhajú zaručiť, že zamestnanci zostanú v rozpočte, poskytnú všetky požadované informácie a míňajú peniaze len tak, ako to požadujú.</span><span class="sxs-lookup"><span data-stu-id="82f52-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="82f52-215">Pre každú politiku výkazov výdavkov a každú politiku schvaľovania výkazov výdavkov, ktorú vytvoríte, musíte urobiť nasledujúce rozhodnutia.</span><span class="sxs-lookup"><span data-stu-id="82f52-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="82f52-216">**Rozhodnutia:**</span><span class="sxs-lookup"><span data-stu-id="82f52-216">**Decisions:**</span></span>

- <span data-ttu-id="82f52-217">Aký je názov politiky?</span><span class="sxs-lookup"><span data-stu-id="82f52-217">What is the name of the policy?</span></span>
- <span data-ttu-id="82f52-218">Na čo slúži výdavková politika?</span><span class="sxs-lookup"><span data-stu-id="82f52-218">What is the expense policy for?</span></span>
- <span data-ttu-id="82f52-219">Ak ste sa predtým rozhodli povoliť medzipodnikové výdavky, na ktoré spoločnosti vo vašej organizácii sa tieto pravidlá budú vzťahovať?</span><span class="sxs-lookup"><span data-stu-id="82f52-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="82f52-220">Kedy politika nadobudne účinnosť?</span><span class="sxs-lookup"><span data-stu-id="82f52-220">When does the policy become effective?</span></span>
- <span data-ttu-id="82f52-221">Kedy vyprší platnosť politiky?</span><span class="sxs-lookup"><span data-stu-id="82f52-221">When does the policy expire?</span></span>
- <span data-ttu-id="82f52-222">Aké je pravidlo politiky?</span><span class="sxs-lookup"><span data-stu-id="82f52-222">What is the policy rule?</span></span>
- <span data-ttu-id="82f52-223">Aký je výsledok pravidla politiky?</span><span class="sxs-lookup"><span data-stu-id="82f52-223">What is the outcome of the policy rule?</span></span>
