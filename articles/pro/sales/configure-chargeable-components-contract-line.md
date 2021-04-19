---
title: Konfigurácia fakturovateľných súčastí riadka zmluvy založenej na projekte
description: Táto téma poskytuje informácie o tom, ako pridávať účtovateľné zložky do riadkov zmluvy v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: ddada2cb412ba7370fb0a750325a84772937d8d0
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858492"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="345ba-103">Konfigurácia fakturovateľných súčastí riadka zmluvy založenej na projekte</span><span class="sxs-lookup"><span data-stu-id="345ba-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="345ba-104">_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="345ba-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="345ba-105">Riadok zmluvy na základe projektu obsahuje *zahrnuté* zložky a *účtovateľné* zložky.</span><span class="sxs-lookup"><span data-stu-id="345ba-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="345ba-106">Zahrnuté zložky sú zložky, ktoré sa vzťahujú na:</span><span class="sxs-lookup"><span data-stu-id="345ba-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="345ba-107">Spôsob fakturácie a rozdelenie zákazníkov</span><span class="sxs-lookup"><span data-stu-id="345ba-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="345ba-108">Limity, ktoré sa nesmú prekročiť</span><span class="sxs-lookup"><span data-stu-id="345ba-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="345ba-109">Nastavenia frekvencie faktúr definované v riadku zmluvy na základe projektu</span><span class="sxs-lookup"><span data-stu-id="345ba-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="345ba-110">Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú pomocou poľa **Typ fakturácie**.</span><span class="sxs-lookup"><span data-stu-id="345ba-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="345ba-111">Pole **Typ fakturácie** je súpravou volieb, ktoré môžu obsahovať nasledujúce hodnoty v kontexte riadka zmluvy:</span><span class="sxs-lookup"><span data-stu-id="345ba-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="345ba-112">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-112">Chargeable</span></span>
  - <span data-ttu-id="345ba-113">Neúčtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-113">Non-chargeable</span></span>

<span data-ttu-id="345ba-114">Účtovateľné zložky možno definovať pre úlohy, roly a kategórie transakcií.</span><span class="sxs-lookup"><span data-stu-id="345ba-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="345ba-115">Účtovateľnosť je definovaná na úlohách pre riadok zmluvy projektu a vzťahuje sa na všetky triedy transakcií zahrnuté v riadku.</span><span class="sxs-lookup"><span data-stu-id="345ba-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="345ba-116">Ak je pole **Zahrnúť úlohy** v riadku zmluvy prázdne alebo nastavené na **Celý projekt**, karta **Účtovateľné úlohy** nebude k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="345ba-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="345ba-117">Účtovateľnosť definovaná pre roly pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Čas**.</span><span class="sxs-lookup"><span data-stu-id="345ba-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="345ba-118">Ak je pole **Zahrnúť čas** v riadku zmluvy nastavené na **Nie**, karta **Účtovateľné roly** nebude k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="345ba-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="345ba-119">Účtovateľnosť definovaná pre kategórie transakcií pre riadok zmluvy projektu sa vzťahuje iba na triedu transakcie **Výdavok**.</span><span class="sxs-lookup"><span data-stu-id="345ba-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="345ba-120">Ak je pole **Zahrnúť výdavky** nastavené na **Nie**, karta **Účtovateľné kategórie** nebude k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="345ba-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="345ba-121">Aktualizácia úlohy projektu ako účtovateľnej alebo neúčtovateľnej</span><span class="sxs-lookup"><span data-stu-id="345ba-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="345ba-122">Projektová úloha môže byť účtovateľná alebo neúčtovateľná v konkrétnom riadku zmluvy, čo umožňuje nasledujúce nastavenie:</span><span class="sxs-lookup"><span data-stu-id="345ba-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="345ba-123">Ak zahŕňa riadok zmluvy založený na projekte **Čas** a určitú úlohu, **T1** je k nej pridružená ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="345ba-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="345ba-124">Ak existuje druhý riadok zmluvy, ktorý obsahuje **Výdavky**, môžete úlohu T1 v riadku zmluvy priradiť ako neúčtovateľnú.</span><span class="sxs-lookup"><span data-stu-id="345ba-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="345ba-125">Výsledkom je, že všetok čas zaznamenaný pri úlohe je účtovateľný a všetky výdavky nie sú neúčtovateľné.</span><span class="sxs-lookup"><span data-stu-id="345ba-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="345ba-126">Typ fakturácie úlohy je možné nakonfigurovať na karte **Fakturovateľné úlohy** riadka zmluvy aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke úlohy riadkov zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="345ba-127">Prípadne môžete aktualizovať pole **Typ fakturácie** vo vedľajšej mriežke nastavenia fakturácie úloh projektu, ktoré zobrazuje riadky zmluvy spojené s úlohou.</span><span class="sxs-lookup"><span data-stu-id="345ba-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="345ba-128">Aktualizácia roly ako účtovateľnej alebo neúčtovateľnej</span><span class="sxs-lookup"><span data-stu-id="345ba-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="345ba-129">Rola môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="345ba-130">Typ fakturácie role je možné nakonfigurovať na karte **Účtovateľné role** v riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="345ba-131">Ak to chcete urobiť, aktualizujte pole **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné roly**.</span><span class="sxs-lookup"><span data-stu-id="345ba-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="345ba-132">Aktualizácia kategórie transakcie ako účtovateľnej alebo neúčtovateľnej</span><span class="sxs-lookup"><span data-stu-id="345ba-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="345ba-133">Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="345ba-134">Typ fakturácie transakcie je možné nakonfigurovať na karte **Účtovateľné kategórie** v riadku zmluvy na základe projektu.</span><span class="sxs-lookup"><span data-stu-id="345ba-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="345ba-135">Ak to chcete urobiť, aktualizujte pole **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné kategórie**.</span><span class="sxs-lookup"><span data-stu-id="345ba-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="345ba-136">Vyriešenie účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="345ba-136">Resolve chargeability</span></span>

