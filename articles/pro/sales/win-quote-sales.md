---
title: Uzavretie cenových ponúk
description: Táto téma poskytuje informácie o uzatváraní cenovej ponuky v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4084285"
---
# <a name="close-quotes"></a><span data-ttu-id="1349b-103">Uzavretie cenových ponúk</span><span class="sxs-lookup"><span data-stu-id="1349b-103">Close quotes</span></span> 

<span data-ttu-id="1349b-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="1349b-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1349b-105">Cenovú ponuku projektu je možné uzavrieť ako Získaná alebo Nevyužitá.</span><span class="sxs-lookup"><span data-stu-id="1349b-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="1349b-106">Operácie Aktivovať a Skontrolovať nie sú v Microsoft Dynamics 365 Project Operations podporované pre cenové ponuky, takže môžete uzavrieť koncept cenovej ponuky.</span><span class="sxs-lookup"><span data-stu-id="1349b-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="1349b-107">Uzavretie cenovej ponuky ako Získaná</span><span class="sxs-lookup"><span data-stu-id="1349b-107">Close a quote as Won</span></span>

<span data-ttu-id="1349b-108">Uzatvorením ponuky projektu ako Získaná uzavriete cenovú ponuku so stavom nastaveným na Uzavretá s dôvodom stavu nastaveným na Získaná.</span><span class="sxs-lookup"><span data-stu-id="1349b-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="1349b-109">Po uzavretí budú cenové ponuky projektu iba na čítanie a vytvorí sa koncept projektovej zmluvy so všetkými informáciami o cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="1349b-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="1349b-110">Pretože uzavretú ponuku nie je možné znovu otvoriť, pred vykonaním zmien sa zobrazí potvrdzovacie dialógové okno a zmeny budú nezvratné.</span><span class="sxs-lookup"><span data-stu-id="1349b-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="1349b-111">Ak je cenová ponuka pripojená k príležitosti, akékoľvek ďalšie projektové ponuky týkajúce sa príležitosti sa automaticky uzavrú ako nezískané.</span><span class="sxs-lookup"><span data-stu-id="1349b-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="1349b-112">Finančný dopad uzavretia cenovej ponuky nastavenej ako Získaná</span><span class="sxs-lookup"><span data-stu-id="1349b-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="1349b-113">Ak na projekte boli zaznamenané nejaké skutočnosti v čase, keď je ešte pripojený ku konceptu cenovej ponuky, zaznamenajú sa iba náklady na čas alebo výdavky.</span><span class="sxs-lookup"><span data-stu-id="1349b-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="1349b-114">Po uzavretí cenovej ponuky ako získanej bude aplikácia refaktorovať náklady obrátením starších skutočných nákladov a opätovným vytvorením nových skutočných nákladov.</span><span class="sxs-lookup"><span data-stu-id="1349b-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="1349b-115">Aplikácia spracuje tieto skutočné náklady na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="1349b-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="1349b-116">Ak sa skutočné náklady vzťahujú na riadok zmluvy pre čas a materiál, systém automaticky vytvorí zodpovedajúce nevyfakturované predajné skutočné hodnoty, keď je cenová ponuka uzavretá a vytvorí sa projektová zmluva.</span><span class="sxs-lookup"><span data-stu-id="1349b-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="1349b-117">Ak sa skutočné náklady vzťahujú na riadku zmluvy s pevnou cenou, aplikácia zastaví spracovanie skutočných nákladov na základe pravidiel rozdeleného fakturovania pre zmluvných zákazníkov pre projekt.</span><span class="sxs-lookup"><span data-stu-id="1349b-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="1349b-118">Uzavretie cenovej ponuky ako nevyužitej:</span><span class="sxs-lookup"><span data-stu-id="1349b-118">Closing a quote as lost:</span></span>

<span data-ttu-id="1349b-119">Uzatvorením ponuky projektu ako Nevyužitá nastavíte stav na Uzavretá s dôvodom stavu Nevyužitá.</span><span class="sxs-lookup"><span data-stu-id="1349b-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="1349b-120">Uzavretie cenovej ponuky spôsobí, že ponuka projektu bude iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="1349b-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="1349b-121">Keďže uzavretú cenovú ponuku nie je možné znovu otvoriť, tak pred zatvorením cenovej ponuky musíte svoje zmeny potvrdiť v dialógovom okne.</span><span class="sxs-lookup"><span data-stu-id="1349b-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="1349b-122">Ak je v cenovej ponuke projektu, ktorá je uzavretá ako Nezískaná, uvedený projekt na ktoromkoľvek z jeho riadkov, tento projekt bude tiež označený ako Uzavretý a všetky rezervácie zdrojov od tohto dňa budú zrušené.</span><span class="sxs-lookup"><span data-stu-id="1349b-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="1349b-123">V rámci Project Operations uzavretie ponuky ako Získaná or Nevyužitá nebude mať vplyv na tento stav príležitosti, ktorá zostane otvorená, kým sa manuálne neuzavrie.</span><span class="sxs-lookup"><span data-stu-id="1349b-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
