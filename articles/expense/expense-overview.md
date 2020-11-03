---
title: Prehľad výdavkov
description: Táto téma poskytuje informácie o funkcii Výdavok v Project Operations.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 6da831fef5dba060b8019d7689645405c7ebdbed
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084244"
---
# <a name="expense-home-page"></a><span data-ttu-id="2586b-103">Domovská stránka výdavkov</span><span class="sxs-lookup"><span data-stu-id="2586b-103">Expense home page</span></span>

<span data-ttu-id="2586b-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="2586b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2586b-105">Dynamics 365 Project Operations podporuje možnosť spracovávania výdavkov.</span><span class="sxs-lookup"><span data-stu-id="2586b-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="2586b-106">Spracovanie výdavkov sa vykonáva s projektmi alebo bez nich pomocou prispôsobiteľného pracovného postupu politík, kategórií transakcií a schválení.</span><span class="sxs-lookup"><span data-stu-id="2586b-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="2586b-107">V Project Operations existujú dva podporované modely nasadenia pre výdavok:</span><span class="sxs-lookup"><span data-stu-id="2586b-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="2586b-108">**Plné** : Plné nasadenie je k dispozícii pre **Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch** alebo **Project Operations pre scenáre založené na výrobných zákazkách**.</span><span class="sxs-lookup"><span data-stu-id="2586b-108">**Full** : Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order based scenarios**.</span></span>
- <span data-ttu-id="2586b-109">**Základné** : Základné nasadenie je k dispozícii pre **Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch** a **Čiastočné nasadenie – dohoda o fakturácii pro forma**.</span><span class="sxs-lookup"><span data-stu-id="2586b-109">**Basic** : Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="2586b-110">Úplný</span><span class="sxs-lookup"><span data-stu-id="2586b-110">Full</span></span> 
<span data-ttu-id="2586b-111">Nasadenie plných výdavkov poskytuje kompletné vynútenie politiky, ktoré zahŕňa schopnosť vytvárať politiky, ako napríklad:</span><span class="sxs-lookup"><span data-stu-id="2586b-111">Full Expense deployment provides a complete policy enforcement which includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="2586b-112">Limity kategóriu výdavku</span><span class="sxs-lookup"><span data-stu-id="2586b-112">Expense category limits</span></span>
  - <span data-ttu-id="2586b-113">Cesta</span><span class="sxs-lookup"><span data-stu-id="2586b-113">Travel</span></span>
  - <span data-ttu-id="2586b-114">Denne</span><span class="sxs-lookup"><span data-stu-id="2586b-114">Per diem</span></span>
  - <span data-ttu-id="2586b-115">Importy kreditnej karty</span><span class="sxs-lookup"><span data-stu-id="2586b-115">Credit card imports</span></span>
  - <span data-ttu-id="2586b-116">Príjem optického rozpoznávania znakov</span><span class="sxs-lookup"><span data-stu-id="2586b-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="2586b-117">Základná</span><span class="sxs-lookup"><span data-stu-id="2586b-117">Basic</span></span> 
<span data-ttu-id="2586b-118">Scenár nasadenia základných výdavkov vám umožňuje zaznamenať iba základné výdavky oproti projektu.</span><span class="sxs-lookup"><span data-stu-id="2586b-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="2586b-119">Ďalšie informácie nájdete v časti [Záznam o výdavku (čiastočný)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="2586b-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="2586b-120">Určenie nasadenia výdavkov</span><span class="sxs-lookup"><span data-stu-id="2586b-120">Determine your Expense deployment</span></span>
<span data-ttu-id="2586b-121">Ak chcete zistiť, či používate nasadenie správy základných výdavkov, skontrolujte, či sa adresa URL končí **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="2586b-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 
