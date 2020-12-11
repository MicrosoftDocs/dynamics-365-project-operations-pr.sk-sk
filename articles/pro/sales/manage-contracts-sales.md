---
title: Správa projektových zmlúv
description: Táto téma poskytuje informácie o prezeraní projektových zmlúv.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 441fbc378a423334f45bc65658811ef238515393
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177350"
---
# <a name="manage-project-contracts"></a><span data-ttu-id="9ca5b-103">Správa projektových zmlúv</span><span class="sxs-lookup"><span data-stu-id="9ca5b-103">Manage project contracts</span></span>

<span data-ttu-id="9ca5b-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="9ca5b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9ca5b-105">Projektové zmluvy v Dynamics 365 Project Operations zachytávajú a spravujú zmluvne dohodnuté záväzky a fakturačné údaje projektu.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-105">Project contracts in Dynamics 365 Project Operations capture and manage the contractually agreed on commitments and billing details of a project.</span></span> <span data-ttu-id="9ca5b-106">Štruktúra projektovej zmluvy v aplikácii Project Operations je prispôsobená projektovej práci s nasledujúcimi komponentmi:</span><span class="sxs-lookup"><span data-stu-id="9ca5b-106">The structure of a project contract in Project Operations is tailored to project-based work with the following components:</span></span>

- <span data-ttu-id="9ca5b-107">Riadky zmluvy, ktoré identifikujú jednotlivé komponenty práce, ktoré budú na faktúre za projekt prezentované ako komponenty na vysokej úrovni.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-107">Contract lines that identify the discrete components of work that will be presented as high-level components on a project invoice.</span></span>
- <span data-ttu-id="9ca5b-108">Podrobnosti riadku zmluvy, ktoré identifikujú a odhadujú prácu pre každý komponent alebo riadok zmluvy na vysokej úrovni.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-108">Contract line details that identify and estimate the work for each high-level component or contract line.</span></span> <span data-ttu-id="9ca5b-109">Odhad zahŕňa plán a finančné aspekty práce súvisiacej s riadkom zmluvy.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-109">The estimate includes the schedule and the financial aspects for the work tied to the contract line.</span></span>
- <span data-ttu-id="9ca5b-110">Zmluvné modely a spoplatnené komponenty sa nastavujú pre každý riadok zmluvy, ktorý obsahuje fakturačné dojednanie pre každý riadok zmluvy a celkovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-110">Contracting models and chargeable components are set up for each contract line that holds the billing arrangement for each contract line and the overall contract.</span></span>

## <a name="view-all-project-based-contracts"></a><span data-ttu-id="9ca5b-111">Zobrazenie všetkých projektových zmlúv</span><span class="sxs-lookup"><span data-stu-id="9ca5b-111">View all project-based contracts</span></span>

<span data-ttu-id="9ca5b-112">Zoznam všetkých projektových zmlúv je uvedený na stránke so zoznamom **Zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-112">A list of all project contracts can be seen on the **Contracts** list page.</span></span> 

1. <span data-ttu-id="9ca5b-113">Prejdite na stránku **Predaj** > **Zmluvy**.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-113">Go to **Sales** > **Contracts**.</span></span> <span data-ttu-id="9ca5b-114">Zobrazí sa zoznam všetkých vašich projektových zmlúv v systéme.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-114">A list of all your project Contracts in the system are shown.</span></span> 
2. <span data-ttu-id="9ca5b-115">Vyberte ikonu **Prepínač zobrazení** (šípka rozbaľovacej ponuky vedľa názvu zobrazenia) a vyberte ďalšie filtrované zobrazenia.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-115">Select the **View switcher** (the drop-down arrow next to the name of the view) to select other filtered views.</span></span> <span data-ttu-id="9ca5b-116">Môžete si vytvoriť svoje vlastné zobrazenia pomocou vlastných kritérií filtra.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-116">You can create your own views with custom filter criteria.</span></span>

<span data-ttu-id="9ca5b-117">Zmluvy je možné vytvárať alebo mazať z tejto stránky so zoznamom alebo zo stránok s podrobnosťami.</span><span class="sxs-lookup"><span data-stu-id="9ca5b-117">Contracts can be created or deleted from this list page or detail pages.</span></span>