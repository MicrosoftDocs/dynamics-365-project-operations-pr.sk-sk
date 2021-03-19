---
title: Navrhnite projektové zdroje
description: Táto téma poskytuje informácie o tom, ako navrhovať projektové zdroje.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 2003f6f06912b0c47eb942aae17e509b00e19487
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283027"
---
# <a name="propose-project-resources"></a><span data-ttu-id="4f76c-103">Navrhnite projektové zdroje</span><span class="sxs-lookup"><span data-stu-id="4f76c-103">Propose project resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4f76c-104">Správcovia zdrojov môžu navrhnúť zdroj projektového manažéra pomocou požiadavky prostriedku.</span><span class="sxs-lookup"><span data-stu-id="4f76c-104">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="4f76c-105">V mriežke požiadavky alebo samotnej žiadosti vyberte položku **Vyhľadať zdroje**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-105">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="4f76c-106">Na stránke **Asistent plánovania** vyberte zdroj a potom v table stav **Vytvoriť rezerváciu zdroja** v poli **Stav rezervácie** zvoľte možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-106">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

    ![Vybratý navrhovaný zdroj](media/Resource-Management-image62.png)

<span data-ttu-id="4f76c-108">Nasledujúce aktualizácie stavu sa vyskytujú:</span><span class="sxs-lookup"><span data-stu-id="4f76c-108">The following status updates occur:</span></span>

- <span data-ttu-id="4f76c-109">Na stránke **Asistent plánovania** sa aktualizujú indikátory stavu, ktoré naznačujú, že rezervácia je navrhnutá a nie je pevne rezervovaná.</span><span class="sxs-lookup"><span data-stu-id="4f76c-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>

    ![Indikátory stavu navrhovanej rezervácie na stránke Asistenta plánovania](media/Resource-Management-image63.png)

- <span data-ttu-id="4f76c-111">Na žiadosť o prostriedok, stav sa zmení na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-111">On the resource request, the status is changed to **Needs Review**.</span></span>

    ![Stav požiadavky na zdroj sa zmenil na Vyžaduje kontrolu](media/Resource-Management-image64.png)

- <span data-ttu-id="4f76c-113">Na karte **Tím** projektu sa hodnota všeobecných členov tímu **Stav žiadosti** zmenila na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-113">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

    ![Stav žiadosti všeobecného člena tímu sa zmenila na karte Tím na Vyžaduje kontrolu](media/Resource-Management-image48.png)

<span data-ttu-id="4f76c-115">Projektový manažér môže buď prijať, alebo zamietnuť návrh.</span><span class="sxs-lookup"><span data-stu-id="4f76c-115">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="4f76c-116">Keď správcovia zdrojov spracúvajú žiadosti o prostriedky, môžu použiť ktorýkoľvek z nasledujúcich prístupov:</span><span class="sxs-lookup"><span data-stu-id="4f76c-116">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="4f76c-117">Navrhnite viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na splnenie požadovaných hodín.</span><span class="sxs-lookup"><span data-stu-id="4f76c-117">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="4f76c-118">Navrhované hodiny sa potom rozdelia medzi viaceré zdroje, ktoré môžu uspokojiť požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="4f76c-118">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="4f76c-119">V tomto scenári, hodiny nemožno prekrývať.</span><span class="sxs-lookup"><span data-stu-id="4f76c-119">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="4f76c-120">Navrhnite menej zdrojov, než je požadované.</span><span class="sxs-lookup"><span data-stu-id="4f76c-120">Propose fewer resources than are required.</span></span> <span data-ttu-id="4f76c-121">V tomto scenári, navrhovaná kapacita prostriedku je menšia ako požadované hodiny, ktoré žiadateľ zadal.</span><span class="sxs-lookup"><span data-stu-id="4f76c-121">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="4f76c-122">Preto, keď žiadateľ akceptuje navrhované prostriedky, nesplnených zdrojov požiadavka je vytvorená na zachytenie zostávajúcich požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="4f76c-122">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="4f76c-123">Zarezervujte viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na dokončenie prác.</span><span class="sxs-lookup"><span data-stu-id="4f76c-123">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="4f76c-124">Rezervujte menej zdrojov, než je požadované.</span><span class="sxs-lookup"><span data-stu-id="4f76c-124">Book fewer resources than are required.</span></span> <span data-ttu-id="4f76c-125">V tomto scenári, rezervované hodiny sú menej ako požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="4f76c-125">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="4f76c-126">Systém vás prevedie navrhnutie zdrojov namiesto rezervácií, aby žiadateľa mohol overiť a sledovať zostávajúci dopyt.</span><span class="sxs-lookup"><span data-stu-id="4f76c-126">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="4f76c-127">Fakturovateľné využitie</span><span class="sxs-lookup"><span data-stu-id="4f76c-127">Billable utilization</span></span>

