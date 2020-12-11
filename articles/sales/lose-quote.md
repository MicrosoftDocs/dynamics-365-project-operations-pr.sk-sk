---
title: Kopírovanie cenových ponúk založených na projekte
description: Táto téma poskytuje informácie o tom, ako kopírovať cenové ponuky založené na projekte v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e4e70ed1451c1076f72ef5d7200b918c626ab23c
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/31/2020
ms.locfileid: "4181831"
---
# <a name="copy-project-based-quotes"></a><span data-ttu-id="37aa6-103">Kopírovanie cenových ponúk založených na projekte</span><span class="sxs-lookup"><span data-stu-id="37aa6-103">Copy project-based quotes</span></span>

<span data-ttu-id="37aa6-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="37aa6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="37aa6-105">Novú cenovú ponuku projektu môžete ľahko vytvoriť skopírovaním existujúcej ponuky.</span><span class="sxs-lookup"><span data-stu-id="37aa6-105">You can easily create a new Project quote by copying an existing one.</span></span> 

- <span data-ttu-id="37aa6-106">Ak chcete skopírovať ponuku projektu na stránke zoznamu **Cenové ponuky projektu** alebo na stránke s podrobnosťami **Cenová ponuka projektu** vyberte ponuku projektu, ktorú chcete skopírovať, a potom vyberte možnosť **Kopírovať**.</span><span class="sxs-lookup"><span data-stu-id="37aa6-106">To copy a Project quote, on the **Project Quotes** list page or the **Project Quote** details page, select the Project quote you want to copy, and then select **Copy**.</span></span>

<span data-ttu-id="37aa6-107">Otvorí sa dialógové okno, na ktorom môžete zadať parametre kópie.</span><span class="sxs-lookup"><span data-stu-id="37aa6-107">This will open a dialog page where you can enter the parameters of the copy.</span></span> <span data-ttu-id="37aa6-108">V nasledujúcej tabuľke je uvedený zoznam polí, ktoré sú obsiahnuté na dialógovej stránke.</span><span class="sxs-lookup"><span data-stu-id="37aa6-108">The following table lists the fields that are included in the dialog page.</span></span> <span data-ttu-id="37aa6-109">V závislosti od zvolených hodnôt sa môže proces kopírovania zmeniť.</span><span class="sxs-lookup"><span data-stu-id="37aa6-109">Depending on the values you select, the copy process may change.</span></span>

