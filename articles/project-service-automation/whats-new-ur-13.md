---
title: Čo je nové v aktualizácii Project Service Automation, vydanie 13, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 13, V3.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: c6f6a5b6-b5bb-467c-b7c7-7fb962504c6d
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5f1b6b3879c94a77ab62082aad1e470a3ba66552
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755585"
---
# <a name="project-service-automation-v3-update-release-13"></a><span data-ttu-id="089c8-103">Aktualizácia Project Service Automation V3, vydanie 13</span><span class="sxs-lookup"><span data-stu-id="089c8-103">Project Service Automation V3, Update Release 13</span></span>
<span data-ttu-id="089c8-104">S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="089c8-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="089c8-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="089c8-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="089c8-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="089c8-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="089c8-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="089c8-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="089c8-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="089c8-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="089c8-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 13.</span><span class="sxs-lookup"><span data-stu-id="089c8-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="089c8-110">Táto verzia má číslo zostavenia V3.10.3.18 a je k dispozícii v nasledujúcom harmonograme:</span><span class="sxs-lookup"><span data-stu-id="089c8-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="089c8-111">**Všeobecná dostupnosť (samoaktualizácia):** November 2019</span><span class="sxs-lookup"><span data-stu-id="089c8-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="089c8-112">**Automatická Aktualizácia** December 2019</span><span class="sxs-lookup"><span data-stu-id="089c8-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="089c8-113">Aktualizácia vydania 13</span><span class="sxs-lookup"><span data-stu-id="089c8-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="089c8-114">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="089c8-114">Bug fixes</span></span>

- <span data-ttu-id="089c8-115">Čas a výdavky</span><span class="sxs-lookup"><span data-stu-id="089c8-115">Time and Expense</span></span>

     - <span data-ttu-id="089c8-116">Oprava: Funkcie vyhľadávania na stránke **Schválenie výdavkov** nefungujú pri vyhľadávaní podľa účelu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="089c8-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="089c8-117">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="089c8-117">Resource Management</span></span>

     - <span data-ttu-id="089c8-118">Oprava: Čísla v odsúhlasení boli aktualizované, aby boli správne zarovnané.</span><span class="sxs-lookup"><span data-stu-id="089c8-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="089c8-119">Oprava: Pomenované zdroje nemôžu byť priradené k úlohám prostredníctvom karty **Plán**.</span><span class="sxs-lookup"><span data-stu-id="089c8-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="089c8-120">Riadenie projektov</span><span class="sxs-lookup"><span data-stu-id="089c8-120">Project Management</span></span>

     - <span data-ttu-id="089c8-121">Oprava: Nulová referenčná výnimka pri prideľovaní člena tímu, keď typu **TransactionType** chýbajú informácie o nastavení pre **Jednotka** a **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="089c8-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="089c8-122">Sales</span><span class="sxs-lookup"><span data-stu-id="089c8-122">Sales</span></span>

     - <span data-ttu-id="089c8-123">Oprava: Duplicitné záznamy typu transakcie vracajú chybu pri vytváraní záznamov o cenách rolí.</span><span class="sxs-lookup"><span data-stu-id="089c8-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="089c8-124">Oprava: Extra tlačidlá pre **Nová príležitosť**, **Cenová ponuka**, **Riadok objednávky** a **Pridať produkt** sú viditeľné v príkazoch pre príležitosti, cenové ponuky, objednávkové produkty a vedľajšiu mriežku riadkov založených na projekte.</span><span class="sxs-lookup"><span data-stu-id="089c8-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines sub-grid.</span></span>