<span data-ttu-id="4f76c-128">Zdroje môžu mať cieľové fakturovateľné využitie.</span><span class="sxs-lookup"><span data-stu-id="4f76c-128">Resources can have a target billable utilization.</span></span> <span data-ttu-id="4f76c-129">Tento cieľ využitia je buď definovaný ako atribút na zdroja predvolenú rolu, alebo nastavenie na záznam jednotlivých rezervovateľných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="4f76c-129">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="4f76c-130">Výpočty využitia sú založené na skutočných hodinách, ktoré zdroje hlásili pomocou schválených časových položiek.</span><span class="sxs-lookup"><span data-stu-id="4f76c-130">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="4f76c-131">Na výpočet využitia sa používajú nasledujúce vzorce:</span><span class="sxs-lookup"><span data-stu-id="4f76c-131">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="4f76c-132">Fakturovateľné využitie = Spoplatnená skutočná kapacita hodín ÷ kapacita zdroja</span><span class="sxs-lookup"><span data-stu-id="4f76c-132">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="4f76c-133">Nefakturovateľné využitie = skutočný čas s fakturáciou typu ID = Nefakturovateľné, doplnkové alebo nie je k dispozícii ÷ zdroj kapacity</span><span class="sxs-lookup"><span data-stu-id="4f76c-133">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="4f76c-134">Interné = skutočný čas bez predajnej zmluvy ÷ kapacita zdrojov</span><span class="sxs-lookup"><span data-stu-id="4f76c-134">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="4f76c-135">Kapacita zdrojov = pracovné hodiny zdroja – mimo pracoviska – dni pracovného času</span><span class="sxs-lookup"><span data-stu-id="4f76c-135">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="4f76c-136">**Zobrazenie využitia** prostriedkov môžete nájsť na table **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-136">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

![Zobrazenie využitia zdrojov](media/Resource-Management-image65.png)

<span data-ttu-id="4f76c-138">Každá bunka v mriežke predstavuje percento fakturovateľného využitia prostriedku v období, ako je napríklad deň, týždeň alebo mesiac.</span><span class="sxs-lookup"><span data-stu-id="4f76c-138">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="4f76c-139">Na vyfarbenie buniek sa používajú nasledujúce vzorce:</span><span class="sxs-lookup"><span data-stu-id="4f76c-139">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="4f76c-140">**Zelená:** Fakturovateľné využitie \>= Cieľové využitie zdroja</span><span class="sxs-lookup"><span data-stu-id="4f76c-140">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="4f76c-141">**Žltá:** Cieľové využitie – 20 \<Fakturovateľná využitie \< Cieľové využitie</span><span class="sxs-lookup"><span data-stu-id="4f76c-141">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="4f76c-142">**Červená:** Fakturovateľná využitie \< Cieľové využitie – 20</span><span class="sxs-lookup"><span data-stu-id="4f76c-142">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="4f76c-143">Keďže zobrazenie **Využitie zdroja** je založené na tabuli plánovania, môžete filtrovať výsledky pomocou možností filtrovania tabule plánovania.</span><span class="sxs-lookup"><span data-stu-id="4f76c-143">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="4f76c-144">Mriežka si vyžaduje, aby ste stanovili cieľové využitie buď roly, alebo individuálneho zdroja.</span><span class="sxs-lookup"><span data-stu-id="4f76c-144">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="4f76c-145">Ak tak chcete urobiť, prejdite na **Zdroje** \> **Zdrojové roly**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-145">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="4f76c-146">Okrem toho musí byť priradená predvolená rola pre každý rezervovateľný prostriedok.</span><span class="sxs-lookup"><span data-stu-id="4f76c-146">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="4f76c-147">Prejdite do **Zdroje** \> **Zdroje**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-147">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="4f76c-148">Na karte **Project Service** skontrolujte, či je definovaná rola prostriedku a že pole **Je predvolená** je nastavené na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-148">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="4f76c-149">Môžete pridať ďalšie roly, kde **Je predvolená = nie**.</span><span class="sxs-lookup"><span data-stu-id="4f76c-149">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="4f76c-150">Úloha, kde **Je predvolená = Áno** sa používa na vyhodnotenie využitia prostriedku proti cieľu pre túto rolu.</span><span class="sxs-lookup"><span data-stu-id="4f76c-150">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

