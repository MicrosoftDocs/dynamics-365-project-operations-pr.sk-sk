---
title: Etapy projektu
description: Táto téma poskytuje informácie o etapách projektu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755560"
---
# <a name="project-stages"></a><span data-ttu-id="f7580-103">Etapy projektu</span><span class="sxs-lookup"><span data-stu-id="f7580-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f7580-104">Etapy projektu sa aktualizujú, aby odrážali stav projektu, ktorý prebieha.</span><span class="sxs-lookup"><span data-stu-id="f7580-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="f7580-105">Predvolený tok obchodného procesu automaticky aktualizuje niektoré etapy projektu, zatiaľ čo iné sú manuálne aktualizované projektovým manažérom.</span><span class="sxs-lookup"><span data-stu-id="f7580-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="f7580-106">Nasledujúce etapy sú definované v predvolenom BPF:</span><span class="sxs-lookup"><span data-stu-id="f7580-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="f7580-107">Nové</span><span class="sxs-lookup"><span data-stu-id="f7580-107">New</span></span>
- <span data-ttu-id="f7580-108">Cenová ponuka</span><span class="sxs-lookup"><span data-stu-id="f7580-108">Quote</span></span>
- <span data-ttu-id="f7580-109">Plánovať</span><span class="sxs-lookup"><span data-stu-id="f7580-109">Plan</span></span>
- <span data-ttu-id="f7580-110">Doručiť</span><span class="sxs-lookup"><span data-stu-id="f7580-110">Deliver</span></span>
- <span data-ttu-id="f7580-111">Hotovo</span><span class="sxs-lookup"><span data-stu-id="f7580-111">Complete</span></span>
- <span data-ttu-id="f7580-112">Zavrieť</span><span class="sxs-lookup"><span data-stu-id="f7580-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="f7580-113">Nové</span><span class="sxs-lookup"><span data-stu-id="f7580-113">New</span></span>

<span data-ttu-id="f7580-114">Po vytvorení projektu sa fáza projektu nastaví na **Nové**.</span><span class="sxs-lookup"><span data-stu-id="f7580-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="f7580-115">Ak bol projekt vytvorený zo šablóny, môže mať údaje o pláne, odhadovaní a tímových údajoch.</span><span class="sxs-lookup"><span data-stu-id="f7580-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="f7580-116">V opačnom prípade je to len obrys projektu a zostávajúce komponenty musia byť zadané.</span><span class="sxs-lookup"><span data-stu-id="f7580-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="f7580-117">Cenová ponuka</span><span class="sxs-lookup"><span data-stu-id="f7580-117">Quote</span></span>

<span data-ttu-id="f7580-118">Po spojení projektu a cenovej ponuky alebo jeho vytvorení z cenovej ponuky sa etapa projektu nastaví na **cenová ponuka** a odhadované dátumy začatia a ukončenia sú aktualizované.</span><span class="sxs-lookup"><span data-stu-id="f7580-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="f7580-119">Keď je projekt vo fáze **cenovej ponuky**, podrobnosti cenovej ponuky sa zobrazia na karte **predaje** na stránke **entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="f7580-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="f7580-120">Plánovať</span><span class="sxs-lookup"><span data-stu-id="f7580-120">Plan</span></span>

<span data-ttu-id="f7580-121">Ak vyhráte cenovú ponuku, ktorá je priradená k projektu a project je posunutý do fázy **zmluvy**, stav projektu sa aktualizuje na **plán**.</span><span class="sxs-lookup"><span data-stu-id="f7580-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="f7580-122">Keď je projekt vo fáze **plánu**, podrobnosti zmluvy sa zobrazia na stránke **entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="f7580-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="f7580-123">Doručiť</span><span class="sxs-lookup"><span data-stu-id="f7580-123">Deliver</span></span>

<span data-ttu-id="f7580-124">Keď je dokončený plán projektu, a ste pripravení na spustenie projektu, projektový manažér by mal aktualizovať fázu projektu na **dodať** aby ukázal, že projekt začal.</span><span class="sxs-lookup"><span data-stu-id="f7580-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="f7580-125">Dokončené</span><span class="sxs-lookup"><span data-stu-id="f7580-125">Complete</span></span> 

<span data-ttu-id="f7580-126">Keď je dokončená práca pre projekt, projektový manažér môže aktualizovať fázu na **dokončené**.</span><span class="sxs-lookup"><span data-stu-id="f7580-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="f7580-127">Aktualizáciou fáze projektu na **dokončené**, projektový manažér naznačuje, že práca je 100-percentne dokončená, ale že projekt je stále otvorený tak, že všetky čakajúce časy alebo výdavkové položky môžu byť zaznamenané.</span><span class="sxs-lookup"><span data-stu-id="f7580-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="f7580-128">Zavrieť</span><span class="sxs-lookup"><span data-stu-id="f7580-128">Close</span></span>

<span data-ttu-id="f7580-129">Keď sú všetky transakcie zaznamenané pre projekt, projektový manažér môže aktualizovať fázu na **zatvorené**.</span><span class="sxs-lookup"><span data-stu-id="f7580-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="f7580-130">V tomto momente nie je možné zaznamenať žiadne transakcie a projekt je nastavený iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="f7580-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
