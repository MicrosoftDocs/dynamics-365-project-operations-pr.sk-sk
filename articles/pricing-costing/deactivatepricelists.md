---
title: Deaktivácia cenníkov
description: Táto téma vysvetľuje, ako deaktivovať alebo odstrániť nepoužívané alebo staré cenníky.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701972"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="1143a-103">Deaktivácia cenníkov</span><span class="sxs-lookup"><span data-stu-id="1143a-103">Deactivate price lists</span></span> 

<span data-ttu-id="1143a-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="1143a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1143a-105">Ak chcete odstrániť staré alebo nepoužívané cenníky z Dynamics 365 Project Operations, musíte vykonať dva kroky.</span><span class="sxs-lookup"><span data-stu-id="1143a-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="1143a-106">Odstráňte alebo vymažte cenník z konkrétnych stránok.</span><span class="sxs-lookup"><span data-stu-id="1143a-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="1143a-107">Cenník deaktivujte alebo odstráňte z aktívnych cenníkov na stránke **Cenníky**.</span><span class="sxs-lookup"><span data-stu-id="1143a-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="1143a-108">Na úplné odstránenie cenníka musíte dokončiť obidva kroky.</span><span class="sxs-lookup"><span data-stu-id="1143a-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="1143a-109">Nestačí iba vykonanie kroku 2, ktorým je priame odstránenie alebo deaktivácia cenníka zo zobrazenia Aktívne cenníky.</span><span class="sxs-lookup"><span data-stu-id="1143a-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="1143a-110">Musíte tiež odstrániť priradenie tohto cenníka zo všetkých miest uvedených v kroku 1.</span><span class="sxs-lookup"><span data-stu-id="1143a-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="1143a-111">Odstránenie cenníka z konkrétnych stránok</span><span class="sxs-lookup"><span data-stu-id="1143a-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="1143a-112">Ak chcete odstrániť cenník z Project Operations, choďte na nasledujúce stránky:</span><span class="sxs-lookup"><span data-stu-id="1143a-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="1143a-113">Stránka **Parametre projektu** > karta **Cenníky**</span><span class="sxs-lookup"><span data-stu-id="1143a-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="1143a-114">Stránka **Organizačná jednotka** > mriežka **Cenníky**</span><span class="sxs-lookup"><span data-stu-id="1143a-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="1143a-115">Stránka **Obchodný vzťah** > mriežka **Projektové cenníky**</span><span class="sxs-lookup"><span data-stu-id="1143a-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="1143a-116">Stránka **Projektové cenové ponuky** > mriežka **Projektové cenníky**: Toto platí pre všetky aktívne projektové cenové ponuky.</span><span class="sxs-lookup"><span data-stu-id="1143a-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="1143a-117">Stránka **Projektové zmluvy** > mriežka **Projektové cenníky**: Toto platí pre všetky aktívne projektové zmluvy.</span><span class="sxs-lookup"><span data-stu-id="1143a-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="1143a-118">Pre každú stránku musíte zvoliť cenník, ktorý chcete odstrániť, a potom zvoliť **Odstrániť**.</span><span class="sxs-lookup"><span data-stu-id="1143a-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="1143a-119">Odstránenie alebo deaktivácia cenníka zo stránky Cenníky</span><span class="sxs-lookup"><span data-stu-id="1143a-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="1143a-120">Ak chcete odstrániť cenník z aktívnych cenníkov, prejdite na **Predaj** > **Zákazníci** > **Cenníky**.</span><span class="sxs-lookup"><span data-stu-id="1143a-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="1143a-121">Vyberte cenník, ktorý chcete odstrániť, a potom vyberte **Odstrániť**.</span><span class="sxs-lookup"><span data-stu-id="1143a-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="1143a-122">Ak sa na cenník odkazuje pri akýchkoľvek existujúcich transakciách, nebudete ho môcť vymazať.</span><span class="sxs-lookup"><span data-stu-id="1143a-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="1143a-123">Ak k tomu dôjde, môžete cenník deaktivovať, aby sa nezobrazil v žiadnom zobrazení.</span><span class="sxs-lookup"><span data-stu-id="1143a-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="1143a-124">Ak chcete cenník deaktivovať, znova vyberte cenník a potom vyberte možnosť **Deaktivovať**.</span><span class="sxs-lookup"><span data-stu-id="1143a-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
