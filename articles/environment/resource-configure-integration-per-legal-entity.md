---
title: Konfigurácia integrácie Project Operations pre každú právnickú osobu
description: Táto téma poskytuje informácie o nastavení a integrácie podľa právnickej osoby v Project Operations.
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000095"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="fe2d2-103">Konfigurácia integrácie Project Operations pre každú právnickú osobu</span><span class="sxs-lookup"><span data-stu-id="fe2d2-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="fe2d2-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="fe2d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fe2d2-105">Táto téma vás prevedie krokmi potrebnými na konfiguráciu aplikácie Dynamics 365 Project Operations pre právnickú osobu.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="fe2d2-106">Aktivácia funkčných klávesov v Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="fe2d2-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="fe2d2-107">Vykonaním nasledujúcich krokov povolíte požadované funkcie.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="fe2d2-108">V Dynamics 365 Finance prejdite na pracovný priestor **Správa funkcií**.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="fe2d2-109">V časti **Zoznam funkcií**, vyhľadajte a povoľte nasledujúce funkcie:</span><span class="sxs-lookup"><span data-stu-id="fe2d2-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="fe2d2-110">**Povoliť pre projekt viac riadkov zmluvy**</span><span class="sxs-lookup"><span data-stu-id="fe2d2-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="fe2d2-111">**Aktivácia Project Operations v Dynamics 365 Customer Engagement**</span><span class="sxs-lookup"><span data-stu-id="fe2d2-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="fe2d2-112">Ak nevidíte uvedené **Funkčné klávesy**, overte, či vaša verzia Finance spĺňa požiadavku na minimálnu verziu (verzia aplikácie 10.0.13 s použitými všetkými aktualizáciami kvality alebo vyššími verziami).</span><span class="sxs-lookup"><span data-stu-id="fe2d2-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="fe2d2-113">Stlačte možnosť **Skontrolovať aktualizácie** na obnovenie zoznamu funkcií.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="fe2d2-114">Definujte scenár nasadenia Project Operations pre právnickú osobu</span><span class="sxs-lookup"><span data-stu-id="fe2d2-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="fe2d2-115">Môžete povoliť Project Operations v Dynamics 365 Customer Engagement na úrovni právnickej osoby.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="fe2d2-116">Môžete mať jeden právny subjekt, ktorý používa Project Operations v Dynamics 365 Customer Engagement pre scenáre založené na zdrojoch/neinventárne scenáre.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="fe2d2-117">V rovnakom prostredí môžete mať inú právnickú osobu, ktorá používa Project Operations pre scenáre skladovaných/výrobných zákaziek.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="fe2d2-118">V Dynamics 365 Finance prejdite na **Projektové riadenie a účtovníctvo** > **Nastaviť** > **Globálne parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="fe2d2-119">V zozname dostupných právnych osôb vyberte subjekty, na ktorých je zapnutých viac riadkov zmlúv a dôjde k aktivácii funkcií Project Operations v Dynamics 365 Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="fe2d2-120">Právnické osoby, ktoré budú používať operácie projektu pre scenáre skladovania/výrobnej objednávky, nechajte nevybrané.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="fe2d2-121">Právnickú osobu je možné vybrať, iba ak nemá žiadne existujúce projekty.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="fe2d2-122">Konfigurácia parametrov riadenia projektu a účtovníctva</span><span class="sxs-lookup"><span data-stu-id="fe2d2-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="fe2d2-123">Každá právnická osoba využívajúca Project Operations v Dynamics 365 Customer Engagement potrebuje množinu predvolených parametrov.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="fe2d2-124">Tieto parametre sú konfigurované na karte **Project Operations** na stránke **Parametre projektového riadenia a účtovníctva**.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="fe2d2-125">Uvedené parametre sú:</span><span class="sxs-lookup"><span data-stu-id="fe2d2-125">The parameters are:</span></span>

  - <span data-ttu-id="fe2d2-126">**Predvolené typy fakturácie**: Project Operations používa pevnú množinu predvolených typov fakturácie, ktorú je potrebné namapovať na vlastnosti riadkov Finance.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="fe2d2-127">Vytvorte záznam pre každý typ fakturácie: **Nešpecifikované**, **Spoplatnené**, **Nedá sa spoplatniť**, **Bezplatné** a **Nie je k dispozícií**.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="fe2d2-128">**Predvolené hodnoty kategórie projektu**: Vyberte predvolené kategórie projektu, ktoré sa majú použiť pre každý typ transakcie.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="fe2d2-129">Tieto predvolené hodnoty sa použijú v **Denníku integrácie Project Operations** a v odhadoch, kde nie je špecifikovaná žiadna kategória transakcií pre skutočný projekt.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="fe2d2-130">**Prognózy**: Vyberte predpovedný model, ktorý sa použije pre odhady času a výdavkov.</span><span class="sxs-lookup"><span data-stu-id="fe2d2-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]