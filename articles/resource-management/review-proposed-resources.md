---
title: Kontrola navrhovaných zdrojov
description: Táto téma poskytuje informácie o tom, ako navrhovať projektové zdroje.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 212b80a7fde8368eedd7572dd5f9278cc53fae98
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897380"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="2bb29-103">Kontrola navrhovaných zdrojov</span><span class="sxs-lookup"><span data-stu-id="2bb29-103">Review proposed resources</span></span>

<span data-ttu-id="2bb29-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="2bb29-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2bb29-105">Správcovia zdrojov môžu navrhnúť zdroj projektového manažéra pomocou požiadavky prostriedku.</span><span class="sxs-lookup"><span data-stu-id="2bb29-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="2bb29-106">V mriežke požiadavky alebo samotnej žiadosti vyberte položku **Vyhľadať zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="2bb29-107">Na stránke **Asistent plánovania** vyberte zdroj a potom v table stav **Vytvoriť rezerváciu zdroja** v poli **Stav rezervácie** zvoľte možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="2bb29-108">Nasledujúce aktualizácie stavu sa vyskytujú:</span><span class="sxs-lookup"><span data-stu-id="2bb29-108">The following status updates occur:</span></span>

- <span data-ttu-id="2bb29-109">Na stránke **Asistent plánovania** sa aktualizujú indikátory stavu, ktoré naznačujú, že rezervácia je navrhnutá a nie je pevne rezervovaná.</span><span class="sxs-lookup"><span data-stu-id="2bb29-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="2bb29-110">Na žiadosť o prostriedok, stav sa zmení na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="2bb29-111">Na karte **Tím** projektu sa hodnota všeobecných členov tímu **Stav žiadosti** zmenila na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="2bb29-112">Projektový manažér môže buď prijať, alebo zamietnuť návrh.</span><span class="sxs-lookup"><span data-stu-id="2bb29-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="2bb29-113">Keď správcovia zdrojov spracúvajú žiadosti o prostriedky, môžu použiť ktorýkoľvek z nasledujúcich prístupov:</span><span class="sxs-lookup"><span data-stu-id="2bb29-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="2bb29-114">Navrhnite viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na splnenie požadovaných hodín.</span><span class="sxs-lookup"><span data-stu-id="2bb29-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="2bb29-115">Navrhované hodiny sa potom rozdelia medzi viaceré zdroje, ktoré môžu uspokojiť požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="2bb29-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="2bb29-116">V tomto scenári, hodiny nemožno prekrývať.</span><span class="sxs-lookup"><span data-stu-id="2bb29-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="2bb29-117">Navrhnite menej zdrojov, než je požadované.</span><span class="sxs-lookup"><span data-stu-id="2bb29-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="2bb29-118">V tomto scenári, navrhovaná kapacita prostriedku je menšia ako požadované hodiny, ktoré žiadateľ zadal.</span><span class="sxs-lookup"><span data-stu-id="2bb29-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="2bb29-119">Preto, keď žiadateľ akceptuje navrhované prostriedky, nesplnených zdrojov požiadavka je vytvorená na zachytenie zostávajúcich požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="2bb29-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="2bb29-120">Zarezervujte viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na dokončenie prác.</span><span class="sxs-lookup"><span data-stu-id="2bb29-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="2bb29-121">Rezervujte menej zdrojov, než je požadované.</span><span class="sxs-lookup"><span data-stu-id="2bb29-121">Book fewer resources than are required.</span></span> <span data-ttu-id="2bb29-122">V tomto scenári, rezervované hodiny sú menej ako požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="2bb29-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="2bb29-123">Systém vás prevedie navrhnutie zdrojov namiesto rezervácií, aby žiadateľa mohol overiť a sledovať zostávajúci dopyt.</span><span class="sxs-lookup"><span data-stu-id="2bb29-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="2bb29-124">Fakturovateľné využitie</span><span class="sxs-lookup"><span data-stu-id="2bb29-124">Billable utilization</span></span>

