---
title: Integrácia duálneho zápisu Project Operations
description: Táto téma poskytuje prehľad integrácie duálneho zápisu Project Operations.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998700"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="21a69-103">Prehľad integrácie duálneho zápisu Project Operations</span><span class="sxs-lookup"><span data-stu-id="21a69-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="21a69-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="21a69-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="21a69-105">Project Operations využíva [možnosti duálneho zápisu](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) na synchronizáciu údajov naprieč Microsoft Dataverse a Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="21a69-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="21a69-106">Nasledujúca ilustrácia ukazuje, ako sa synchronizujú údaje ako súčasť tejto integrácie medzi Dataverse a Finance.</span><span class="sxs-lookup"><span data-stu-id="21a69-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Prehľad tokov údajov Project Operations](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="21a69-108">Project Operations v Dataverse poskytujú moderné používateľské rozhranie (UI) a ľahkú rozšíriteľnosť bez kódu/s nízkym kódom pomocou možností Power Platform.</span><span class="sxs-lookup"><span data-stu-id="21a69-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="21a69-109">Projektoví manažéri, manažéri zdrojov, členovia projektového tímu a ďalšie osobnosti front-office vykonávajú svoje činnosti v rámci Project Operations v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="21a69-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="21a69-110">Project Operations vo Finance poskytuje podporu projektového účtovníctva a uznávania výnosov.</span><span class="sxs-lookup"><span data-stu-id="21a69-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="21a69-111">Project Operations sa pripájajú k finančnému rámcu v Finance pre výpočet dane z obratu, výmenné kurzy, vykazovanie finančnej dimenzie a ďalšie.</span><span class="sxs-lookup"><span data-stu-id="21a69-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="21a69-112">Skúsenosti účtovníka projektu sú väčšinou založené v nástroji Finance.</span><span class="sxs-lookup"><span data-stu-id="21a69-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="21a69-113">Integrácia Project Operations pozostáva z nasledujúcej integrácie komponentov:</span><span class="sxs-lookup"><span data-stu-id="21a69-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="21a69-114">Integrácia nastavenia a konfiguračných údajov aplikácie Project Operations</span><span class="sxs-lookup"><span data-stu-id="21a69-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="21a69-115">Odhady a skutočné hodnoty projektu</span><span class="sxs-lookup"><span data-stu-id="21a69-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="21a69-116">Projektové faktúry</span><span class="sxs-lookup"><span data-stu-id="21a69-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="21a69-117">Správa výdavkov</span><span class="sxs-lookup"><span data-stu-id="21a69-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="21a69-118">Faktúra dodávateľa</span><span class="sxs-lookup"><span data-stu-id="21a69-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
