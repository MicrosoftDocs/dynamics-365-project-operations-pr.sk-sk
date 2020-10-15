---
title: Konfigurácia kategórií projektov
description: Táto téma poskytuje informácie o nastavovaní kategórií projektov.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 84033182ce047d230724409eef9bc6afcaefd2b4
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3895985"
---
# <a name="configure-project-categories"></a><span data-ttu-id="04368-103">Konfigurácia kategórií projektov</span><span class="sxs-lookup"><span data-stu-id="04368-103">Configure project categories</span></span>

<span data-ttu-id="04368-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="04368-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="04368-105">Project Operations ponúka rozsiahle možnosti kategorizácie výnosov a výdavkov na projekty.</span><span class="sxs-lookup"><span data-stu-id="04368-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="04368-106">Kategórie poskytujú schopnosť reportovať a analyzovať projektové transakcie a riadiť účtovanie do všeobecnej hlavnej knihy.</span><span class="sxs-lookup"><span data-stu-id="04368-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="04368-107">Nasledujúci diagram ilustruje koreláciu medzi kategóriami transakcií, zdieľanými kategóriami a kategóriami projektu.</span><span class="sxs-lookup"><span data-stu-id="04368-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="04368-108">Kategórie transakcií sú základným zoskupením pre projektové transakcie.</span><span class="sxs-lookup"><span data-stu-id="04368-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="04368-109">V rámci tohto zoskupenia existuje skupina zdieľaných kategórií, ktoré je možné zdieľať medzi aplikáciami a modulmi.</span><span class="sxs-lookup"><span data-stu-id="04368-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="04368-110">Keď sa pozrieme ešte ďalej na špecifiká, kategórie projektov sú najpodrobnejšou úrovňou kategórií.</span><span class="sxs-lookup"><span data-stu-id="04368-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="04368-111">Kategórie projektov sú špecifické pre právnické osoby, moduly a aplikácie.</span><span class="sxs-lookup"><span data-stu-id="04368-111">Project categories are specific to legal entity, module, and application.</span></span>

![Korelácia medzi kategóriami transakcií, zdieľanými kategóriami a kategóriami projektu](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="04368-113">Kategórie transakcií</span><span class="sxs-lookup"><span data-stu-id="04368-113">Transaction categories</span></span>

<span data-ttu-id="04368-114">Kategórie transakcií predstavujú základné zoskupenie pre projektové transakcie a nie sú špecifické pre spoločnosť alebo typ transakcie.</span><span class="sxs-lookup"><span data-stu-id="04368-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="04368-115">Spoločnosť Contoso Robotics napríklad používa na zoskupenie transakcií projektu kategórie Dizajn, Cestovanie, Inštalácia a Transakcie služieb.</span><span class="sxs-lookup"><span data-stu-id="04368-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="04368-116">Kategórie transakcií sú definované v module Project Operations.</span><span class="sxs-lookup"><span data-stu-id="04368-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="04368-117">Prejdite do **Nastavenia** \> **Kategórie transakcií** na otvorenie formulára.</span><span class="sxs-lookup"><span data-stu-id="04368-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="04368-118">Vytvorte novú kategóriu transakcií výberom možnosti **Nová** alebo výberom možnosti **Import z programu Excel**.</span><span class="sxs-lookup"><span data-stu-id="04368-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="04368-119">Zdieľané kategórie</span><span class="sxs-lookup"><span data-stu-id="04368-119">Shared categories</span></span>

<span data-ttu-id="04368-120">Dynamics 365 používa koncept zdieľaných kategórií na kategorizáciu výdavkov v rôznych aplikáciách, ako napr. Dynamics 365 Finance, Dynamics 365 Supply Chain a Dynamics 365 Project Operations.</span><span class="sxs-lookup"><span data-stu-id="04368-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="04368-121">Pre každú vytvorenú kategóriu transakcií Project Operations automaticky vytvorí štyri súvisiace zdieľané kategórie: Hodiny, Výdavok, Poplatky a Položka.</span><span class="sxs-lookup"><span data-stu-id="04368-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="04368-122">Zdieľané kategórie môžete skontrolovať a upraviť v časti **Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Kategórie** \> **Zdieľané kategórie**.</span><span class="sxs-lookup"><span data-stu-id="04368-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="04368-123">Kategórie projektov</span><span class="sxs-lookup"><span data-stu-id="04368-123">Project categories</span></span>

<span data-ttu-id="04368-124">Kategórie projektu predstavujú najpodrobnejšiu úroveň konfigurácie kategórií a musia byť nakonfigurované osobitne a pre každú spoločnosť účtovníkom projektu.</span><span class="sxs-lookup"><span data-stu-id="04368-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="04368-125">Prejdite do **Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Kategórie** \> **Kategórie projektov**.</span><span class="sxs-lookup"><span data-stu-id="04368-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="04368-126">Vyberte **Nové**.</span><span class="sxs-lookup"><span data-stu-id="04368-126">Select **New**.</span></span>
3. <span data-ttu-id="04368-127">Vyberte možnosť **ID kategórie** zdieľanej kategórie, ktorú ste vytvorili v predchádzajúcej časti.</span><span class="sxs-lookup"><span data-stu-id="04368-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="04368-128">Project Operations umožňuje používať iba tie zdieľané kategórie, ktoré sú spojené s kategóriami transakcií.</span><span class="sxs-lookup"><span data-stu-id="04368-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="04368-129">Vyberte skupinu kategórií.</span><span class="sxs-lookup"><span data-stu-id="04368-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="04368-130">Skupiny kategórií</span><span class="sxs-lookup"><span data-stu-id="04368-130">Category groups</span></span>

<span data-ttu-id="04368-131">Skupiny kategórií sa používajú na zdieľanie vlastností, predovšetkým odosielanie profilov medzi súvisiacimi kategóriami projektu.</span><span class="sxs-lookup"><span data-stu-id="04368-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="04368-132">Pre každý typ transakcie musí existovať najmenej jedna skupina kategórií a každej kategórii projektu je priradená skupina.</span><span class="sxs-lookup"><span data-stu-id="04368-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="04368-133">Špecifikácie účtovania v Project Operations sú definované pravidlami profilu nákladov a výnosov projektu, kategóriami projektov a skupinami kategórií.</span><span class="sxs-lookup"><span data-stu-id="04368-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="04368-134">Skupiny kategórií môžete nastaviť tak, že prejdete na **Riadenie projektu a účtovníctvo** \> **Nastaviť** \> **Kategórie** \> **Skupiny kategórií**.</span><span class="sxs-lookup"><span data-stu-id="04368-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>
