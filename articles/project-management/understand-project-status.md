---
title: Oboznámenie sa so stavom projektu
description: Táto téma poskytuje informácie o stave priradenom k projektom v Dynamics 365 Project Operations.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965695"
---
# <a name="understand-project-status"></a><span data-ttu-id="4be7b-103">Oboznámenie sa so stavom projektu</span><span class="sxs-lookup"><span data-stu-id="4be7b-103">Understand project status</span></span>

<span data-ttu-id="4be7b-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="4be7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="4be7b-105">V časti **Stav** na stránke **Entita projektu** sa zobrazuje súhrn stavu projektu na základe nákladov a úsilia.</span><span class="sxs-lookup"><span data-stu-id="4be7b-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="4be7b-106">Polia súhrnu stavu</span><span class="sxs-lookup"><span data-stu-id="4be7b-106">Status summary fields</span></span>

- <span data-ttu-id="4be7b-107">Pole **Celkový stav projektu** je editovateľné pole, ktoré zobrazuje celkový stav projektu.</span><span class="sxs-lookup"><span data-stu-id="4be7b-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="4be7b-108">Pole používa farebné kódovanie, ako je zelená, žltá a červená, na označenie rastúceho rizika.</span><span class="sxs-lookup"><span data-stu-id="4be7b-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="4be7b-109">Pole **Poznámky** umožňuje správcovi projektu zadať konkrétne poznámky o stave.</span><span class="sxs-lookup"><span data-stu-id="4be7b-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="4be7b-110">Pole **Stav aktualizovaný dňa** sa nedá upraviť.</span><span class="sxs-lookup"><span data-stu-id="4be7b-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="4be7b-111">Hodnota v tomto poli je časová pečiatka, ktorá označuje, kedy bol stav naposledy aktualizovaný.</span><span class="sxs-lookup"><span data-stu-id="4be7b-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="4be7b-112">Polia **Výkonnosť plánu** a **Výkonnosť nákladov** sa nastavujú v mriežke sledovania.</span><span class="sxs-lookup"><span data-stu-id="4be7b-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="4be7b-113">Keď plán a odchýlka nákladov pre koreňový uzol v zobrazení **Sledovanie úsilia** budú pozitívne, tieto polia sa aktualizujú na **Popredu**.</span><span class="sxs-lookup"><span data-stu-id="4be7b-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="4be7b-114">Keď časový rozvrh a odchýlka nákladov pre koreňový uzol sú záporné, tieto polia sa nastavia na možnosť **Pozadu**.</span><span class="sxs-lookup"><span data-stu-id="4be7b-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
