---
title: Poskytovať odhad práce na projekt počas procesu predaja
description: Ako poskytnúť odhad prác pre projekt počas procesu predaja v Project Service
author: ruhercul
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
ms.openlocfilehash: d1daff101f9f0342bb691253fee1290d2335318c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998250"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="63135-103">Poskytovať práce odhaduje na projekt počas procesu predaja (Project Service)</span><span class="sxs-lookup"><span data-stu-id="63135-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="63135-104">Počas procesu predaja si môžete vypracovať predajné odhady od základov prostredníctvom riadkov cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="63135-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="63135-105">Možnosti[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] v [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] poskytujú vedeckejšie a určujúcejšie spôsoby prichádzania s odhadmi predajov rozložením pracovných položiek a priradením relevantných atribútov, ktoré prispievajú k odhadom projektu v štruktúre rozdelenia práce.</span><span class="sxs-lookup"><span data-stu-id="63135-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="63135-106">Keď vyhráte predaja, môžete použiť štruktúry rozdelenia práce spojené v plán projektu, pričom ich môžete podľa potreby upraviť pre úspešné dokončenie svojho projektu.</span><span class="sxs-lookup"><span data-stu-id="63135-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="63135-107">Prepojenie projektu s riadkom cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="63135-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="63135-108">Pri tvorbe riadku cenovej ponuky projektu, môžete vytvoriť nový projekt z riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="63135-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="63135-109">Potom môžete použiť šablóny projektu, ktoré sú vopred nakonfigurované štandardné projektové plány a finančné odhady spoločnej organizácii, alebo kópiu plánu projektu a odhady z minulých projektov.</span><span class="sxs-lookup"><span data-stu-id="63135-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="63135-110">Keď vytvoríte projekt, vybrať šablónu projektu poskytuje ponúka základ na spresnenie požiadavky plánu, odhady a úlohy projektu.</span><span class="sxs-lookup"><span data-stu-id="63135-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="63135-111">Vytvorením projektu od cenovej ponuky sa projekt automaticky priradí k riadku cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="63135-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="63135-112">Súčasťami odhadu projektu</span><span class="sxs-lookup"><span data-stu-id="63135-112">Project estimate components</span></span>  
 <span data-ttu-id="63135-113">Štruktúry rozdelenia práce v projekte poskytuje spôsob, ako rozdeliť prácu na úlohy, hierarchia úloh a priradiť odhad úsilie potrebné na dokončenie každej úlohy.</span><span class="sxs-lookup"><span data-stu-id="63135-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="63135-114">Môžete tiež priradiť úlohy k úlohe na uvedenie odhad typ zdroja, ktoré sú potrebné na dokončenie úlohy a harmonogram.</span><span class="sxs-lookup"><span data-stu-id="63135-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="63135-115">Štruktúry rozdelenia práce vám pomôžu určiť odhady pracovného úsilia a plánovania.</span><span class="sxs-lookup"><span data-stu-id="63135-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="63135-116">Projekt predvolene používa predvolený cenník, ktorý ste určili predtým.</span><span class="sxs-lookup"><span data-stu-id="63135-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="63135-117">Náklady a predajných cien definovaných v cenníkoch pomôžu určiť finančné odhady pre rozdelenie práce projektu.</span><span class="sxs-lookup"><span data-stu-id="63135-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="63135-118">Ak je váš projekt spojený s cenovou ponukou, ktorá obsahuje iný cenník než je predvolený, ponuka cenník sa používa pre finančné odhady.</span><span class="sxs-lookup"><span data-stu-id="63135-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="63135-119">Import odhadov z projektu do cenovej ponuky</span><span class="sxs-lookup"><span data-stu-id="63135-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="63135-120">Akonáhle budete mať projekt odhadov v projekte, môžete importovať tieto odhady do riadku dopytu:</span><span class="sxs-lookup"><span data-stu-id="63135-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="63135-121">V **Podrobnosti riadku cenovej ponuky**, kliknite na tlačidlo **Import z odhadov**.</span><span class="sxs-lookup"><span data-stu-id="63135-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="63135-122">Vyberte, či chcete importovať projekt odhady zhrnuté typ transakcie, úlohu alebo prácu rozpis rozdelenia práce na úrovni uzla.</span><span class="sxs-lookup"><span data-stu-id="63135-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="63135-123">Pozrite si tiež:</span><span class="sxs-lookup"><span data-stu-id="63135-123">See Also</span></span>  
 [<span data-ttu-id="63135-124">Príručka projektového manažéra</span><span class="sxs-lookup"><span data-stu-id="63135-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]