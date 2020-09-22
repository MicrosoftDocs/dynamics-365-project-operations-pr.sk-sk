---
title: Konfigurujte doplňujúce parametre nastavenia
description: Ako na konfiguráciu dodatočných nastavení parametrov v Project Service
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 03/24/2020
ms.locfileid: "3755679"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="8cb42-103">Konfigurácia dodatočných nastavení parametrov (Project Service)</span><span class="sxs-lookup"><span data-stu-id="8cb42-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="8cb42-104">Akonáhle ste nastavili položky v predchádzajúcich témach, musíte nastaviť ďalšie parametre projektu na použitie pri projektoch.</span><span class="sxs-lookup"><span data-stu-id="8cb42-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="8cb42-105">Pri prvej inštalácii [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], ste vytvorili nastavenia parametrov, aby najprv vytvorili všetky záznamy potrebné pre prevádzku [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)].</span><span class="sxs-lookup"><span data-stu-id="8cb42-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="8cb42-106">Teraz je čas sa vrátiť a nastaviť ďalšie polia pre tieto nastavenia.</span><span class="sxs-lookup"><span data-stu-id="8cb42-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="8cb42-107">Budete musieť nakonfigurovať nasledujúce nastavenia:</span><span class="sxs-lookup"><span data-stu-id="8cb42-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="8cb42-108">Organizačná jednotka</span><span class="sxs-lookup"><span data-stu-id="8cb42-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="8cb42-109">Frekvencia faktúr</span><span class="sxs-lookup"><span data-stu-id="8cb42-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="8cb42-110">Šablóna pracovnej doby</span><span class="sxs-lookup"><span data-stu-id="8cb42-110">Work hours template</span></span>  
  
-   <span data-ttu-id="8cb42-111">Cenník</span><span class="sxs-lookup"><span data-stu-id="8cb42-111">Price list</span></span>  
 
<span data-ttu-id="8cb42-112">V tomto kroku tiež zadáte, ktorý typ pridelenia zdroja chcete:</span><span class="sxs-lookup"><span data-stu-id="8cb42-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="8cb42-113">**Centrálne**.</span><span class="sxs-lookup"><span data-stu-id="8cb42-113">**Central**.</span></span> <span data-ttu-id="8cb42-114">Iba manažéri zdrojov môžete prideliť zdroje k projektom.</span><span class="sxs-lookup"><span data-stu-id="8cb42-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="8cb42-115">**Hybridné**.</span><span class="sxs-lookup"><span data-stu-id="8cb42-115">**Hybrid**.</span></span> <span data-ttu-id="8cb42-116">Správcovia zdrojov, projektoví manažéri a správcovia účtu môžu prideliť zdroje k projektom.</span><span class="sxs-lookup"><span data-stu-id="8cb42-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="8cb42-117">Nastavenie projektových parametrov:</span><span class="sxs-lookup"><span data-stu-id="8cb42-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="8cb42-118">Prejdite na **Project Service > Parametre.**</span><span class="sxs-lookup"><span data-stu-id="8cb42-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="8cb42-119">Kliknite na nastavenie parametrov, ktoré chcete nakonfigurovať (tie, ktoré ste vytvorili pre prvú inštaláciu [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), alebo kliknite na tlačidlo **Nové** a vytvorte nový.</span><span class="sxs-lookup"><span data-stu-id="8cb42-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="8cb42-120">V oblasti **Všeobecné** nastavte všetky možnosti parametrov projektu.</span><span class="sxs-lookup"><span data-stu-id="8cb42-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="8cb42-121">V oblasti **Cenník** kliknite na **+**, čím pridáte cenník. V rozbaľovacom zozname **Cenník parametrov projektu** si vyberte cenník a kliknite na možnosť **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="8cb42-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="8cb42-122">Kliknite na tlačidlo **Uložiť** v pravom dolnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="8cb42-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="8cb42-123">Aby služba Project Service fungovala správne, musí sa zachovať záznam parametrov projektu.</span><span class="sxs-lookup"><span data-stu-id="8cb42-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="8cb42-124">Tento záznam by sa nemal vymazať.</span><span class="sxs-lookup"><span data-stu-id="8cb42-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="8cb42-125">Pozrite si tiež</span><span class="sxs-lookup"><span data-stu-id="8cb42-125">See Also</span></span>  
 [<span data-ttu-id="8cb42-126">Nastavenie prostriedkov</span><span class="sxs-lookup"><span data-stu-id="8cb42-126">Set up resources</span></span>](../project-service/set-up-resources.md)
