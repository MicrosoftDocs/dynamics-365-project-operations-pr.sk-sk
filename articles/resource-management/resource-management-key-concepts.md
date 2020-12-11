---
title: Kľúčové koncepty riadenia zdrojov
description: Táto téma poskytuje informácie o možnostiach správy zdrojov v Microsoft Dynamics Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: a14f0ec328049d1b199201955c384df9fac61e39
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123892"
---
# <a name="resource-management-key-concepts"></a><span data-ttu-id="065cf-103">Kľúčové koncepty riadenia zdrojov</span><span class="sxs-lookup"><span data-stu-id="065cf-103">Resource management key concepts</span></span>

<span data-ttu-id="065cf-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="065cf-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="065cf-105">Zdroje sú najdôležitejším prínosom organizácie založenej na službe.</span><span class="sxs-lookup"><span data-stu-id="065cf-105">Resources are the most important asset of a service-based organization.</span></span> <span data-ttu-id="065cf-106">Schopnosť nájsť správne zdroje v pravý čas, rezervovať tieto zdroje na projektoch, a udržať zdroje využité pomáha organizácii splniť ciele príjmov a spokojnosť zákazníkov.</span><span class="sxs-lookup"><span data-stu-id="065cf-106">The ability to find the right resources at the right time, book those resources on projects and keep them utilized, helps the organization meet revenue targets and customer satisfaction goals.</span></span> <span data-ttu-id="065cf-107">Môžete použiť funkciu zdroja projektu v Dynamics 365 Project Operations a vykonať nasledovné úlohy:</span><span class="sxs-lookup"><span data-stu-id="065cf-107">You can use the project resourcing functionality in Dynamics 365 Project Operations to do the following tasks:</span></span>

- <span data-ttu-id="065cf-108">Vytvárať projektové tímy podľa dostupnej rezervácie a kvalifikovaných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="065cf-108">Form project teams by booking available and qualified resources.</span></span>
- <span data-ttu-id="065cf-109">Vytvárať záznamy všeobecných členov tímu a definovať ich roly a zdrojovú organizačnú jednotku.</span><span class="sxs-lookup"><span data-stu-id="065cf-109">Create generic team member records and define their roles and resource organization unit.</span></span>
- <span data-ttu-id="065cf-110">Generovať požiadavky na zdroje pre všeobecných členov tímu z ich priradenia úloh.</span><span class="sxs-lookup"><span data-stu-id="065cf-110">Generate resource requirements for generic team members from their task assignments.</span></span>
- <span data-ttu-id="065cf-111">Priraďovať zručnosti identifikáciou zručností definovaných v zdrojovej požiadavke v porovnaní s dostupnými zručnosťami zdroja.</span><span class="sxs-lookup"><span data-stu-id="065cf-111">Match skills by identifying the skills defined on the resource demand against available resource skills.</span></span>
- <span data-ttu-id="065cf-112">Nahraďte zdroje.</span><span class="sxs-lookup"><span data-stu-id="065cf-112">Substitute resources.</span></span>
- <span data-ttu-id="065cf-113">Zarovnať priradenia projektového plánovania a rezervácií zdroja.</span><span class="sxs-lookup"><span data-stu-id="065cf-113">Align project schedule assignments and resource bookings.</span></span>
- <span data-ttu-id="065cf-114">Zosúladiť rozdiely v rezerváciách a úlohách.</span><span class="sxs-lookup"><span data-stu-id="065cf-114">Reconcile differences in bookings and assignments.</span></span>
- <span data-ttu-id="065cf-115">Zmena rezervácie zdrojov v reakcii na stav mimo pracoviska.</span><span class="sxs-lookup"><span data-stu-id="065cf-115">Change resource bookings in response to out-of-office status.</span></span>
- <span data-ttu-id="065cf-116">Spolupracujte medzi projektovými manažérmi a manažérmi zdrojov.</span><span class="sxs-lookup"><span data-stu-id="065cf-116">Collaborate between project managers and resource managers.</span></span>
- <span data-ttu-id="065cf-117">Zobraziť históriu využitia zdrojov proti cieľu, vrátane rozdelenia toho, ako sa využíval čas zdrojov.</span><span class="sxs-lookup"><span data-stu-id="065cf-117">View the history of resource utilization against a target, including a breakdown of how the resources' time was utilized.</span></span>
- <span data-ttu-id="065cf-118">Zabezpečenie zručností a odbornej spôsobilosti.</span><span class="sxs-lookup"><span data-stu-id="065cf-118">Maintain a skills and proficiency repository.</span></span>


<span data-ttu-id="065cf-119">Zamestnancom vášho projektu môžete poskytnúť všeobecný tím alebo vymenované zdroje v Project Operations.</span><span class="sxs-lookup"><span data-stu-id="065cf-119">You can staff your project with a team of generic or named resources in Project Operations.</span></span> <span data-ttu-id="065cf-120">Môžete použiť rôzne metódy na pridávanie a priraďovanie členov tímu a spravovanie ich rezervácií a priradení.</span><span class="sxs-lookup"><span data-stu-id="065cf-120">You can use various methods to add and assign team members and to manage their bookings and assignments.</span></span> 