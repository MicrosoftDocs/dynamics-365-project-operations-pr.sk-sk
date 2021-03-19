---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 13, V3
description: Táto téma poskytuje informácie o tom, čo je nové v aktualizácii Project Service Automation, vydanie 13, V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: dbdcb811bfeacf17e841d679f097c591c16cd4c0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281047"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="50533-103">Aktualizácia pre Project Service Automation, vydanie 13, V3</span><span class="sxs-lookup"><span data-stu-id="50533-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="50533-104">S potešením vám oznamujeme najnovšiu aktualizáciu pre aplikáciu Dynamics 365 Project Service Automation (PSA).</span><span class="sxs-lookup"><span data-stu-id="50533-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="50533-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="50533-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="50533-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="50533-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="50533-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="50533-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="50533-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="50533-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="50533-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu Project Service Automation V3, vydanie 13.</span><span class="sxs-lookup"><span data-stu-id="50533-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="50533-110">Táto verzia má číslo zostavenia V3.10.3.18 a je k dispozícii v nasledujúcom harmonograme:</span><span class="sxs-lookup"><span data-stu-id="50533-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="50533-111">**Všeobecná dostupnosť (samoaktualizácia):** November 2019</span><span class="sxs-lookup"><span data-stu-id="50533-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="50533-112">**Automatická Aktualizácia** December 2019</span><span class="sxs-lookup"><span data-stu-id="50533-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="50533-113">Aktualizácia vydania 13</span><span class="sxs-lookup"><span data-stu-id="50533-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="50533-114">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="50533-114">Bug fixes</span></span>

- <span data-ttu-id="50533-115">Čas a výdavky</span><span class="sxs-lookup"><span data-stu-id="50533-115">Time and Expense</span></span>

     - <span data-ttu-id="50533-116">Oprava: Funkcie vyhľadávania na stránke **Schválenie výdavkov** nefungujú pri vyhľadávaní podľa účelu výdavkov.</span><span class="sxs-lookup"><span data-stu-id="50533-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="50533-117">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="50533-117">Resource Management</span></span>

     - <span data-ttu-id="50533-118">Oprava: Čísla v odsúhlasení boli aktualizované, aby boli správne zarovnané.</span><span class="sxs-lookup"><span data-stu-id="50533-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="50533-119">Oprava: Pomenované zdroje nemôžu byť priradené k úlohám prostredníctvom karty **Plán**.</span><span class="sxs-lookup"><span data-stu-id="50533-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="50533-120">Riadenie projektov</span><span class="sxs-lookup"><span data-stu-id="50533-120">Project Management</span></span>

     - <span data-ttu-id="50533-121">Oprava: Nulová referenčná výnimka pri prideľovaní člena tímu, keď typu **TransactionType** chýbajú informácie o nastavení pre **Jednotka** a **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="50533-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="50533-122">Sales</span><span class="sxs-lookup"><span data-stu-id="50533-122">Sales</span></span>

     - <span data-ttu-id="50533-123">Oprava: Duplicitné záznamy typu transakcie vracajú chybu pri vytváraní záznamov o cenách rolí.</span><span class="sxs-lookup"><span data-stu-id="50533-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="50533-124">Opravené: Extra tlačidlá pre **Nová príležitosť**, **Cenová ponuka**, **Riadok objednávky** a **Pridať produkt** sú viditeľné v príkazoch pre Príležitosti, Cenové ponuky, Produkty objednávky a vedľajšiu mriežku riadkov založených na projektoch.</span><span class="sxs-lookup"><span data-stu-id="50533-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]