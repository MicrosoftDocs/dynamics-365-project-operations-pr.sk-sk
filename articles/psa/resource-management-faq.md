---
title: Časté otázky pre správu zdrojov
description: Táto téma obsahuje odpovede na často kladené otázky týkajúce sa správy zdrojov.
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
ms.openlocfilehash: 38d9509768323a5a1d78683a2e65ade241adc65f
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120157"
---
# <a name="resource-management-faq"></a><span data-ttu-id="52837-103">Časté otázky pre správu zdrojov</span><span class="sxs-lookup"><span data-stu-id="52837-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="52837-104">Aký je rozdiel medzi členom tímu a požiadavkou na zdroje?</span><span class="sxs-lookup"><span data-stu-id="52837-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="52837-105">Člen projektového tímu môže byť priradený k úlohám, môže byť rezervovaný alebo prerezervovaný a nastavený ako schvaľovateľ.</span><span class="sxs-lookup"><span data-stu-id="52837-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="52837-106">Požiadavka na zdroje môže existovať bez člena projektového tímu, ako koncept poznámky o dopyte.</span><span class="sxs-lookup"><span data-stu-id="52837-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="52837-107">Aký je rozdiel medzi navrhnutými a predbežne rezervovanými hodinami?</span><span class="sxs-lookup"><span data-stu-id="52837-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="52837-108">Navrhované hodiny a predbežne rezervované hodiny sa líšia vo viditeľnosti.</span><span class="sxs-lookup"><span data-stu-id="52837-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="52837-109">Navrhované hodiny sú viditeľné len pre správcov zdrojov a projektového manažéra, ktorý inicioval dopyt pomocou požiadavky na zdroje.</span><span class="sxs-lookup"><span data-stu-id="52837-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="52837-110">Predbežne rezervované hodiny sú viditeľné pre každého, kto má prístup k tabuli plánovania.</span><span class="sxs-lookup"><span data-stu-id="52837-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="52837-111">Ako môžem zobraziť predbežne rezervované hodiny pre zdroje v tíme?</span><span class="sxs-lookup"><span data-stu-id="52837-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="52837-112">Predbežné rezervácie možno uskutočniť pri rezervácii požiadavky o zdroj.</span><span class="sxs-lookup"><span data-stu-id="52837-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="52837-113">Zdroje, ktoré sú predbežne rezervované v projektovom tíme, sa zobrazujú ako členovia tímu, ktorí majú predbežne rezervované hodiny.</span><span class="sxs-lookup"><span data-stu-id="52837-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="52837-114">Zobrazia sa tiež na tabuli plánu.</span><span class="sxs-lookup"><span data-stu-id="52837-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="52837-115">Ako zmením požadované hodiny a počiatočný a koncový dátum pre zdroj (všeobecný alebo pomenovaný), ktorý som rezervoval?</span><span class="sxs-lookup"><span data-stu-id="52837-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="52837-116">Po rezerváciách zdrojov vyberte položku **Spravovanie rezervácií**, aby ste mohli vykonať požadované zmeny.</span><span class="sxs-lookup"><span data-stu-id="52837-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="52837-117">Aké typy prostriedkov podporuje Project Service Automation?</span><span class="sxs-lookup"><span data-stu-id="52837-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="52837-118">**Používateľ** a **Kontakt** sú jedinými typmi prostriedkov, ktoré sú podporované v Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="52837-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="52837-119">Aj keď môžete vytvoriť iné typy zdrojov (napríklad **Zariadenie** a **Skupina**), nie je pre nich podporovaný žiadny prípad použitia end-to-end.</span><span class="sxs-lookup"><span data-stu-id="52837-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="52837-120">Aký je rozdiel medzi priradením a rezerváciou?</span><span class="sxs-lookup"><span data-stu-id="52837-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="52837-121">Priradenia sú priraďovanie zdrojov k projektovým úlohám v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="52837-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="52837-122">Zdroje môžu byť buď skutočnými, alebo všeobecnými zdrojmi.</span><span class="sxs-lookup"><span data-stu-id="52837-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="52837-123">Rezervácie sú pevné alebo predbežné alokácie zdrojov k projektu.</span><span class="sxs-lookup"><span data-stu-id="52837-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="52837-124">Pevné rezervácie spotrebúvajú kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="52837-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="52837-125">V ideálnom prípade sa pri reálnych zdrojoch musia rezervácie a priradenia zhodnúť, pretože sa nelíšia.</span><span class="sxs-lookup"><span data-stu-id="52837-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="52837-126">Avšak, PSA nepresadzuje túto zmluvu.</span><span class="sxs-lookup"><span data-stu-id="52837-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="52837-127">V zobrazení Vyrovnanie sa zobrazuje projektový manažér, v ktorom nesúhlasia rezervácie a priradenia.</span><span class="sxs-lookup"><span data-stu-id="52837-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>