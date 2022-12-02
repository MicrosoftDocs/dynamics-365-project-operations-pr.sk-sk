---
title: Riadky faktúr dodávateľov pre kategórie výdavkov
description: Tento článok vysvetľuje, ako zaznamenať riadky faktúry dodávateľa pre kategórie výdavkov.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261719"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Riadky faktúr dodávateľov pre kategórie výdavkov

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Faktúra dodávateľa v Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa pre kategórie výdavkov. Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre kategórie výdavkov na zaznamenanie nákladov na služby, ktoré sú obstarané ako kategórie výdavkov.

Riadky faktúry dodávateľa pre kategórie výdavkov môžu alebo nemusia odkazovať na riadok subdodávateľskej zmluvy pre kategórie výdavkov. Ak riadok faktúry dodávateľa pre kategórie výdavkov odkazuje na subdodávateľskú zmluvu, projektoví manažéri budú môcť porovnať a overiť výdavky, ktoré sú fakturované riadkom faktúry dodávateľa, s výdavkami, ktoré sú zaznamenané v týchto kategóriách výdavkov a schválené projektovými manažérmi na projekte.

Nasledujúca tabuľka poskytuje informácie o poliach na riadku faktúry dodávateľa pre kategórie výdavkov.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadka faktúry dodávateľa, ktorý má pomôcť s identifikáciou. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúr dodávateľov. |
| Description | Stručný opis služieb, ktoré dodávateľ fakturuje na riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávateľská zmluva, na základe ktorej boli služby pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávateľská zmluva, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávateľské zmluvy. |
| Riadok subdodávateľskej zmluvy | Riadok subdodávateľskej zmluvy, na základe ktorého boli služby objednané. Zoznam riadkov subdodávateľských zmlúv, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávateľskej zmluve. | Keď je vybratý riadok subdodávateľskej zmluvy na riadku faktúry dodávateľa pre kategórie výdavkov, predvolené hodnoty pre polia **Projekt**, **Úloha**, a **Kategória transakcie** sa zadávajú z príslušných polí v riadku subdodávateľskej zmluvy. Ak má vybraný riadok subdodávateľskej zmluvy hodnoty v poliach **Projekt**, **Projektová úloha**, a **Kategória transakcie**, hodnoty zodpovedajúcich polí v riadku faktúry dodávateľa sa nemôžu líšiť od týchto hodnôt. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. |None |
| Trieda transakcie | Vyberte **Výdavok** na zaznamenanie faktúry dodávateľa pre kategóriu výdavkov. | Hodnota **Výdavok** označuje, že riadok faktúry dodávateľa sa používa na zaznamenanie sumy faktúry za služby, ktoré boli obstarané ako kategórie výdavkov. |
| Project | Názov projektu, v rámci ktorého boli fakturované služby použité. | Toto pole je povinné a nemôže ostať prázdne. |
| Úloha | Názov projektovej úlohy, v rámci ktorého boli fakturované služby použité. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry dodávateľa k výdavkom, ktoré sú zaznamenané pri akejkoľvek úlohe projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávateľskej zmluvy a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia podľa úloh, nemusí byť možné náklady fakturovať koncovému zákazníkovi. |
| Kategória transakcie | Kategória transakcie, ktorá sa fakturuje. Pre vybratú kategóriu transakcií musí byť vytvorená zodpovedajúca kategória výdavkov. | Kombinácia hodnôt **Kategória transakcie** a **Jednotka** budú použité ako predvolená alebo vypočítaná hodnota pre pole **Jednotková cena** na riadku faktúry dodávateľa. |
| Množstvo | Do riadku faktúry zadajte množstvo, ktoré fakturuje dodávateľ. |None|
| Jednotková skupina | Zadá sa predvolená hodnota založená na jednotkovej skupine vybranej kategórie transakcie. | None |
| Jednotka | Predvolená hodnota v základnej jednotke jednotkovej skupiny, ktorá je vybraná. Túto hodnotu môžete zmeniť, aby ste si mohli kúpiť akúkoľvek jednotku jednotkovej skupiny. | Kombinácia hodnôt **Kategória transakcie** a **Jednotka** budú použité ako predvolená alebo vypočítaná hodnota pre pole **Jednotková cena** na riadku faktúry dodávateľa. |
| Jednotková cena | Predvolená jednotková cena používa kombináciu hodnôt **Kategória transakcie** a **Jednotka** z cenníka projektu, ktorý sa vzťahuje na dátum transakcie riadku faktúry dodávateľa. | Ak je cena pre príslušný cenník projektu nastavená v jednotke, ktorá sa líši od jednotky na riadku faktúry dodávateľa, systém použije na výpočet jednotkovej ceny konverziu jednotky. |
| Medzisúčet | Toto pole určené len na čítanie sa vypočíta ako *Množstvo* &times; *Jednotková cena*, ak sú hodnoty zadané v poli **Množstvo** aj v poli **Jednotková cena**. Ak sú jedno alebo obe tieto polia prázdne, môžete do tohto poľa zadať hodnotu.| None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková čiastka | Celková čiastka riadka faktúry dodávateľa vrátane daní. Toto pole sa počíta ako *Medzisúčet* + *Daň z predaja*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
