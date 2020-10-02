---
title: Splnenie všeobecných požiadaviek zdrojov
description: Táto téma poskytuje informácie o rezervácii pomenovaných zdrojov pre požiadavku na všeobecné zdroje.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 76dd47fa2451b5cb61298ff332d77bae646a288a
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897605"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="0240f-103">Splnenie všeobecných požiadaviek zdrojov</span><span class="sxs-lookup"><span data-stu-id="0240f-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="0240f-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="0240f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0240f-105">Môžete rezervovať pomenovaný zdroj k výmene všeobecného zdroja, ktorý má zdrojovú požiadavku.</span><span class="sxs-lookup"><span data-stu-id="0240f-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="0240f-106">Na stránke **Projekty** vyberte kartu **Tím**.</span><span class="sxs-lookup"><span data-stu-id="0240f-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="0240f-107">Vyberte všeobecný zdroj, ktorý má zdrojovú požiadavku zo zoznamu a potom vyberte **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="0240f-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="0240f-108">Alebo otvorte zdrojovú požiadavku a potom vyberte **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="0240f-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="0240f-109">Na stránke **Asistent plánovania** vyberte pomenovaný zdroj, ktorý chcete rezervovať do projektového tímu, a potom vyberte **Rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="0240f-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="0240f-110">Po dokončení rezervácie a splnení pomenovaného zdroja sa všeobecný zdroj nahradí názvom zdroja.</span><span class="sxs-lookup"><span data-stu-id="0240f-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="0240f-111">Priradenia v pláne sú tiež aktualizované s názvom zdroja.</span><span class="sxs-lookup"><span data-stu-id="0240f-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="0240f-112">Naplnenie všeobecného zdroja s viacerými pomenovaniami zdrojov</span><span class="sxs-lookup"><span data-stu-id="0240f-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="0240f-113">Splnenie požiadavky na všeobecný zdroj s viacerými pomenovanými zdrojmi je podobné priradením jediného pomenovaného zdroja.</span><span class="sxs-lookup"><span data-stu-id="0240f-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="0240f-114">Napríklad, je tam úloha s trvaním päť dní a 120 hodín úsilia.</span><span class="sxs-lookup"><span data-stu-id="0240f-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="0240f-115">Túto úlohu nie je možné dokončiť jedným zdrojom, ktorý pracuje s typickým osemhodinovým dňom počas päťdňového týždňa.</span><span class="sxs-lookup"><span data-stu-id="0240f-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="0240f-116">Požiadavka je 120 hodín inžinierstva robotiky počas piatich dní, čo je 24 hodín denne.</span><span class="sxs-lookup"><span data-stu-id="0240f-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="0240f-117">Toto je príklad, kedy sú potrebné viaceré pomenované zdroje na splnenie všeobecnej zdrojovej požiadavky.</span><span class="sxs-lookup"><span data-stu-id="0240f-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="0240f-118">Budete musieť rezervovať viac zdrojov na splnenie požiadavky.</span><span class="sxs-lookup"><span data-stu-id="0240f-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="0240f-119">Hlavný rozdiel v tomto scenári je, že všeobecný zdroj zostáva priradený k tímovej úlohe a rezervované pomenované zdroje členov tímu nie sú priradené ako súčasť pozície.</span><span class="sxs-lookup"><span data-stu-id="0240f-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="0240f-120">Projektový manažér môže priradiť prácu podľa zodpovedajúcich pomenovaných prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="0240f-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="0240f-121">Zobrazenie **odsúhlasenia** môže pomôcť projektovému manažérovi pri rozbití rezervácií naprieč viacerými zdrojmi na priradenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="0240f-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="0240f-122">To sa nerobí automaticky, pretože v každom scenári, ktorú je zložitejší ako jednoduchý príklad vyššie, ako napr. keď máte zväzok úloh, ktoré tvoria požiadavku alebo zámer, ako chce projektový manažér vykonať priradenie, je potrebné predpokladať systémovo.</span><span class="sxs-lookup"><span data-stu-id="0240f-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="0240f-123">Vzhľadom k tomu, že systém nemôže pochopiť zámer, je pravdepodobné, že predpoklady budú iné, než je určené, a stane sa nesprávny alebo nepredvídateľný výsledok.</span><span class="sxs-lookup"><span data-stu-id="0240f-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="0240f-124">Predvídateľný výsledok je, že všeobecný zdroj zostáva priradený, kým projektový manažér zámerne vytvorí úlohy, s pomocou zobrazenia **odsúhlasenia**.</span><span class="sxs-lookup"><span data-stu-id="0240f-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


