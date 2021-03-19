---
title: Prehľad medzipodnikovej fakturácie
description: Táto téma poskytuje informácie a príklady medzipodnikovej fakturácie pre projekty.
author: sigitac
manager: tfehr
ms.date: 11/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 3ad75089de1a2f99646f7aba213e199a2bec347d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287347"
---
# <a name="intercompany-invoicing-overview"></a><span data-ttu-id="172aa-103">Prehľad medzipodnikovej fakturácie</span><span class="sxs-lookup"><span data-stu-id="172aa-103">Intercompany invoicing overview</span></span>

<span data-ttu-id="172aa-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="172aa-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="172aa-105">Vaša organizácia môže mať viac divízií, dcérskych spoločností a ďalších právnych subjektov, ktoré si navzájom prenášajú produkty a služby na účely projektov.</span><span class="sxs-lookup"><span data-stu-id="172aa-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="172aa-106">Právnická osoba, ktorá poskytuje službu alebo produkt, sa nazýva *požičiavajúca právnická osoba*.</span><span class="sxs-lookup"><span data-stu-id="172aa-106">The legal entity that provides the service or product is called the *lending legal entity*.</span></span> <span data-ttu-id="172aa-107">Právnická osoba, ktorá prijíma službu alebo produkt, sa nazýva *požičiavajúca si právnická osoba*.</span><span class="sxs-lookup"><span data-stu-id="172aa-107">The legal entity that receives the service or product is called the *borrowing legal entity*.</span></span>

<span data-ttu-id="172aa-108">Nasledujúca ilustrácia ukazuje typický scenár, keď dve právnické osoby, Contoso Robotics USA (požičiavajúca si právnická osoba) a Contoso Robotics UK (požičiavajúca právnická osoba) zdieľajú zdroje na realizáciu projektu pre zákazníka, spoločnosť Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="172aa-108">The following illustration shows a typical scenario where two legal entities, Contoso Robotics USA (the borrowing legal entity) and Contoso Robotics UK (the lending legal entity) share resources to deliver a project for the customer, Adventure works.</span></span> <span data-ttu-id="172aa-109">Pre tento scenár má spoločnosť Contoso Robotics USA zmluvu na dodanie diela spoločnosti Adventure Works.</span><span class="sxs-lookup"><span data-stu-id="172aa-109">For this scenario, Contoso Robotics USA is contracted to deliver the work to Adventure Works.</span></span>

![Medzipodniková fakturácia](./media/IntercompanyScenario.png) 

<span data-ttu-id="172aa-111">Dynamics 365 Project Operations používa na spracovanie medzipodnikových transakcií nasledujúci postup:</span><span class="sxs-lookup"><span data-stu-id="172aa-111">Dynamics 365 Project Operations uses the following flow to process intercompany transactions:</span></span>

