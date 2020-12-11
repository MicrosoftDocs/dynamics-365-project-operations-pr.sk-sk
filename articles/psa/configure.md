---
title: Konfigurácia Project Service Automation
description: Kroky konfigurácie Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129202"
---
# <a name="configure-project-service"></a><span data-ttu-id="9e23a-103">Konfigurácia Project Service</span><span class="sxs-lookup"><span data-stu-id="9e23a-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9e23a-104">Pred použitím možností automatizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] na správu účtov, projektov a zdrojov, musíte dokončiť niekoľko konfiguračných krokov, aby sa zabezpečilo, že riešenie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bude vyhovovať potrebám organizácie.</span><span class="sxs-lookup"><span data-stu-id="9e23a-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="9e23a-105">Tieto kroky obsahujú:</span><span class="sxs-lookup"><span data-stu-id="9e23a-105">These steps include:</span></span>  
  
-   <span data-ttu-id="9e23a-106">[Nastavenie časových jednotiek](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="9e23a-107">Nastaviť merné jednotky doby v katalógu produktov, ktorý použijete ako základ pre plánovanie a vyúčtovanie projektov.</span><span class="sxs-lookup"><span data-stu-id="9e23a-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="9e23a-108">[Nastavenie meny a výmenných kurzov](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="9e23a-109">Nastavenie meny pre vaše projekty.</span><span class="sxs-lookup"><span data-stu-id="9e23a-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="9e23a-110">[Vytvorenie organizačných jednotiek](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="9e23a-111">Nastaviť skupiny, ktoré vaša spoločnosť používa na rozdelenie svoje podnikanie, geografia, obchodné funkcie, alebo iné logické divízie.</span><span class="sxs-lookup"><span data-stu-id="9e23a-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="9e23a-112">[Nastavenie frekvencie fakturácie](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="9e23a-113">Nastaviť časové obdobia, ktoré chcete použiť pre fakturáciu vašich klientov.</span><span class="sxs-lookup"><span data-stu-id="9e23a-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="9e23a-114">[Konfigurácia kategórií transakcií](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="9e23a-115">Nastaviť kategórie transakcií, ktoré môžu vaši poradcovia účtovať pri účtovateľných a neúčtovateľných nákladoch.</span><span class="sxs-lookup"><span data-stu-id="9e23a-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="9e23a-116">[Konfigurácia kategórií výdavkov](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="9e23a-117">Nastaviť kategórie, ktoré môžu vaši poradcovia účtovať pri účtovateľných a neúčtovateľných nákladoch.</span><span class="sxs-lookup"><span data-stu-id="9e23a-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="9e23a-118">[Vytvorenie položiek v katalógu produktov](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="9e23a-119">Pridať produkty, ktoré predávate, napríklad softvérové licencie do katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="9e23a-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="9e23a-120">[Vytvorenie cenníka](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="9e23a-121">Nastaviť rôzne cenníky, v závislosti na tom, koľko chcete účtovať vašim klientom za každú rolu, ktorú si ich projekt vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="9e23a-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="9e23a-122">[Nastavenie zdrojov](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="9e23a-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="9e23a-123">Pridať schopností, zručností, roly prostriedkov a ďalších zdrojov informácií, ktoré budete potrebovať pre vaše projekty.</span><span class="sxs-lookup"><span data-stu-id="9e23a-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9e23a-124">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="9e23a-124">See Also</span></span>  
 <span data-ttu-id="9e23a-125">[Project Service Automation – prehľad](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="9e23a-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="9e23a-126">[Konfigurácia Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="9e23a-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="9e23a-127">[Príručka manažéra obchodného vzťahu](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9e23a-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="9e23a-128">[Príručka projektového manažéra](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9e23a-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="9e23a-129">[Príručka správcu zdrojov](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="9e23a-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="9e23a-130">Príručka časom, nákladmi a spoluprácou</span><span class="sxs-lookup"><span data-stu-id="9e23a-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)