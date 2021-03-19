---
title: Odhady nákladov
description: Táto téma poskytuje informácie o definovaní alebo odhade výdavkov na základe projektu.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3f0429366c69346113003355679c055cd2c74ca3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287077"
---
# <a name="expense-estimates"></a><span data-ttu-id="f0095-103">Odhady nákladov</span><span class="sxs-lookup"><span data-stu-id="f0095-103">Expense estimates</span></span>
<span data-ttu-id="f0095-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="f0095-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f0095-105">Spolu s definovaním odhadov založených na zdrojoch umožňuje Dynamics 365 Project Operations projektovým manažérom definovať projektové výdavky pre každý projekt.</span><span class="sxs-lookup"><span data-stu-id="f0095-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="f0095-106">Každú položku výdavkov je možné priradiť ku konkrétnej projektovej úlohe alebo kategórii výdavkov.</span><span class="sxs-lookup"><span data-stu-id="f0095-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="f0095-107">Kategórie výdavkov sú zvyčajne definované na úrovni organizácie.</span><span class="sxs-lookup"><span data-stu-id="f0095-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="f0095-108">Cena pre každú kategóriu výdavkov je zvyčajne definovaná v nasledujúcej hierarchii:</span><span class="sxs-lookup"><span data-stu-id="f0095-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="f0095-109">Organizácia</span><span class="sxs-lookup"><span data-stu-id="f0095-109">Organization</span></span>
- <span data-ttu-id="f0095-110">Zákazník</span><span class="sxs-lookup"><span data-stu-id="f0095-110">Customer</span></span>
- <span data-ttu-id="f0095-111">Cenová ponuka/zmluva</span><span class="sxs-lookup"><span data-stu-id="f0095-111">Quote/contract</span></span>

<span data-ttu-id="f0095-112">Ak chcete zobraziť, pridať alebo odstrániť projektové výdavky, postupujte podľa nasledujúcich krokov.</span><span class="sxs-lookup"><span data-stu-id="f0095-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="f0095-113">Prejdite do časti **Projekty** a vyberte projekt, na ktorom chcete pracovať.</span><span class="sxs-lookup"><span data-stu-id="f0095-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="f0095-114">Vyberte kartu **Odhady projektu** a prezrite si zoznam projektových výdavkov.</span><span class="sxs-lookup"><span data-stu-id="f0095-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="f0095-115">Vyberte **Nový výdavok** na pridanie výdavku.</span><span class="sxs-lookup"><span data-stu-id="f0095-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="f0095-116">Alebo vyberte výdavok, ktorý chcete odstrániť, a potom vyberte **Odstrániť výdavok**.</span><span class="sxs-lookup"><span data-stu-id="f0095-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="f0095-117">Pre každú položku riadka výdavku sú definované nasledujúce atribúty:</span><span class="sxs-lookup"><span data-stu-id="f0095-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="f0095-118">**Kategória** :Bežné zoskupenia používané na popis všetkých výdavkov vzniknutých v súvislosti s projektom.</span><span class="sxs-lookup"><span data-stu-id="f0095-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="f0095-119">**Dátum začiatku**: Dátum, kedy sa predpokladá vznik výdavkov.</span><span class="sxs-lookup"><span data-stu-id="f0095-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="f0095-120">**Množstvo**: Odhadovaný počet položiek výdavkov pre konkrétnu kategóriu.</span><span class="sxs-lookup"><span data-stu-id="f0095-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="f0095-121">**Jednotková obstarávacia cena**: Jednotková cena použitá na náklady výdavkov.</span><span class="sxs-lookup"><span data-stu-id="f0095-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="f0095-122">**Jednotková predajná cena**: Jednotková cena použitá na výpočet predajných cien výdavkov.</span><span class="sxs-lookup"><span data-stu-id="f0095-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]