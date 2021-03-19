---
title: Výkon plánovania projektového zdroja
description: Táto téma poskytuje informácie o tom, ako zlepšiť výkon plánovania prostriedkov pre veľký počet projektov.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 34c31570778f9b64c23387112cf56fa1139cd0fd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289028"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="87ff1-103">Výkon plánovania projektového zdroja</span><span class="sxs-lookup"><span data-stu-id="87ff1-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="87ff1-104">Problémy s výkonom súvisiace s plánovaním zdrojov môžu nastať, keď počet projektov dosiahne tisíce.</span><span class="sxs-lookup"><span data-stu-id="87ff1-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="87ff1-105">Na zlepšenie výkonu plánovania prostriedkov je k dispozícii funkcia, ktorá používateľom umožňuje skrátiť čas potrebný na spustenie formulára dostupnosti prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="87ff1-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="87ff1-106">Týmto sa konkrétne odstráni proces synchronizácie súhrnnej kapacity zdrojov a použije sa **ResProjectResource** tabuľka na urýchlenie vyhľadávania zdrojov.</span><span class="sxs-lookup"><span data-stu-id="87ff1-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="87ff1-107">Všimnite si, že tabuľka **ResRollup** sa už nebude používať.</span><span class="sxs-lookup"><span data-stu-id="87ff1-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="87ff1-108">Ak existuje závislosť buď od procesu synchronizácie súhrnnej kapacity zdrojov, alebo od **ResProjectResource** nepoužívajte túto funkciu.</span><span class="sxs-lookup"><span data-stu-id="87ff1-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="87ff1-109">Povoliť vylepšenie výkonu plánovania zdrojov</span><span class="sxs-lookup"><span data-stu-id="87ff1-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="87ff1-110">Ak chcete povoliť vylepšenie výkonu plánovania prostriedkov, vykonajte nasledujúce kroky.</span><span class="sxs-lookup"><span data-stu-id="87ff1-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="87ff1-111">Prejdite do **Správa funkcií** > **Všetky** a v zozname funkcií vyhľadajte možnosť **Povoliť funkciu vylepšenia výkonu plánovania zdrojov projektu**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="87ff1-112">Vyberte položku **Povoliť teraz**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="87ff1-113">Ak nenájdete funkciu v zozname, stlačte možnosť **Skontrolovať aktualizácie** a obnovte zoznam.</span><span class="sxs-lookup"><span data-stu-id="87ff1-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="87ff1-114">Obnovte prehľadávač a potom prejdite na **Projektové riadenie a účtovníctvo** > **Periodické** > **Zdroje projektu** > **Synchronizujte kapacitu kalendárov zdrojov vo všetkých spoločnostiach**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="87ff1-115">Nastavte **Odstrániť existujúce záznamy o kapacite** na **Áno** na odstránenie predchádzajúcich údajov.</span><span class="sxs-lookup"><span data-stu-id="87ff1-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="87ff1-116">Ak chcete generovať prírastkové údaje, nastavte ich na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="87ff1-117">V poli **Kód obdobia** vyberte obdobie, v ktorom sa majú údaje generovať.</span><span class="sxs-lookup"><span data-stu-id="87ff1-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="87ff1-118">Ak vyberiete kód obdobia, nie je potrebné definovať počiatočný a konečný dátum.</span><span class="sxs-lookup"><span data-stu-id="87ff1-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="87ff1-119">Ak ponecháte pole **Kód obdobia** prázdne, vyberte konkrétne dátumy začatia a ukončenia na generovanie údajov.</span><span class="sxs-lookup"><span data-stu-id="87ff1-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="87ff1-120">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="87ff1-121">Toto bude distribuovať všeobecné údaje do tabuľky **ResCalendarCapacity** naprieč všetkými spoločnosťami vo vašom prostredí, takže dávkovú prácu je potrebné spustiť iba v jednej právnickej osobe.</span><span class="sxs-lookup"><span data-stu-id="87ff1-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="87ff1-122">Údaje v tejto dávkovej úlohe sú potrebné na výpočet kapacity prostriedkov prostredníctvom súvisiaceho kalendára.</span><span class="sxs-lookup"><span data-stu-id="87ff1-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="87ff1-123">Prejdite do **Projektové riadenie a účtovníctvo** > **Periodické** > **Zdroje projektu** > **Naplňte zdroje projektu vo všetkých spoločnostiach** a potom vyberte **OK**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="87ff1-124">Toto je skript na aktualizáciu údajov pre všeobecné údaje v tabuľkách **ResProjectResource**, **ResCalendarDateTimeRange** a **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="87ff1-125">Hodnoty pre pole **PSAPRojSchedRole.RootActivity** sa tiež aktualizujú.</span><span class="sxs-lookup"><span data-stu-id="87ff1-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="87ff1-126">Ak to nie je spustené, dostanete varovanie, keď sa pokúsite vykonať operácie plánovania prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="87ff1-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="87ff1-127">Vypnutie vylepšenia výkonu plánovania zdrojov</span><span class="sxs-lookup"><span data-stu-id="87ff1-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="87ff1-128">Prejdite do **Správa funkcií** > **Všetky** a v zozname funkcií vyhľadajte možnosť **Povoliť funkciu vylepšenia výkonu plánovania zdrojov projektu**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="87ff1-129">Vyberte funkciu a potom stlačte tlačidlo **Zakázať**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="87ff1-130">Obnovte prehliadač.</span><span class="sxs-lookup"><span data-stu-id="87ff1-130">Refresh your browser.</span></span>
4. <span data-ttu-id="87ff1-131">Prejdite na **Projektové riadenie a účtovníctvo** > **Pravidelne** > **Synchronizácia kapacity** > **Synchronizácia súhrnov kapacity zdroja**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="87ff1-132">Na stránke **Synchronizácia súhrnnej kapacity** nastavte **Odstrániť existujúce záznamy o kapacite** na **Áno** na odstránenie predchádzajúcich údajov.</span><span class="sxs-lookup"><span data-stu-id="87ff1-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="87ff1-133">Ak chcete generovať prírastkové údaje, nastavte ich na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="87ff1-134">V poli **Kód obdobia** vyberte obdobie, v ktorom sa majú údaje generovať.</span><span class="sxs-lookup"><span data-stu-id="87ff1-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="87ff1-135">Ak vyberiete kód obdobia, nie je potrebné definovať počiatočný a konečný dátum.</span><span class="sxs-lookup"><span data-stu-id="87ff1-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="87ff1-136">Ak ponecháte pole **Kód obdobia** prázdne, vyberte konkrétne dátumy začatia a ukončenia na generovanie údajov.</span><span class="sxs-lookup"><span data-stu-id="87ff1-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="87ff1-137">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="87ff1-138">Toto bude distribuovať všeobecné údaje do tabuľky **ResRollup** naprieč všetkými spoločnosťami vo vašom prostredí, takže dávkovú prácu je potrebné spustiť iba v jednej právnickej osobe.</span><span class="sxs-lookup"><span data-stu-id="87ff1-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="87ff1-139">Táto hromadná úloha je potrebná pre všetky zobrazenia **Dostupnosť zdrojov**.</span><span class="sxs-lookup"><span data-stu-id="87ff1-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="87ff1-140">Ak táto dávková úloha nie je spustená, údaje **ResRollup** sa budú generovať za chodu, čo môže chvíľu trvať.</span><span class="sxs-lookup"><span data-stu-id="87ff1-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]