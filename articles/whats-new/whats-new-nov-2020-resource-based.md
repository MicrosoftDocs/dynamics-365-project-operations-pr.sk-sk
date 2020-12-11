---
title: Čo je nové v novembri 2020 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch
description: Táto téma poskytuje informácie o aktualizáciách kvality, ktoré sú k dispozícii vo vydaní Project Operations z novembra 2020, pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: c7ec9360401bf214ae867769b0e48e545a6bad48
ms.sourcegitcommit: 64d0de964a9b66c015ffcf1db62cbb6216cb3187
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/03/2020
ms.locfileid: "4367285"
---
# <a name="whats-new-november-2020---project-operations-for-resourcenon-stocked-based-scenarios"></a><span data-ttu-id="d911e-103">Čo je nové v novembri 2020 – Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch</span><span class="sxs-lookup"><span data-stu-id="d911e-103">What's new November 2020 - Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="d911e-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="d911e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d911e-105">Táto téma sa týka nasledujúcich komponentov a verzií Dynamics 365 Project Operations:</span><span class="sxs-lookup"><span data-stu-id="d911e-105">This topic applies to the following Dynamics 365 Project Operations components and versions:</span></span>

- <span data-ttu-id="d911e-106">Project Operations v prostredí CDS environment verzie 4.4.0.70</span><span class="sxs-lookup"><span data-stu-id="d911e-106">Project Operations on CDS environment version 4.4.0.70</span></span>
- <span data-ttu-id="d911e-107">Projektový manažment a účtovanie v prostredí Dynamics 365 Finance verzie 10.0.14</span><span class="sxs-lookup"><span data-stu-id="d911e-107">Project management and accounting in Dynamics 365 Finance environment version 10.0.14</span></span>

## <a name="updates-to-project-operations-for-resource-non-stocked-based-scenarios"></a><span data-ttu-id="d911e-108">Aktualizácie aplikácie Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch</span><span class="sxs-lookup"><span data-stu-id="d911e-108">Updates to Project Operations for resource-non-stocked based scenarios</span></span>

### <a name="project-operations-on-cds"></a><span data-ttu-id="d911e-109">Project Operations v prostredí CDS</span><span class="sxs-lookup"><span data-stu-id="d911e-109">Project Operations on CDS</span></span>

