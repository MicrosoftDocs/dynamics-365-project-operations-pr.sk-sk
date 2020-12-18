---
title: Prehľad priznania výnosov
description: Táto téma poskytuje informácie o priznaní výnosov v aplikácii Project Operations.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6844f4c5d4cda8a6a901b0302448f70f4c597f5d
ms.sourcegitcommit: 2d399bc9d07807626f0d6b2d0cf304240c47591c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 11/17/2020
ms.locfileid: "4531548"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="87aa5-103">Prehľad priznania výnosov</span><span class="sxs-lookup"><span data-stu-id="87aa5-103">Revenue recognition overview</span></span>

<span data-ttu-id="87aa5-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="87aa5-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="87aa5-105">V Dynamics 365 Project Operations sa princípy priznania výnosov líšia v závislosti od zvolenej metódy fakturácie pre projekt alebo časť projektu.</span><span class="sxs-lookup"><span data-stu-id="87aa5-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="87aa5-106">Táto téma poskytuje informácie o priznaní výnosov v aplikácii Project Operations.</span><span class="sxs-lookup"><span data-stu-id="87aa5-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="87aa5-107">Transakcie účtované použitím spôsobu fakturácie času a materiálu</span><span class="sxs-lookup"><span data-stu-id="87aa5-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="87aa5-108">Priznanie nákladov a výnosov je prepojené.</span><span class="sxs-lookup"><span data-stu-id="87aa5-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="87aa5-109">Transakčné náklady a nefakturované predaje sa zaúčtujú pomocou [Denník integrácie Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="87aa5-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="87aa5-110">Profil nákladov a výnosov projektu určuje, či sa nevyfakturované predajné transakcie zaúčtujú do hlavnej účtovnej knihy.</span><span class="sxs-lookup"><span data-stu-id="87aa5-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="87aa5-111">Ak je vybraná možnosť **Prírastok príjmu**, systém používa pri zaúčtovaní účty **Hodnota predaja WIP** a **Hodnota prírastkov predajných výnosov**.</span><span class="sxs-lookup"><span data-stu-id="87aa5-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="87aa5-112">Nasleduje príklad tejto metódy.</span><span class="sxs-lookup"><span data-stu-id="87aa5-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="87aa5-113">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="87aa5-113">Transaction type</span></span> | <span data-ttu-id="87aa5-114">Debet/Kredit</span><span class="sxs-lookup"><span data-stu-id="87aa5-114">Debit/Credit</span></span> | <span data-ttu-id="87aa5-115">Množstvo</span><span class="sxs-lookup"><span data-stu-id="87aa5-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="87aa5-116">Hodnota predaja WIP</span><span class="sxs-lookup"><span data-stu-id="87aa5-116">WIP Sales value</span></span> | <span data-ttu-id="87aa5-117">Debet</span><span class="sxs-lookup"><span data-stu-id="87aa5-117">Debit</span></span> | <span data-ttu-id="87aa5-118">100</span><span class="sxs-lookup"><span data-stu-id="87aa5-118">100</span></span> |
  | <span data-ttu-id="87aa5-119">Hodnota prírastkov predajných výnosov</span><span class="sxs-lookup"><span data-stu-id="87aa5-119">Accrued revenue sales value</span></span> | <span data-ttu-id="87aa5-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="87aa5-120">Credit</span></span> | <span data-ttu-id="87aa5-121">100</span><span class="sxs-lookup"><span data-stu-id="87aa5-121">100</span></span> |

- <span data-ttu-id="87aa5-122">Výnos sa rozpoznáva počas fakturácie.</span><span class="sxs-lookup"><span data-stu-id="87aa5-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="87aa5-123">Systém používa účet **Fakturovaný výnos** počas zaúčtovania.</span><span class="sxs-lookup"><span data-stu-id="87aa5-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="87aa5-124">Nasleduje príklad tejto metódy.</span><span class="sxs-lookup"><span data-stu-id="87aa5-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="87aa5-125">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="87aa5-125">Transaction type</span></span> | <span data-ttu-id="87aa5-126">Debet/Kredit</span><span class="sxs-lookup"><span data-stu-id="87aa5-126">Debit/Credit</span></span> | <span data-ttu-id="87aa5-127">Množstvo</span><span class="sxs-lookup"><span data-stu-id="87aa5-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="87aa5-128">Zostatok zákazníka</span><span class="sxs-lookup"><span data-stu-id="87aa5-128">Customer balance</span></span> | <span data-ttu-id="87aa5-129">Debet</span><span class="sxs-lookup"><span data-stu-id="87aa5-129">Debit</span></span> | <span data-ttu-id="87aa5-130">120</span><span class="sxs-lookup"><span data-stu-id="87aa5-130">120</span></span> |
  | <span data-ttu-id="87aa5-131">Splatná daň z predaja</span><span class="sxs-lookup"><span data-stu-id="87aa5-131">Sales tax payable</span></span> | <span data-ttu-id="87aa5-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="87aa5-132">Credit</span></span> | <span data-ttu-id="87aa5-133">20</span><span class="sxs-lookup"><span data-stu-id="87aa5-133">20</span></span> |
  | <span data-ttu-id="87aa5-134">Fakturovaný výnos</span><span class="sxs-lookup"><span data-stu-id="87aa5-134">Invoiced Revenue</span></span> | <span data-ttu-id="87aa5-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="87aa5-135">Credit</span></span> | <span data-ttu-id="87aa5-136">100</span><span class="sxs-lookup"><span data-stu-id="87aa5-136">100</span></span> |

- <span data-ttu-id="87aa5-137">Ak bol výnos zhromaždený pri zaúčtovaní nevyfakturovaných predajov, systém tieto zhromaždené výnosy pri fakturácii vráti späť.</span><span class="sxs-lookup"><span data-stu-id="87aa5-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="87aa5-138">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="87aa5-138">Transaction type</span></span> | <span data-ttu-id="87aa5-139">Debet/Kredit</span><span class="sxs-lookup"><span data-stu-id="87aa5-139">Debit/Credit</span></span> | <span data-ttu-id="87aa5-140">Množstvo</span><span class="sxs-lookup"><span data-stu-id="87aa5-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="87aa5-141">Hodnota predaja WIP</span><span class="sxs-lookup"><span data-stu-id="87aa5-141">WIP Sales value</span></span> | <span data-ttu-id="87aa5-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="87aa5-142">Credit</span></span> | <span data-ttu-id="87aa5-143">100</span><span class="sxs-lookup"><span data-stu-id="87aa5-143">100</span></span> |
  | <span data-ttu-id="87aa5-144">Hodnota prírastkov predajných výnosov</span><span class="sxs-lookup"><span data-stu-id="87aa5-144">Accrued revenue sales value</span></span> | <span data-ttu-id="87aa5-145">Debet</span><span class="sxs-lookup"><span data-stu-id="87aa5-145">Debit</span></span> | <span data-ttu-id="87aa5-146">100</span><span class="sxs-lookup"><span data-stu-id="87aa5-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="87aa5-147">Transakcie účtované použitím spôsobu fakturácie pevnej ceny</span><span class="sxs-lookup"><span data-stu-id="87aa5-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="87aa5-148">Priznanie nákladov a výnosov je oddelené.</span><span class="sxs-lookup"><span data-stu-id="87aa5-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="87aa5-149">Transakčné náklady sa zaúčtujú pomocou [Denníka integrácie Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="87aa5-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="87aa5-150">Nevyfakturované predajné transakcie sa nevytvárajú.</span><span class="sxs-lookup"><span data-stu-id="87aa5-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="87aa5-151">Výnosy môžu byť uznané počas fakturácie, ak majú projektové náklady a profil výnosov **Zásadu použitú pri výpočtoch dokončenia projektu** nastavenú na **Žiadne WIP**.</span><span class="sxs-lookup"><span data-stu-id="87aa5-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="87aa5-152">Túto metódu používajte iba na krátkodobé jednoduché projekty.</span><span class="sxs-lookup"><span data-stu-id="87aa5-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="87aa5-153">Výnosy možno vykázať pomocou odhadov výnosov s pevnou cenou, buď metódou **Dokončená zmluva** alebo **Vykázanie percentuálneho vykázania výnosov**.</span><span class="sxs-lookup"><span data-stu-id="87aa5-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87aa5-154">Ďalšie zdroje</span><span class="sxs-lookup"><span data-stu-id="87aa5-154">Additional resources</span></span>
[<span data-ttu-id="87aa5-155">Článok Konfigurácia účtovníctva pre fakturovateľné projekty</span><span class="sxs-lookup"><span data-stu-id="87aa5-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="87aa5-156">Projekty odhadov výnosov s pevnou cenou</span><span class="sxs-lookup"><span data-stu-id="87aa5-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="87aa5-157">Správa odhadov výnosov</span><span class="sxs-lookup"><span data-stu-id="87aa5-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="87aa5-158">Náklady na dokončenie metód</span><span class="sxs-lookup"><span data-stu-id="87aa5-158">Cost to complete methods</span></span>](cost-complete-methods.md)
