---
title: Vytvoriť zadanie času
description: Táto téma poskytuje informácie o tom, ako vytvoriť zadania času.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084455"
---
# <a name="create-time-entries"></a><span data-ttu-id="aed4f-103">Vytvoriť zadanie času</span><span class="sxs-lookup"><span data-stu-id="aed4f-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="aed4f-104">V predchádzajúcich verziách Dynamics 365 Project Service Automation boli zadané časové zápisy na týždennej báze.</span><span class="sxs-lookup"><span data-stu-id="aed4f-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="aed4f-105">Vo verzii 3 Project Service Automation, časové zadávania sú zapisujú na dennej báze.</span><span class="sxs-lookup"><span data-stu-id="aed4f-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="aed4f-106">Po vytvorení niekoľkých časových položiek ich však môžete hromadne vytvárať alebo kopírovať.</span><span class="sxs-lookup"><span data-stu-id="aed4f-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="aed4f-107">Vytvoriť zadanie času</span><span class="sxs-lookup"><span data-stu-id="aed4f-107">Create a time entry</span></span>

<span data-ttu-id="aed4f-108">Ak chcete vytvoriť zadanie času, postupujte podľa týchto krokov.</span><span class="sxs-lookup"><span data-stu-id="aed4f-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="aed4f-109">Na stránke **Zadania času** stlačte možnosť **Nové**.</span><span class="sxs-lookup"><span data-stu-id="aed4f-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="aed4f-110">V dialógovom okne **Rýchle vytvorenie: Zadanie času** zadajte dobu trvania položky v minútach, hodinách alebo dňoch.</span><span class="sxs-lookup"><span data-stu-id="aed4f-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="aed4f-111">Trvanie musí byť zadané v nasledujúcom formáte *x* minút, *x* hodín alebo *x* dní.</span><span class="sxs-lookup"><span data-stu-id="aed4f-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="aed4f-112">Hodiny a dni je taktiež možné zadať pomocou desatinných miest, napríklad *x.x* hod. alebo *x.x* dní.</span><span class="sxs-lookup"><span data-stu-id="aed4f-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="aed4f-113">Vyberte typ časovej položky a projekt, pre ktorý zadávate časovú položku.</span><span class="sxs-lookup"><span data-stu-id="aed4f-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="aed4f-114">V poli **Projektová úloha** nájdite úlohu pre túto časovú položku.</span><span class="sxs-lookup"><span data-stu-id="aed4f-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="aed4f-115">Ak vytvárate časovú položku pre úlohu, ktorá nie je priradená používateľovi, v poli **Úloha projektu** vyberte tlačidlo **Hľadať** , vyberte položku **Zmeniť zobrazenie** a potom vyberte **Všetky aktívne projektové úlohy** na vypísanie všetkých úloh.</span><span class="sxs-lookup"><span data-stu-id="aed4f-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="aed4f-116">Zadajte prípadne vyžadovaný popis a potom stlačte možnosť **Uložiť a zavrieť**.</span><span class="sxs-lookup"><span data-stu-id="aed4f-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="aed4f-117">Po vytvorení a uložení časovej položky ho môžete upraviť v mriežke časového vstupu.</span><span class="sxs-lookup"><span data-stu-id="aed4f-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="aed4f-118">Mriežka časového vstupu podporuje dva formáty:</span><span class="sxs-lookup"><span data-stu-id="aed4f-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="aed4f-119">Môžete zadať časové zápisy vo formáte **hh:mm**.</span><span class="sxs-lookup"><span data-stu-id="aed4f-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="aed4f-120">Tento formát sa potom skonvertuje na hodiny a zlomky.</span><span class="sxs-lookup"><span data-stu-id="aed4f-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="aed4f-121">Môžete zadať hodiny a zlomky priamo.</span><span class="sxs-lookup"><span data-stu-id="aed4f-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="aed4f-122">Všimnite si, že zlomky hodiny nie sú minúty.</span><span class="sxs-lookup"><span data-stu-id="aed4f-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="aed4f-123">Preto 1,5 hodín predstavuje 1 hodinu a 30 minút.</span><span class="sxs-lookup"><span data-stu-id="aed4f-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="aed4f-124">Rovnaké pravidlo platí pre zlomky dňa.</span><span class="sxs-lookup"><span data-stu-id="aed4f-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="aed4f-125">Jeden deň je 24 hodín a 0,5 dní predstavuje 12 hodín.</span><span class="sxs-lookup"><span data-stu-id="aed4f-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="aed4f-126">Hromadné vytvorenie zadaní času</span><span class="sxs-lookup"><span data-stu-id="aed4f-126">Bulk create time entries</span></span>

