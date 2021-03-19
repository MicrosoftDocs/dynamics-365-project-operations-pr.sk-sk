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
ms.openlocfilehash: 06a29f67040cd7da583bdeae85d6a0f6a3684c52
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290603"
---
# <a name="configure-project-service"></a><span data-ttu-id="73bcc-103">Konfigurácia Project Service</span><span class="sxs-lookup"><span data-stu-id="73bcc-103">Configure Project Service</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="73bcc-104">Pred použitím možností automatizácie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] na správu účtov, projektov a zdrojov, musíte dokončiť niekoľko konfiguračných krokov, aby sa zabezpečilo, že riešenie [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] bude vyhovovať potrebám organizácie.</span><span class="sxs-lookup"><span data-stu-id="73bcc-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="73bcc-105">Tieto kroky obsahujú:</span><span class="sxs-lookup"><span data-stu-id="73bcc-105">These steps include:</span></span>  
  
-   <span data-ttu-id="73bcc-106">[Nastavenie časových jednotiek](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="73bcc-107">Nastaviť merné jednotky doby v katalógu produktov, ktorý použijete ako základ pre plánovanie a vyúčtovanie projektov.</span><span class="sxs-lookup"><span data-stu-id="73bcc-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="73bcc-108">[Nastavenie meny a výmenných kurzov](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="73bcc-109">Nastavenie meny pre vaše projekty.</span><span class="sxs-lookup"><span data-stu-id="73bcc-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="73bcc-110">[Vytvorenie organizačných jednotiek](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="73bcc-111">Nastaviť skupiny, ktoré vaša spoločnosť používa na rozdelenie svoje podnikanie, geografia, obchodné funkcie, alebo iné logické divízie.</span><span class="sxs-lookup"><span data-stu-id="73bcc-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="73bcc-112">[Nastavenie frekvencie fakturácie](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="73bcc-113">Nastaviť časové obdobia, ktoré chcete použiť pre fakturáciu vašich klientov.</span><span class="sxs-lookup"><span data-stu-id="73bcc-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="73bcc-114">[Konfigurácia kategórií transakcií](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="73bcc-115">Nastaviť kategórie transakcií, ktoré môžu vaši poradcovia účtovať pri účtovateľných a neúčtovateľných nákladoch.</span><span class="sxs-lookup"><span data-stu-id="73bcc-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="73bcc-116">[Konfigurácia kategórií výdavkov](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="73bcc-117">Nastaviť kategórie, ktoré môžu vaši poradcovia účtovať pri účtovateľných a neúčtovateľných nákladoch.</span><span class="sxs-lookup"><span data-stu-id="73bcc-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="73bcc-118">[Vytvorenie položiek v katalógu produktov](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="73bcc-119">Pridať produkty, ktoré predávate, napríklad softvérové licencie do katalógu produktov.</span><span class="sxs-lookup"><span data-stu-id="73bcc-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="73bcc-120">[Vytvorenie cenníka](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="73bcc-121">Nastaviť rôzne cenníky, v závislosti na tom, koľko chcete účtovať vašim klientom za každú rolu, ktorú si ich projekt vyžaduje.</span><span class="sxs-lookup"><span data-stu-id="73bcc-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="73bcc-122">[Nastavenie zdrojov](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="73bcc-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="73bcc-123">Pridať schopností, zručností, roly prostriedkov a ďalších zdrojov informácií, ktoré budete potrebovať pre vaše projekty.</span><span class="sxs-lookup"><span data-stu-id="73bcc-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="73bcc-124">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="73bcc-124">See Also</span></span>  
 <span data-ttu-id="73bcc-125">[Project Service Automation – prehľad](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="73bcc-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="73bcc-126">[Konfigurácia Project Service Automation](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="73bcc-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="73bcc-127">[Príručka manažéra obchodného vzťahu](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="73bcc-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="73bcc-128">[Príručka projektového manažéra](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="73bcc-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="73bcc-129">[Príručka správcu zdrojov](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="73bcc-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="73bcc-130">Príručka časom, nákladmi a spoluprácou</span><span class="sxs-lookup"><span data-stu-id="73bcc-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]