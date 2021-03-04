---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 28, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 28, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150642"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="d3c41-103">Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 28, V3</span><span class="sxs-lookup"><span data-stu-id="d3c41-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d3c41-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d3c41-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d3c41-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="d3c41-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="d3c41-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d3c41-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d3c41-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="d3c41-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="d3c41-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d3c41-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d3c41-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre Project Service Automation V3, aktualizované vydanie 28. Táto verzia má číslo zostavenia V3.10.46.32 a je všeobecne dostupná prostredníctvom automatickej aktualizácie v januári 2021.</span><span class="sxs-lookup"><span data-stu-id="d3c41-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="d3c41-110">Aktualizácia vydania 28</span><span class="sxs-lookup"><span data-stu-id="d3c41-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d3c41-111">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="d3c41-111">Bug fixes</span></span>

<span data-ttu-id="d3c41-112">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="d3c41-112">**Time and Expense**</span></span>

<span data-ttu-id="d3c41-113">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="d3c41-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="d3c41-114">Používatelia môžu používať **Hromadné úpravy** na aktualizovanie časových zadaní, ktoré boli schválené a odoslané.</span><span class="sxs-lookup"><span data-stu-id="d3c41-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="d3c41-115">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="d3c41-115">**Project Management**</span></span>

<span data-ttu-id="d3c41-116">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="d3c41-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="d3c41-117">V prípadoch, keď sa identifikátor GUID úlohy interpretuje ako číslo, úlohy nemožno otvoriť na úpravu pomocou možnosti **Upraviť úlohu** v páse s nástrojmi na stránke **Štruktúra rozdelenia práce**.</span><span class="sxs-lookup"><span data-stu-id="d3c41-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="d3c41-118">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d3c41-118">**Sales**</span></span>

<span data-ttu-id="d3c41-119">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="d3c41-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="d3c41-120">Nulová referenčná výnimka sa vygeneruje, keď je vyvolaný doplnok **GetEstimatesForProject**.</span><span class="sxs-lookup"><span data-stu-id="d3c41-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="d3c41-121">**Značka je pripravená na fakturáciu** v mriežke medzníkov aktualizuje atribúty iba čiastočne, s výnimkou atribútu **InvoiceStatus**, ktorý sa aktualizuje.</span><span class="sxs-lookup"><span data-stu-id="d3c41-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

