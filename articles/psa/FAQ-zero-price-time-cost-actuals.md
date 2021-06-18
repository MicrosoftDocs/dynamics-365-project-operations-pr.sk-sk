---
title: Prečo je predvolene cena na skutočných časových nákladoch nulová?
description: Riešenie problémov, keď je predvolená cena 0 na skutočných časových nákladoch.
author: rumant
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
ms.openlocfilehash: ffe915a48f088bde457121a323325ba490c24e45
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993075"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a>Prečo je predvolene cena na skutočných časových nákladoch nulová?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tieto najčastejšie otázky sa vzťahuje na skutočné hodnoty, kde je trieda transakcie stanovená na Čas a typ transakcie na Náklady. Nasledujúce tri kontroly vám pomôžu pri riešení problémov s predvolenou cenou 0 pri skutočných hodnotách časových nákladov.
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a>Kontrola č. 1: Identifikovať obstarávaciu cenu projektu

Vyhľadajte projekt v poli projektu skutočných hodnôt a prejdite na stránku projektu. V poli kliknite na odkaz na zmluvnú jednotku. Na stránke zmluvnej jednotky skontrolujte, či má zmluvná jednotka cenník v mriežke Cenníky obstarávacích cien.

Ak sa tam vyskytuje viac než jeden cenník, izolovali ste problém. Project Service podporuje iba jeden cenník na organizačnú jednotku. Odstraňuje z tejto entity cenníky, pokým tam v mriežke Cenníky obstarávacích cien organizačnej jednotky nebude priložený iba jeden cenník.

Ak neexistujú žiadne ceny zoznamy pripojené na organizačnú jednotku, poznačte si mene organizačnej jednotky. Prejdite do Project Service a potom parametre a otvoriť cenníky kreslenie overiť, ak existuje akýkoľvek cenníky s súvislosti nákladov a mene, ktorá zodpovedá mene organizačnej jednotky.
 
Ak neexistujú žiadne cenníkov, ktoré vyhovujú týmto kritériám, máte izolovaný problém. Uistite sa, že máte aspoň jeden cenník ktorého kontext nastavený na náklady a menou zápasy mene organizačnej jednotky.

Ak existuje viac ako jeden cenník, ktorý týmto kritériám nezodpovedajú, pokračovať v čítaní tohto dokumentu vykonať ďalšie kontroly.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a>Kontrola č. 2: Sú niektoré z cenníkov identifikovaných vyššie platné pre konkrétny dátum skutočných časových nákladov?

Aby Project Service považovala cenník za predvolenú cenu, musí byť daný cenník platné pred dátum skutočnej hodnoty časových nákladov. Skontrolujte nasledovné položky a zistite, či cenníky určené vyššie vyhovujú:

- Skontrolujte, či dátum začiatku a konca na karte všeobecných informácií pre priložené cenníky nie sú prázdne. Ak počiatočné a koncové dátumy na cenu zoznamy uvedené vyššie sú prázdne, izolovali ste problém. 
- Poznačte si pole počiatočného dátumu skutočnej hodnoty časových nákladov a skontrolujte, či pre daný dátum platí niektorý z identifikovaných cenníkov. Dátum skutočnej hodnoty časových nákladov musí spadať do počiatočného a koncového dátumu cenníka. 
    - Ak neexistuje žiadny cenník, ktorý pokrýva tento dátum na skutočné časové náklady, izolovali ste problém. Upraviť počiatočné a koncové dátumy cenníka a zabezpečte, že cenník pokrýva dátum skutočných časových nákladov. 
    - Ak existuje viac než jeden cenník, ktorý pokrýva dátum skutočných časových nákladov, izolovali ste problém. Tento problém možno vyriešiť úpravou počiatočných a koncových dátumov cenníka ta, aby existoval iba jeden cenník, ktorý pokrýva dátum skutočných časových nákladov. 
    - Ak existuje iba jeden cenník, ktorý pokrýva tohto dátumu skutočného času nákladov, presunúť do nasledujúcej kontroly v dokumente.
Po vykonaní požadovaných opráv opätovne vytvorte položku času, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty časových nákladov zobrazujú platnú cenu.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a>Kontrola č. 3: Existuje cena v cenníku pre dimenziu oceňovania na skutočné časové náklady?

Ak ste úspešne dokončili kontrolu 1 a 2, mali by ste mať iba jeden cenník, ktorý sa vzťahuje na dátum skutočne hodnoty časových nákladov. Otvorte tento cenník a prejdite na kartu Ceny rol. Skontrolujte, že existuje riadok v mriežke pre dimenzie oceňovania pre skutočné hodnoty časových nákladov.

Ak neexistuje žiadny riadok v role cenníka pre dimenzie oceňovania v skutočných hodnotách časových nákladov, izolovali ste problém. Vytvorte riadok v mriežke cien roly pre dimenzie oceňovania skutočných časových nákladov. Keď tak urobíte, opätovne vytvorte položku času, schváľte ju a skontrolujte, že skutočné hodnoty časových nákladov zobrazujú platnú cenu.
 
Ak stále nevidíte platnú cenu na váš skutočný časový náklad po týchto troch kontroly vyššie, prihláste sa prosím na podporu lístok.





[!INCLUDE[footer-include](../includes/footer-banner.md)]