---
title: Časový plán výdavkov na vyšetrovanie federálnych ocenení
description: Táto téma poskytuje informácie o dotazníku Časový plán výdavkov federálneho ocenenia.
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010085"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="98f8b-103">Časový plán výdavkov na vyšetrovanie federálnych ocenení</span><span class="sxs-lookup"><span data-stu-id="98f8b-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98f8b-104">Podľa Úradu pre správu a rozpočet A-133 sa na agentúry, ktoré dostávajú federálne fondy, vzťahujú požiadavky na audit, ktoré sa označujú aj ako jednotné audity.</span><span class="sxs-lookup"><span data-stu-id="98f8b-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="98f8b-105">Proces auditu sa používa na opakované podávanie správ o príjmoch a výdavkoch federálnych grantov.</span><span class="sxs-lookup"><span data-stu-id="98f8b-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="98f8b-106">Súčasťou správy o jednotnom audite je Časový plán výdavkov federálneho ocenenia (SEFA).</span><span class="sxs-lookup"><span data-stu-id="98f8b-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="98f8b-107">Časový plán výdavkov na federálne ocenenia obsahuje názov a číslo Katalógu federálnej domácej pomoci (CFDA), číslo grantu, rok poskytnutia grantu, názov federálnej agentúry, ktorá poskytuje finančné prostriedky, a názov hesla prostredníctvom subjektu.</span><span class="sxs-lookup"><span data-stu-id="98f8b-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="98f8b-108">Dotaz je na konkrétne obdobie.</span><span class="sxs-lookup"><span data-stu-id="98f8b-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="98f8b-109">Toto obdobie je zvyčajne rovnaké ako obdobie účtovnej závierky, čo je fiškálny rok.</span><span class="sxs-lookup"><span data-stu-id="98f8b-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="98f8b-110">Dotaz zahŕňa granty, ktoré majú predpokladané dátumy vo vybranom rozsahu dátumov.</span><span class="sxs-lookup"><span data-stu-id="98f8b-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="98f8b-111">**Grantová agentúra** v stĺpci dopytu sa zobrazuje zákazník s grantom alebo v prípade grantu s priamym prenosom agentúra s grantom.</span><span class="sxs-lookup"><span data-stu-id="98f8b-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="98f8b-112">Pokiaľ ide o prechodný grant, **Agentúra s priamym prechodom** stĺpec zobrazuje zákazníka s grantom.</span><span class="sxs-lookup"><span data-stu-id="98f8b-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="98f8b-113">Pokiaľ nejde o prechodný grant, **Agentúra s priamym prechodom** stĺpec bude prázdny.</span><span class="sxs-lookup"><span data-stu-id="98f8b-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="98f8b-114">Nastavenie klastrov CFDA</span><span class="sxs-lookup"><span data-stu-id="98f8b-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="98f8b-115">Klastre CFDA, ktoré môžu byť spojené s číslami CFDA, musíte nastaviť v dotazníku Schedule of Expenditures of Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="98f8b-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="98f8b-116">Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Nastavenie \> Granty \> Katalóg klastrov federálnej domácej pomoci**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="98f8b-117">Stlačte možnosť **Nový** a vytvorte klaster CFDA.</span><span class="sxs-lookup"><span data-stu-id="98f8b-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="98f8b-118">Zadajte názov klastra.</span><span class="sxs-lookup"><span data-stu-id="98f8b-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="98f8b-119">Zmeny vykonajte výberom položky **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="98f8b-120">Nastavte čísla CFDA</span><span class="sxs-lookup"><span data-stu-id="98f8b-120">Set up CFDA numbers</span></span>