1. <span data-ttu-id="172aa-112">Zdroje z požičiavajúcej právnickej osoby zaznamenávajú medzipodnikové časové alebo nákladové transakcie podľa času rezervácie a výdavkov voči projektom u požičiavajúcej si právnickej osoby.</span><span class="sxs-lookup"><span data-stu-id="172aa-112">Resources from the lending legal entity record intercompany time or expense transactions by booking time and expense against projects in the borrowing legal entity.</span></span>
2. <span data-ttu-id="172aa-113">Časové a nákladové výdavky sa zaznamenávajú u požičiavajúcej spoločnosti pomocou cenníka jednotkových obstarávacích cien požičiavajúcej si spoločnosti.</span><span class="sxs-lookup"><span data-stu-id="172aa-113">Time and expense costs are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
3. <span data-ttu-id="172aa-114">Medzipodnikové nefakturované obchodné transakcie sa zaznamenávajú u požičiavajúcej spoločnosti pomocou cenníka jednotkových obstarávacích cien požičiavajúcej si spoločnosti.</span><span class="sxs-lookup"><span data-stu-id="172aa-114">Intercompany unbilled sale transactions are recorded in the lending company by using the borrowing company's unit cost price list.</span></span>
4. <span data-ttu-id="172aa-115">Nevyfakturované výnosy sa zaznamenávajú v požičiavajúcej si spoločnosti pomocou predajného cenníka projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="172aa-115">Unbilled revenue is recorded in the borrowing company using the project contract sales price list.</span></span> <span data-ttu-id="172aa-116">Zákazníkovi je možné fakturovať, keď sa zaznamenajú nevyfakturované výnosy.</span><span class="sxs-lookup"><span data-stu-id="172aa-116">The customer can be billed when unbilled revenue is recorded.</span></span> <span data-ttu-id="172aa-117">Zákazník nemusí čakať, kým sa dokončí spracovanie medzipodnikovej faktúry.</span><span class="sxs-lookup"><span data-stu-id="172aa-117">The customer doesn't have to wait until intercompany invoice processing is complete.</span></span>
5. <span data-ttu-id="172aa-118">Medzipodnikové zákaznícke faktúry sa v požičiavajúcej spoločnosti vytvárajú pravidelne.</span><span class="sxs-lookup"><span data-stu-id="172aa-118">Intercompany customer invoices are created on a periodic basis in the lending company.</span></span> <span data-ttu-id="172aa-119">Faktúry sa vytvárajú ručne alebo pomocou periodického automatizovaného procesu.</span><span class="sxs-lookup"><span data-stu-id="172aa-119">The invoices are created manually or by using a periodic automated process.</span></span> <span data-ttu-id="172aa-120">Pre každú požičiavajúcu si právnickú osobu je možné vytvoriť jednu faktúru alebo je možné vytvoriť samostatné faktúry podľa projektu.</span><span class="sxs-lookup"><span data-stu-id="172aa-120">A single invoice can be created for each borrowing legal entity or separate invoices can be created by project.</span></span>
6. <span data-ttu-id="172aa-121">Keď je zaúčtovaná medzipodniková faktúra zákazníka u požičiavajúcej právnickej osoby, zodpovedajúca nevybavená faktúra dodávateľa sa vytvorí u požičiavajúcej si právnickej osoby.</span><span class="sxs-lookup"><span data-stu-id="172aa-121">When the intercompany customer invoice is posted in the lending legal entity, the corresponding pending vendor invoice is created in the borrowing legal entity.</span></span> <span data-ttu-id="172aa-122">Po zaúčtovaní faktúry sa náklady na čakajúcej faktúre dodávateľa zaznamenajú do vedľajšej účtovnej knihy projektu.</span><span class="sxs-lookup"><span data-stu-id="172aa-122">The costs in the pending vendor invoice will be recorded to the project subledger when the invoice is posted.</span></span>

<span data-ttu-id="172aa-123">Nasledujúci diagram ilustruje medzipodnikovú fakturáciu, pretože sa týka účtovných udalostí a očakávaných zaúčtovaní do hlavnej účtovnej knihy.</span><span class="sxs-lookup"><span data-stu-id="172aa-123">The following diagram illustrates intercompany invoicing as it relates to accounting events and expected postings to the general ledger.</span></span>

![Medzipodnikový postup](./media/IntercompanyFlow.png)

## <a name="additional-resources"></a><span data-ttu-id="172aa-125">Ďalšie zdroje</span><span class="sxs-lookup"><span data-stu-id="172aa-125">Additional resources</span></span>

- [<span data-ttu-id="172aa-126">Konfigurácia medzipodnikovej fakturácie</span><span class="sxs-lookup"><span data-stu-id="172aa-126">Configure intercompany invoicing</span></span>](configure-intercompany-invoicing.md)
- [<span data-ttu-id="172aa-127">Záznam medzipodnikových transakcií</span><span class="sxs-lookup"><span data-stu-id="172aa-127">Record intercompany transactions</span></span>](create-intercompany-transactions.md)
- [<span data-ttu-id="172aa-128">Vytvorenie medzipodnikových faktúr zákazníkov a dodávateľov</span><span class="sxs-lookup"><span data-stu-id="172aa-128">Create intercompany customer and vendor invoices</span></span>](create-intercompany-customer-vendor-invoices.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]