---
title: Určenie typu nasadenia
description: Táto téma poskytuje informácie, ktoré vám pomôžu určiť správny typ nasadenia Project operations pre vašu spoločnosť.
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 564f2878553fe3904a7c47c7e80a3b57c763a3b2
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084368"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="3b5a7-103">Určenie typu nasadenia</span><span class="sxs-lookup"><span data-stu-id="3b5a7-103">Determine your deployment type</span></span>

<span data-ttu-id="3b5a7-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="3b5a7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3b5a7-105">Po zakúpení licencie začnite v tejto časti a vyberte najlepší model nasadenia Dynamics 365 Project Operations pomocou [Riadeného postupu inštalácie](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="3b5a7-106">Po dokončení postupu riadenej inštalácie budete presmerovaní na správny portál na riadenie, aby ste dokončili inštaláciu.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="3b5a7-107">Dokončite inštaláciu podľa podrobností nasadenia.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="3b5a7-108">Existujúci zákazníci systému Dynamics používajú Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3b5a7-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="3b5a7-109">Project Operations obsahuje funkcie dodávané s Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="3b5a7-110">Pre týchto zákazníkov bude v budúcnosti vydaná aktualizácia.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="3b5a7-111">Existujúci zákazníci Dynamics 365 Finance používajúci Projektové riadenie a účtovníctvo</span><span class="sxs-lookup"><span data-stu-id="3b5a7-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="3b5a7-112">Existujúci zákazníci možnosti Financie, ktorí používajú funkciu projektového riadenia a účtovníctva, ju môžu naďalej používať tak, ako je.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use this as is.</span></span> <span data-ttu-id="3b5a7-113">Pozrite si [Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky](#pma).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="3b5a7-114">Typy nasadenia</span><span class="sxs-lookup"><span data-stu-id="3b5a7-114">Deployment types</span></span>
<span data-ttu-id="3b5a7-115">Project Operations podporuje viac možností nasadenia, aby zodpovedali vašim požiadavkám.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="3b5a7-116">Či už ste novým alebo existujúcim zákazníkom Dynamics 365, Project Operations môže podporiť vaše potreby.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="3b5a7-117">Náš [Dotazník o nasadení](https://aka.ms/provisionprojectoperations) vám pomôže určiť správne nasadenie.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="3b5a7-118">Výsledky vás prevedú jedným z nasledujúcich typov nasadenia:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="3b5a7-119">Čiastočné nasadenie – dohoda o fakturácii pro forma</span><span class="sxs-lookup"><span data-stu-id="3b5a7-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="3b5a7-120">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek</span><span class="sxs-lookup"><span data-stu-id="3b5a7-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="3b5a7-121">Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky</span><span class="sxs-lookup"><span data-stu-id="3b5a7-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="3b5a7-122">Project Operations podporuje scenáre využívajúce skladované materiály/výrobné objednávky a neskladové scenáre/scenáre založené na zdrojoch v rovnakom prostredí prostredníctvom konfigurácií na úrovni právnických osôb.</span><span class="sxs-lookup"><span data-stu-id="3b5a7-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="3b5a7-123">Spoločnosť Contoso môže napríklad využiť možnosti skladovaných materiálov/výrobných objednávok vo svojom výrobnom závode v USA (právnická entita = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="3b5a7-124">Spoločnosť Contoso môže využívať možnosti neskladovaných položiek/zdrojov vo svojom servisnom stredisku Contoso Robotics Arms vo Veľkej Británii (právnická entita = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="3b5a7-125">Jednoduché nasadenie – dohoda o fakturácii pro forma</span><span class="sxs-lookup"><span data-stu-id="3b5a7-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="3b5a7-126">Jednoduché nasadenie zahŕňa nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="3b5a7-127">Plánovanie projektu pomocou programu Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="3b5a7-127">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="3b5a7-128">Viacrozmerné ceny</span><span class="sxs-lookup"><span data-stu-id="3b5a7-128">Multi-dimensional pricing</span></span>
- <span data-ttu-id="3b5a7-129">Jednotná správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="3b5a7-129">Unified Resource Management</span></span>
- <span data-ttu-id="3b5a7-130">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="3b5a7-130">Time Tracking</span></span>
- <span data-ttu-id="3b5a7-131">Základné výdavky</span><span class="sxs-lookup"><span data-stu-id="3b5a7-131">Basic Expense</span></span>
- <span data-ttu-id="3b5a7-132">Návrh faktúry</span><span class="sxs-lookup"><span data-stu-id="3b5a7-132">Invoice Proposal</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3b5a7-133">Postup nasadenia</span><span class="sxs-lookup"><span data-stu-id="3b5a7-133">Deployment steps</span></span>
<span data-ttu-id="3b5a7-134">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-134">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3b5a7-135">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](lite-preview-subscription-sign-up.md) a [Zriadenie nového prostredia](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-135">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="3b5a7-136">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek</span><span class="sxs-lookup"><span data-stu-id="3b5a7-136">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="3b5a7-137">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek zahŕňa nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="3b5a7-137">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="3b5a7-138">Plánovanie projektu pomocou programu Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="3b5a7-138">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="3b5a7-139">Viacrozmerné ceny</span><span class="sxs-lookup"><span data-stu-id="3b5a7-139">Multi-dimensional pricing</span></span>
- <span data-ttu-id="3b5a7-140">Jednotná správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="3b5a7-140">Unified Resource Management</span></span>
- <span data-ttu-id="3b5a7-141">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="3b5a7-141">Time Tracking</span></span>
- <span data-ttu-id="3b5a7-142">Základné výdavky</span><span class="sxs-lookup"><span data-stu-id="3b5a7-142">Basic Expense</span></span>
- <span data-ttu-id="3b5a7-143">Úplný výdavok</span><span class="sxs-lookup"><span data-stu-id="3b5a7-143">Full Expense</span></span>
- <span data-ttu-id="3b5a7-144">Potvrdenie autorizácie vrátenia tovaru</span><span class="sxs-lookup"><span data-stu-id="3b5a7-144">Receipt OCR</span></span>
- <span data-ttu-id="3b5a7-145">Úplné účtovanie</span><span class="sxs-lookup"><span data-stu-id="3b5a7-145">Full Invoicing</span></span>
- <span data-ttu-id="3b5a7-146">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="3b5a7-146">Revenue Recognition</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3b5a7-147">Postup nasadenia</span><span class="sxs-lookup"><span data-stu-id="3b5a7-147">Deployment steps</span></span>
<span data-ttu-id="3b5a7-148">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-148">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3b5a7-149">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](resource-sign-up-preview-subscription.md) a [Zriadenie nového prostredia](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-149">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="3b5a7-150">Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky</span><span class="sxs-lookup"><span data-stu-id="3b5a7-150">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="3b5a7-151">Plánovanie projektu pomocou štruktúry WBS</span><span class="sxs-lookup"><span data-stu-id="3b5a7-151">Project planning using WBS</span></span>
- <span data-ttu-id="3b5a7-152">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="3b5a7-152">Resource Management</span></span>
- <span data-ttu-id="3b5a7-153">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="3b5a7-153">Time Tracking</span></span>
- <span data-ttu-id="3b5a7-154">Úplný výdavok</span><span class="sxs-lookup"><span data-stu-id="3b5a7-154">Full Expense</span></span>
- <span data-ttu-id="3b5a7-155">Potvrdenie autorizácie vrátenia tovaru</span><span class="sxs-lookup"><span data-stu-id="3b5a7-155">Receipt OCR</span></span>
- <span data-ttu-id="3b5a7-156">Úplné účtovanie</span><span class="sxs-lookup"><span data-stu-id="3b5a7-156">Full Invoicing</span></span>
- <span data-ttu-id="3b5a7-157">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="3b5a7-157">Revenue Recognition</span></span>
- <span data-ttu-id="3b5a7-158">Výrobné zákazky</span><span class="sxs-lookup"><span data-stu-id="3b5a7-158">Production Orders</span></span>
- <span data-ttu-id="3b5a7-159">Podpora materiálov</span><span class="sxs-lookup"><span data-stu-id="3b5a7-159">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="3b5a7-160">Postup nasadenia</span><span class="sxs-lookup"><span data-stu-id="3b5a7-160">Deployment steps</span></span>
<span data-ttu-id="3b5a7-161">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-161">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="3b5a7-162">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) a [Zriadenie nového prostredia](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="3b5a7-162">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

