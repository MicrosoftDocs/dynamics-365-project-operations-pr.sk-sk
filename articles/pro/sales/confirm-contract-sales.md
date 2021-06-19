---
title: Potvrdenie projektovej zmluvy
description: Táto téma poskytuje informácie o spôsobe potvrdenia zmluvy v aplikácii Project Operations.
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5eabcad028a8282f552f3571b170d9b933a7b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003695"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="e5800-103">Potvrdenie projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="e5800-103">Confirm a project contract</span></span>

<span data-ttu-id="e5800-104">_**Platí pre:** Projektové operácie pre scenáre založené na zdrojoch/chýbajúcich zdrojoch, čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="e5800-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e5800-105">Zmluva o projekte v aplikácii Dynamics 365 Project Operations môže byť aktívna z dôvodu **Potvrdené**, alebo môže byť uzavretá z dôvodu **Stratené**.</span><span class="sxs-lookup"><span data-stu-id="e5800-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="e5800-106">Po potvrdení projektovej zmluvy sa stav aktualizuje z **Koncept** na **Aktívna** a dôvod stavu je **Potvrdená**.</span><span class="sxs-lookup"><span data-stu-id="e5800-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="e5800-107">Aktívnu alebo uzavretú zmluvu nie je možné upraviť ani znova otvoriť.</span><span class="sxs-lookup"><span data-stu-id="e5800-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="e5800-108">Finančný dopad potvrdenia projektovej zmluvy</span><span class="sxs-lookup"><span data-stu-id="e5800-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="e5800-109">Po potvrdení projektovej zmluvy aplikácia prepočíta náklady obrátením starších skutočných nákladov a vytvorením nových skutočných nákladov.</span><span class="sxs-lookup"><span data-stu-id="e5800-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="e5800-110">Nové skutočné náklady sa potom spracujú na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="e5800-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="e5800-111">Ak sa skutočné náklady odvolávajú na riadok zmluvy Čas a materiál, aplikácia automaticky znova vytvorí príslušné nevyfakturované skutočné hodnoty predaja.</span><span class="sxs-lookup"><span data-stu-id="e5800-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="e5800-112">Ak sa skutočné náklady odvolávajú na riadok zmluvy Pevná cena, aplikácia zastaví spracovanie skutočných nákladov.</span><span class="sxs-lookup"><span data-stu-id="e5800-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="e5800-113">V rámci procesu potvrdzovania sa vyhodnocujú a aktualizujú limity, ktoré sa nesmú prekročiť, nastavenie účtovateľnosti a ceny a náklady pri skutočných hodnotách.</span><span class="sxs-lookup"><span data-stu-id="e5800-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="e5800-114">Uzavretie projektovej zmluvy ako nevyužitej</span><span class="sxs-lookup"><span data-stu-id="e5800-114">Close a project contract as lost</span></span>

<span data-ttu-id="e5800-115">Keď uzavriete projektovú zmluvu ako nevyužitú, stav zmluvy sa aktualizuje na **Uzavretá** a dôvod stavu je **Nevyužitá**.</span><span class="sxs-lookup"><span data-stu-id="e5800-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="e5800-116">Projektová zmluva bude iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="e5800-116">The project contract becomes read-only.</span></span> <span data-ttu-id="e5800-117">Pred dokončením zmien sa zobrazí dialógové okno s potvrdením, pretože nemôžete znovu otvoriť uzavretú projektovú zmluvu.</span><span class="sxs-lookup"><span data-stu-id="e5800-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="e5800-118">Ak projektová zmluva, ktorá je uzavretá ako nevyužitá, odkazuje na projekt v jeho riadkoch, tento projekt sa tiež označí ako uzavretý.</span><span class="sxs-lookup"><span data-stu-id="e5800-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="e5800-119">Všetky rezervácie zdrojov od daného dňa budú zrušené.</span><span class="sxs-lookup"><span data-stu-id="e5800-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="e5800-120">Akékoľvek nevyfakturované predajné skutočné údaje o projektovej zmluve, ktoré ešte nie sú na faktúre, budú vrátené späť.</span><span class="sxs-lookup"><span data-stu-id="e5800-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="e5800-121">V aplikácii Dynamics 365 Project Operations uzavretie projektovej zmluvy ako stratenej nebude mať vplyv na tento stav súvisiacej príležitosti.</span><span class="sxs-lookup"><span data-stu-id="e5800-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="e5800-122">Príležitosť zostane otvorená a musí byť uzavretá manuálne.</span><span class="sxs-lookup"><span data-stu-id="e5800-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]