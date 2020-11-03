---
title: Vytvorenie modelov prognóz pre rozpočty projektov
description: Táto téma popisuje, ako vytvoriť model prognózy pre zostávajúce rozpočty.
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084500"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="2e71c-103">Vytvorenie modelov prognóz pre rozpočty projektov</span><span class="sxs-lookup"><span data-stu-id="2e71c-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e71c-104">Táto téma popisuje, ako vytvoriť model prognózy pre zostávajúce rozpočty.</span><span class="sxs-lookup"><span data-stu-id="2e71c-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="2e71c-105">Projekt, ktorý podlieha kontrole rozpočtu, používa dva typy rozpočtov: pôvodný a zvyšný.</span><span class="sxs-lookup"><span data-stu-id="2e71c-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="2e71c-106">Pri vytváraní rozpočtu projektu musíte určiť pôvodný a zostávajúci model prognózy rozpočtu, ktoré boli vytvorené na stránke **Modely prognóz**.</span><span class="sxs-lookup"><span data-stu-id="2e71c-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="2e71c-107">Rozpočty projektu založené na zadaných modeloch sa vytvárajú pri potvrdení projektového rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="2e71c-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="2e71c-108">Model prognózy, ktorý sa používa na kontrolu rozpočtu, nemôže mať podmodel alebo ho nemožno použiť ako podmodel.</span><span class="sxs-lookup"><span data-stu-id="2e71c-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="2e71c-109">Vyberte **Projektové riadenie a účtovníctvo** > **Nastavenie** > **Prognózy**  > **Modely prognóz**.</span><span class="sxs-lookup"><span data-stu-id="2e71c-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="2e71c-110">Vyberte možnosť **Nový** a vytvorte nový model prognózy a potom zadajte číslo ID a názov nového modelu.</span><span class="sxs-lookup"><span data-stu-id="2e71c-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="2e71c-111">Nastavte možnosť **Zastavené** na **Áno** , čím zabránite akýmkoľvek zmenám v riadkoch prognózy pre model prognózy.</span><span class="sxs-lookup"><span data-stu-id="2e71c-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="2e71c-112">Ak by riadky prognózy, s ktorými je model spojený, mali generovať prognózy peňažných tokov v hlavnej účtovnej knihe, nastavte možnosť **Zahrnúť do prognóz peňažného toku** na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="2e71c-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="2e71c-113">Ak chcete ako dátum fakturácie použiť dátum projektu, nastavte možnosť **Prognóza dátumu faktúry** na **Áno**.</span><span class="sxs-lookup"><span data-stu-id="2e71c-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="2e71c-114">V poli **Typ rozpočtu** vyberte jeden z nasledujúcich typov modelov:</span><span class="sxs-lookup"><span data-stu-id="2e71c-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="2e71c-115">**Pôvodný rozpočet** : Použite pôvodné sumy rozpočtu, ktoré sú potvrdené pri vytvorení a schválení pôvodného rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="2e71c-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="2e71c-116">**Zostávajúci rozpočet** : Použite zostávajúce sumy rozpočtu počas realizácie projektu.</span><span class="sxs-lookup"><span data-stu-id="2e71c-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="2e71c-117">Zostatky v tomto modeli prognózy sa znižujú o skutočné transakcie a zvyšujú alebo znižujú sa revíziami rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="2e71c-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="2e71c-118">**Preniesť** : Použite sumy preneseného rozpočtu pre projekt.</span><span class="sxs-lookup"><span data-stu-id="2e71c-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="2e71c-119">Prenos je voliteľný proces, pomocou ktorého je možné preniesť nevyužité sumy rozpočtu z jedného fiškálneho roka na druhý.</span><span class="sxs-lookup"><span data-stu-id="2e71c-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="2e71c-120">Podľa potreby nastavte nasledujúce možnosti:</span><span class="sxs-lookup"><span data-stu-id="2e71c-120">Set the following options as required:</span></span>

   - <span data-ttu-id="2e71c-121">Povoľte možnosť **Prognóza dátumu faktúry** , ak chcete ako dátum faktúry použiť dátum projektu.</span><span class="sxs-lookup"><span data-stu-id="2e71c-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="2e71c-122">Povoľte možnosť **Prognóza s WIP** pre prognózu na základe prebiehajúcej práce (WIP), a potom vyberte typ WIP.</span><span class="sxs-lookup"><span data-stu-id="2e71c-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="2e71c-123">Môžete ponechať predvolené nastavenie **Typ rozpočtu** ako **Žiadny** alebo zadajte nový typ.</span><span class="sxs-lookup"><span data-stu-id="2e71c-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="2e71c-124">Po zmene záznamu nie je možné zmeniť typ rozpočtu.</span><span class="sxs-lookup"><span data-stu-id="2e71c-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="2e71c-125">Ak zmeníte predvolený typ rozpočtu, pre aktualizácie nebudú k dispozícii žiadne ďalšie možnosti a tento model prognózy nebudete môcť znova použiť.</span><span class="sxs-lookup"><span data-stu-id="2e71c-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

