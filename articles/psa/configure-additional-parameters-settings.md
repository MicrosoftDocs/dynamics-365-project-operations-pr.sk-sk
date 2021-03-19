---
title: Konfigurujte doplňujúce parametre nastavenia
description: Ako na konfiguráciu dodatočných nastavení parametrov v Project Service
author: JohnPBurrows
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
ms.openlocfilehash: bac484e29f1a0578042f350b1657a42e80b48cb4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290783"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="2721a-103">Konfigurácia dodatočných nastavení parametrov (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2721a-103">Configure additional parameter settings (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2721a-104">Akonáhle ste nastavili položky v predchádzajúcich témach, musíte nastaviť ďalšie parametre projektu na použitie pri projektoch.</span><span class="sxs-lookup"><span data-stu-id="2721a-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="2721a-105">Pri prvej inštalácii [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ste vytvorili nastavenia parametrov, aby najprv vytvorili všetky záznamy potrebné pre prevádzku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="2721a-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="2721a-106">Teraz je čas sa vrátiť a nastaviť ďalšie polia pre tieto nastavenia.</span><span class="sxs-lookup"><span data-stu-id="2721a-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="2721a-107">Budete musieť nakonfigurovať nasledujúce nastavenia:</span><span class="sxs-lookup"><span data-stu-id="2721a-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="2721a-108">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="2721a-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="2721a-109">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="2721a-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="2721a-110">Šablóna pracovnej doby</span><span class="sxs-lookup"><span data-stu-id="2721a-110">Work hours template</span></span>  
  
-   <span data-ttu-id="2721a-111">Cenník</span><span class="sxs-lookup"><span data-stu-id="2721a-111">Price list</span></span>  
 
<span data-ttu-id="2721a-112">V tomto kroku tiež zadáte, ktorý typ pridelenia zdroja chcete:</span><span class="sxs-lookup"><span data-stu-id="2721a-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="2721a-113">**Centrálne**.</span><span class="sxs-lookup"><span data-stu-id="2721a-113">**Central**.</span></span> <span data-ttu-id="2721a-114">Iba manažéri zdrojov môžete prideliť zdroje k projektom.</span><span class="sxs-lookup"><span data-stu-id="2721a-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="2721a-115">**Hybridné**.</span><span class="sxs-lookup"><span data-stu-id="2721a-115">**Hybrid**.</span></span> <span data-ttu-id="2721a-116">Správcovia zdrojov, projektoví manažéri a správcovia účtu môžu prideliť zdroje k projektom.</span><span class="sxs-lookup"><span data-stu-id="2721a-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="2721a-117">Nastavenie projektových parametrov:</span><span class="sxs-lookup"><span data-stu-id="2721a-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="2721a-118">Prejdite na **Project Service > Parametre.**</span><span class="sxs-lookup"><span data-stu-id="2721a-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="2721a-119">Kliknite na nastavenie parametrov, ktoré chcete nakonfigurovať (tie, ktoré ste vytvorili pre prvú inštaláciu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), alebo kliknite na tlačidlo **Nové** a vytvorte nový.</span><span class="sxs-lookup"><span data-stu-id="2721a-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="2721a-120">V oblasti **Všeobecné** nastavte všetky možnosti parametrov projektu.</span><span class="sxs-lookup"><span data-stu-id="2721a-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="2721a-121">V oblasti **Cenník** kliknite na **+**, čím pridáte cenník. V rozbaľovacom zozname **Cenník parametrov projektu** si vyberte cenník a kliknite na možnosť **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="2721a-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="2721a-122">Kliknite na tlačidlo **Uložiť** v pravom dolnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="2721a-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="2721a-123">Aby služba Project Service fungovala správne, musí sa zachovať záznam parametrov projektu.</span><span class="sxs-lookup"><span data-stu-id="2721a-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="2721a-124">Tento záznam by sa nemal vymazať.</span><span class="sxs-lookup"><span data-stu-id="2721a-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="2721a-125">Pozrite si tiež</span><span class="sxs-lookup"><span data-stu-id="2721a-125">See Also</span></span>  
 [<span data-ttu-id="2721a-126">Nastavenie prostriedkov</span><span class="sxs-lookup"><span data-stu-id="2721a-126">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]