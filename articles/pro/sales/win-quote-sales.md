---
title: Uzavretie cenovej ponuky – čiastočné
description: Táto téma poskytuje informácie o uzatváraní cenovej ponuky v Project Operations.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8d387816f51f63ecd95df6534c7c012b323e6ddc
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764883"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="5cf27-103">Uzavretie cenovej ponuky – čiastočné</span><span class="sxs-lookup"><span data-stu-id="5cf27-103">Close a quote - lite</span></span>

<span data-ttu-id="5cf27-104">_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_</span><span class="sxs-lookup"><span data-stu-id="5cf27-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5cf27-105">Cenovú ponuku projektu je možné uzavrieť ako Získaná alebo Nevyužitá.</span><span class="sxs-lookup"><span data-stu-id="5cf27-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="5cf27-106">Koncept cenovej ponuky je možné uzavrieť, pretože operácie Aktivovať a Upraviť pre cenovú ponuku nie sú v Microsoft Dynamics 365 Project Operations podporované.</span><span class="sxs-lookup"><span data-stu-id="5cf27-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="5cf27-107">Uzavretie cenovej ponuky ako Získaná</span><span class="sxs-lookup"><span data-stu-id="5cf27-107">Close a quote as Won</span></span>

<span data-ttu-id="5cf27-108">Keď uzavriete ponuku projektu ako Získaná, stav sa nastaví na Uzavretá a dôvod stavu je Získaná.</span><span class="sxs-lookup"><span data-stu-id="5cf27-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="5cf27-109">Po uzavretí budú cenové ponuky projektu iba na čítanie a vytvorí sa koncept projektovej zmluvy so všetkými informáciami o cenovej ponuke.</span><span class="sxs-lookup"><span data-stu-id="5cf27-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="5cf27-110">Pretože uzavretú cenovú ponuku nie je možné znovu otvoriť, vaše zmeny sa potvrdia v potvrdzovacom dialógovom okne.</span><span class="sxs-lookup"><span data-stu-id="5cf27-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="5cf27-111">Ak je cenová ponuka pripojená k príležitosti, akékoľvek ďalšie projektové ponuky týkajúce sa príležitosti sa automaticky uzavrú ako nezískané.</span><span class="sxs-lookup"><span data-stu-id="5cf27-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="5cf27-112">Finančný dopad uzavretia cenovej ponuky nastavenej ako Získaná</span><span class="sxs-lookup"><span data-stu-id="5cf27-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="5cf27-113">Ak v projekte existujú časové údaje, zatiaľ čo je ešte pripojený k návrhu cenovej ponuky, zaznamenajú sa iba náklady na čas alebo výdavky.</span><span class="sxs-lookup"><span data-stu-id="5cf27-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="5cf27-114">Po uzavretí cenovej ponuky ako získanej bude aplikácia refaktorovať náklady obrátením starších skutočných nákladov a opätovným vytvorením nových skutočných nákladov.</span><span class="sxs-lookup"><span data-stu-id="5cf27-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="5cf27-115">Aplikácia spracuje tieto skutočné náklady na základe metódy fakturácie súvisiacej s riadkom zmluvy projektu.</span><span class="sxs-lookup"><span data-stu-id="5cf27-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="5cf27-116">Ak sa skutočné náklady odvolávajú na časový a materiálny riadok zmluvy, zodpovedajúce nevyúčtované predajné skutočnosti sa vytvoria, keď sa ponuka uzavrie a vytvorí sa projektová zmluva.</span><span class="sxs-lookup"><span data-stu-id="5cf27-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="5cf27-117">Ak sa skutočná cena odvoláva na riadok zmluvy so stanovenou cenou, aplikácia zastaví spracovanie skutočných nákladov, ktoré sú založené na pravidlách rozdeleného fakturovania pre zákazníkov projektovej zmluvy.</span><span class="sxs-lookup"><span data-stu-id="5cf27-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="5cf27-118">Uzavretie cenovej ponuky ako nevyužitej:</span><span class="sxs-lookup"><span data-stu-id="5cf27-118">Closing a quote as lost:</span></span>

<span data-ttu-id="5cf27-119">Keď uzavriete ponuku projektu ako Nevyužitá, stav sa nastaví na Uzavretá a dôvod stavu je Nevyužitá.</span><span class="sxs-lookup"><span data-stu-id="5cf27-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="5cf27-120">Uzavretie cenovej ponuky spôsobí, že ponuka projektu bude iba na čítanie.</span><span class="sxs-lookup"><span data-stu-id="5cf27-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="5cf27-121">Keďže uzavretú cenovú ponuku nie je možné znovu otvoriť, tak pred zatvorením cenovej ponuky musíte svoje zmeny potvrdiť v dialógovom okne.</span><span class="sxs-lookup"><span data-stu-id="5cf27-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="5cf27-122">Ak projektová cenová ponuka, ktorá je uzavretá ako Nezískaná, odkazuje na projekt v ktoromkoľvek z jeho riadkov, tento projekt sa tiež označí ako Zatvorený.</span><span class="sxs-lookup"><span data-stu-id="5cf27-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="5cf27-123">Všetky rezervácie zdrojov od daného dňa budú zrušené.</span><span class="sxs-lookup"><span data-stu-id="5cf27-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="5cf27-124">V rámci Project Operations uzavretie ponuky ako Získaná or Nevyužitá nebude mať vplyv na tento stav príležitosti, ktorá zostane otvorená, kým sa manuálne neuzavrie.</span><span class="sxs-lookup"><span data-stu-id="5cf27-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
