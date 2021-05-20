---
title: Zakúpenie neskladovaných materiálov použitím čakajúcej faktúry dodávateľa
description: Táto téma vysvetľuje, ako zaznamenávať čakajúce faktúry dodávateľa.
author: sigitac
manager: tfehr
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a706f419443dcdf92ce3b247d719943272907d0
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880684"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="df9dd-103">Zakúpenie neskladovaných materiálov použitím čakajúcej faktúry dodávateľa</span><span class="sxs-lookup"><span data-stu-id="df9dd-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="df9dd-104">_**Platí pre:** Project Operations pre scenáre založené na zdrojoch/chýbajúcich zdrojoch_</span><span class="sxs-lookup"><span data-stu-id="df9dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="df9dd-105">Keďže spoločnosť obstaráva pre projekt neskladované materiály, náklady je možné okamžite zaznamenať oproti projektu.</span><span class="sxs-lookup"><span data-stu-id="df9dd-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="df9dd-106">Napríklad Contoso Robotics US realizuje projekt obnovy zariadenia a potrebuje softvérové licencie.</span><span class="sxs-lookup"><span data-stu-id="df9dd-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="df9dd-107">Tieto licencie sú obstarávané od dodávateľa tretej strany.</span><span class="sxs-lookup"><span data-stu-id="df9dd-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="df9dd-108">Použitím Dynamics 365 Finance, referent pre účty zaúčtuje dokument faktúry čakajúceho dodávateľa a pripíše náklady na licenciu priamo oproti projektu obnovy zariadenia.</span><span class="sxs-lookup"><span data-stu-id="df9dd-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="df9dd-109">Pred použitím funkcií popísaných v tejto téme si prečítajte a vykonajte požadované konfigurácie.</span><span class="sxs-lookup"><span data-stu-id="df9dd-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="df9dd-110">Viac informácií nájdete v časti [Povoliť neskladované materiály a čakajúce faktúry dodávateľa](configure-materials-nonstocked.md).</span><span class="sxs-lookup"><span data-stu-id="df9dd-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="df9dd-111">Zaúčtujte faktúru dodávateľa čakajúcu na projekt</span><span class="sxs-lookup"><span data-stu-id="df9dd-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="df9dd-112">Faktúry čakajúcich dodávateľov možno zaznamenať na stránke **Čakajúce faktúry dodávateľa** (**Záväzky** > **Faktúry** > **Čakajúce faktúry dodávateľa**).</span><span class="sxs-lookup"><span data-stu-id="df9dd-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="df9dd-113">Ak chcete zaúčtovať nespracovanú faktúru dodávateľa súvisiacej s projektom, postupujte takto:</span><span class="sxs-lookup"><span data-stu-id="df9dd-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="df9dd-114">Prejdite na **Záväzky** > **Faktúry** a stlačte možnosť **Nový**.</span><span class="sxs-lookup"><span data-stu-id="df9dd-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="df9dd-115">V poli **Účet faktúry** vyberte dodávateľa a v poli **Číslo** do poľa zadajte identifikáciu faktúry dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="df9dd-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="df9dd-116">Pridajte riadok k faktúre dodávateľa a do poľa **Číslo položky** vyberte skladovú položku zakúpenú od dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="df9dd-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="df9dd-117">Riadky faktúr dodávateľa, ktoré sú založené na kategórii obstarávania, sa proti projektu nedajú zaznamenať.</span><span class="sxs-lookup"><span data-stu-id="df9dd-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="df9dd-118">Pridajte zakúpené množstvo.</span><span class="sxs-lookup"><span data-stu-id="df9dd-118">Add the quantity purchased.</span></span> <span data-ttu-id="df9dd-119">Systém vyplní jednotkovú cenu na základe konfigurácie ceny tovaru, ktorý nie je na sklade.</span><span class="sxs-lookup"><span data-stu-id="df9dd-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="df9dd-120">Celkovú sumu a ďalšie požadované podrobnosti overte na riadku.</span><span class="sxs-lookup"><span data-stu-id="df9dd-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="df9dd-121">Na riadku podrobnosti na karte **Projekt** vyberte projekt, do ktorého sa táto položka zaznamená.</span><span class="sxs-lookup"><span data-stu-id="df9dd-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="df9dd-122">Voliteľne vyberte číslo aktivity a aktualizujte kategóriu projektu a vlastnosť riadka.</span><span class="sxs-lookup"><span data-stu-id="df9dd-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="df9dd-123">Zaúčtujte čakajúcu faktúru dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="df9dd-123">Post pending vendor invoice.</span></span> <span data-ttu-id="df9dd-124">Po zaúčtovaní faktúry systém zaznamená:</span><span class="sxs-lookup"><span data-stu-id="df9dd-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="df9dd-125">Suma zostatku dodávateľa.</span><span class="sxs-lookup"><span data-stu-id="df9dd-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="df9dd-126">Suma dane z predaja.</span><span class="sxs-lookup"><span data-stu-id="df9dd-126">The sales tax amount.</span></span>
    - <span data-ttu-id="df9dd-127">Náklady oproti projektu sa zaznamenajú na účet integrácie obstarávania.</span><span class="sxs-lookup"><span data-stu-id="df9dd-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="df9dd-128">Skutočná transakcia projektu v Dataverse.</span><span class="sxs-lookup"><span data-stu-id="df9dd-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="df9dd-129">Táto transakcia sa ďalej spracováva pomocou [denníka integrácie Project Operations](../project-accounting/project-operations-integration-journal.md).</span><span class="sxs-lookup"><span data-stu-id="df9dd-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="df9dd-130">Zaúčtovaním tohto denníka sa suma presunie z účtu integrácie obstarávania do účtu nákladov na projekt.</span><span class="sxs-lookup"><span data-stu-id="df9dd-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
