---
title: Prehľad výdavkov
description: Táto téma poskytuje informácie o funkcii Výdavok v Project Operations.
author: stsporen
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: stsporen
ms.custom: intro-internal
ms.openlocfilehash: 921df6fa8f1eb33bd01792c0b7c787fc74604adf
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368585"
---
# <a name="expense-home-page"></a><span data-ttu-id="d959d-103">Domovská stránka výdavkov</span><span class="sxs-lookup"><span data-stu-id="d959d-103">Expense home page</span></span>

<span data-ttu-id="d959d-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="d959d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="d959d-105">Dynamics 365 Project Operations podporuje schopnosť spracovávať výdavky.</span><span class="sxs-lookup"><span data-stu-id="d959d-105">Dynamics 365 Project Operations supports the ability to process expenses.</span></span> <span data-ttu-id="d959d-106">Spracovanie výdavkov sa vykonáva s projektmi alebo bez nich pomocou prispôsobiteľného pracovného postupu politík, kategórií transakcií a schválení.</span><span class="sxs-lookup"><span data-stu-id="d959d-106">Expense processing occurs with or without projects by using a customizable workflow of policies, transaction categories, and approvals.</span></span>

<span data-ttu-id="d959d-107">V Project Operations existujú dva podporované modely nasadenia pre výdavok:</span><span class="sxs-lookup"><span data-stu-id="d959d-107">In Project Operations, there are two supported deployment models for Expense:</span></span> 

- <span data-ttu-id="d959d-108">**Plné**: Plné nasadenie je k dispozícii pre **Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch** alebo **Project Operations pre scenáre založené na výrobných zákazkách**.</span><span class="sxs-lookup"><span data-stu-id="d959d-108">**Full**: Full deployment is available for **Project Operations for resource/non-stocked based scenarios** or **Project Operations for production order-based scenarios**.</span></span>
- <span data-ttu-id="d959d-109">**Základné**: Základné nasadenie je k dispozícii pre **Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch** a **Čiastočné nasadenie – dohoda o fakturácii pro forma**.</span><span class="sxs-lookup"><span data-stu-id="d959d-109">**Basic**: Basic deployment is available for **Project Operations for resource/non-stocked based scenarios** and **Lite deployment – deal to proforma invoicing**.</span></span>

## <a name="full"></a><span data-ttu-id="d959d-110">Úplný</span><span class="sxs-lookup"><span data-stu-id="d959d-110">Full</span></span> 
<span data-ttu-id="d959d-111">Plné nasadenie výdavkov poskytuje úplné vynútenie politiky, ktoré zahŕňa schopnosť vytvárať politiky, napríklad:</span><span class="sxs-lookup"><span data-stu-id="d959d-111">Full Expense deployment provides a complete policy enforcement that includes the ability to create policies, such as:</span></span>

  - <span data-ttu-id="d959d-112">Limity kategóriu výdavku</span><span class="sxs-lookup"><span data-stu-id="d959d-112">Expense category limits</span></span>
  - <span data-ttu-id="d959d-113">Cesta</span><span class="sxs-lookup"><span data-stu-id="d959d-113">Travel</span></span>
  - <span data-ttu-id="d959d-114">Denne</span><span class="sxs-lookup"><span data-stu-id="d959d-114">Per diem</span></span>
  - <span data-ttu-id="d959d-115">Importy kreditnej karty</span><span class="sxs-lookup"><span data-stu-id="d959d-115">Credit card imports</span></span>
  - <span data-ttu-id="d959d-116">Príjem optického rozpoznávania znakov</span><span class="sxs-lookup"><span data-stu-id="d959d-116">Receipt optical character recognition</span></span>

## <a name="basic"></a><span data-ttu-id="d959d-117">Základná</span><span class="sxs-lookup"><span data-stu-id="d959d-117">Basic</span></span> 
<span data-ttu-id="d959d-118">Scenár nasadenia základných výdavkov vám umožňuje zaznamenať iba základné výdavky oproti projektu.</span><span class="sxs-lookup"><span data-stu-id="d959d-118">Basic Expense deployment scenario only allows you to record basic expenses against a project.</span></span> 

<span data-ttu-id="d959d-119">Ďalšie informácie nájdete v časti [Záznam o výdavku (čiastočný)](basic-expense.md)</span><span class="sxs-lookup"><span data-stu-id="d959d-119">For more information, see [Expense entry (lite)](basic-expense.md)</span></span>

## <a name="determine-your-expense-deployment"></a><span data-ttu-id="d959d-120">Určenie nasadenia výdavkov</span><span class="sxs-lookup"><span data-stu-id="d959d-120">Determine your Expense deployment</span></span>
<span data-ttu-id="d959d-121">Ak chcete zistiť, či používate nasadenie správy základných výdavkov, skontrolujte, či sa adresa URL končí **.crm.dynamics.com**.</span><span class="sxs-lookup"><span data-stu-id="d959d-121">To determine if you're running the Basic Expense management deployment, verify that the address URL ends with **.crm.dynamics.com**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]