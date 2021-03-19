---
title: Odstránenie odhadu projektu
description: Táto téma poskytuje informácie o odstránení odhadu projektu po jeho dokončení.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
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
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270697"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="e70ae-103">Odstránenie odhadu projektu</span><span class="sxs-lookup"><span data-stu-id="e70ae-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e70ae-104">Odhady projektu poskytujú finančné náhľady pre prácu, ktorá sa odhaduje a plánuje pre projekt.</span><span class="sxs-lookup"><span data-stu-id="e70ae-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="e70ae-105">Ak chcete pracovať s odhadmi projektu, musíte pripojiť projekt k projektu odhadu.</span><span class="sxs-lookup"><span data-stu-id="e70ae-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="e70ae-106">Projekt odhadu je vždy založený na existujúcom projekte, avšak na jeden projekt odhadu sa môže vzťahovať viac projektov.</span><span class="sxs-lookup"><span data-stu-id="e70ae-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="e70ae-107">K projektom odhadu je možné pripojiť iba investičné projekty s pevnou cenou a tieto projekty musia patriť do rovnakej projektovej skupiny ako projekt odhadu.</span><span class="sxs-lookup"><span data-stu-id="e70ae-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="e70ae-108">Ak chcete vylúčiť projekt odhadu, musí byť dokončený.</span><span class="sxs-lookup"><span data-stu-id="e70ae-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="e70ae-109">Nasledujúce kroky vysvetľujú, ako odstrániť odhad.</span><span class="sxs-lookup"><span data-stu-id="e70ae-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="e70ae-110">Prejdite do časti **Riadenie projektu a účtovníctvo** > **Všetky projekty** a otvorte projekt.</span><span class="sxs-lookup"><span data-stu-id="e70ae-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="e70ae-111">Na karte **Spravovať** vyberte **Odhady** a na stránke **Odhad** vyberte možnosť **Eliminovať**.</span><span class="sxs-lookup"><span data-stu-id="e70ae-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="e70ae-112">Na stránke **Odstrániť odhad** na karte **Všeobecné** nastavte nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="e70ae-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="e70ae-113">**Kód obdobia**: Vyberte kód obdobia a vyberte vhodné projekty odhadu.</span><span class="sxs-lookup"><span data-stu-id="e70ae-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="e70ae-114">**Dátum odhadu** : Vyberte vhodný dátum odhadu na odstránenie.</span><span class="sxs-lookup"><span data-stu-id="e70ae-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="e70ae-115">**Eliminovať varovaniami WIP**: Túto možnosť povoľte, ak chcete dostávať oznámenie, keď bude eliminovaný odhad spojený s prebiehajúcou prácou (WIP).</span><span class="sxs-lookup"><span data-stu-id="e70ae-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="e70ae-116">Ak táto možnosť nie je povolená, eliminovanie nemôže pokračovať, ak existujú neodhadnuté transakcie.</span><span class="sxs-lookup"><span data-stu-id="e70ae-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="e70ae-117">Táto možnosť je k dispozícii, iba ak sa na projekt odhadu použije eliminácia.</span><span class="sxs-lookup"><span data-stu-id="e70ae-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="e70ae-118">Nie je k dispozícii, ak používate pravidelné zverejňovanie zverejňovania.</span><span class="sxs-lookup"><span data-stu-id="e70ae-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="e70ae-119">Toto nastavenie funguje s nastaveniami na karte **Odhad** na stránke **Parametre projektu** v skupine poľa **Povoliť eliminovanie, ak existujú neodhadované transakcie**.</span><span class="sxs-lookup"><span data-stu-id="e70ae-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="e70ae-120">**Nastaviť etapu na dokončenú**: Povolením tejto možnosti nastavíte po spustení eliminácie etapu projektu odhadu na **Dokončený**.</span><span class="sxs-lookup"><span data-stu-id="e70ae-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="e70ae-121">**Vytlačiť zoznam odhadov**: Vyberte informácie, ktoré sa majú zahrnúť pri vytlačení zoznamu odhadov.</span><span class="sxs-lookup"><span data-stu-id="e70ae-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="e70ae-122">**Zobraziť Infolog**: Povolením tejto možnosti zobrazíte Infolog.</span><span class="sxs-lookup"><span data-stu-id="e70ae-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="e70ae-123">**Dátum zverejnenia**: Vyberte dátum zverejnenia odhadu v hlavnej knihe.</span><span class="sxs-lookup"><span data-stu-id="e70ae-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="e70ae-124">Vyberte položku **OK**.</span><span class="sxs-lookup"><span data-stu-id="e70ae-124">Select **OK**.</span></span>
5. <span data-ttu-id="e70ae-125">Po dokončení procesu eliminácie sa projekt eliminovaného odhadu zobrazí so zápornou hodnotou.</span><span class="sxs-lookup"><span data-stu-id="e70ae-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="e70ae-126">Ak ste nemali v úmysle eliminovať odhad, môžete vybrať eliminovaný odhad a vybrať **Vrátiť eliminovanie**.</span><span class="sxs-lookup"><span data-stu-id="e70ae-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]