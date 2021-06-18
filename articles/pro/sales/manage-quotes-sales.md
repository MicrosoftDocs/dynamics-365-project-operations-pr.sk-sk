---
title: Správa projektových cenových ponúk
description: Táto téma poskytuje informácie o projektových cenových ponukách.
author: rumant
ms.date: 10/26/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8e0b20d4780a14edc3c242e261e22d4905f783a4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994830"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="47100-103">Správa projektových cenových ponúk</span><span class="sxs-lookup"><span data-stu-id="47100-103">Manage project quotes</span></span>

<span data-ttu-id="47100-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="47100-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47100-105">V Dynamics 365 Project Operations sú projektové cenové ponuky navrhnuté tak, aby pomáhali vytvárať návrhy pre projektové práce.</span><span class="sxs-lookup"><span data-stu-id="47100-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="47100-106">Štruktúra projektovej cenovej ponuky v aplikácii Project Operations je prispôsobená projektovým návrhom s nasledujúcimi komponentmi:</span><span class="sxs-lookup"><span data-stu-id="47100-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="47100-107">Riadky cenovej ponuky, ktoré identifikujú jednotlivé komponenty práce, ktoré budú prezentované ako komponenty na vysokej úrovni.</span><span class="sxs-lookup"><span data-stu-id="47100-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="47100-108">Podrobnosti riadka cenovej ponuky, ktoré identifikujú a odhadujú prácu pre každý komponent alebo riadok cenovej ponuky na vysokej úrovni.</span><span class="sxs-lookup"><span data-stu-id="47100-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="47100-109">Odhady plánu alebo dátumu a finančné aspekty práce sú zviazané s riadkom cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="47100-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="47100-110">Pre každý riadok cenovej ponuky sú nastavené zmluvné modely a fakturovateľné komponenty.</span><span class="sxs-lookup"><span data-stu-id="47100-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="47100-111">Toto nastavenie pomáha odhadnúť rozloženie výnosov, výdavkov a ziskovosti pre každý riadok cenovej ponuky a celkovú cenovú ponuku.</span><span class="sxs-lookup"><span data-stu-id="47100-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="47100-112">Zobrazenie všetkých projektových cenových ponúk</span><span class="sxs-lookup"><span data-stu-id="47100-112">View all project-based quotes</span></span>

<span data-ttu-id="47100-113">Zoznam všetkých projektových cenových ponúk je uvedený na stránke so zoznamom **Cenové ponuky**.</span><span class="sxs-lookup"><span data-stu-id="47100-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="47100-114">Prejdite do časti **Predaj** > **Cenové ponuky**.</span><span class="sxs-lookup"><span data-stu-id="47100-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="47100-115">Zobrazí sa zoznam všetkých vašich projektových cenových ponúk v systéme.</span><span class="sxs-lookup"><span data-stu-id="47100-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="47100-116">Použite **Prepínač zobrazení** na výber ďalších filtrovaných zobrazení cenových ponúk.</span><span class="sxs-lookup"><span data-stu-id="47100-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="47100-117">Pomocou vlastných kritérií filtra môžete nakonfigurovať svoje vlastné zobrazenia a možnosti navigácie.</span><span class="sxs-lookup"><span data-stu-id="47100-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="47100-118">Cenové ponuky je možné vytvárať alebo mazať z tejto stránky so zoznamom alebo zo stránok s podrobnosťami.</span><span class="sxs-lookup"><span data-stu-id="47100-118">Quotes can be created or deleted from this list page or detail pages.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]