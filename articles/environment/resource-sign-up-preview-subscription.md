---
title: Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov
description: Táto téma poskytuje informácie o tom, ako sa prihlásiť na odber a nasadiť Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949072"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="2f9d0-103">Registrácia na odber ukážky Project Operations pre scenáre zdrojov/chýbajúcich zdrojov</span><span class="sxs-lookup"><span data-stu-id="2f9d0-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="2f9d0-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="2f9d0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="2f9d0-105">Táto téma vysvetľuje, ako sa prihlásiť na odber ukážky/ponuky partnera a nasadiť prostredie Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2f9d0-106">Predpoklady</span><span class="sxs-lookup"><span data-stu-id="2f9d0-106">Prerequisites</span></span>

- <span data-ttu-id="2f9d0-107">Dostanete e-mail s pozvánkou na účasť v ukážke.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="2f9d0-108">O ukážku môžete požiadať na [webovej stránke Project Operations](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="2f9d0-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="2f9d0-109">Používateľ, ktorý nasadí ukážku, musí mať práva globálneho správcu nájomníka platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="2f9d0-110">Nasadenie finančného prostredia vyžaduje platné predplatné služieb Azure, ktoré sa bude fakturovať za každé prostredie.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="2f9d0-111">Na začiatok môžete použiť existujúce predplatné svojich organizácií alebo použiť [skúšobnú verziu Azure](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="2f9d0-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="2f9d0-112">Prostredie CDS bude počas obmedzeného obdobia 30 dní poskytovaný zadarmo.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="2f9d0-113">Prihlásiť sa na odber</span><span class="sxs-lookup"><span data-stu-id="2f9d0-113">Subscribe</span></span>

<span data-ttu-id="2f9d0-114">Keď je vaše schválenie [žiadosti o ukážku](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) schválené, dostanete e-mailom dve ponuky od spoločnosti Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="2f9d0-115">Tieto ponuky vám umožňujú nasadiť ukážku Project Operations:</span><span class="sxs-lookup"><span data-stu-id="2f9d0-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="2f9d0-116">Dynamics 365 Project Operations – skúšobná verzia ukážky</span><span class="sxs-lookup"><span data-stu-id="2f9d0-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="2f9d0-117">Skúšobná verzia ukážky Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f9d0-118">Túto úlohu musí vykonať iba jedna osoba, správca nájomníka v organizácii.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="2f9d0-119">Ak nie ste predplatiteľom tohto vydania, počkajte, kým nebude zaregistrovaná vaša organizácia a kým dostanete svoje prihlasovacie údaje.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="2f9d0-120">Dynamics 365 Project Operations – skúšobná verzia ukážky</span><span class="sxs-lookup"><span data-stu-id="2f9d0-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="2f9d0-121">Uplatnite prvú ponuku, **skúšobnú verziu Dynamics 365 Project Operations** s adresou URL uvedenou v uvítacom e-maile.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Prvá ponuka](./media/1FirstOffer.png)

2. <span data-ttu-id="2f9d0-123">Skontrolujte, či ste prihlásený ako používateľ, ktorý patrí k organizácii, ktorá si predplatí službu.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="2f9d0-124">Pokračujte v uplatnení ponuky.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="2f9d0-125">Vyberte **Áno, pridať do môjho účtu**.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-125">Select **Yes, add it to my account**.</span></span>

![Uplatniť ponuku](./media/2RedeemFirstOffer.png)

![Potvrdiť ponuku](./media/3ConfirmFirstOffer.png)

![Ponuka uplatnená](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="2f9d0-129">Skúšobná verzia ukážky Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="2f9d0-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="2f9d0-130">Rovnaké kroky zopakujte aj pri druhej ponuke z uvítacieho e-mailu.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="2f9d0-131">Priradenie licencií</span><span class="sxs-lookup"><span data-stu-id="2f9d0-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2f9d0-132">Na dokončenie nasledujúcich krokov budete potrebovať prístup správcu k Office 365 vo vašej organizácii .</span><span class="sxs-lookup"><span data-stu-id="2f9d0-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="2f9d0-133">Prejdite na [Centrum pre správu Microsoft 365](https://portal.office.com/) na pridelenie licencií vašim používateľom.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![Portál na správu služieb Office](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="2f9d0-135">Na stránke **Aktívni používatelia** vyberte používateľov, ktorým chcete priradiť licenciu.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Priradenie licencií](./media/6AssignLicenses.png)

3. <span data-ttu-id="2f9d0-137">Skontrolujte, či bola vybratá licencia Project Operations, a vyberte **Uložiť zmeny**.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="2f9d0-138">Ponuku na vyskúšanie služby Finance nie je potrebné priradiť používateľovi.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="2f9d0-139">Začatie nového projektu v LCS</span><span class="sxs-lookup"><span data-stu-id="2f9d0-139">Start a new project in LCS</span></span>

<span data-ttu-id="2f9d0-140">Vytvorte nový projekt LCS podľa popisu v téme [Začatie nového projektu v LCS](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="2f9d0-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="2f9d0-141">Pridanie predplatného služieb Azure do projektu LCS</span><span class="sxs-lookup"><span data-stu-id="2f9d0-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="2f9d0-142">Pri dokončení tejto úlohy postupujte podľa pokynov v téme [Pridanie predplatného služieb Azure do projektu LCS](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="2f9d0-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="2f9d0-143">Nasadenie ukážky prostredia Finance s Project Operations pre scenáre zdrojov/chýbajúcich zdrojov</span><span class="sxs-lookup"><span data-stu-id="2f9d0-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="2f9d0-144">Postupujte podľa pokynov v téme [Zriadenie nového prostredia](resource-provision-new-environment.md) na dokončenie nasadenia.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="2f9d0-145">Použite typ nasadenia [ukážkové prostredie](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) pre ukážku.</span><span class="sxs-lookup"><span data-stu-id="2f9d0-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="2f9d0-146">Inštalácia údajov CDS pre nastavenie a konfiguráciu</span><span class="sxs-lookup"><span data-stu-id="2f9d0-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="2f9d0-147">Nainštalujte údaje pre nastavenie a konfiguráciu CDS podľa popisu v téme [Nastavenie a použitie konfiguračných údajov v Common Data Service](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="2f9d0-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

