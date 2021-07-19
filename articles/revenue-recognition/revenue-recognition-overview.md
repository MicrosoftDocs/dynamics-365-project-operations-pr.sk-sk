---
title: Prehľad priznania výnosov
description: Táto téma poskytuje informácie o priznaní výnosov v aplikácii Project Operations.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: ab9b36b71223b1bcfe48de5f9b68b6fb6a98f388
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368045"
---
# <a name="revenue-recognition-overview"></a><span data-ttu-id="867d2-103">Prehľad priznania výnosov</span><span class="sxs-lookup"><span data-stu-id="867d2-103">Revenue recognition overview</span></span>

<span data-ttu-id="867d2-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="867d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="867d2-105">V Dynamics 365 Project Operations sa princípy priznania výnosov líšia v závislosti od zvolenej metódy fakturácie pre projekt alebo časť projektu.</span><span class="sxs-lookup"><span data-stu-id="867d2-105">In Dynamics 365 Project Operations, revenue recognition principles vary based on the selected billing method for a project or portion of the project.</span></span> <span data-ttu-id="867d2-106">Táto téma poskytuje informácie o priznaní výnosov v aplikácii Project Operations.</span><span class="sxs-lookup"><span data-stu-id="867d2-106">This topic provides information about revenue recognition in Project Operations.</span></span>

## <a name="transactions-accounted-using-time-and-material-billing-method"></a><span data-ttu-id="867d2-107">Transakcie účtované použitím spôsobu fakturácie času a materiálu</span><span class="sxs-lookup"><span data-stu-id="867d2-107">Transactions accounted using time and material billing method</span></span>

