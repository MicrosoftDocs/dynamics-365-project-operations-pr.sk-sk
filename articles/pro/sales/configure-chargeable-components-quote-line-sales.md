---
title: Nakonfigurujte účtovateľné zložky riadka cenovej ponuky
description: Táto téma poskytuje informácie o nastavení účtovateľných a neúčtovateľných zložiek v riadku cenovej ponuky založenej na projekte.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003785"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="f90b3-103">Konfigurácia fakturovateľných súčastí riadka cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="f90b3-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="f90b3-104">_**Vzťahuje sa na:** Čiastočné nasadenie – dohoda o fakturácii pro forma, Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="f90b3-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f90b3-105">Riadok cenovej ponuky na základe projektu má koncept *zahrnutej* zložky a *účtovateľnej* zložky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="f90b3-106">Zahrnuté komponenty sa vzťahujú na:</span><span class="sxs-lookup"><span data-stu-id="f90b3-106">Included components are subject to:</span></span>

  - <span data-ttu-id="f90b3-107">Spôsob fakturácie a rozdelenie zákazníkov</span><span class="sxs-lookup"><span data-stu-id="f90b3-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="f90b3-108">Limity, ktoré sa nesmú prekročiť</span><span class="sxs-lookup"><span data-stu-id="f90b3-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="f90b3-109">Nastavenia frekvencie faktúr definované v riadku cenovej ponuky na základe projektu</span><span class="sxs-lookup"><span data-stu-id="f90b3-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="f90b3-110">Podskupinu zahrnutých zložiek možno označiť ako účtovateľnú pomocou poľa **Typ fakturácie**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="f90b3-111">Pole **Typ fakturácie** je súpravou volieb, ktoré môžu obsahovať nasledujúce hodnoty v kontexte riadka cenovej ponuky:</span><span class="sxs-lookup"><span data-stu-id="f90b3-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="f90b3-112">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-112">Chargeable</span></span>
  - <span data-ttu-id="f90b3-113">Neúčtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-113">Non-chargeable</span></span>

