---
title: Rezervujte pomenované zdroje zo zdrojových požiadaviek.
description: Táto téma poskytuje informácie o rezervácii pomenovaných zdrojov pre požiadavku na všeobecné zdroje.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
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
ms.openlocfilehash: d7ff58ec08661adc702867c6c26805a74a3637c9
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125917"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="23b87-103">Rezervujte pomenované zdroje zo zdrojových požiadaviek.</span><span class="sxs-lookup"><span data-stu-id="23b87-103">Book named resources from resource requirements</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="23b87-104">Môžete rezervovať pomenovaný zdroj k výmene všeobecného zdroja, ktorý má zdrojovú požiadavku.</span><span class="sxs-lookup"><span data-stu-id="23b87-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="23b87-105">V Project Service Automation (PSA) na stránke **projekty** kliknite na kartu **Tím**.</span><span class="sxs-lookup"><span data-stu-id="23b87-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="23b87-106">Vyberte všeobecný zdroj, ktorý má zdrojovú požiadavku zo zoznamu a potom kliknite na položku **rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="23b87-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="23b87-107">Alebo otvorte zdrojovú požiadavku a potom kliknite na položku **rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="23b87-107">Or, open the resource requirement and then click **Book**.</span></span>


![Rezervácia všeobecného člena tímu](media/RM-how-to-14.png)


3. <span data-ttu-id="23b87-109">Na stránke **asistent plánovania** vyberte pomenovaný zdroj, ktorý chcete rezervovať do projektového tímu, a potom kliknite na položku **rezervovať**.</span><span class="sxs-lookup"><span data-stu-id="23b87-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![Rezervácia všeobecného člena tímu pomocou Asistenta plánovania](media/RM-how-to-15.png)

<span data-ttu-id="23b87-111">Po dokončení rezervácie a splnení pomenovaného zdroja sa všeobecný zdroj nahradí názvom zdroja.</span><span class="sxs-lookup"><span data-stu-id="23b87-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![Pomenovaný člen tímu nahrádza všeobecného člena tímu](media/RM-how-to-16.png)

<span data-ttu-id="23b87-113">Priradenia v pláne sú tiež aktualizované s názvom zdroja.</span><span class="sxs-lookup"><span data-stu-id="23b87-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![Pomenovaný člen tímu priradený k úlohám projektu](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="23b87-115">Naplnenie všeobecného zdroja s viacerými pomenovaniami zdrojov</span><span class="sxs-lookup"><span data-stu-id="23b87-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="23b87-116">Splnenie požiadavky na všeobecný zdroj s viacerými pomenovanými zdrojmi je podobné priradením jediného pomenovaného zdroja.</span><span class="sxs-lookup"><span data-stu-id="23b87-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="23b87-117">Napríklad, je tam úloha s trvaním päť dní a 120 hodín úsilia.</span><span class="sxs-lookup"><span data-stu-id="23b87-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="23b87-118">Túto úlohu nie je možné dokončiť jedným zdrojom, ktorý pracuje s typickým osemhodinovým dňom počas päťdňového týždňa.</span><span class="sxs-lookup"><span data-stu-id="23b87-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![Úloha, ktorá potrebuje 120 hodín úsilia počas piatich dní](media/RM-how-to-21.png)

<span data-ttu-id="23b87-120">Požiadavka je 120 hodín inžinierstva robotiky počas piatich dní, čo je 24 hodín denne.</span><span class="sxs-lookup"><span data-stu-id="23b87-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![Denná požiadavka](media/RM-how-to-22.png)

<span data-ttu-id="23b87-122">Toto je príklad, kedy sú potrebné viaceré pomenované zdroje na splnenie všeobecnej zdrojovej požiadavky.</span><span class="sxs-lookup"><span data-stu-id="23b87-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="23b87-123">Budete musieť rezervovať viac zdrojov na splnenie požiadavky.</span><span class="sxs-lookup"><span data-stu-id="23b87-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![Rezervácia viacerých zdrojov na splnenie požiadavky.](media/RM-how-to-23.png)

<span data-ttu-id="23b87-125">Hlavný rozdiel v tomto scenári je, že všeobecný zdroj zostáva priradený k tímovej úlohe a rezervované pomenované zdroje členov tímu nie sú priradené ako súčasť pozície.</span><span class="sxs-lookup"><span data-stu-id="23b87-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="23b87-126">Projektový manažér môže priradiť prácu podľa zodpovedajúcich pomenovaných prostriedkov.</span><span class="sxs-lookup"><span data-stu-id="23b87-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="23b87-127">Zobrazenie **odsúhlasenia** môže pomôcť projektovému manažérovi pri rozbití rezervácií naprieč viacerými zdrojmi na priradenie úlohy.</span><span class="sxs-lookup"><span data-stu-id="23b87-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="23b87-128">To sa nerobí automaticky, pretože v každom scenári zložitejšie ako jednoduchý príklad vyššie, ako keď máte zväzok úloh, ktoré tvoria požiadavku, zámer, ako chce projektový manažér priradiť, je potrebné systémovo predpokladať.</span><span class="sxs-lookup"><span data-stu-id="23b87-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="23b87-129">Vzhľadom k tomu, že systém nemôže pochopiť zámer, je pravdepodobné, že predpoklady budú iné, než je určené, a stane sa nesprávny alebo nepredvídateľný výsledok.</span><span class="sxs-lookup"><span data-stu-id="23b87-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="23b87-130">Predvídateľný výsledok je, že všeobecný zdroj zostáva priradený, kým projektový manažér zámerne vytvorí úlohy, s pomocou zobrazenia **odsúhlasenia**.</span><span class="sxs-lookup"><span data-stu-id="23b87-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