| <span data-ttu-id="37aa6-110">**Pole**</span><span class="sxs-lookup"><span data-stu-id="37aa6-110">**Field**</span></span> | <span data-ttu-id="37aa6-111">**Opis**</span><span class="sxs-lookup"><span data-stu-id="37aa6-111">**Description**</span></span> | <span data-ttu-id="37aa6-112">**Nadväzujúci vplyv**</span><span class="sxs-lookup"><span data-stu-id="37aa6-112">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="37aa6-113">Predmet</span><span class="sxs-lookup"><span data-stu-id="37aa6-113">Topic</span></span> | <span data-ttu-id="37aa6-114">Zadajte príslušnú tému alebo názov cieľovej cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="37aa6-114">Enter the relevant topic, or name, of the target quote.</span></span> <span data-ttu-id="37aa6-115">Keď sa otvorí dialógové okno, systém ho nastaví na tému zdrojovej ponuky s doplnkom **-kópia**.</span><span class="sxs-lookup"><span data-stu-id="37aa6-115">When the dialog opens, the system will set it to the topic of the source quote with **-copy** appended to it.</span></span> | |
| <span data-ttu-id="37aa6-116">Potenciálny zákazník</span><span class="sxs-lookup"><span data-stu-id="37aa6-116">Potential Customer</span></span> | <span data-ttu-id="37aa6-117">Odkaz na záznam zákazníka spoločnosti zákazníka alebo obchodného vzťahu.</span><span class="sxs-lookup"><span data-stu-id="37aa6-117">Reference to the customer's company or account record.</span></span> <span data-ttu-id="37aa6-118">Po otvorení dialógového okna ho systém nastaví na účet uvedený v zdrojovej cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="37aa6-118">When the dialog opens, the system will set it to the account on the source quote.</span></span> | <span data-ttu-id="37aa6-119">Toto pole je primárnym zákazníkom v cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="37aa6-119">This field is the primary customer on the quote.</span></span> |
| <span data-ttu-id="37aa6-120">Zmluvná jednotka</span><span class="sxs-lookup"><span data-stu-id="37aa6-120">Contracting Unit</span></span> | <span data-ttu-id="37aa6-121">Organizačná jednotka, ktorá je zodpovedná za realizáciu projektov spojených s týmto obchodom.</span><span class="sxs-lookup"><span data-stu-id="37aa6-121">The organization unit that is responsible for the delivery of the project(s) associated with this deal.</span></span>
<span data-ttu-id="37aa6-122">Po otvorení dialógového okna ho systém nastaví na zmluvnú jednotku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="37aa6-122">When the dialog opens, the system will set it to the contracting unit of the source quote.</span></span> | <span data-ttu-id="37aa6-123">Zmluvnou jednotkou je divízia spoločnosti, ktorá bude po uzatvorení obchodu realizovať projekty.</span><span class="sxs-lookup"><span data-stu-id="37aa6-123">Contracting unit is the division of the company that will execute the projects after the deal is closed.</span></span> <span data-ttu-id="37aa6-124">Každá zmluvná jednotka má menu.</span><span class="sxs-lookup"><span data-stu-id="37aa6-124">Every contracting unit has a currency.</span></span> <span data-ttu-id="37aa6-125">Mena sa používa na vykazovanie odhadovaných a skutočných nákladov vzniknutých počas realizácie projektu.</span><span class="sxs-lookup"><span data-stu-id="37aa6-125">The currency is used to report estimated and actual costs incurred during the execution of the project.</span></span> |
| <span data-ttu-id="37aa6-126">Mena</span><span class="sxs-lookup"><span data-stu-id="37aa6-126">Currency</span></span> | <span data-ttu-id="37aa6-127">Je to mena, v ktorej sa obchoduje transakcia.</span><span class="sxs-lookup"><span data-stu-id="37aa6-127">This is the currency that the deal is transacted in.</span></span> <span data-ttu-id="37aa6-128">Po otvorení dialógového okna ho systém nastaví na menu cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="37aa6-128">When the dialog opens, the system will set it to the currency of the source quote.</span></span> <span data-ttu-id="37aa6-129">Môže sa upravovať a ak ide o zmenu, pole **Kopírovať ceny** je vždy nastavené na **Nie**.</span><span class="sxs-lookup"><span data-stu-id="37aa6-129">This can be modified and if it is change, the **Copy Pricing** field is always set to **No**.</span></span> <span data-ttu-id="37aa6-130">Je to tak preto, lebo cenníky pri zdrojovej ponuke už nie sú relevantné.</span><span class="sxs-lookup"><span data-stu-id="37aa6-130">This is because the price lists on source quote are no longer relevant.</span></span> | <span data-ttu-id="37aa6-131">Mena sa používa na predvolenie cenníka, na zostavenie finančného odhadu cenovej ponuky a prípadne na fakturáciu zákazníkovi, keď dôjde k získaniu obchodu.</span><span class="sxs-lookup"><span data-stu-id="37aa6-131">Currency is used to default a price list, to build a financial estimate on the quote,  and eventually to invoice the customer when the deal is won.</span></span> |
| <span data-ttu-id="37aa6-132">Požadovaný dátum doručenia</span><span class="sxs-lookup"><span data-stu-id="37aa6-132">Requested Delivery Date</span></span> | <span data-ttu-id="37aa6-133">Toto je dátum doručenia požadovaný zákazníkom.</span><span class="sxs-lookup"><span data-stu-id="37aa6-133">This is the date of delivery requested by the customer.</span></span> | <span data-ttu-id="37aa6-134">Používa sa ako konečný dátum pri vytváraní fakturačných dátumov podľa konkrétnej frekvencie.</span><span class="sxs-lookup"><span data-stu-id="37aa6-134">This is used as the end date when creating invoicing dates along a specific frequency.</span></span> |
| <span data-ttu-id="37aa6-135">Kopírovať cenu</span><span class="sxs-lookup"><span data-stu-id="37aa6-135">Copy pricing</span></span> | <span data-ttu-id="37aa6-136">Hodnota Áno/Nie označuje, či sa má cena v cenovej ponuke kopírovať zo zdrojovej cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="37aa6-136">A Yes/No value indicates whether the pricing on the quote should be copied from the source quote.</span></span> | <span data-ttu-id="37aa6-137">Ak je vybraná možnosť **Áno**, cenník projektu a referencie cenníka produktu sa skopírujú zo zdrojovej cenovej ponuky do cieľovej cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="37aa6-137">If **Yes** is selected, the project price list and product price list references are copied from the source quote to the target quote.</span></span> <span data-ttu-id="37aa6-138">Ak je vybraná možnosť **Nie**, cenníky sa predvolene nastavujú na základe najnovších cenníkov, ktoré boli nastavené v parametroch účtu alebo projektu.</span><span class="sxs-lookup"><span data-stu-id="37aa6-138">If **No** is selected, price lists are re-defaulted based on the latest price lists that were set up on the account or project parameters.</span></span> |