- <span data-ttu-id="867d2-108">Priznanie nákladov a výnosov je prepojené.</span><span class="sxs-lookup"><span data-stu-id="867d2-108">Cost and revenue recognition are connected.</span></span> <span data-ttu-id="867d2-109">Transakčné náklady a nefakturované predaje sa zaúčtujú pomocou [Denník integrácie Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="867d2-109">Transaction cost and unbilled sales are posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span>
- <span data-ttu-id="867d2-110">Profil nákladov a výnosov projektu určuje, či sa nevyfakturované predajné transakcie zaúčtujú do hlavnej účtovnej knihy.</span><span class="sxs-lookup"><span data-stu-id="867d2-110">Project cost and revenue profile determine if unbilled sales transactions are posted to the general ledger.</span></span> <span data-ttu-id="867d2-111">Ak je vybraná možnosť **Prírastok príjmu**, systém používa pri zaúčtovaní účty **Hodnota predaja WIP** a **Hodnota prírastkov predajných výnosov**.</span><span class="sxs-lookup"><span data-stu-id="867d2-111">If **Accrue revenue** is selected, the system uses the **WIP sales value** and the **Accrued revenue sales value** accounts during posting.</span></span> <span data-ttu-id="867d2-112">Nasleduje príklad tejto metódy.</span><span class="sxs-lookup"><span data-stu-id="867d2-112">The following is an example of this method.</span></span>  

  | <span data-ttu-id="867d2-113">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="867d2-113">Transaction type</span></span> | <span data-ttu-id="867d2-114">Debet/Kredit</span><span class="sxs-lookup"><span data-stu-id="867d2-114">Debit/Credit</span></span> | <span data-ttu-id="867d2-115">Množstvo</span><span class="sxs-lookup"><span data-stu-id="867d2-115">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="867d2-116">Hodnota predaja WIP</span><span class="sxs-lookup"><span data-stu-id="867d2-116">WIP Sales value</span></span> | <span data-ttu-id="867d2-117">Debet</span><span class="sxs-lookup"><span data-stu-id="867d2-117">Debit</span></span> | <span data-ttu-id="867d2-118">100</span><span class="sxs-lookup"><span data-stu-id="867d2-118">100</span></span> |
  | <span data-ttu-id="867d2-119">Hodnota prírastkov predajných výnosov</span><span class="sxs-lookup"><span data-stu-id="867d2-119">Accrued revenue sales value</span></span> | <span data-ttu-id="867d2-120">Kredit</span><span class="sxs-lookup"><span data-stu-id="867d2-120">Credit</span></span> | <span data-ttu-id="867d2-121">100</span><span class="sxs-lookup"><span data-stu-id="867d2-121">100</span></span> |

- <span data-ttu-id="867d2-122">Výnos sa rozpoznáva počas fakturácie.</span><span class="sxs-lookup"><span data-stu-id="867d2-122">Revenue is recognized during invoicing.</span></span> <span data-ttu-id="867d2-123">Systém používa účet **Fakturovaný výnos** počas zaúčtovania.</span><span class="sxs-lookup"><span data-stu-id="867d2-123">The system uses the **Invoiced revenue** account during posting.</span></span> <span data-ttu-id="867d2-124">Nasleduje príklad tejto metódy.</span><span class="sxs-lookup"><span data-stu-id="867d2-124">The following is an example of this method.</span></span>  

  | <span data-ttu-id="867d2-125">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="867d2-125">Transaction type</span></span> | <span data-ttu-id="867d2-126">Debet/Kredit</span><span class="sxs-lookup"><span data-stu-id="867d2-126">Debit/Credit</span></span> | <span data-ttu-id="867d2-127">Množstvo</span><span class="sxs-lookup"><span data-stu-id="867d2-127">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="867d2-128">Zostatok zákazníka</span><span class="sxs-lookup"><span data-stu-id="867d2-128">Customer balance</span></span> | <span data-ttu-id="867d2-129">Debet</span><span class="sxs-lookup"><span data-stu-id="867d2-129">Debit</span></span> | <span data-ttu-id="867d2-130">120</span><span class="sxs-lookup"><span data-stu-id="867d2-130">120</span></span> |
  | <span data-ttu-id="867d2-131">Splatná daň z predaja</span><span class="sxs-lookup"><span data-stu-id="867d2-131">Sales tax payable</span></span> | <span data-ttu-id="867d2-132">Kredit</span><span class="sxs-lookup"><span data-stu-id="867d2-132">Credit</span></span> | <span data-ttu-id="867d2-133">20</span><span class="sxs-lookup"><span data-stu-id="867d2-133">20</span></span> |
  | <span data-ttu-id="867d2-134">Fakturovaný výnos</span><span class="sxs-lookup"><span data-stu-id="867d2-134">Invoiced Revenue</span></span> | <span data-ttu-id="867d2-135">Kredit</span><span class="sxs-lookup"><span data-stu-id="867d2-135">Credit</span></span> | <span data-ttu-id="867d2-136">100</span><span class="sxs-lookup"><span data-stu-id="867d2-136">100</span></span> |

- <span data-ttu-id="867d2-137">Ak bol výnos zhromaždený pri zaúčtovaní nevyfakturovaných predajov, systém tieto zhromaždené výnosy pri fakturácii vráti späť.</span><span class="sxs-lookup"><span data-stu-id="867d2-137">If revenue was accrued when the unbilled sales are posted, the system will reverse the accrued revenue at invoicing.</span></span>

  | <span data-ttu-id="867d2-138">Typ transakcie</span><span class="sxs-lookup"><span data-stu-id="867d2-138">Transaction type</span></span> | <span data-ttu-id="867d2-139">Debet/Kredit</span><span class="sxs-lookup"><span data-stu-id="867d2-139">Debit/Credit</span></span> | <span data-ttu-id="867d2-140">Množstvo</span><span class="sxs-lookup"><span data-stu-id="867d2-140">Amount</span></span> |
  | --- | --- | --- |
  | <span data-ttu-id="867d2-141">Hodnota predaja WIP</span><span class="sxs-lookup"><span data-stu-id="867d2-141">WIP Sales value</span></span> | <span data-ttu-id="867d2-142">Kredit</span><span class="sxs-lookup"><span data-stu-id="867d2-142">Credit</span></span> | <span data-ttu-id="867d2-143">100</span><span class="sxs-lookup"><span data-stu-id="867d2-143">100</span></span> |
  | <span data-ttu-id="867d2-144">Hodnota prírastkov predajných výnosov</span><span class="sxs-lookup"><span data-stu-id="867d2-144">Accrued revenue sales value</span></span> | <span data-ttu-id="867d2-145">Debet</span><span class="sxs-lookup"><span data-stu-id="867d2-145">Debit</span></span> | <span data-ttu-id="867d2-146">100</span><span class="sxs-lookup"><span data-stu-id="867d2-146">100</span></span> |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a><span data-ttu-id="867d2-147">Transakcie účtované použitím spôsobu fakturácie pevnej ceny</span><span class="sxs-lookup"><span data-stu-id="867d2-147">Transactions accounted using the fixed price billing method</span></span>

- <span data-ttu-id="867d2-148">Priznanie nákladov a výnosov je oddelené.</span><span class="sxs-lookup"><span data-stu-id="867d2-148">Cost and revenue recognition are separate.</span></span> <span data-ttu-id="867d2-149">Transakčné náklady sa zaúčtujú pomocou [Denníka integrácie Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="867d2-149">Transaction cost is posted using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="867d2-150">Nevyfakturované predajné transakcie sa nevytvárajú.</span><span class="sxs-lookup"><span data-stu-id="867d2-150">Unbilled sales transactions aren't created.</span></span>
- <span data-ttu-id="867d2-151">Výnosy môžu byť uznané počas fakturácie, ak majú projektové náklady a profil výnosov **Zásadu použitú pri výpočtoch dokončenia projektu** nastavenú na **Žiadne WIP**.</span><span class="sxs-lookup"><span data-stu-id="867d2-151">Revenue can be recognized during invoicing if the project cost and revenue profile have **Principle used for project completion calculations** set to **No WIP**.</span></span> <span data-ttu-id="867d2-152">Túto metódu používajte iba na krátkodobé jednoduché projekty.</span><span class="sxs-lookup"><span data-stu-id="867d2-152">Only use this method for short term, simple projects.</span></span>
- <span data-ttu-id="867d2-153">Výnosy možno vykázať pomocou odhadov výnosov s pevnou cenou, buď metódou **Dokončená zmluva** alebo **Vykázanie percentuálneho vykázania výnosov**.</span><span class="sxs-lookup"><span data-stu-id="867d2-153">Revenue can be recognized using fixed price revenue estimates, with either the **Completed contract** or **Percent completion revenue recognition** method.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="867d2-154">Ďalšie zdroje</span><span class="sxs-lookup"><span data-stu-id="867d2-154">Additional resources</span></span>
[<span data-ttu-id="867d2-155">Článok Konfigurácia účtovníctva pre fakturovateľné projekty</span><span class="sxs-lookup"><span data-stu-id="867d2-155">Configure accounting for billable projects article</span></span>](../project-accounting/configure-accounting-billable-projects.md)

[<span data-ttu-id="867d2-156">Projekty odhadov výnosov s pevnou cenou</span><span class="sxs-lookup"><span data-stu-id="867d2-156">Fixed price revenue estimate projects</span></span>](rev-rec-percentage-completion-method.md)

[<span data-ttu-id="867d2-157">Správa odhadov výnosov</span><span class="sxs-lookup"><span data-stu-id="867d2-157">Manage revenue estimates</span></span>](rev-rec-completed-contract-method.md)

[<span data-ttu-id="867d2-158">Náklady na dokončenie metód</span><span class="sxs-lookup"><span data-stu-id="867d2-158">Cost to complete methods</span></span>](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]