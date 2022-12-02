---
title: Riadky faktúr dodávateľov pre produkty
description: Tento článok vysvetľuje, ako zaznamenávať riadky faktúry dodávateľa pre produkty a používať rôzne polia na zaznamenávanie nákupov produktov od dodávateľov.
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

Faktúra dodávateľa v Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa pre produkty (tiež označované ako materiály). Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre produkty na zaznamenanie nákladov na produkty, ktoré boli zakúpené v rámci projektov.

Riadky faktúry dodávateľa pre produkty môžu alebo nemusia odkazovať na riadok subdodávateľskej zmluvy pre materiály. Ak riadok faktúry dodávateľa pre produkty odkazuje na subdodávateľskú zmluvu, projektoví manažéri budú môcť porovnať a overiť produkty, ktoré sú fakturované riadkom faktúry dodávateľa, so zakúpenými produktmi, ktoré sú zaznamenané a schválené projektovými manažérmi na projekte.

Nasledujúca tabuľka poskytuje informácie o poliach na riadku faktúry dodávateľa pre produkty.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadka faktúry dodávateľa, ktorý má pomôcť s identifikáciou. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúr dodávateľov. |
| Description | Stručný opis produktov, ktoré dodávateľ fakturuje na riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávateľská zmluva, na základe ktorej boli produkty pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávateľská zmluva, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávateľské zmluvy. |
| Riadok subdodávateľskej zmluvy | Riadok subdodávateľskej zmluvy, na základe ktorého boli produkty objednané. Zoznam riadkov subdodávateľských zmlúv, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávateľskej zmluve. | Keď je vybratý riadok subdodávateľskej zmluvy na riadku faktúry dodávateľa pre produkty, predvolené hodnoty pre polia **Projekt**, **Úloha**, a **Produkt** sa zadávajú z príslušných polí v riadku subdodávateľskej zmluvy. Ak má vybraný riadok subdodávateľskej zmluvy hodnoty v poliach **Projekt**, **Úloha** a **Produkt**, hodnoty zodpovedajúcich polí v riadku faktúry dodávateľa sa nemôžu líšiť od týchto hodnôt. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. | None|
| Trieda transakcie | Keď sú produkty fakturované, toto pole by malo byť nastavené na **Materiál**. | Hodnota **Materiál** označuje, že riadok faktúry dodávateľa sa používa na zaznamenanie sumy faktúry za materiály, ktoré boli zakúpené. |
| Project | Názov projektu, v rámci ktorého boli fakturované produkty použité. | Toto pole je povinné a nemôže ostať prázdne. |
| Úloha | Názov úlohy projektu, v rámci ktorého boli fakturované produkty použité. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry k zakúpenému produktu, ktorý sa používa pri akejkoľvek úlohe projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávateľskej zmluvy a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia podľa úloh, nie je možné náklady fakturovať koncovému zákazníkovi. |
| Vybrať produkt | Vyberte, či je fakturovaný produkt existujúcim produktom z katalógu alebo produktom nezahrnutým do katalógu. | Predvolená hodnota sa zadáva z riadku subdodávateľskej zmluvy, keď je vybratý riadok subdodávateľskej zmluvy. |
| Produkt | Vyberte produkt z katalógu. Ak je produkt produktom nezahrnutým do katalógu, zadajte názov produktu. | Toto pole sa používa na zadanie predvolených nákupných cien pre existujúce produkty. |
| Množstvo | Do riadku tejto faktúry zadajte množstvo materiálu, ktoré fakturuje dodávateľ. | None |
| Jednotková skupina | Vyberte jednotkovú skupinu jednotiek, v ktorej je vyjadrené množstvo, ktoré sa fakturuje. | None |
| Jednotka | Predvolená hodnota v základnej jednotke jednotkovej skupiny, ktorá je vybraná. Túto hodnotu môžete zmeniť, aby ste si mohli zaplatiť akúkoľvek jednotku vybranej jednotkovej skupiny. | Kombinácia hodnôt **Produkt** a **Jednotka** budú použité ako predvolená alebo vypočítaná hodnota pre pole **Jednotková cena** na riadku faktúry dodávateľa. |
| Jednotková cena | Predvolená jednotková cena používa kombináciu hodnôt **Produkt** a **Jednotka** z cenníka projektu, ktorý sa vzťahuje na dátum transakcie riadku faktúry dodávateľa. | None |
| Medzisúčet | Toto pole určené len na čítanie sa vypočíta ako *Množstvo* &times; *Jednotková cena*, ak sú hodnoty zadané v poli **Množstvo** aj v poli **Jednotková cena**. Ak sú jedno alebo obe tieto polia prázdne, môžete do tohto poľa zadať hodnotu. | None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková čiastka | Celková čiastka riadka faktúry dodávateľa vrátane daní. Toto pole sa počíta ako *Medzisúčet* + *Daň z predaja*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
