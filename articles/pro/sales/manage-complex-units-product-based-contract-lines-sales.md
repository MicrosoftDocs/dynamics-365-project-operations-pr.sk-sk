---
title: Správa komplexných jednotiek pre riadky zmlúv založených na produkte – čiastočné
description: Tento článok poskytuje informácie o podpore predaja produktov založených na predplatnom.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f48ac31778e34ace79dbce74cff752343484e5a5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919941"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a>Správa komplexných jednotiek pre riadky zmlúv založených na produkte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations používa množstvo faktorov na podporu predaja produktov založených na predplatnom. V prípade produktov založených na predplatnom sa množstvo v riadku zmluvy alebo projektu vyjadrí ako počet používateľských mesiacov.

Cena predplatného softvéru je uložená v katalógu ako cena za používateľa mesačne. Počas predajného procesu je cena v riadku zmluvy zvyčajne cena za používateľa, za mesiac, ktorá bola dohodnutá a zľavnená agentom predaja. Každý obchod má iný počet užívateľov a iný počet predplatných mesiacov. Množstvo, ktoré sa používa na výpočet čiastky riadka zmluvy, je produktom počtu používateľov a počtu mesiacov predplatného.

Na podporu tohto druhu predaja, podporuje Project Operations koncept *faktorov kvantity*. Faktory kvantity sa spoliehajú na atribúty produktov. Keď nakonfigurujete špecifické vlastnosti produktu, môžete označiť podmnožinu týchto vlastností alebo všetky vlastnosti ako faktory kvantity.

Project Operations overuje, že iba číselné vlastnosti alebo vlastnosti produktu, ktoré majú číselný typ údajov, sú označené ako faktory kvantity. Keď sa produkt s nakonfigurovanými faktormi kvantity pridá do riadku zmluvy, pole **Množstvo** sa zmení iba na čítanie. Po zadaní hodnôt pre vlastnosti produktu, ktoré sú faktormi kvantity, Project Operations vypočíta množstvo riadka zmluvy.

Napríklad, Dynamics 365 Sales môže mať nasledujúce vlastnosti:

- **Počet používateľov**: Počet používateľov.
- **Počet mesiacov**: Počet mesiacov predplatného.
- **SKU produktu**: Skladová jednotka (SKU) pre produkt.

Vlastnosti **Počet používateľov** a **Počet mesiacov** môžu byť označené ako faktory kvantity úpravou vlastnosti produktového riadku.

Ak chcete z vlastností produktu vytvoriť faktory množstva, vykonajte nasledujúce kroky.

1. V časti **Project Operations** vyberte **Predajné produkty**.
2. Otvorte produkt, pre ktorý potrebujete nastaviť faktory kvantity. Skontrolujte, či má produkt už nastavené vlastnosti.
3. Na stránke **Informácie o projekte** vyberte kartu **Faktory kvantity**.
4. Vo vedľajšej mriežke vyberte **+ Výpočet nového poľa**.
5. Zadajte názov **Faktora kvantity** a vyberte hodnotu vlastnosti, ktorá sa mapuje na výpočet poľa.
6. Uloží a zavrie formulár.
7. Opakujte kroky 2 až 6 pre všetky vlastnosti, ktoré spolu tvoria kvantitu riadok zmluvy založenej na produkte.

Keď sú nastavené faktory kvantity, keď používateľ vytvorí pre tento produkt riadok zmluvy, kvantita riadka zmluvy sa uzamkne. Kvantita sa potom vypočíta ako súčin hodnôt vlastností pre daný riadok zmluvy.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]