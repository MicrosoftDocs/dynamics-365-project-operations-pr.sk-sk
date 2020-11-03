---
title: Samostatná rezervácia zdrojov
description: Táto téma poskytuje informácie o požiadavkách na predbežnú rezerváciu.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 861e484ea2fc251e0082b4cb0cd5409a45a74057
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084574"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="0c03e-103">Požiadavky na predbežnú rezerváciu.</span><span class="sxs-lookup"><span data-stu-id="0c03e-103">Soft-book requirements</span></span>

<span data-ttu-id="0c03e-104">Požiadavku na zdroje možno rezervovať na pevno.</span><span class="sxs-lookup"><span data-stu-id="0c03e-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="0c03e-105">Pevná rezervácia vytvára návrh, ktorý spotrebuje kapacitu prostriedku.</span><span class="sxs-lookup"><span data-stu-id="0c03e-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="0c03e-106">Návrh sa potom odošle späť žiadateľovi na schválenie.</span><span class="sxs-lookup"><span data-stu-id="0c03e-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="0c03e-107">Predbežná rezervácia predbežne pridá zdroj do projektového tímu a má iný stav na tabuli plánovania, ale nespotrebuje kapacitu prostriedku.</span><span class="sxs-lookup"><span data-stu-id="0c03e-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="0c03e-108">Na predbežné rezervovanie zdroja na tabuli plánovania nastavte pole **Stav rezervácie** na **Predbežné**.</span><span class="sxs-lookup"><span data-stu-id="0c03e-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Stav rezervácie je nastavený na Predbežné](media/Resource-Management-image77.png)

<span data-ttu-id="0c03e-110">Keď sa karta **Tím** nachádza v zobrazení **Vymenovaní členovia tímu** , tu sa zobrazí zdroj.</span><span class="sxs-lookup"><span data-stu-id="0c03e-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="0c03e-111">Predbežne rezervované hodiny sa vykážu v stĺpci **Počet predbežne rezervovaných hodín**.</span><span class="sxs-lookup"><span data-stu-id="0c03e-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Predbežne rezervované hodiny v zobrazení Vymenovaní členovia tímu](media/Resource-Management-image78.png)

<span data-ttu-id="0c03e-113">Členovia tímu, ktorí sú predbežne rezervovaní, nemôžu byť priradení k úlohám.</span><span class="sxs-lookup"><span data-stu-id="0c03e-113">Soft-booked team members can be assigned to tasks.</span></span>

![Členov tímu, ktorý je predbežne rezervovany, priradený k úlohe](media/Resource-Management-image79.png)

<span data-ttu-id="0c03e-115">Na karte **Vyrovnanie** sa pre predbežne rezervovaný zdroj nezobrazujú žiadne rezervácie, pretože karta **Vyrovnanie** zohľadňuje iba pevné rezervácie.</span><span class="sxs-lookup"><span data-stu-id="0c03e-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Predbežne rezervovaný zdroj bez rezervácií na karte Vyrovnanie](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="0c03e-117">Zdroj nemožno predbežne rezervovať z požiadavky, ktorá bola vygenerované zo všeobecného člena tímu.</span><span class="sxs-lookup"><span data-stu-id="0c03e-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="0c03e-118">Na tabuli plánovania sa na predbežnú rezerváciu zdroja využíva iné farebné označenie.</span><span class="sxs-lookup"><span data-stu-id="0c03e-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Predbežné rezervácie na tabuli plánovania](media/Resource-Management-image81.png)

<span data-ttu-id="0c03e-120">Ak chcete predbežnú rezerváciu zmeniť na pevnú, na tabuli plánovania kliknite pravým tlačidlom na predbežnú rezerváciu, kde stlačte možnosť **Zmeniť stav** \> **Pevne rezervovať** \> **Pevne**.</span><span class="sxs-lookup"><span data-stu-id="0c03e-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Zmena stavu rezervácie na pevný](media/Resource-Management-image82.png)

<span data-ttu-id="0c03e-122">Rezervácia sa zmení a stav sa zmení na tabuli plánovania.</span><span class="sxs-lookup"><span data-stu-id="0c03e-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="0c03e-123">Keďže stav rezervácie je teraz **Pevný** , zdroj je zobrazený ako rezervovaný a jeho kapacita a dostupnosť sa upravia.</span><span class="sxs-lookup"><span data-stu-id="0c03e-123">Because the booking status is now **Hard** , the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="0c03e-124">Rovnakú metódu môžete použiť na zrušenie pevnej rezervácie alebo predbežnej rezervácie z tabule plánovania.</span><span class="sxs-lookup"><span data-stu-id="0c03e-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="0c03e-125">Ak chcete konvertovať predbežne rezervovaný prostriedok na pevne rezervovaný prostriedok, na projektovej karte **Tím** vyberte zdroj, a potom stlačte **Potvrdiť**.</span><span class="sxs-lookup"><span data-stu-id="0c03e-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Príkaz potvrdenia](media/Resource-Management-image83.png)