![Súbor predvolenej roly](media/Resource-Management-image67.png)

<span data-ttu-id="4f76c-152">Na karte **Project Service** môžete tiež nastaviť individuálne cieľové využitie prostriedku.</span><span class="sxs-lookup"><span data-stu-id="4f76c-152">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="4f76c-153">Výpočet využitia potom použije cieľové využitie na vyhodnotenie cieľového prostriedku namiesto cieľa predvolenej roly prostriedku.</span><span class="sxs-lookup"><span data-stu-id="4f76c-153">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="4f76c-154">Využitie sa zobrazuje pre zdroj len vtedy, ak tento prostriedok schválil účtovateľný čas počas obdobia, ktoré je zobrazené v mriežke.</span><span class="sxs-lookup"><span data-stu-id="4f76c-154">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="4f76c-155">Dostupnosť zdroja</span><span class="sxs-lookup"><span data-stu-id="4f76c-155">Resource availability</span></span>

<span data-ttu-id="4f76c-156">Je dôležité, aby správcovia zdrojov mohli zobraziť dostupnosť zdrojov a aktualizovať rezervácie.</span><span class="sxs-lookup"><span data-stu-id="4f76c-156">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="4f76c-157">V niektorých prípadoch neexistuje žiadny formálny dopyt (požiadavka na zdroje), ale správca prostriedkov musí reagovať na neplánovaný dopyt, ktorý sa dodáva prostredníctvom kanálov, ako je e-mail, telefonát alebo okamžitá správa.</span><span class="sxs-lookup"><span data-stu-id="4f76c-157">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="4f76c-158">Správcovia zdrojov používajú tabule plánovania na aktualizáciu zdrojov a rezervácií.</span><span class="sxs-lookup"><span data-stu-id="4f76c-158">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="4f76c-159">Pracovné hodiny prostriedkov sa používajú ako základ pre výpočet dostupnosti prostriedku.</span><span class="sxs-lookup"><span data-stu-id="4f76c-159">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="4f76c-160">Rezervácie zdrojov spotrebúvajú kapacitu zdrojov.</span><span class="sxs-lookup"><span data-stu-id="4f76c-160">Resource bookings consume the capacity of the resources.</span></span>

![Tabuľa plánovania](media/Resource-Management-image68.png)

<span data-ttu-id="4f76c-162">Tabule plánovania používajú farby a tieňovanie na zobrazovanie rezervácií, dostupnosti a nadmernej rezervácie, ako aj stav rezervácií.</span><span class="sxs-lookup"><span data-stu-id="4f76c-162">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="4f76c-163">Nastavenie v nastaveniach tabule plánovania vám umožňuje zobraziť legendu.</span><span class="sxs-lookup"><span data-stu-id="4f76c-163">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="4f76c-164">Ak sa vedľa individuálneho rezervovateľného prostriedku na tabuli plánovania zobrazí šípka ukazujúca vpravo, zdroj možno rozbaliť a zobraziť podrobnosti o práci, na ktorej je zdroj rezervovaný.</span><span class="sxs-lookup"><span data-stu-id="4f76c-164">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

![Rezervovateľný zdroj rozbalený na tabuli plánovania](media/Resource-Management-image69.png)

<span data-ttu-id="4f76c-166">Pretože Dynamics 365 Project Service Automation používa systém Universal Resource Scheduling, ak ste tiež Dynamics 365 Field Service nainštalovali, môžete zobraziť podrobnosti o rezerváciách zdrojov pre projekty, pracovné objednávky a všetky ostatné entity, na ktoré ste rozšírili plánovanie.</span><span class="sxs-lookup"><span data-stu-id="4f76c-166">Because Dynamics 365 Project Service Automation uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

![Podrobnosti o rezerváciách zdrojov pre projekty a pracovné objednávky](media/Resource-Management-image70.png)

<span data-ttu-id="4f76c-168">Ak chcete zobraziť ďalšie podrobnosti o jednotlivých prostriedkoch, kliknite naň pravým tlačidlom a otvorte kartu zdroja.</span><span class="sxs-lookup"><span data-stu-id="4f76c-168">To view more details about an individual resource, right-click it to open the resource card.</span></span>

![Karta zdroja](media/Resource-Management-image71.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]