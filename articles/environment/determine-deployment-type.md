---
title: Určenie typu nasadenia
description: Táto téma poskytuje informácie, ktoré vám pomôžu určiť správny typ nasadenia Project operations pre vašu spoločnosť.
author: stsporen
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: e9d3a5d8e6e1daafac72a3b4c0380b679d1869bd
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401237"
---
# <a name="determine-your-deployment-type"></a><span data-ttu-id="ba29f-103">Určenie typu nasadenia</span><span class="sxs-lookup"><span data-stu-id="ba29f-103">Determine your deployment type</span></span>

<span data-ttu-id="ba29f-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="ba29f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ba29f-105">Po zakúpení licencie začnite v tejto časti a vyberte najlepší model nasadenia Dynamics 365 Project Operations pomocou [Riadeného postupu inštalácie](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ba29f-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="ba29f-106">Po dokončení postupu riadenej inštalácie budete presmerovaní na správny portál na riadenie, aby ste dokončili inštaláciu.</span><span class="sxs-lookup"><span data-stu-id="ba29f-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="ba29f-107">Dokončite inštaláciu podľa podrobností nasadenia.</span><span class="sxs-lookup"><span data-stu-id="ba29f-107">See the deployment details to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="ba29f-108">Existujúci zákazníci systému Dynamics používajú Dynamics 365 Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="ba29f-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="ba29f-109">Project Operations obsahuje funkcie dodávané s Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="ba29f-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="ba29f-110">Pre týchto zákazníkov bude vydaný aktualizačný postup v 1. vlne vydaní na rok 2021.</span><span class="sxs-lookup"><span data-stu-id="ba29f-110">An upgrade path will be released for these customers in the 2021 release wave 1.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="ba29f-111">Existujúci zákazníci Dynamics 365 Finance používajúci Projektové riadenie a účtovníctvo</span><span class="sxs-lookup"><span data-stu-id="ba29f-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="ba29f-112">Existujúci zákazníci aplikácie Financie, ktorí používajú funkciu Projektový manažment a účtovníctvo, ju môžu naďalej používať tak, ako je.</span><span class="sxs-lookup"><span data-stu-id="ba29f-112">Existing customers of Finance who use the Project management and accounting functionality can continue to use it as is.</span></span> <span data-ttu-id="ba29f-113">Pozrite si [Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky](#pma).</span><span class="sxs-lookup"><span data-stu-id="ba29f-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>


## <a name="deployment-types"></a><span data-ttu-id="ba29f-114">Typy nasadenia</span><span class="sxs-lookup"><span data-stu-id="ba29f-114">Deployment types</span></span>
<span data-ttu-id="ba29f-115">Project Operations podporuje viac možností nasadenia, aby zodpovedali vašim požiadavkám.</span><span class="sxs-lookup"><span data-stu-id="ba29f-115">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="ba29f-116">Či už ste novým alebo existujúcim zákazníkom Dynamics 365, Project Operations môže podporiť vaše potreby.</span><span class="sxs-lookup"><span data-stu-id="ba29f-116">Whether you're a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="ba29f-117">Náš [Dotazník o nasadení](https://aka.ms/provisionprojectoperations) vám pomôže určiť správne nasadenie.</span><span class="sxs-lookup"><span data-stu-id="ba29f-117">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="ba29f-118">Výsledky vás prevedú jedným z nasledujúcich typov nasadenia:</span><span class="sxs-lookup"><span data-stu-id="ba29f-118">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="ba29f-119">Čiastočné nasadenie – dohoda o fakturácii pro forma</span><span class="sxs-lookup"><span data-stu-id="ba29f-119">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="ba29f-120">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek</span><span class="sxs-lookup"><span data-stu-id="ba29f-120">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="ba29f-121">Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky</span><span class="sxs-lookup"><span data-stu-id="ba29f-121">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="ba29f-122">Project Operations podporuje scenáre využívajúce skladované materiály/výrobné objednávky a neskladové scenáre/scenáre založené na zdrojoch v rovnakom prostredí prostredníctvom konfigurácií na úrovni právnických osôb.</span><span class="sxs-lookup"><span data-stu-id="ba29f-122">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="ba29f-123">Spoločnosť Contoso môže napríklad využiť možnosti skladovaných materiálov/výrobných objednávok vo svojom výrobnom závode v USA (právnická entita = Contoso Manufacturing United States).</span><span class="sxs-lookup"><span data-stu-id="ba29f-123">For example, Contoso can use the stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States).</span></span> <span data-ttu-id="ba29f-124">Spoločnosť Contoso môže využívať možnosti neskladovaných položiek/zdrojov vo svojom servisnom stredisku Contoso Robotics Arms vo Veľkej Británii (právnická entita = Contoso Robotics United Kingdom).</span><span class="sxs-lookup"><span data-stu-id="ba29f-124">Contoso can use the non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

### <a name="lite-deployment---deal-to-proforma-invoicing"></a><a  name="lite"></a><span data-ttu-id="ba29f-125">Jednoduché nasadenie – dohoda o fakturácii pro forma</span><span class="sxs-lookup"><span data-stu-id="ba29f-125">Lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="ba29f-126">Jednoduché nasadenie zahŕňa nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="ba29f-126">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="ba29f-127">Proces predaja pre projekty, ktoré rozširujú možnosti aplikácie Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="ba29f-127">Sales process for projects that extends Dynamics 365 Sales application experiences</span></span>
- <span data-ttu-id="ba29f-128">Plánovanie projektu pomocou programu Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="ba29f-128">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ba29f-129">Viacrozmerné ceny</span><span class="sxs-lookup"><span data-stu-id="ba29f-129">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ba29f-130">Jednotná správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="ba29f-130">Unified resource management</span></span>
- <span data-ttu-id="ba29f-131">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="ba29f-131">Time tracking</span></span>
- <span data-ttu-id="ba29f-132">Základné výdavky</span><span class="sxs-lookup"><span data-stu-id="ba29f-132">Basic expense</span></span>
- <span data-ttu-id="ba29f-133">Fakturácia pro forma a fakturácia orientovaná na zákazníka</span><span class="sxs-lookup"><span data-stu-id="ba29f-133">Proforma and customer-facing invoicing</span></span> 