<span data-ttu-id="37aa6-139">Keď vyberiete **OK** na dialógovej stránke, systém vytvorí kópiu ponuky projektu na základe parametrov vybratých v dialógovom okne.</span><span class="sxs-lookup"><span data-stu-id="37aa6-139">When you select **OK** on the dialog page, the system creates a copy of the project quote based on the parameters selected in the dialog.</span></span> <span data-ttu-id="37aa6-140">Otvorí sa nová ponuka projektu.</span><span class="sxs-lookup"><span data-stu-id="37aa6-140">The new project quote opens.</span></span> 

> [!NOTE]
> <span data-ttu-id="37aa6-141">Nasledujúce informácie sa nekopírujú zo zdrojovej ponuky do cieľovej ponuky:</span><span class="sxs-lookup"><span data-stu-id="37aa6-141">The following information is not copied from the Source to the Target quote:</span></span>
>
> - <span data-ttu-id="37aa6-142">Plány faktúry</span><span class="sxs-lookup"><span data-stu-id="37aa6-142">Invoice schedules</span></span>
> - <span data-ttu-id="37aa6-143">Zákazníci v cenovej ponuke a v riadkoch cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="37aa6-143">Quote and quote line customers</span></span>
> - <span data-ttu-id="37aa6-144">Odkaz na projekt v riadkoch založených na cenovej ponuke založených na projekte – Informácie o rozpočte zákazníka</span><span class="sxs-lookup"><span data-stu-id="37aa6-144">Project reference on the project – based quote lines -Customer budget information</span></span>
>
><span data-ttu-id="37aa6-145">Pretože sú tieto informácie veľmi špecifické pre každú cenovú ponuku, tieto polia a záznamy sa nekopírujú.</span><span class="sxs-lookup"><span data-stu-id="37aa6-145">Because this information is very specific to each quote, these fields and records are not copied.</span></span> <span data-ttu-id="37aa6-146">Skopírujú sa riadky cenovej ponuky pre projekty a produkty, odhady podrobností ponuky a hodnoty neprekročenia na úrovni ponuky.</span><span class="sxs-lookup"><span data-stu-id="37aa6-146">Quote lines for projects and products, estimates on quote line details, and not-to-exceed values at the quote level are copied.</span></span> <span data-ttu-id="37aa6-147">Predvolené ceny a sadzby nákladov závisia od možnosti **Kopírovať ceny** vybranej na dialógovej stránke **Kopírovať parametre**.</span><span class="sxs-lookup"><span data-stu-id="37aa6-147">Price and cost rate defaults depend on the **Copy pricing** option selected on the **Copy parameters** dialog page.</span></span>