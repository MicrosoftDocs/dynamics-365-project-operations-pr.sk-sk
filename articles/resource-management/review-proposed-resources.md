---
title: Kontrola navrhovaných zdrojov
description: Táto téma poskytuje informácie o tom, ako navrhovať projektové zdroje.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401192"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="6de77-103">Kontrola navrhovaných zdrojov</span><span class="sxs-lookup"><span data-stu-id="6de77-103">Review proposed resources</span></span>

<span data-ttu-id="6de77-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="6de77-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6de77-105">Správcovia zdrojov môžu navrhnúť zdroj projektového manažéra pomocou požiadavky prostriedku.</span><span class="sxs-lookup"><span data-stu-id="6de77-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="6de77-106">V mriežke požiadavky alebo samotnej žiadosti vyberte položku **Vyhľadať zdroje**.</span><span class="sxs-lookup"><span data-stu-id="6de77-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="6de77-107">Na stránke **Asistent plánovania** vyberte zdroj a potom v table stav **Vytvoriť rezerváciu zdroja** v poli **Stav rezervácie** zvoľte možnosť **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="6de77-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="6de77-108">Nasledujúce aktualizácie stavu sa vyskytujú:</span><span class="sxs-lookup"><span data-stu-id="6de77-108">The following status updates occur:</span></span>

- <span data-ttu-id="6de77-109">Na stránke **Asistent plánovania** sa aktualizujú indikátory stavu, ktoré naznačujú, že rezervácia je navrhnutá a nie je pevne rezervovaná.</span><span class="sxs-lookup"><span data-stu-id="6de77-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="6de77-110">Na žiadosť o prostriedok, stav sa zmení na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="6de77-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="6de77-111">Na karte **Tím** projektu sa hodnota všeobecných členov tímu **Stav žiadosti** zmenila na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="6de77-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="6de77-112">Projektový manažér môže buď prijať, alebo zamietnuť návrh.</span><span class="sxs-lookup"><span data-stu-id="6de77-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="6de77-113">Keď správcovia zdrojov spracúvajú žiadosti o prostriedky, môžu použiť ktorýkoľvek z nasledujúcich prístupov:</span><span class="sxs-lookup"><span data-stu-id="6de77-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="6de77-114">Navrhnite viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na splnenie požadovaných hodín.</span><span class="sxs-lookup"><span data-stu-id="6de77-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="6de77-115">Navrhované hodiny sa potom rozdelia medzi viaceré zdroje, ktoré môžu uspokojiť požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="6de77-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="6de77-116">V tomto scenári, hodiny nemožno prekrývať.</span><span class="sxs-lookup"><span data-stu-id="6de77-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="6de77-117">Navrhnite menej zdrojov, než je požadované.</span><span class="sxs-lookup"><span data-stu-id="6de77-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="6de77-118">V tomto scenári, navrhovaná kapacita prostriedku je menšia ako požadované hodiny, ktoré žiadateľ zadal.</span><span class="sxs-lookup"><span data-stu-id="6de77-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="6de77-119">Preto, keď žiadateľ akceptuje navrhované prostriedky, nesplnených zdrojov požiadavka je vytvorená na zachytenie zostávajúcich požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="6de77-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="6de77-120">Zarezervujte viacero zdrojov na uspokojenie dopytu, ak nie je k dispozícii žiadny jediný prostriedok na dokončenie prác.</span><span class="sxs-lookup"><span data-stu-id="6de77-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="6de77-121">Rezervujte menej zdrojov, než je požadované.</span><span class="sxs-lookup"><span data-stu-id="6de77-121">Book fewer resources than are required.</span></span> <span data-ttu-id="6de77-122">V tomto scenári, rezervované hodiny sú menej ako požadované hodiny.</span><span class="sxs-lookup"><span data-stu-id="6de77-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="6de77-123">Systém vás prevedie navrhnutie zdrojov namiesto rezervácií, aby žiadateľa mohol overiť a sledovať zostávajúci dopyt.</span><span class="sxs-lookup"><span data-stu-id="6de77-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="6de77-124">Dostupnosť zdroja</span><span class="sxs-lookup"><span data-stu-id="6de77-124">Resource availability</span></span>

<span data-ttu-id="6de77-125">Je dôležité, aby správcovia zdrojov mohli zobraziť dostupnosť zdrojov a aktualizovať rezervácie.</span><span class="sxs-lookup"><span data-stu-id="6de77-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="6de77-126">V niektorých prípadoch neexistuje žiadny formálny dopyt (požiadavka na zdroje), ale správca prostriedkov musí reagovať na neplánovaný dopyt, ktorý sa dodáva prostredníctvom kanálov, ako je e-mail, telefonát alebo okamžitá správa.</span><span class="sxs-lookup"><span data-stu-id="6de77-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="6de77-127">Správcovia zdrojov používajú tabule plánovania na aktualizáciu zdrojov a rezervácií.</span><span class="sxs-lookup"><span data-stu-id="6de77-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="6de77-128">Pracovné hodiny prostriedkov sa používajú ako základ pre výpočet dostupnosti prostriedku.</span><span class="sxs-lookup"><span data-stu-id="6de77-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="6de77-129">Rezervácie zdrojov spotrebúvajú kapacitu zdrojov.</span><span class="sxs-lookup"><span data-stu-id="6de77-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="6de77-130">Tabule plánovania používajú farby a tieňovanie na zobrazovanie rezervácií, dostupnosti a nadmernej rezervácie, ako aj stav rezervácií.</span><span class="sxs-lookup"><span data-stu-id="6de77-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="6de77-131">Nastavenie v nastaveniach tabule plánovania vám umožňuje zobraziť legendu.</span><span class="sxs-lookup"><span data-stu-id="6de77-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="6de77-132">Ak sa vedľa individuálneho rezervovateľného prostriedku na tabuli plánovania zobrazí šípka ukazujúca vpravo, zdroj možno rozbaliť a zobraziť podrobnosti o práci, na ktorej je zdroj rezervovaný.</span><span class="sxs-lookup"><span data-stu-id="6de77-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="6de77-133">Pretože Dynamics 365 Project Operations používa systém Universal Resource Scheduling, ak ste nainštalovali aj Dynamics 365 Field Service, môžete zobraziť podrobnosti o rezerváciách zdrojov pre projekty, objednávky prác a všetky ostatné entity, na ktoré ste rozšírili plánovanie.</span><span class="sxs-lookup"><span data-stu-id="6de77-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="6de77-134">Ak chcete zobraziť ďalšie podrobnosti o jednotlivých prostriedkoch, kliknite naň pravým tlačidlom a otvorte kartu zdroja.</span><span class="sxs-lookup"><span data-stu-id="6de77-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

