---
title: Etapy projektu
description: Táto téma poskytuje informácie o etapách projektu, ktoré sú dostupné v Microsoft Dynamics Project Operations.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286807"
---
# <a name="project-stages"></a><span data-ttu-id="fd87b-103">Etapy projektu</span><span class="sxs-lookup"><span data-stu-id="fd87b-103">Project stages</span></span>

<span data-ttu-id="fd87b-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="fd87b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="fd87b-105">Etapy projektu slúžia na to, aby odrážali stav projektu, ktorý postupuje.</span><span class="sxs-lookup"><span data-stu-id="fd87b-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="fd87b-106">Prispôsobenia sa dajú použiť na automatickú aktualizáciu etáp pomocou postupov obchodného procesu, Power Automate alebo rozšírení doplnkov.</span><span class="sxs-lookup"><span data-stu-id="fd87b-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="fd87b-107">Nasledujúce etapy sú definované v predvolenom toku obchodného procesu:</span><span class="sxs-lookup"><span data-stu-id="fd87b-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="fd87b-108">Nový</span><span class="sxs-lookup"><span data-stu-id="fd87b-108">New</span></span>
- <span data-ttu-id="fd87b-109">Ponuka</span><span class="sxs-lookup"><span data-stu-id="fd87b-109">Quote</span></span>
- <span data-ttu-id="fd87b-110">Plán</span><span class="sxs-lookup"><span data-stu-id="fd87b-110">Plan</span></span>
- <span data-ttu-id="fd87b-111">Doručiť</span><span class="sxs-lookup"><span data-stu-id="fd87b-111">Deliver</span></span>
- <span data-ttu-id="fd87b-112">Hotovo</span><span class="sxs-lookup"><span data-stu-id="fd87b-112">Complete</span></span>
- <span data-ttu-id="fd87b-113">Zatvoriť</span><span class="sxs-lookup"><span data-stu-id="fd87b-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="fd87b-114">Nový</span><span class="sxs-lookup"><span data-stu-id="fd87b-114">New</span></span>

<span data-ttu-id="fd87b-115">Po vytvorení projektu sa fáza projektu nastaví na **Nové**.</span><span class="sxs-lookup"><span data-stu-id="fd87b-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="fd87b-116">Ak bol projekt vytvorený zo šablóny, môže mať údaje o pláne, odhadovaní a tímových údajoch.</span><span class="sxs-lookup"><span data-stu-id="fd87b-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="fd87b-117">V opačnom prípade je to obrys projektu a zostávajúce komponenty musia byť zadané.</span><span class="sxs-lookup"><span data-stu-id="fd87b-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="fd87b-118">Cenová ponuka</span><span class="sxs-lookup"><span data-stu-id="fd87b-118">Quote</span></span>

<span data-ttu-id="fd87b-119">Po spojení projektu a cenovej ponuky alebo jeho vytvorení z cenovej ponuky sa etapa projektu nastaví na **cenová ponuka** a odhadované dátumy začatia a ukončenia sú aktualizované.</span><span class="sxs-lookup"><span data-stu-id="fd87b-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="fd87b-120">Keď je projekt vo fáze **cenovej ponuky**, podrobnosti cenovej ponuky sa zobrazia na karte **predaje** na stránke **entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="fd87b-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="fd87b-121">Plánovať</span><span class="sxs-lookup"><span data-stu-id="fd87b-121">Plan</span></span>

<span data-ttu-id="fd87b-122">Ak vyhráte cenovú ponuku, ktorá je priradená k projektu a project je posunutý do fázy **zmluvy**, stav projektu sa aktualizuje na **plán**.</span><span class="sxs-lookup"><span data-stu-id="fd87b-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="fd87b-123">Keď je projekt vo fáze **plánu**, podrobnosti zmluvy sa zobrazia na stránke **entita projektu**.</span><span class="sxs-lookup"><span data-stu-id="fd87b-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="fd87b-124">Doručiť</span><span class="sxs-lookup"><span data-stu-id="fd87b-124">Deliver</span></span>

<span data-ttu-id="fd87b-125">Keď je dokončený plán projektu, a ste pripravení na spustenie projektu, projektový manažér by mal aktualizovať fázu projektu na **dodať** aby ukázal, že projekt začal.</span><span class="sxs-lookup"><span data-stu-id="fd87b-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="fd87b-126">Dokončené</span><span class="sxs-lookup"><span data-stu-id="fd87b-126">Complete</span></span> 

<span data-ttu-id="fd87b-127">Keď je dokončená práca pre projekt, projektový manažér môže aktualizovať fázu na **dokončené**.</span><span class="sxs-lookup"><span data-stu-id="fd87b-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="fd87b-128">Aktualizáciou fáze projektu na **dokončené**, projektový manažér naznačuje, že práca je 100-percentne dokončená, ale že projekt je stále otvorený tak, že všetky čakajúce časy alebo výdavkové položky môžu byť zaznamenané.</span><span class="sxs-lookup"><span data-stu-id="fd87b-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="fd87b-129">Zavrieť</span><span class="sxs-lookup"><span data-stu-id="fd87b-129">Close</span></span>

<span data-ttu-id="fd87b-130">Keď sú všetky transakcie zaznamenané pre projekt, projektový manažér môže aktualizovať fázu na **zatvorené**.</span><span class="sxs-lookup"><span data-stu-id="fd87b-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="fd87b-131">V tomto momente nie je možné zaznamenať žiadne transakcie a projekt je nastavený iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="fd87b-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]