#### <a name="deployment-steps"></a><span data-ttu-id="ba29f-134">Postup nasadenia</span><span class="sxs-lookup"><span data-stu-id="ba29f-134">Deployment steps</span></span>
<span data-ttu-id="ba29f-135">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ba29f-135">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ba29f-136">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](lite-preview-subscription-sign-up.md) a [Zriadenie nového prostredia](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="ba29f-136">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


### <a name="project-operations-for-resourcenon-stocked-scenarios"></a><a name="integrated"></a><span data-ttu-id="ba29f-137">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek</span><span class="sxs-lookup"><span data-stu-id="ba29f-137">Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="ba29f-138">Project Operations pre scenáre riešenia zdrojov/neskladovaných položiek zahŕňa nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="ba29f-138">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
 
- <span data-ttu-id="ba29f-139">Proces predaja pre projekty, ktoré rozširujú aplikáciu Dynamics 365 Sales</span><span class="sxs-lookup"><span data-stu-id="ba29f-139">Sales process for projects that extends the Dynamics 365 Sales application</span></span>
- <span data-ttu-id="ba29f-140">Plánovanie projektu pomocou programu Microsoft Project for the Web</span><span class="sxs-lookup"><span data-stu-id="ba29f-140">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="ba29f-141">Viacrozmerné ceny</span><span class="sxs-lookup"><span data-stu-id="ba29f-141">Multi-dimensional pricing</span></span>
- <span data-ttu-id="ba29f-142">Jednotná správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="ba29f-142">Unified resource management</span></span>
- <span data-ttu-id="ba29f-143">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="ba29f-143">Time tracking</span></span>
- <span data-ttu-id="ba29f-144">Základné výdavky</span><span class="sxs-lookup"><span data-stu-id="ba29f-144">Basic expense</span></span>
- <span data-ttu-id="ba29f-145">Úplný výdavok</span><span class="sxs-lookup"><span data-stu-id="ba29f-145">Full expense</span></span>
- <span data-ttu-id="ba29f-146">Potvrdenie autorizácie vrátenia tovaru</span><span class="sxs-lookup"><span data-stu-id="ba29f-146">Receipt OCR</span></span>
- <span data-ttu-id="ba29f-147">Fakturácia pro forma a fakturácia orientovaná na zákazníka</span><span class="sxs-lookup"><span data-stu-id="ba29f-147">Proforma and customer-facing invoicing</span></span> 
- <span data-ttu-id="ba29f-148">Priznanie výnosov pre projekty</span><span class="sxs-lookup"><span data-stu-id="ba29f-148">Revenue recognition for projects</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="ba29f-149">Postup nasadenia</span><span class="sxs-lookup"><span data-stu-id="ba29f-149">Deployment steps</span></span>
<span data-ttu-id="ba29f-150">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ba29f-150">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ba29f-151">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](resource-sign-up-preview-subscription.md) a [Zriadenie nového prostredia](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="ba29f-151">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


### <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="ba29f-152">Project Operations pre scenáre využívajúce skladované materiály/výrobné objednávky</span><span class="sxs-lookup"><span data-stu-id="ba29f-152">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="ba29f-153">Plánovanie projektu pomocou štruktúry WBS</span><span class="sxs-lookup"><span data-stu-id="ba29f-153">Project planning using WBS</span></span>
- <span data-ttu-id="ba29f-154">Správa zdrojov</span><span class="sxs-lookup"><span data-stu-id="ba29f-154">Resource Management</span></span>
- <span data-ttu-id="ba29f-155">Sledovanie času</span><span class="sxs-lookup"><span data-stu-id="ba29f-155">Time Tracking</span></span>
- <span data-ttu-id="ba29f-156">Úplný výdavok</span><span class="sxs-lookup"><span data-stu-id="ba29f-156">Full Expense</span></span>
- <span data-ttu-id="ba29f-157">Potvrdenie autorizácie vrátenia tovaru</span><span class="sxs-lookup"><span data-stu-id="ba29f-157">Receipt OCR</span></span>
- <span data-ttu-id="ba29f-158">Úplné účtovanie</span><span class="sxs-lookup"><span data-stu-id="ba29f-158">Full Invoicing</span></span>
- <span data-ttu-id="ba29f-159">Priznanie výnosov</span><span class="sxs-lookup"><span data-stu-id="ba29f-159">Revenue Recognition</span></span>
- <span data-ttu-id="ba29f-160">Výrobné zákazky</span><span class="sxs-lookup"><span data-stu-id="ba29f-160">Production Orders</span></span>
- <span data-ttu-id="ba29f-161">Podpora materiálov</span><span class="sxs-lookup"><span data-stu-id="ba29f-161">Materials support</span></span>

#### <a name="deployment-steps"></a><span data-ttu-id="ba29f-162">Postup nasadenia</span><span class="sxs-lookup"><span data-stu-id="ba29f-162">Deployment steps</span></span>
<span data-ttu-id="ba29f-163">Určte najlepší model nasadenia Project Operations pomocou [Dotazníka o nasadení](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="ba29f-163">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="ba29f-164">Toto nasadenie je popísané v časti [Registrácia na odber ukážky](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) a [Zriadenie nového prostredia](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ba29f-164">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 