| <span data-ttu-id="d911e-110">Oblasť funkcií</span><span class="sxs-lookup"><span data-stu-id="d911e-110">Feature area</span></span>                 | <span data-ttu-id="d911e-111">Číslo odkazu</span><span class="sxs-lookup"><span data-stu-id="d911e-111">Reference number</span></span> | <span data-ttu-id="d911e-112">Aktualizácia kvality</span><span class="sxs-lookup"><span data-stu-id="d911e-112">Quality update</span></span>                                                                                                                                                                    |
|------------------------------|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d911e-113"> Správa príležitostí</span><span class="sxs-lookup"><span data-stu-id="d911e-113">Opportunity management</span></span>       | <span data-ttu-id="d911e-114">2036993</span><span class="sxs-lookup"><span data-stu-id="d911e-114">2036993</span></span>          | <span data-ttu-id="d911e-115">Riadok odhadu a riadky zmlúv priradenia zdroja sa aktualizujú v získaných cenových ponukách, keď je typ riadku cenovej ponuky **Všetky úlohy**.</span><span class="sxs-lookup"><span data-stu-id="d911e-115">Estimate line and resource   assignment contract lines are updated on winning quotes when the quote line   type is **All tasks**.</span></span>                                                 |
| <span data-ttu-id="d911e-116">Fakturácia a tvorba cien</span><span class="sxs-lookup"><span data-stu-id="d911e-116">Billing and pricing</span></span>          | <span data-ttu-id="d911e-117">2070392</span><span class="sxs-lookup"><span data-stu-id="d911e-117">2070392</span></span>          | <span data-ttu-id="d911e-118">Riadky projektovej zmluvy na faktúre sa zvyšujú vždy po výbere možnosti **Obnovenie fakturačných transakcií**.</span><span class="sxs-lookup"><span data-stu-id="d911e-118">Project contract lines on the   invoice increase every time **Refresh invoice transactions** is selected.</span></span>                                                                         |
| <span data-ttu-id="d911e-119">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-119">Project planning</span></span>             | <span data-ttu-id="d911e-120">2043336</span><span class="sxs-lookup"><span data-stu-id="d911e-120">2043336</span></span>          | <span data-ttu-id="d911e-121">Nie je možné odstrániť záznam člena projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="d911e-121">Unable to delete a project team   member record.</span></span>                                                                                                                                  |
| <span data-ttu-id="d911e-122">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-122">Project planning</span></span>             | <span data-ttu-id="d911e-123">2046013</span><span class="sxs-lookup"><span data-stu-id="d911e-123">2046013</span></span>          | <span data-ttu-id="d911e-124">Nekonzistentné správanie pre stĺpce značky Odhady počas načítania a pri zmene typu časovej fázy.</span><span class="sxs-lookup"><span data-stu-id="d911e-124">Inconsistent behavior for   Estimates tag columns during load vs. on change of time-phase type.</span></span>                                                                                   |
| <span data-ttu-id="d911e-125">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-125">Project planning</span></span>             | <span data-ttu-id="d911e-126">2046647</span><span class="sxs-lookup"><span data-stu-id="d911e-126">2046647</span></span>          | <span data-ttu-id="d911e-127">Počiatočný a konečný čas sú o hodinu vypnuté, keď sa požiadavky na zdroje generujú od členov projektového tímu.</span><span class="sxs-lookup"><span data-stu-id="d911e-127">Start and end times are off by   an hour when resource requirements are generated from project team members.</span></span>                                                                      |
| <span data-ttu-id="d911e-128">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-128">Project planning</span></span>             | <span data-ttu-id="d911e-129">2053879</span><span class="sxs-lookup"><span data-stu-id="d911e-129">2053879</span></span>          | <span data-ttu-id="d911e-130">(Podľa pripravovaného zavádzania CDS) PublishUnassignedAssignments zruší pokus o uloženie úlohy pri chybe „Hodnota odovzdaná pre ConditionOperator.In je prázdna.“</span><span class="sxs-lookup"><span data-stu-id="d911e-130">(Per the upcoming CDS rollout)   PublishUnassignedAssignments breaks an attempt to save a task when the error, "The value passed for ConditionOperator.In is empty."</span></span>                       |
| <span data-ttu-id="d911e-131">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-131">Project planning</span></span>             | <span data-ttu-id="d911e-132">2055501</span><span class="sxs-lookup"><span data-stu-id="d911e-132">2055501</span></span>          | <span data-ttu-id="d911e-133">Odchod s prázdnou hodnotou **Dátum začatia projektu** spôsobí zlyhanie plánu.</span><span class="sxs-lookup"><span data-stu-id="d911e-133">Leaving the **Project Start   Date** empty causes a failure in the schedule.</span></span>                                                                                                      |
| <span data-ttu-id="d911e-134">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-134">Project planning</span></span>             | <span data-ttu-id="d911e-135">2066817</span><span class="sxs-lookup"><span data-stu-id="d911e-135">2066817</span></span>          | <span data-ttu-id="d911e-136">Nie je možné vytvoriť všeobecný zdroj pomocou nástroja na výber ľudí na karte **Úlohy**.</span><span class="sxs-lookup"><span data-stu-id="d911e-136">Can't create a generic resource   using the people picker on the **Tasks** tab.</span></span>                                                                                                   |
| <span data-ttu-id="d911e-137">Plánovanie projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-137">Project planning</span></span>             | <span data-ttu-id="d911e-138">2067034</span><span class="sxs-lookup"><span data-stu-id="d911e-138">2067034</span></span>          | <span data-ttu-id="d911e-139">Tlačidlo **Zobraziť podrobnosti** nie je k dispozícii na stránke **Podrobnosti úlohy**.</span><span class="sxs-lookup"><span data-stu-id="d911e-139">**View Details** button is not   available on the **Details of Task** page.</span></span>                                                                                                       |
| <span data-ttu-id="d911e-140">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="d911e-140">Resource management</span></span>          | <span data-ttu-id="d911e-141">2046667</span><span class="sxs-lookup"><span data-stu-id="d911e-141">2046667</span></span>          | <span data-ttu-id="d911e-142">Všeobecní členovia tímu sa neodstránia ani po splnení všetkých zdrojov.</span><span class="sxs-lookup"><span data-stu-id="d911e-142">Generic team members aren't   deleted even after all resources are fulfilled.</span></span>                                                                                                    |
| <span data-ttu-id="d911e-143">Položka času a rýchleho výdavku</span><span class="sxs-lookup"><span data-stu-id="d911e-143">Time and quick expense entry</span></span> | <span data-ttu-id="d911e-144">2047499</span><span class="sxs-lookup"><span data-stu-id="d911e-144">2047499</span></span>          | <span data-ttu-id="d911e-145">Tlačidlo **Nový** na stránke Časový vstup otvorí stránku **Nový e-mailový podpis**.</span><span class="sxs-lookup"><span data-stu-id="d911e-145">The **New** button on the Time   Entry page opens the **New Email Signature** page.</span></span>                                                                                               |
| <span data-ttu-id="d911e-146">Položka času a rýchleho výdavku</span><span class="sxs-lookup"><span data-stu-id="d911e-146">Time and quick expense entry</span></span> | <span data-ttu-id="d911e-147">2059859</span><span class="sxs-lookup"><span data-stu-id="d911e-147">2059859</span></span>          | <span data-ttu-id="d911e-148">Pri vytváraní položky výdavkov sa otvorí neočakávané vyskakovacie okno.</span><span class="sxs-lookup"><span data-stu-id="d911e-148">Unexpected pop-up opens when   creating an expense entry.</span></span>                                                                                                                         |
| <span data-ttu-id="d911e-149">Ostatné</span><span class="sxs-lookup"><span data-stu-id="d911e-149">Other</span></span>                        | <span data-ttu-id="d911e-150">2044181</span><span class="sxs-lookup"><span data-stu-id="d911e-150">2044181</span></span>          | <span data-ttu-id="d911e-151">(Odinštalovanie nákupnej objednávky) Pri pokuse o odinštalovanie základných riešení aplikácie Project Service msdyn_ProjectServiceCore_Patch a msdyn sa vyskytne chyba „Záznam nie je k dispozícii“.</span><span class="sxs-lookup"><span data-stu-id="d911e-151">(Uninstalling purchase order)   When trying to uninstall msdyn_ProjectServiceCore_Patch and msdyn Project   service core solutions, the error, "Record is unavailable"   occurs.</span></span>  |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a><span data-ttu-id="d911e-152">Projektový manažment a účtovníctvo v Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="d911e-152">Project management and accounting in Dynamics 365 Finance</span></span>

