---
title: Odoslanie žiadosti o zdroj
description: Požiadavku vygenerovaného prostriedku môžete odoslať ako požiadavku na zdroj. Žiadosť sa potom odošle správcovi prostriedkov na naplnenie.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279157"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="97343-104">Odoslanie žiadosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="97343-104">Submit a resource request</span></span>

<span data-ttu-id="97343-105">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="97343-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="97343-106">Požiadavku vygenerovaného prostriedku môžete odoslať ako požiadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="97343-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="97343-107">Žiadosť sa potom odošle správcovi prostriedkov na naplnenie.</span><span class="sxs-lookup"><span data-stu-id="97343-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="97343-108">V Dynamics 365 Project Operations na stránke **Projekty** vyberte kartu **Tím** a zobrazte zoznam rezervovateľných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="97343-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="97343-109">Zo zoznamu vyberte všeobecný zdroj, ktorý má požiadavku na zdroj a potom kliknite na položku **Odoslať žiadosť**.</span><span class="sxs-lookup"><span data-stu-id="97343-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="97343-110">Žiadosť stav generického člena tímu sa zmení na **Odoslané**.</span><span class="sxs-lookup"><span data-stu-id="97343-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="97343-111">Po splnení požiadavky sa všeobecný zdroj nahradí názvom zdroja, ak správca zdrojov splní požiadavku s rezerváciou pomenovaného zdroja.</span><span class="sxs-lookup"><span data-stu-id="97343-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="97343-112">V opačnom prípade, ak správca zdrojov navrhne pomenovaný zdroj, všeobecný zdroj zostane v tíme a stav žiadosti sa zmení na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="97343-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]