<span data-ttu-id="98f8b-121">Klastre CFDA, ktoré môžu byť priradené ku grantom a môžu byť zaradené v dotazníku Schedule of Expenditures of Federal Awards.</span><span class="sxs-lookup"><span data-stu-id="98f8b-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="98f8b-122">Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Nastavenie \> Granty \> Katalóg čísel federálnej domácej pomoci**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="98f8b-123">Stlačte možnosť **Nový** a vytvorte číslo CFDA.</span><span class="sxs-lookup"><span data-stu-id="98f8b-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="98f8b-124">V stĺpci **Číslo** zadajte číslo CFDA.</span><span class="sxs-lookup"><span data-stu-id="98f8b-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="98f8b-125">Stlačte kláves **Tab**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="98f8b-126">V stĺpci **Opis** zadajte názov CFDA.</span><span class="sxs-lookup"><span data-stu-id="98f8b-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="98f8b-127">Stlačte kláves **Tab**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="98f8b-128">V priečinku **Programový klaster** do poľa pridajte vhodný klaster CFDA.</span><span class="sxs-lookup"><span data-stu-id="98f8b-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="98f8b-129">Zmeny vykonajte výberom položky **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="98f8b-130">Nastaviť granty pre správu pre Schedule of Expenditures of Federal Awards</span><span class="sxs-lookup"><span data-stu-id="98f8b-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="98f8b-131">Prejdite do **Projektové riadenie a účtovníctvo \> Granty \> Granty** a zvoľte si existujúci grant.</span><span class="sxs-lookup"><span data-stu-id="98f8b-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="98f8b-132">Na rýchlej karte **Nastavenia** v poli **Katalóg Federal Domestic Assistance** priraďte číslo CFDA.</span><span class="sxs-lookup"><span data-stu-id="98f8b-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="98f8b-133">Číslo CFDA na grante určuje klaster CFDA na vykazovanie.</span><span class="sxs-lookup"><span data-stu-id="98f8b-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="98f8b-134">Na FastTab **Kontaktné informácie** zadajte informácie o poskytovateľovi vykonaním týchto krokov:</span><span class="sxs-lookup"><span data-stu-id="98f8b-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="98f8b-135">V poli **Zákazník grantu** do poľa zadajte zákazníka, ktorý je zodpovedný za grant.</span><span class="sxs-lookup"><span data-stu-id="98f8b-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="98f8b-136">V prípade existujúceho grantu môžu byť tieto informácie už zadané.</span><span class="sxs-lookup"><span data-stu-id="98f8b-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="98f8b-137">Uveďte, či je grantový zákazník donorom.</span><span class="sxs-lookup"><span data-stu-id="98f8b-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="98f8b-138">Ak je grantovým zákazníkom donor, nechajte políčko **Priamy prechod** neoznačené.</span><span class="sxs-lookup"><span data-stu-id="98f8b-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="98f8b-139">Ak je finančným darcom iný zákazník a zákazník, ktorý je príjemcom grantu, je zodpovedný za výdavky a sledovanie peňazí, označte políčko **Priamy prechod**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="98f8b-140">Ak ste začiarkli políčko **Priamy prechod** v predchádzajúcom kroku, v priečinku **Grantová agentúra** do poľa zadajte zákazníka, ktorý poskytol grant.</span><span class="sxs-lookup"><span data-stu-id="98f8b-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="98f8b-141">Agentúra poskytujúca pomoc a zákazník, ktorý je príjemcom grantu, nemôžu byť rovnakí zákazníci.</span><span class="sxs-lookup"><span data-stu-id="98f8b-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="98f8b-142">Tu je príklad priameho grantu:</span><span class="sxs-lookup"><span data-stu-id="98f8b-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="98f8b-143">Federálna vláda financovala štátny projekt infraštruktúry.</span><span class="sxs-lookup"><span data-stu-id="98f8b-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="98f8b-144">Federálna vláda dala peniaze štátu na utratenie.</span><span class="sxs-lookup"><span data-stu-id="98f8b-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="98f8b-145">V tomto prípade je federálnou vládou agentúra poskytujúca granty a štát je zákazníkom grantu.</span><span class="sxs-lookup"><span data-stu-id="98f8b-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="98f8b-146">Pri prvom zapnutí tejto funkcie sa počiatočné čísla CFDA zadajú pomocou existujúcich čísel v grantoch.</span><span class="sxs-lookup"><span data-stu-id="98f8b-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="98f8b-147">Vylúčiť granty z vykazovania SEFA na základe typu grantu</span><span class="sxs-lookup"><span data-stu-id="98f8b-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="98f8b-148">Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Nastavenie \> Granty \> Typy grantov**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="98f8b-149">Na karte rýchlej karte **Predvolené informácie** označte políčko **Vylúčte z rozvrhu výdavkov federálnych ocenení**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="98f8b-150">Zmeny vykonajte výberom položky **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="98f8b-151">Spustite Časový plán výdavkov na vyšetrovanie federálnych ocenení</span><span class="sxs-lookup"><span data-stu-id="98f8b-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="98f8b-152">Prejdite do ponuky **Projektové riadenie a účtovníctvo \> Dotazy a otázky \> Dotaz na udelenie grantu \> Časový plán výdavkov federálnych ocenení**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="98f8b-153">V časti **Parametre** dodržiavajte nasledovné kroky:</span><span class="sxs-lookup"><span data-stu-id="98f8b-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="98f8b-154">V poli **Interval dátumu** zvoľte kód pre interval dátumov.</span><span class="sxs-lookup"><span data-stu-id="98f8b-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="98f8b-155">Prípadne v poliach **Dátum Od** a **Dátum Do** definujte časový interval.</span><span class="sxs-lookup"><span data-stu-id="98f8b-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="98f8b-156">Voliteľné: Ak chcete do dopytu zahrnúť iba fakturované transakcie, nastavte možnosť **Zahrňte iba fakturované výnosy** na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="98f8b-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="98f8b-157">Stĺpce</span><span class="sxs-lookup"><span data-stu-id="98f8b-157">Columns</span></span>

<span data-ttu-id="98f8b-158">Dotazník o Časový plán výdavkov na vyšetrovanie federálnych ocenení zahŕňa nasledovné stĺpce:</span><span class="sxs-lookup"><span data-stu-id="98f8b-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="98f8b-159">Katalóg názvu klastra federálnej domácej pomoci</span><span class="sxs-lookup"><span data-stu-id="98f8b-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="98f8b-160">Grantová agentúra</span><span class="sxs-lookup"><span data-stu-id="98f8b-160">Grantor agency</span></span>
- <span data-ttu-id="98f8b-161">Agentúra s priamym prechodom</span><span class="sxs-lookup"><span data-stu-id="98f8b-161">Pass-through agency</span></span>
- <span data-ttu-id="98f8b-162">Názov grantu</span><span class="sxs-lookup"><span data-stu-id="98f8b-162">Grant name</span></span>
- <span data-ttu-id="98f8b-163">ID grantu</span><span class="sxs-lookup"><span data-stu-id="98f8b-163">Grant ID</span></span>
- <span data-ttu-id="98f8b-164">ID žiadosti o grant</span><span class="sxs-lookup"><span data-stu-id="98f8b-164">Grant application ID</span></span>
- <span data-ttu-id="98f8b-165">Katalóg klastra federálnej domácej pomoci</span><span class="sxs-lookup"><span data-stu-id="98f8b-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="98f8b-166">Potvrdenia</span><span class="sxs-lookup"><span data-stu-id="98f8b-166">Receipts</span></span>
- <span data-ttu-id="98f8b-167">Výdavky</span><span class="sxs-lookup"><span data-stu-id="98f8b-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]