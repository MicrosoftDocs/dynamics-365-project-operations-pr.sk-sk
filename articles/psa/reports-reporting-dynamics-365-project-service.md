---
title: Domovská stránka vykazovania
description: Táto téma poskytuje informácie o vykazovaní v Dynamics 365 Project Service Automation.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 25486b0c153842cab4331f27eea4872f848bea50
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147717"
---
# <a name="reporting-home-page"></a><span data-ttu-id="08b30-103">Domovská stránka vykazovania</span><span class="sxs-lookup"><span data-stu-id="08b30-103">Reporting home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="08b30-104">Microsoft Dynamics 365 Project Service Automation umožňuje projektovým organizáciám efektívne riadiť operácie ich podnikania.</span><span class="sxs-lookup"><span data-stu-id="08b30-104">Microsoft Dynamics 365 Project Service Automation lets project-based organizations efficiently manage the operations of their business.</span></span> <span data-ttu-id="08b30-105">Na akomkoľvek projekte, členovia tímu musia riadiť príležitosť, cenovú ponuku a plánovanie práce, zdroj projektov, riadiť prácu podľa plánu, fakturácia práce a potom vykonajte práce potrebné na dokončenie projektu.</span><span class="sxs-lookup"><span data-stu-id="08b30-105">On any project, team members must manage the opportunity, quote and plan the work, resource the projects, manage the work according to the plan, bill for the work, and then do the work to complete the project.</span></span> <span data-ttu-id="08b30-106">Schopnosť správy o operáciách je kľúčom k určiteľnosti zdravotného stavu organizácie a prijatím akýchkoľvek nápravných opatrení, ktoré je potrebné.</span><span class="sxs-lookup"><span data-stu-id="08b30-106">The ability to report on operations is key to determining the health of the organization and taking any corrective action that's required.</span></span> <span data-ttu-id="08b30-107">PSA používa využíva Microsoft Dynamics 365 metódy a technológie pre všetky svoje vykazovania.</span><span class="sxs-lookup"><span data-stu-id="08b30-107">PSA uses Microsoft Dynamics 365 reporting methods and technologies for all its reporting.</span></span> <span data-ttu-id="08b30-108">Viac informácií o možnostiach vykazovania nájdete na stránke [Sprievodca písaním správ pre Dynamics 365 Customer Engagement (on-premises), verzia 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span><span class="sxs-lookup"><span data-stu-id="08b30-108">For more information about the options for reporting, see the [Report writing guide for Dynamics 365 Customer Engagement (on-premises), version 9](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/reporting-analytics-with-dynamics-365).</span></span>

## <a name="report-wizard"></a><span data-ttu-id="08b30-109">Sprievodca zostavou</span><span class="sxs-lookup"><span data-stu-id="08b30-109">Report Wizard</span></span>

<span data-ttu-id="08b30-110">Sprievodca zostavou umožňuje nevývojárom vytvárať jednoduché zostavy.</span><span class="sxs-lookup"><span data-stu-id="08b30-110">The Report Wizard lets non-developers create simple reports.</span></span> <span data-ttu-id="08b30-111">Keďže je aplikácia postavená na existujúcej platforme, skúsenosť je rovnaká ako skúsenosť, ktorá je zdokumentovaná v časti [Vytvorenie alebo úprava zostavy pomocou Sprievodcu zostavou](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span><span class="sxs-lookup"><span data-stu-id="08b30-111">Because the app is built on an existing platform, the experience is the same as the experience that is documented in [Create or edit a report using the Report Wizard](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/basics/create-edit-copy-report-wizard).</span></span> <span data-ttu-id="08b30-112">Avšak, budete používať špecifické entity Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="08b30-112">However, you will use the Project Service Automation-specific entities.</span></span>

## <a name="custom-sql-server-reporting-services-reports"></a><span data-ttu-id="08b30-113">Vlastné zostavy SQL Server Reporting Services</span><span class="sxs-lookup"><span data-stu-id="08b30-113">Custom SQL Server Reporting Services reports</span></span>

<span data-ttu-id="08b30-114">Ak vaša firma vyžaduje konkrétnu zostavu, ktorú nie je možné vytvoriť pomocou sprievodcu zostavou, môžete vytvárať vlastnú zostavu.</span><span class="sxs-lookup"><span data-stu-id="08b30-114">If your business requires a specific report that can't be created by using the Report Wizard, you can create a custom report.</span></span> <span data-ttu-id="08b30-115">Musíte mať nainštalovaný Microsoft Visual Studio, spolu s príslušnými rozšíreniami Microsoft SQL Server Data Tools a Report Authoring.</span><span class="sxs-lookup"><span data-stu-id="08b30-115">You must have Microsoft Visual Studio installed, together with the appropriate Microsoft SQL Server Data Tools and Report Authoring Extensions.</span></span> <span data-ttu-id="08b30-116">Ďalšie informácie o nástrojoch a verziách nájdete v téme [Prostredie zápisu zostavy pomocou SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span><span class="sxs-lookup"><span data-stu-id="08b30-116">For more information about tools and versions, see [Report writing environment using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/report-writing-environment-using-sql-server-data-tools).</span></span> <span data-ttu-id="08b30-117">Informácie o vytvorení vlastnej zostavy nájdete v téme [Vytvoriť novú zostavu pomocou SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools)</span><span class="sxs-lookup"><span data-stu-id="08b30-117">For information about how to create a custom report, see [Create a new report using SQL Server Data Tools](https://docs.microsoft.com/dynamics365/customerengagement/on-premises/analytics/create-a-new-report-using-sql-server-data-tools).</span></span>

## <a name="power-bi-insights-apps"></a><span data-ttu-id="08b30-118">Aplikácie Power BI Insights</span><span class="sxs-lookup"><span data-stu-id="08b30-118">Power BI insights apps</span></span>

<span data-ttu-id="08b30-119">Spoločnosť Microsoft Power BI a Dynamics 365 spolu poskytujú účinný spôsob práce s vašimi údajmi vo forme aplikácií Insights.</span><span class="sxs-lookup"><span data-stu-id="08b30-119">Together, Microsoft Power BI and Dynamics 365 give you a powerful way to work with your data, in the form of insights apps.</span></span> <span data-ttu-id="08b30-120">Informácie o dostupnosti aplikácií Insights nájdete na [Stránke aplikácií Power BI Insights](https://powerbi.microsoft.com/power-bi-insights-apps/).</span><span class="sxs-lookup"><span data-stu-id="08b30-120">For information about the availability of insights apps, see the [Power BI insights apps page](https://powerbi.microsoft.com/power-bi-insights-apps/).</span></span>


## <a name="additional-resources"></a><span data-ttu-id="08b30-121">Ďalšie zdroje</span><span class="sxs-lookup"><span data-stu-id="08b30-121">Additional resources</span></span>
<span data-ttu-id="08b30-122">Ďalšie informácie o hlásení v PSA nájdete v nasledujúcich témach:</span><span class="sxs-lookup"><span data-stu-id="08b30-122">For more information about reporting in PSA, see the following topics:</span></span>

- [<span data-ttu-id="08b30-123">Práca s dátovým modelom Project Service</span><span class="sxs-lookup"><span data-stu-id="08b30-123">Working with the Project Service data model</span></span>](reports-working-project-service-data-model.md)
- [<span data-ttu-id="08b30-124">Tabule</span><span class="sxs-lookup"><span data-stu-id="08b30-124">Dashboards</span></span>](reports-dashboards.md)

