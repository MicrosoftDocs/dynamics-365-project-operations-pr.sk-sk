---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 30, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 30, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 1169ee13c42e982cb30a40d92df660f8933786a9
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852893"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="ce54a-103">Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 30, V3</span><span class="sxs-lookup"><span data-stu-id="ce54a-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="ce54a-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="ce54a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="ce54a-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="ce54a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="ce54a-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="ce54a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="ce54a-107">Ak chcete aktualizovať toto vydanie, navštívte stránku online riešení v centre spravovania služby Dynamics 365 a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="ce54a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="ce54a-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="ce54a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="ce54a-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 30.</span><span class="sxs-lookup"><span data-stu-id="ce54a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="ce54a-110">Táto verzia má číslo V3.10.51.61 a v apríli 2021 je všeobecne k dispozícii prostredníctvom automatickej aktualizácie.</span><span class="sxs-lookup"><span data-stu-id="ce54a-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="ce54a-111">Aktualizácia vydania 30</span><span class="sxs-lookup"><span data-stu-id="ce54a-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="ce54a-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="ce54a-112">Bug fixes</span></span>

<span data-ttu-id="ce54a-113">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="ce54a-113">**Time and Expense**</span></span>

<span data-ttu-id="ce54a-114">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="ce54a-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="ce54a-115">Pri vytváraní a ukladaní záznamu času na stránke **Rýchle vytvorenie**, ak je odstránené pole **Rola**, sa vyskytne chyba.</span><span class="sxs-lookup"><span data-stu-id="ce54a-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="ce54a-116">Filter zadania času použije nesprávny operátor filtra.</span><span class="sxs-lookup"><span data-stu-id="ce54a-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="ce54a-117">Po výbere možnosti **Kopírovať týždeň** na ovládacom prvku zadania času sa skopírované časové rozvrhy nezobrazia automaticky.</span><span class="sxs-lookup"><span data-stu-id="ce54a-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="ce54a-118">**Správa zdrojov**</span><span class="sxs-lookup"><span data-stu-id="ce54a-118">**Resource Management**</span></span>

<span data-ttu-id="ce54a-119">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="ce54a-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="ce54a-120">Po predĺžení rezervácie je stav rezervácie priradený k tvrdej rezervácii nesprávny.</span><span class="sxs-lookup"><span data-stu-id="ce54a-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="ce54a-121">Predĺženie rezervácie rešpektuje stav rezervácie definovaný ako **Pridelený** v metadátach nastavenia rezervácie.</span><span class="sxs-lookup"><span data-stu-id="ce54a-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="ce54a-122">Ak nie je zadaný platný stav rezervácie, chybové hlásenie nie je správne lokalizované.</span><span class="sxs-lookup"><span data-stu-id="ce54a-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="ce54a-123">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="ce54a-123">**Project Management**</span></span>

<span data-ttu-id="ce54a-124">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="ce54a-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="ce54a-125">Projekty nemožno vytvoriť v jednej mene a zahrnúť súvisiace úlohy v inej mene.</span><span class="sxs-lookup"><span data-stu-id="ce54a-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="ce54a-126">**Predaj**</span><span class="sxs-lookup"><span data-stu-id="ce54a-126">**Sales**</span></span>

<span data-ttu-id="ce54a-127">Vyriešili sa tieto problémy:</span><span class="sxs-lookup"><span data-stu-id="ce54a-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="ce54a-128">Po skopírovaní cenníka sa ceny neaktualizujú.</span><span class="sxs-lookup"><span data-stu-id="ce54a-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="ce54a-129">Uzavretie cenovej ponuky ako získanej sa nepodarí, ak má detail ceny pôvodnú hodnotu.</span><span class="sxs-lookup"><span data-stu-id="ce54a-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="ce54a-130">V entite **Projektová úloha** bola položka **Odhadovaný náklad** premenovaná na **Plánovaný náklad (základný)**.</span><span class="sxs-lookup"><span data-stu-id="ce54a-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="ce54a-131">Pri vytváraní alebo mazaní faktúr sa generuje výnimka odkazu na hodnotu null.</span><span class="sxs-lookup"><span data-stu-id="ce54a-131">A null reference exception is generated when invoices are created or deleted.</span></span>
