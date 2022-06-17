---
title: Správa komplexných jednotiek, napríklad podľa používateľa alebo podľa mesiaca, pre riadky cenových ponúk založených na produkte – čiastočné
description: Tento článok poskytuje informácie o správe zložitých jednotiek pre cenové ponuky založené na produktoch.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 88173468cd2e898331c4aa0a398792d9a0f3df10
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929923"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a>Správa komplexných jednotiek, napríklad podľa používateľa alebo podľa mesiaca, pre riadky cenových ponúk založených na produkte – čiastočné

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Dynamics 365 Project Operations používa množstvo faktorov na podporu predaja produktov založených na predplatnom. V prípade produktov založených na predplatnom sa množstvo v riadku cenovej ponuky alebo projektu vyjadrí ako počet používateľských mesiacov.

Zvyčajne je cena predplatného softvéru uložená v katalógu ako cena za používateľa mesačne. Počas predajného procesu je cena v riadku cenovej ponuky zvyčajne cena za používateľa, za mesiac, ktorá bola dohodnutá a zľavnená agentom predaja IT. Každý obchod má iný počet užívateľov a iný počet predplatných mesiacov. Množstvo používané na výpočet riadka cenovej ponuky je násobkom počtu používateľov a počtu mesiacov predplatného.

Na podporu tohto druhu predaja, Project Operations predstavil koncept kvantity faktorov. Množstvo faktorov sa spolieha na atribúty v Dynamics 365. Keď nakonfigurujete špecifické vlastnosti produktu, Project Operations vám umožní označiť podmnožinu alebo všetky vlastnosti ako množstevné faktory.

Project Operations overuje, že iba číselné vlastnosti alebo vlastnosti produktu, ktoré majú číselný typ údajov, sú označené ako faktory kvantity. Keď do riadku cenovej ponuky pridáte produkt s faktormi kvantity, pole **Množstvo** bude iba na čítanie. Po zadaní hodnôt pre vlastnosti produktu, ktoré sú faktory kvantity, Project Operations vypočíta množstvo riadka cenovej ponuky.

Napríklad, Dynamics 365 Sales môže mať nasledujúce vlastnosti:

- **Počet používateľov**: Počet používateľov
- **Počet mesiacov**: Počet mesiacov predplatného
- **Produkt SKU**

Vlastnosti **Počet používateľov** a **Počet mesiacov** môžete označiť príznakom ako faktory kvantity úpravou vlastnosti produktového riadku.

Ak chcete vytvoriť faktory kvantity z vlastností produktu, postupujte nasledovne:

1. Na ľavej navigačnej table Project Operations prejdite na **Predaj** > **Produkty**.
2. Otvorte produkt, pre ktorý potrebujete nakonfigurovať faktory kvantity. Skontrolujte, či má produkt už nakonfigurované vlastnosti.
3. Na stránke **Informácie o projekte** pre produkt vyberte kartu **Faktory kvantity**.
4. Vo vedľajšej mriežke vyberte **+ Výpočet nového poľa**.
5. Zadajte názov faktora kvantity a vyberte hodnotu vlastnosti, ktorá sa mapuje na výpočet poľa.
6. Uloží a zavrie formulár. Zopakujte tieto kroky pre všetky vlastnosti, ktoré sa majú použiť na výpočet množstva pre riadok cenovej ponuky založenej na produkte.

Keď vytvoríte riadok cenovej ponuky založenej na produkte pre produkt, množstvo riadka cenovej ponuky sa uzamkne. Množstvo sa vypočíta ako súčin hodnôt vlastností, ktoré zadáte pre daný riadok cenovej ponuky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]