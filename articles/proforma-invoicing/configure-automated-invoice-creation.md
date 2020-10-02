---
title: Konfigurácia automatizovaného vytvárania faktúr
description: Táto téma poskytuje informácie o konfigurácii systému na automatické generovanie faktúr.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 764fd4568619e4f5676ee3cbf7fce14ffb069548
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898145"
---
# <a name="configure-automated-invoice-creation"></a><span data-ttu-id="c4a88-103">Konfigurácia automatizovaného vytvárania faktúr</span><span class="sxs-lookup"><span data-stu-id="c4a88-103">Configure automated invoice creation</span></span>

<span data-ttu-id="c4a88-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="c4a88-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c4a88-105">Vykonajte nasledujúce kroky na konfiguráciu automatického vytvárania faktúr v Project Operations.</span><span class="sxs-lookup"><span data-stu-id="c4a88-105">Complete the following steps to configure an automated invoice run in Project operations.</span></span>

1. <span data-ttu-id="c4a88-106">Prejdite do časti **Nastavenia** \> **Dávkové úlohy**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-106">Go to **Settings** \> **Batch jobs**.</span></span>
2. <span data-ttu-id="c4a88-107">Vytvorte dávkovú úlohu a pomenujte ju **Vytvorenie faktúr Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="c4a88-108">Názov dávkovej úlohy musí obsahovať výraz „Vytvorenie faktúr“.</span><span class="sxs-lookup"><span data-stu-id="c4a88-108">The name of the batch job must include the term "create invoices."</span></span>
3. <span data-ttu-id="c4a88-109">V poli **typ úlohy** vyberte položku **žiadne**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-109">In the **Job type** field, select **None**.</span></span> <span data-ttu-id="c4a88-110">Štandardne je **frekvencia denne** a **je aktívne** možnosti nastavená na **Áno.**</span><span class="sxs-lookup"><span data-stu-id="c4a88-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="c4a88-111">Vyberte **spustiť pracovný postup**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-111">Select **Run Workflow**.</span></span> <span data-ttu-id="c4a88-112">V dialógovom okne **vyhľadať záznam** sa zobrazia tri pracovné postupy:</span><span class="sxs-lookup"><span data-stu-id="c4a88-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="c4a88-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="c4a88-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="c4a88-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="c4a88-114">ProcessRunner</span></span>
    - <span data-ttu-id="c4a88-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="c4a88-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="c4a88-116">Vyberte **ProcessRunCaller** a potom **pridať**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-116">Select **ProcessRunCaller**, and then select **Add**.</span></span>
6. <span data-ttu-id="c4a88-117">V ďalšom dialógovom okne kliknite na **OK**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="c4a88-118">Pracovný postup **spánok** je nasledovaný pracovným postupom **proces**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

    <span data-ttu-id="c4a88-119">Môžete tiež vybrať **processrunner** v kroku 5.</span><span class="sxs-lookup"><span data-stu-id="c4a88-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="c4a88-120">Potom, keď vyberiete **OK**, pracovný postup **proces** je nasledovaný pracovným postupom **spánok**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-120">Then, when you select **OK**, a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="c4a88-121">Pracovné postupy **processruncaller** a **processrunner** vytvárajú faktúry.</span><span class="sxs-lookup"><span data-stu-id="c4a88-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="c4a88-122">**ProcessRunCaller** volá **processrunner**.</span><span class="sxs-lookup"><span data-stu-id="c4a88-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="c4a88-123">**ProcessRunner** je pracovný postup, ktorý skutočne vytvára faktúry.</span><span class="sxs-lookup"><span data-stu-id="c4a88-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="c4a88-124">Prechádza všetky riadky zmluvy, pre ktoré musia byť vytvorené faktúry, a vytvára faktúry pre tieto riadky.</span><span class="sxs-lookup"><span data-stu-id="c4a88-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="c4a88-125">Ak chcete určiť riadky zmluvy, pre ktoré musia byť vytvorené faktúry, úloha sa pozerá na dátumy spustenia faktúry pre riadky zmluvy.</span><span class="sxs-lookup"><span data-stu-id="c4a88-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="c4a88-126">Ak riadky zmluvy patriace do jednej zmluvy majú rovnaký dátum spustenia faktúry, transakcie sa skombinujú do jednej faktúry, ktorá má dva riadky faktúry.</span><span class="sxs-lookup"><span data-stu-id="c4a88-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="c4a88-127">Ak neexistujú žiadne transakcie na vytvorenie faktúr, úloha vynechá vytvorenie faktúry.</span><span class="sxs-lookup"><span data-stu-id="c4a88-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="c4a88-128">Po dokončení **procesrunnera**, sa volá **processruncaller**, ktorý poskytuje čas ukončenia a je uzavretý.</span><span class="sxs-lookup"><span data-stu-id="c4a88-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller**, provides the end time, and is closed.</span></span> <span data-ttu-id="c4a88-129">**ProcessRunCaller** potom spustí časovač, ktorý beží 24 hodín od zadaného času ukončenia.</span><span class="sxs-lookup"><span data-stu-id="c4a88-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="c4a88-130">Na konci časovača, je **processruncaller** uzavretý.</span><span class="sxs-lookup"><span data-stu-id="c4a88-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="c4a88-131">Dávková úloha pre vytváranie faktúr je opakujúca sa úloha.</span><span class="sxs-lookup"><span data-stu-id="c4a88-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="c4a88-132">Ak je táto dávková úloha spustená mnohokrát, sú vytvorené viaceré inštancie úlohy a spôsobujú chyby.</span><span class="sxs-lookup"><span data-stu-id="c4a88-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="c4a88-133">Preto by ste mali spustiť dávkový proces len raz, a mali by ste ho reštartovať iba v prípade, že prestane fungovať.</span><span class="sxs-lookup"><span data-stu-id="c4a88-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="c4a88-134">Hromadná fakturácia sa spustí iba pre riadky zmlúv projektu, ktoré sú konfigurované podľa plánov faktúr.</span><span class="sxs-lookup"><span data-stu-id="c4a88-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="c4a88-135">Riadok zmluvy s metódou fakturácie podľa fixnej ceny musí mať nakonfigurované medzníky.</span><span class="sxs-lookup"><span data-stu-id="c4a88-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="c4a88-136">V riadku zmluvy projektu s metódou fakturácie podľa času a materiálu bude potrebné zostaviť plán fakturácie založený na dátume.</span><span class="sxs-lookup"><span data-stu-id="c4a88-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="c4a88-137">To isté platí pre riadok zmluvy založený na projekte.</span><span class="sxs-lookup"><span data-stu-id="c4a88-137">The same applies to a project-based contract line.</span></span>     
