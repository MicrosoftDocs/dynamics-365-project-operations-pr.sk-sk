---
title: Riadky faktúry dodávateľa pre kategórie výdavkov
description: Táto téma vysvetľuje, ako zaznamenať riadky faktúry dodávateľa pre kategórie výdavkov.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 209460680c9e5c2e39f98ba5c48aa18992775db1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: sk-SK
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579555"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Riadky faktúry dodávateľa pre kategórie výdavkov

[!include [banner](../../includes/dataverse-preview.md)]

_**Platí pre:** Čiastočné nasadenie – dohoda o fakturácii pro forma_

Faktúra dodávateľa v spoločnosti Microsoft Dynamics 365 Project Operations môže mať riadky faktúry dodávateľa pre kategórie výdavkov. Projektoví manažéri môžu použiť riadky faktúry dodávateľa pre kategórie výdavkov na zaznamenanie nákladov na služby, ktoré sú obstarané ako kategórie výdavkov.

Riadky faktúry dodávateľa pre kategórie výdavkov môžu alebo nemusia odkazovať na riadok subdodávok pre kategórie výdavkov. Ak riadok faktúry dodávateľa pre kategórie výdavkov odkazuje na subdodávku, projektoví manažéri budú môcť porovnať a overiť výdavky, ktoré sú fakturované riadkom faktúry dodávateľa, s výdavkami, ktoré sú zaznamenané v týchto kategóriách výdavkov a schválené projektovými manažérmi na projekte.

Nasledujúca tabuľka poskytuje informácie o poliach na riadkoch faktúry dodávateľa pre kategórie výdavkov.

| Pole | Description | Funkčný vplyv |
| --- | --- | --- |
| Name | Názov riadku faktúry dodávateľa na uľahčenie identifikácie. | Tento názov sa zobrazí ako prvý stĺpec vo všetkých vyhľadávaniach, ktoré sú založené na riadkoch faktúry dodávateľa. |
| Description | Stručný popis služieb, ktoré sú fakturované dodávateľom v riadku faktúry dodávateľa. | None |
| Subdodávateľská zmluva | Subdodávateľská zmluva, na základe ktorej boli služby pôvodne objednané. | Keď je pre faktúru dodávateľa vybratá subdodávka, všetky riadky na faktúre dodávateľa zdedia tento výber. Faktúra dodávateľa nemôže obsahovať riadky faktúry dodávateľa, ktoré odkazujú na rôzne subdodávky. |
| Subdodávateľská linka | Subdodávateľská linka, na ktorej boli služby objednané. Zoznam riadkov subdodávok, ktoré je možné vybrať, je obmedzený na riadky vo vybranej subdodávke. | Keď je vybratý riadok subdodávky na riadku faktúry dodávateľa pre kategórie výdavkov, predvolené hodnoty pre **Projekt**, **a** **Kategória transakcie** polia sa zadávajú z príslušných polí v riadku subdodávky. Ak má vybraný riadok subdodávky hodnoty v **Projekt**, **úloha** a **Kategória transakcie** hodnoty zodpovedajúcich polí v riadku faktúry dodávateľa sa nemôžu líšiť od týchto hodnôt. |
| Dátum transakcie | Dátum, kedy budú skutočné náklady riadku faktúry dodávateľa zaznamenané v projekte. |None |
| Trieda transakcie | Vyberte **Výdavok** na zaznamenanie faktúry dodávateľa pre kategóriu nákladov. | Hodnota **Výdavok** označuje, že riadok faktúry dodávateľa sa používa na zaznamenanie sumy faktúry za služby, ktoré boli obstarané ako kategórie nákladov. |
| Project | Názov projektu, na ktorý sa použili fakturované služby. | Toto pole je povinné a nemôže zostať prázdne. |
| Úloha | Názov projektovej úlohy, na ktorú boli použité služby, ktoré sú fakturované. Toto pole je dostupné len vtedy, ak je vybratý projekt. Výber projektovej úlohy je voliteľný. | Ak toto pole ponecháte prázdne, projektový manažér môže priradiť riadok faktúry dodávateľa k výdavkom, ktoré sú zaznamenané pri akejkoľvek úlohe projektu. Ak riadok faktúry dodávateľa neodkazuje na riadok subdodávky a toto pole zostane prázdne, skutočné náklady vytvorené riadkom faktúry dodávateľa nebudú prepojené so žiadnymi skutočnými nevyfakturovanými predajmi. V tomto prípade, ak je nastavená fakturácia na základe úloh, nemusí byť možné náklady fakturovať koncovému zákazníkovi. |
| Kategória transakcie | Kategória transakcie, ktorá sa fakturuje. Pre zvolenú kategóriu transakcií musí byť vytvorená zodpovedajúca kategória výdavkov. | Kombinácia **Kategória transakcie** a **Jednotka** hodnoty sa použijú ako predvolená alebo vypočítaná hodnota pre **Jednotková cena** v riadku faktúry dodávateľa. |
| Množstvo | Do riadku faktúry zadajte množstvo, ktoré fakturuje dodávateľ. |None|
| Jednotková skupina | Predvolená hodnota sa zadáva na základe skupiny jednotiek vybranej kategórie transakcií. | None |
| Jednotka | Predvolená hodnota je základná jednotka zvolenej skupiny jednotiek. Túto hodnotu môžete zmeniť na nákup v akejkoľvek jednotke skupiny jednotiek. | Kombinácia **Kategória transakcie** a **Jednotka** hodnoty sa použijú ako predvolená alebo vypočítaná hodnota pre **Jednotková cena** v riadku faktúry dodávateľa. |
| Jednotková cena | Predvolená jednotková cena používa kombináciu **Kategória transakcie** a **Jednotka** hodnoty z cenníka projektu, ktorý sa vzťahuje na dátum transakcie riadku faktúry dodávateľa. | Ak je cena pre príslušný projektový cenník nastavená v jednotke, ktorá sa líši od jednotky na riadku faktúry dodávateľa, systém použije prepočet jednotiek na výpočet jednotkovej ceny. |
| Medzisúčet | Toto pole len na čítanie sa vypočíta ako *množstvo*&times;*Jednotková cena*, ak sú hodnoty zadané v oboch **množstvo** pole a **Jednotková cena** lúka. Ak sú jedno alebo obe polia prázdne, môžete do tohto poľa zadať hodnotu.| None |
| Daň z predaja | Zadajte sumu dane z predaja. | None |
| Celková suma | Celková suma riadku faktúry dodávateľa vrátane daní. Toto pole sa vypočíta ako *Medzisúčet* + *Daň z predaja*. | None |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
