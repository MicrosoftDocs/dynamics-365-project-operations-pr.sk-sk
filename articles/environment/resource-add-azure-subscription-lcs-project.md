---
title: Pridanie predplatného služieb Azure do projektu LCS
description: Táto téma poskytuje informácie o tom, ako pripojiť vaše predplatné služieb Azure k projektu LCS.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289928"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="a7225-103">Pridanie predplatného služieb Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="a7225-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="a7225-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="a7225-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="a7225-105">Prostredia hosťované v cloude musia byť nasadené pomocou existujúceho predplatného služieb Azure.</span><span class="sxs-lookup"><span data-stu-id="a7225-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="a7225-106">Táto téma vysvetľuje, ako pripojiť vaše existujúce predplatné služieb Azure k projektu LCS.</span><span class="sxs-lookup"><span data-stu-id="a7225-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="a7225-107">Udelenie súhlasu správcu</span><span class="sxs-lookup"><span data-stu-id="a7225-107">Grant admin consent</span></span>

1. <span data-ttu-id="a7225-108">V projekte LCS v časti **Prostredia** vyberte **Nastavenia Microsoft Azure**.</span><span class="sxs-lookup"><span data-stu-id="a7225-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![Nastavenia aplikácie Microsoft Azure](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="a7225-110">Na stránke **Nastavenia projektu** na karte **Konektory Azure** vyberte **Povoliť**.</span><span class="sxs-lookup"><span data-stu-id="a7225-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="a7225-111">Potom bude možné nasadiť prostredia do tohto projektu.</span><span class="sxs-lookup"><span data-stu-id="a7225-111">This allows environments to be deployed to this project.</span></span>

![Konektory Azure](./media/2AzureConnectors.png)

3. <span data-ttu-id="a7225-113">Znova vyberte **Povoliť** na poskytnutie súhlasu správcu.</span><span class="sxs-lookup"><span data-stu-id="a7225-113">Select **Authorize** again to provide admin consent.</span></span>

![Udelenie súhlasu správcu](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="a7225-115">Prijmite žiadosť o povolenie.</span><span class="sxs-lookup"><span data-stu-id="a7225-115">Accept the permissions request.</span></span>

![Prijmite žiadosť o povolenie](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="a7225-117">Autorizácia je teraz hotová.</span><span class="sxs-lookup"><span data-stu-id="a7225-117">The authorization is now complete.</span></span> 

![Autorizácia bola úspešná](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="a7225-119">Poskytnite službe Dynamics Deployment Services prístup k vášmu predplatnému služieb Azure</span><span class="sxs-lookup"><span data-stu-id="a7225-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="a7225-120">Prejdite do ponuky [Fakturácia Microsoft Azure](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) a zvoľte svoje predplatné.</span><span class="sxs-lookup"><span data-stu-id="a7225-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="a7225-121">Aby mohla služba Dynamics Deployment Services nasadiť prostredia, musí mať prístup k tomuto predplatnému.</span><span class="sxs-lookup"><span data-stu-id="a7225-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![Podrobnosti o predplatnom služieb Azure](./media/6AzureSubscription.png)

2. <span data-ttu-id="a7225-123">Na navigačnej table vyberte **Kontrola prístupu (IAM)** a potom vyberte **Pridať priradenie roly**.</span><span class="sxs-lookup"><span data-stu-id="a7225-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="a7225-124">V posúvači na pravej strane vyberte **Rola prispievateľa** a v uvedenom zozname vyhľadajte a vyberte **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="a7225-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="a7225-125">Vyberte položku **Uložiť**.</span><span class="sxs-lookup"><span data-stu-id="a7225-125">Select **Save**.</span></span>

![Prístup k predplatnému](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="a7225-127">Pridajte konektor predplatného do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="a7225-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="a7225-128">Vo projekte LCS na stránke **Nastavenia Microsoft Azure** vyberte **Pridať** na pridanie nového konektora.</span><span class="sxs-lookup"><span data-stu-id="a7225-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="a7225-129">Zadajte svoje ID predplatného Azure.</span><span class="sxs-lookup"><span data-stu-id="a7225-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="a7225-130">Svoje ID predplatného Azure nájdete na [portáli Azure](https://ms.portal.azure.com/) v časti **Nastavenia** v ľavom dolnom rohu obrazovky.</span><span class="sxs-lookup"><span data-stu-id="a7225-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="a7225-131">V poli **Nakonfigurovať použitie Azure Resource Manager** vyberte **Áno**.</span><span class="sxs-lookup"><span data-stu-id="a7225-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="a7225-132">Uistite sa, že sa predplatné Azure AAD Tenant Domain zhoduje s predplatným Azure s vlastníctvom domény, ktoré používate, a vyberte **Ďalej**.</span><span class="sxs-lookup"><span data-stu-id="a7225-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="a7225-133">Na obrazovke **Nastaviť Microsoft Azure** zvoľte **Ďalej** na potvrdenie.</span><span class="sxs-lookup"><span data-stu-id="a7225-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="a7225-134">Ak sa vám na tejto obrazovke zobrazí chyba, vráťte sa do sekcie [Poskytnúť službe Dynamics Deployment Services prístup k predplatnému Azure](#provide) v tejto téme a uistite sa, že ste dokončili všetky kroky.</span><span class="sxs-lookup"><span data-stu-id="a7225-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="a7225-135">Stiahnite si certifikát Azure Management do lokálneho priečinka vo vašom počítači a potom ho nahrajte na portál Azure Management Portal prechodom do časti **Nastavenia** > **Certifikáty pre správu**.</span><span class="sxs-lookup"><span data-stu-id="a7225-135">Download the Azure Management Certificate to a local folder on your computer, and then upload it to Azure Management Portal by going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="a7225-136">Tento certifikát umožní spoločnosti LCS komunikovať s Azure vo vašom mene.</span><span class="sxs-lookup"><span data-stu-id="a7225-136">This certificate will enable LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="a7225-137">Tento krok môžete preskočiť, ak má váš používateľ prístup k predplatnému.</span><span class="sxs-lookup"><span data-stu-id="a7225-137">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="a7225-138">Vyberte **Ďalej**.</span><span class="sxs-lookup"><span data-stu-id="a7225-138">Select  **Next**.</span></span>
8. <span data-ttu-id="a7225-139">Vyberte oblasť Azure, do ktorého chcete vykonať nasadenie a vyberte údajové centrum, ktoré je blízko miesta, kde plánujete tento systém používať.</span><span class="sxs-lookup"><span data-stu-id="a7225-139">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="a7225-140">Vyberte možnosť **Pripojiť**.</span><span class="sxs-lookup"><span data-stu-id="a7225-140">Select  **Connect**.</span></span>

<span data-ttu-id="a7225-141">Úspešne ste pripojili svoje predplatné služieb Azure.</span><span class="sxs-lookup"><span data-stu-id="a7225-141">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="a7225-142">Teraz môžete nasadiť prostredia Dynamics 365 Finance hosťované na cloude.</span><span class="sxs-lookup"><span data-stu-id="a7225-142">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]