---
title: Odoslanie žiadosti o zdroj
description: Požiadavku vygenerovaného prostriedku môžete odoslať ako požiadavku na zdroj. Žiadosť sa potom odošle správcovi prostriedkov na naplnenie.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 2cf93d8bf0be5b61a739195a41334c34d910e9ba
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/05/2020
ms.locfileid: "3961746"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="94f12-104">Odoslanie žiadosti o zdroj</span><span class="sxs-lookup"><span data-stu-id="94f12-104">Submit a resource request</span></span>

<span data-ttu-id="94f12-105">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="94f12-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="94f12-106">Požiadavku vygenerovaného prostriedku môžete odoslať ako požiadavku na zdroj.</span><span class="sxs-lookup"><span data-stu-id="94f12-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="94f12-107">Žiadosť sa potom odošle správcovi prostriedkov na naplnenie.</span><span class="sxs-lookup"><span data-stu-id="94f12-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="94f12-108">V Dynamics 365 Project Operations na stránke **Projekty** vyberte kartu **Tím** a zobrazte zoznam rezervovateľných zdrojov.</span><span class="sxs-lookup"><span data-stu-id="94f12-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="94f12-109">Zo zoznamu vyberte všeobecný zdroj, ktorý má požiadavku na zdroj a potom kliknite na položku **Odoslať žiadosť**.</span><span class="sxs-lookup"><span data-stu-id="94f12-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="94f12-110">Žiadosť stav generického člena tímu sa zmení na **Odoslané**.</span><span class="sxs-lookup"><span data-stu-id="94f12-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="94f12-111">Po splnení požiadavky sa všeobecný zdroj nahradí názvom zdroja, ak správca zdrojov splní požiadavku s rezerváciou pomenovaného zdroja.</span><span class="sxs-lookup"><span data-stu-id="94f12-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="94f12-112">V opačnom prípade, ak správca zdrojov navrhne pomenovaný zdroj, všeobecný zdroj zostane v tíme a stav žiadosti sa zmení na **Vyžaduje kontrolu**.</span><span class="sxs-lookup"><span data-stu-id="94f12-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
