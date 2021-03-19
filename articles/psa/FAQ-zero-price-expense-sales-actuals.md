---
title: Prečo je predvolene cena na skutočných predajných výdavkoch nulová?
description: Nasledujúce tri kontroly vám pomôžu pri riešení problémov s predvolenou cenou 0 pri skutočných hodnotách predajných výdavkov.
author: rumant
manager: kfend
ms.prod: ''
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
ms.openlocfilehash: bd474d7c0cd64262fdb21d6269efa781b6dc31f2
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285907"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-sales-actuals"></a>Prečo je predvolene cena na skutočných predajných výdavkoch nulová?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Tieto najčastejšie otázky sa vzťahuje na skutočné výdavky, kde je trieda transakcie stanovená na Výdavky a typ transakcie na Nefakturované predaje. Nasledujúce tri kontroly vám pomôžu pri riešení problémov s predvolenou cenou (sadzba fakturácie) 0 pri skutočných hodnotách predajných výdavkov.

## <a name="check-1-identify-the-sales-price-list-for-project"></a>Kontrola č. 1: Identifikovať predajný cenník projektov

Vyhľadajte projekt v poli projektu skutočných hodnôt a prejdite na stránku projektu. Potom prejdite na kartu predaja. Na mriežke riadok zmluvy projektu kliknite na odkaz v poli Projektová zmluva. Otvorí sa stránka Projektovej zmluvy. Na stránke projektovej zmluvy prejdite na kartu Projektové cenníky. Skontrolujte, či je tam priložený aspoň jeden cenník.

Ak v mriežke projektových cenníkov projektovej zmluvy nie je žiaden cenník, vykonajte nasledujúce:

- Priložte cenník k mriežke projektových cenníkov. Cenník, ktorý tu možno priložiť, musí obsahovať kontextové pole nastavené na Predaj a pole meny cenníka, ktoré sa musí zhodovať s poľom meny v Projektovej zmluve. Po vykonaní požadovaných opráv opätovne vytvorte položku nákladov, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty predajov zobrazujú platnú cenu.
- Ak máte jeden alebo viac cenníkov pripojených v mriežke projektových cenníkov projektovej zmluvy, prejdite na kontrolu 2.

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-expense-actual"></a>Kontrola č. 2: Sú niektoré z cenníkov identifikovaných vyššie platné pre konkrétny dátum skutočných hodnôt výdavkov?

Aby Project Service považovala cenník za predvolenú cenu, musí byť daný cenník platné pred dátum skutočnej hodnoty výdavkov predaja. Skontrolujte nasledovné položky a zistite, či cenníky určené vyššie vyhovujú:

- Začnite kontrolou, či dátum začiatku a konca na karte všeobecných informácií pre priložené cenníky nie sú prázdne. Ak počiatočné a koncové dátumy na cenu zoznamy uvedené vyššie sú prázdne, izolovali ste problém. 
- Poznačte si pole počiatočného dátumu skutočnej hodnoty nákladov predaja a skontrolujte, či pre daný dátum platí niektorý z identifikovaných cenníkov. Dátum skutočnej hodnoty výdavkov musí spadať do počiatočného a koncového dátumu cenníka. 
    - Ak neexistuje žiadny cenník, ktorý pokrýva tento dátum na skutočné výdavky predaja, izolovali ste problém. Upraviť počiatočné a koncové dátumy cenníka a zabezpečte, že cenník pokrýva dátum skutočných výdavkov. 
    - Ak existuje viac než jeden cenník, ktorý pokrýva dátum skutočných predajných výdavkov, izolovali ste problém. Upravte počiatočné a koncové dátumy cenníka tak, aby existoval iba jeden cenník, ktorý pokrýva dátum skutočnej hodnoty výdavkov. 
    - Ak existuje iba jeden cenník, ktorý pokrýva daný dátum skutočných výdavkov, prejdite na kontrolu 3.
Po vykonaní požadovaných opráv opätovne vytvorte položku nákladov, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty predajov zobrazujú platnú cenu.

## <a name="check-3-is-there-a-valid-price-for-the-expense-category-in-the-applicable-project-price-list"></a>Kontrola č. 3: Existuje platná cena pre kategóriu výdavkov v platnom projektovom cenníku? 

Ak ste úspešne dokončili kontrolu 1 a 2, mali by ste mať iba jeden projektový cenník, ktorý sa vzťahuje na dátum skutočne hodnoty predajných nákladov. Otvorte projektový cenník a prejdite na kartu Ceny kategórií. Presvedčte sa, že v mriežke je riadok pre konkrétnu kategóriu výdavkov v rámci skutočnej hodnoty výdavkov.
 
- Ak sa tam riadok nenachádza, izolovali ste problém. Vytvorte v mriežke ceny kategórie riadok pre kategóriu skutočných hodnôt výdavkov. Potom opätovne vytvorte položku nákladov, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty predajov zobrazujú platnú cenu. 
- Ak v mriežke cien kategórie riadok pre kategóriu výdavkov existuje, skontrolujte, že má stanovenú platnú cenu.

Ak chcete zistiť, čo predstavuje platnú cenu, použite tieto spôsoby:

- Ak metóda oceňovania v riadku kategórie cena je nastavená na náklady, jednotkovej sadzby na skutočné náklady predaja bude predvolené na hodnotu v položke náklady.
- Ak metóda oceňovania v riadku kategórie cena je nastavená na percentuálne, potom skontrolovať, ak pole percento nastavená na platnú hodnotu. Jednotkovej sadzby na skutočné náklady predaja vykresľuje uplatnením tejto značky percent k cene v položke náklady.
- Ak metóda oceňovania v riadku kategórie cena je nastavená na cenu za jednotku, potom skontrolovať, ak pole Cena nastavená na platnú hodnotu. Jednotkovej sadzby na skutočné náklady predaja bude predvolene nastavené na sumu v mene zadaného v poli cena.

Ak cena nastavená pre kategóriu výdavkov nie je platná, izolovali ste problém. Riešením je upraviť kategóriu radu ceny s platnú cenu pre kategóriu nákladov v súlade s vyššie uvedenými pravidlami. Keď tak urobíte, opätovne vytvorte položku nákladov, schváľte ju a skontrolujte, že nevyfakturované skutočné hodnoty predajov zobrazujú platnú cenu.

Ak stále nevidíte platnú cenu na váš skutočný predajný výdavok po týchto troch kontrolách vyššie, prihláste sa na žiadosť o podporu.




[!INCLUDE[footer-include](../includes/footer-banner.md)]