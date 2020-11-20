---
title: Sledovať stavu projektu
description: Ako na sledovanie stavu projektu v Project Service
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 00b6d874b42a415fe567d17e49c0ea319d8952a0
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127852"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="d51e0-103">Sledovanie stavu projektu (Project Service)</span><span class="sxs-lookup"><span data-stu-id="d51e0-103">Track a project’s status (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="d51e0-104">Použite [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] na sledovanie pokroku projektu klienta.</span><span class="sxs-lookup"><span data-stu-id="d51e0-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="d51e0-105">Počas procesu sa fázy projektu aktualizujú vzhľadom na priebeh:</span><span class="sxs-lookup"><span data-stu-id="d51e0-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="d51e0-106">**Nové**</span><span class="sxs-lookup"><span data-stu-id="d51e0-106">**New**</span></span>    | <span data-ttu-id="d51e0-107">Po vytvorení projektu sa fáza nastaví na **Nové**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="d51e0-108">Ak ste vytvorili projekt zo šablóny, v tejto fáze projektu môže mať plán, odhady a tím údajov.</span><span class="sxs-lookup"><span data-stu-id="d51e0-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="d51e0-109">V opačnom prípade bude náčrt projektu a musíte ručne zadajte zvyšku komponentov projektu.</span><span class="sxs-lookup"><span data-stu-id="d51e0-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="d51e0-110">**Ponuka**</span><span class="sxs-lookup"><span data-stu-id="d51e0-110">**Quote**</span></span>   |      <span data-ttu-id="d51e0-111">Po spojení projektu a cenovej ponuky alebo jeho vytvorení z cenovej ponuky sa fáza projektu nastaví na **Cenová ponuka** a aktualizujú sa aj odhadovaný dátum začatia a ukončenia.</span><span class="sxs-lookup"><span data-stu-id="d51e0-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="d51e0-112">Keď projekt je vo fáze cenová ponuka, podrobnosti cenovej ponuky sa zobrazia na karte **Predaj** stránky **projektu**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="d51e0-113">**Plánovať**</span><span class="sxs-lookup"><span data-stu-id="d51e0-113">**Plan**</span></span>   |                                     <span data-ttu-id="d51e0-114">Ak sa cenová ponuka priradená k projektu využije a proces sa dostane do fázy kontraktu, stav projektu sa aktualizuje na **Plán**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="d51e0-115">Podrobnosti zmluvy sa zobrazia na karte **Predaj** stránky **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="d51e0-116">**Hotovo**</span><span class="sxs-lookup"><span data-stu-id="d51e0-116">**Complete**</span></span> |                    <span data-ttu-id="d51e0-117">Po dokončení prác na projekte môžete jeho fázu prehodiť na **Dokončené**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="d51e0-118">Fáza dokončenia projektu predpokladá, že je práca hotová na 100 %, no projekt zostáva otvorený až do času, kým sa nezaznamenajú záznamy nákladov.</span><span class="sxs-lookup"><span data-stu-id="d51e0-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="d51e0-119">**Zavrieť**</span><span class="sxs-lookup"><span data-stu-id="d51e0-119">**Close**</span></span>   |           <span data-ttu-id="d51e0-120">Keď všetky transakcie boli zaznamenané na projekte a už sa nemusí čakať na žiadny záznam, môžete manuálne nastaviť fázu **Zatvorený**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="d51e0-121">Ak je stav projektu **Zatvorený**, nemôžete doň zadávať žiadne ďalšie transakcie a projekt prechádza do stavu len na čítanie.</span><span class="sxs-lookup"><span data-stu-id="d51e0-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="d51e0-122">Sledovanie stavu projektu</span><span class="sxs-lookup"><span data-stu-id="d51e0-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="d51e0-123">Prejdite na **Project Service > Projekty**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="d51e0-124">Kliknite na projekt, na ktorom chcete pracovať.</span><span class="sxs-lookup"><span data-stu-id="d51e0-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="d51e0-125">Na paneli v hornej časti obrazovky zvoľte šípku ukazujúcu nadol vedľa názvu projektu a potom kliknite na **Sledovanie projektu**.</span><span class="sxs-lookup"><span data-stu-id="d51e0-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="d51e0-126">Vyberte **Sledovanie úsilia** alebo **sledovanie nákladov** v rozbaľovacom zozname nad zoznamom úloh.</span><span class="sxs-lookup"><span data-stu-id="d51e0-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="d51e0-127">Dvakrát kliknite na akúkoľvek úlohu, čím ju upravíte.</span><span class="sxs-lookup"><span data-stu-id="d51e0-127">Double-click any task to edit it.</span></span> <span data-ttu-id="d51e0-128">Tiež môžete premiestniť alebo meniť veľkosť pruhy Ganttovho grafu na zmenu času a postupu úlohy.</span><span class="sxs-lookup"><span data-stu-id="d51e0-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="d51e0-129">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="d51e0-129">See Also</span></span>  
 [<span data-ttu-id="d51e0-130">Príručka projektového manažéra</span><span class="sxs-lookup"><span data-stu-id="d51e0-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
