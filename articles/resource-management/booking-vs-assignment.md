---
title: Rezervácie verzus priradenia
description: Táto téma poskytuje informácie o rozdieloch medzi rezerváciami zdrojov a priradeniami zdrojov.
author: ruhercul
manager: Annbe
ms.date: 01/08/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 9e346766e6ccbb3dff59ef12072a1cd63f1e4231
ms.sourcegitcommit: 260ce052fed760bb44c514517806049ca13a5459
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 01/08/2021
ms.locfileid: "4841191"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="94e43-103">Rezervácie verzus priradenia</span><span class="sxs-lookup"><span data-stu-id="94e43-103">Bookings vs assignments</span></span>

<span data-ttu-id="94e43-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="94e43-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94e43-105">Rezervácie sú pevné alebo predbežné alokácie zdrojov k projektu.</span><span class="sxs-lookup"><span data-stu-id="94e43-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="94e43-106">Pevné rezervácie spotrebúvajú kapacitu zdroja.</span><span class="sxs-lookup"><span data-stu-id="94e43-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="94e43-107">Rezervácie predstavujú organizačné koncepty pre tímy, aby mohli pochopiť, ako sa budú využívať zdroje v rôznych projektoch.</span><span class="sxs-lookup"><span data-stu-id="94e43-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="94e43-108">Dynamics 365 Project Operations považuje rezervácie za koncept na úrovni projektu.</span><span class="sxs-lookup"><span data-stu-id="94e43-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="94e43-109">Na rozdiel od rezervácií sú priradenia sú priraďovaním zdrojov k projektovým úlohám v pláne projektu.</span><span class="sxs-lookup"><span data-stu-id="94e43-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="94e43-110">Zdroje môžu byť pomenované alebo všeobecné.</span><span class="sxs-lookup"><span data-stu-id="94e43-110">The resources can be named or generic.</span></span>  <span data-ttu-id="94e43-111">Keď sa požiadavka na zdroj odvodí z priradenia projektovej úlohy, aplikácia Project Operations použije kontúry úsilia priradenia zdrojov na vytvorenie kontúr detailov požiadavky na zdroje.</span><span class="sxs-lookup"><span data-stu-id="94e43-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="94e43-112">Odkaz na priradenie zdrojov sa však neudržiava.</span><span class="sxs-lookup"><span data-stu-id="94e43-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="94e43-113">Aktualizácie rezervácií odvodené z požiadavky na zdroje neaktualizujú žiadne priradenia zdrojov.</span><span class="sxs-lookup"><span data-stu-id="94e43-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="94e43-114">Súčet rezervácií zdroja sa zvyčajne bude rovnať súčtu priradení zdroja k jednej alebo viacerým úlohám.</span><span class="sxs-lookup"><span data-stu-id="94e43-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="94e43-115">Project Operations však nepresadzuje túto zmluvu.</span><span class="sxs-lookup"><span data-stu-id="94e43-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="94e43-116">V zobrazení **Vyrovnanie** zobrazuje Projektový manažér miesta, kde nesúhlasia rezervácie a priradenia.</span><span class="sxs-lookup"><span data-stu-id="94e43-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>


