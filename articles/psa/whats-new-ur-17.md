---
title: Čo je nové alebo zmenené v aktualizácii Project Service Automation, vydanie 17, V3
description: Táto téma obsahuje zoznam funkcií a opráv dostupných v aktualizácii Project Service Automation, vydanie 17, V3
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 03/06/2020
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
ms.openlocfilehash: c2b27582a401e41da0a9e60c8f2f32dcdd1944c2
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949248"
---
# <a name="project-service-automation-update-release-17-v3"></a><span data-ttu-id="d93c0-103">Aktualizácia pre Project Service Automation, vydanie 17, V3</span><span class="sxs-lookup"><span data-stu-id="d93c0-103">Project Service Automation Update Release 17, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="d93c0-104">S potešením vám oznamujeme najnovšiu aktualizáciu aplikácie Project Service Automation pre Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="d93c0-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="d93c0-105">Toto vydanie obsahuje niekoľko dôležitých zlepšení kvality, výkonu a použiteľnosti.</span><span class="sxs-lookup"><span data-stu-id="d93c0-105">This release includes some important improvements to quality, performance, and usability.</span></span>  <span data-ttu-id="d93c0-106">Toto vydanie je kompatibilné s Dynamics 365 9.x.</span><span class="sxs-lookup"><span data-stu-id="d93c0-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="d93c0-107">Ak chcete aktualizovať toto vydanie, navštívte centrum spravovania pre Dynamics 365 online, prejdite na stránku riešení a nainštalujte aktualizáciu.</span><span class="sxs-lookup"><span data-stu-id="d93c0-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="d93c0-108">Ďalšie informácie sa dozviete v časti [Inštalácia, aktualizácia alebo odstránenie preferovaného riešenia](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="d93c0-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="d93c0-109">Táto téma obsahuje zoznam funkcií a opráv, ktoré sú nové alebo zmenené pre aktualizáciu PSA V3, vydanie 17.</span><span class="sxs-lookup"><span data-stu-id="d93c0-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 17.</span></span> <span data-ttu-id="d93c0-110">Táto verzia má číslo zostavy V3.10.6.34 a je všeobecne dostupná prostredníctvom samoaktualizácie v marci 2020.</span><span class="sxs-lookup"><span data-stu-id="d93c0-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in March 2020.</span></span>


## <a name="update-release-17"></a><span data-ttu-id="d93c0-111">Aktualizácia vydania 17</span><span class="sxs-lookup"><span data-stu-id="d93c0-111">Update Release 17</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="d93c0-112">Opravy chýb</span><span class="sxs-lookup"><span data-stu-id="d93c0-112">Bug fixes</span></span>

<span data-ttu-id="d93c0-113">**Všeobecné**</span><span class="sxs-lookup"><span data-stu-id="d93c0-113">**General**</span></span>

- <span data-ttu-id="d93c0-114">Oprava: Aktualizácia Project Service Automation na vynútenie licencií členov tímu (Centrum projektových zdrojov bude obsahovať metaúdaje plánu Team Member Service 3.x)</span><span class="sxs-lookup"><span data-stu-id="d93c0-114">Fixed: Update Project Service Automation to enforce Team Member licenses (Project Resource Hub will include Team Member Service plan metadata 3.x)</span></span>
 
<span data-ttu-id="d93c0-115">**Čas a výdavky**</span><span class="sxs-lookup"><span data-stu-id="d93c0-115">**Time and Expense**</span></span>

- <span data-ttu-id="d93c0-116">Oprava: Nie je možné zmeniť odhad výdavkov z nenulovej ceny na nulu (0).</span><span class="sxs-lookup"><span data-stu-id="d93c0-116">Fixed: It is not possible to change an expense estimate from a non-zero price to zero (0).</span></span> <span data-ttu-id="d93c0-117">Zmena sa ignoruje.</span><span class="sxs-lookup"><span data-stu-id="d93c0-117">The change is ignored.</span></span>

<span data-ttu-id="d93c0-118">**Riadenie projektov**</span><span class="sxs-lookup"><span data-stu-id="d93c0-118">**Project Management**</span></span>

- <span data-ttu-id="d93c0-119">Oprava: Do názvu pozície člena tímu bola pridaná kontrola nulových hodnôt.</span><span class="sxs-lookup"><span data-stu-id="d93c0-119">Fixed: A check for null values has been added on a team member's position name.</span></span>
- <span data-ttu-id="d93c0-120">Opravené: pole **msdyn_userresourceid** v entite **msdyn_resourceassignment** bolo zastarané.</span><span class="sxs-lookup"><span data-stu-id="d93c0-120">Fixed: **msdyn_userresourceid** field on the **msdyn_resourceassignment** entity has been deprecated.</span></span>
- <span data-ttu-id="d93c0-121">Oprava: Aktualizácia z 2.x na 3.x teraz spracováva prázdne kontúry úsilia pri prideľovaní úloh.</span><span class="sxs-lookup"><span data-stu-id="d93c0-121">Fixed: Upgrade from 2.x to 3.x now handles empty effort contours on task assignments.</span></span>

<span data-ttu-id="d93c0-122">**Sales**</span><span class="sxs-lookup"><span data-stu-id="d93c0-122">**Sales**</span></span>

- <span data-ttu-id="d93c0-123">Opravené: **Invoice.PreValidateInvoiceUpdate** teraz rieši scenár správneho priradenia vlastníkov záznamov.</span><span class="sxs-lookup"><span data-stu-id="d93c0-123">Fixed: **Invoice.PreValidateInvoiceUpdate** now handles the scenario of reassigning record owners properly.</span></span>
- <span data-ttu-id="d93c0-124">Oprava: Keď je trieda transakcie **Čas**, **UnitGroup** nie je možné upravovať pre všetky entity vrátane **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail** a **ContractLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="d93c0-124">Fixed: When the transaction class is **Time**, **UnitGroup** is non-editable for all entities including, **QuoteLineDetails**, **JournalLine**, **InvoiceLineDetail**, and **ContractLineDetails**.</span></span> <span data-ttu-id="d93c0-125">Avšak **Jednotka** nie je upraviteľná len pre **JournalLine** a **InvoiceLineDetails**.</span><span class="sxs-lookup"><span data-stu-id="d93c0-125">However, **Unit** is non-editable only for **JournalLine** and **InvoiceLineDetails**.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]