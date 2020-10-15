---
title: Typy nasadenia
description: Táto téma poskytuje informácie, ktoré vám pomôžu určiť správny typ nasadenia Project operations pre vašu spoločnosť.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949068"
---
# <a name="deployment-types"></a><span data-ttu-id="43941-103">Typy nasadenia</span><span class="sxs-lookup"><span data-stu-id="43941-103">Deployment types</span></span>

<span data-ttu-id="43941-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="43941-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="43941-105">Po zakúpení licencie začnite v tejto časti a vyberte najlepší model nasadenia Dynamics 365 Project Operations pomocou [Riadeného postupu inštalácie](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="43941-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="43941-106">Po dokončení postupu riadenej inštalácie budete presmerovaní na správny portál na riadenie, aby ste dokončili inštaláciu.</span><span class="sxs-lookup"><span data-stu-id="43941-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="43941-107">Dokončite inštaláciu podľa podrobností nasadenia nižšie.</span><span class="sxs-lookup"><span data-stu-id="43941-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="43941-108">Existujúci zákazníci systému Dynamics používajú Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="43941-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="43941-109">Project Operations obsahuje funkcie dodávané s Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="43941-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="43941-110">Pre týchto zákazníkov bude v budúcnosti vydaná aktualizácia.</span><span class="sxs-lookup"><span data-stu-id="43941-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="43941-111">Existujúci zákazníci Dynamics 365 Finance používajúci Projektové riadenie a účtovníctvo</span><span class="sxs-lookup"><span data-stu-id="43941-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="43941-112">Existujúci zákazníci možnosti Financie, ktorí používajú funkciu projektového riadenia a účtovníctva, ju môžu naďalej používať tak, ako je.</span><span class="sxs-lookup"><span data-stu-id="43941-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="43941-113">Pozrite si [Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky](#pma).</span><span class="sxs-lookup"><span data-stu-id="43941-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="43941-114">Project Operations podporuje viac možností nasadenia, aby zodpovedali vašim požiadavkám.</span><span class="sxs-lookup"><span data-stu-id="43941-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="43941-115">Či už ste novým alebo existujúcim zákazníkom Dynamics 365, Project Operations môže podporiť vaše potreby.</span><span class="sxs-lookup"><span data-stu-id="43941-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="43941-116">Náš [Dotazník o nasadení](https://aka.ms/provisionprojectoperations) vám pomôže určiť správne nasadenie.</span><span class="sxs-lookup"><span data-stu-id="43941-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="43941-117">Výsledky vás prevedú jedným z nasledujúcich typov nasadenia:</span><span class="sxs-lookup"><span data-stu-id="43941-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="43941-118">Čiastočné nasadenie – dohoda o fakturácii pro forma</span><span class="sxs-lookup"><span data-stu-id="43941-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="43941-119">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek</span><span class="sxs-lookup"><span data-stu-id="43941-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="43941-120">Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky</span><span class="sxs-lookup"><span data-stu-id="43941-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="43941-121">Project Operations podporuje scenáre využívajúce skladované materiály/výrobné objednávky a neskladové scenáre/scenáre založené na zdrojoch v rovnakom prostredí prostredníctvom konfigurácií na úrovni právnických osôb.</span><span class="sxs-lookup"><span data-stu-id="43941-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="43941-122">Napríklad spoločnosť Contoso môže vo svojom výrobnom závode v USA (právnická osoba = Contoso Manufacturing United States) využívať možnosti skladových/výrobných objednávok a v rámci svojho servisného strediska Contoso Robotics Arms vo Veľkej Británii (právnická osoba = Contoso Robotics United Kingdom) neskladové možnosti/možnosti založené na zdrojoch.</span><span class="sxs-lookup"><span data-stu-id="43941-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="43941-123"><a name="lite"><a/>Jednoduché nasadenie – dohoda o fakturácii pro forma</span><span class="sxs-lookup"><span data-stu-id="43941-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="43941-124">Jednoduché nasadenie zahŕňa nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="43941-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="43941-125">Plánovanie projektu pomocou programu Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="43941-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="43941-126">Viacrozmerné ceny</span><span class="sxs-lookup"><span data-stu-id="43941-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="43941-127">Jednotná správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="43941-127">Unified Resource Management</span></span>
- <span data-ttu-id="43941-128">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="43941-128">Time Tracking</span></span>
- <span data-ttu-id="43941-129">Základné výdavky</span><span class="sxs-lookup"><span data-stu-id="43941-129">Basic Expense</span></span>
- <span data-ttu-id="43941-130">Návrh faktúry</span><span class="sxs-lookup"><span data-stu-id="43941-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="43941-131">Postup nasadenia:</span><span class="sxs-lookup"><span data-stu-id="43941-131">Deployment steps:</span></span>
<span data-ttu-id="43941-132">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="43941-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="43941-133">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](lite-preview-subscription-sign-up.md) a [Zriadenie nového prostredia](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="43941-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="43941-134"><a name="integrated"><a/>Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek</span><span class="sxs-lookup"><span data-stu-id="43941-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="43941-135">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek zahŕňa nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="43941-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="43941-136">Plánovanie projektu pomocou programu Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="43941-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="43941-137">Viacrozmerné ceny</span><span class="sxs-lookup"><span data-stu-id="43941-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="43941-138">Jednotná správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="43941-138">Unified Resource Management</span></span>
- <span data-ttu-id="43941-139">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="43941-139">Time Tracking</span></span>
- <span data-ttu-id="43941-140">Základné výdavky</span><span class="sxs-lookup"><span data-stu-id="43941-140">Basic Expense</span></span>
- <span data-ttu-id="43941-141">Úplný výdavok</span><span class="sxs-lookup"><span data-stu-id="43941-141">Full Expense</span></span>
- <span data-ttu-id="43941-142">Potvrdenie autorizácie vrátenia tovaru</span><span class="sxs-lookup"><span data-stu-id="43941-142">Receipt OCR</span></span>
- <span data-ttu-id="43941-143">Úplné účtovanie</span><span class="sxs-lookup"><span data-stu-id="43941-143">Full Invoicing</span></span>
- <span data-ttu-id="43941-144">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="43941-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="43941-145">Postup nasadenia:</span><span class="sxs-lookup"><span data-stu-id="43941-145">Deployment steps:</span></span>
<span data-ttu-id="43941-146">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="43941-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="43941-147">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](resource-sign-up-preview-subscription.md) a [Zriadenie nového prostredia](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="43941-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="43941-148">Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky</span><span class="sxs-lookup"><span data-stu-id="43941-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="43941-149">Plánovanie projektu pomocou štruktúry WBS</span><span class="sxs-lookup"><span data-stu-id="43941-149">Project planning using WBS</span></span>
- <span data-ttu-id="43941-150">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="43941-150">Resource Management</span></span>
- <span data-ttu-id="43941-151">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="43941-151">Time Tracking</span></span>
- <span data-ttu-id="43941-152">Úplný výdavok</span><span class="sxs-lookup"><span data-stu-id="43941-152">Full Expense</span></span>
- <span data-ttu-id="43941-153">Potvrdenie autorizácie vrátenia tovaru</span><span class="sxs-lookup"><span data-stu-id="43941-153">Receipt OCR</span></span>
- <span data-ttu-id="43941-154">Úplné účtovanie</span><span class="sxs-lookup"><span data-stu-id="43941-154">Full Invoicing</span></span>
- <span data-ttu-id="43941-155">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="43941-155">Revenue Recognition</span></span>
- <span data-ttu-id="43941-156">Výrobné zákazky</span><span class="sxs-lookup"><span data-stu-id="43941-156">Production Orders</span></span>
- <span data-ttu-id="43941-157">Podpora materiálov</span><span class="sxs-lookup"><span data-stu-id="43941-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="43941-158">Postup nasadenia:</span><span class="sxs-lookup"><span data-stu-id="43941-158">Deployment steps:</span></span>
<span data-ttu-id="43941-159">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="43941-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="43941-160">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) a [Zriadenie nového prostredia](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="43941-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