<span data-ttu-id="345ba-137">Odhad alebo skutočná hodnota vytvorené pre čas sa považuje za účtovateľné iba v nasledujúcich prípadoch:</span><span class="sxs-lookup"><span data-stu-id="345ba-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="345ba-138">**Čas** je uvedený na riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="345ba-139">**Rola** je nakonfigurovaná ako účtovateľná na riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="345ba-140">**Zahrnuté úlohy** sú nastavené na **Vybrané úlohy** na riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="345ba-141">Ak sú tieto tri veci pravdivé, úloha je nakonfigurovaná ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="345ba-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="345ba-142">Odhad alebo skutočná hodnota vytvorené pre výdavky sa považujú za účtovateľné iba v nasledujúcich prípadoch:</span><span class="sxs-lookup"><span data-stu-id="345ba-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="345ba-143">**Výdavok** je uvedený na riadku zmluvy</span><span class="sxs-lookup"><span data-stu-id="345ba-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="345ba-144">**Kategória transakcie** je nakonfigurovaná ako účtovateľná na riadku zmluvy</span><span class="sxs-lookup"><span data-stu-id="345ba-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="345ba-145">**Zahrnuté úlohy** sú nastavené na **Vybraná úloha** na riadku zmluvy.</span><span class="sxs-lookup"><span data-stu-id="345ba-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="345ba-146">Ak sú tieto tri veci pravdivé, **Úloha** je nakonfigurovaná ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="345ba-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="345ba-147">Odhad alebo skutočná hodnota vytvorené pre materiál sa považujú za účtovateľné iba v nasledujúcich prípadoch:</span><span class="sxs-lookup"><span data-stu-id="345ba-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="345ba-148">**Materiály** sú uvedené na riadku zmluvy</span><span class="sxs-lookup"><span data-stu-id="345ba-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="345ba-149">**Zahrnuté úlohy** sú nastavené na **Vybrané úlohy** na riadku zmluvy</span><span class="sxs-lookup"><span data-stu-id="345ba-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="345ba-150">Ak sú tieto dve veci pravdivé, **Úloha** je nakonfigurovaná ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="345ba-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-151">
                    <strong>Zahrnie čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="345ba-152">
                    <strong>Zahrnie výdavok</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="345ba-153">
                    <strong>Zahŕňa materiály</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="345ba-154">
                    <strong>Zahrnuté úlohy</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-155">
                    <strong>Rola</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-156">
                    <strong>Kategória</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-157">
                    <strong>Úloha</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="345ba-158">
                    <strong>Dopad účtovateľnosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-159">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-160">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-161">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-162">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="345ba-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-163">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-164">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-165">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-166">Fakturácia skutočnej hodnoty času: <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-167">Typ fakturácie skutočnej hodnoty výdavku: <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-168">Typ fakturácie skutočnej hodnoty materiálu: <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-169">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-170">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-171">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-172">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="345ba-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-173">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-174">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-175">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-176">Fakturácia skutočnej hodnoty času: <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-177">Typ fakturácie skutočnej hodnoty výdavku: <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-178">Typ fakturácie skutočnej hodnoty materiálu: <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-179">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-180">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-181">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-182">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="345ba-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-183">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-184">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-185">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-186">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-187">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="345ba-188">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-189">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-190">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-191">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-192">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="345ba-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-193">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-194">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-195">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-196">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-197">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-198">Typ fakturácie skutočnej hodnoty materiálu: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-199">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-200">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-201">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-202">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="345ba-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-203">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-204">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-205">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-206">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-207">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-208">Typ fakturácie skutočnej hodnoty materiálu: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-209">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-210">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-211">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-212">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="345ba-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-213">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-214">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-215">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-216">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-217">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-218">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-220">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-221">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-222">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="345ba-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-223">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-224">
                    <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-225">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-226">Fakturácia skutočnej hodnoty času: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-227">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="345ba-228">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-230">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-231">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-232">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="345ba-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-233">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-234">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-235">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-236">Fakturácia skutočnej hodnoty času: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-237">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-238">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-239">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="345ba-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-241">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-242">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="345ba-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-243">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-244">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-245">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-246">Fakturácia skutočnej hodnoty času: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="345ba-247">Typ fakturácie skutočnej hodnoty výdavku:<strong> Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-248">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-249">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="345ba-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="345ba-251">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-252">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="345ba-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-253">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-254">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-255">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-256">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-257">Typ fakturácie skutočnej hodnoty výdavku:<strong> Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-258">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-259">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-260">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="345ba-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-262">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="345ba-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-263">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-264">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-265">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-266">Fakturácia skutočnej hodnoty času: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="345ba-267">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="345ba-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="345ba-268">Typ fakturácie skutočnej hodnoty materiálu: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="345ba-269">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="345ba-270">Áno</span><span class="sxs-lookup"><span data-stu-id="345ba-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="345ba-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="345ba-272">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="345ba-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="345ba-273">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="345ba-274">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="345ba-275">Nie je možné nastaviť</span><span class="sxs-lookup"><span data-stu-id="345ba-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="345ba-276">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-277">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="345ba-278">Typ fakturácie skutočnej hodnoty materiálu: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="345ba-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
