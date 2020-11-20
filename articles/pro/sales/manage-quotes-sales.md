---
title: Správa projektových cenových ponúk
description: Táto téma poskytuje informácie o projektových cenových ponukách.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177845"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="54931-103">Správa projektových cenových ponúk</span><span class="sxs-lookup"><span data-stu-id="54931-103">Manage project quotes</span></span>

<span data-ttu-id="54931-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="54931-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="54931-105">V Dynamics 365 Project Operations sú projektové cenové ponuky navrhnuté tak, aby pomáhali vytvárať návrhy pre projektové práce.</span><span class="sxs-lookup"><span data-stu-id="54931-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="54931-106">Štruktúra projektovej cenovej ponuky v aplikácii Project Operations je prispôsobená projektovým návrhom s nasledujúcimi komponentmi:</span><span class="sxs-lookup"><span data-stu-id="54931-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="54931-107">Riadky cenovej ponuky, ktoré identifikujú jednotlivé komponenty práce, ktoré budú prezentované ako komponenty na vysokej úrovni.</span><span class="sxs-lookup"><span data-stu-id="54931-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="54931-108">Podrobnosti riadka cenovej ponuky, ktoré identifikujú a odhadujú prácu pre každý komponent alebo riadok cenovej ponuky na vysokej úrovni.</span><span class="sxs-lookup"><span data-stu-id="54931-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="54931-109">Odhady plánu alebo dátumu a finančné aspekty práce sú zviazané s riadkom cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="54931-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="54931-110">Pre každý riadok cenovej ponuky sú nastavené zmluvné modely a fakturovateľné komponenty.</span><span class="sxs-lookup"><span data-stu-id="54931-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="54931-111">Toto nastavenie pomáha odhadnúť rozloženie výnosov, výdavkov a ziskovosti pre každý riadok cenovej ponuky a celkovú cenovú ponuku.</span><span class="sxs-lookup"><span data-stu-id="54931-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="54931-112">Zobrazenie všetkých projektových cenových ponúk</span><span class="sxs-lookup"><span data-stu-id="54931-112">View all project-based quotes</span></span>

<span data-ttu-id="54931-113">Zoznam všetkých projektových cenových ponúk je uvedený na stránke so zoznamom **Cenové ponuky**.</span><span class="sxs-lookup"><span data-stu-id="54931-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="54931-114">Prejdite do časti **Predaj** > **Cenové ponuky**.</span><span class="sxs-lookup"><span data-stu-id="54931-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="54931-115">Zobrazí sa zoznam všetkých vašich projektových cenových ponúk v systéme.</span><span class="sxs-lookup"><span data-stu-id="54931-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="54931-116">Použite **Prepínač zobrazení** na výber ďalších filtrovaných zobrazení cenových ponúk.</span><span class="sxs-lookup"><span data-stu-id="54931-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="54931-117">Pomocou vlastných kritérií filtra môžete nakonfigurovať svoje vlastné zobrazenia a možnosti navigácie.</span><span class="sxs-lookup"><span data-stu-id="54931-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="54931-118">Cenové ponuky je možné vytvárať alebo mazať z tejto stránky so zoznamom alebo zo stránok s podrobnosťami.</span><span class="sxs-lookup"><span data-stu-id="54931-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