<span data-ttu-id="2bb29-125">Zdroje môžu mať cieľové fakturovateľné využitie.</span><span class="sxs-lookup"><span data-stu-id="2bb29-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="2bb29-126">Tento cieľ využitia je buď definovaný ako atribút na zdroja predvolenú rolu, alebo nastavenie na záznam jednotlivých rezervovateľných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="2bb29-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="2bb29-127">Výpočty využitia sú založené na skutočných hodinách, ktoré zdroje hlásili pomocou schválených časových položiek.</span><span class="sxs-lookup"><span data-stu-id="2bb29-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="2bb29-128">Na výpočet využitia sa používajú nasledujúce vzorce:</span><span class="sxs-lookup"><span data-stu-id="2bb29-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="2bb29-129">Fakturovateľné využitie = Spoplatnená skutočná kapacita hodín ÷ kapacita zdroja</span><span class="sxs-lookup"><span data-stu-id="2bb29-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="2bb29-130">Nefakturovateľné využitie = skutočný čas s fakturáciou typu ID = Nefakturovateľné, doplnkové alebo nie je k dispozícii ÷ zdroj kapacity</span><span class="sxs-lookup"><span data-stu-id="2bb29-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="2bb29-131">Interné = skutočný čas bez predajnej zmluvy ÷ kapacita zdrojov</span><span class="sxs-lookup"><span data-stu-id="2bb29-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="2bb29-132">Kapacita zdrojov = pracovné hodiny zdroja – mimo pracoviska – dni pracovného času</span><span class="sxs-lookup"><span data-stu-id="2bb29-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="2bb29-133">**Zobrazenie využitia** prostriedkov môžete nájsť na table **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="2bb29-134">Každá bunka v mriežke predstavuje percento fakturovateľného využitia prostriedku v období, ako je napríklad deň, týždeň alebo mesiac.</span><span class="sxs-lookup"><span data-stu-id="2bb29-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="2bb29-135">Na vyfarbenie buniek sa používajú nasledujúce vzorce:</span><span class="sxs-lookup"><span data-stu-id="2bb29-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="2bb29-136">**Zelená:** Fakturovateľné využitie \>= Cieľové využitie zdroja</span><span class="sxs-lookup"><span data-stu-id="2bb29-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="2bb29-137">**Žltá:** Cieľové využitie – 20 \<Fakturovateľná využitie \< Cieľové využitie</span><span class="sxs-lookup"><span data-stu-id="2bb29-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="2bb29-138">**Červená:** Fakturovateľná využitie \< Cieľové využitie – 20</span><span class="sxs-lookup"><span data-stu-id="2bb29-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="2bb29-139">Keďže zobrazenie **Využitie zdroja** je založené na tabuli plánovania, môžete filtrovať výsledky pomocou možností filtrovania tabule plánovania.</span><span class="sxs-lookup"><span data-stu-id="2bb29-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="2bb29-140">Mriežka si vyžaduje, aby ste stanovili cieľové využitie buď roly, alebo individuálneho zdroja.</span><span class="sxs-lookup"><span data-stu-id="2bb29-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="2bb29-141">Ak tak chcete urobiť, prejdite na **Zdroje** \> **Zdrojové roly**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="2bb29-142">Okrem toho musí byť priradená predvolená rola pre každý rezervovateľný prostriedok.</span><span class="sxs-lookup"><span data-stu-id="2bb29-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="2bb29-143">Prejdite do **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="2bb29-144">Na karte **Project Service** skontrolujte, či je definovaná rola prostriedku a že pole **Je predvolená** je nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="2bb29-145">Môžete pridať ďalšie roly, kde **Je predvolená = nie**.</span><span class="sxs-lookup"><span data-stu-id="2bb29-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="2bb29-146">Úloha, kde **Je predvolená = Áno** sa používa na vyhodnotenie využitia prostriedku proti cieľu pre túto rolu.</span><span class="sxs-lookup"><span data-stu-id="2bb29-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="2bb29-147">Na karte **Project Service** môžete tiež nastaviť individuálne cieľové využitie prostriedku.</span><span class="sxs-lookup"><span data-stu-id="2bb29-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="2bb29-148">Výpočet využitia potom použije cieľové využitie na vyhodnotenie cieľového prostriedku namiesto cieľa predvolenej roly prostriedku.</span><span class="sxs-lookup"><span data-stu-id="2bb29-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="2bb29-149">Využitie sa zobrazuje pre zdroj len vtedy, ak tento prostriedok schválil účtovateľný čas počas obdobia, ktoré je zobrazené v mriežke.</span><span class="sxs-lookup"><span data-stu-id="2bb29-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="2bb29-150">Dostupnosť zdroja</span><span class="sxs-lookup"><span data-stu-id="2bb29-150">Resource availability</span></span>

<span data-ttu-id="2bb29-151">Je dôležité, aby správcovia zdrojov mohli zobraziť dostupnosť zdrojov a aktualizovať rezervácie.</span><span class="sxs-lookup"><span data-stu-id="2bb29-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="2bb29-152">V niektorých prípadoch neexistuje žiadny formálny dopyt (požiadavka na zdroje), ale správca prostriedkov musí reagovať na neplánovaný dopyt, ktorý sa dodáva prostredníctvom kanálov, ako je e-mail, telefonát alebo okamžitá správa.</span><span class="sxs-lookup"><span data-stu-id="2bb29-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="2bb29-153">Správcovia zdrojov používajú tabule plánovania na aktualizáciu zdrojov a rezervácií.</span><span class="sxs-lookup"><span data-stu-id="2bb29-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="2bb29-154">Pracovné hodiny prostriedkov sa používajú ako základ pre výpočet dostupnosti prostriedku.</span><span class="sxs-lookup"><span data-stu-id="2bb29-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="2bb29-155">Rezervácie zdrojov spotrebúvajú kapacitu zdrojov.</span><span class="sxs-lookup"><span data-stu-id="2bb29-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="2bb29-156">Tabule plánovania používajú farby a tieňovanie na zobrazovanie rezervácií, dostupnosti a nadmernej rezervácie, ako aj stav rezervácií.</span><span class="sxs-lookup"><span data-stu-id="2bb29-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="2bb29-157">Nastavenie v nastaveniach tabule plánovania vám umožňuje zobraziť legendu.</span><span class="sxs-lookup"><span data-stu-id="2bb29-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="2bb29-158">Ak sa vedľa individuálneho rezervovateľného prostriedku na tabuli plánovania zobrazí šípka ukazujúca vpravo, zdroj možno rozbaliť a zobraziť podrobnosti o práci, na ktorej je zdroj rezervovaný.</span><span class="sxs-lookup"><span data-stu-id="2bb29-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="2bb29-159">Pretože Dynamics 365 Project Operations používa systém Universal Resource Scheduling, ak ste nainštalovali aj Dynamics 365 Field Service, môžete zobraziť podrobnosti o rezerváciách zdrojov pre projekty, objednávky prác a všetky ostatné entity, na ktoré ste rozšírili plánovanie.</span><span class="sxs-lookup"><span data-stu-id="2bb29-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="2bb29-160">Ak chcete zobraziť ďalšie podrobnosti o jednotlivých prostriedkoch, kliknite naň pravým tlačidlom a otvorte kartu zdroja.</span><span class="sxs-lookup"><span data-stu-id="2bb29-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

