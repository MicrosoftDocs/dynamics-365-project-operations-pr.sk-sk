---
title: Prehľad riadkov cenových ponúk založených na produkte – čiastočné
description: Táto téma poskytuje informácie o práci s riadkami cenovej ponuky založenej na projekte.
author: rumant
ms.date: 10/30/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5cc3a97194e01b14de054a93a6268c1f0c24bc25
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: sk-SK
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994470"
---
# <a name="product-based-quote-lines-overview---lite"></a>Prehľad riadkov cenových ponúk založených na produkte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Môžete vytvoriť riadky cenových ponúk v Dynamics 365 Project Operations. Riadky cenových ponúk založených na produkte je možné pridávať ručne alebo môžu byť položkami z katalógu produktov.

## <a name="product-catalog"></a>Katalóg produktov

Každý produkt v katalógu produktov má predvolenú jednotku a jednotkovú skupinu. Ak viac produktov zdieľa rovnakú množinu atribútov, môžete vytvoriť produktovú rodinu, ktorá zdieľa tieto atribúty. 

Spoločnosť napríklad predáva licencie na predplatné pre rôzne druhy softvéru. Všetky predplatné softvéry májú nasledujúce dva atribúty:

- Počet používateľov
- Trvanie predplatného merané v mesiacoch

Ak chcete udržiavať tento typ katalógu, vytvorte rodinu produktov s názvom **Predplatné softvéru** a ako atribúty pridajte počet používateľov a trvanie predplatného. Ďalej môžete do rodiny produktov **Predplatné softvéru** pridať jednotlivé produkty.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Pridanie položiek katalógu produktov do projektovej cenovej ponuky

Stránky **Projektová cenová ponuka** a **Projektová zmluva** majú sekcie pre riadky založené na projekte a riadky založené na produkte. Pre riadky založené na produkte rozbaľovací zoznam v riadku cenovej ponuky alebo riadku projektovej zmluvy obsahuje všetky produkty a jednotky v cenníku produktov. Môžete tiež pridať produkty, ktoré nie sú súčasťou cenníka produktov.

Okrem toho môžete vybrať produkty z iných cenníkov alebo priamo z katalógu produktov. Keď vyberiete produkty priamo z katalógu produktov, na získanie predajnej ceny produktu sa použije predvolený cenník daného produktu. Ak predvolený cenník nie je nastavený, cena je nastavená na hodnotu nula (0).

Ak je riadok cenovej ponuky založený na katalógu produktov, predajnú cenu môžete prepísať priamo v riadku cenovej ponuky. Cenová ponuka v poli **Ceny** s dvoma dostupnými hodnotami:

- **Prepísanie ceny**
- **Použiť predvolený**

Ak vyberiete **Prepísať ceny**, predvolená cena nie je nastavená. Namiesto toho musíte zadať cenu produktu v riadku cenovej ponuky. Ak vyberiete **Použiť predvolené**, použije sa predvolená predajná cena a pole je pre úpravy uzamknuté.

Predvolené predajné ceny sa zapisujú do riadkov na základe produktov v cenovej ponuke. Pole **Ceny** sa potom nastaví na **Prepísanie cien**, aby ste mohli upraviť predvolenú cenu v riadkoch cenovej ponuky. Toto je prepísanie riadkov založených na produktoch špecifické pre aplikáciu Project Operations v Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]