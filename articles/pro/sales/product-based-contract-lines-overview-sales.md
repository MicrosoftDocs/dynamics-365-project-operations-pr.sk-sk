---
title: Prehľad riadkov zmlúv založených na produkte – čiastočné
description: Táto téma poskytuje informácie o riadkoch zmluvy založenej na produkte.
author: rumant
ms.date: 10/07/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 8006e90e0d4fdf02042f26b261775a92f87f47ca
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598231"
---
# <a name="product-based-contract-lines-overview---lite"></a>Prehľad riadkov zmlúv založených na produkte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Môžete vytvoriť riadky zmlúv v Dynamics 365 Project Operations. Produktové riadky zmlúv môžu byť manuálne vytvorenými riadkami alebo môžu byť položkami z katalógu produktov.

## <a name="product-catalog"></a>Katalóg produktov

Produkty v katalógu produktov majú predvolenú jednotku a jednotkovú skupinu. Ak niekoľko produktov zdieľa rovnakú množinu atribútov, môžete vytvoriť produktovú rodinu, ktorá má tiež tieto atribúty. Všetky produkty v jednej produktovej rodine zdedia rovnakú množinu atribútov.

Spoločnosť napríklad predáva licencie na predplatné pre rôzne druhy softvéru. Všetky predplatné softvéry májú nasledujúce dva atribúty:

- Počet používateľov
- Trvanie predplatného (v mesiacoch)

Ak chcete zachovať tento typ katalógu, vytvorte rodinu produktov s názvom **Predplatený softvér**. Pridajte atribúty **Počet používateľov** a **Trvanie predplatného** do rodiny výrobkov. Potom pridajte jednotlivé produkty do produktovej rodiny **Predplatený softvér**.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Pridanie položiek katalógu produktov k projektovej zmluve

Projektové zmluvy majú sekcie pre dva typy riadkov: riadky založené na projekte a založené na produkte. Produktové rady zahŕňajú všetky produkty a jednotky uvedené v cenníku produktov na zmluve. Možno pridávať produkty, ktoré nie sú súčasťou produktového cenníka zmluvy.

Produkty si môžete vybrať z iných cenníkov alebo priamo z produktového katalógu. Keď vyberiete produkty priamo z katalógu produktov, na získanie predajnej ceny produktu sa použije predvolený cenník daného produktu. Ak predvolený cenník nie je nastavený, cena je nastavená na hodnotu 0 (nula).

Ak je riadok zmluvy založený na katalógu produktov, predajnú cenu môžete prepísať priamo v riadku. Riadok zmluvy disponuje poľom **Tvorba ceny** s dvomi hodnotami:

- **Prepíšte cenu**
- **Použiť predvolenú hodnotu**

Ak nastavíte toto pole **Tvorba ceny** na **Prepísať cenu**, predvolená cena sa nenastaví. Do riadka zmluvy zadajte cenu produktu. Ak nastavíte pole na **Použiť predvolené**, použije sa predvolená predajná cena a pole nebude možné upraviť.

Po nainštalovaní Project Operations sa predvolené predajné ceny zapisujú do riadkov na základe zmluvy. Pole **Ceny** sa potom nastaví na **Prepíšte cenu**, aby ste mohli upraviť predvolenú cenu v riadkoch zmluvy. Toto je špecifické prepísanie v rámci Project Operations na produktoch v aplikácii Dynamics 365 Sales.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]