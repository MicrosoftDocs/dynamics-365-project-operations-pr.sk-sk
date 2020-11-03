---
title: Odhady nákladov
description: Táto téma poskytuje informácie o definovaní alebo odhade výdavkov na základe projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084286"
---
# <a name="expense-estimates"></a><span data-ttu-id="9acae-103">Odhady nákladov</span><span class="sxs-lookup"><span data-stu-id="9acae-103">Expense estimates</span></span>
<span data-ttu-id="9acae-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="9acae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9acae-105">Spolu s definovaním odhadov založených na zdrojoch umožňuje Dynamics 365 Project Operations projektovým manažérom definovať výdavky na základe projektu pre každý projekt.</span><span class="sxs-lookup"><span data-stu-id="9acae-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="9acae-106">Každú položku výdavkov je možné priradiť ku konkrétnej projektovej úlohe alebo kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9acae-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="9acae-107">Kategórie výdavkov sú zvyčajne definované na úrovni organizácie.</span><span class="sxs-lookup"><span data-stu-id="9acae-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="9acae-108">Cena pre každú kategóriu výdavkov je zvyčajne definovaná v nasledujúcej hierarchii:</span><span class="sxs-lookup"><span data-stu-id="9acae-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="9acae-109">Organizácia</span><span class="sxs-lookup"><span data-stu-id="9acae-109">Organization</span></span>
- <span data-ttu-id="9acae-110">Zákazník</span><span class="sxs-lookup"><span data-stu-id="9acae-110">Customer</span></span>
- <span data-ttu-id="9acae-111">Cenová ponuka/zmluva</span><span class="sxs-lookup"><span data-stu-id="9acae-111">Quote/contract</span></span>

<span data-ttu-id="9acae-112">Ak chcete zobraziť, pridať alebo odstrániť projektové výdavky, postupujte podľa nasledujúcich krokov.</span><span class="sxs-lookup"><span data-stu-id="9acae-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="9acae-113">Prejdite do časti **Projekty** a vyberte projekt, na ktorom chcete pracovať.</span><span class="sxs-lookup"><span data-stu-id="9acae-113">Go to **Projects** , and select the project you want to work on.</span></span>
2. <span data-ttu-id="9acae-114">Vyberte kartu **Odhady projektu** a prezrite si zoznam projektových výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9acae-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="9acae-115">Vyberte **Nový výdavok** na pridanie výdavku.</span><span class="sxs-lookup"><span data-stu-id="9acae-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="9acae-116">Alebo vyberte výdavok, ktorý chcete odstrániť, a potom vyberte **Odstrániť výdavok**.</span><span class="sxs-lookup"><span data-stu-id="9acae-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="9acae-117">Pre každú položku riadka výdavku sú definované nasledujúce atribúty:</span><span class="sxs-lookup"><span data-stu-id="9acae-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="9acae-118">**Kategória** :Bežné zoskupenia používané na popis všetkých výdavkov vzniknutých v súvislosti s projektom.</span><span class="sxs-lookup"><span data-stu-id="9acae-118">**Category** : The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="9acae-119">**Dátum začiatku** : Dátum, kedy sa predpokladá vznik výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9acae-119">**Start Date** : The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="9acae-120">**Množstvo** : Odhadovaný počet položiek výdavkov pre konkrétnu kategóriu.</span><span class="sxs-lookup"><span data-stu-id="9acae-120">**Quantity** : The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="9acae-121">**Jednotková obstarávacia cena** : Jednotková cena použitá na náklady výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9acae-121">**Unit Cost Price** : The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="9acae-122">**Jednotková predajná cena** : Jednotková cena použitá na výpočet predajných cien výdavkov.</span><span class="sxs-lookup"><span data-stu-id="9acae-122">**Unit Sales Price** : The unit price used to calculate the sale prices of the expense.</span></span>

