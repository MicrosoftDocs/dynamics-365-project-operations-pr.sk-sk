---
title: Rezervácie verzus priradenia
description: Táto téma poskytuje informácie o rozdieloch medzi rezerváciami zdrojov a priradeniami zdrojov.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130237"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="624e0-103">Rezervácie verzus priradenia</span><span class="sxs-lookup"><span data-stu-id="624e0-103">Bookings vs assignments</span></span>

<span data-ttu-id="624e0-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="624e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="624e0-105">Rezervácie sú pevné alebo predbežné alokácie zdrojov k projektu.</span><span class="sxs-lookup"><span data-stu-id="624e0-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="624e0-106">Pevné rezervácie spotrebúvajú kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="624e0-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="624e0-107">Rezervácie predstavujú organizačné koncepty pre tímy, aby mohli pochopiť, ako sa budú využívať zdroje v rôznych projektoch.</span><span class="sxs-lookup"><span data-stu-id="624e0-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="624e0-108">Dynamics 365 Project Operations považuje rezervácie za koncept na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="624e0-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="624e0-109">Na rozdiel od rezervácií sú priradenia sú priraďovaním zdrojov k projektovým úlohám v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="624e0-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="624e0-110">Zdroje môžu byť pomenované alebo všeobecné.</span><span class="sxs-lookup"><span data-stu-id="624e0-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="624e0-111">Súčet rezervácií zdroja sa zvyčajne bude rovnať súčtu priradení zdroja k jednej alebo viacerým úlohám.</span><span class="sxs-lookup"><span data-stu-id="624e0-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="624e0-112">Project Operations však nepresadzuje túto zmluvu.</span><span class="sxs-lookup"><span data-stu-id="624e0-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="624e0-113">V zobrazení **Vyrovnanie** zobrazuje Projektový manažér miesta, kde nesúhlasia rezervácie a priradenia.</span><span class="sxs-lookup"><span data-stu-id="624e0-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
