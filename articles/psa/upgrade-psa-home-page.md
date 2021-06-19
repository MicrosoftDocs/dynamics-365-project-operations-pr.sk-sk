---
title: Inovovať domovskú stránku
description: Táto téma zobrazuje Dynamics 365 Project Service Automation, kde nájdete dôležité informácie o nových a zmenených funkciách a procese inovácie na najnovšiu verziu.
ms.prod: ''
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a2e17fbdfb71eb62053236bf6c8a3d1aedf332df
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012380"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="48c2b-103">Inovovať domovskú stránku</span><span class="sxs-lookup"><span data-stu-id="48c2b-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="48c2b-104">Inovujte z verzie 2.x alebo 1.x na verziu 3.x aplikácie PSA</span><span class="sxs-lookup"><span data-stu-id="48c2b-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="48c2b-105">Nové inštancie</span><span class="sxs-lookup"><span data-stu-id="48c2b-105">New instances</span></span>

<span data-ttu-id="48c2b-106">Od 17. mája 2019, keď sa Project Service Automation vyberie vybratá počas poskytovania novej inštancie, verzia 3. x sa predvolene nainštaluje.</span><span class="sxs-lookup"><span data-stu-id="48c2b-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="48c2b-107">Existujúce inštancie</span><span class="sxs-lookup"><span data-stu-id="48c2b-107">Existing instances</span></span>

<span data-ttu-id="48c2b-108">Predtým zákazníci, ktorí majú inštanciu PSA verzia 2.x a potrebovali ju inovovať na verziu 3.x, ktorá predstavuje zjednotené klientské používateľské rozhranie (UCI) verzia PSA, museli kontaktovať podporu spoločnosti Microsoft a poskytnúť podrobnosti o ich inštancii, aby mohla pripraviť inštanciu na inováciu na verziu 3.x.</span><span class="sxs-lookup"><span data-stu-id="48c2b-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="48c2b-109">Od 1. marca 2020 budú mať zákazníci, ktorí majú inštanciu PSA verzie 2.x a potrebujú aktualizáciu na verziu 3.x, možnosť inovovať svoje inštancie priamo z portálu správy služby bez toho, aby museli kontaktovať podporu spoločnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="48c2b-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="48c2b-110">PSA verzia 3.x obsahuje významné zmeny.</span><span class="sxs-lookup"><span data-stu-id="48c2b-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="48c2b-111">Bola vytvorená na rámci zjednoteného rozhrania, aby pomáhala poskytovať zlepšenú používateľskú skúsenosť.</span><span class="sxs-lookup"><span data-stu-id="48c2b-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="48c2b-112">Pretvorená aplikácia ponúka jednotné používateľské rozhranie (UI), ktoré nasleduje responzívne princípy dizajnu pre optimálne prezeranie na ľubovoľnej veľkosti obrazovky alebo zariadení.</span><span class="sxs-lookup"><span data-stu-id="48c2b-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="48c2b-113">Počas celej aplikácie sa vyskytli ďalšie zmeny.</span><span class="sxs-lookup"><span data-stu-id="48c2b-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="48c2b-114">Medzi niektoré z oblastí, ktoré boli zmenené, patria ceny, rezervácie a priraďovanie zdrojov, času, výdavkov a schválenia.</span><span class="sxs-lookup"><span data-stu-id="48c2b-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="48c2b-115">Pred začatím procesu inovácie, odporúčame, aby ste dokončili nasledujúce úlohy:</span><span class="sxs-lookup"><span data-stu-id="48c2b-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="48c2b-116">Overte, či Dynamics 365 Field Service a Project Service Automation sú nainštalované na identifikovanej inštancii.</span><span class="sxs-lookup"><span data-stu-id="48c2b-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="48c2b-117">Ak sú nainštalované obidva riešenia, mali by ste plánovať inováciu skôr, ako obnovíte pravidelné používanie inštancie.</span><span class="sxs-lookup"><span data-stu-id="48c2b-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="48c2b-118">Pozorne si prečítajte nasledujúce témy.</span><span class="sxs-lookup"><span data-stu-id="48c2b-118">Carefully review the following topics.</span></span> <span data-ttu-id="48c2b-119">Povedomie a pochopenie zmien medzi verziami vám pomôže s procesom inovácie.</span><span class="sxs-lookup"><span data-stu-id="48c2b-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="48c2b-120">Tieto témy poskytujú informácie o hlavných zmenách v PSA, spolu s úvahami a odporúčaniami pre plánovanie inovácie na verziu 3.x.</span><span class="sxs-lookup"><span data-stu-id="48c2b-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="48c2b-121">Čo je nové alebo zmenené v Project Service Automation verzia 3</span><span class="sxs-lookup"><span data-stu-id="48c2b-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="48c2b-122">Informácie o inovácii – Project Service Automation verzia 2.x alebo 1.x na verziu 3</span><span class="sxs-lookup"><span data-stu-id="48c2b-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="48c2b-123">Inovujte inštancia izolovaného priestoru na vyhodnotenie zmien vo vykonávaní pred inováciou výrobnej inštancie.</span><span class="sxs-lookup"><span data-stu-id="48c2b-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="48c2b-124">Potom, čo ste preskúmali témy, ktoré boli spomenuté skôr a sú pripravení na upgrade na PSA verzia 3.x alebo verzia UCI, odošlite požiadavku na podporu spoločnosti Microsoft, aby inovácia bola k dispozícii z centra správcu.</span><span class="sxs-lookup"><span data-stu-id="48c2b-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="48c2b-125">V žiadosti uveďte podrobnosti o vašej inštancii.</span><span class="sxs-lookup"><span data-stu-id="48c2b-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="48c2b-126">Staršie verzie PSA (PSA verzia 2.x) v novo vytvorenej inštancie</span><span class="sxs-lookup"><span data-stu-id="48c2b-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="48c2b-127">Od mája 17, 2019, všetky nové inštancie budú mať UCI ako predvolený klient.</span><span class="sxs-lookup"><span data-stu-id="48c2b-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="48c2b-128">Pre vyrovnanie s touto zmenou, PSA verzia 3.x a Field Service verzia 8.x bude poskytnutá v predvolenom nastavení, pretože tieto verzie sú navrhnuté pre prácu s klientom UCI.</span><span class="sxs-lookup"><span data-stu-id="48c2b-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="48c2b-129">Od 1. marca 2020 už zákazníci systému Dynamics PSA nebudú môcť vytvárať nové prostredie so staršími verziami PSA, napríklad PSA verzie 2.x alebo nižšou.</span><span class="sxs-lookup"><span data-stu-id="48c2b-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="48c2b-130">Akékoľvek nové prostredie bude mať získať iba verziu 3.x PSA.</span><span class="sxs-lookup"><span data-stu-id="48c2b-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="48c2b-131">Najlepšie skúsenosti pri používaní starších verzií služieb Field Service a PSA nájdete na stránke **Systémové nastavenia** a pre pole **Používanie výhradne nového Zjednoteného rozhrania (odporúča sa)** zvoľte možnosť **Nie**, pretože tieto verzie nie sú navrhnuté tak, aby sa správne načítavali v UCI.</span><span class="sxs-lookup"><span data-stu-id="48c2b-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="48c2b-132">Potom, čo ste vypli UCI, môžete otvoriť a spustiť tieto verzie Field Service a PSA pomocou starého webového klienta.</span><span class="sxs-lookup"><span data-stu-id="48c2b-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]