<span data-ttu-id="aed4f-127">Po vytvorení niekoľkých časových položiek ich môžete skopírovať na hromadné vytvorenie dodatočných časových položiek.</span><span class="sxs-lookup"><span data-stu-id="aed4f-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="aed4f-128">Na stránke **Zadania času** stlačte možnosť **Kopírovať týždeň**.</span><span class="sxs-lookup"><span data-stu-id="aed4f-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="aed4f-129">V skupine poľa **Obdobie od** použite polia **Počiatočný dátum** a **Koncový dátum** na definovanie rozsahu dátumov, z ktorého sa majú kopírovať časové položky.</span><span class="sxs-lookup"><span data-stu-id="aed4f-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="aed4f-130">V skupine poľa **Obdobie do** v poli **Počiatočný dátum** zadajte dátum vytvorenia položiek času.</span><span class="sxs-lookup"><span data-stu-id="aed4f-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="aed4f-131">Výberom položky **Kopírovať** vytvoríte kópiu časových položiek zodpovedajúcich dňu týždňa, ktorý je zadaný v skupine poľa **Obdobie do**.</span><span class="sxs-lookup"><span data-stu-id="aed4f-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="aed4f-132">Napríklad, pondelkové časové zadanie z minulého týždňa bude skopírované do pondelka pre týždeň uvedený v skupine poľa **Obdobie do**.</span><span class="sxs-lookup"><span data-stu-id="aed4f-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="aed4f-133">Import údajov pre zadania času</span><span class="sxs-lookup"><span data-stu-id="aed4f-133">Import data for time entries</span></span>

<span data-ttu-id="aed4f-134">Môžete importovať údaje z projektových rezervácií a priradení.</span><span class="sxs-lookup"><span data-stu-id="aed4f-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="aed4f-135">Keď importujete údaje, môžete zadať rozsah dátumov rezervácií, ktoré chcete importovať, a potom explicitne vybrať rezervácie, ktoré by sa mali vytvoriť ako časové zadania **Koncept**.</span><span class="sxs-lookup"><span data-stu-id="aed4f-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="aed4f-136">Možnosti zoskupovania, zoraďovania, vyhľadávania a filtrovania</span><span class="sxs-lookup"><span data-stu-id="aed4f-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="aed4f-137">Položky času môžete zoskupiť a filtrovať podľa dimenzií, ktoré sú zadané v stĺpcoch.</span><span class="sxs-lookup"><span data-stu-id="aed4f-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="aed4f-138">V poli **Zoskupiť podľa** vyberte dimenziu, ktorá sa má použiť na filtrovanie časových položiek.</span><span class="sxs-lookup"><span data-stu-id="aed4f-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="aed4f-139">Záznamy časových položiek môžete zoradiť vo vzostupnom alebo zostupnom poradí pomocou šípky zoradiť v záhlaví stĺpcov.</span><span class="sxs-lookup"><span data-stu-id="aed4f-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="aed4f-140">Okrem toho môžete zobraziť alebo skryť položky výberom tlačidla **Filter** na hlavičke stĺpcov a potom do **vyhľadávacieho** poľa zadajte text, ktorý by sa mal použiť na vyhľadávanie časových položiek podľa názvu projektu, úlohy projektu, času položka alebo zdroj.</span><span class="sxs-lookup"><span data-stu-id="aed4f-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