| <span data-ttu-id="d911e-153">Oblasť funkcií</span><span class="sxs-lookup"><span data-stu-id="d911e-153">Feature area</span></span>        | <span data-ttu-id="d911e-154">Číslo odkazu</span><span class="sxs-lookup"><span data-stu-id="d911e-154">Reference number</span></span> | <span data-ttu-id="d911e-155">Aktualizácia kvality</span><span class="sxs-lookup"><span data-stu-id="d911e-155">Quality update</span></span>                                                                                                                                                            |
|---------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d911e-156">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="d911e-156">Revenue recognition</span></span> | [<span data-ttu-id="d911e-157">451662</span><span class="sxs-lookup"><span data-stu-id="d911e-157">451662</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=451662)           | <span data-ttu-id="d911e-158">Percento dokončenia odhadu projektu je nesprávne, keď zmluva používa cudziu menu a percento postupu práce pre metódu dokončenia.</span><span class="sxs-lookup"><span data-stu-id="d911e-158">Project estimate percentage   complete is wrong when the contract is using a foreign currency and the work   progress percentage for complete method.</span></span>                     |
| <span data-ttu-id="d911e-159">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="d911e-159">Revenue recognition</span></span> | [<span data-ttu-id="d911e-160">469894</span><span class="sxs-lookup"><span data-stu-id="d911e-160">469894</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469894)           | <span data-ttu-id="d911e-161">Odhady nie je možné odoslať s metódou dokončenia **Skutočné náklady**.</span><span class="sxs-lookup"><span data-stu-id="d911e-161">Unable to post estimates with   the **Actual cost** completion method.</span></span>                                                                                                    |
| <span data-ttu-id="d911e-162">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="d911e-162">Revenue recognition</span></span> | [<span data-ttu-id="d911e-163">485439</span><span class="sxs-lookup"><span data-stu-id="d911e-163">485439</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=485439)           | <span data-ttu-id="d911e-164">Vylúčenie zlyhá z dôvodu chyby nerovnováhy poukazu, keď sa mena spoločnosti a mena transakcie líšia.</span><span class="sxs-lookup"><span data-stu-id="d911e-164">Elimination fails because of a   voucher imbalance error when the company currency and transaction currency   are different.</span></span>                                              |
| <span data-ttu-id="d911e-165">Správa výdavkov</span><span class="sxs-lookup"><span data-stu-id="d911e-165">Expense management</span></span>  | [<span data-ttu-id="d911e-166">456882</span><span class="sxs-lookup"><span data-stu-id="d911e-166">456882</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=456822)           | <span data-ttu-id="d911e-167">Pre používateľov, ktorí nie sú správcami, sa hodnoty vyhľadávania pre stĺpce riadkov výdavkov, ako napr. **ID projektu** a **Kategória výdavkov** v ráme dátového konektora nezobrazujú správne.</span><span class="sxs-lookup"><span data-stu-id="d911e-167">For non-admin users, the lookup   values for expense line columns such as **Project ID** and **Expense   Category** aren't showing correctly in the data connector frame.</span></span> |
| <span data-ttu-id="d911e-168">Správa výdavkov</span><span class="sxs-lookup"><span data-stu-id="d911e-168">Expense management</span></span>  | [<span data-ttu-id="d911e-169">469300</span><span class="sxs-lookup"><span data-stu-id="d911e-169">469300</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469300)           | <span data-ttu-id="d911e-170">Predvolená vlastnosť riadku sa nezobrazuje pre kategórie výdavkov.</span><span class="sxs-lookup"><span data-stu-id="d911e-170">The line property default isn't   showing for Expense categories.</span></span>                                                                                                         |
| <span data-ttu-id="d911e-171">Správa výdavkov</span><span class="sxs-lookup"><span data-stu-id="d911e-171">Expense management</span></span>  | [<span data-ttu-id="d911e-172">469302</span><span class="sxs-lookup"><span data-stu-id="d911e-172">469302</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=469302)           | <span data-ttu-id="d911e-173">Integrácia výdavkov musí obsahovať vlastnosť riadka z výkazu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="d911e-173">Expense integration must include   the line property from the expense report.</span></span>                                                                                             |
| <span data-ttu-id="d911e-174">Účtovanie</span><span class="sxs-lookup"><span data-stu-id="d911e-174">Invoicing</span></span>           | [<span data-ttu-id="d911e-175">462499</span><span class="sxs-lookup"><span data-stu-id="d911e-175">462499</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=462499)           | <span data-ttu-id="d911e-176">Nie je možné zaúčtovať návrhy projektových faktúr kvôli chybovej správe, ktorá hovorí, že kombinácia FD nebola overená.</span><span class="sxs-lookup"><span data-stu-id="d911e-176">Can't post project invoice   proposals because of an error message that says the combination of FD wasn't   validated.</span></span>                                                    |
| <span data-ttu-id="d911e-177">Účtovanie</span><span class="sxs-lookup"><span data-stu-id="d911e-177">Invoicing</span></span>           | [<span data-ttu-id="d911e-178">470614</span><span class="sxs-lookup"><span data-stu-id="d911e-178">470614</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470614)           | <span data-ttu-id="d911e-179">Nie je možné zobraziť transakcie zo stránky s podrobnosťami **faktúra**.</span><span class="sxs-lookup"><span data-stu-id="d911e-179">Can't view transactions from the   **invoice** details page.</span></span>                                                                                                              |
| <span data-ttu-id="d911e-180">Účtovanie</span><span class="sxs-lookup"><span data-stu-id="d911e-180">Invoicing</span></span>           | [<span data-ttu-id="d911e-181">480070</span><span class="sxs-lookup"><span data-stu-id="d911e-181">480070</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480070)           | <span data-ttu-id="d911e-182">Riadky s návrhom faktúry je možné odstrániť.</span><span class="sxs-lookup"><span data-stu-id="d911e-182">Invoice proposal lines can be   deleted.</span></span>                                                                                                                                  |
| <span data-ttu-id="d911e-183">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-183">Project accounting</span></span>  | [<span data-ttu-id="d911e-184">470293</span><span class="sxs-lookup"><span data-stu-id="d911e-184">470293</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=470293)           | <span data-ttu-id="d911e-185">Položky ponuky **Predpoveď** nie sú viditeľné na stránke so zoznamom **Projekty**.</span><span class="sxs-lookup"><span data-stu-id="d911e-185">**Forecast** menu items aren't   visible on the **Projects** list page.</span></span>                                                                                                   |
| <span data-ttu-id="d911e-186">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-186">Project accounting</span></span>  | [<span data-ttu-id="d911e-187">475873</span><span class="sxs-lookup"><span data-stu-id="d911e-187">475873</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475873)           | <span data-ttu-id="d911e-188">Nedá sa otvoriť **Vyhlásenie o projekte**   > **Transakcie a predpoveď**.</span><span class="sxs-lookup"><span data-stu-id="d911e-188">Can't open **Project statement**   > **Transactions and forecast**.</span></span>                                                                                                       |
| <span data-ttu-id="d911e-189">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-189">Project accounting</span></span>  | [<span data-ttu-id="d911e-190">475879</span><span class="sxs-lookup"><span data-stu-id="d911e-190">475879</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=475879)           | <span data-ttu-id="d911e-191">**Upraviť účtovníctvo** nie je povolené pre fakturované projektové transakcie.</span><span class="sxs-lookup"><span data-stu-id="d911e-191">**Adjust accounting** isn't   enabled for invoiced project transactions.</span></span>                                                                                                  |
| <span data-ttu-id="d911e-192">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-192">Project accounting</span></span>  | [<span data-ttu-id="d911e-193">480962</span><span class="sxs-lookup"><span data-stu-id="d911e-193">480962</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480962)           | <span data-ttu-id="d911e-194">Podrobnosti účtovníctva nie sú zahrnuté v tabuľke **ProjCDSActualsImport**, keď je uverejnený denník **Integrácia**.</span><span class="sxs-lookup"><span data-stu-id="d911e-194">Accounting details aren't   included on the **ProjCDSActualsImport** table when the **Integration**   journal is posted.</span></span>                                                  |
| <span data-ttu-id="d911e-195">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-195">Project accounting</span></span>  | [<span data-ttu-id="d911e-196">482558</span><span class="sxs-lookup"><span data-stu-id="d911e-196">482558</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482558)           | <span data-ttu-id="d911e-197">Položka prognózy projektu sa zdvojnásobí, keď odstránite a znovu pridáte priradenie zdrojov.</span><span class="sxs-lookup"><span data-stu-id="d911e-197">The Project forecast entry is   doubled when you remove and then readd a resource assignment.</span></span>                                                                            |
| <span data-ttu-id="d911e-198">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-198">Project accounting</span></span>  | [<span data-ttu-id="d911e-199">502019</span><span class="sxs-lookup"><span data-stu-id="d911e-199">502019</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=502019)           | <span data-ttu-id="d911e-200">Výber odkazu na ID projektu neotvorí adresu URL priameho odkazu do CDS.</span><span class="sxs-lookup"><span data-stu-id="d911e-200">Selecting a Project ID link   doesn't open the CDS deep link URL.</span></span>                                                                                                         |
| <span data-ttu-id="d911e-201">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-201">Project accounting</span></span>  | [<span data-ttu-id="d911e-202">505458</span><span class="sxs-lookup"><span data-stu-id="d911e-202">505458</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505458)           | <span data-ttu-id="d911e-203">Nie je možné aktualizovať dátum začatia úlohy v službe CDS.</span><span class="sxs-lookup"><span data-stu-id="d911e-203">Can't update the start date on a   task in CDS.</span></span>                                                                                                                           |
| <span data-ttu-id="d911e-204">Účtovníctvo v rámci projektu</span><span class="sxs-lookup"><span data-stu-id="d911e-204">Project accounting</span></span>  | [<span data-ttu-id="d911e-205">510041</span><span class="sxs-lookup"><span data-stu-id="d911e-205">510041</span></span>](https://fix.lcs.dynamics.com/Issue/Details/?bugId=510041)           | <span data-ttu-id="d911e-206">Po povolení tejto funkcie nie sú možné viaceré riadky zmluvy bez integrácie CDS.</span><span class="sxs-lookup"><span data-stu-id="d911e-206">Enabling the feature, Multiple contract lines isn't possible without CDS integration.</span></span>                                                                                   |

### <a name="regulatory-updates"></a><span data-ttu-id="d911e-207">Regulačné aktualizácie</span><span class="sxs-lookup"><span data-stu-id="d911e-207">Regulatory updates</span></span>
<span data-ttu-id="d911e-208">Informácie o regulačných aktualizáciách pre aplikácie Finance and Operations sú uvedené v časti [Regulačné aktualizácie](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span><span class="sxs-lookup"><span data-stu-id="d911e-208">For information about regulatory updates for Finance and Operations apps, see [Regulatory updates](https://docs.microsoft.com/dynamics365/finance/localizations/regulatory-updates).</span></span> <span data-ttu-id="d911e-209">Môžete sa tiež prihlásiť do LCS a pozrieť si plánované regulačné aktualizácie pomocou nástroja na vyhľadanie problému.</span><span class="sxs-lookup"><span data-stu-id="d911e-209">You can also sign in to LCS and view the planned regulatory updates using the Issue search tool.</span></span> <span data-ttu-id="d911e-210">Vyhľadávanie problémov vám umožňuje vyhľadávať podľa krajiny, typu funkcie a vydania.</span><span class="sxs-lookup"><span data-stu-id="d911e-210">Issue search lets you search by country, type of feature, and release.</span></span>