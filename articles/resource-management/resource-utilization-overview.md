---
title: Prehľad využitia zdroja
description: Táto téma poskytuje informácie o zobrazení využitia zdrojov v aplikácii Project Operations.
author: ruhercul
ms.date: 11/05/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: c9464b1de87211f8317a39a1d749e619769309ae
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367955"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="873ed-103">Prehľad využitia zdroja</span><span class="sxs-lookup"><span data-stu-id="873ed-103">Resource utilization overview</span></span>

<span data-ttu-id="873ed-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="873ed-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="873ed-105">Zdroje môžu mať cieľové fakturovateľné využitie.</span><span class="sxs-lookup"><span data-stu-id="873ed-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="873ed-106">Tento cieľ využitia je definovaný ako atribút v predvolenej role zdroja, alebo nastavenie v zázname jednotlivých rezervovateľných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="873ed-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="873ed-107">Výpočty využitia sú založené na skutočných hodinách, ktoré zdroje hlásili pomocou schválených časových položiek.</span><span class="sxs-lookup"><span data-stu-id="873ed-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="873ed-108">Na výpočet využitia sa používajú nasledujúce vzorce:</span><span class="sxs-lookup"><span data-stu-id="873ed-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="873ed-109">Fakturovateľné využitie = Spoplatnená skutočná kapacita hodín ÷ kapacita zdroja</span><span class="sxs-lookup"><span data-stu-id="873ed-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="873ed-110">Nefakturovateľné využitie = skutočný čas s fakturáciou typu ID = Nefakturovateľné, doplnkové alebo nie je k dispozícii ÷ zdroj kapacity</span><span class="sxs-lookup"><span data-stu-id="873ed-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="873ed-111">Interné = skutočný čas bez predajnej zmluvy ÷ kapacita zdrojov</span><span class="sxs-lookup"><span data-stu-id="873ed-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="873ed-112">Kapacita zdrojov = pracovné hodiny zdroja – mimo pracoviska – dni pracovného času</span><span class="sxs-lookup"><span data-stu-id="873ed-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="873ed-113">**Zobrazenie využitia** prostriedkov môžete nájsť na table **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="873ed-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="873ed-114">Každá bunka v mriežke predstavuje percento fakturovateľného využitia prostriedku v období, ako je napríklad deň, týždeň alebo mesiac.</span><span class="sxs-lookup"><span data-stu-id="873ed-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="873ed-115">Na vyfarbenie buniek sa používajú nasledujúce vzorce:</span><span class="sxs-lookup"><span data-stu-id="873ed-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="873ed-116">**Zelená**: Fakturovateľné využitie > = Cieľ využívanie zdrojov</span><span class="sxs-lookup"><span data-stu-id="873ed-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="873ed-117">**Žltá**: Cieľové využitie – 20 < = Fakturovateľná využitie < Cieľové využitie</span><span class="sxs-lookup"><span data-stu-id="873ed-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="873ed-118">**Červená**: Fakturovateľná využitie < Cieľové využitie – 20</span><span class="sxs-lookup"><span data-stu-id="873ed-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="873ed-119">Keďže zobrazenie **Využitie zdroja** je založené na tabuli plánovania, môžete filtrovať výsledky pomocou možností filtrovania tabule plánovania.</span><span class="sxs-lookup"><span data-stu-id="873ed-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="873ed-120">Mriežka si vyžaduje, aby ste stanovili cieľové využitie buď roly, alebo individuálneho zdroja.</span><span class="sxs-lookup"><span data-stu-id="873ed-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="873ed-121">Ak tak chcete urobiť, prejdite na **Zdroje** > **Zdrojové roly**.</span><span class="sxs-lookup"><span data-stu-id="873ed-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="873ed-122">Okrem toho musí byť priradená predvolená rola pre každý rezervovateľný prostriedok.</span><span class="sxs-lookup"><span data-stu-id="873ed-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="873ed-123">Prejdite na **Zdroje** > **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="873ed-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="873ed-124">Na karte **Project Service** skontrolujte, či je definovaná rola zdroja a či pole **Je predvolená** je nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="873ed-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="873ed-125">Môžete pridať ďalšie roly, kde **Je predvolená** = **Nie**.</span><span class="sxs-lookup"><span data-stu-id="873ed-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="873ed-126">Rola, kde **Je predvolená** = **Áno** sa používa na vyhodnotenie využitia zdroja proti cieľu pre túto rolu.</span><span class="sxs-lookup"><span data-stu-id="873ed-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="873ed-127">Na karte **Project Service** môžete tiež nastaviť individuálne cieľové využitie prostriedku.</span><span class="sxs-lookup"><span data-stu-id="873ed-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="873ed-128">Výpočet využitia potom použije cieľové využitie na vyhodnotenie cieľového prostriedku namiesto cieľa predvolenej roly prostriedku.</span><span class="sxs-lookup"><span data-stu-id="873ed-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="873ed-129">Využitie sa zobrazuje pre zdroj len vtedy, ak tento zdroj schválil účtovateľný čas počas obdobia, ktoré je zobrazené v mriežke.</span><span class="sxs-lookup"><span data-stu-id="873ed-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]