---
title: Rezervácie verzus priradenia
description: Táto téma poskytuje informácie o rozdieloch medzi rezerváciami zdrojov a priradeniami zdrojov.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084213"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="205c8-103">Rezervácie verzus priradenia</span><span class="sxs-lookup"><span data-stu-id="205c8-103">Bookings vs assignments</span></span>

<span data-ttu-id="205c8-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="205c8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="205c8-105">Rezervácie sú pevné alebo predbežné alokácie zdrojov k projektu.</span><span class="sxs-lookup"><span data-stu-id="205c8-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="205c8-106">Pevné rezervácie spotrebúvajú kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="205c8-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="205c8-107">Priradenia sú priraďovanie zdrojov k projektovým úlohám v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="205c8-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="205c8-108">Zdroje môžu byť skutočné alebo všeobecné.</span><span class="sxs-lookup"><span data-stu-id="205c8-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="205c8-109">V ideálnom prípade sa pri reálnych zdrojoch musia rezervácie a priradenia zhodnúť, pretože sa nelíšia.</span><span class="sxs-lookup"><span data-stu-id="205c8-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="205c8-110">Microsoft Dynamics Project Operations však nepresadzuje túto zmluvu.</span><span class="sxs-lookup"><span data-stu-id="205c8-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="205c8-111">V zobrazení **Vyrovnanie** sa zobrazuje projektový manažér, v ktorom nesúhlasia rezervácie a priradenia.</span><span class="sxs-lookup"><span data-stu-id="205c8-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
