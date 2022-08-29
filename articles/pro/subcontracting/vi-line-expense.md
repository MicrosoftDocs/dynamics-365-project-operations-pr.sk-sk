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

Faktúra dodávateľa v spoločnosti Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa pre kategórie výdavkov. Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre kategórie výdavkov na zaznamenanie nákladov na služby, ktoré sú obstarané ako kategórie výdavkov.

Riadky faktúry dodávateľa pre kategórie výdavkov môžu alebo nemusia odkazovať na riadok subdodávok pre kategórie výdavkov. Ak riadok faktúry dodávateľa pre kategórie výdavkov odkazuje na subdodávku, projektoví manažéri budú môcť porovnať a overiť výdavky, ktoré sú fakturované riadkom faktúry dodávateľa, s výdavkami, ktoré sú zaznamenané v týchto kategóriách výdavkov a schválené projektovými manažérmi na projekte.

Nasledujúca tabuľka poskytuje informácie o poliach na riadkoch faktúry dodávateľa pre kategórie výdavkov.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadku faktúry dodávateľa na uľahčenie identifikácie. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúry dodávateľa. |
| Description | Stručný popis služieb, ktoré sú fakturované dodávateľom v riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávka, na základe ktorej boli služby pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávka, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávky. |
| Subdodávateľská linka | Subdodávateľská linka, na ktorej boli služby objednané. Zoznam riadkov subdodávok, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávke. | Keď je vybratý riadok subdodávky na riadku faktúry dodávateľa pre kategórie výdavkov, predvolené hodnoty pre **Projekt**, **·**, a **Kategória transakcie** polia sa zadávajú z príslušných polí v riadku subdodávky. Ak má vybraný riadok subdodávky hodnoty v **Projekt**, **úloha**, a **Kategória transakcie** hodnoty zodpovedajúcich polí v riadku faktúry dodávateľa sa nemôžu líšiť od týchto hodnôt. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. |None |
| Trieda transakcie | Vyberte **Výdavok** na zaznamenanie faktúry dodávateľa pre kategóriu nákladov. | Hodnota **Výdavok** označuje, že riadok faktúry dodávateľa sa používa na zaznamenanie sumy faktúry za služby, ktoré boli obstarané ako kategórie nákladov. |
| Project | Názov projektu, na ktorý boli použité služby, ktoré sú fakturované. | Toto pole je povinné a nemôže zostať prázdne. |
| Úloha | Názov projektovej úlohy, na ktorú sa použili fakturované služby. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry dodávateľa k výdavkom, ktoré sú zaznamenané pri akejkoľvek úlohe projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávky a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia podľa úloh, nemusí byť možné náklady fakturovať koncovému zákazníkovi. |
| Kategória transakcie | Kategória transakcie, ktorá sa fakturuje. Pre vybratú kategóriu transakcií musí byť vytvorená zodpovedajúca kategória výdavkov. | Kombinácia **Kategória transakcie** a **Jednotka** hodnoty sa použijú ako predvolená alebo vypočítaná hodnota pre **Jednotková cena** v riadku faktúry dodávateľa. |
| Množstvo | Do riadku faktúry zadajte množstvo, ktoré fakturuje dodávateľ. |None|
| Jednotková skupina | Predvolená hodnota sa zadáva na základe skupiny jednotiek vybranej kategórie transakcií. | None |
| Jednotka | Predvolená hodnota je základná jednotka zvolenej skupiny jednotiek. Túto hodnotu môžete zmeniť na nákup v akejkoľvek jednotke skupiny jednotiek. | Kombinácia **Kategória transakcie** a **Jednotka** hodnoty sa použijú ako predvolená alebo vypočítaná hodnota pre **Jednotková cena** v riadku faktúry dodávateľa. |
| Jednotková cena | Predvolená jednotková cena používa kombináciu **Kategória transakcie** a **Jednotka** hodnoty z cenníka projektu, ktorý sa vzťahuje na dátum transakcie riadku faktúry dodávateľa. | Ak je cena pre príslušný projektový cenník nastavená v jednotke, ktorá sa líši od jednotky na riadku faktúry dodávateľa, systém použije na výpočet jednotkovej ceny konverziu jednotiek. |
| Medzisúčet | Toto pole len na čítanie sa vypočíta ako *Množstvo*&times;*Jednotková cena*, ak sú hodnoty zadané v oboch **Množstvo** pole a **Jednotková cena** lúka. Ak sú jedno alebo obe polia prázdne, môžete do tohto poľa zadať hodnotu.| None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková suma | Celková suma riadku faktúry dodávateľa vrátane daní. Toto pole sa vypočíta ako *Medzisúčet* + *Daň z predaja*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