<span data-ttu-id="f90b3-114">Účtovateľné zložky možno definovať pre úlohy, roly a kategórie transakcií.</span><span class="sxs-lookup"><span data-stu-id="f90b3-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="f90b3-115">Účtovateľnosť je definovaná na úlohách pre riadok cenovej ponuky a vzťahuje sa na všetky triedy transakcií zahrnuté v tomto riadku.</span><span class="sxs-lookup"><span data-stu-id="f90b3-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="f90b3-116">Ak je pole **Zahrnúť úlohy** nastavené na **Celý projekt** alebo je ponechané prázdne, karta **Účtovateľné úlohy** nebude k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="f90b3-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="f90b3-117">Účtovateľnosť je definovaná pre riadok cenovej ponuky a vzťahuje sa iba na triedu transakcie **Čas**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="f90b3-118">Ak je pole **Zahrnúť čas** nastavené na **Nie** v riadku cenovej ponuky projektu, karta **Účtovateľné roly** nebude k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="f90b3-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="f90b3-119">Účtovateľnosť je definovaná pre kategórie transakcií pre riadok cenovej ponuky sa vzťahuje iba na triedu transakcie **Výdavok**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="f90b3-120">Ak je pole **Zahrnúť výdavky** nastavené na **Nie** v riadku cenovej ponuky projektu, karta **Účtovateľné kategórie** nebude k dispozícii.</span><span class="sxs-lookup"><span data-stu-id="f90b3-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="f90b3-121">Aktualizácia úlohy projektu, ktorá má byť účtovateľná alebo neúčtovateľná</span><span class="sxs-lookup"><span data-stu-id="f90b3-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="f90b3-122">Projektová úloha môže byť účtovateľná alebo neúčtovateľná v kontexte špecifického riadku cenovej ponuky na základe projektu, čo umožňuje nasledujúce nastavenie.</span><span class="sxs-lookup"><span data-stu-id="f90b3-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="f90b3-123">Ak riadok cenovej ponuky založený na projekte obsahuje **Čas** a úlohu **T1**, úloha je priradená k riadku cenovej ponuky ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="f90b3-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="f90b3-124">Ak existuje druhý riadok cenovej ponuky, ktorý obsahuje **Výdavky**, môžete úlohu **T1** v riadku cenovej ponuky priradiť ako neúčtovateľnú.</span><span class="sxs-lookup"><span data-stu-id="f90b3-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="f90b3-125">Výsledkom je, že všetok čas zaznamenaný pri úlohe je účtovateľný a všetky výdavky zaznamenané pre úlohu nie sú neúčtovateľné.</span><span class="sxs-lookup"><span data-stu-id="f90b3-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="f90b3-126">Typ fakturácie úlohy je možné nakonfigurovať na karte **Fakturovateľné úlohy** riadku cenovej ponuky založenej na projekte aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Úlohy riadkov cenovej ponuky**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="f90b3-127">Prípadne môžete aktualizovať typ fakturácie pre projektovú úlohu v poli **Typ fakturácie** vo vedľajšej mriežke v nastavení fakturácie úloh projektu, ktoré zobrazuje riadky cenovej ponuky spojené s úlohou.</span><span class="sxs-lookup"><span data-stu-id="f90b3-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="f90b3-128">Aktualizácia roly, ktorá má byť účtovateľná alebo neúčtovateľná</span><span class="sxs-lookup"><span data-stu-id="f90b3-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="f90b3-129">Rola môže byť účtovateľná alebo neúčtovateľná v kontexte konkrétneho riadka cenovej ponuky založenej na projekte.</span><span class="sxs-lookup"><span data-stu-id="f90b3-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="f90b3-130">Typ fakturácie roly je možné nakonfigurovať na karte **Fakturovateľné roly** riadku cenovej ponuky aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné roly**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="f90b3-131">Aktualizácia kategórie transakcie, ktorá má byť účtovateľná alebo neúčtovateľná</span><span class="sxs-lookup"><span data-stu-id="f90b3-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="f90b3-132">Kategória transakcie môže byť účtovateľná alebo neúčtovateľná na konkrétnom riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="f90b3-133">Typ fakturácie transakcie je možné nakonfigurovať na karte **Fakturovateľné kategórie** riadku cenovej ponuky aktualizáciou poľa **Typ fakturácie** na vedľajšej mriežke **Fakturovateľné kategórie**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="f90b3-134">Vyriešenie účtovateľnosti</span><span class="sxs-lookup"><span data-stu-id="f90b3-134">Resolve chargeability</span></span>
<span data-ttu-id="f90b3-135">Odhad alebo skutočná hodnota vytvorené pre čas sa budú považovať za účtovateľné iba v nasledujúcich prípadoch:</span><span class="sxs-lookup"><span data-stu-id="f90b3-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="f90b3-136">**Čas** je uvedený na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="f90b3-137">**Rola** je nakonfigurovaná ako účtovateľná na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="f90b3-138">**Zahrnuté úlohy** sú nastavené na možnosť **Vybrané úlohy** na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="f90b3-139">Ak sú tieto tri veci pravdivé, **Úloha** je tiež nakonfigurovaná ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="f90b3-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="f90b3-140">Odhad alebo skutočná hodnota vytvorené pre výdavky sa považujú za účtovateľné iba v nasledujúcich prípadoch:</span><span class="sxs-lookup"><span data-stu-id="f90b3-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="f90b3-141">**Výdavok** je uvedený na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="f90b3-142">**Kategória transakcie** je nakonfigurovaná ako účtovateľná na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="f90b3-143">**Zahrnuté úlohy** sú nastavené na možnosť **Vybrané úlohy** na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="f90b3-144">Ak sú tieto tri veci pravdivé, **Úloha** je tiež nakonfigurovaná ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="f90b3-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="f90b3-145">Odhad alebo skutočná hodnota vytvorené pre materiál sa budú považovať za účtovateľné iba v nasledujúcich prípadoch:</span><span class="sxs-lookup"><span data-stu-id="f90b3-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="f90b3-146">**Materiál** je uvedený na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="f90b3-147">**Zahrnuté úlohy** sú nastavené na možnosť **Vybrané úlohy** na riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="f90b3-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="f90b3-148">Ak sú tieto dve veci pravdivé, **Úloha** by mala byť tiež nakonfigurovaná ako účtovateľná.</span><span class="sxs-lookup"><span data-stu-id="f90b3-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-149">
                    <strong>Zahrnie čas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="f90b3-150">
                    <strong>Zahrnie výdavok</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="f90b3-151">
                    <strong>Zahŕňa materiály</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="f90b3-152">
                    <strong>Zahrnuté úlohy</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-153">
                    <strong>Rola</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-154">
                    <strong>Kategória</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-155">
                    <strong>Úloha</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="f90b3-156">
                    <strong>Dopad účtovateľnosti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-157">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-158">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-159">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-160">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="f90b3-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-161">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-162">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-163">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-164">Fakturácia skutočnej hodnoty času: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-165">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-166">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-167">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-168">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-169">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-170">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="f90b3-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-171">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-172">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-173">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-174">Fakturácia skutočnej hodnoty času: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-175">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-176">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-177">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-178">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-179">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-180">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="f90b3-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-181">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-182">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-183">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-184">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-185">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-186">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-187">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-188">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-189">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-190">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="f90b3-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-191">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-192">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-193">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-194">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-195">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-196">Typ fakturácie skutočnej hodnoty materiálu: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-197">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-198">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-199">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-200">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="f90b3-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-201">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-202">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-203">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-204">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-205">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-206">Typ fakturácie skutočnej hodnoty materiálu: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-207">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-208">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-209">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-210">Iba vybraté úlohy</span><span class="sxs-lookup"><span data-stu-id="f90b3-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-211">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-212">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-213">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-214">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-215">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-216">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-218">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-219">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-220">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="f90b3-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-221">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-222">
                    <strong>Účtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-223">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-224">Fakturácia skutočnej hodnoty času: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-225">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-226">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-228">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-229">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-230">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="f90b3-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-231">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-232">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-233">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-234">Fakturácia skutočnej hodnoty času: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-235">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-236">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-237">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="f90b3-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-239">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-240">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="f90b3-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-241">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-242">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-243">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-244">Fakturácia skutočnej hodnoty času: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-245">Typ fakturácie skutočnej hodnoty výdavku:<strong> Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-246">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-247">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="f90b3-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="f90b3-249">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-250">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="f90b3-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-251">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-252">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-253">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-254">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-255">Typ fakturácie skutočnej hodnoty výdavku:<strong> Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-256">Typ fakturácie skutočnej hodnoty materiálu: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-257">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-258">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="f90b3-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-260">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="f90b3-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-261">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-262">Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-263">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-264">Fakturácia skutočnej hodnoty času: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-265">Typ fakturácie skutočnej hodnoty výdavku: Účtovateľné</span><span class="sxs-lookup"><span data-stu-id="f90b3-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="f90b3-266">Typ fakturácie skutočnej hodnoty materiálu: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="f90b3-267">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="f90b3-268">Áno</span><span class="sxs-lookup"><span data-stu-id="f90b3-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="f90b3-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="f90b3-270">Celý projekt</span><span class="sxs-lookup"><span data-stu-id="f90b3-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="f90b3-271">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="f90b3-272">
                    <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="f90b3-273">Nedá sa nastaviť</span><span class="sxs-lookup"><span data-stu-id="f90b3-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="f90b3-274">Fakturácia skutočnej hodnoty času: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-275">Typ fakturácie skutočnej hodnoty výdavku: <strong>Neúčtovateľné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="f90b3-276">Typ fakturácie skutočnej hodnoty materiálu: <strong>Nedostupné</strong>
                </span><span class="sxs-lookup"><span data-stu-id="f90b3-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
