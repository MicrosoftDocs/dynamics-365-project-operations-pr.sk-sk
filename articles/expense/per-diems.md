---
title: Za každý deň
description: Táto téma poskytuje informácie o pravidlách diét, ktoré sa používajú v správe výdavkov.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908586"
---
# <a name="per-diems"></a><span data-ttu-id="113f3-103">Za každý deň</span><span class="sxs-lookup"><span data-stu-id="113f3-103">Per diems</span></span>

<span data-ttu-id="113f3-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="113f3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="113f3-105">Diéta je príspevok, ktorý sa vypláca pracovníkovi, ktorý cestuje za prácou.</span><span class="sxs-lookup"><span data-stu-id="113f3-105">A per diem is an allowance that is paid to a worker who is traveling for work.</span></span> <span data-ttu-id="113f3-106">V správe výdavkov môžete vytvoriť pravidlá diét pre rôzne cestovné situácie.</span><span class="sxs-lookup"><span data-stu-id="113f3-106">In Expense management, you can create per diem rules for  various travel situations.</span></span> <span data-ttu-id="113f3-107">Sadzby za diéty môžu byť založené na ročnom období, mieste cesty alebo oboch.</span><span class="sxs-lookup"><span data-stu-id="113f3-107">Per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="113f3-108">Keď vytvoríte pravidlo týkajúce sa diéty, môžete určiť, že bude zadržané percento z diéty, ak pracovník dostane bezplatné stravovanie alebo služby.</span><span class="sxs-lookup"><span data-stu-id="113f3-108">When you create a per diem  rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="113f3-109">Môžete tiež nastaviť minimálny a maximálny počet hodín, pre ktoré môže platiť diéta pre cestu pracovníka.</span><span class="sxs-lookup"><span data-stu-id="113f3-109">You can also set a minimum and maximum number of hours that the per diem rate can apply to a worker's travel.</span></span>

## <a name="configuration"></a><span data-ttu-id="113f3-110">Konfigurácia</span><span class="sxs-lookup"><span data-stu-id="113f3-110">Configuration</span></span> 

1. <span data-ttu-id="113f3-111">Ak chcete pridať miesta diét, prejdite na **Nastaviť** > **Výpočty a kódy** > **Miesta diét**.</span><span class="sxs-lookup"><span data-stu-id="113f3-111">To add per diem locations, go to **Set up** > **Calculations and codes** > **Per diem locations**.</span></span>
2. <span data-ttu-id="113f3-112">Pre každé z miest pridaných vyššie vyberte sadzbu diét a menu, ktorá je platná medzi konkrétnym dátumom začatia a ukončenia hotela, stravovania a ďalších výdavkov.</span><span class="sxs-lookup"><span data-stu-id="113f3-112">For each of the locations added above, select a per diem rate and currency that is valid between a specific start and end date for hotel, meals, and other expenses.</span></span> <span data-ttu-id="113f3-113">Sadzby a meny diét sú nakonfigurované v časti **Nastaviť** > **Výpočty a kódy** > **Diéty**.</span><span class="sxs-lookup"><span data-stu-id="113f3-113">Per diem rates and currencies are configured under **Set up** > **Calculations and codes** > **Per diems**.</span></span>
3. <span data-ttu-id="113f3-114">Na stránke **Miesta diét** stránka, nakonfigurujte úrovne denných diét.</span><span class="sxs-lookup"><span data-stu-id="113f3-114">On the **Per diem locations** page, configure per diem rate tiers.</span></span> <span data-ttu-id="113f3-115">Úrovne denných diét vám umožňujú definovať percentuálne rozdelenie denného príspevku na hotel, stravu a ďalšie výdavky.</span><span class="sxs-lookup"><span data-stu-id="113f3-115">Per diem rate tiers allow you to define the percentage split of a daily allowance for hotel, meal, and other expenses.</span></span> 
4. <span data-ttu-id="113f3-116">Ak chcete určiť zníženie percento jedla pri raňajkách, obede alebo večeri, aktualizujte polia na stránke **Parametre správy výdavkov** na karte **Diéty**.</span><span class="sxs-lookup"><span data-stu-id="113f3-116">To specify the meal percentage reduction for breakfast, lunch, or dinner, update the fields on the **Expense management parameters** page on the **Per diem** tab.</span></span> 
    
## <a name="submit-expenses-using-per-diem"></a><span data-ttu-id="113f3-117">Predloženie výdavkov pri použití diét</span><span class="sxs-lookup"><span data-stu-id="113f3-117">Submit expenses using per diem</span></span>
<span data-ttu-id="113f3-118">Na predloženie výdavkov s použitím diét pri vytváraní výkazu výdavkov použite kategóriu výdavkov **Diéty**.</span><span class="sxs-lookup"><span data-stu-id="113f3-118">To submit expenses utilizing per diems, use the **Per diem** expense category when you create an expense report.</span></span> <span data-ttu-id="113f3-119">Prejdite do **Diéty od dátumu**, **Diéta k dátumu** a **Miesto diét**.</span><span class="sxs-lookup"><span data-stu-id="113f3-119">Enter the **Per diem from date**, **Per diem to date**,  and the **Per diem location**.</span></span> <span data-ttu-id="113f3-120">Suma sa vypočíta na základe sadzieb diét pre vybrané miesto a zníženie jedál sa vypočíta na základe úrovní denných diét.</span><span class="sxs-lookup"><span data-stu-id="113f3-120">The amount will be calculated based on the per diem rates for the selected location and meal reduction will be calculated based on the per diem rate tiers.</span></span>
