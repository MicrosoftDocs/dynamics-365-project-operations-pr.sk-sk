---
title: Nasadenie aplikácie Project Operations – čiastočné
description: Táto téma poskytuje informácie o tom, ako nainštalovať jednoduché nasadenie Project Operations – dohoda o fakturácii pro forma.
author: stsporen
ms.date: 10/02/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cb1f1ad86e19d84d68a40b32b2fdb08dc4777a78
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995550"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="5174e-103">Nasadenie aplikácie Project Operations – čiastočné</span><span class="sxs-lookup"><span data-stu-id="5174e-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="5174e-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="5174e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="5174e-105">Project Operations podporuje viac modelov nasadenia.</span><span class="sxs-lookup"><span data-stu-id="5174e-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="5174e-106">Najlepší model nasadenia nájdete v časti [Typy nasadenia](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="5174e-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="5174e-107">Toto nasadenie, jednoduché nasadenie – dohoda o fakturácii pro forma, má za následok **Common Data Service – iba nasadenie Project Operations**.</span><span class="sxs-lookup"><span data-stu-id="5174e-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="5174e-108">Inštalácia Project Operations do nového prostredia CDS</span><span class="sxs-lookup"><span data-stu-id="5174e-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="5174e-109">Inštalácia do existujúceho prostredia CDS</span><span class="sxs-lookup"><span data-stu-id="5174e-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="5174e-110">Inštalácia Project Operations do nového prostredia CDS</span><span class="sxs-lookup"><span data-stu-id="5174e-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="5174e-111">Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou na Project Operations vytvorte nové prostredie CDS v [Centrum spravovania PowerPlatform](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="5174e-111">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="5174e-112">Uistite sa, že sú povolené **Databáza CDS** a **Aplikácie Dynamics 365** .</span><span class="sxs-lookup"><span data-stu-id="5174e-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="5174e-113">Ďalšie informácie nájdete v časti [Vytváranie a správa prostredí v centre spravovania Power Platform](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="5174e-113">For more information, see [Create and manage environments in the Power Platform admin center](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="5174e-114">Vyberte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5174e-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="5174e-115">Inštalácia Project Operations do existujúceho prostredia CDS</span><span class="sxs-lookup"><span data-stu-id="5174e-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="5174e-116">Ako [Globálny správca alebo správca Power Platform](/power-platform/admin/global-service-administrators-can-administer-without-license) s licenciou Project Operations vyhľadajte prostredie v [Centre spravovania PowerPlatform](https://admin.powerplatform.com), kde chcete nainštalovať Project Operations.</span><span class="sxs-lookup"><span data-stu-id="5174e-116">As the [Global or Power Platform Administrator](/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="5174e-117">Nainštalujte **Microsoft Dynamics 365 Project Operations** zo zoznamu nasadenia aplikácií Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="5174e-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="5174e-118">Ďalšie informácie nájdete v časti [Správa aplikácií Dynamics 365](/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="5174e-118">For more information, see [Manage Dynamics 365 apps](/power-platform/admin/manage-apps).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]