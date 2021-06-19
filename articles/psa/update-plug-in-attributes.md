---
title: Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien
description: Táto téma poskytuje informácie o aktualizácii atribútov doplnkov pre dimenzie cien.
author: Rumant
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: b0d50733340f277453f4ef5b52bdd3ee089449cd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012830"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="7fb81-103">Aktualizácia atribútov doplnkov na zahrnutie nových dimenzií cien</span><span class="sxs-lookup"><span data-stu-id="7fb81-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="7fb81-104">Ak nepoužívate program Project Service Automation (PSA) a funkcie uzatvárania zmlúv, môžete túto tému vynechať.</span><span class="sxs-lookup"><span data-stu-id="7fb81-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="7fb81-105">Pred začatím tejto témy sa predpokladá, že ste dokončili postupy v témach [Vytvorte vlastné polia a entity](create-custom-fields-entities.md), [Pridanie vlastných polí do cenového nastavenia a transakčných entít](field-references.md) a [Nastavenie vlastných polí ako dimenzií cien](set-up-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="7fb81-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="7fb81-106">Ak ste tieto postupy nedokončili, vráťte sa späť a dokončite ich a potom sa vráťte na túto tému.</span><span class="sxs-lookup"><span data-stu-id="7fb81-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="7fb81-107">Keď sa vytvorí podrobnosti riadka cenovej ponuky na stránke **Riadok cenovej ponuky** pre riadok projektovej ponuky vytvorí detail riadka cenovej ponuky, systém vytvorí dva riadky odhadu v pozadí – jeden riadok pre stranu nákladov odhadu a jeden pre predajnú stranu.</span><span class="sxs-lookup"><span data-stu-id="7fb81-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="7fb81-108">Toto je rovnaké pre riadky projektových zmlúv.</span><span class="sxs-lookup"><span data-stu-id="7fb81-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="7fb81-109">Keď vykonáte zmenu množstva alebo poľa na strane nákladov, táto zmena sa vyplní na strane predaja.</span><span class="sxs-lookup"><span data-stu-id="7fb81-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="7fb81-110">Je to možné, pretože nasledujúce doplnky musia byť znovu registrované po zmene cenových dimenzií.</span><span class="sxs-lookup"><span data-stu-id="7fb81-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="7fb81-111">PreOperationContractLineDetailUpdate - Aktualizácie **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="7fb81-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="7fb81-112">PreOperationQuoteLineDetailUpdate - Aktualizácie **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="7fb81-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="7fb81-113">Nasledujúce kroky vám vysvetlia proces registrácie doplnkov.</span><span class="sxs-lookup"><span data-stu-id="7fb81-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="7fb81-114">Otvorte **PluginRegistrationTool** a pripojte sa k online inštancii.</span><span class="sxs-lookup"><span data-stu-id="7fb81-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="7fb81-115">Vyberte položku **Hľadať** a vyhľadajte doplnok, ktorý chcete aktualizovať.</span><span class="sxs-lookup"><span data-stu-id="7fb81-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Snímka obrazovky zo stromu vyhľadávania](media/PRT-1.png)

3. <span data-ttu-id="7fb81-117">Po rozpoznaní doplnku ho označte a potom kliknite na možnosť **Vybrať na hlavnom formulári**.</span><span class="sxs-lookup"><span data-stu-id="7fb81-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="7fb81-118">Vyberte krok doplnku, ktorý chcete aktualizovať, kliknite pravým tlačidlom myši a potom vyberte položku **aktualizovať.**</span><span class="sxs-lookup"><span data-stu-id="7fb81-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Snímka obrazovky doplnku určeného na aktualizáciu](media/PRT-2.png)
 
5. <span data-ttu-id="7fb81-120">V okne aktualizácia kliknite na tri bodky (**...**) v atribútoch filtrovania.</span><span class="sxs-lookup"><span data-stu-id="7fb81-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Snímka obrazovka z aktualizácie existujúceho kroku informácií konfigurácie](media/PRT-3.png)
 
6. <span data-ttu-id="7fb81-122">Začiarknite políčka atribút ceny.</span><span class="sxs-lookup"><span data-stu-id="7fb81-122">Select the pricing attribute check boxes.</span></span>

 ![Snímka obrazovka znázorňujúce označenie začiarkávacieho poľa atribútov ceny](media/PRT-4.png)

7. <span data-ttu-id="7fb81-124">Kliknite na tlačidlo **OK** pre stránky a potom vyberte **Aktualizovať**.</span><span class="sxs-lookup"><span data-stu-id="7fb81-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Snímka obrazovky zobrazujúca tlačidlo „Aktualizovať”](media/PRT-5.png)
 
8. <span data-ttu-id="7fb81-126">Tento postup zopakujte pri druhom doplnku, **PreOperationQuoteLineDetail - Aktualizácia msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="7fb81-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="7fb81-127">Zatvorte registračný nástroj doplnku.</span><span class="sxs-lookup"><span data-stu-id="7fb81-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]