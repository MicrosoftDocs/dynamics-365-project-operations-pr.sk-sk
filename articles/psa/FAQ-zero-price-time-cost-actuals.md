---
title: Prečo je predvolene cena na skutočných časových nákladoch nulová?
description: Riešenie problémov, keď je predvolená cena 0 na skutočných časových nákladoch.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131401"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="5caf0-103">Prečo je predvolene cena na skutočných časových nákladoch nulová?</span><span class="sxs-lookup"><span data-stu-id="5caf0-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5caf0-104">Tieto najčastejšie otázky sa vzťahuje na skutočné hodnoty, kde je trieda transakcie stanovená na Čas a typ transakcie na Náklady.</span><span class="sxs-lookup"><span data-stu-id="5caf0-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="5caf0-105">Nasledujúce tri kontroly vám pomôžu pri riešení problémov s predvolenou cenou 0 pri skutočných hodnotách časových nákladov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="5caf0-106">Kontrola č. 1: Identifikovať obstarávaciu cenu projektu</span><span class="sxs-lookup"><span data-stu-id="5caf0-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="5caf0-107">Vyhľadajte projekt v poli projektu skutočných hodnôt a prejdite na stránku projektu.</span><span class="sxs-lookup"><span data-stu-id="5caf0-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="5caf0-108">V poli kliknite na odkaz na zmluvnú jednotku.</span><span class="sxs-lookup"><span data-stu-id="5caf0-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="5caf0-109">Na stránke zmluvnej jednotky skontrolujte, či má zmluvná jednotka cenník v mriežke Cenníky obstarávacích cien.</span><span class="sxs-lookup"><span data-stu-id="5caf0-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="5caf0-110">Ak sa tam vyskytuje viac než jeden cenník, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="5caf0-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="5caf0-111">Project Service podporuje iba jeden cenník na organizačnú jednotku.</span><span class="sxs-lookup"><span data-stu-id="5caf0-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="5caf0-112">Odstraňuje z tejto entity cenníky, pokým tam v mriežke Cenníky obstarávacích cien organizačnej jednotky nebude priložený iba jeden cenník.</span><span class="sxs-lookup"><span data-stu-id="5caf0-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="5caf0-113">Ak neexistujú žiadne ceny zoznamy pripojené na organizačnú jednotku, poznačte si mene organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="5caf0-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="5caf0-114">Prejdite do Project Service a potom parametre a otvoriť cenníky kreslenie overiť, ak existuje akýkoľvek cenníky s súvislosti nákladov a mene, ktorá zodpovedá mene organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="5caf0-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="5caf0-115">Ak neexistujú žiadne cenníkov, ktoré vyhovujú týmto kritériám, máte izolovaný problém.</span><span class="sxs-lookup"><span data-stu-id="5caf0-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="5caf0-116">Uistite sa, že máte aspoň jeden cenník ktorého kontext nastavený na náklady a menou zápasy mene organizačnej jednotky.</span><span class="sxs-lookup"><span data-stu-id="5caf0-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="5caf0-117">Ak existuje viac ako jeden cenník, ktorý týmto kritériám nezodpovedajú, pokračovať v čítaní tohto dokumentu vykonať ďalšie kontroly.</span><span class="sxs-lookup"><span data-stu-id="5caf0-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="5caf0-118">Kontrola č. 2: Sú niektoré z cenníkov identifikovaných vyššie platné pre konkrétny dátum skutočných časových nákladov?</span><span class="sxs-lookup"><span data-stu-id="5caf0-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="5caf0-119">Aby Project Service považovala cenník za predvolenú cenu, musí byť daný cenník platné pred dátum skutočnej hodnoty časových nákladov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="5caf0-120">Skontrolujte nasledovné položky a zistite, či cenníky určené vyššie vyhovujú:</span><span class="sxs-lookup"><span data-stu-id="5caf0-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="5caf0-121">Skontrolujte, či dátum začiatku a konca na karte všeobecných informácií pre priložené cenníky nie sú prázdne.</span><span class="sxs-lookup"><span data-stu-id="5caf0-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="5caf0-122">Ak počiatočné a koncové dátumy na cenu zoznamy uvedené vyššie sú prázdne, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="5caf0-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="5caf0-123">Poznačte si pole počiatočného dátumu skutočnej hodnoty časových nákladov a skontrolujte, či pre daný dátum platí niektorý z identifikovaných cenníkov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="5caf0-124">Dátum skutočnej hodnoty časových nákladov musí spadať do počiatočného a koncového dátumu cenníka.</span><span class="sxs-lookup"><span data-stu-id="5caf0-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="5caf0-125">Ak neexistuje žiadny cenník, ktorý pokrýva tento dátum na skutočné časové náklady, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="5caf0-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="5caf0-126">Upraviť počiatočné a koncové dátumy cenníka a zabezpečte, že cenník pokrýva dátum skutočných časových nákladov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="5caf0-127">Ak existuje viac než jeden cenník, ktorý pokrýva dátum skutočných časových nákladov, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="5caf0-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="5caf0-128">Tento problém možno vyriešiť úpravou počiatočných a koncových dátumov cenníka ta, aby existoval iba jeden cenník, ktorý pokrýva dátum skutočných časových nákladov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="5caf0-129">Ak existuje iba jeden cenník, ktorý pokrýva tohto dátumu skutočného času nákladov, presunúť do nasledujúcej kontroly v dokumente.</span><span class="sxs-lookup"><span data-stu-id="5caf0-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="5caf0-130">Po vykonaní požadovaných opráv opätovne vytvorte položku času, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty časových nákladov zobrazujú platnú cenu.</span><span class="sxs-lookup"><span data-stu-id="5caf0-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="5caf0-131">Kontrola č. 3: Existuje cena v cenníku pre dimenziu oceňovania na skutočné časové náklady?</span><span class="sxs-lookup"><span data-stu-id="5caf0-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="5caf0-132">Ak ste úspešne dokončili kontrolu 1 a 2, mali by ste mať iba jeden cenník, ktorý sa vzťahuje na dátum skutočne hodnoty časových nákladov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="5caf0-133">Otvorte tento cenník a prejdite na kartu Ceny rol. Skontrolujte, že existuje riadok v mriežke pre dimenzie oceňovania pre skutočné hodnoty časových nákladov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="5caf0-134">Ak neexistuje žiadny riadok v role cenníka pre dimenzie oceňovania v skutočných hodnotách časových nákladov, izolovali ste problém.</span><span class="sxs-lookup"><span data-stu-id="5caf0-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="5caf0-135">Vytvorte riadok v mriežke cien roly pre dimenzie oceňovania skutočných časových nákladov.</span><span class="sxs-lookup"><span data-stu-id="5caf0-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="5caf0-136">Keď tak urobíte, opätovne vytvorte položku času, schváľte ju a skontrolujte, že skutočné hodnoty časových nákladov zobrazujú platnú cenu.</span><span class="sxs-lookup"><span data-stu-id="5caf0-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="5caf0-137">Ak stále nevidíte platnú cenu na váš skutočný časový náklad po týchto troch kontroly vyššie, prihláste sa prosím na podporu lístok.</span><span class="sxs-lookup"><span data-stu-id="5caf0-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



