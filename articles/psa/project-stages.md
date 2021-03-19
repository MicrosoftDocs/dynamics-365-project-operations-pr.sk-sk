---
title: Typy etapy projektu
description: Táto téma poskytuje informácie o etapách projektu.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283702"
---
# <a name="project-stage-types"></a><span data-ttu-id="1b847-103">Typy etapy projektu</span><span class="sxs-lookup"><span data-stu-id="1b847-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="1b847-104">Etapy projektu slúžia na to, aby odrážali stav projektu, ktorý postupuje.</span><span class="sxs-lookup"><span data-stu-id="1b847-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="1b847-105">Prispôsobenia sa dajú použiť na automatickú aktualizáciu etáp pomocou postupov obchodného procesu, Power Automate alebo rozšírení doplnkov.</span><span class="sxs-lookup"><span data-stu-id="1b847-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="1b847-106">Nasledujúce etapy sú definované v predvolenom BPF:</span><span class="sxs-lookup"><span data-stu-id="1b847-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="1b847-107">Nová</span><span class="sxs-lookup"><span data-stu-id="1b847-107">New</span></span>
- <span data-ttu-id="1b847-108">Ponuka</span><span class="sxs-lookup"><span data-stu-id="1b847-108">Quote</span></span>
- <span data-ttu-id="1b847-109">Plánovať</span><span class="sxs-lookup"><span data-stu-id="1b847-109">Plan</span></span>
- <span data-ttu-id="1b847-110">Doručiť</span><span class="sxs-lookup"><span data-stu-id="1b847-110">Deliver</span></span>
- <span data-ttu-id="1b847-111">Hotovo</span><span class="sxs-lookup"><span data-stu-id="1b847-111">Complete</span></span>
- <span data-ttu-id="1b847-112">Zavrieť</span><span class="sxs-lookup"><span data-stu-id="1b847-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="1b847-113">Nové</span><span class="sxs-lookup"><span data-stu-id="1b847-113">New</span></span>

<span data-ttu-id="1b847-114">Po vytvorení projektu sa fáza projektu nastaví na **Nové**.</span><span class="sxs-lookup"><span data-stu-id="1b847-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="1b847-115">Ak bol projekt vytvorený zo šablóny, môže mať údaje o pláne, odhadovaní a tímových údajoch.</span><span class="sxs-lookup"><span data-stu-id="1b847-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="1b847-116">V opačnom prípade je to len obrys projektu a zostávajúce komponenty musia byť zadané.</span><span class="sxs-lookup"><span data-stu-id="1b847-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="1b847-117">Cenová ponuka</span><span class="sxs-lookup"><span data-stu-id="1b847-117">Quote</span></span>

<span data-ttu-id="1b847-118">Po spojení projektu a cenovej ponuky alebo jeho vytvorení z cenovej ponuky sa etapa projektu nastaví na **cenová ponuka** a odhadované dátumy začatia a ukončenia sú aktualizované.</span><span class="sxs-lookup"><span data-stu-id="1b847-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="1b847-119">Keď je projekt vo fáze **cenovej ponuky**, podrobnosti cenovej ponuky sa zobrazia na karte **predaje** na stránke **entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="1b847-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="1b847-120">Plánovať</span><span class="sxs-lookup"><span data-stu-id="1b847-120">Plan</span></span>

<span data-ttu-id="1b847-121">Ak vyhráte cenovú ponuku, ktorá je priradená k projektu a project je posunutý do fázy **zmluvy**, stav projektu sa aktualizuje na **plán**.</span><span class="sxs-lookup"><span data-stu-id="1b847-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="1b847-122">Keď je projekt vo fáze **plánu**, podrobnosti zmluvy sa zobrazia na stránke **entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="1b847-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="1b847-123">Doručiť</span><span class="sxs-lookup"><span data-stu-id="1b847-123">Deliver</span></span>

<span data-ttu-id="1b847-124">Keď je dokončený plán projektu, a ste pripravení na spustenie projektu, projektový manažér by mal aktualizovať fázu projektu na **dodať** aby ukázal, že projekt začal.</span><span class="sxs-lookup"><span data-stu-id="1b847-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="1b847-125">Dokončené</span><span class="sxs-lookup"><span data-stu-id="1b847-125">Complete</span></span> 

<span data-ttu-id="1b847-126">Keď je dokončená práca pre projekt, projektový manažér môže aktualizovať fázu na **dokončené**.</span><span class="sxs-lookup"><span data-stu-id="1b847-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="1b847-127">Aktualizáciou fáze projektu na **dokončené**, projektový manažér naznačuje, že práca je 100-percentne dokončená, ale že projekt je stále otvorený tak, že všetky čakajúce časy alebo výdavkové položky môžu byť zaznamenané.</span><span class="sxs-lookup"><span data-stu-id="1b847-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="1b847-128">Zavrieť</span><span class="sxs-lookup"><span data-stu-id="1b847-128">Close</span></span>

<span data-ttu-id="1b847-129">Keď sú všetky transakcie zaznamenané pre projekt, projektový manažér môže aktualizovať fázu na **zatvorené**.</span><span class="sxs-lookup"><span data-stu-id="1b847-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="1b847-130">V tomto momente nie je možné zaznamenať žiadne transakcie a projekt je nastavený iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="1b847-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]