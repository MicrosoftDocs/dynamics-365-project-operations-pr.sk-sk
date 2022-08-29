---
title: Riadky faktúr dodávateľov pre produkty
description: Tento článok vysvetľuje, ako zaznamenať riadky faktúry dodávateľa pre produkty a ako použiť rôzne polia na zaznamenanie nákupov produktov od dodávateľov.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261578"
---
# <a name="vendor-invoice-lines-for-products"></a>Riadky faktúr dodávateľov pre produkty

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Faktúra dodávateľa v spoločnosti Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa pre produkty (tiež označované ako materiály). Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre produkty na zaznamenanie nákladov na produkty, ktoré boli zakúpené v rámci projektov.

Riadky faktúry dodávateľa za produkty môžu alebo nemusia odkazovať na riadok subdodávok pre materiály. Ak riadok faktúry dodávateľa pre produkty odkazuje na subdodávku, projektoví manažéri budú môcť spárovať a overiť produkty, ktoré sú fakturované riadkom faktúry dodávateľa, s použitím zakúpených produktov, ktoré sú zaznamenané a schválené projektovými manažérmi.

Nasledujúca tabuľka poskytuje informácie o poliach v riadkoch faktúry dodávateľa pre produkty.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadku faktúry dodávateľa na uľahčenie identifikácie. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúry dodávateľa. |
| Description | Stručný popis produktov, ktoré sú fakturované dodávateľom v riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávka, na základe ktorej boli produkty pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávka, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávky. |
| Subdodávateľská linka | Subdodávateľská linka, na ktorej boli produkty objednané. Zoznam riadkov subdodávok, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávke. | Keď je v riadku faktúry dodávateľa pre produkty vybratý riadok subdodávok, predvolené hodnoty pre **Projekt**, **·**, a **Produkt** polia sa zadávajú z príslušných polí v riadku subdodávky. Ak má vybraný riadok subdodávky hodnoty v **Projekt**, **·**, a **Produkt** hodnoty zodpovedajúcich polí v riadku faktúry dodávateľa sa nemôžu líšiť od týchto hodnôt. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. | None|
| Trieda transakcie | Keď sú produkty fakturované, toto pole by malo byť nastavené na **Materiál**. | Hodnota **Materiál** označuje, že riadok faktúry dodávateľa sa používa na zaznamenanie sumy faktúry za materiál, ktorý bol zakúpený. |
| Project | Názov projektu, v ktorom boli použité produkty, ktoré sú fakturované. | Toto pole je povinné a nemôže zostať prázdne. |
| Úloha | Názov projektovej úlohy, na ktorú boli použité produkty, ktoré sú fakturované. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry dodávateľa k zakúpenému produktu, ktorý sa používa na ľubovoľnú úlohu projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávky a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia podľa úloh, náklady nebude možné fakturovať koncovému zákazníkovi. |
| Vybrať produkt | Vyberte, či je produkt, ktorý sa fakturuje, existujúci produkt z katalógu alebo produkt so zápisom. | Predvolená hodnota sa zadáva z riadku subdodávky, keď je vybratý riadok subdodávky. |
| Produkt | Vyberte si produkt z katalógu. Ak ide o produkt na zápis, zadajte názov produktu. | Toto pole sa používa na zadanie predvolených nákupných cien pre existujúce produkty. |
| Množstvo | V tomto riadku faktúry zadajte množstvo materiálu, ktoré fakturuje dodávateľ. | None |
| Jednotková skupina | Vyberte skupinu jednotiek jednotky, v ktorej je vyjadrené množstvo, ktoré sa fakturuje. | None |
| Jednotka | Predvolená hodnota je základná jednotka zvolenej skupiny jednotiek. Túto hodnotu môžete zmeniť, aby ste platili v ľubovoľnej jednotke vybranej skupiny jednotiek. | Kombinácia **Produkt** a **Jednotka** hodnoty sa použijú ako predvolená alebo vypočítaná hodnota pre **Jednotková cena** v riadku faktúry dodávateľa. |
| Jednotková cena | Predvolená jednotková cena používa kombináciu **Produkt** a **Jednotka** hodnoty z cenníka projektu, ktorý sa vzťahuje na dátum transakcie riadku faktúry dodávateľa. | None |
| Medzisúčet | Toto pole len na čítanie sa vypočíta ako *Množstvo*&times;*Jednotková cena*, ak sú hodnoty zadané v oboch **Množstvo** pole a **Jednotková cena** lúka. Ak sú jedno alebo obe polia prázdne, môžete do tohto poľa zadať hodnotu. | None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková suma | Celková suma riadku faktúry dodávateľa vrátane daní. Toto pole sa vypočíta ako *Medzisúčet* + *Daň z predaja*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
