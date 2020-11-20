---
title: Prečo je predvolene cena na skutočných časových predajoch nulová?
description: Riešenie problémov, keď je predvolená cena 0 na skutočných hodnotách času predaja.
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
ms.openlocfilehash: 5106e8c1a059bbb0efbeb73dc63e03e8bc9e4b7b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 10/28/2020
ms.locfileid: "4125962"
---
# <a name="why-is-price-defaulting-to-zero-on-time-sales-actuals"></a>Prečo je predvolene cena na skutočných časových predajoch nulová?

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tieto najčastejšie otázky sa vzťahuje na skutočné výdavky, kde je trieda transakcie stanovená na Čas a typ transakcie na Nefakturované predaje. Nasledujúce tri kontroly vám pomôžu pri riešení problémov s predvolenou cenou (sadzba fakturácie) 0 pri skutočných hodnotách časových predajov.

## <a name="check-1-identify-the-sales-price-list-for-the-project"></a>Kontrola č. 1: Identifikovať predajný cenník projektov

Vyhľadajte projekt v poli projektu skutočných hodnôt a prejdite na stránku projektu. Potom prejdite na kartu predaja. Na mriežke riadok zmluvy projektu kliknite na odkaz v poli Projektová zmluva. Otvorí sa stránka Projektovej zmluvy. Na stránke projektovej zmluvy prejdite na kartu Projektové cenníky. Skontrolujte, či je tam priložený aspoň jeden cenník. Ak v mriežke projektových cenníkov projektovej zmluvy nie je žiaden cenník, izolovali ste problém. Priložte cenník k mriežke projektových cenníkov. Cenník, ktorý tu možno priložiť, musí obsahovať kontextové pole nastavené na Predaj a pole meny cenníka, ktoré sa musí zhodovať s poľom meny v Projektovej zmluve. Po vykonaní požadovaných opráv opätovne vytvorte položku času, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty predajov zobrazujú platnú cenu. 

Ak máte jeden alebo viac cenníkov pripojených v mriežke projektových cenníkov projektovej zmluvy, pokračujte na ďalšiu kontrolu v dokumente.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-sales-actual"></a>Kontrola č. 2: Sú niektoré z cenníkov identifikovaných vyššie platné pre konkrétny dátum skutočných časových predajov?

Aby Project Service považovala cenník za predvolenú cenu, musí byť daný cenník platné pred dátum skutočnej hodnoty časového predaja. Skontrolujte nasledovné položky a zistite, či cenníky určené vyššie vyhovujú:
- Skontrolujte, či dátum začiatku a konca na karte všeobecných informácií pre priložené cenníky nie sú prázdne. Ak počiatočné a koncové dátumy na cenu zoznamy uvedené vyššie sú prázdne, izolovali ste problém. 
- Poznačte si pole počiatočného dátumu skutočnej hodnoty časových predajov a skontrolujte, či pre daný dátum platí niektorý z identifikovaných cenníkov. Dátum skutočnej hodnoty časových predajov musí spadať do počiatočného a koncového dátumu cenníka. 
    - Ak neexistuje žiadny cenník, ktorý pokrýva tento dátum na skutočné časové predaje, izolovali ste problém. Upraviť počiatočné a koncové dátumy cenníka a zabezpečte, že cenník pokrýva dátum skutočných časových predajov. 
    - Ak existuje viac než jeden cenník, ktorý pokrýva dátum skutočných časových predajov, izolovali ste problém. Tento problém možno vyriešiť úpravou počiatočných a koncových dátumov cenníka ta, aby existoval iba jeden cenník, ktorý pokrýva dátum skutočných časových predajov. 
    - Ak existuje iba jeden cenník, ktorý pokrýva daný dátum skutočných časových predajov, prejdite na kontrolu 3.
Po vykonaní požadovaných opráv opätovne vytvorte položku času, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty časových predajov zobrazujú platnú cenu.

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-sales-actual"></a>Kontrola č. 3: Existuje cena v cenníku pre dimenzie oceňovania na skutočných hodnotách časových predajov?

Ak ste úspešne dokončili kontrolu 1 a 2, mali by ste mať iba jeden cenník, ktorý sa vzťahuje na dátum skutočne hodnoty časových predajov. Otvorte tento cenník a prejdite na kartu Ceny rol. Skontrolujte, že existuje riadok v mriežke pre dimenzie oceňovania pre skutočné hodnoty časových predajov.

Ak neexistuje žiadny riadok v role cenníka pre dimenzie oceňovania v skutočných hodnotách časového predaja, izolovali ste problém. Vytvorte riadok v mriežke cien roly pre dimenzie oceňovania skutočných časových predajov. Keď tak urobíte, opätovne vytvorte položku času, schváľte ju a skontrolujte, že skutočné hodnoty časových predajov zobrazujú platnú cenu.

Ak stále nevidíte platnú cenu na váš skutočný čas predaja po týchto troch kontroly vyššie, prihláste sa prosím na podporu lístok. 

