---
title: Odoslanie žiadosti o zdroj
description: Táto téma poskytuje informácie o odoslaní žiadosti o projektový prostriedok.
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: acdd228a9eb9d6c6c56f126ccca416613332a838
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013190"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="7aa6b-103">Odoslanie žiadosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="7aa6b-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7aa6b-104">Požiadavku vygenerovaného prostriedku môžete odoslať ako požiadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="7aa6b-105">Žiadosť sa potom odošle správcovi prostriedkov na naplnenie.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="7aa6b-106">V Project Service Automation (PSA) na stránke **Projekty** kliknite na kartu **Tím** a zobrazte zoznam rezervovateľných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="7aa6b-107">Vyberte všeobecný zdroj, ktorý má zdrojovú požiadavku zo zoznamu a potom kliknite na položku **Odoslať žiadosť**.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Odoslanie žiadosti o zdroj](media/RM-how-to-18.png)

<span data-ttu-id="7aa6b-109">Žiadosť stav generického člena tímu sa zmení na **Odoslané**.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="7aa6b-110">Po splnení požiadavky správcom prostriedkov sa všeobecný prostriedok nahradí názvom prostriedku, ak správca prostriedkov splní požiadavku s rezerváciou pomenovaného prostriedku.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="7aa6b-111">V opačnom prípade všeobecný prostriedok zostane v tíme a stav požiadavky sa zmení na **Vyžaduje kontrolu**, ak správca prostriedkov navrhol pomenovaný prostriedok.</span><span class="sxs-lookup"><span data-stu-id="7aa6b-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]