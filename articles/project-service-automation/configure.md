---
title: Konfigurácia Project Service Automation
description: Kroky konfigurácie Project Service
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 56ba0b8d-808c-48d6-965f-abd74b49c2b4
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 52be4705e6ef983dcf421df5d1bfb5c6de8e9a30
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755569"
---
# <a name="configure-project-service"></a><span data-ttu-id="7c848-103">Konfigurácia Project Service</span><span class="sxs-lookup"><span data-stu-id="7c848-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7c848-104">Pred použitím možností automatizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] na správu účtov, projektov a zdrojov, musíte dokončiť niekoľko konfiguračných krokov, aby sa zabezpečilo, že riešenie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bude vyhovovať potrebám organizácie.</span><span class="sxs-lookup"><span data-stu-id="7c848-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="7c848-105">Tieto kroky obsahujú:</span><span class="sxs-lookup"><span data-stu-id="7c848-105">These steps include:</span></span>  
  
-   <span data-ttu-id="7c848-106">[Nastavenie časových jednotiek](../project-service/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-106">[Set up time units](../project-service/set-up-time-units.md).</span></span> <span data-ttu-id="7c848-107">Nastaviť merné jednotky doby v katalógu produktov, ktorý použijete ako základ pre plánovanie a vyúčtovanie projektov.</span><span class="sxs-lookup"><span data-stu-id="7c848-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="7c848-108">[Nastavenie meny a výmenných kurzov](../project-service/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-108">[Set up currencies and exchange rates](../project-service/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="7c848-109">Nastavenie meny pre vaše projekty.</span><span class="sxs-lookup"><span data-stu-id="7c848-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="7c848-110">[Vytvorenie organizačných jednotiek](../project-service/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-110">[Create organizational units](../project-service/create-organizational-units.md).</span></span> <span data-ttu-id="7c848-111">Nastaviť skupiny, ktoré vaša spoločnosť používa na rozdelenie svoje podnikanie, geografia, obchodné funkcie, alebo iné logické divízie.</span><span class="sxs-lookup"><span data-stu-id="7c848-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="7c848-112">[Nastavenie frekvencie fakturácie](../project-service/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-112">[Set up invoice frequencies](../project-service/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="7c848-113">Nastaviť časové obdobia, ktoré chcete použiť pre fakturáciu vašich klientov.</span><span class="sxs-lookup"><span data-stu-id="7c848-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="7c848-114">[Konfigurácia kategórií transakcií](../project-service/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-114">[Configure transaction categories](../project-service/configure-transaction-categories.md).</span></span> <span data-ttu-id="7c848-115">Nastaviť kategórie transakcií, ktoré môžu vaši poradcovia účtovať pri účtovateľných a neúčtovateľných nákladoch.</span><span class="sxs-lookup"><span data-stu-id="7c848-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="7c848-116">[Konfigurácia kategórií výdavkov](../project-service/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-116">[Configure expense categories](../project-service/configure-expense-categories.md).</span></span> <span data-ttu-id="7c848-117">Nastaviť kategórie, ktoré môžu vaši poradcovia účtovať pri účtovateľných a neúčtovateľných nákladoch.</span><span class="sxs-lookup"><span data-stu-id="7c848-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="7c848-118">[Vytvorenie položiek v katalógu produktov](../project-service/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-118">[Create product catalog items](../project-service/create-product-catalog-items.md).</span></span> <span data-ttu-id="7c848-119">Pridať produkty, ktoré predávate, napríklad softvérové licencie do katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="7c848-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="7c848-120">[Vytvorenie cenníka](../project-service/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-120">[Create a price list](../project-service/create-price-list.md).</span></span> <span data-ttu-id="7c848-121">Nastaviť rôzne cenníky, v závislosti na tom, koľko chcete účtovať vašim klientom za každú rolu, ktorú si ich projekt vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="7c848-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="7c848-122">[Nastavenie zdrojov](../project-service/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="7c848-122">[Set up resources](../project-service/set-up-resources.md).</span></span> <span data-ttu-id="7c848-123">Pridať schopností, zručností, roly prostriedkov a ďalších zdrojov informácií, ktoré budete potrebovať pre vaše projekty.</span><span class="sxs-lookup"><span data-stu-id="7c848-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="7c848-124">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="7c848-124">See Also</span></span>  
 <span data-ttu-id="7c848-125">[Project Service Automation – prehľad](../project-service/overview.md) </span><span class="sxs-lookup"><span data-stu-id="7c848-125">[Overview of Project Service Automation](../project-service/overview.md) </span></span>  
 <span data-ttu-id="7c848-126">[Konfigurácia Project Service Automation](../project-service/configure.md) </span><span class="sxs-lookup"><span data-stu-id="7c848-126">[Configure Project Service Automation](../project-service/configure.md) </span></span>  
 <span data-ttu-id="7c848-127">[Príručka manažéra obchodného vzťahu](../project-service/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7c848-127">[Account Manager Guide](../project-service/account-manager-guide.md) </span></span>  
 <span data-ttu-id="7c848-128">[Príručka projektového manažéra](../project-service/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7c848-128">[Project Manager Guide](../project-service/project-manager-guide.md) </span></span>  
 <span data-ttu-id="7c848-129">[Príručka správcu zdrojov](../project-service/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="7c848-129">[Resource Manager Guide](../project-service/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="7c848-130">Príručka časom, nákladmi a spoluprácou</span><span class="sxs-lookup"><span data-stu-id="7c848-130">Time, Expense, and Collaboration Guid</span></span>](../project-service/time-expense-collaboration-guide.md)
